# Developing a Simple Webserver
Name:  PYNAM VINODH
ID:  23004069
Email : pynamvinodh6@gmail.com
# AIM:

Develop a webserver to display about top five web application development frameworks.

# DESIGN STEPS:

## Step 1:

HTML content creation is done

## Step 2:

Design of webserver workflow

## Step 3:

Implementation using Python code

## Step 4:

Serving the HTML pages.

## Step 5:

Testing the webserver
# PROGRAM:
```from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
<head>
<body>
<h1>Welcome</h1>
</body>
</head>
</html>
"""

class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request recieved")
        self.send_response(200)
        self.send_header('Content-type','text/html;charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my webserver")
server_address = ('',80)
httpd = HTTPServer(server_address,HelloHandler)
```
# OUTPUT:
![image](https://github.com/PYNAMVINODH/Web_server/assets/145742678/e73e0d69-a3ff-4392-9f19-27498c4f8ccf)

# RESULT:

The program is executed succesfully
