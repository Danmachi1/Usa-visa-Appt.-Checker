# **Visa Appointment Checker - Automated Availability Notifier**

## **Overview**
The **Visa Appointment Checker** is a **PowerShell script** designed to automatically check for available **US visa interview appointments**. Instead of manually refreshing the scheduling page, this script **logs in**, checks for appointment availability, and **alerts** you when a slot opens.

## **Features**
✅ **Automated Login** - Uses your provided credentials to log into the visa scheduling portal.  
✅ **Real-time Appointment Check** - Fetches the latest availability status.  
✅ **Notification for Available Slots** - Alerts you when a new appointment is found.  
✅ **Customizable Schedule** - Run the script periodically to track changes.  
✅ **Saves Time** - Eliminates the need for manual refreshing and monitoring.  

## **Prerequisites**
- **Windows PowerShell** (Pre-installed on Windows)
- **Internet Connection**
- A valid **US Visa scheduling account** (https://ais.usvisa-info.com/)

## **Installation**
1. **Download the script**:
   ```powershell
   git clone https://github.com/your-repo/visa-appointment-checker.git
   cd visa-appointment-checker
   ```
2. **Ensure PowerShell script execution is enabled**:
   ```powershell
   Set-ExecutionPolicy Unrestricted -Scope CurrentUser
   ```
3. **Run the script** using your account credentials:
   ```powershell
   .\visa-appointment-checker.ps1 -email "your-email@example.com" -password "your-password" -scheduleId 123456
   ```

## **Usage**
Run the script periodically to check for available appointments. If slots are available, the script will notify you.

### **Command Syntax**
```powershell
.\visa-appointment-checker.ps1 -email "your-email@example.com" -password "your-password" -scheduleId 123456
```
- **`-email`** → Your login email for the visa scheduling website.  
- **`-password`** → Your password (Ensure proper security measures when handling credentials).  
- **`-scheduleId`** → The **schedule ID** (Can be found in the URL when scheduling an appointment).  

## **Example**
```powershell
.\visa-appointment-checker.ps1 -email "john.doe@gmail.com" -password "SuperSecure123" -scheduleId 987654
```

## **How It Works**
1. The script **logs in** to the US Visa scheduling system.
2. It **fetches** the appointment schedule page.
3. It **parses** the content to check if there are available appointment slots.
4. If **slots are available**, it will **notify** you via output messages.

## **Security Considerations**
- **Do not share** your login credentials in public repositories.
- **Use a secure storage method** like environment variables instead of hardcoding passwords.
- **Run on a trusted machine** to avoid credential leaks.

## **Troubleshooting**
- If the script doesn’t run, ensure execution policy is set:
  ```powershell
  Set-ExecutionPolicy Unrestricted -Scope CurrentUser
  ```
- If login fails, verify your **email, password, and schedule ID**.
- If no appointments are available, wait and **rerun the script later**.

## **Disclaimer**
This script is **not affiliated with the US visa system**. It simply automates the **checking process** and does not guarantee appointment availability.

## **License**
This project is licensed under the **MIT License**.
