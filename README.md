# Recipe Tracking App

>A frontend CRUD application for creating, editing, displaying, tracking, and deleting recipes
## Languages

- React, Javascript, HTML5, CSS, Bootstrap

## What it does

1. Create new recipes
   * RecipeCreate creates a form on screen for users to type in new recipes and submit them to the page to be displayed
   * Stores its own state for form inputs
   * Uses ```createRecipe()``` as props to handle when user submits the form
2. Format new recipes
   * RecipeFormat handles the input of a single recipe, and returns it formatted as a ```<tr>``` element with nested ```<td>``` elements for each key-value of the recipe
   * Adds a delete button to the recipe, using ```handleDelete()``` when button is clicked
3. List all available recipes
   * RecipeList renders full table display for all current recipes, using RecipeFormat to map the list of recipes to ```<tbody>``` element
4. App component
   * Stores state for recipes, so all children have access if needed through props
   * Holds ```handleDelete()``` and ```createRecipe()``` methods to manage state of recipes, methods are passed to children as props
   * Returns ```<div>``` element with a header, our RecipeList table display, and the RecipeCreate form
