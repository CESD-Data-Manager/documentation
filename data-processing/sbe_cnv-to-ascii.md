
# SeaBird Data Processing Guides - Converting generated .`CNV` files to common `.ASCII` format for analysis in another software package

## Introduction

This guide is written to help staff convert their SeaBird CTD and Temperature logger data from the raw data files to a final human-readable ASCII format that can be used for analysis with the software of your choice.

> **Before you begin:**  
> Make sure you have already created a `.CNV` file from the `.HEX` and `.CON`/`.XMLCON` files.

---

## Setup

1. Go to the DFO Software Centre and search for **"Seasoft"**.
2. Install Seasoft.

---

## SBEDataProcessing

1. Open **SBEDataProcessing-Win32**.
    - Click the Windows icon in the taskbar and start typing `SBEDataProcessing-Win32`.
    - Select the application if it is installed.
2. SBEDataProcessing should open.
3. Click **Run** in the menu bar.
4. Choose **15. ASCII Out…**

---

## File Setup Tab

1. The **ASCII Out** window will open. The first time you open it, it will save a **Program Setup File** (`.PSA`) which remembers your preferences. *If you already have one of these files, you can re-use it or share it with someone as well.*
2. In the **Input Directory** section:
    - Click **Select**.
    - Navigate to and select your `.cnv` file.
    - Click **OK**.
3. Check the **Output Directory** and note if you want to append anything to the end of the created file.

---

## Data Setup Tab

1. Choose if you want a header file to be output (**Yes** recommended).
2. Choose if you want a data file to be output (**Yes** recommended).
3. Label columns at the top of the file.
4. Choose **Comma** for the column separator.
5. Press the **Time Conversion Formats** button.  
    - Choose the appropriate options for your purposes.  
    - (Recommended: `dd mmm yyyy hh:mm:ss (UTC)` — but be consistent.)
6. Press **Save and Exit**.
7. Press **Select Output Variables…**
    - Select all variables unless you have a specific reason not to.
    - Press **Save and Exit**.

---

## Process File

1. Press **Start Process** at the bottom of the window.
2. Your `.ASCII` and `.HDR` files will now be created in your chosen destination folder. 
3. Do science!

---
