# Intermediate-Assessment
Logistics &amp; Transportation -Fleet Performance &amp; Delivery Efficiency
DATA CLEANING  -DONE IN EXCEL QUERY IN TRIP QUERY RENAMED PROJECT COLUMN "TRIP ID" FORMAT DATA TYPE FOR REQIURED COLUMNS
Trim and clean text columns ,removed duplicate rows and unwanted columns in"distance" column replace 116+666 with total
Vehicle_Master query format "maintenance cost" to currency trim and clean text columns
merge trip and vehicle_master query with vehicle id  and groupy done with vehicle type with average of fuel comsumption
again merge average fuel table with trip with vehicle type
loaded this data into power bi
vehcle_ master and trip relatiship was connected using one to many relation
calculated column "Route" = CONCATENATE(Trip[Origin],CONCATENATE("-",Trip[Destination]))
calculated measures:Cost per km = DIVIDE([Total Fuel Cost]+[Total Maintenance Cost],[Total Distance],0)
Fuel Efficiency = DIVIDE([Total Distance],[Total Fuel Consumed],0)
On-Time Delivery % = DIVIDE(CALCULATE(COUNTROWS(Trip),Trip[Delivery_Status]="On-Time"),[Total Trips],0)
Total Distance = SUM(Trip[Distance_km])
Total Fuel Consumed = SUM(Trip[Fuel_Consumed_L])
Total Fuel Cost = [Fuel rate per Litre]*[Total Fuel Consumed]
Total Maintenance Cost = SUM(Vehicle_Master[Maintenance_Cost])
Total Trips = COUNTROWS(Trip)
fleet perfromance and delivery efficiency dashboard for jan-feb month created with bar chart ,line map visual table ,slicer and kpi cards
