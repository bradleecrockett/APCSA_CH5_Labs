# APCSA_CH5_Labs

## 5.1 Cars

1. Complete the ```Car.java``` class so that it meets the following requirements:

2. Every ```Car``` object should know its ```make``` (a String), ```model``` (a String), ```fuelMileage``` (a double), ```numberOfDoors``` (an int) and its ```topSpeed``` (an int).

3. Create a default constructor that is not passed any parameters.  A default ```Car``` should have a make and model of ```"Generic"``` fuel mileage of 25.5 miles per gallon, 4 doors and a top speed of 105 miles per hour. 

4. Create an overloaded constructor that is passed 3 paramaters to initialize the instance variables (in alphabetical order).

5. All instance variables should have appropriately named accessor and mutator methods.

6. Override the ```toString``` method from the ```Object``` class in the format:
     ```
     Make: Toyota  Model: Camry
     Doors: 4   Fuel Mileage: 34 mpg   
     Top Speed: 115 mph
     ```
7. Create a driver program ```CarTester.java``` to test your ```Car``` class.  Create 3 different ```Car``` objects, including a default ```Car```.  Then print each ```Car``` using the ```toString``` method.  You should also test your accessor and mutator methods in your driver class.  When you test them print the object, mutate a field, then print the field again.

## 5.2 Trucks

1. Create a ```Truck``` class that is a subclass of a ```Car``` object.

2. A ```Truck``` should know everything that a ```Car``` knows as well as have a boolean value ```isFourWheelDrive``` and a feild for its ```towingCapacity``` (an int).

3. Create a default constructor that initializes that leaves all of the default ```Car``` fields the same other than ```numDoors``` which should automatically be changed to 2.  The default ```Truck``` should be 2 wheel drive and have a towing capacity of 6500 pounds.

4. Create an overloaded constructor which takes 7 parameters, in alphabetical order to initialize all of the ```Truck``` fields.

5. Override the ```toString``` method to print the ```Truck``` objects in the formaat:
     ```
     Make: Chevrolet  Model: Silverado
     Doors: 2   Fuel Mileage: 20 mpg   
     Top Speed: 100 mph
     Four Wheel Drive: true
     Towing Capacity: 6500 lbs
     ```
6. Create a driver program ```TruckTester.java``` to test your ```Truck``` class.  Create 3 different ```Truck``` objects, including a default ```Truck```. Then print each ```Truck``` using the ```toString``` method. You should also test your accessor and mutator methods in your driver class. When you test them print the object, mutate a field, then print the field again.

## 5.3 Parking Lot

1. Create a class called ```ParkingLot.java``` that has one instance varaible ```lot``` that is an array that can hold ```Car``` and ```Truck``` objects. The parking lot should only be able to hold up to 20 vehicles.

2. Create a class variable ```numVehicles``` that keeps track of the number of vehicles in the lot.

3. Create a default constructor that intializes the ```lot``` to an empty array with 20 spaces.

4. Create a method called ```parkVehicle``` which excepts a ```Car``` or ```Truck``` object as a parameter and adds that Vehicle to the ```lot```. It also needs to update the number of vehicles in the lot. This method should never park a vehicle if ther is not a space available to park in. Meaning if the lot is full it should deny parkVehicle and print a message that the lot is full.

5. Write a ```toString``` method for the ```ParkingLot``` class that uses a loop to print each ```Car``` and ```Truck``` in the lot.

6. Create a driver class ```ParkingLotTester.java``` that creates one ```ParkingLot``` object called ```berryLot```.

7. Manually add the following vehicles to the array (do not use a Scanner):

  Make | Model | Doors | Mileage | Top Speed | Four Wheel Drive | Towing Capacity
  --- | --- | --- | --- | --- | --- | ---  
  Ford | Escort | 4 | 35.2 | 85 |   |   
  Ford | F250 | 2 | 24.3 | 115 | true | 9000  
  Chevy | Impala | 4 | 27.8 | 120 |   |   
  Toyota | Corolla | 4 | 38.7 | 100 |  |   
  Dodge | Ram | 4 | 19.3 | 110 | false | 7000  
  Generic | Generic | 4 | 25.5 | 105 |  |   
  Generic | Generic | 2 | 25.5 | 105 | false | 6500  
  GMC | Sierra | 4 | 23.1 | 125 | true | 8000  
  
8. Call ```System.out.println(berryLot);```

## 5.4 Comparing Cars

1. Modify the ```Car``` class so that it implements ```Comparable```.

2. ```Car``` and ```Truck``` objects are only ranked based on their top speed.  The lower the top speed, the lower the rank of the vehicle.

3. Add the method ```sortLot()``` to the ```ParkingLot``` class.  This is a mutator method that sorts the ```lot``` instance variable using one single statement: ```Arrays.sort(lot);```.

4. Make a copy of ```ParkingLotTester``` and rename it ```ParkingLotTester2```. At the very end of the main method, call ```berryLot.sortLot()``` then call ```System.out.println(berryLot);``` once more.


