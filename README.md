# Python-Week-5-Assignment


#Activity One
# Base class representing a generic electronic device
class Device:
    def __init__(self, brand, model):
        # Initialize common attributes
        self.brand = brand
        self.model = model

    def power_on(self):
        # Generic method to simulate powering on
        print(f"{self.brand} {self.model} is now ON.")

# Derived class representing a Smartphone, inherits from Device
class Smartphone(Device):
    def __init__(self, brand, model, os, storage):
        # Call parent constructor using super()
        super().__init__(brand, model)
        # Add smartphone-specific attributes
        self.os = os
        self.storage = storage

    def install_app(self, app_name):
        # Method to simulate installing an app
        print(f"Installing {app_name} on {self.brand} {self.model}...")

    def show_specs(self):
        # Display all the smartphone's specifications
        print(f"Brand: {self.brand}, Model: {self.model}, OS: {self.os}, Storage: {self.storage}GB")

# Create an object of Smartphone
phone = Smartphone("Samsung", "Galaxy S21", "Android", 128)
phone.power_on()
phone.show_specs()
phone.install_app("WhatsApp")

#Activity 2
# Base class representing a generic vehicle
class Vehicle:
    def move(self):
        # Placeholder method
        print("The vehicle is moving.")

# Derived class representing a Car
class Car(Vehicle):
    def move(self):
        # Override move method for a car
        print("Driving 🚗")

# Derived class representing a Plane
class Plane(Vehicle):
    def move(self):
        # Override move method for a plane
        print("Flying ✈️")

# Derived class representing a Boat
class Boat(Vehicle):
    def move(self):
        # Override move method for a boat
        print("Sailing 🚢")

# Demonstrate polymorphism
def travel(vehicle):
    # This function accepts any vehicle and calls its move method
    vehicle.move()

# Create objects of different vehicle types
car = Car()
plane = Plane()
boat = Boat()

# Use polymorphism: same function call behaves differently
travel(car)    # Outputs: Driving 🚗
travel(plane)  # Outputs: Flying ✈️
travel(boat)   # Outputs: Sailing 🚢
