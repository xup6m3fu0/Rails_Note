###Controller for 新增、修改、閱讀、刪除

app/controllers/app_controller.rb

```ruby
class AppsController < ApplicationController

	def index  #for index.html.erb
    @apps=App.all
	end

  def show 
    @app=App.find(params[:id])
  end

  def new   #submit to create 
    @app=App.new
  end

  def edit  #submit to update
    @app=App.find(params[:id])
  end

  def create
    @app=App.new(app_params)

    if @app.save@!   #notice app.save will be execute
      redirect_to root_path
    end
  end

  def update
    @app=App.find(params[:id])
    @app.update(app_params)
    redirect_to root_path
  end

  def destroy
    @app=App.find(params[:id])
    @app.destroy
    redirect_to root_path
  end

  private     #must last!
  def app_params
    params.require(:table).permit(:cols,:cols...)
  end

end


```
