List<VehicleDetails> Sports = [];
List<VehicleDetails> Heavy = [];
List<VehicleDetails> Normal = [];

class Vehicle {
  addVehicle(
      {String type,
      int modelNo,
      int enginePower,
      int weight,
      String engine,
      int tireSize,
      bool turbo}) {
    if (type == 'Sports') {
      engine = 'Oil';
      turbo = true;
      Sports.add(VehicleDetails(
          modelNo: modelNo,
          enginePower: enginePower,
          engine: engine,
          tireSize: tireSize,
          type: type,
          turbo: turbo));
    }

    if (type == 'Heavy') {
      engine = 'Diesel';
      Heavy.add(VehicleDetails(
          modelNo: modelNo,
          enginePower: enginePower,
          engine: engine,
          tireSize: tireSize,
          weight: weight,
          type: type));
    }

    if (type == 'Normal') {
      Normal.add(VehicleDetails(
          modelNo: modelNo,
          enginePower: enginePower,
          engine: engine,
          tireSize: tireSize,
          type: type));
    }
  }

  getVehicle() {
    int count = 30;
    count = count + Sports.length * 20;

    print(
        'There are ${Sports.length} Sports Car, ${Heavy.length} Heavy Car and ${Normal.length} Normal Car in the showroom');
    print('Expected Visitor Count is $count' + '\n');

    Sports.forEach((element) => element.getModel());
    Heavy.forEach((element) => element.getModel());
    Normal.forEach((element) => element.getModel());
  }

  removeVehicle({String type, int modelNo}) {
    if (type == 'Sports') {
      int a = Sports.indexWhere((o) => o.type == type && o.modelNo == modelNo);
      print('loalasd $a');
      Sports.removeAt(a);
    }
    if (type == 'Heavy') {
      int a = Heavy.indexWhere((o) => o.type == type && o.modelNo == modelNo);
      print('loalasd $a');
      Heavy.removeAt(a);
    }
    if (type == 'Normal') {
      int a = Heavy.indexWhere((o) => o.type == type && o.modelNo == modelNo);
      print('loalasd $a');
      Heavy.removeAt(a);
    }
  }
}

class VehicleDetails {
  String type;
  int modelNo;
  int enginePower;
  int tireSize;
  int weight;
  String engine;
  bool turbo;

  VehicleDetails(
      {this.modelNo,
      this.enginePower,
      this.engine,
      this.tireSize,
      this.turbo,
      this.weight,
      this.type}) {}
  void getModel() {
    if (type == 'Heavy') {
      print('Car type : $type');
      print('Model no : $modelNo');
      print('Weight : $weight');
      print('engine : $engine');
      print('EnginePower : $enginePower');
      print('TireSize : $tireSize');
      print('\n');
    } else if (type == 'Sports') {
      print('Car type : $type');
      print('Model no : $modelNo');
      print('Engine : $engine');
      print('EnginePower : $enginePower');
      print('TireSize : $tireSize');
      print('Turbo : $turbo');
      print('\n');
    } else if (type == 'Normal') {
      print('Car type : $type');
      print('Model no : $modelNo');
      print('Engine : $engine');
      print('EnginePower : $enginePower');
      print('TireSize : $tireSize');
      print('\n');
    }
  }
}

void main() {
  Vehicle vehicle = new Vehicle();

  vehicle.addVehicle(type: 'Sports', modelNo: 1, enginePower: 3, tireSize: 20);

  vehicle.addVehicle(type: 'Sports', modelNo: 3, enginePower: 5, tireSize: 40);

  vehicle.addVehicle(
      type: 'Heavy', modelNo: 2, enginePower: 3, weight: 650, tireSize: 10);

  vehicle.addVehicle(
      type: 'Normal', modelNo: 5, enginePower: 7, tireSize: 10, engine: 'Gas');

  // vehicle.removeVehicle(type: 'Sports',modelNo:3);

  vehicle.getVehicle();
}
