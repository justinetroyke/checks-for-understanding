### Week 5 Questions

Re-pull from this repository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

### Week 5 Questions
1. How do we make flash messages display on a page?
  In the app/layouts/application you need to put
  <% flash.each do |name, msg| %>
    <%= content_tag :div, msg, class: name %>
  <% end %>
 Then you can put the flash in the controller as
 flash[:error]
 flash[:success]
 flash[:notice]

2. Where is cart information/temporary information usually stored?
  In the session

3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?'
 It can leave a messy database, you would have to do multiple updates/delete or set a time limit to how long to keep a record on an item someone never checked out with. It would require user to log in before adding items to cart.

4. What is the purpose of the asset pipeline?
  To increase the time it takes to load a page.

5. Why do we precompile our assets?
 To organize and keep accessible

6. What do each of the following tags do?

```ruby
<%= stylesheet_link_tag "application" %>
'Tells where to retrieve styling assets'

<%= javascript_include_tag "application" %>
'Tells where to retrieve the Javascript assets'

<%= image_tag "rails.png" %>
'Retrieves image path'
```

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
Make good first impression
Including key points of the apps purpose/functionality
Point out stand out features

8. What are the top four accessibility issues that we as developers should be aware of?
Visual
Mobility
Cognition
Hearing

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
It's a callback
It lives in the model

10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)
```
 User.where(active: true)

11. What is the difference between a scope and a class method?
Scope can be used to grab what you want to without accounting for nil.
You can chains scopes together.
Class methods are easier to use with database methods or when you need more complex logic.

### Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4?  
  given[:cart]['48'] = 4

  12b. How would you increase the quantity of item 29?
  x = given.[:cart]["29"] + 1
  given[:cart]["29"] = x

  12c. How would you find out how many items your user is thinking about purchasing?  
  given[:cart].count

13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?
An object can be categorized as multiple classes and with duck-typing if it has the behavior of and responds like one object you can treat or manipulate it as such.

We use it with our ActiveRecord objects, they can behave like hashes and so you can call out information like you would a hash. 

14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  
  new = given.gsub(/[()-]/, '.').chars
  result = (new[1..4] + new[6..13]).join

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
