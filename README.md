# AndrazKumarAssignment

A modern Android application featuring a scrollable UI with CircleImageView implementation, data binding, and a structured layout hierarchy.

## 📱 Overview

It is an Android application that showcases best practices in UI design and modern Android development techniques. The app implements a scroll view with linear layout (vertical orientation) as the parent container, which hosts multiple constraint layouts as child elements.

## ✨ Features

- Implementation of CircleImageView for rounded profile images
- Data binding for efficient view access and management
- Custom Drawable background
- Structured layout hierarchy with ScrollView, LinearLayout, and ConstraintLayout

## 📸 Screenshots

<div align="center">
  <p>
    <img src="screenshots/Screenshot 2025-05-20 112232.png" width="250" alt="Profile Screen" />
  </p>
  <img src="screenshots/Screenshot 2025-05-20 111915.png" width="450" height="320" alt="Main Screen"/> <img src="screenshots/Screenshot 2025-05-20 111954.png" width="450" height="320" alt="Detail Screen"/>
  <img src="screenshots/Screenshot 2025-05-20 112011.png" width="450" height="320" alt="Profile Screen"/> <img src="screenshots/Screenshot 2025-05-20 112029.png" width="450" height="320" alt="Profile Screen"/>
  <img src="screenshots/Screenshot 2025-05-20 112046.png" width="450" height="320" alt="Profile Screen"/> <img src="screenshots/Screenshot 2025-05-20 112327.png" width="450" height="320" alt="Profile Screen"/>
</div>


## 🛠️ Technical Implementation

### Dependencies

The app utilizes several key libraries:

```gradle
dependencies {
    // CircleImageView for rounded profile images
    implementation("de.hdodenhof:circleimageview:3.1.0")
    
    // Other dependencies
    implementation("androidx.core:core-ktx:1.10.1")
    implementation("androidx.appcompat:appcompat:1.6.1")
    implementation("com.google.android.material:material:1.9.0")
    implementation("androidx.constraintlayout:constraintlayout:2.1.4")
}
```

### Data Binding

Data binding is implemented to eliminate boilerplate code for UI operations:

```kotlin
// In build.gradle
android {
    buildFeatures {
        dataBinding true
    }
}

// In your Activity/Fragment
private lateinit var binding: ActivityMainBinding

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)

        binding = ActivityMainBinding.inflate(layoutInflater)
        setContentView(binding.root)
    }
```

### Layout Structure

The app implements a hierarchical layout structure:

1. **ScrollView** as the root container
2. **LinearLayout** with vertical orientation as the direct child of ScrollView
3. Multiple **ConstraintLayout** containers as children of the LinearLayout

```xml
[NOTE: It a demo code for reference, not the actual code used in the assignment]
<?xml version="1.0" encoding="utf-8"?>
<ScrollView xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#161616"
    tools:context=".MainActivity">
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical">


        <androidx.constraintlayout.widget.ConstraintLayout
            android:id="@+id/topBar"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:paddingVertical="24dp"
            app:layout_constraintTop_toTopOf="parent">
            <androidx.cardview.widget.CardView
                android:id="@+id/supportCard"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_marginEnd="16dp"
                app:cardBackgroundColor="#333333"
                app:cardCornerRadius="24dp"
                app:layout_constraintBottom_toBottomOf="parent"
                app:layout_constraintEnd_toEndOf="parent"
                app:layout_constraintTop_toTopOf="parent">
        </androidx.constraintlayout.widget.ConstraintLayout>
    </LinearLayout>
</ScrollView>
```

## 🚀 Getting Started

### Prerequisites

- Android Studio Arctic Fox or newer
- Android SDK 21 or higher
- Gradle 7.0+

### Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/your-app-name.git
```

2. Open the project in Android Studio

3. Sync Gradle files

4. Run the app on an emulator or physical device


## 📞 Contact

- Your Name - Rishi2705 
- email@rishiarora2705@gmail.com
- Project Link: [https://github.com/yourusername/your-app-name](https://github.com/Rishi2705/AndazKumarAssignment)
