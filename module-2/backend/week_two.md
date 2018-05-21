## Week Two - Module 2 Recap

Fork or re-pull this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!).

Note: When you're done, submit a PR.


### Week 2 Questions

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
  It's an ORM, provides access to database through methods.

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
  Team.first
  Team.all
  Team.create
  Team.validates

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?
  <!-- 1. Team.find(4)
  2. id = Team.find(4).owner_id
    Owner.find(id).name -->
    team = Team.find(4)
    team.name
    o = Owner.find_by(t.owner_id)
    o.name

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
  Team.find(4).owner.name



5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.

  create_table "teachers", force: :cascade do |t|
    t.string "name"
    t.datetime "created_at", null: false
    t.datetime "updated_at", null: false
  end

  create_table "students", force: :cascade do |t|
    t.string "name"
    t.datetime "created_at", null: false
    t.datetime "updated_at", null: false
    t.bigint "teacher_id"
    t.index ["teacher_id"], name: "index_students_on_teacher_id"
  end

6. Define foreign key, primary key, and schema.
    Foreign key: a column of ids on one table that provides a reference of a primary key on another table.
    Primary key: a unique ID that identifies each row of information
    schema: blueprint of how the tables are set up

7. Describe the relationship between a foreign key on one table and a primary key on another table.
  A foreign key provides a reference to a primary key in order to access the information in that table associated with that foreign key.

8. What are the parts of an HTTP response?
  <!-- GET: specifies verb, path and protocol
  Host: where the request is sent
  Accept: specifies format for client to get -->
  Status
  Headers
  Body - HTML code you requested

### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
3. What two columns does `t.timestamps null: false` create in our database?
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
6. Give an example of when you might want to store information besides ids on a join table.
7. Describe and diagram the relationship between patients and doctors.
8. Describe and diagram the relationship between museums and original_paintings.
9. What could you see in your code that would make you think you might want to create a partial?

### Self Assessment:
Choose One:
* I was able to answer a few questions independently, but relied heavily on outside resources

Choose One:
* I feel overwhelmed by the content presented this week
