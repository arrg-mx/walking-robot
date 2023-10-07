# ARRG: Curso ROS2 Humble, 2024-I - Walking Robot

## Contenido

- [Desarrollo](#desarrollo)
- [Equipo](#equipo)
- [Referencias](#referencias)

## Desarrollo

- [ ] Documentación y justificación de la configuración del robot.
- [ ] Planteamiento del modelo cinemático directo de la postura y planteamiento del modelo cinemático inverso de la postura.
- [ ] Diseño e implementación de un modelo virtual del caminante.
	- [ ] Modelo de una pierna del robot.
	- [ ] Modelo del robot completo.
- [ ] Realización de las pruebas dentro del modelo virtual y reporte de resultados.
- [ ] Construcción de un modelo físico del robot.
	- [ ] Construcción de una pierna del robot.
	- [ ] Construcción de la estructura del robot.
- [ ] Implementación de los resultados en el prototipo físico.
	- [ ] Prototipo de una pierna.
	- [ ] Prototipo del robot completo
- [ ] Reporte de resultados finales.
- [ ] Conclusiones y Discusión

## Equipo

**Integrantes del proyecto:**

| Nombre | Observaciones |
| :----------| :----------- |
| Hernández Romero Naomi Estefanía | **responsable** |
| Vargas Gutiérrez Kevin | |
| Hernández Hernández Danae Montserrat | |
| Martínez Merino Luis Eduardo | |

## Referencias

### ¿Dónde empezar?

**Artículos**

1. **Control of a Hexapod Robot Considering Terrain Interaction** [Arxiv Cornell University - article](https://arxiv.org/abs/2112.10206)
	> M. Zangrandi, S. Arrigoni, and F. Braghin, Control of a Hexapod Robot Considering Terrain Interaction. 2021. 
	> 
	> doi: 10.48550/arXiv.2112.10206
1. *Real-Time Stabilisation for Hexapod Robots* **DOI:** <https://doi.org/10.1007/978-3-319-23778-7_48>
	> M. Hörger, N. Kottege, T. Bandyopadhyay, A. Elfes, and P. Moghadam, “Real-Time Stabilisation for Hexapod Robots,” in Experimental Robotics: 
	> The 14th International Symposium on Experimental Robotics, M. A. Hsieh, O. Khatib, and V. Kumar, Eds. Cham: Springer International Publishing, 2016, pp. 729–744. 
	> 
	> doi: 10.1007/978-3-319-23778-7_48. 
1. **Kinematic and Dynamic Modeling of the PhantomX AX Metal Hexapod Mark III Robot using Quaternions**	[IEEE article](https://ieeexplore.ieee.org/abstract/document/9624596)
	> A. J. P. A. Chávez and J. H. A. Alcántara, "Kinematic and Dynamic Modeling of the PhantomX AX Metal Hexapod 
	> Mark III Robot using Quaternions," 2021 International Conference on Control, Automation and Information Sciences (ICCAIS), Xi'an, China, 2021, pp. 595-601, 
	>
	> doi: 10.1109/ICCAIS52680.2021.9624596.
1. **Dynamic Modeling and Control of the Hexapod Robot Using Matlab SimMechanics** [ResearchGate article](https://www.researchgate.net/publication/330405549_Dynamic_Modeling_and_Control_of_the_Hexapod_Robot_Using_Matlab_SimMechanics)
	> Beaber, Sameh & Zaghloul, Abdelrahman & Kamel, Mohamed & Hussein, Wessam. (2018). Dynamic Modeling and Control of the Hexapod Robot Using Matlab SimMechanics. 
	> V04AT06A036. 10.1115/IMECE2018-88226. 
	>
	> DOI:10.1115/IMECE2018-88226
1. **Locomotion Control of PhantomX Hexapod Robot with Touch-Pressure Sensor and RoboComp**	[ResearchGate article](https://ieeexplore.ieee.org/abstract/document/9247874).
	> J. E. C. Fuertes, J. J. M. Arciniegas, P. B. G. de Castro and O. A. V. Albán, "Locomotion Control of PhantomX Hexapod Robot with Touch-Pressure Sensor and RoboComp," 
	> 2020 IEEE Colombian Conference on Applications of Computational Intelligence (IEEE ColCACI 2020), Cali, Colombia, 2020, pp. 1-6, 
	> 
	> doi: 10.1109/ColCACI50549.2020.9247874.
1. **Dynamic modeling and real-time evaluation of reaction forces and torques of hexapod robot** [ResearchGate article](https://www.researchgate.net/publication/350820943_Dynamic_modeling_and_real-time_evaluation_of_reaction_forces_and_torques_of_hexapod_robot)
	> S. Beaber, A. Zaghloul, M. Kamel, and W. Hussein, “Dynamic modeling and real-time evaluation of reaction forces and torques of hexapod robot,” Apr. 2021, p. 30. 
	> 
	> doi: 10.1117/12.2596113. 
1. **Design, Construction, and Rough-Terrain Locomotion Control of Novel Hexapod Walking Robot With Four Degrees of Freedom Per Leg** [IEEE article](https://ieeexplore.ieee.org/abstract/document/9330519)
	> P. Čížek, M. Zoula and J. Faigl, "Design, Construction, and Rough-Terrain Locomotion Control of Novel Hexapod Walking Robot With Four Degrees of Freedom Per Leg," 
	> in IEEE Access, vol. 9, pp. 17866-17881, 2021, 
	>
	> doi: 10.1109/ACCESS.2021.3053492.

**Blogs**

1. *Love, Death, and Robot simulators* [medium post](https://medium.datadriveninvestor.com/love-death-and-robot-simulators-9ad7c62d46ae). 
	- **Posted by:** [Mithi](https://medium.com/@mithi?source=post_page-----9ad7c62d46ae--------------------------------)
	- **Published:** March 30, 2020
	- **Posted in:** [DataDrivenInvestor](https://medium.datadriveninvestor.com/?source=post_page-----9ad7c62d46ae--------------------------------)
	- **Source Code:** **Hexapod Kinematics Library** [Github repository](https://github.com/mithi/hexapod-kinematics-library). By [**Mithi Sevilla´s** Github Profile](https://github.com/mithi). 
	Code you can use to solve forward/inverse kinematics and generate walk sequences of hexapod robots. 
	- **Tags:** [Robotics](https://medium.com/tag/robotics?source=post_page-----9ad7c62d46ae---------------robotics-----------------), 
	[Artificial Intelligence](https://medium.com/tag/artificial-intelligence?source=post_page-----9ad7c62d46ae---------------artificial_intelligence-----------------), 
	[Open Source](https://medium.com/tag/open-source?source=post_page-----9ad7c62d46ae---------------open_source-----------------), 
	[Electronics](https://medium.com/tag/electronics?source=post_page-----9ad7c62d46ae---------------electronics-----------------), 
	[Coding](https://medium.com/tag/coding?source=post_page-----9ad7c62d46ae---------------coding-----------------)

**Legacy/Opensource Projects, Applications and, Libraries**

1. **Interbotics ROS Crawlers** [github repository](https://github.com/Interbotix/interbotix_ros_crawlers). ***ROS2 Humble*** *Compatible*
	- This repo contains custom ROS packages to control the various types of crawlers sold at [Interbotix](https://www.trossenrobotics.com/). 
	- These ROS packages build upon the ROS driver nodes found in the [interbotix_ros_core](https://github.com/Interbotix/interbotix_ros_core) *repository*. 
	- Support-level software can be found in the [interbotix_ros_toolboxes](https://github.com/Interbotix/interbotix_ros_toolboxes) *repository*.
1. **PhantomX Hexapod Mark II**
	- Google search [results](https://www.google.com/search?client=firefox-b-d&q=PhantomX+Hexapod+Mark+II)
	- **PhantomX AX Metal Hexapod MK-III Kit** [Trossen Robotics #Item](https://www.trossenrobotics.com/phantomx-ax-hexapod.aspx)
	- **PhantomX AX Metal Hexapod Mark III** [YT video](https://www.youtube.com/watch?v=8v16kpBj9JQ). [Trossen Robotics - YT channel](https://www.youtube.com/@InterbotixTrossenRobotics)
	- **PhantomX Hexapod Mark II** [GrabCad model](https://grabcad.com/library/phantomx-hexapod-mark-ii-1)
	- **HumaRobotics**
		- **phantomx_description** [github repository](https://github.com/HumaRobotics/phantomx_description)
		- **phantomx_control** [github repository](https://github.com/HumaRobotics/phantomx_control)
		- **phantomx_gazebo** [github repository](https://github.com/HumaRobotics/phantomx_gazebo)
		- **geomagic_touch** [github repository](https://github.com/HumaRobotics/geomagic_touch)
	- **PhantomX Hexapod Examples Various demos for the PhantomX Hexapod** [github repository](https://github.com/Interbotix/PhantomXHexapodExamples)
1. **hexapod-robot** [github repository](https://github.com/ibarbech/hexapod-robot)
1. **ROS Hexapod Stack** [github repository](https://github.com/KevinOchs/hexapod_ros/tree/master)
1. **Syropod High-level Controller** [Github repository](https://github.com/csiro-robotics/syropod_highlevel_controller)
	- **OpenSHC: A Versatile Multilegged Robot Controller** [YT video](https://www.youtube.com/watch?v=-E7-2UMP5XU)
	- **Note:** The codebase is largely copied from [Mithi's Bare Minimum Hexapod Robot Simulator 2](https://github.com/mithi/hexapod).
1. **Hexi** *(project)* [about](https://hexyrobot.wordpress.com/)
	- [Github repository](https://github.com/mithi/hexy)


