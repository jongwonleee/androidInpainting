# androidInpainting
--------------
[![](https://jitpack.io/v/jongwonleee/androidInpainting.svg)](https://jitpack.io/#jongwonleee/androidInpainting) [![API](https://img.shields.io/badge/API-21%2B-brightgreen.svg?style=flat)](https://android-arsenal.com/api?level=21)

This will fill the empty space of mask when you excute the library. This object uses patch-match algorithm to inpaint the image, it takes 20 secs to 5 minutes depends on the size of the image. 

refer to [@davidchatting](https://github.com/davidchatting/PatchMatch)

---
### Example
##### Original Image
![original](/sample/original.jpg)

##### Mask Image
![mask](/sample/mask.jpg)

##### Result Image
![result](/sample/result.jpg)

---
### Gradle
##### Root build.gradle
```gradle
allprojects {
    repositories {
         ...
        maven { url 'https://jitpack.io' }

    }
}
```

##### App build.gradle
```gradle
implementation 'com.github.jongwonleee:androidInpainting:0.10.2
```

---
### How To USe
```java
val bitmap = Inpaint().inpaint(@originalImage, @maskedImage , @calculateRadius)
```
- @original image: a bitmap image you want to get filled
- @masked image: a bitmap image which contains hole where original image wants to get filled
- @calculate radius: the smaller the radius, high quality you get, slower the algorithm
- return: a bitmap image that has filled by inpainting


---
### License
Copyright 2020 @jongwonleee

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
