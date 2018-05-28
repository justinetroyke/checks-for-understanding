## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?
  An ID on the client side to link that client to their session.

2. What’s the difference between a session and a cookie?
  Session is server side and is the counterpart to the cookie in order to retrieve that client's session info

3. What’s a flash and when do you want to use flashes?
  Flash is a way to insert a temporary conditional message to a view. You can use it to confirm an added item or failed log in attempt.

4. Why do people say “HTTP is stateless”?
  Doesn't have the server require session information so each client visit whether previous or not would be like a brand new client.

5. What’s authentication? Explain.
  Let's the server know who the client is, validates their identity.

6. What’s the difference between authentication and authorization?
  Authorization is what the client is allowed to do based on their authenticated identity.

7. What’s a before filter?
  Is a way to keep cleaner code but still limit what user types can see, the traffic cop of views/access.

8. How do we keep track of a user once they’ve logged in?
  Defining them as a current_user within the application controller.

9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
  Namespacing should be done when the thing won't be it's own resource, like an admin. Nesting a resource is when you link one resource through another in order to allow dynamic access.

10. At a high level, what tools can you use to implement authorization? How would you use them?
  current_admin? helper method, if current_user == current_admin? make certain actions or views available.

  adding role to a user table as an enum

11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
  Creates a default information through an integer in ActiveRecord.
  You put it on the migration table on the row of the column header.

12. What are some strategies you can use to keep your views DRY?
  POROS
  Helper method like current_admin? on views so you don't the same page.

### Reviews Questions
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[{holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}}, {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}}, {holiday: {name: "Hanukkah", supplies: ["Menorah"]}}]
```  
  new = given.map do |holiday|
    holiday[:holiday][:name]
  end
  new.sort

14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few
More than usual! Yay!!

Choose One:
* I feel comfortable(with growing confidence) with the content presented this week


Week Four Recap
Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.
