Demo project for using OpenCV from a generated Java binding (Bytedeco's jars made with JavaCPP)

On the command line, run:

```
mvn clean install exec:java -Dplatform.dependencies -Dexec.mainClass=Stitching -Dexec.args="panorama_image1.jpg panorama_image2.jpg --output panorama_stitched.jpg --try_use_gpu yes"

```
First time through, this is going to go off to Maven's central repo and download Bytedeco, including the libraries for Windows, Linux and Mac (regardless of your current platform). 

After running the above, take a look at the resulting file panorama_stitched.jpg.  The two pictures to
stitch are taken from [Ramsri Goutham's blog entry on stitching panoramas with OpenCV](http://ramsrigoutham.com/2012/11/22/panorama-image-stitching-in-opencv).

The way that Java interoperates with OpenCV is fairly faithful to the OpenCV api, including capitalization.
The classes and methods in the resulting Java binding the
same case as the C++ project. Indeed many are static methods.

There's command line passing going on, which strictly speaking is not really needed for
a demo, as file names could be hard coded. It allows you to experiment a little,
though.

Note: The pom file contains a classifer for Mac (64bit) usage. Other classifiers
might be better for your platform, in which case edit the pom first, commenting out/in lines as appropriate.

After running the demo, you should be comfortable enough to use OpenCV in a Java solution of your own.