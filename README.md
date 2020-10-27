# Datasaur

### Notes

* It's a usual fork it, clone it, run `jest --watch-all` type of exercise.
* You'll practice your `map` and `filter` operations using helper functions!
* You'll also get some object practice.
* And some of that object work might look familiar, as we've covered the same problems before. If you can, don't look at the old solutions and come up with new versions with the knowledge and techniques you've gained in the meantime!

### A Note On Mutation

There are two levels at which we worry about mutation here. The easier to avoid is the array level. If you `push` or otherwise mutate the array you take in as a parameter, it will affect the array that was passed in as well (since they are, in fact, the same array). But the more insidious mutation--the one that's easier to miss--is the object level. Each element of the array is a mutable object, and if you mutate the object that's in the array, you'll mutate the object in the array outside as well.

So make sure to make a copy of the object and work only on that copy!

### Tasks


##### Helper Function for Map Helper Functions

* `makeDino` - you want to create a new object based on the parameters passed in.
    * HINT: This one can also be a helper function for the three mapping helper functions below.
    * HINT: you can check if `extinct` is undefined and give it the default value asked for if it is, but don't forget to allow a real value passed in to get there if it exists!


##### Map Helper Functions

These functions will return a new element based on the ONE element they're passed (sometimes unchanged!). They don't have to concern themselves with multiple elements or arrays; they just deal with one element at a time!

* `makeExtinct` - given one dinosaur object, return a dinosaur with its `extinct` propety set to true. As with all the mapping helper functions, don't forget that you can pass to `makeDino` the values from the object you were passed to make a copy before working on it. HINT: you can even pass to `makeDino` different values from the values on the object you were passed!
* `truncateSpecies` - given one dinosaur object, if its `species` property is longer than 10 characters, return a NEW dinosaur object with the same values, but with the `species` changed to be the `species` name's first 7 characters, followed by a `...`. If the species name is already short, you can return a copy of the dinosaur that is unchanged. HINT: the previous hint! HINT: make sure you're returning the full dinosaur object, and NOT just the dino's `species` property. HINT: you can use `.slice` to get a range of characters from the original string.
* `makeSingular` - given one dinosaur object, if its `species` property ends with `us`, return a NEW dinosaur object with the same values, but with the `species` changed to remove the `us` from the end. If the species name doesn't end with `us`, you can return a copy of the dinosaur that is unchanged. HINT: all previous hints! HINT: `.slice` can take a negative index!


##### Filter Helper Functions

Just some general hints with these:

* You will always be taking in one dinosaur object.
* You always want to return a boolean.
* Don't worry too much about conciseness of code the first time you write it, but do feel free to refactor once your test is greeen.


##### Mapping Functions

Just some general hints with these as well:

* Don't forget your general steps: make a new empty array, loop through the old array populating the new one based on its values, and of course return that new array.
* A map ALWAYS pushes in to the new array once for every element of the old array.
* A map ALWAYS runs each element through a transformation function before pushing it.


##### Filter Functions

Just some general hints with these as well:

* Don't forget your general steps: make a new empty array, loop through the old array populating the new one based on its values, and of course return that new array.
* A filter may sometimes skip an element (`if` is great for this!), pushing in to the new array only some elements from the old array. How does it decide? Using the boolean return value from the helper function!
* A filter NEVER runs its element through transformation functions. Every element that DOES make it into the final array does so unchanged.
