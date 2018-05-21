## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?
  rails new project_name -T -d="postgresql"

2. What do Models generally inherit from in rails?
  ActiveRecord or ApplicationRecord which is same same but different

3. What do Controllers generally inherit from in a rails project?
  ApplicationController

4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
  resources :horses, only [:show]

5. What rake task is useful when looking at routes, and what information does it give you?
  $rake routes

6. What is an example of a route helper? When would you use them?
  Route helper can be seen when running rails routes and is the pointer for where the path should be so
  that you aren't writing out the URL. With the horse example above it would be horse_path(id).

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
  '_url' is absolute and must be used in a redirect with secure sites. Otherwise '_path' is a reference that will take you to the same place, for the most part, in rails.

8. What are strong params and why are they necessary?
  Strong params is a security measure to ensure only what you want to allow can be passed into your controller
  as params.

9. What role does `form_for` play in helping us create our forms?
  It provides a way to re-use the sam form for create and edit actions. It routes to the controller action needed,
  labels input fields for controller recognition and fills in partial information for editing an existing record.

10. How does `form_for` know where to submit the user's input?
  Because you pass it the object for which you want to apply the form as an argument and the action you want
  to take is passed through the correlating view. example new.html.erb or edit.html.erb

11. Create a form using a `form_for` helper to create a new `Horse`.
form file:
  <%= form_for @horse do |f| %>
    <%= f.label :name %>
    <%= f.text_field :name %>

    <%= f.submit %>
  <% end %>

new.html.erb file:
  <h2>Add Horse here!</h2>

  <%= render partial: "form" %>

12. Why do we want to validate our models?
  To make sure only valid information is saved to your database.

13. What are the steps of the DNS lookup?
  Client send web address to sever
  Server goes to Root servers to find address,
  Goes back to DNS resolver with address,
  goes tocwebsite address,
  sends back to server with info requested,
  goes back to client with page/info

### Review Questions
14. How would you call the method `prance` from within the method `move` on a `Horse` instance?
  Horse.move.prance

15. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?
  furniture[:purchased] returns true
  furniture[:table][:height] returns would return 3
  This is a nested collection and for access to 3 you have to go 2 collections deep where true can be
  accessed from the first collection layer.

16. What is inheritance?
  Gives new object to take on properties of an existing object or class. Basically this is all inception.

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week

I'm feeling stressed about having been sick this past week, the challenges and mid mod but surprisingly feel better about
a lot of this after working on my project.
I feel like more and more is starting to sink in, probably not the rate of which I need and that makes me
uncomfortable. I would definitely like to know how exactly I did on the mid mod and where I stand. 
