# Excel_Car_Data_Analytics

## Introduction
With an ever-expanding market of car options and rising vehicle prices, choosing the right car at the right price has become more challenging than ever. It is imperative for consumers to make informed decisions, understanding not just the type of car they want but also how its pricing compares to market trends. To simplify this process, I have developed a **Car Pricing Dashboard** in Excel. 

Taken from the kaggle dataset, this interactive tool empowers consumers by providing clear, data-driven insights into car prices, helping them navigate their options with confidence.

### Dashboard File
My final dashboard is [Excel_Car_Data_Analytics](Car_Price_Dashboard.xlsx)

### Excel Skills Used
The following Excel skills were utilized for analysis:

- **Charts and Formatting**
- **Formulas and Functions**
- **Data Validation**

### Car Pricing Dataset
The following dataset came from [Kaggle](kaggle.com), and includes detailed information on:

- **Model**
- **Engine Size**
- **Mileage**
- **Owner Count**
- **Price**

## Dashboard Build

### Charts

**Car Model Prices - Bar Chart**

<img width="397" alt="Screenshot 2025-04-03 at 12 28 49 PM" src="https://github.com/user-attachments/assets/4d3ab481-779f-4a68-8ec4-c98fcca161ea" />  

- **Excel Features:** Utilized bar chart and highlighted selected model for visual clarity
- **Data Organization:** Separated car models based on their respective brand, and sorted based on descending prices for improved readability
- **Insights Gained:** Enables quick and accessible identification of pricing trends of car models, based on brand and year. According to data, the Accord is shown to be the most expensive model in Honda's collection

**Car Model Prices - Scatter Plot**

<img width="369" alt="Screenshot 2025-04-03 at 1 00 19 PM" src="https://github.com/user-attachments/assets/c1f025d0-1191-4172-ab4f-9c8dc9e8a65a" />

- **Excel Features:** Utilized scatter plot and highlighted selected year for clarity
- **Data Organization:** Plotted the years of each brand and model, and sorted based on ascending year for visualization
- **Insights Gained:** Enables quick identification of pricing trends of cars throughout the years. Starting from year 2000, car prices have shown a linear increase each year.

**Car Mileage - Gauge Chart**

<img width="298" alt="Screenshot 2025-04-03 at 2 20 31 PM" src="https://github.com/user-attachments/assets/025ab9ce-352d-4adf-8168-7caefd6e499d" />

- **Excel Features:** Utilized a pie and doughnut chart to indicate car mileage of car model
- **Data Organization:** Indicated the median car mileage and where it falls in terms of low, medium, or high mileage
- **Insights Gained:** Enables visualization of car mileage, as an important factor to consider when buying a used car. Being in the green, it indicates that the CR-V has a mileage of 21,000 miles, making it low and good to buy.

### Formulas and Functions

**Median Price by Brand**

```excel
=MEDIAN(
       IF(
          (cars[Model]=A11)*
          (cars[Brand]=brand)*
          (cars[Year]=year)*
          (cars[Price]<>0),
          cars[Price]
       )
)
```
- **Multi-Criteria Filtering:** Filters cars based on brand, model, and year while excluding blank prices
- **Array Formula:** Utilizes ```MEDIAN()``` function with nested ```IF``` statement
- **Insights Gained:** Delivers precise pricing insights based on selected brand, model, and year
- **Formula Purpose:** The formula above generated the first table shown below, grouping the model and returning the median salary based on brand and year

**Mileage Grouped Condition**

```excel
=IFS(
             (B2<25000),"< 25,000",
    AND(B2>=25000, B2<50000),"25,000 - 50,000",
             (B2>50000),"> 50,000"
)
```
- **Filtering:** Categorizes cars based on mileage, making it easier to assess their condition
- **Insights Gained:** Counts the number of cars in each mileage category and provides an overview of how much each model has been driven
- **Formula Purpose:** Generates a summary table that groups car mileage into predefined categories, offering a clear breakdown of mileage distribution


**Background Table** 

**Median Price by Brand**  

<img width="166" alt="Screenshot 2025-04-03 at 2 59 01 PM" src="https://github.com/user-attachments/assets/326f43dc-2996-428d-901a-b8ae600d6799" />

**Mileage Grouped Condition**  

<img width="166" alt="Screenshot 2025-04-03 at 3 11 43 PM" src="https://github.com/user-attachments/assets/929b50c9-ac07-42e8-95c8-5002ee1a99c2" />

## Conclusion

With the increasing variety of car options and rising prices, making an informed decision is crucial. This **Car Pricing Dashboard** was designed to simplify the decision-making process by providing clear, data-driven insights into car prices and mileage. Ultimately, this dashboard serves as a valuable tool to help consumers navigate the complexities of car pricing with confidence.
