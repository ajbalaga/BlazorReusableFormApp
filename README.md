# Reusable Form Component (Blazor Server)

## 🧩 Overview

This project demonstrates the creation of a **reusable form component** in a Blazor Server application. The goal is to design a clean, maintainable, and reusable UI component that follows standard Blazor patterns, with proper separation of concerns and good usability practices.

Target Framework: .Net 10

---

## 🎯 Objective

Build a reusable Blazor component that:

* Collects user information
* Can be integrated across different pages
* Keeps business logic separate from UI logic

---

## 🏗️ Project Structure

```
BlazorReusableFormApp/
│
├── Connected Services/
├── Dependencies/
├── Properties/
│
├── wwwroot/
│   ├── lib/
│   ├── app.css
│   └── favicon.png
│
├── Components/
│   ├── Layout/
│   │   ├── MainLayout.razor
│   │   └── ReconnectModal.razor
│   │
│   └── Pages/
│       ├── Index.razor          // reusable component is called
│       ├── NotFound.razor
│       └── UserFormPage.razor   // Sample page using the reusable form
│
├── Models/
│   └── UserModel.cs             // Data model with validation
│
├── _Imports.razor
├── App.razor
├── Routes.razor
│
├── appsettings.json
└── Program.cs
```

---

## 🧱 Component: UserForm

### 📍 Location

```
/Components/Pages/UserFormPage.razor
```

### ✨ Features

* Accepts a model from the parent component
* Emits a submit event using `EventCallback`
* Designed for reuse across multiple pages
* Contains no business logic (UI only)
* Not found page
---

## 📝 Form Fields

The form includes the following inputs:

* Name
* Address
* Age
* Email Address
* Submit Button

---

## ⚙️ Implementation Details

### ✔ Form Handling

* Uses `EditForm`
* Implements proper data binding
* Uses Blazor input components:
  * `InputText`
  * `InputNumber`
* Supports validation via `DataAnnotations`

### ✔ Validation

* Field-level validation messages
* Validation summary
* Clear and user-friendly feedback

---

## 🔁 Reusability Design

The component is built to be reusable by:

* Accepting a model via `[Parameter]`
* Exposing a submit handler using `EventCallback<T>`
* Avoiding any embedded business logic

---

## 🚀 How to Run

1. Clone the repository
2. Open the solution in Visual Studio
3. Run the project

---

## 🧠 Key Concepts Demonstrated

* Component reusability in Blazor Server
* Separation of concerns
* Event handling with `EventCallback`
* Form handling with `EditForm`
* Data validation using `DataAnnotations`

---

✨ *Simple, structured, and reusable — just like good Blazor components should be.*
