![image](https://user-images.githubusercontent.com/70546234/194403276-912687e3-4a92-429c-b643-66e0a317187f.png)
## Classes
### Recipe
Included essentially as a way to conveniently refer to a recipe with ingredients and a name, rather than storing them separately. A list of them will be in the database, and is managed by the `RecipeManager`.
### RecipeManager
A layer between the database and the recipes themselves, which handles getting recipes from the database and holding data about them so they can be operated on. Essentially a collection of recipes with related methods.
### Exercise
A way to conveniently refer to a specific exercise, much in the same way as `Recipe`s, with instructions and a name. A list of them is in the database, controlled by `ExerciseManager`.
### ExerciseManager
A layer between the database and the exercises themselves, which handles getting exercises from the database and holding data about them so they can be operated on and displayed. A collection of exercises with related methods, similar to the `RecipeManager`.
### ExerciseLog
A logged exercise by a user to be used in the exercise logging system. Will be displayed as a point on the exercise timeline, and stores information about itself, like what `type` of `Exercise` it is.
### User
A way to store user information, which currently only includes a user's `ExerciseLog`s. Basically just a way to aggregate `ExerciseLog`s together into a list.
### Controller
A layer between the UI and backend, which is used to call methods from classes like `RecipeManager` and `ExerciseManager`. The 'C' of MVC.
### DatabaseManager
The class that actually interacts with the database. Can get items from the database which can be specified with a parameter, likely a SQL command.
