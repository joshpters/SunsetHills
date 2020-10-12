# Sunset Hills Challenge MiniSite

This is a complete minisite that contains a visual representation of the "Sunset Hills" challenge.

![Screenshot](/Images/screenshot.jpg)

This project was created using Bootstrap 4.5, HTML5, CSS3, and JavaScript.
All logic & JavaScript DOM changes were custom coded for this project.

## What is the "Sunset Hills" challenge?

Sunset Hills is an array manipulation challenge: the sun is setting in the West, and from West to East the heights of each
building is given in an integer array. Which of the buildings can see the sunset?

This challenge or a slight variation has been used by technology companies such as Amazon and was also
featured on a Geeks for Geeks blog post titled “Amazon Interview Experience | Set 189 (For SDE-1)”

## Installation

You can view this site [live](https://sunset-hills-challenge.netlify.app/).

To download and run locally, clone this repository and open index.html.

``` sourceCode
git clone https://github.com/joshpters/SunsetHills
```

## Core Function

This is a basic form of the function that determines which buildings can see the sunset.

The minisite has a modified version of this function to work with the page animations & grid generation.

```javascript
//sunset hills algorithm
function sunsetHills(buildingHeights) {
    let sunsetHillsOutput = new Array();
    let highestBuilding = 0;
    for (i = 0; i < buildingHeights.length; i++) {
        if (buildingHeights[i] <= highestBuilding) {
            sunsetHillsOutput.push(false);
            continue;
        }
        highestBuilding = buildingHeights[i];
        sunsetHillsOutput.push(true);
    }
    //output will be an array of booleans
    return sunsetHillsOutput;
}
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
