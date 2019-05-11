# GeoMap: Computer Geo-Locations

![alt text](images/Geographic%20Map%20of%20Asset%20Inventory.PNG "Computer Geo-Locations")

1. In *Azure Monitor Logs*, run the following query using any time interval you wish:

   ```
   // Table: Computer Geo-Locations
   Heartbeat
   | distinct Computer, ComputerEnvironment, RemoteIPCountry, RemoteIPLatitude, RemoteIPLongitude
   ```

2. Export the query, then copy and paste the exported file contents into *PowerBI Desktop*:

   <https://docs.microsoft.com/en-us/azure/azure-monitor/platform/powerbi>

   <details>

   <summary>Click here for a summary of the instructions...</summary>

   <p>

   In *Azure Monitor Logs*:

   1. After running a query, in the menu bar select **Export > Power BI Query (M)** to generate a "PowerBIQuery.txt" file.

   2. Open the "PowerBIQuery.txt" text file and copy its contents.

   In *PowerBI Desktop*:

   1. In the top menu bar click on the **Get Data** button and choose **Blank Query** to open the *Query Editor* window.

   2. In the *Query Editor* window, from the top menu bar select **Advanced Editor**.

   3. In the *Advanced Editor* window paste the contents of the exported file into the query and click **Done**. You may be prompted for credentials to connect to Azure.

   4. Type in a descriptive name for the query if you wish, then click **Close and Apply** to add the dataset to the report.

   </p>

   </details>

3. In *PowerBI Desktop*, select the **Map** visualization and drag the following **Fields** to their matching data points:

   | Field | Map Data Point | Note |
   | --- | --- | --- |
   | Computer | Size | |
   | ComputerEnvironment | Legend | |
   | RemoteIPLatitude | Latitude | Choose *"Don't summarize"* for the aggregation. |
   | RemoteIPLongitude | Longitude | Choose *"Don't summarize"* for the aggregation. |
   
   ***Variation 1:*** If you would like to see the Computer Names in each location, instead of the Environment Name, drag the *Computer* field to the *Legend* data point.
   
   ***Variation 2:*** If you prefer a simplified Country-level view you can drag the *RemoteIPCountry* field to the *Location* data point, however you cannot have both the *Location* and the combination of *Lat/Long* data points populated simultaneously.
   