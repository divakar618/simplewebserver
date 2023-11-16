# Developing a Simple Webserver
## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation
### Step 2:
Design of webserver workflow
### Step 3:
Implementation using Python code
### Step 4:
Serving the HTML pages.
### Step 5:
Testing the webserver

## PROGRAM:

'''
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html>
<head>
<title>My webserver</title>
</head>
<body>
<h1><u>Top 5 Revenue Generating Companies</u><h1>
<ul>
<li>Apple</li>
<li>Amazon</li>
<li>Microsoft</li>
<li>Samsung</li>
<li>Google</li>
</body>
</html>
"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
```

# Top Five Web Application Development Frameworks

## 1.Apple 
## 2.Amaozon
## 3.Microsoft
## 4.Samsung 
## 5.Google



## OUTPUT:

![Screenshot 2023-10-30 205752](https://github.com/divakar618/simplewebserver/assets/121932143/614a96b0-5c02-42d0-8fad-1f82fa0f0095)


## RESULT:
The program for implementing simple webserver is executed successfully.
