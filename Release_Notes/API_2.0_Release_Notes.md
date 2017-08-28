# NCR Counterpoint API 2.0 Release Notes
Version 2.0 of the NCR Counterpoint API includes the following new features...
## Start/End Date Filters for Item, Customer, and Inventory Endpoints
In this version of the NCR Counterpoint API,  a number of endpoints now support the **StartDate** and **EndDate** filter parameters. These parameters allow you to specify a date range that filters the modified date (**RS_UTC_DT**) field for calls to the following endpoints:
- [**GET /Customers**](../Endpoints/GET_Customers.md)
- [**GET /Customers/EC**](../Endpoints/GET_Customers_EC.md)
- [**GET /Inventory/EC**](../blob/master/Endpoints/GET_InventoryEC.md)
- [**GET /Inventory/{LocID}**](../blob/master/Endpoints/GET_Inventory_ByLocation.md)
- [**GET /Items**](../blob/master/Endpoints/GET_Items.md)
- [**GET /Items/{LocID}**](../blob/master/Endpoints/GET_Items_ByLocation.md)

**NOTE:** We strongly recommend you use ISO 8601 format in the **StartDate** and **EndDate** parameters. Other formats may produce unexpected results.
## Paging Parameters for Item, Customer, and Inventory Endpoints
To accomodate large data sets, a number of endpoints now support the new **Page** and **Rows** parameters. These parameters allow you to specify the number of rows to retrieve per page and the specific page number to retrieve for the following endpoints:
- [**GET /Customers**](../blob/master/Endpoints/GET_Customers.md)
- [**GET /Customers/EC**](../blob/master/Endpoints/GET_Customers_EC.md)
- [**GET /Inventory/EC**](../blob/master/Endpoints/GET_InventoryEC.md)
- [**GET /Inventory/{LocID}**](../blob/master/Endpoints/GET_Inventory_ByLocation.md)
- [**GET /Items**](../blob/master/Endpoints/GET_Items.md)
- [**GET /Items/{LocID}**](../blob/master/Endpoints/GET_Items_ByLocation.md)
## New Endpoint: GET /Inventory/Locations
This version of the NCR Counterpoint API includes a new [**GET /Inventory/Locations**](../blob/master/Endpoints/GET_InventoryLocations.md) endpoint that allows you to retrieve detailed information from the IM_LOC table for all stocking locations for your company.
## Bug Fixes
In addition, version 2.0 addresses a number of issues reported from the field in the initial 1.0 release, including...
### Issue number (CP-2320)
Blah...
### Issue number (
Blah...
