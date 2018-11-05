### Import multiple items

> _Available for: [Managers](/managers/manager.md) and [Administrators](/admins/admin.md)_

On the [Recommendations](/visitors/recommendations.md), [Actions](/visitors/actions.md), [SDG Targets](/visitors/sdg-targets.md), and [Indicators](/visitors/indicators.md) list views you will (if signed in as a Manager or Administrator) find an 'Import' button (circled in screenshot below) to start adding multiple items at once - a time-efficient way to add new items:

![](/assets/m-action-import.png)  
_Screenshot from demo site ([demo.impactoss.org](https://demo.impactoss.org)) - all content for demo purposes only_

> When importing it is only possible to import actual item attributes (for recommendations this would be Title, Reference, Accepted Status and Accepted Response) but not any associations (e.g. thematic clusters, human rights body and cycle, etc.) - these will have to be set up manually.

#### Batch Import Screen

![](/assets/m-batch-import.png)  
_Screenshot from demo site ([demo.impactoss.org](https://demo.impactoss.org)) - all content for demo purposes only_

For all items the batch import screen (pictured above) allows you to  
1. Download a CSV template that specifies all the available fields that you can import (specific to each item type). If the template structure is not used then the batch import will not work.  
2. Select and upload a CSV file with content to import

#### How to import multiple items

> Note: the following import process is explained using item type 'Recommendations' but works the same for actions, indicators and SDG targets.

1. **Sign in**

   To use the batch import feature you will need to be signed with a user account of type [Manager](/managers/manager.md) or [Administrator](/admins/admin.md)

   See [Login](/guests/login.md).

2. **Open the batch import screen**

   From the recommendation list view (or any other item that allows importing), open the batch import screen by clicking the 'Import' button (see screenshot above).

3. **Download CSV template** (IMPACT OSS)

   If you do not already have a compatible CSV file for the item you are trying to import, you can download a CSV template on the batch import screen by clicking the 'Download the CSV template' link.

4. **Open CSV template** (MS Excel or similar spreadsheet editing software)

   Open the downloaded CSV template as a spreadsheet in MS Excel or similar spreadsheet editing software and inspect the fields.

   An example recommendations template opened in MS Excel is shown in the screenshot below:

   ![](/assets/import-rec-template.png)  
   _Screenshot of template downloaded from demo site ([demo.impactoss.org](https://demo.impactoss.org)) and opened in MS Excel - all content for demo purposes only_

   The first row's columns contain all the field descriptions and database field names in the square brackets `[database:title]` - please do not remove or edit the square brackets as these are required for the database to map the data.

   The second row contains some additional hints for each field, specifically specifying if the field is 'Required' or 'Optional', as well as the field type. Field types can be

   * `text`: a basic text field;
   * `text (markdown supported)`: a text field with basic formatting support using the markdown syntax (see [http://commonmark.org/help](http://commonmark.org/help) for formatting options);
   * `boolean`: a field that can either be true or false, accepted values are `true` or `false`, also `TRUE` or `FALSE`;
   * `date`: a date using the specified format (e.g. `YYYY-MM-DD`).

   See **[Principal concepts](concepts.md)** for required or optional fields.

   > Please note: the available fields may differ depending on your application set up.

5. **Prepare CSV template**

   To prepare the CSV template, please delete the second row. Do not however delete or replace the first row.

6. **Enter your data**

   Enter or copy and paste your data into the spreadsheet, using **one row for each recommendation** (or whatever items you are importing).

   ![](/assets/import-rec-editing.png)  
   _Screenshot of template downloaded from demo site ([demo.impactoss.org](https://demo.impactoss.org)) and opened in MS Excel - all content for demo purposes only_

   > Please note: when using the import feature for the first time it is recommended to test it with a small file only containing a limited number of items

7. **Save CSV file**

   Once all items have been entered, it is important to save the CSV file in the format "CSV UTF-8 (Comma delimited)", especially when special characters need to be supported.

   From the MS Excel 'File' menu select 'Save As', enter a suitable 'Filename' and select the format "CSV UTF-8 (Comma delimited)" from the 'Save as type:' dropdown as shown in the screenshot below

   ![](/assets/import-rec-save-csv.png)

   After selecting 'Save', Excel will then also require you to confirm the selected format:

   ![](/assets/import-rec-save-csv-confirm.png)

   > Note: this option is only available from Office 2016 - if you are using Office 2013 or older you will have to follow the instructions provided here  [https://help.evertrue.com/article/347-creating-a-utf-8-encoded-csv-file](https://help.evertrue.com/article/347-creating-a-utf-8-encoded-csv-file) or here [https://workstars-global-documentation.readthedocs-hosted.com/en/latest/howto/save-csv-utf8.html\#office-2013-and-older](https://workstars-global-documentation.readthedocs-hosted.com/en/latest/howto/save-csv-utf8.html#office-2013-and-older)

8. **Load file** (IMPACT OSS)

   Now that you have saved your file in the correct format, you are ready to load the file into IMPACT OSS. To do so

   * click the 'Select file' button in the batch import screen (see screenshot above)
   * select your file and press 'Open'
   * wait for IMPACT OSS to check and analyse your file

9. **Import data**

   If your file is compatible, the application will display the filename and make the 'Import' button available that also informs you about the number of found rows (excluding the first header row) as shown in the screenshot below:

   ![](/assets/import-rec-import.png)

   Then once you click 'Import x rows' the application will try to create each item one by one, raising any errors it may encounter in the process.

10. **Import complete**

    Once the import has successfully completed you can either chose to 'IMPORT ANOTHER FILE' or return 'BACK TO LIST' of recommendations (see screenshot below)

    ![](/assets/import-rec-import-success.png)

    > Please note: if you encounter any errors with some of the items, then make sure to remove the successfully imported rows from the template before trying again

11. **Review newly imported items**

    When returned back to the list view you can identify the recently imported items by filtering the list by 'Publication status' (select 'Draft') as the import feature only creates draft items (see [Explore Draft Content](/contributors/draft.md)). An alternative method would be to sort the list by creation date (see also [List view options](/visitors/lists.md)).

    Then open and inspect each item (or a large enough subset of the items) and verify that the data was imported as expected.

12. **Make linkages with categories and other items**

    If you are happy with the imported records you can then add tags such as 'human rights body' or 'affected person'. This is best done using the [batch edit feature](/managers/batch-edit.md)

13. **Publish newly imported items**

    As the batch import feature will always set the publication status to 'Draft', you will still have to publish them once you have reviewed and linked them. For how to publish a single item or multiple items see:[ Publish items](/managers/publish.md).
