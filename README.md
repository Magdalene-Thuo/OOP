# OOP

class Smartphone:
    def __init__(self, brand, model, color, storage, battery):
        self.brand = brand
        self.model = model
        self.color = color
        self.storage = storage
        self.battery = battery

    def display_info(self):
        print(f"Smartphone Info:\nBrand: {self.brand}\nModel: {self.model}\nColor: {self.color}\nStorage: {self.storage}GB\nBattery: {self.battery}%")

    def charge_battery(self, amount):
        if self.battery + amount <= 100:
            self.battery += amount
            print(f"Battery charged! Current battery: {self.battery}%")
        else:
            self.battery = 100
            print("Battery fully charged!")

# Create an instance of the Smartphone class
my_phone = Smartphone("Apple", "iPhone 14", "Blue", 128, 50)

# Call methods on the object
my_phone.display_info()
my_phone.charge_battery(30)
---------------------------------------------------------------------
Step 2: Add an inheritance layer to explore polymorphism
class SmartphoneWithCamera(Smartphone):
    def __init__(self, brand, model, color, storage, battery, camera_quality):
        super().__init__(brand, model, color, storage, battery)
        self.camera_quality = camera_quality

    def take_photo(self):
        print(f"Taking a photo with {self.camera_quality} camera quality!")

# Create an instance of SmartphoneWithCamera
camera_phone = SmartphoneWithCamera("Samsung", "Galaxy S23", "Black", 256, 80, "108MP")

# Call methods on the object
camera_phone.display_info()
camera_phone.take_photo()
camera_phone.charge_battery(20)
---------------------------------------------------------------------------

Activity 2: Polymorphism Challenge (Animals Example) 🎭
class Animal:
    def move(self):
        pass  # This is an empty method to be overridden

class Dog(Animal):
    def move(self):
        print("The dog is running! 🐕")

class Cat(Animal):
    def move(self):
        print("The cat is jumping! 🐈")

class Fish(Animal):
    def move(self):
        print("The fish is swimming! 🐟")

# Instantiate objects of each class and call their move methods
animals = [Dog(), Cat(), Fish()]

for animal in animals:
    animal.move()
** Output**
The dog is running! 🐕
The cat is jumping! 🐈
The fish is swimming! 🐟














