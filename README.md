# EX01 Developing a Simple Webserver

# Date: 24-07-2026

# AIM:
To develop a simple webserver to serve html pages and display the configuration details of laptop.

# DESIGN STEPS:
## Step 1:
HTML content creation.

## Step 2:
Design of webserver workflow.

## Step 3:
Implementation using Python code.

## Step 4:
Serving the HTML pages.

## Step 5:
Testing the webserver.

# PROGRAM:

```
from http.server import HTTPServer, BaseHTTPRequestHandler
content='''<html>
<h1>Hello everyone!!!</h1>
</html>'''
class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request recieved...")
        self.send_response(200)
        self.send_header("content-type", "text/html")
        self.end_headers()
        self.wfile.write(content.encode())
print("This is my webserver")
server_address=('',8000)
httpd= HTTPServer(server_address,MyServer)
httpd.serve_forever()
```

# OUTPUT:

<img width="1917" height="1078" alt="image" src="https://github.com/user-attachments/assets/d4d94f79-d34b-4407-ad4d-056f3b8a6542" />


<img width="1102" height="263" alt="Screenshot 2026-07-21 144756" src="https://github.com/user-attachments/assets/424d1a67-b7fd-4414-8377-028e302d5ae0" />

# RESULT:
The program for implementing simple webserver is executed successfully.
