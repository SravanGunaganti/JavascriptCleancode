//Use meaningful and pronounceable variable names

//Bad:

const yyyymmdstr = new Date();
const fname = 'Sravan';
const lname = 'Gunaganti';

//Good:

const currentDate = new Date();
const firstName = 'Sravan';
const lastName = 'Gunaganti';



//-----2----Don't add unneeded context

//If your class/object name tells you something, don't repeat that in your variable name.

//Bad:

const Car = {
  carMake: "Honda",
  carModel: "Accord",
  carColor: "Blue"
};

function paintCar(car, color) {
  car.carColor = color;
}

//Good:

const Car = {
  make: "Honda",
  model: "Accord",
  color: "Blue"
};

function paintCar(car, color) {
  car.color = color;
}


//---3----

