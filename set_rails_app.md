#Create new rails app
1.$rails new app_name  
2.$rails server  
3.http://localhost:3000 					  

#Setting Files
>Note:  
>>Step1.  Create names_controller.rb
>>>!! class name must call NamesController
>>Step2.  Create names Folder
>>step3.  Create name of method of names_controller.rb , html.erb

***
./app/controllers/users_controller.rb
```ruby
class UsersController < ApplicationController
	def index
	end

	def greet
		@show="Welcome to here!"
	end

end
```
***
./app/views/users/index.html.erb
```html
<h1>Hello World</h1>
```
./app/views/users/greet.html.erb
```html
<h1>show the greet method message</h1>
<%= @show %>
```
***
./config/routes.rb
```ruby
root 'users#index' 	 #http://localhost:3000/users/greet.html

get 'users/greet' => 'users#greet'	#http://localhost:3000/users/greet.html

resources :users
```
