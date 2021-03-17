# Vehicle Showroom System

A Command Line System for Vehicle Showroom System. The program is written in Dart language. 
You can directly run the application using the following link :
https://dartpad.dev/d6ea2c9975a3b10660805580244f275f


In the main function there are three types of command
1. addVehicle adds a vehicle to the showroom where the user has to mention the specification of the cars
2. getVehicle gives the list of all vehicles available in the showroom
3. removeVehicle removes the vehicle from the showroom based on the vehicle type and its model no.



System Description:

A "Vehicle" has following descriptions: 1. model number 2. engine type.

There are three types of engines a. oil b. gas c. diesel 3. engine power 4. tire size. 


In the vehicle showroom there are 3 types of vehicles - Normal Vehicles, Sports Vehicles & Heavy Vehicles. 

For "Normal Vehicle" There is no extra property, so it will have all the descriptions as above described descriptions of a "Vehicle".

For "Sports Vehicle" There are two extra properties or attributes you can say. And these are : 1. turbo 2. engine type is oil only 

For "Heavy Vehicle" There are also two extra properties or attributes you can say. And these are : 1. weight 2. engine type is diesel only 


The system has the following functionality: 
a. Add any type of vehicle in showroom. 
b. Remove any of the vehicles from showroom. 
c. Show the vehicle lists with details currently have in showroom.
d. Show the list of vehicles with current expected visitor count


The regular expected visitor count of the vehicle showroom is 30. But whenever a new "Sports Vehicle" is added in the showroom the expected visitor count increase by 20.  