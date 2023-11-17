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
```
<!DOCTYPE html>
<html>
<head>
<title>My webserver</title>
</head>
<body  bgcolor="lightblue">
<h1>TOP 5 LARGEST SOFTWARE COMPANIES IN THE WORLD</h1>
<br>
<br>
<h2>
    <ol>
        <li>GOOGLE</li>
        <li>APPLE</li>
        <li>AMAZON</li>
        <li>TESLA</li>
        <li>MICROSOFT</li>
    </ol>
</h2>
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



## OUTPUT:

![Screenshot 2023-10-30 205752](https://github.com/divakar618/simplewebserver/assets/121932143/614a96b0-5c02-42d0-8fad-1f82fa0f0095)


## RESULT:
The program for implementing simple webserver is executed successfully.
