# Contents and Quick Notes

(Big) Data Engineering:

"Typical data modeling techniques — like the star schema — which defined our approach to data modeling for the analytics workloads typically associated with data warehouses, are less relevant than they once were.more generally, it’s arguable to say that with the commoditization of compute cycles and with more people being data-savvy then before, there’s less need to precompute and store results in the warehouse. For instance you can have complex Spark job that can compute complex analysis on-demand only, and not be scheduled to be part of the warehouse.
--The Rise of Data Engineering"
https://medium.freecodecamp.org/the-rise-of-the-data-engineer-91be18f1e603

Python Learning Resource:
1. Import Python data into SQL:
  1)https://stackoverflow.com/questions/29287946/programmingerror-the-sql-contains-1-parameter-markers-but-2-parameters-were
  2)https://stackoverflow.com/questions/30984968/pyodbc-sql-server-typeerror-not-all-arguments-converted-during-string-formatt

#Python Time Series Resource: 
https://jakevdp.github.io/PythonDataScienceHandbook/03.11-working-with-time-series.html

API Parameters: 
headers = {"Content-type": "application/x-www-form-urlencoded",  
        "Accept": "application/json","Content-type":"application/xml; charset=utf=8"}  
conn = httplib.HTTPConnection("www.xxx.com")  
conn.request("GET","/get?id=1","",headers)  
response = conn.getresponse()  
print "Return code:", response.status, " reason:", response.reason  
print response.status  
if response.status == 200:  
    usersdata = response.read()  
    user = json.loads(usersdata)  
    print user[0]  
else:  
    print "Error sending message,check your account" 

#Deal with Json Data: 
import json  
json_class = json.JSONDecoder()  
a = json_class.raw_decode(jstr)  
print a  
 
b = json_class.decode(jstr)  
print b  
  
c = json.loads(jstr)  
print c  


Create executable GUI app by Python: 

First you will need some GUI library with Python bindings and then (if you want) some program that will convert your python scripts into standalone executables.

Cross-platform GUI libraries with Python bindings (Windows, Linux, Mac)

Of course, there are many, but the most popular that I've seen in wild are:

Tkinter - based on Tk GUI toolkit (de-facto standard GUI library for python, free for commercial projects)
WxPython - based on WxWidgets (very popular, free for commercial projects)
PyQt - based on Qt (also very popular and more stable than WxWidgets but costly license for commercial projects)
Complete list is at http://wiki.python.org/moin/GuiProgramming

Single executable (Windows)

py2exe - Probably the most popular out there (PyInstaller is also gaining in popularity)
Single executable (Linux)

Freeze - works the same way like py2exe but targets Linux platform
Single executable (Mac)

py2app - again, works like py2exe but targets Mac OS
*source: https://stackoverflow.com/questions/2933/how-can-i-create-a-directly-executable-cross-platform-gui-app-using-python
