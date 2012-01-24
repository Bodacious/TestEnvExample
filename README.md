[App for this question on stack overflow.](https://github.com/Bodacious/TestEnvExample)

In my Rails app, I'm accessing the env hash in one of my controller actions.

Something along the lines of:

``` ruby
def my_before_filter
  env['some.key'] = "Something or other"
end
```

This works great for my requirements.

If I start my Rails app in test environment, and visit an action like:

``` ruby
# /users in UsersController#index
def index
  puts env.inspect
end
```

Then the content of the env hash is output to the console as expected.

When I get this action from within an RSPec example, the output is an empty hash?

``` ruby
it 'should get the index action' do
  get :index
end
```

```
.....{}.... # rspec output
``` 

**Why is the env hash empty?**
