**Android Jetpack masterclass in Kotlin**

If you follow this lessons on chapter Navigation from lessons 14 - 17, and working on android studio Arctic Fox
pay attention to change in 

* build.gradle (project level)

dependencies {

        classpath "com.android.tools.build:gradle:7.0.3" (change 7.0.4 to 7.0.3 - bcz 7.0.4 have problems to work with dataBinding)
        
        def nav_version = "2.4.1"
        
        classpath("androidx.navigation:navigation-safe-args-gradle-plugin:$nav_version")  (add navigation-safe-args-gradle-plugin)
        
        }
        
* at build.gradle (app level)

plugins {

    id 'kotlin-kapt'
    
    id "androidx.navigation.safeargs"
    
    }
    
* add at android in build.gradle (app level)   
 
android {

    buildFeatures {
    
        dataBinding true
        
    }
    
    }
    
* Then will be changes in both fragments - look at DetailFragment.kt and ListFragment.kt

* and in MainActivity.kt - we will use supportFragmentManager
    
    
    
    
    

