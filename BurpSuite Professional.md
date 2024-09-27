Download the BurpSuite pro cracked version latest from Dr.FarFar website for free.

Extract the file in to `/opt` Directory
```sh
cd /path/to/burpsuite/pro
```

Check if Java is available.
```sh
java --version
```

Run `Dr-FarFar.jar`
```sh
./Dr-FarFar.jar
```

When running for the first time we will have to setup the license for this application.

Click on `run` in the launcher
![[Attachments/Pasted image 20240825023455.png]]

It will launch the BurpSuite professional window for license activation.

Copy the License Key from the Private Loader and paste in burp license window. Follow the steps and activate the burp license.

Create a desktop launcher in Desktop
```sh
# Create a launcher on desktop
# Give it a name as Burpsuite-pro.desktop
# Give it an icon 
# Fill in the command field as below.
"/usr/lib/jvm/java-23-openjdk-amd64/bin/java" "--add-opens=java.desktop/javax.swing=ALL-UNNAMED" "--add-opens=java.base/java.lang=ALL-UNNAMED" "--add-opens=java.base/jdk.internal.org.objectweb.asm=ALL-UNNAMED" "--add-opens=java.base/jdk.internal.org.objectweb.asm.tree=ALL-UNNAMED" "--add-opens=java.base/jdk.internal.org.objectweb.asm.Opcodes=ALL-UNNAMED" "-javaagent:Dr-FarFar.jar" "-noverify" "-jar" "/opt/Burp Suite Professional Edition v2024.7.3 x64 Full Activated + Extensions - WwW.Dr-FarFar.CoM/Burp Suite Professional Edition/burpsuite_pro_v2024.7.3.jar" 
```

![[Attachments/Pasted image 20240825023846.png]]

```sh
# Move the file
cd /path/to/burp/pro/directory
mv ~/Desktop/Burpsuite-Pro.desktop ./
```

Create a bash script for easy execution
Call it `Burpsuite-Pro`
```sh
#!/usr/bin/sh

cd '/opt/Burp Suite Professional Edition v2024.7.3 x64 Full Activated + Extensions - WwW.Dr-FarFar.CoM/Burp Suite Professional Edition'
xdg-open BurpSuite\ Professional.desktop
````

Change the permission
```sh
chmod +x Burpsuite-pro
```

Move or Copy the file to an environment path for exection
```sh
sudo cp Burpsuite-pro /usr/local/bin/
```

Now the `Burpsuite` will be executable from anywhere.
```sh
Burpsuite-pro &
```