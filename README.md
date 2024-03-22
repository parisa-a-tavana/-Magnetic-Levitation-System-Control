# Magnetic-Levitation-System-Control
<br>
Magnetic levitation enables gravity defying by applying magnetic fields to suspend objects in mid-air. This occurs as the magnetic force generated counteracts gravity, resulting in the object's suspension. An application of this is evident in Maglev trains, which glide almost frictionlessly above the track surface due to the absence of physical contact. Consequently, these trains can attain remarkable speeds. The operational mechanism involves altering the magnetic polarity along the rails to propel the train forward or backward.
<br>
<br>

__System Description__:
<br>
In the system below, there is a coil around the magnetic core and an iron ball. By applying a voltage to the coil and passing current, It attracts an iron ball from it. The purpose of this system is to control the height of the iron ball by the input voltage. In this system, y distance of the iron ball from the magnetic core, V  is the applied voltage to the system and I is the circuit current.

<br>

![Image 1](images/system.jpg)


<br>
Here is the equations describing the system:
<br>
![Image 2](images/equations.jpg)
<br>
After finding the equilibrium point of the system and linearizing the system around that point, we calculate the state matrices:
<br>
![Image 3](images/state_space.jpg)
<br>

__Controller__:
<br>
We design an analog PID controller for the system:
<br>
![Image 4](images/analog_controller_function.jpg)
<br>
![Image 5](images/analog_controller_system.jpg)
<br>
![Image 6](images/analog_controller_diagram.jpg)
<br>
![Image 7](images/analog_controller_params.jpg)
<br>
<br>
Then we xheck the controller performance in the non-linear system.
<br>
![Image 8](images/analog_controller_nonlinear.jpg)
<br>
![Image 9](images/analog_controller_nonlinear_diagram.jpg)
<br>

__System Discretization__:

<br>
Now we discretize the system
<br>

![Image 10](images/discrete.jpg)

<br>

![Image 11](images/discrete_transfer_func.jpg)


<br>

![Image 12](images/dimages/discrete_rlocus.jpg.jpg)


<br> 

![Image 13](images/discrete_bode.jpg)


<br>

![Image 14](images/discrete_band_width.jpg)

<br>

<br>

__Discrete Controller__:

<br>
<br>
We design a discrete controller that has similiar parameters to the analog one
<br>

![Image 15](images/discrete_controller.jpg)

<br>

![Image 16](images/discrete_controller_diagram.jpg)



<br> 

![Image 17](images/discrete_controller_params.jpg)




<br>
We check the performance of the controller on the non linear system
<br>

![Image 19](images/discrete_controller_nonlinear.jpg)

<br>

![Image 20](images/discrete_controller_nonlinear_diagram.jpg)



