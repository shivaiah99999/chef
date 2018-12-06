#default.rb
package "httpd" do
action :install
end
service "httpd" do
action :start
end
service "httpd" do
action :enable
end
file "/var/www/html/index.html" do
action :create
mode "0644"
content "<html><body bgcolor= #cc4488><h1>welcome to shiva</h1></body></html>"
end
