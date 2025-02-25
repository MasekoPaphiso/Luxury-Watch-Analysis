# Luxury-Watch-Analysis
# 📋 Overview  
This Power BI dashboard provides a comprehensive analysis of the luxury watch market, exploring pricing trends, material preferences, technical specifications, and brand positioning. Designed for watch enthusiasts, retailers, and analysts, it transforms raw data into actionable insights through interactive visualizations.

# 1. **Price Analysis**  
- **Case Diameter Impact**:  
  - Larger diameters (41mm, 45mm) correlate with premium pricing appealing to modern trends favoring bold designs.
  - Smaller diameters (30–35mm) are affordable targeting classic or unisex styles.

- **Opportunity:**
  - Market larger watches as "statement pieces" for luxury buyers.
  - Position smaller sizes for entry-level or vintage-inspired collections.
<br />
<br />
<img src="https://i.imgur.com/8MnCsUx.png"/>

---

# 2. **Brand Positioning**  
- **Luxury Tier (≥$5K):**
  - Top Brands: Audemars Piguet, Patek Philippe, Rolex, Vacheron Constantin.
  - Insight: Swiss brands dominate the ultra-luxury segment.
- **Premium Tier (1K–5K):**
  - Top Brands: Omega, Breitling, Tag Heuer, Montblanc.
  - Insight: Focus on heritage and technical innovation (e.g., Omega’s co-axial escapement).
- **Affordable Tier (<$1K):**
  - Top Brands: Tissot, Hamilton, Citizen, Seiko.
  - Insight: Emphasize affordability and reliability (e.g., Seiko’s Prospex line). 

- **Purpose:**
  - To categorize watches into price segments for trend analysis and audience targeting.

- **Reasoning:**
  - **Business Context:** Luxury buyers prioritize exclusivity, while affordable buyers seek value. Segmenting by price tier helps tailor marketing strategies.
  - **Technical Logic:** SWITCH(TRUE(), ...) evaluates conditions sequentially and assigns the first matching tier.

<br />
<br />
<img src="https://i.imgur.com/MfbaUOJ.png"/>                                        <img src="https://i.imgur.com/XXXuJlK.png"/>
<img src="https://i.imgur.com/rsSKVhI.png"/>                                        <img src="https://i.imgur.com/v3kU1Pk.png"/>

---

# 3. **Material Preferences**  
- **Case Material**:  
  - Stainless steel (91.47%) is the industry standard for its durability and timeless design.
  - Titanium (8.53%) is a premium alternative for lightweight, high-end models.
- **Recommendation:**
  - Promote titanium models as "innovative" or "luxury-performance" timepieces.
  
- **Strap Material**:  
  - Rose Gold and Alligator Leather straps command the highest prices signaling exclusivity.
  - Rubber and Silicone straps are budget-friendly (under $10K), common in sport/dive watches (e.g., Seiko Prospex).
- **Trend:**
  - Luxury buyers prioritize rare materials (alligator, rose gold), while casual buyers favor functionality (rubber, fabric).

<br />
<br />
<img src="https://i.imgur.com/vm6c49H.png"/>
<img src="https://i.imgur.com/JiIMCQx.png"/>

---

# 4. **Technical Specifications**  
- **Water Resistance**:  
  1. **Premium Pricing for 300m–600m Water Resistance:**
   - Watches rated for 300m and 600m command the highest average prices.
   - Reason: These are industry standards for luxury dive watches (e.g., Rolex Submariner, Omega Seamaster), blending prestige with professional functionality.

  2. **Ultra-High Water Resistance ≠ Highest Price:**
   - 2000m and 1000m models have lower average prices (10K–20K) despite extreme ratings.
   - Reason: Niche markets (technical diving) lack mainstream demand, and brands like Seiko Prospex or Citizen Promaster dominate this segment with affordable tool watches.

  3. **Entry-Level Water Resistance (30m–100m):**
   - Priced under $10K, targeting casual buyers .
   - Insight: Minimal water resistance suffices for everyday wear, prioritizing style over technical specs.

  4. **Mid-Tier (100m–200m):**
   - Prices range from 10K–20K, appealing to enthusiasts seeking balanced performance .
   - Trend: Ideal for recreational diving and swimming, driving demand in the premium segment.
  
- **Movement Types**:  
  - Automatic movements dominate (87.09%), reflecting their prestige and craftsmanship appeal in luxury watches.
  - Manual movements (10.25%) cater to collectors valuing mechanical artistry, while quartz (2.25%) is rare due to its association with affordability.
- **Recommendation:**
  - Highlight automatic movements in marketing to target luxury buyers.
  - Position manual watches as niche collector items.
 
<br />
<br />
<img src="https://i.imgur.com/dRr9HbC.png"/>
<img src="https://i.imgur.com/2DcqthC.png"/>

---

# 5. **Complications**   
 -  **Key Insights:**
  1. **Dominance of Practical Complications**
   - Date (264): The most common complication, reflecting its everyday utility.
   - Chronograph (93): Popular in sports and luxury watches (e.g., Rolex Daytona, Omega Speedmaster).
  2. **Niche High-End Features**
  - GMT (9): Rare but premium, often paired with luxury travel watches (e.g., Rolex GMT-Master II).
  - World Time (1): Ultra-niche, signaling exclusivity (e.g., Patek Philippe World Time).
  3. **Simplicity Sells**
  - No Complications (118): Many watches prioritize minimalist design, appealing to buyers valuing elegance over complexity.
<br />
<br />
<img src="https://i.imgur.com/nZ3H0N9.png"/>

# 🛠️ Features  
- **Interactive Filters**:  
  - Filter by **Brand**, **Price Tier**, **Water Resistance**, and **Movement Type**.  
- **Tooltip Details**:  
  - Hover over visuals to see model-specific details (e.g., strap material, complications).

  ---

## 📊 Data Sources  
- **Primary Dataset**: [Luxury Watch Dataset] (hypothetical source - anonymized for privacy).  
- **Cleaning**: Data standardized in Excel (removed duplicates, fixed typos like "Patek Philippe").  

---

## 🛠️ Tools Used  
- **Power BI Desktop**: Dashboard design, DAX measures, and data modeling.
- **Purpose:**
  - To create a comma-separated list of brands for tooltips or summary visuals.
- **Reasoning:**
  - **User Experience:** Displays all brands in a category (e.g., "Luxury tier: Rolex, Patek Philippe, Audemars Piguet") without cluttering visuals.
  - **Technical Logic:** CONCATENATEX: Iterates through unique brands (VALUES()) and concatenates them into a single text string.
<img src="https://i.imgur.com/YkaY13B.png"/>
  
- **Excel**: Initial data cleaning and validation.  
- **GitHub**: Version control and portfolio hosting.  
