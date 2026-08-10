# Google Play Console Submission Info - Quick Reference

Use the details below to complete your app submission on the Google Play Console.

---

## 🔗 Privacy Policy URL
Copy and paste this link into the **App Content** > **Privacy Policy** section:
```text
https://adhikshita.in/privacy/
```
*(This page has been created on your web domain to comply with Google Play Developer policies).*

---

## 📝 Main Store Listing Info

* **App Name**: `Adhikshita Kumarpur Land`
* **Short Description** (Max 80 chars):
  ```text
  Browse and book premium industrial and factory plots in Kumarpur, West Bengal.
  ```
* **Full Description** (Max 4000 chars):
  ```text
  Explore and reserve ready-to-build industrial land and plots in Kumarpur, West Bengal. Developed by Adhikshita Plotters Private Limited, this app provides detailed plot layouts, pricing tables, connectivity details, and live walkthrough videos of our industrial corridor. 
  
  Zoned for factories, warehouses, and cold storage with 50 ft wide main roads, clear titles, and flexible payment options. Book your plot today through the integrated direct-to-WhatsApp booking form.
  ```
* **Category**: `Productivity` or `Business`
* **Tags**: `Real Estate`, `Business`

---

## 🛠️ App Content Declarations & Questionnaire Answers

Complete these declarations inside the **App Content** page in the left menu:

### 1. App Access (Restricted Content)
* Choose: **"All functionality is available without special access"**
  *(There are no login walls, passwords, or restricted portals in the app).*

### 2. Ads
* Choose: **"No, my app does not contain ads"**

### 3. Content Rating (PEGI / ESRB questionnaire)
* **Category**: Select **Utility, Productivity, Communication, or Other**
* **Violence, Sexual Content, Offensive Language**: Choose **No** for all questions.
* **Miscellaneous**:
  - Does the app share the user's physical location? **No**
  - Does the app allow users to purchase digital goods? **No**
  - Does the app contain online user-to-user interactions? **No** (selecting No is recommended since the app itself has no native chat or social networks, it just redirects to standard external apps like WhatsApp or email).

### 4. Target Audience and Content
* Select: **18 and over**
  *(Selecting 18+ keeps validation extremely simple and fast since there are no child-safety policies to satisfy).*

### 5. News Apps
* Select: **"No, my app is not a news app"**

### 6. COVID-19 tracing/status
* Select: **"My app is not a publicly available COVID-19 contact tracing or status app"**

### 7. Government Apps
* Select: **"No, my app is not developed on behalf of a government entity"**

---

## 🛡️ Data Safety Questionnaire Answers

This is the most critical section. Answer the questions as follows:

1. **Does your app collect or share any of the required user data types?**
   - Answer: **Yes** *(because users voluntarily enter their Name and Phone number in the contact/booking forms).*
2. **Is all of the user data collected by your app encrypted in transit?**
   - Answer: **Yes** *(since the WebView loads over HTTPS).*
3. **Do you provide a way for users to request that their data be deleted?**
   - Answer: **Yes** *(you can delete their information if they contact your official support email).*

### Data Types Declared:
On the **Data Types** page, check the following boxes:
* **Personal Info**:
  - Check **Name**
  - Check **Phone number**

### Data Usage Declarations:
For both **Name** and **Phone number**, configure the settings as follows:
* **Is this data collected, shared, or both?**: Choose **Collected** (not shared).
* **Is this data processed ephemerally?**: Choose **No**.
* **Is this data required or optional?**: Choose **Optional** (users can use the app without booking).
* **Why is this data collected?**: Check **App functionality** (to process inquiries and bookings).
