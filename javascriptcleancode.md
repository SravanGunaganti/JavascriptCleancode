##Javascript cleancode practice

## 1.Use meaningful and pronounceable variable names

//Bad:

const yyyymmdstr = new Date();
const fname = 'Sravan';
const lname = 'Gunaganti';

//Good:

const currentDate = new Date();
const firstName = 'Sravan';
const lastName = 'Gunaganti';




## 2.Don't add unneeded context

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



## 3.Function names should say what they do.

//Bad:

const Person = {
    firstName: "Sravan",
    lastName: "Gunaganti",
  };
  
function name(person) {
  return `${person.firstName} ${person.lastName}`
}

//Good:

const Person = {
  firstName: "Sravan",
  lastName: "Gunaganti",
};

function getFullName(person) {
  return `${person.firstName} ${person.lastName}`
}




## 4.Use default arguments instead of short circuiting or conditionals

/*Default arguments are often cleaner than short circuiting. Be aware that if you use them, your function will only provide default values for undefined arguments. Other "falsy" values such as '', "", false, null, 0, and NaN, will not be replaced by a default value.*/

//Bad:

function getUserData(name) {
  const userName = name || "sravan;
  // ...
}

//Good:

function getUserData(name = "sravan") {
  // ...
}



## 5.Remove commented code

//Bad:

doSomething();
// doOtherStuff();
//doSomeMoreStuff();


//Good:

doSomething();
