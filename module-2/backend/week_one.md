## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.
  GET: Retrieve resource
  POST: Create a new resource
  PUT: Update entire resource
  PATCH: update partial resource
  DELETE: destroy resource

2. What is Sinatra?
  Web app frame work

4. What is MVC?
  M: Model
  V: View
  C: Controller

5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
  Code readability and ease of user interaction/familiarity

6. What types of variables are accessible in our view templates without explicitly passing them?
  Locals and Instance Variables

7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    @count = 1

    erb :inde
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
  ```ruby
  get '/horses' do

    erb :index, :locals => {:name => 'Mr. Ed'}
  end
  ```

9. What's the purpose of ERB?
  Translates Ruby to HTML

10. Why do I need a development AND test database?
  Less expensive to test

11. What is CRUD and why is it important?
  C: Create
  R: Read
  U: update
  D: Delete
  User interaction with resources

12. What does HTTP stand for?
  H: Hyper
  T:Text
  T: Transfer
  P: Protocol

13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
  <%= %> - displays on the page
  <% %> - will not display

14. What's an ORM?
  Object Relational Mappers

15. What's the most commonly used ORM in ruby (Sinatra & Rails)?
  ActiveRecord

16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
  1. GET '/' access to dashboard
  2. GET '/restaurants' index of all restaurants
  3. GET '/restaurant/new' collect info in form
  4. POST '/restaurants' saves new info
  5. GET '/restaurant/:id' finds a specific restaurant'
  6. PUT '/restaurant/:id/edit' edits a specific restaurant
  7. DELETE '/restaurant/:id' destroys specific restaurant

17. What's a migration?
  Maps data into tables

18. When you create a migration, does it automatically modify your database?
  No, just fills in the table.

19. How does a model relate to a database?
  The model can read and make changes to the database.

20. What is the difference between `#new` and `#create`?
  #new - stores in model
  #create - saves to database

### Review Questions:  
21. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  
  In terminal: `rake db:create_migration NAME=create_films`
  in migration file
  `def change
    create_table :films do |t|
      t.integer :id
      t.text    :title
      t.text :description

      t.timestamps null: false
    end`
  In terminal `rake db:migrate`

22. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone']},
  brunch: {cost: $35, supplies: ['mimosa flutes']},
  antiquing: {cost: $200, supplies: ['list of antique stores']}
}
```
How would I add 'granola bar' to things you should have when hiking?

  activities[:hiking][:supplies].push('granola bar')

23. What are the 4 Principles of OOP? Give a one sentence explanation of each.
  Encapsulation - The attributes/actions of an object live in that object like methods encapsulated in class they apply to
  Data Abstraction - Basically hiding the delegate or the controller only having access to model and view but they can't access each other.
  Polymorphism- An object can be multiple instances of classes. Ex, you have a class of IDs an ID could be both an instance of an integer and ID.
  Inheritance- You can make a class from another class in a hierarchy.

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:
* I feel comfortable with the content presented this week
