# NALTTI  ReadMe
Description

Naltti Scarves is a single page application using the MERN stack to give users the ability to see a range of silk scarves. The project was done in 3 days.


Deployment link

https://scarvesnaltti-2b2495217c08.herokuapp.com/

Getting Started/Code Installation

The app has been deployed using heroku and my code can be accessed on GitHub @renad1999

Timeframe & Working Team (Solo/Pair/Group)

Instructions

I had 1 week to work on it but only managed to get work done in the last 3 days due to  health issues. It was a solo project. I worked on getting a functional single page application using MongoDB, React, Node, Express, JavaScript and CSS.


Technologies Used


MongoDB, Express, React, Node, CSS, JavaScript

Mongo DB helps in storing data in a document oriented format which allows handling of large volumes of data and provides flexibility in data structure. 

 Express allows for a flexible web application framework for Node.js. It helps simplify the process of building web apps and APIs by providing a  set of powerful features and middleware.

 React is a powerful JavaScript library for building user interfaces. It helps create reusable UI components and efficiently manage the state of the web application. 
Node.js is a JavaScript runtime built on Chrome's V8 engine making it easy to build scalable and real-time applications



Brief

☐ A working full-stack, single-page application hosted on Heroku.
☐ Incorporate the technologies of the MERN-stack:
MongoDB/Mongoose
Express
React
Node
☐ Have a well-styled interactive front-end.
☐ Communicates with the Express backend via AJAX.
☐ Implement token-based authentication. Including the ability of a user to sign-up, log in & log out.
☐ Implement authorization by restricting CUD data functionality to authenticated users. Also, navigation should respond to the login status of the user.
☐ Have a well-scoped feature-set. Full-CRUD data operations are not required if one or more other features are included, for example:
Consume data from a third-party API.
Implement additional functionality if the user is an admin.
Implementation of a highly dynamic UI or data visualisation.
Other, instructor approved, complexity/features.


The minimum viable product was to have a single page app that has full CRUD working.

Planning

<img width="627" alt="Screenshot 2023-08-17 at 01 51 36" src="https://github.com/renad1999/naltti/assets/112344006/c323deef-c862-48fc-aec4-fe1b56072af0">
<img width="530" alt="Screenshot 2023-08-17 at 01 52 16" src="https://github.com/renad1999/naltti/assets/112344006/6ef9a9fd-08b6-48c8-868a-6b24148fdd1c">
<img width="566" alt="Screenshot 2023-08-17 at 01 52 32" src="https://github.com/renad1999/naltti/assets/112344006/1993c591-131c-4cd7-acf7-17d385aef0be">

Those are the wireframes of what the original website was going to be like, giving users the option to view clothes, choose the correct size and to add a review . 



The ERD was going to link between the products, category, user, shopping cart item and review components. 
<img width="676" alt="Screenshot 2023-08-17 at 01 53 00" src="https://github.com/renad1999/naltti/assets/112344006/f1d4b912-5dfe-4695-85e5-2b8369623417">


Build/Code Process


<img width="620" alt="Screenshot 2023-08-17 at 01 54 17" src="https://github.com/renad1999/naltti/assets/112344006/fbea4318-01da-4fed-8fa7-ea7eeea0b02f">


This piece of code is used to display item details on a webpage. First, it logs the user's ID to the console. Then, within a containing <div>, it sets up the layout for displaying item information. It includes an <h1> heading indicating that this is the "Item Details" page. Inside the layout, there's a condition: if an item is available (presumably fetched from some data source), it displays the item's image, name, price, and description within a list. The image is shown using an <img> tag with the src attribute set to the item's image URL. The name, price, and description are displayed as separate paragraphs. On the other hand, if the item isn't available yet, it displays a message indicating that the item details are currently being loaded. This code snippet effectively creates a user interface to show item details while providing feedback during loading.



Some people will document the build/code process by discussing the key stages they worked on. Others will do a day by day guide. It’s entirely up to you how you structure this, as long as you discuss all the key things above.

Insert your Build/Code Process here:

Building this application was interesting, I wanted to make sure I was able to achieve the things I needed within the time frame I had.
The code below was my first time trying to add testimonials to my website to make it look like real people have left their reviews. After searching up how to do it online, I figured it out. It  was much simpler than I thought and it gave the website the look and feel I was going for!



const testimonialsData = [
 {
   id: 1,
   name: 'Sara Al',
   text: 'I absolutely love the scarves I ordered from Naltti! They are stunning and of excellent quality. Highly recommended!',
   photo: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSxnyIPaIgyvVqQZARwGPJiNDPfJGiwPc41VA&usqp=CAU'
 },
 



const handleSubmit = async (e) => {
e.preventDefault();


const itemData = { name, price, description, image };


const response = await fetch('/api/items', {
method: 'POST',
body: JSON.stringify(itemData),
headers: {
'Content-Type': 'application/json'
}
});
const json = await response.json();


if (!response.ok) {
setError(json.error);
setEmptyFields(json.emptyFields || []);
} else {
setName('');
setPrice('');
setImage('');
setDescription('');
setError(null);
setEmptyFields([]);
console.log('New Item Added', json);
dispatch({ type: 'CREATE_ITEM', payload: json });
}
};

The code above defines a function called handle submit that manages the submission of a form for adding new items. When the form is submitted, the function prevents the default behaviour to avoid page reloading. It gathers data like item name, price, description, and image, and sends this data as a JSON payload to an API endpoint using the fetch function. The API response is then awaited and processed as JSON. If the response indicates an error, the function updates the error message and highlights any empty fields. On a successful response, the input fields are cleared, error messages are removed, and the new item information is logged to the console.




Challenges

The biggest challenge for me was that I initially wanted to build an clothing e-commerce site but due to some issues and careful consideration on what I will be able to complete with the time I had left I decided to change the initial plan to the Silk Scarves webpage. 


Wins

A win for me was doing a MERN Stack app, along with all the challenges I faced personally. I enjoyed how simple React can be if we understand how to use it and optimise it to give users an easier and quicker experience.


Key Learnings/Takeaways

I feel more confident using React, understanding how to use components. I also enjoy styling on MERN stack more than I did on any other language.
I learnt how important it is to prioritise mental health to be able to always give the best work possible and to portray the capabilities I know I possess. 



Bugs


My wishlist button is not working, and my update form is not what i intended it to be. It should have the scarf item details already showing in each slot for the user to only change what they would like. I would like the user to be able to add and delete items from their wishlist along with the cart. I would also like to add more pictures for each item with the appropriate descriptions needed for an ecommerce website.

Future Improvements


The future improvements I would like to implement is to get the website to have the initial plan I wanted it to have. For it to be a clothing e-commerce website allowing the user to be able to choose between sizes, add items to their cart and to their wishlist and to give them the ability to add and delete items from their cart and from their wishlist. 
