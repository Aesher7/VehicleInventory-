class Automobile:
    def __init__(self, make, model, color, year, mileage):
        self.make = make
        self.model = model
        self.color = color
        self.year = year
        self.mileage = mileage

class DealershipInventory:
    def __init__(self):
        self.inventory = []

    def add_vehicle(self, make, model, color, year, mileage):
        vehicle = Automobile(make, model, color, year, mileage)
        self.inventory.append(vehicle)
        print("Vehicle added:", vehicle.make, vehicle.model)

    def remove_vehicle(self, make, model):
        for vehicle in self.inventory:
            if vehicle.make == make and vehicle.model == model:
                self.inventory.remove(vehicle)
                print("Vehicle removed:", make, model)
                break

    def update_vehicle(self, make, model, attribute, new_value):
        for vehicle in self.inventory:
            if vehicle.make == make and vehicle.model == model:
                setattr(vehicle, attribute, new_value)
                print("Vehicle updated:", make, model, attribute, "set to", new_value)
                break

    def export_inventory_to_file(self, filename):
        with open(filename, 'w') as file:
            file.write("Make,Model,Color,Year,Mileage\n")
            for vehicle in self.inventory:
                file.write(f"{vehicle.make},{vehicle.model},{vehicle.color},{vehicle.year},{vehicle.mileage}\n")
            print("Inventory exported to file:", filename)


inventory = DealershipInventory()

print("Adding vehicles:")
inventory.add_vehicle("Ford", "Mustang", "Red", 2021, 1000)
inventory.add_vehicle("Tesla", "Model 3", "Blue", 2022, 5000)
inventory.add_vehicle("Chevrolet", "Camaro", "Black", 2020, 2000)

print("\nUpdating vehicle mileage:")
inventory.update_vehicle("Tesla", "Model 3", "mileage", 6000)

print("\nRemoving vehicle:")
inventory.remove_vehicle("Ford", "Mustang")

print("\nExporting inventory to file:")
inventory.export_inventory_to_file("inventory.txt")
