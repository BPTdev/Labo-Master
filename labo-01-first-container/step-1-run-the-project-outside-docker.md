# Step 1 - Run the project outside Docker

* [Official Source](https://docs.docker.com/language/java/build-images/)

## Get the project source code

* Clone the repo

```
git clone https://github.com/spring-projects/spring-petclinic.git
```

* Read the readme file carefully

<!---->

* [ ] What type of application is it?
* [ ] Which database engine is used?
* [ ] Do we need to install the package manager _MAVEN_ before building the project?

<!---->

* Inspect the dependencies (pom.xml)

<!---->

* [ ] Which version of Java should be compatible with the code provided?

## Setup Java components

### Check your current Java installation

* [ ] Where is Java installed?

```
[INPUT]
where java

[OUTPUT]
no result shown
```

* [ ] Which current compiler is installed (JDK)?

<pre><code><strong>[INPUT]
</strong>//TODO

[OUTPUT]
//TODO
</code></pre>

* [ ] Which current runtime is installed (JRE)?

```
[INPUT]
java -version

[OUTPUT]
java version "1.8.0_281"
Java(TM) SE Runtime Environment (build 1.8.0_281-b09)
Java HotSpot(TM) 64-Bit Server VM (build 25.281-b09, mixed mode)
```

* [ ] Do we need to install the Java virtual machine (JVM)?

```
No
```

### Install the Open JDK

* [Oracle Download WebSite](https://jdk.java.net/20/)

{% hint style="info" %}
* Accept the end user license before trying, then
* Then get the target URL (cookies).
{% endhint %}

```powershell
[INPUT]
curl -O https://download.java.net/java/GA/jdk20.0.1/b4887098932d415489976708ad6d1a4b/9/GPL/openjdk-20.0.1_windows-x64_bin.zip



[OUTPUT]
java is installed
```

#### Check the archive integrity before installing the JDK

* [Get the hash provided by Oracle](https://download.java.net/java/GA/jdk20.0.1/b4887098932d415489976708ad6d1a4b/9/GPL/openjdk-20.0.1\_windows-x64\_bin.zip.sha256)
* Generate your local hash based on the archive downloaded ([help](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/get-filehash?view=powershell-7.3))
* Compare both hashes...

```powershell
[INPUT]
certutil -hashfile ~/Download openjdk-20.0.1_windows-x64_bin.zip https://download.java.net/java/GA/jdk20.0.1/b4887098932d415489976708ad6d1a4b/9/GPL/openjdk-20.0.1_windows-x64_bin.zip.sha256


[OUTPUT]
//TODO
```

#### Unzip jdk archive

```
[INPUT]
expand -r ~/Download/openjdk-20.0.1_windows-x64_bin.zip ~/Download/openjdk-20.0.1_windows-x64_bin

[OUTPUT]
//TODO
```

#### Move the unzip folder to Programs Folder

```
[INPUT]
move ~/Download/openjdk-20.0.1_windows-x64_bin "C:\Program Files"

[OUTPUT]
//TODO
```

#### Set environment variables

* [Java official documentation](https://dev.java/learn/getting-started/)

<!---->

* [ ] Set JAVA\_HOME variable

```
[INPUT]
setx JAVA_HOME "C:\Program Files\openjdk-20.0.1_windows-x64_bin"

[OUTPUT]
//TODO
```

* [ ] Update PATH environment variable

{% hint style="info" %}
Back up your current path before updating it.

echo %PATH% > path.back
{% endhint %}

```
[INPUT]
setx PATH_BACKUP "%PATH%"
setx PATH "%PATH%;%JAVA_HOME%\bin"


[OUTPUT]
//TODO

```

* [ ] Check the variables

```
[INPUT]
echo %PATH%


[OUTPUT]
[The PATH content]

```

## Build and test the project

```
[INPUT]
I don't found it

[OUTPUT]
//TODO
```

### Result expected 

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>
