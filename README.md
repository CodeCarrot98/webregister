# Device Registry Web Form

A lightweight, mobile-responsive web form hosted on **GitHub Pages** that automatically captures device information and timestamps, sending all data directly to a **Google Sheet**.

## 🚀 Features
- **Auto-Detection:** Identifies if the user is on a Laptop, Android, or iOS device.
- **Hidden Metadata:** Captures the full browser User Agent and exact timestamp without cluttering the UI.
- **Google Sheets Integration:** No database required; uses Google Apps Script as a backend.
- **Compulsory Validation:** Ensures Name and Official Number are provided before submission.

## 📋 Form Fields
| Field | Type | Behavior |
| :--- | :--- | :--- |
| **Name** | Visible | Compulsory |
| **Official Number** | Visible | Compulsory |
| **Timestamp** | Hidden | Auto-generated |
| **Device** | Visible | Auto-detected (Editable) |
| **Auto-Detected Info** | Hidden | Technical Metadata |

---

## 🛠️ Setup Instructions

### 1. Google Sheets Configuration
1. Create a new Google Sheet named `Official_Number_List`.
2. Set the following headers in the first row (A to E):
   - `Name`, `Official Number`, `Timestamp`, `Device`, `Auto-Detected Info`.
3. Go to **Extensions > Apps Script**.
4. Paste the `Code.gs` provided in this project.
5. Click **Deploy > New Deployment**.
   - Select **Web App**.
   - Set "Execute as" to **Me**.
   - Set "Who has access" to **Anyone**.
6. **Copy the Web App URL**.

### 2. Website Deployment
1. Open `index.html`.
2. Locate the constant `SCRIPT_URL` and paste your Google Web App URL.
3. Upload `index.html` to your GitHub repository.
4. Go to **Settings > Pages** and enable deployment from the `main` branch.

---

## 🛠️ Technology Stack
- **Frontend:** HTML5, CSS3, JavaScript (ES6+)
- **Backend:** Google Apps Script (GAS)
- **Database:** Google Sheets API
- **Hosting:** GitHub Pages
