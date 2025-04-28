# Online-Hausarbeit 1: Build a Solar System

> Bearbeitungszeitraum: 06.07.2020 00:00 Uhr - 10.07.2020 23:59Uhr
>
> Computer Graphics 1 - Summer Semester 2020 - LMU Munich

To report your implemented features, please check the items in the [Feature List](#feature-list) section. For instance:

- [ ] This is an unchecked item
- [x] This is a checked item

## Feature List (50p)

1. create the skystar background **(total: 5p)**
   - [x] use the given params `this.params.universe.radius`, and `this.params.segment` for geometry (1p)
   - [x] use the texture from `this.params.universe.texture` as the background material for the starry sky (1p)
   - [x] reduce a possible blur effect occuring for the background in all directions (1p)
   - [x] create the background 3D object (1p)
   - [x] then add it to the scene graph (1p)

2. create a sun as the center of the solar system **(total: 5p)**
   - [x] use the given params: `this.params.sun.radius`, and `this.params.segment` for geometry (1p)
   - [x] use the texture from `this.params.sun.texture` as the sun material (1p)
   - [x] reduce a possible blur effect occuring at the poles (1p)
   - [x] create the 3D sun object and assign to `this.sun` (1p)
   - [x] then add it to the scene graph (1p)

3. create light to simulate the sun illumination **(total: 2p)**
   - [x] create a point light using the given params in `this.params.sun.light` (1p)
   - [x] create ambient light using the given params in `this.params.sun.light` (1p)

4. create the eight planets using provided textures, and move them with a given distance to the sun **(total: 7p)**
   - [x] use the given params in `this.params.planets.<name>.radius`, `this.params.segment` for the planet geometry (1p)
   - [x] use the texture from `this.params.planets.<name>.texture` then create the correct material to show the phong illumination model (1p)
   - [x] reduce a possible blur effect occuring at the poles (1p)
   - [x] move each planet around the sun with a given distance (`this.params.planets.<name>.distance`) (1p)
   - [x] create each planet and assign them to `this.planets.<name>.planet` (2p)
   - [x] then add eight of them to the scene graph (1p)

5. draw a (circular) orbit for each planet **(total: 7p)**
   - [x] use the given params in `this.params.planets.<name>.distance`, `this.params.segment` for the circle geometry (1p)
   - [x] use the given params in `this.params.orbit` then create the line basic material (1p)
   - [x] create each orbit and assign them to `this.planets.<name>.orbit` (2p)
   - [x] then add eight of them to the scene graph (1p)
   - [x] transform each orbit and place it in x-z plane (1p)
   - [x] manipulate the vertices to guarantee the orbit is drawn as a closed circle (1p)

6. create the moon and its orbit **(total: 6p)**
   - [x] create the moon and assign the 3D moon object to `this.planets.earth.moon.planet` using the given params (`this.params.planets.earth.moon`, `this.params.segment`). The moon's material should show the phong illumination model (1p)
   - [x] set the moon to the correct position with a distance (`this.params.planets.earth.moon.distance`) to the earth (1p)
   - [x] add the moon to the scene graph (1p)
   - [x] create the moon orbit and assign it to `this.planets.earth.moon.orbit` using the given params `this.params.planets.earth.moon.distance` and `this.params.orbit` (1p)
   - [x] transform the moon's orbit that is located around the earth in x-z plane, make sure the orbit is drawed in a closed circle (1p)
   - [x] add the moon's orbit to the scene graph (1p)

7. create the saturn ring and apply corresponing texture mapping with a customized fragment shader **(total: 8p)**
   - [x] use the given params `this.params.planets.saturn.ring` to create the saturn ring using ring geometry and a shader material then assign it to `this.planets.saturn.ring` (1p)
   - [x] make sure the saturn ring is rendered on both sides (1p)
   - [x] pass the needed uniforms to the customized shaders (1p)
   - [x] write a customized vertex shader that passes the position to fragment shader(`src/shaders/saturn_ring.vs.glsl`) (1p)
   - [x] write a customized fragment shader that performs the UV mapping (`src/shaders/saturn_ring.fs.glsl`) (2p)
   - [x] transform the saturn ring so that is located around the saturn and that it is rotating around x axis with the given angle in `this.params.planets.saturn.ring` and make sure the orbit is drawn in a closed circle (1p)
   - [x] add the saturn ring to the scene graph (1p)

8. add self rotation to the sun **(total: 1p)**
   - [x] use the given params `this.params.sun.selfRotate` and add self rotation to the sun around the y-axis. The given parameter is the rotation angle (radians) of each frame. (1p)

9. add self rotation to the eight planets **(total: 2p)**
   - [x] use the given params `this.params.planets.<name>.selfRotate` and add self rotation to each planet around y-axis. The given parameters are the rotation angle (radians) of each frame. (2p)

10. add revolution to the eight planets **(total: 3p)**
    - [x] use the given params `this.params.planets.<name>.revolution` and add revolution (2p)
    - [x] to each planet (1p) that rotates around the sun.

1.  add self rotation and revolution to the moon **(total: 3p)**
    - [x] use the given params `this.params.planets.earth.moon.selfRotate` and add self rotation to the moon (1p).
    - [x] use the given params `this.params.planets.earth.moon.revolution` and add revolution to the moon (1p).
    - [x] move the orbit while the earth is moving by changing the position of the moon (1p).

2.  move the saturn ring while saturn is moving **(total: 1p)**
    - [x] move the saturn ring while saturn is moving by changing the position of the saturn ring (1p)