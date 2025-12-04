<div align="center">

# 🆘 Disaster Relief Management System

### Comprehensive Platform for Coordinating Emergency Relief Operations

[![ASP.NET Core](https://img.shields.io/badge/ASP.NET_Core-512BD4?style=for-the-badge&logo=.net&logoColor=white)](https://dotnet.microsoft.com/)
[![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white)](https://docs.microsoft.com/en-us/dotnet/csharp/)
[![Entity Framework](https://img.shields.io/badge/Entity_Framework-512BD4?style=for-the-badge&logo=.net&logoColor=white)](https://docs.microsoft.com/en-us/ef/)
[![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white)](https://www.microsoft.com/en-us/sql-server)
[![Bootstrap](https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white)](https://getbootstrap.com/)

**Empowering communities to respond effectively to disasters through efficient coordination of donations, incident reporting, and volunteer management**

[Features](#-features) • [Installation](#-installation) • [Architecture](#-architecture) • [Documentation](#-usage-guide) • [Contributing](#-contributing)

---

</div>

## 🎯 Project Overview

The **Disaster Relief Management System** is a comprehensive ASP.NET Core web application designed to streamline disaster response operations. By providing a centralized platform for donation management, real-time incident reporting, and volunteer coordination, this system enables communities and organizations to respond swiftly and effectively to emergencies.

### **Mission Statement**
*"Bridging the gap between those who need help and those who can provide it, ensuring no disaster response is delayed by lack of coordination."*

---

## ✨ Features

<div align="center">

| Module | Capabilities |
|:------:|:------------|
| 👥 **User Management** | Secure registration, authentication & profile management |
| 🎁 **Donations** | Submit, track & manage relief donations |
| 🚨 **Incidents** | Report & monitor disaster incidents in real-time |
| 🤝 **Volunteers** | Coordinate volunteer registration & skill matching |

</div>

### 👥 **User Management System**

```
✓ Secure Registration & Authentication with BCrypt password hashing
✓ Comprehensive Profile Management with edit capabilities
✓ Role-based Access Control for different user types
✓ Session Management with cookie-based authentication
✓ Password Recovery (planned enhancement)
```

**Key Features:**
- 🔐 **Enhanced Security**: BCrypt password hashing ensures user credentials are protected
- 🎭 **Role-Based Access**: Different functionality based on authentication status
- 👤 **Profile Customization**: Users can manage their personal information
- 📊 **Activity Tracking**: Monitor user engagement and contribution history

---

### 🎁 **Donation Management**

Transform how relief supplies are collected and distributed with intelligent donation tracking.

**Donation Categories:**
- 🍎 **Food Items** - Non-perishable foods, fresh produce, water
- 👕 **Clothing** - Blankets, warm clothing, footwear
- 💊 **Medical Supplies** - First aid kits, medications, hygiene products
- 🏠 **Shelter Materials** - Tents, tarpaulins, building materials
- 📦 **Other** - Electronics, tools, household items

**Features:**
```
✓ Multi-category donation submission with detailed descriptions
✓ Quantity and unit tracking (boxes, bags, items, etc.)
✓ Target area specification for precise distribution
✓ Special instructions for handling requirements
✓ Real-time status tracking (Pending, In Transit, Delivered)
✓ Complete donation history for donors
✓ Admin dashboard for all donations
```

---

### 🚨 **Incident Reporting System**

Enable rapid response through comprehensive incident documentation and tracking.

**Disaster Types Supported:**
- 🌪️ Natural Disasters (earthquakes, floods, hurricanes)
- 🔥 Accidents (fires, explosions, structural collapses)
- 🏥 Health Emergencies (disease outbreaks, mass casualties)
- 🌊 Environmental Incidents (chemical spills, contamination)

**Key Capabilities:**
```
✓ Detailed incident reporting with location data
✓ Urgency level classification (Low, Medium, High, Critical)
✓ Affected areas documentation
✓ Real-time status updates
✓ Comprehensive incident history
✓ Multi-field search and filtering
✓ Incident resolution tracking
```

**Urgency Levels:**
| Level | Description | Response Time |
|-------|-------------|---------------|
| 🔴 **Critical** | Immediate life-threatening situation | < 1 hour |
| 🟠 **High** | Severe impact requiring urgent response | < 6 hours |
| 🟡 **Medium** | Moderate impact with manageable timeline | < 24 hours |
| 🟢 **Low** | Minor impact, preventive measures | < 72 hours |

---

### 🤝 **Volunteer Coordination**

Harness the power of community volunteers through intelligent skill matching and availability management.

**Volunteer Features:**
```
✓ Comprehensive volunteer registration
✓ Skills and expertise tracking (medical, logistics, construction, etc.)
✓ Availability calendar management
✓ Transportation capability indication
✓ Preferred location settings
✓ Emergency contact information
✓ Active volunteer directory
✓ Status management (Active, Inactive, On Assignment)
```

**Tracked Skills:**
- 🏥 Medical/First Aid
- 🚛 Logistics & Transportation
- 🔨 Construction & Repairs
- 💻 IT & Communications
- 🍳 Food Preparation
- 👶 Childcare
- 🗣️ Translation Services
- 📋 Administrative Support

---

## 🏗️ Architecture

### **Technology Stack**

<div align="center">

```
┌─────────────────────────────────────────────────┐
│              Frontend Layer                     │
│     Razor Views + Bootstrap + jQuery            │
└────────────────────┬────────────────────────────┘
                     │
                     ↓
┌─────────────────────────────────────────────────┐
│           Presentation Layer                    │
│        ASP.NET Core MVC Controllers             │
└────────────────────┬────────────────────────────┘
                     │
                     ↓
┌─────────────────────────────────────────────────┐
│            Business Logic Layer                 │
│          Services + ViewModels                  │
└────────────────────┬────────────────────────────┘
                     │
                     ↓
┌─────────────────────────────────────────────────┐
│            Data Access Layer                    │
│        Entity Framework Core + LINQ             │
└────────────────────┬────────────────────────────┘
                     │
                     ↓
┌─────────────────────────────────────────────────┐
│              Database Layer                     │
│             SQL Server Database                 │
└─────────────────────────────────────────────────┘
```

</div>

### **Project Structure**

```
AAPRPOEPART2/
│
├── 🎮 Controllers/
│   ├── AccountController.cs          # Authentication & user profiles
│   ├── DonationController.cs         # Donation CRUD operations
│   ├── IncidentController.cs         # Incident reporting & tracking
│   ├── VolunteerController.cs        # Volunteer management
│   └── HomeController.cs             # Landing pages & navigation
│
├── 📊 Models/
│   ├── User.cs                       # User entity with auth
│   ├── Donation.cs                   # Donation entity
│   ├── IncidentReport.cs             # Incident entity
│   ├── Volunteer.cs                  # Volunteer entity
│   └── ViewModels/
│       ├── LoginViewModel.cs         # Login data transfer
│       ├── RegisterViewModel.cs      # Registration data
│       ├── DonationViewModel.cs      # Donation forms
│       ├── IncidentReportViewModel.cs# Incident forms
│       └── VolunteerViewModel.cs     # Volunteer forms
│
├── 🎨 Views/
│   ├── Account/
│   │   ├── Login.cshtml
│   │   ├── Register.cshtml
│   │   └── Profile.cshtml
│   ├── Donation/
│   │   ├── Create.cshtml
│   │   ├── Index.cshtml
│   │   └── Details.cshtml
│   ├── Incident/
│   │   ├── Report.cshtml
│   │   ├── Index.cshtml
│   │   └── Details.cshtml
│   ├── Volunteer/
│   │   ├── Register.cshtml
│   │   ├── Index.cshtml
│   │   └── Details.cshtml
│   ├── Home/
│   │   ├── Index.cshtml
│   │   └── About.cshtml
│   └── Shared/
│       ├── _Layout.cshtml
│       └── _ValidationScriptsPartial.cshtml
│
├── 📁 Data/
│   ├── ApplicationDbContext.cs       # EF Core DbContext
│   └── Migrations/                   # Database migrations
│
├── 🌐 wwwroot/
│   ├── css/                          # Custom stylesheets
│   ├── js/                           # JavaScript files
│   ├── images/                       # Static images
│   └── lib/                          # Client libraries
│
├── ⚙️ appsettings.json               # Application configuration
├── 🚀 Program.cs                     # Application startup
└── 📦 AAPRPOEPART2.csproj           # Project file
```

---

## 📊 Database Schema

### **Entity Relationship Diagram**

```
┌─────────────────┐
│     Users       │
├─────────────────┤
│ UserId (PK)     │─┐
│ Username        │ │
│ Email           │ │
│ PasswordHash    │ │
│ FirstName       │ │
│ LastName        │ │
│ PhoneNumber     │ │
│ CreatedAt       │ │
│ IsActive        │ │
└─────────────────┘ │
                    │
        ┌───────────┴────────────┬─────────────┐
        │                        │             │
        ↓                        ↓             ↓
┌─────────────────┐    ┌──────────────────┐  ┌─────────────────┐
│   Donations     │    │ IncidentReports  │  │   Volunteers    │
├─────────────────┤    ├──────────────────┤  ├─────────────────┤
│ DonationId (PK) │    │ IncidentId (PK)  │  │ VolunteerId(PK) │
│ UserId (FK)     │    │ UserId (FK)      │  │ UserId (FK)     │
│ DonationType    │    │ Title            │  │ Skills          │
│ ItemDescription │    │ Description      │  │ Availability    │
│ Quantity        │    │ Location         │  │ HasTransport    │
│ Unit            │    │ IncidentDate     │  │ PreferredLoc    │
│ TargetArea      │    │ DisasterType     │  │ EmergencyPhone  │
│ Instructions    │    │ AffectedAreas    │  │ RegisteredAt    │
│ DonationDate    │    │ UrgencyLevel     │  │ Status          │
│ Status          │    │ ReportedAt       │  └─────────────────┘
└─────────────────┘    │ Status           │
                       └──────────────────┘
```

### **Table Definitions**

#### **Users Table**
```sql
CREATE TABLE Users (
    UserId NVARCHAR(450) PRIMARY KEY,
    Username NVARCHAR(100) NOT NULL UNIQUE,
    Email NVARCHAR(256) NOT NULL UNIQUE,
    PasswordHash NVARCHAR(MAX) NOT NULL,
    FirstName NVARCHAR(100),
    LastName NVARCHAR(100),
    PhoneNumber NVARCHAR(20),
    CreatedAt DATETIME2 DEFAULT GETDATE(),
    IsActive BIT DEFAULT 1
);
```

#### **Donations Table**
```sql
CREATE TABLE Donations (
    DonationId INT PRIMARY KEY IDENTITY,
    UserId NVARCHAR(450) FOREIGN KEY REFERENCES Users(UserId),
    DonationType NVARCHAR(50) NOT NULL,
    ItemDescription NVARCHAR(500),
    Quantity DECIMAL(10,2) NOT NULL,
    Unit NVARCHAR(20),
    TargetArea NVARCHAR(200),
    SpecialInstructions NVARCHAR(MAX),
    DonationDate DATETIME2 DEFAULT GETDATE(),
    Status NVARCHAR(20) DEFAULT 'Pending'
);
```

#### **IncidentReports Table**
```sql
CREATE TABLE IncidentReports (
    IncidentId INT PRIMARY KEY IDENTITY,
    UserId NVARCHAR(450) FOREIGN KEY REFERENCES Users(UserId),
    Title NVARCHAR(200) NOT NULL,
    Description NVARCHAR(MAX) NOT NULL,
    Location NVARCHAR(300) NOT NULL,
    IncidentDate DATETIME2 NOT NULL,
    DisasterType NVARCHAR(50) NOT NULL,
    AffectedAreas NVARCHAR(500),
    UrgencyLevel NVARCHAR(20) NOT NULL,
    ReportedAt DATETIME2 DEFAULT GETDATE(),
    Status NVARCHAR(20) DEFAULT 'Reported'
);
```

#### **Volunteers Table**
```sql
CREATE TABLE Volunteers (
    VolunteerId INT PRIMARY KEY IDENTITY,
    UserId NVARCHAR(450) FOREIGN KEY REFERENCES Users(UserId),
    Skills NVARCHAR(500),
    Availability NVARCHAR(200),
    HasTransportation BIT DEFAULT 0,
    PreferredLocation NVARCHAR(200),
    EmergencyContact NVARCHAR(20),
    RegisteredAt DATETIME2 DEFAULT GETDATE(),
    Status NVARCHAR(20) DEFAULT 'Active'
);
```

---

## 🔐 Security Features

### **Authentication & Authorization**

```
🔒 Security Layers:
├── Cookie-based Authentication
├── BCrypt Password Hashing (Salt Rounds: 12)
├── Anti-Forgery Token Validation
├── Role-Based Access Control
├── Secure Session Management
└── HTTPS Enforcement (Production)
```

### **Data Protection**

| Threat | Protection Mechanism |
|--------|---------------------|
| 💉 **SQL Injection** | Entity Framework parameterized queries |
| 🎭 **XSS Attacks** | ASP.NET Core built-in encoding |
| 🔓 **CSRF** | Anti-forgery tokens on all POST requests |
| 🕵️ **Session Hijacking** | Secure cookie flags & HTTPS |
| 📡 **Man-in-the-Middle** | SSL/TLS encryption |

### **Password Security**
```csharp
// BCrypt hashing implementation
string hashedPassword = BCrypt.Net.BCrypt.HashPassword(password, 12);
bool isValid = BCrypt.Net.BCrypt.Verify(inputPassword, storedHash);
```

---

## 🚀 Installation

### **Prerequisites**

Ensure you have the following installed:

- ✅ **.NET 6.0 SDK** or later ([Download](https://dotnet.microsoft.com/download))
- ✅ **SQL Server** (LocalDB, Express, or Full) ([Download](https://www.microsoft.com/en-us/sql-server/sql-server-downloads))
- ✅ **Visual Studio 2022** or **VS Code** ([Download](https://visualstudio.microsoft.com/))
- ✅ **Git** for version control ([Download](https://git-scm.com/))

### **Step-by-Step Installation**

#### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/yourusername/disaster-relief-system.git
cd disaster-relief-system
```

#### **2️⃣ Configure Database Connection**

Update `appsettings.json` with your SQL Server connection string:

```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=(localdb)\\mssqllocaldb;Database=DisasterReliefDB;Trusted_Connection=True;MultipleActiveResultSets=true"
  }
}
```

**For SQL Server Express:**
```json
"Server=localhost\\SQLEXPRESS;Database=DisasterReliefDB;Trusted_Connection=True;"
```

#### **3️⃣ Restore Dependencies**
```bash
dotnet restore
```

#### **4️⃣ Apply Database Migrations**
```bash
# Create initial migration (if not exists)
dotnet ef migrations add InitialCreate

# Update database
dotnet ef database update
```

#### **5️⃣ Build the Project**
```bash
dotnet build
```

#### **6️⃣ Run the Application**

**Option A - Command Line:**
```bash
dotnet run
```

**Option B - Visual Studio:**
- Open `AAPRPOEPART2.sln` in Visual Studio
- Press `F5` or click the "Run" button

#### **7️⃣ Access the Application**
```
🌐 HTTPS: https://localhost:5001
🌐 HTTP:  http://localhost:5000
```

### **Troubleshooting**

<details>
<summary><b>Database connection issues</b></summary>

- Verify SQL Server is running
- Check connection string in `appsettings.json`
- Ensure database exists: `dotnet ef database update`
- Try using SQL Server Management Studio to connect manually
</details>

<details>
<summary><b>Migration errors</b></summary>

```bash
# Drop database and recreate
dotnet ef database drop
dotnet ef database update

# Or remove all migrations and start fresh
rm -rf Migrations/
dotnet ef migrations add InitialCreate
dotnet ef database update
```
</details>

<details>
<summary><b>Port already in use</b></summary>

Edit `Properties/launchSettings.json` and change the port numbers:
```json
"applicationUrl": "https://localhost:5002;http://localhost:5001"
```
</details>

---

## 📈 Usage Guide

### **For Donors 🎁**

1. **Register/Login** to your account
2. Navigate to **Donations** → **Create Donation**
3. Select donation type and fill in details:
   - Choose category (Food, Clothing, Medical, etc.)
   - Provide item description
   - Specify quantity and unit
   - Add target area for distribution
   - Include special handling instructions
4. **Submit** donation
5. **Track** your donations in the **My Donations** section

### **For Incident Reporters 🚨**

1. **Login** to your account
2. Navigate to **Incidents** → **Report Incident**
3. Fill in incident details:
   - Provide descriptive title
   - Detail the situation
   - Specify exact location
   - Select disaster type
   - Choose urgency level
   - List affected areas
4. **Submit** report
5. **Monitor** incident status for updates

### **For Volunteers 🤝**

1. **Login** to your account
2. Navigate to **Volunteers** → **Register as Volunteer**
3. Provide volunteer information:
   - List your skills and expertise
   - Set your availability
   - Indicate transportation capability
   - Choose preferred location
   - Add emergency contact
4. **Submit** registration
5. **View** your status in the volunteer directory

### **For Administrators 👨‍💼**

1. **Login** with admin credentials
2. Access **Admin Dashboard**
3. Monitor all activities:
   - View all donations and update statuses
   - Review incident reports
   - Manage volunteer assignments
   - Generate reports and analytics
4. **Coordinate** response efforts
5. **Update** statuses as situations evolve

---

## 🔧 Configuration

### **Application Settings**

#### **appsettings.json**
```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=(localdb)\\mssqllocaldb;Database=DisasterReliefDB;Trusted_Connection=True;"
  },
  "Authentication": {
    "CookieExpiration": 30,
    "RequireConfirmedEmail": false,
    "LockoutDuration": 5
  },
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft.AspNetCore": "Warning"
    }
  },
  "AllowedHosts": "*"
}
```

#### **appsettings.Development.json**
```json
{
  "Logging": {
    "LogLevel": {
      "Default": "Debug",
      "Microsoft.AspNetCore": "Information"
    }
  }
}
```

### **Environment Variables**

Set environment-specific variables:

```bash
# Development
export ASPNETCORE_ENVIRONMENT=Development

# Production
export ASPNETCORE_ENVIRONMENT=Production
export ConnectionStrings__DefaultConnection="your-production-connection-string"
```

---

## 🧪 Testing

### **Manual Testing Checklist**

#### **User Management**
- [ ] User registration with validation
- [ ] Login with correct credentials
- [ ] Login failure with incorrect credentials
- [ ] Profile viewing and editing
- [ ] Session persistence
- [ ] Logout functionality

#### **Donation Management**
- [ ] Create donation with all fields
- [ ] View donation list
- [ ] Filter donations by type
- [ ] Update donation status
- [ ] View donation details

#### **Incident Reporting**
- [ ] Submit incident report
- [ ] View all incidents
- [ ] Filter by urgency level
- [ ] Update incident status
- [ ] View incident details

#### **Volunteer Coordination**
- [ ] Register as volunteer
- [ ] View volunteer directory
- [ ] Update availability
- [ ] Deactivate volunteer status

### **Unit Testing (Planned)**

```csharp
// Example test structure
public class DonationControllerTests
{
    [Fact]
    public async Task CreateDonation_ValidModel_ReturnsRedirect()
    {
        // Arrange
        var controller = new DonationController(mockContext);
        var donation = new DonationViewModel { /* valid data */ };
        
        // Act
        var result = await controller.Create(donation);
        
        // Assert
        Assert.IsType<RedirectToActionResult>(result);
    }
}
```

---

## 🚨 Error Handling

### **Global Error Pages**

```
├── 400 - Bad Request
├── 401 - Unauthorized
├── 403 - Forbidden
├── 404 - Page Not Found
├── 500 - Internal Server Error
└── 503 - Service Unavailable
```

### **Validation Strategy**

```
┌─────────────────────────────────────┐
│     Client-Side Validation          │
│  (jQuery Unobtrusive Validation)    │
└───────────────┬─────────────────────┘
                │
                ↓
┌─────────────────────────────────────┐
│     Server-Side Validation          │
│    (DataAnnotations + Model         │
│         State Validation)           │
└───────────────┬─────────────────────┘
                │
                ↓
┌─────────────────────────────────────┐
│      Business Logic Validation      │
│   (Domain Rules + Constraints)      │
└─────────────────────────────────────┘
```

### **Logging Strategy**

```csharp
// Structured logging example
_logger.LogInformation(
    "Donation created: {DonationId} by User: {UserId}",
    donation.DonationId,
    userId
);

_logger.LogError(
    exception,
    "Failed to create donation for User: {UserId}",
    userId
);
```

---

## 📱 Future Enhancements

### **Phase 1 - Communication** (Q1 2025)
- [ ] 📧 Email notifications for status updates
- [ ] 📱 SMS alerts for critical incidents
- [ ] 🔔 Real-time push notifications
- [ ] 💬 In-app messaging system

### **Phase 2 - Advanced Features** (Q2 2025)
- [ ] 🗺️ GIS integration for incident mapping
- [ ] 📊 Analytics dashboard for administrators
- [ ] 📱 Progressive Web App (PWA) support
- [ ] 🌐 Multi-language internationalization
- [ ] 📸 Image upload for incidents and donations

### **Phase 3 - Mobile & Integration** (Q3 2025)
- [ ] 📱 Native mobile apps (iOS & Android)
- [ ] 🔗 RESTful API for third-party integration
- [ ] 🤖 AI-powered incident categorization
- [ ] 📈 Predictive analytics for resource allocation
- [ ] 🔄 Integration with emergency services

### **Phase 4 - Scalability** (Q4 2025)
- [ ] ⚡ Redis caching implementation
- [ ] 🔍 Elasticsearch for advanced search
- [ ] 📦 Microservices architecture
- [ ] ☁️ Cloud deployment (Azure/AWS)
- [ ] 🔄 Load balancing and auto-scaling

---

## 🤝 Contributing

We welcome contributions from the community! Here's how you can help:

### **How to Contribute**

1. **Fork** the repository
2. **Create** a feature branch
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. **Commit** your changes
   ```bash
   git commit -m 'Add some amazing feature'
   ```
4. **Push** to the branch
   ```bash
   git push origin feature/amazing-feature
   ```
5. **Open** a Pull Request

### **Development Guidelines**

#### **Code Standards**
- Follow C# coding conventions
- Use async/await for I/O operations
- Implement proper error handling
- Write XML documentation for public APIs
- Add unit tests for new features

#### **Commit Message Format**
```
<type>(<scope>): <subject>

<body>

<footer>
```

**Types:**
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes
- `refactor`: Code refactoring
- `test`: Adding tests
- `chore`: Maintenance tasks

**Example:**
```
feat(donations): add donation filtering by date range

Implemented date range picker component and backend filtering logic
to allow users to filter donations by custom date ranges.

Closes #123
```

### **Areas for Contribution**

| Area | Priority | Difficulty |
|------|----------|-----------|
| 🧪 Unit Tests | High | Medium |
| 📱 Mobile Responsive Design | High | Easy |
| 🌐 Localization | Medium | Medium |
| 📊 Analytics Dashboard | Medium | Hard |
| 🗺️ Map Integration | Low | Hard |

---

## 📄 License

This project is developed for **educational purposes** as part of the **AAPRPOE assessment**.

```
Educational License
Copyright (c) 2024 Thato Kenny Msina

This project is created for academic purposes and demonstration of 
ASP.NET Core development skills. Commercial use is not permitted 
without explicit permission.
```

---

## 👨‍💻 Author

<div align="center">

### **Thato Kenny Msina**
*Full-Stack Developer | ASP.NET Core Specialist*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/thato-msina/)
[![Portfolio](https://img.shields.io/badge/Portfolio-FF5722?style=for-the-badge&logo=todoist&logoColor=white)](https://thatos-portfoloi.netlify.app/)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:Thatomsina@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/St10245564)

📍 Johannesburg, South Africa 🇿🇦  
📧 Thatomsina@gmail.com  
📱 +27 69 212 2826

</div>

---

## 🙏 Acknowledgments

Special thanks to:

- 🎓 **FNB App Academy & CAPACITI** for comprehensive training
- 💻 **Microsoft** for ASP.NET Core framework and excellent documentation
- 🎨 **Bootstrap Team** for the responsive CSS framework
- 🗄️ **Entity Framework Core Team** for the powerful ORM
- 🔐 **BCrypt.NET** for secure password hashing
- 🌟 **Open Source Community** for inspiration and resources

---

## 📞 Support

Need help? Here's how to get support:

### **Technical Issues**
1. 📖 Check the [Documentation](#-usage-guide)
2. 🔍 Review [Troubleshooting](#troubleshooting) section
3. 💬 Open an [Issue](https://github.com/yourusername/disaster-relief-system/issues)
4. 📧 Email: Thatomsina@gmail.com

### **Feature Requests**
- Open a [Feature Request](https://github.com/yourusername/disaster-relief-system/issues/new?template=feature_request.md)
- Provide detailed description and use cases

### **Security Vulnerabilities**
- **Do not** open public issues for security vulnerabilities
- Email directly: Thatomsina@gmail.com
- Include steps to reproduce and potential impact

---

## 📊 Project Statistics

<div align="center">

![GitHub Stars](https://img.shields.io/github/stars/yourusername/disaster-relief-system?style=social)
![GitHub Forks](https://img.shields.io/github/forks/yourusername/disaster-relief-system?style=social)
![GitHub Issues](https://img.shields.io/github/issues/yourusername/disaster-relief-system)
![GitHub Pull Requests](https://img.shields.io/github/issues-pr/yourusername/disaster-relief-system)

</div>

---

<div align="center">

### 🆘 Making Disaster Relief More Efficient, One Line of Code at a Time

**Built with ❤️ using ASP.NET Core MVC**

---

*"In times of crisis, coordination saves lives. This system ensures that help reaches those who need it most, when they need it most."*

---

![Visitor Count](https://komarev.com/ghpvc/?username=St10245564&color=blueviolet&style=for-the-badge&label=Profile+Views)

**⭐ If this project helps you, please consider giving it a star! ⭐**

</di
