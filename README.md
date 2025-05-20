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
  <img src="screenshots/screenshot1.jpg" width="250" alt="Main Screen"/>
  <img src="screenshots/screenshot2.jpg" width="250" alt="Detail Screen"/>
  <img src="screenshots/screenshot3.jpg" width="250" alt="Profile Screen"/>
</div>

## 🛠️ Technical Implementation

### Dependencies

The app utilizes several key libraries:

```gradle
dependencies {
    // CircleImageView for rounded profile images
    implementation 'de.hdodenhof:circleimageview:3.1.0'
    
    // Other dependencies
    implementation 'androidx.core:core-ktx:1.10.1'
    implementation 'androidx.appcompat:appcompat:1.6.1'
    implementation 'com.google.android.material:material:1.9.0'
    implementation 'androidx.constraintlayout:constraintlayout:2.1.4'
    // Add other dependencies here
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
    binding = DataBindingUtil.setContentView(this, R.layout.activity_main)
    
    // Now you can access views directly through binding
    binding.yourViewModel = viewModel
    binding.lifecycleOwner = this
}
```

### Layout Structure

The app implements a hierarchical layout structure:

1. **ScrollView** as the root container
2. **LinearLayout** with vertical orientation as the direct child of ScrollView
3. Multiple **ConstraintLayout** containers as children of the LinearLayout

```xml
<ScrollView
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical">

        <!-- First ConstraintLayout child -->
        <androidx.constraintlayout.widget.ConstraintLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:padding="16dp">

            <!-- CircleImageView implementation -->
            <de.hdodenhof.circleimageview.CircleImageView
                android:id="@+id/profile_image"
                android:layout_width="96dp"
                android:layout_height="96dp"
                android:src="@drawable/profile"
                app:civ_border_width="2dp"
                app:civ_border_color="#FF000000"
                app:layout_constraintStart_toStartOf="parent"
                app:layout_constraintTop_toTopOf="parent"/>

            <!-- Other views within this ConstraintLayout -->
            
        </androidx.constraintlayout.widget.ConstraintLayout>

        <!-- Second ConstraintLayout child -->
        <androidx.constraintlayout.widget.ConstraintLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:padding="16dp">
            
            <!-- Content for second section -->
            
        </androidx.constraintlayout.widget.ConstraintLayout>

        <!-- Additional ConstraintLayout children as needed -->
        
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

## 📋 To-Do

- [ ] Add feature X
- [ ] Improve UI for screen Y
- [ ] Fix bug Z

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Contact

Your Name - [@yourtwitter](https://twitter.com/yourtwitter) - email@example.com

Project Link: [https://github.com/yourusername/your-app-name](https://github.com/yourusername/your-app-name)
