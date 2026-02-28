# Sales-dashboard-Project
An interactive Power BI dashboard analyzing 10 years of sales data, featuring regional performance tracking and customer segmentation.
## Project Overview
โปรเจกต์นี้เป็นการวิเคราะห์ข้อมูลยอดขายย้อนหลัง 10 ปี (2015-2025) เพื่อค้นหา Insight ทางธุรกิจและทำความเข้าใจพฤติกรรมของลูกค้า โดยใช้ Power BI ในการสร้าง Interactive Dashboard นำเสนอข้อมูลแบบรอบด้าน ตั้งแต่ภาพรวมระดับผู้บริหาร ไปจนถึงการจัดกลุ่มลูกค้า (Customer Segmentation)

**เครื่องมือที่ใช้ (Tools & Technologies):**
* **Power BI:** สำหรับทำ Data Modeling, สร้าง DAX Measures, และ Data Visualization
* **DAX:** Time Intelligence (YTD, YoY), และ Customer Segmentation

---

## โครงสร้างของ Dashboard (Dashboard Pages)

ออกแบบ Dashboard แบ่งออกเป็น 3 หน้าหลัก เพื่อตอบโจทย์ทางธุรกิจในมุมมองที่ต่างกัน ดังนี้:

### Page 1: Executive Summary 
หน้าที่ออกแบบมาเพื่อให้ผู้บริหารเห็นภาพรวมผลประกอบการของบริษัทได้อย่างรวดเร็ว
* **Key Metrics:** สรุปตัวเลข Total Revenue, Total Profit, Profit Margin % และจำนวนลูกค้า
* **Trend Analysis:** กราฟแสดงแนวโน้มยอดขายและกำไรตลอด 10 ปี เพื่อดูการเติบโตและฤดูกาลขาย (Seasonality)
* **Revenue Breakdown:** สัดส่วนรายได้แยกตามหมวดหมู่สินค้า (Product Category) และภูมิภาค (Region) 

### Page 2: Product & Regional Analysis 
หน้าที่เน้นการวิเคราะห์ประสิทธิภาพของสินค้าแต่ละประเภทในแต่ละพื้นที่ เพื่อหาจุดแข็งและจุดที่ต้องปรับปรุง
* **Profitability Matrix:** ตารางแจกแจงยอดขายและกำไรแยกตามพื้นที่และสินค้า พร้อม Conditional Formatting ไฮไลต์จุดที่กำไรบางหรือขาดทุน
* **Product Portfolio Analysis (Scatter Chart):** จัดกลุ่มสินค้าตามยอดขายและเปอร์เซ็นต์กำไร เพื่อหาสินค้า (กำไรดี+ขายดี) และสินค้าที่ควรระวัง
* **Regional Performance:** แผนที่ (Treemap) เปรียบเทียบขนาดยอดขายตามภูมิภาค

### Page 3: Customer Insights & Segmentation (วิเคราะห์พฤติกรรมลูกค้า)
หน้านี้ใช้สำหรับวิเคราะห์ฐานลูกค้าและพฤติกรรมการซื้อ เพื่อนำไปต่อยอดแคมเปญการตลาด
* **Customer Segmentation:** มีการเขียนสูตร DAX จัดกลุ่มลูกค้า (Tier) เป็น VIP, Gold, Silver และ Bronze ตามยอดซื้อสะสม เพื่อดูว่ารายได้หลักมาจากลูกค้าระดับใด
* **Top 10 VIP Customers:** จัดอันดับลูกค้ารายใหญ่ที่สร้างกำไรสูงสุดให้บริษัท
* **Behavior Analysis:** วิเคราะห์ความสัมพันธ์ระหว่าง "ความถี่ในการซื้อ (Transactions)" และ "ยอดการสั่งซื้อ (Revenue)"
* **Customer Growth:** กราฟติดตามการเติบโตของจำนวนลูกค้าใหม่ในแต่ละปี
----------------------------------------------
## Technical Highlights
* **Data Modeling:** สร้างความสัมพันธ์แบบ Star Schema โดยมีตาราง `Sales` เป็น Fact Table และเชื่อมต่อกับตาราง `Calendar` เพื่อให้สูตรวันที่ทำงานได้อย่างถูกต้อง
* **Time Intelligence DAX:** สร้างฟังก์ชันวิเคราะห์เปรียบเทียบข้ามปี เช่น YTD (Year-to-Date), YoY Growth (Year-over-Year)
* **Dynamic Segmentation:** สร้าง Calculated Column ด้วยคำสั่ง `SWITCH` เพื่อแบ่งกลุ่มลูกค้าอัตโนมัติตามเงื่อนไขยอดขาย

