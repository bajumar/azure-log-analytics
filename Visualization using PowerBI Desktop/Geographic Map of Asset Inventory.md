
# Geographic Map of Asset Inventory

***UNDER CONSTRUCTION***

1. Run the following query in Azure Monitor Logs:

   ```
   // Table of Computer Geo-Locations
   Heartbeat
   | distinct Computer, ComputerEnvironment, RemoteIPCountry, RemoteIPLatitude, RemoteIPLongitude
   ```

2. Folow the instuctions to export the query and import it into PowerBI Desktop - https://docs.microsoft.com/en-us/azure/azure-monitor/platform/powerbi

   <details><summary>Click here for a summary of the instructions...</summary>
   <p>

   **In Azure Monitor Logs:**

   1. After running a query, in the menu bar select **Export > Power BI Query (M)** to generate a "PowerBIQuery.txt" file.

   2. Open the "PowerBIQuery.txt" text file and copy its contents.

   **In PowerBI Desktop:**

   1. In the top menu bar click on the **Get Data** button and choose **Blank Query** to open the *Query Editor* window.

   2. In the *Query Editor* window, from the top menu bar select **Advanced Editor**.

   3. In the *Advanced Editor* window paste the contents of the exported file into the query and click **Done**. You may be prompted for credentials to connect to Azure.

   4. Type in a descriptive name for the query if you wish, then click **Close and Apply** to add the dataset to the report.

   5. Create your report. If you wish to publish the report to PowerBI, in the top menu bar click on the **Publish** button.

   </p>

3. In PowerBI Desktop, select the **Map** visualization and drag the following **Fields** to their matching data points: