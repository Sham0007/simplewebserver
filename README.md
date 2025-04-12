# EX01 Developing a Simple Webserver
## Date:

## AIM:
To develop a simple webserver to serve html pages and display the list of protocols in TCP/IP Protocol Suite.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Import the necessary modules.

### Step 5:
Define a custom request handler.

### Step 6:
Start an HTTP server on a specific port.

### Step 7:
Run the Python script to serve web pages.

### Step 8:
Serve the HTML pages.

### Step 9:
Start the server script and check for errors.

### Step 10:
Open a browser and navigate to http://127.0.0.1:8000 (or the assigned port).

## PROGRAM:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Web Server</title>
    <style>
        /* Global Styles */
        body {
            font-family: 'Cambria', Cochin, Georgia, Times, 'Times New Roman', serif;
            background-color: #e8f1f8;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
        }

        h1 {
            color: #00334e;
            margin-bottom: 30px;
            font-size: 2rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
        }

        /* Table Styles */
        table {
            width: 90%;
            max-width: 1200px;
            margin: 20px auto;
            border-collapse: collapse;
            background: linear-gradient(to bottom, #ffffff, #f8f9fa);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
            border: 1px solid #ccdce3;
            border-radius: 8px;
            overflow: hidden;
        }

        th, td {
            padding: 15px;
            text-align: left;
            border: 1px solid #ddd;
            font-size: 1rem;
        }

        th {
            background-color: #00496b;
            color: #ffffff;
            text-transform: uppercase;
            letter-spacing: 0.05em;
        }

        td {
            color: #00334e;
            background-color: #ffffff;
        }

        tr:nth-child(even) td {
            background-color: #f4f9fc;
        }

        /* Add hover effects */
        tr:hover td {
            background-color: #dce9f3;
            color: #002c43;
        }

        /* Responsive Design */
        (max-width: 768px) {
            table {
                width: 100%;
            }

            th, td {
                padding: 10px;
                font-size: 0.9rem;
            }
        }
    </style>
</head>
<body>

    <h1>Laptop Features and Components</h1>

    <table>
        <thead>
            <tr>
                <th>Feature</th>
                <th>Details</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Processor</td>
                <td>13th Intel(R) Core(TM) i5-1224P, 1300 MHz, 10 Core(s), 12 Logical Processor</td>
            </tr>
            <tr>
                <td>Storage (HDD/SSD)</td>
                <td>SAMSUNG QXST2708THES-00BL1</td>
            </tr>
            <tr>
                <td>Memory</td>
                <td>800 GB</td>
            </tr>
            <tr>
                <td>Graphics Card</td>
                <td>Intel(R) Iris(R) Xe Graphics, NVIDIA GeForce MX550</td>
            </tr>
            <tr>
                <td>Operating System</td>
                <td>Edition: Linux, Version: 22H2, OS Build: 22621.4169</td>
            </tr>
            <tr>
                <td>RAM</td>
                <td>32.0 GB</td>
            </tr>
        </tbody>
    </table>

</body>
</html>
class myhandler(BaseHTTPRequestHandler):
   def do_GET(self):
       print("request received")
       self.send_response(200)
       self.send_headers('content-type','text/html;charset=utf-8')
       self.end_headers()
       self.wfile.write(content.encode())
server_address=('',8000)
httpd=HTTPServer(server_address,myhandler)
print("my webser is running...")
httpd.serve_forever()
```
## OUTPUT:
![Screenshot 2025-04-12 103616](https://github.com/user-attachments/assets/0553e266-d1b3-43c3-9e53-92444b1fcba2)
![Screenshot 2025-04-12 103824](https://github.com/user-attachments/assets/d3927082-26ac-410a-8e4a-522bba54706e)



## RESULT:
The program for implementing simple webserver is executed successfully.
