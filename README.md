🌱 Agri-Energy Connect 🔋
<div align="center">





<h3>Sustainable Agriculture Meets Green Energy</h3> <p>A modern platform connecting sustainable farmers with renewable energy solutions</p> </div>
📖 Table of Contents
Overview

Key Features

User Roles

Technology Stack

Prerequisites

Setup Instructions

1. Clone the Repository

2. Database Configuration

3. Apply Database Migrations

4. Build and Run the Application

Using the Application

Landing Page

Authentication

Dashboard

For Employees

For Farmers

Development Workflow

Project Structure

Extending the Application

Testing

Troubleshooting

Deployment

License

Contact

📘 Overview
Agri-Energy Connect is a web-based platform designed to bridge the gap between sustainable agriculture and green energy solutions in South Africa. The platform connects farmers with energy experts, facilitating knowledge sharing, resource access, and collaboration opportunities to promote sustainable farming practices and renewable energy adoption.

🔑 Key Features
User Authentication: Secure login and role-based access control.

Farmer Profiles: Detailed farmer information and farm details.

Product Marketplace: Platform for farmers to showcase their sustainable agricultural products.

Responsive Design: Mobile-friendly interface using Bootstrap 5.

Data Management: Entity Framework Core with SQL Server backend.

Real-time Chat: Communication between farmers using SignalR.

GIS Integration: Mapbox GL for geospatial data visualization.

👥 User Roles
The platform supports two primary user roles:

Employee: System administrators who can:

Manage farmer accounts and profiles.

View all products across the platform.

Access farmer details and performance metrics.

Farmer: Agricultural producers who can:

Manage their profile and farm information.

Add and manage their product listings.

View products from other farmers.

Engage in real-time chat with other farmers.

🛠️ Technology Stack
Framework: ASP.NET Core 9.0 MVC

Frontend: HTML5, CSS3, JavaScript, Bootstrap 5

Backend: C#, Entity Framework Core

Database: Microsoft SQL Server

Authentication: Session-based authentication with password hashing

Styling: Bootstrap Icons, Google Fonts (Montserrat, Poppins)

Real-time Communication: SignalR

Geospatial Visualization: Mapbox GL

📋 Prerequisites
Before you begin, ensure you have the following installed:

.NET 9.0 SDK

Visual Studio 2022 (recommended) or Visual Studio Code

SQL Server 2019 or later (Express edition is sufficient for development)

SQL Server Management Studio (or any SQL client)

⚙️ Setup Instructions
1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/ST10254797/AgriEnergyConnects
cd AgriEnergyConnects
2. Database Configuration
Open SQL Server Management Studio or your preferred SQL client.

Create a new database named AgriEnergyDB.

Update the connection string in appsettings.json to match your SQL Server instance:

json
Copy
Edit
"ConnectionStrings": {
  "DefaultConnection": "Server=YOUR_SERVER_NAME;Database=AgriEnergyDB;Trusted_Connection=True;MultipleActiveResultSets=true;TrustServerCertificate=True"
}
Replace YOUR_SERVER_NAME with your actual SQL Server name.

3. Apply Database Migrations
Using Visual Studio:

Open the Package Manager Console (Tools > NuGet Package Manager > Package Manager Console).

Run the following commands:

powershell
Copy
Edit
Add-Migration InitialCreate
Update-Database
Using the command line:

bash
Copy
Edit
dotnet ef migrations add InitialCreate
dotnet ef database update
4. Build and Run the Application
Using Visual Studio:
Open the solution file (AgriEnergyConnects.sln) in Visual Studio.

Build the solution (Ctrl+Shift+B).

Press F5 to run the application.

Using the command line:
bash
Copy
Edit
dotnet build
dotnet run
The application should now be running at https://localhost:7066/.

🧭 Using the Application
Landing Page
The landing page provides a welcome screen.

It includes access to the Login page (via the Login button) and the Register page (via the Register button) for creating a new account.

Authentication
Use the following demo credentials to test the application:

Email: dd@gmail.com

Password: Sh@ldon3

Farmers:

Email: shaldon1@gmail.com

Password: Br@yden3


Dashboard
Upon successful login or registration, users are redirected to the Home page, which displays a welcome message. The navigation bar is dynamically populated with views relevant to the user's role.

For Employees
Managing Farmers:

Navigate to the "Farmers" section to view the list of registered farmers.

Add new farmers using the "Create New" button.

View detailed farmer profiles by clicking on "Details".

Delete farmer profiles by clicking on "Delete".

Viewing Products:

Access the "All Products" section to browse products from all farmers.

Filter products by category or date range.

For Farmers
Managing Profile:

Access your profile from the "Farmers Profile" tab.

Edit/update your profile information using the "Save Changes" button.

Managing Products:

Navigate to "Products" to view your current product listings.

Add new products using the "Create New Product" button.

Edit, view, or delete existing products from this page.

Forum/Farmers Chat:

Navigate to the "Farmers Chat" to chat with other farmers.

Tap on "Send Message" to send a message to the community.

🧑‍💻 Development Workflow
Project Structure
The application follows the standard ASP.NET Core MVC structure:

Controllers/: Contains the application's controllers.

AppRolesController.cs: Handles user authentication.

ChatController.cs: Handles the chats between the farmers.

FarmersController.cs: Manages farmer-related operations.

HomeController.cs: Handles dashboard and home page.

ProductsController.cs: Manages product operations.

Models/: Contains the application's data models.

ApplicationUser.cs: Represents users (employees and farmers).

ChatMessage.cs: Represents the chats.

Product.cs: Represents agricultural products.

ErrorViewModel.cs: Used for error handling.

Farmer.cs: Represents the farmers' details.

Views/: Contains the application's views, organized by controller.

AppRoles/: Login and registration views.

Farmers/: Farmer management views.

Home/: Dashboard views.

Products/: Product management views.

Chats/: Manages the messages.

Data/: Contains database context and configurations.

ApplicationDbContext.cs: Entity Framework database context.

wwwroot/: Contains static files.

css/: Stylesheet files.

js/: JavaScript files.

images/: Image assets.

lib/: Client-side libraries.

Extending the Application
Adding New Features:

Create new controllers in the Controllers/ directory.

Add corresponding views in the Views/ directory.

Update navigation in _Layout.cshtml.

Modifying Database Schema:

Update model classes in the Models/ directory.

Create a new migration using Entity Framework:

Using Visual Studio:

powershell
Copy
Edit
Add-Migration MigrationName
Update-Database
Using the command line:

bash
Copy
Edit
dotnet ef migrations add MigrationName
dotnet ef database update
🧪 Testing
The application includes sample data to facilitate testing:

Sample Users:

Employee:

Email: dd@gmail.com

Password: Sh@ldon3

Farmers:

Email: shaldon1@gmail.com

Password: Br@yden3


Sample Products:

Organic Tomatoes

Free-Range Eggs

Grass-Fed
