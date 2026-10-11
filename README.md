# Inventory & Supply Chain Analytics Dashboard (Excel)

## Overview
Excel portfolio project for analyzing a synthetic inventory dataset, estimating inventory value, identifying reorder candidates, and comparing stock by category and warehouse.

## Dataset
- 420 synthetic inventory records
- Five warehouse locations
- INR currency
- Educational practice data; not a real business inventory export

## Features
- Raw and cleaned data worksheets
- Inventory value and potential revenue calculations
- Gross profit per unit
- Estimated stock cover in days
- Rule-based stock status and reorder quantity
- KPI cards with warehouse selector
- Charts for inventory value by category and warehouse, plus stock-status breakdown
- Data dictionary and usage guide

## Calculations
- Inventory value = stock on hand × unit cost
- Potential revenue = stock on hand × selling price
- Gross profit per unit = selling price − unit cost
- Stock cover days = stock on hand ÷ (units sold in last 30 days / 30)
- Reorder status: `Reorder Now` if stock on hand <= reorder point; `Overstock` if stock > 1.5 × target stock; otherwise `Healthy`.
- Reorder quantity = target stock − stock on hand when reorder threshold is reached, floored at zero.

## Workbook tabs
- `Dashboard`: KPI cards and charts; choose warehouse in B4.
- `Raw_Data`: original synthetic records.
- `Clean_Data`: cleaned records and calculated fields.
- `Analysis`: formula-driven summary tables.
- `Data_Dictionary`: column definitions.
- `Start_Here`: guide and assumptions.

## Limitations
The dataset is synthetic. Stock-status rules are a simple demonstration and do not replace forecasting or operational decisions based on real demand, supplier reliability, safety stock, and lead-time variability.

## How to use
Open `workbook/Inventory_Supply_Chain_Dashboard.xlsx` in Excel and allow formulas to recalculate. Change `Dashboard!B4` to All or a warehouse to update KPI cards.
