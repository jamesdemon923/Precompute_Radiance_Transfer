# Precomputed Radiance Transfer (PRT)

## Setup

**Operating & compiling environment**:

* **Real-time**: Visual studio code (Windows 11) & Live server
* **Precompute**: Cmake & Visual studio 2022 (Windows 11)

**Framework**:

* WebGL
* [Nori](https://github.com/wjakob/nori)

## Spherical Harmonics

### Defination:

### Properties:

1. **Orthogonality**

   For Basis functions $B(i)$

   <p align="center">   <img src="images/Theory/Equation/Orthogonality1.png"/> </p>

   <p align="center">   <img src="images/Theory/Equation/Orthogonality2.png"/> </p>
   
2. **Rotationally invariant**

## Precompute Radiance Transfer

$$
L(o) = \rho \int_{\Omega}L(i)V(i)max(0,n \cdot i)\mathrm{d}i
$$

**Spherical harmonic coefficient**: **Environmental light** & **Light transport**

## Pipeline

### Precompute:

#### Calculate the Spherical harmonic coefficient in Nori

**Environmental light:**

Riemann integral 

**Light transport:**

Diffuse unshadowed

Diffuse shadowed

Diffuse interreflection

### Real time:

#### Render the scene with light.txt and transport.txt from Nori.

### Environmental light spherical harmonic rotation

## Result

<table>
    <tr>
        <th colspan="1">Precompute Radiance Transfer</th>
    </tr>
    <tr>
        <td ><center><img src="images/Result/PRT/PRT.gif" >Precompute Radiance Transfer by Nori </center></td>
    </tr>

<table>
    <tr>
        <th colspan="1">Interreflection with 3 bounces</th>
        <th colspan="1">Shadowed</th>
    </tr>
    <tr>
        <td ><center><img src="images/Result/Static/GC with interBo3.jpg" style="zoom:80%;">Grace Cathedral Interreflection</center></td>
        <td ><center><img src="images/Result/Static/GC with shadowed.jpg">Grace Cathedral Shadowed</center></td>
    </tr>
    <tr>
        <td ><center><img src="images/Result/Static/Indoor with interBo3.jpg" style="zoom:80%;">Indoor Interreflection</center></td>
        <td ><center><img src="images/Result/Static/Indoor with shadowed.jpg">Indoor Shadowed</center></td>
    </tr>
    <tr>
        <td ><center><img src="images/Result/Static/Skybox with interBo3.jpg" style="zoom:80%;">Sky Box Interreflection</center></td>
        <td ><center><img src="images/Result/Static/Skybox with shadowed.jpg">Sky Box Shadowed</center></td>
    </tr>
    <tr>
        <td ><center><img src="images/Result/Static/CB with interBo3.jpg" style="zoom:80%;">Cornell Box Interreflection</center></td>
        <td ><center><img src="images/Result/Static/CB with shadowed.jpg">Cornell Box Shadowed</center></td>
    </tr>

<table>
    <tr>
        <th colspan="2">Environmental light spherical harmonic rotation</th>
    </tr>
    <tr>
        <td ><center><img src="images/Result/Rotation/GC with rotation.gif" >Grace Cathedral</center></td>
    </tr>
    <tr>
        <td ><center><img src="images/Result/Rotation/Indoor with rotation.gif" >Indoor</center></td>
    </tr>
    <tr>
        <td ><center><img src="images/Result/Rotation/Skybox with rotation.gif" >Sky Box</center></td>
    </tr>
    <tr>
        <td ><center><img src="images/Result/Rotation/CB with rotation.gif" >Cornell Box</center></td>
    </tr>

