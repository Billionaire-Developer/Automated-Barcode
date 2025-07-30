# 📚 Educational Dashboard with Barcode Access

A simple front-end web application for navigating categorized educational content using a dashboard. Users register, log in, and access subcategories of lessons that are unlocked via barcode scanning.

---

## 🔐 User Flow

1. **Register** a new account via `register.html` (auto login after register).
2. **Login** via `login.html` to access the dashboard.
3. On **dashboard.html**, users see 3 main category cards:
   - Science
   - Commercial
   - Art
4. Clicking a category opens `category.html?category=science`, listing its subcategories.
5. Clicking a subcategory opens `subcategory.html?category=science&sub=physics`, showing content files.
6. Clicking a file triggers `scanner.html` for barcode simulation.
7. After scanning, the app redirects to `content.html?file=lesson1`, displaying the unlocked file content.

---

## 🗂️ Project Structure

project-folder/
├── index.html # Entry point
├── register.html # New user registration
├── login.html # User login page
├── dashboard.html # Main dashboard with categories
├── category.html # Lists subcategories of a category
├── subcategory.html # Displays content files under a subcategory
├── scanner.html # Simulates barcode scanning
├── content.html # Final content display page
├── data.json # Static content structure (categories, subcategories, files)
├── Auth.js # Handles login/registration logic using localStorage
├── styles.css # Shared styles across pages
├── README.md # Project documentation


---

## 🧠 Technologies Used

- HTML5  
- CSS3  
- JavaScript (Vanilla)  
- `localStorage` for authentication simulation  
- `fetch()` for dynamic JSON data loading  

---

## ⚙️ Setup Instructions

### 1. Clone or Download the Project

```bash
git clone https://github.com/your-username/educational-dashboard.git
cd educational-dashboard

graph TD;
  A[Register / Login] --> B[Dashboard.html];
  B --> C[Click on Category Card];
  C --> D[Category.html];
  D --> E[Click on Subcategory];
  E --> F[Subcategory.html];
  F --> G[Click on File];
  G --> H[Scanner.html];
  H --> I[Simulate Barcode Scan];
  I --> J[Content.html];
