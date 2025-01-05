# 📊 Analyzing GSM Outdoor’s Marketing Funnel  

Welcome to my deep dive into GSM Outdoor’s marketing funnel! This project was all about wrangling data, uncovering insights, and visualizing trends to help drive smarter decisions. Here's how it all went down:  

---

## **Project Overview**  
This project involved:  
- Querying data from multiple tables in a Google Sheet  
- Processing date information  
- Performing aggregations on the resulting data  

**Key Learnings:**  
- 🔗 Joining data from multiple locations in Google Sheets  
- 🛠️ Processing and preparing data for analysis  
- 📈 Aggregating and visualizing data  

---

## **From Cleaning to Insights**  

### **Starting with the Basics: Data Cleaning**  
I began by cleaning and manipulating the data using various formulas, adding columns, and addressing missing values to ensure verything was ready for analysis.

The columns added to the orignal dataset are below, along with the formulas used to populate their values:

1️⃣ Month Contacted: Converts the contact date into a formatted "YYYY-MM" string to group data by month easily.

**Formula:** `=TEXT(B2,"yyyy-mm")`  

---

2️⃣ Closed Deal Match: Matches the deal to the 'Closed Deals' table. If no match is found, the cell is left blank.

**Formula:** `=IFERROR(VLOOKUP(A2,'Closed Deals'!A:A,1,0)," ")`  

---

3️⃣ Closed Won: Indicates whether the deal was successfully closed. If there’s no match in the "Closed Deal Match" column, it returns "NO"; otherwise, "YES."

**Formula:** `=IF(G2=" ","NO","YES")`  

---

4️⃣ Won Date: Retrieves the closing date for deals from the 'Closed Deals' table. Returns blank if no match is found.

**Formula:** `=IFERROR(VLOOKUP(A2,'Closed Deals'!A:E,5,0)," ")`  

---

5️⃣ Days to Close: Calculates the number of days it took to close a deal by subtracting the contact date from the closing date. Returns blank if no closing date is available.

**Formula:** `=IFERROR(I2-B2," ")` 

---

These columns allowed me to enrich the dataset and prepare it for deeper analysis. 📊

---

### **Diving into Analysis**  

#### **Which Lead Origin Generates the Most Leads?**  
I created a pivot table and chart to analyze lead origins.  
- The **Conversion Rate** column showed the efficiency of each origin.  
- Top converting source? **Unknown (17%)**, followed by **Paid Search** and **Organic Search (12%)**.
- To make the data more digestible, I visualized it using a clean chart.

---

#### **Are MLQs Growing Month Over Month?**  
I used pivot tables to track MLQs (Marketing Qualified Leads) by origin, month-over-month (MoM).  
- A stacked column chart highlighted the growth in MLQs.  
- Paid and Organic Search emerged as the top-performing origins, confirming the company is on the right track.

---

#### **How Long Does It Take to Close a Deal?**  
Using the **Days to Close** column, I:  
- Created a pivot table to calculate the average days to close, segmented by the month contacted.  
- Visualized it with a column chart to reveal:  
  - The time to close is decreasing over time, showing improved efficiency in sales.

---

#### **Deep Dive into Closed Deals**  
I analyzed **Closed Deal Data** to identify:  
1. **Top Lead Types:**  
   - Online_medium leads dominate.  
2. **Top Business Segments:**  
   - Outdoor home products  
   - Outdoor safety and health products  
   - Car accessories  

---

## **Key Insights**  
🚀 Doubled leads month-over-month from 2017 to 2018.  
🔍 Paid and Organic Search are the most effective channels for generating closed deals.  
🕒 Sales are becoming faster and more efficient.  
🎯 Top lead types target online-medium platforms.  
🏆 The company’s top-performing segments are:  
  - **Outdoor Home Products**: Patio furniture, garden tools, weather protection, etc.  
  - **Outdoor Safety & Health Products**: First aid kits, protective gear, health monitors.  
  - **Car Accessories**: Roof racks, dash cams, emergency kits.  

---

## **Recommendations for the Marketing Team**  
1. **Double Down on Top Channels:**  
   - Invest in **Paid Search Ads** and enhance **SEO** strategies.  
2. **Target Ideal Customer Profiles (ICPs):**  
   - Use insights to strategize email campaigns and promotions for our best-performing segments.  
3. **Keep Streamlining Sales:**  
   - Continue optimizing processes to reduce time-to-close metrics.
4. ** Next steps:**
   - I'd recommend diving into the unknown Lead Origin Source we discovered during analysis to identify the source and leverage it for more contact to closed success.

---
