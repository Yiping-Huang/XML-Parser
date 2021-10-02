from urllib.request import urlopen
import xml.etree.ElementTree as ET
import ssl

# Ignore SSL certificate errors
ctx = ssl.create_default_context()
ctx.check_hostname = False
ctx.verify_mode = ssl.CERT_NONE


address = 'http://py4e-data.dr-chuck.net/comments_1209106.xml'
xml = urlopen(address, context=ctx).read()
tree = ET.fromstring(xml)

counts = tree.findall('.//count')
result = 0
    
for digit in counts:
    result = result + int(digit.text)

print(result)
