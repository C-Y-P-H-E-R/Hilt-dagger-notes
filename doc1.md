# `Hilt-dagger-notes`
## Doc one

### lines to be added in gradle build.
 in app/build.gradle -> add 
 {
    dependencies: 
    {
      implementation "com.google.dagger:hilt-android:2.38.1"
      kapt "com.google.dagger:hilt-compiler:2.38.1"
    }
    
    include these too at the top
    {
      id 'kotlin-kapt'
      id 'dagger.hilt.android.plugin'
    }
    complile options need to be added too 
    -------------------------------
    compileOptions {
        sourceCompatibility JavaVersion.VERSION_1_8
        targetCompatibility JavaVersion.VERSION_1_8
    }
 }
 
 lastly, add the classpath to the build.gradle 
 dependencies {
    classpath 'com.google.dagger:hilt-android-gradle-plugin:2.38.1'
 }
 
 
 ### work flow
 
 first we need to create a container class in kotlin to keep all the dependencies. 
 it has to be created in the directory containing mainactivity.kt
 then we can create a package separately containing a kotlin class, having a member method to be injected once we introduce it to the main container class.
 then we can inject it following the appropriate scope rules.
 
 creating the container class
 upon creating the file,
 the contents of the file should be as follows:
 
 
 
 
