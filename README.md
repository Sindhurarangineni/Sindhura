Demo of OpenCV usage via the Bytedeco generated Java binding for OpenCV.

On the command line, run:

```
mvn clean install exec:java -Dplatform.dependencies -Dexec.mainClass=Stitching -Dexec.args="panorama_image1.jpg panorama_image2.jpg --output panorama_stitched.jpg --try_use_gpu yes"

```

Then take a look at the resulting file panorama_stitched.jpg/

The way that Java interoperates with OpenCV is fairly faithful to the OpenCV api.
The classes and methods (indeed many are static) in the resulting Java binding the
same case as the C++ project. 

Note: The pom file contains a classifer for Mac (64bit) usage. Other classifiers
might be better for your platform, in which case edit the pom first.