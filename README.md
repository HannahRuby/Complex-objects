D09
🧩 JS: Complex Objects

🧩 JS: Complex Objects
Completion requirements

Complex Objects
Overview
Objects can contain other objects, arrays, and arrays of objects. This allows us to represent more complex data structures.

For example, a blog post might have an author, and the author might have a name, age, and favourite colour. The blog post might also have a list of tags associated with it.

Class Plan
Demo: Demonstration of complex objects and how they work
Workshop: Write some complex objects to the console
Topics
What is a complex object?
How to create a complex object
How to access properties on a complex object
How to add properties to a complex object
Resources
MDN: Objects
MDN: Object basics
Workshop
Creating complex objects
⛳️ In a new index.html file, add a script tag containing a console.log. Open the file in your browser and check the console to see the output.

console.log("Hello world!");
 
⛳️ Create an object called blogPost with a title, author, and tags. Log the object to the console.

const blogPost = {
  title: "My first blog post",
  author: {
    name: "Bob",
    age: 30,
    favouriteColour: "red",
  },
  tags: ["coding", "javascript", "objects", "arrays"],
  content: "This is my blog post about learning objects and arrays.",
};
 
Accessing properties
Objects inside objects, like the author object here, are accessible by chaining the dot notation together.

console.log(blogPost.author.name); // Output: Bob
 
Arrays inside objects are accessible by using the index of the item in the array.

console.log(blogPost.tags[0]); // Output: coding
 
You can print out the number of tags by checking the length of the tags array:

console.log(blogPost.tags.length); // Output: 4
 
You can combine this with a traditional for loop:

console.log(
  `There are ${blogPost.tags.length} tags for post "${blogPost.title}":`
); // Output: There are 4 tags for post "My first blog post":
for (let i = 0; i < blogPost.tags.length; i++) {
  console.log(blogPost.tags[i]); // Output: coding, javascript, objects, arrays
}
 
Or use a for of loop if you don't need the index:

console.log(`Tags for post "${blogPost.title}":`); // Output: Tags for post "My first blog post":
for (let tag of blogPost.tags) {
  console.log(tag); // Output: coding, javascript, objects, arrays
}
