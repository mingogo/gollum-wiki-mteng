To check the user name and password before accessing the wiki, use the following configuration:

```rb
# authentication.rb
module Precious
  class App < Sinatra::Base
    use Rack::Auth::Basic, "Restricted Area" do |username, password|
      [username, password] == ['admin', 'admin']
    end
  end
end
```