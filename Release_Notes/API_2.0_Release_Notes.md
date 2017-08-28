# NCR Counterpoint API 2.0 Release Notes
Version 2.0 of the NCR Counterpoint API includes the following new features and improvements:
## Start/End Date Filters for Item, Customer, and Inventory Endpoints
To provide date filtering functionality, a number of endpoints now support the **StartDate** and **EndDate** parameters. These parameters allow you to specify a date range that filters the modified date (**RS_UTC_DT**) field for calls to the following endpoints:
- [**GET /Customers**](../Endpoints/GET_Customers.md)
- [**GET /Customers/EC**](../Endpoints/GET_Customers_EC.md)
- [**GET /Inventory/EC**](../Endpoints/GET_InventoryEC.md)
- [**GET /Inventory/{LocID}**](../Endpoints/GET_Inventory_ByLocation.md)
- [**GET /Items**](../Endpoints/GET_Items.md)
- [**GET /Items/{LocID}**](../Endpoints/GET_Items_ByLocation.md)

**NOTE:** We strongly recommend you use ISO 8601 format in the **StartDate** and **EndDate** parameters. Other formats may produce unexpected results.
## Paging Parameters for Item, Customer, and Inventory Endpoints
To accomodate large data sets, a number of endpoints now support the new **Page** and **Rows** parameters. These parameters allow you to specify the number of rows to retrieve per page and the specific page number to retrieve for the following endpoints:
- [**GET /Customers**](../Endpoints/GET_Customers.md)
- [**GET /Customers/EC**](../Endpoints/GET_Customers_EC.md)
- [**GET /Inventory/EC**](../blob/master/Endpoints/GET_InventoryEC.md)
- [**GET /Inventory/{LocID}**](../blob/master/Endpoints/GET_Inventory_ByLocation.md)
- [**GET /Items**](../blob/master/Endpoints/GET_Items.md)
- [**GET /Items/{LocID}**](../blob/master/Endpoints/GET_Items_ByLocation.md)
## New Endpoint: GET /Inventory/Locations
This version of the NCR Counterpoint API includes a new [**GET /Inventory/Locations**](../blob/master/Endpoints/GET_InventoryLocations.md) endpoint, which allows you to retrieve information from the IM_LOC table for all stocking locations.
## Issues Resolved
Version 2.0 addresses a number of issues that were reported in the initial v1.0 release of the NCR Counterpoint API, including:
### Issue #7: /Items Endpoint - Error 500
Previously, calls to the **/Items** endpoint in databases with a large number (10,000+) of item records returned an error, due to the size of the dataset and the number of child records that needed to be retreived.
In this version, the underlying queries for the following endpoints have been updated to be able to retrieve large datasets without returning an error: 
- **GET /Customers/EC**
- **GET /Inventory/{LocID}**
- **GET /Inventory/EC**
- **GET /Item**
- **GET /Items/{LocID}**
### Issue number
Blah...
