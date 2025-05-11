
# JavaScript Arrays in GIS — Q&A Format

This document includes questions and answers with code examples on JavaScript arrays applied to GIS contexts.

---

### ❓ Q1: How do you store a list of latitude and longitude coordinates for cities?

```javascript
const locations = [
  { city: "London", coordinates: [48.8566, 2.3522] },
  { city: "Paris", coordinates: [35.6895, 139.6917] },
  { city: "New York", coordinates: [40.7128, -74.0060] }
];

for (const city of locations) {
  console.log(`City: ${city.city}, Coordinates: ${city.coordinates}`);
}
```
✅ **A:** This uses an array of objects, each with a city name and coordinates as an array.

---

### ❓ Q2: How can you access the coordinates of the third city?

```javascript
let cities = [
  { name: "Paris", coords: [48.8566, 2.3522] },
  { name: "Tokyo", coords: [35.6895, 139.6917] },
  { name: "New York", coords: [40.7128, -74.0060] }
];

const thirdCity = cities[2];
console.log(`Name: ${thirdCity.name}, Coordinates: ${thirdCity.coords[0]}, ${thirdCity.coords[1]}`);
```
✅ **A:** Access by index `2` for the third city, and use `coords[0]`, `coords[1]` for latitude and longitude.

---

### ❓ Q3: How do you convert an object property (like `id`) to a string?

```javascript
var feature = {
  type: "Feature",
  geometry: {
    type: "Point",
    coordinates: [102.0, 0.5]
  },
  properties: {
    name: "Sample Point",
    id: 42
  }
};

console.log(feature.properties.id.toString());
```
✅ **A:** Use `.toString()` to convert a number to a string.

---

### ❓ Q4: Can `.toString()` be used on numbers like zoom levels?

```javascript
var zoom_level = 5;
console.log(zoom_level.toString());
```
✅ **A:** Yes, any number can be converted to a string with `.toString()`.

---

### ❓ Q5: How can you display all properties of a GIS feature?

```javascript
var feature = {
  type: "Feature",
  geometry: {
    type: "Point",
    coordinates: [45.0, 90.0]
  },
  properties: {
    id: 101
  }
};

console.log(JSON.stringify(feature.properties));
```
✅ **A:** Use `JSON.stringify()` to convert the properties object into a readable string.

---

### ❓ Q6: How to print both coordinates and ID of a GIS feature in a single string?

```javascript
var feature = {
  type: "Feature",
  geometry: {
    type: "Point",
    coordinates: [45.0, 90.0]
  },
  properties: {
    id: 101
  }
};

var output = "ID: " + feature.properties.id.toString() + 
             ", Coordinates: " + feature.geometry.coordinates.toString();
console.log(output); 
// Output: "ID: 101, Coordinates: 45,90"
```
✅ **A:** Concatenate string values with `.toString()` for display or logging.

---
