# SamsungSmartTV

Warning: This app is a legacy program meant for older Samsung Smart TVs running Orsay (pre-2015), which has since been replaced by Tizen. It may be possible to use this app by side-loading, but it is considered unsupported (we are unable to help you with it).

You may also wish to try a web browser with Jellyfin, wherever possible.

---

This app is working just fine in any Samsung Legacy TV model, running Orsay (pre-2015), aka non Tizen. You can see a list of Samsung TV models here

As for the installation guide, you can use a usb stick(should be connected to the tv at all times) or download the zip and host it on your own web server

Jellyfin Legacy Samsung app installation instructions for Windows server:

Download the zip file jellyfin-samsungtv-master.zip.
Extract content and zip all content of the jellyfin-samsungtv-master folder to a new zip file called ex. jellyfin.zip.Copy the zip file to a subfolder ex: Widgets under the root of the default download folder on your web server
I'm using IIS and the zip file is in:
C:\inetpub\wwwroot\Widgets\jellyfin.zip (example filename)

Create a file called widgetlist.xml in the root folder
C:\inetpub\wwwroot\widgetlist.xml

Place this information in the xml file changing the IP to your web server's IP and the filename if needed.

<rsp stat="ok">
<list>
<widget id="Jellyfin">
<title>jellyfin</title>
<compression type="zip" size="919000"/>
<description/>
<download>http://192.168.x.x/Widgets/jellyfin.zip</download>
</widget>
</list>
</rsp>
Install the app using your own web server's IP and the appropriate instructions for your model year TV. Look here
