# Step 1 - Run the project outside Docker

* [Official Source](https://docs.docker.com/language/java/build-images/)

## Get the project source code

* Clone the repo

```
git clone https://github.com/spring-projects/spring-petclinic.git
```

* Read carefully the readme file

<!---->

* [ ] What type of application is it ? 
`Heavy application`
* [ ] Which database engine is used ?
`mysql`
* [ ] Do we need to install the package manager _MAVEN_ before building the project ?
`yes if we want to auto build the project`
<!---->

* Inspect the dependencies (pom.xml)

<!---->

* [ ] Which version of Java should compatible with the code provided ?

## Setup Java components

### Check your current java installation

* [ ] Where is java installed ?

```
[INPUT]
where java

[OUTPUT]
C:\Program Files (x86)\Common Files\Oracle\Java\javapath\java.exe
```

* [ ] Which current compiler is installed (JDK) ?

```
[INPUT]
java -version

[OUTPUT]
java version "1.8.0_281"
Java(TM) SE Runtime Environment (build 1.8.0_281-b09)
Java HotSpot(TM) 64-Bit Server VM (build 25.281-b09, mixed mode)
```

* [ ] Which current runtime is installed (JRE) ?

```
[INPUT]
java -version

[OUTPUT]
java version "1.8.0_281"
Java(TM) SE Runtime Environment (build 1.8.0_281-b09)
Java HotSpot(TM) 64-Bit Server VM (build 25.281-b09, mixed mode)
```

* [ ] Do we need to install the java virtual machine (JVM) ?


```
No its not required
```

### Install the Open JDK

* [Oracle Download Web Site](https://jdk.java.net/20/)

{% hint style="info" %}
* Accept the end user license before trying, then
* Then get the target url (cookies.
{% endhint %}

```
[INPUT]
//TODO
curl https://download.java.net/java/GA/jdk20.0.1/b4887098932d415489976708ad6d1a4b/9/GPL/openjdk-20.0.1_windows-x64_bin.zip --output
[OUTPUT]
//TODO
```

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption><p>Powershell output during sdk download process</p></figcaption></figure>

#### Check the archive integrity before installing the JDK

* [Get the hash provided by Oracle](https://download.java.net/java/GA/jdk20.0.1/b4887098932d415489976708ad6d1a4b/9/GPL/openjdk-20.0.1\_windows-x64\_bin.zip.sha256)
* Generate your local hash based on the archive downloaded ([help](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/get-filehash?view=powershell-7.3))
* Compare both hashes...

```
[INPUT]
//TODO

[OUTPUT]
//TODO
```

#### Unzip jdk archive

```
[INPUT]
//TODO

[OUTPUT]
//TODO
```

<figure><img src="../../.gitbook/assets/image (4) (1).png" alt=""><figcaption><p>Powershell output during unzip process</p></figcaption></figure>

#### Move the unzip folder to Progams Folder

```
[INPUT]
//TODO

[OUTPUT]
//TODO
```

#### Set environment variables

* [Java official documentation](https://dev.java/learn/getting-started/)

<!---->

* [ ] Set JAVA\_HOME variable

```
[INPUT]
> set JAVA_HOME=C:\tools\JDK\jdk-20.0.1


[OUTPUT]
//TODO
```

* [ ] Update PATH environment variable

{% hint style="info" %}
Backup your current path before updating it.

echo %PATH% > path.back
{% endhint %}

```
[INPUT]
//TODO

[OUTPUT]
//TODO
```

* [ ] Check the variables settings

```
[INPUT]
//TODO

[OUTPUT]
//TODO
```

## Build and test the project

```
[INPUT]
//TODO

[OUTPUT]
//TODO
```


### Result expected 

```
[INPUT]
//TODO

[OUTPUT]
//TODO
```