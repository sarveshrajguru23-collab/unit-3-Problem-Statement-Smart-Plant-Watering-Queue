# Smart Plant Watering Queue

## 1. Project Overview

Smart Plant Watering Queue is a C++ Data Structures mini-project that manages plant-watering tasks using a Queue data structure. Plants with low soil moisture are added to a queue and processed in First-In, First-Out (FIFO) order.

## 2. Problem Statement

Watering multiple plants manually can make it difficult to track which plants need water first. This project provides a queue-based system to organize watering tasks and prioritize plants that require watering.

## 3. Objectives

* Manage multiple plants using a queue.
* Check soil moisture values entered by the user.
* Add plants requiring water to the queue.
* Process watering tasks in FIFO order.
* Display pending plants and the next plant to be watered.
* Demonstrate practical use of queue operations.

## 4. Technologies Used

* Programming Language: C++
* Data Structure: Queue
* Storage: Array
* Interface: Console-based application

## 5. Features

1. Add a plant to the watering queue.
2. Skip plants with sufficient moisture.
3. Water the next plant in FIFO order.
4. Display pending plants.
5. Show the next plant to be watered.
6. Handle empty and full queue conditions.

## 6. Queue Operations

* Enqueue: Adds a plant to the queue.
* Dequeue: Removes the plant after simulated watering.
* Peek: Displays the next plant.
* Display: Lists all pending plants.

## 7. How to Run

1. Download or clone this repository.
2. Open `main.cpp` in a C++ compiler.
3. Compile and run the program.

Example compilation command:

`g++ main.cpp -o plant_queue`

Run on Windows:

`plant_queue.exe`

## 8. Sample Input

* Plant Name: Rose
* Soil Moisture: 20%

## 9. Sample Output

`Rose added to the watering queue.`

When the user selects Water Next Plant:

`Watering plant: Rose`

`Watering completed!`

## 10. Limitations

* The current project is a software simulation.
* Soil moisture values are entered manually.
* No physical soil moisture sensor or water pump is connected.
* The moisture threshold of 40% is an example setting.

## 11. Future Scope

* Integrate soil moisture sensors.
* Connect an automatic water pump.
* Monitor plants in real time.
* Add a graphical user interface.
* Store plant information for future analysis.

## 12. Conclusion

The Smart Plant Watering Queue demonstrates the application of queue operations to a practical plant-watering scenario. It provides a foundation for developing a sensor-based automatic irrigation system.
