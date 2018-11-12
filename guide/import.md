### Import: create multiple items

This step-by-step guide will illustrate how to import multiple **Recommendations** or **Government actions** at once.

> Note: When importing it is only possible to import actual item attributes (for recommendations this would be Title, Reference, Accepted Status and Accepted Response) but not any associations (e.g. thematic clusters, human rights body and cycle, etc.) - these will have to be set up manually.

![](https://docs.google.com/drawings/d/e/2PACX-1vQ07OAJSQ-heRG6_rbq06Cl72D8RwxHN_UJDLExztrjbseZd4i9I_x7ImuyP_m10L0l2tB_z3Z6FoyY/pub?w=972&h=579)

> Note: the following screenshots are either showing recommendation OR action lists but unless otherwise stated they are applicable to both (in fact they also apply in principal to any other list page, including **User admin**, **Page admin**, and **Indicator list**, as well as **SDG target** list if configured)

---

#### Pre-requisites: registered, promoted and logged in

In order to enter and cluster recommendations you will need to

1. be registered
2. be promoted to a 'Manager' or 'Administrator' user role (see **[User roles](/info/userroles.md)**)
3. logged in

---

#### 1. Go to list page

To go to the list of recommendations simply select **Recommendations** from the primary navigation menu, for the list of actions that form the implementation plan select **Implementation plan** (also see [Navigation](/intro/navigation.md)).

![](/assets/enter-recs_1-1.png)
_Screenshot from demo site ([demo-rights.impactoss.org](https://demo-rights.impactoss.org)) - all content for demo purposes only_

> Note: depending on your configuration menu item names may differ

---

#### 2. Click IMPORT

From the recommendation list view (or any other item that allows importing), open the batch import screen by clicking the 'Import' button (see screenshot above).

![](/assets/import_2.png)
_Screenshot from demo site ([demo-rights.impactoss.org](https://demo-rights.impactoss.org)) - all content for demo purposes only_

---

#### 3. Prepare CSV file

##### 3.1. Download CSV template (IMPACT OSS)

If you do not already have a compatible CSV file for the item you are trying to import, you can download a CSV template on the batch import screen by clicking the 'Download the CSV template' link.

![](/assets/import_3.png)
_Screenshot from demo site ([demo-rights.impactoss.org](https://demo-rights.impactoss.org)) - all content for demo purposes only_

##### 3.2. Open CSV template (MS Excel or similar spreadsheet editing software)

 Open the downloaded CSV template as a spreadsheet in MS Excel or similar spreadsheet editing software and inspect the fields.

 An example recommendations template opened in MS Excel is shown in the screenshot below:

 ![](/assets/import_3-2.png)  
 _Screenshot of template downloaded from demo site ([demo-rights.impactoss.org](https://demo-rights.impactoss.org)) and opened in MS Excel - all content for demo purposes only_

The first row's columns contain all the field descriptions and database field names in the square brackets `[database:title]` - please do not remove or edit the square brackets as these are required for the database to map the data.

The second row contains some additional hints for each field, specifically specifying if the field is 'Required' or 'Optional', as well as the field type. Field types can be

* `text`: a basic text field;
* `text (markdown supported)`: a text field with basic formatting support using the markdown syntax (see [http://commonmark.org/help](http://commonmark.org/help) for formatting options);
* `boolean`: a field that can either be true or false, accepted values are `true` or `false`, also `TRUE` or `FALSE`;
* `date`: a date using the specified format (e.g. `YYYY-MM-DD`).

> Please note: the available fields may differ depending on your application set up.

##### 3.3. Prepare CSV template

To prepare the CSV template, please delete the second row. Do not however delete or replace the first row.

##### 3.4. Enter your data

Enter or copy and paste your data into the spreadsheet, using **one row for each recommendation** (or whatever items you are importing).

![](/assets/import_3-4.png)  
_Screenshot of template downloaded from demo site ([demo-rights.impactoss.org](https://demo-rights.impactoss.org)) and opened and updated in MS Excel - all content for demo purposes only_

> Please note: when using the import feature for the first time it is recommended to test it with a small file only containing a limited number of items

##### 3.5. Save CSV file

 Once all items have been entered, it is important to save the CSV file in the format "CSV UTF-8 (Comma delimited)", especially when special characters need to be supported.

 From the MS Excel 'File' menu select 'Save As', enter a suitable 'Filename' and select the format "CSV UTF-8 (Comma delimited)" from the 'Save as type:' dropdown as shown in the screenshot below

 ![](/assets/import-rec-save-csv.png)

 After selecting 'Save', Excel will then also require you to confirm the selected format:

 ![](/assets/import-rec-save-csv-confirm.png)

 > Note: this option is only available from Office 2016 - if you are using Office 2013 or older you will have to follow the instructions provided here  [https://help.evertrue.com/article/347-creating-a-utf-8-encoded-csv-file](https://help.evertrue.com/article/347-creating-a-utf-8-encoded-csv-file) or here [https://workstars-global-documentation.readthedocs-hosted.com/en/latest/howto/save-csv-utf8.html\#office-2013-and-older](https://workstars-global-documentation.readthedocs-hosted.com/en/latest/howto/save-csv-utf8.html#office-2013-and-older)

---

#### 4. Import data (IMPACT OSS)

##### 4.1. Load file

Now that you have saved your file in the correct format, you are ready to load the file into IMPACT OSS. To do so

* click the 'Select file' button in the batch import screen (see screenshot above)
  ![](/assets/import_4-1-1.png)    
* select your file and press 'Open'
  ![](/assets/import_4-1-2.png)  
* wait for IMPACT OSS to check and analyse your file

##### 4.2. Import data

If your file is compatible, the application will display the filename and make the 'Import' button available that also informs you about the number of found rows (excluding the first header row) as shown in the screenshot below:

![](/assets/import-rec-import.png)

Then once you click 'Import x rows' the application will try to create each item one by one, raising any errors it may encounter in the process.

Once the import has successfully completed you can either chose to **IMPORT ANOTHER FILE** or return **BACK TO LIST** of recommendations (see screenshot below)

![](/assets/import-rec-import-success.png)

> Please note: if you encounter any errors with some of the items, then make sure to remove the successfully imported rows from the template before trying again

##### 4.3. Review items

When returned back to the list view you can identify the recently imported items by filtering the list by 'Publication status' (select 'Draft') as the import feature only creates draft items. An alternative method would be to sort the list by creation date (see also [List view options](/visitors/lists.md)).

Then open and inspect each item (or a large enough subset of the items) and verify that the data was imported as expected.

##### 4.4. Publish items

As the batch import feature will always set the publication status to 'Draft', you will still have to publish them once you have reviewed and linked them. For how to publish a single item please see for example section 3 of [Recommendations: enter & cluster](/guide/enter-recommendations.md) or for multiple items at once see [Batch edit: update multiple](/guide/batch-edit.md).
