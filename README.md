# 📚 Bookstore Inventory App

A modern Android inventory management application built with Kotlin for managing bookstore inventory. Track books, vendors, and inventory with an intuitive Material Design interface.

## ✨ Features

### Core Functionality
- **Book Management**: Add, edit, view, and delete book entries
- **Authentication System**: Secure login and signup functionality
- **Search & Filter**: Real-time search by book title or author
- **Vendor Management**: Track and manage book vendors and their details
- **Image Support**: Upload and display book cover images using device gallery
- **Detailed Book Information**: View comprehensive book details including:
  - Title, Author, Publisher
  - Price, Quantity, Category
  - Edition, Vendor information
  - Book cover image

### User Interface
- **Bottom Navigation**: Easy navigation between main app sections
- **Material Design**: Modern UI with CardViews and Material components
- **Edge-to-Edge Display**: Immersive full-screen experience
- **Responsive Layouts**: Optimized for various screen sizes

## 🛠️ Technical Stack

- **Language**: Kotlin 100%
- **Minimum SDK**: 24 (Android 7.0)
- **Target SDK**: 35 (Android 15)
- **Architecture**: Activity-based architecture
- **Database**: SQLite (local storage)
- **Image Loading**: Glide 4.16.0

### Dependencies
```gradle
- AndroidX Core KTX
- AppCompat
- Material Design Components
- ConstraintLayout
- Glide (Image Loading)
- JUnit & Espresso (Testing)
```

## 📱 App Screens

1. **Home Activity** (Launcher)
   - Main dashboard displaying book inventory
   - Search functionality
   - Book list with RecyclerView

2. **Login/Signup Activities**
   - User authentication
   - Shared preferences for session management

3. **Add/Edit Activity**
   - Add new books to inventory
   - Edit existing book information
   - Image picker for book covers

4. **Details Activity**
   - Detailed book view
   - Dropdown search for quick book lookup
   - Comprehensive book information display

5. **Profile Activity**
   - User profile management

6. **Vendors Activity**
   - Vendor list and management
   - Vendor details view

## 🚀 Getting Started

### Prerequisites
- Android Studio Hedgehog | 2023.1.1 or later
- JDK 11 or higher
- Android device or emulator running Android 7.0+

### Installation

1. Clone the repository:
```bash
git clone https://github.com/vanshjain99/BookstoreInventoryApp.git
```

2. Open the project in Android Studio

3. Sync Gradle files

4. Run the app on an emulator or physical device

### Permissions Required
The app requires the following permissions:
- `READ_EXTERNAL_STORAGE` (for SDK ≤ 32)
- `READ_MEDIA_IMAGES` (for SDK ≥ 33)

## 📂 Project Structure

```
app/
├── src/
│   ├── main/
│   │   ├── java/com/example/bookstoreinventoryapp/
│   │   │   ├── MainActivity.kt
│   │   │   ├── HomeActivity.kt
│   │   │   ├── LoginActivity.kt
│   │   │   ├── SignupActivity.kt
│   │   │   ├── AddEditActivity.kt
│   │   │   ├── DetailsActivity.kt
│   │   │   ├── ProfileActivity.kt
│   │   │   ├── VendorsActivity.kt
│   │   │   ├── VendorDetailsActivity.kt
│   │   │   ├── Book.kt (Data Class)
│   │   │   ├── BookAdapter.kt (RecyclerView Adapter)
│   │   │   └── BookDatabaseHelper.kt (SQLite Helper)
│   │   ├── res/
│   │   │   ├── layout/
│   │   │   ├── drawable/
│   │   │   └── values/
│   │   └── AndroidManifest.xml
│   ├── androidTest/
│   └── test/
└── build.gradle.kts
```

## 💾 Database Schema

### Books Table
```sql
- id (INTEGER, PRIMARY KEY, AUTOINCREMENT)
- title (TEXT)
- author (TEXT)
- price (TEXT)
- category (TEXT)
- quantity (INTEGER)
- publisher (TEXT)
- edition (TEXT)
- vendor (TEXT)
- imageUri (TEXT)
```

## 🔧 Key Components

### Book Data Class
```kotlin
data class Book(
    val id: Long = 0,
    val title: String,
    val author: String,
    val price: String,
    val category: String,
    val quantity: Int,
    val publisher: String,
    val edition: String,
    val vendor: String,
    val imageUri: String
)
```

### Database Operations
- Insert, Update, Delete books
- Search books by title/author
- Retrieve all books or specific book details
- Sample data population

## 🎨 Features in Detail

### Book Adapter
- RecyclerView implementation for book list
- Click handlers for view details and delete
- Glide integration for image loading
- Real-time data updates

### Authentication
- Session management using SharedPreferences
- User authentication with user_id tracking
- Automatic redirect to login if not authenticated

### Image Management
- Gallery picker integration
- Glide-based image loading with placeholders
- URI-based image storage

## 📝 Usage

1. **First Launch**: Create an account through the signup screen
2. **Login**: Use your credentials to access the app
3. **Add Books**: Navigate to Add/Edit section to add new inventory
4. **Search**: Use the search feature to find specific books
5. **View Details**: Click on any book to view detailed information
6. **Edit/Delete**: Manage inventory through edit and delete options
7. **Vendors**: Track vendor information in the Vendors section

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is available for educational and personal use.

## 👤 Author

**Vansh Jain**
- GitHub: [@vanshjain99](https://github.com/vanshjain99)

## 📱 Screenshots

_Add screenshots of your app here_

## 🔮 Future Enhancements

- Export inventory to CSV/PDF
- Barcode scanning for quick book entry
- Analytics and reporting dashboard
- Cloud sync functionality
- Multi-user support with role-based access
- Low stock alerts and notifications

## ⚠️ Known Issues

Please check the [Issues](https://github.com/vanshjain99/BookstoreInventoryApp/issues) page for known issues and feature requests.

---

**Note**: This app is designed for inventory management in bookstores and can be adapted for other retail inventory needs.
