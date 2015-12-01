#Create new rails app
1.rails new app_name  #open terminal  
2.rails server  
3.localhost 					#open Browser  

#Set files
./app/controllers/users_controller.rb
```ruby
class UsersController < ApplicationController
	def index
	end
end
```
***
./app/views/users/index.html.erb
```html
<h1>Hello World</h1>
```
***
./config/routes.rb
```ruby
root 'users#index'  

get 'users/greet' => 'users#greet' #new files (greet.html.erb),new method greet in UsersController.rb

resources :users

