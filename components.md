### Principal concepts

The following diagram that is also rendered on the application's Overview page (see [Visitor overview](visitors/visitor.html)) shows the principal concepts of IMPACT OSS and how they relate.

![](/assets/concepts.png)  
_Screenshot from demo site ([demo.impactoss.org](https://demo.impactoss.org)) - all content for demo purposes only_

---

#### Recommendations

![](/assets/icon-recommendations.png)

Each country is party to a number of human rights treaties. For each treaty it has a range of legal obligations to implement and it regularly receives **Recommendations**, also called observations, from the respective Treaty Bodies on specific areas for improvement.

Additionally each country undertakes a **Universal periodic Review (UPR)** every 4.5 years and has a standing invitation to all **United Nations Special Procedures**. Out of both of these processes each country receives also recommendations for how to implement its human rights obligations.

##### Recommendation fields

Required fields:

- **Title**: The full text or public title of a recommendation or observation. If an additional field for the 'Full recommendation text' is available (depends on configuration, see below), a less technical and shorter title also aimed at public audiences should be entered here.
- **Reference**: A _unique_ reference that allows to easily identify a particular recommendation. For references it is best to use any references or numbers if provided by the recommending mechanism and thus allow universal identification and if not a sensible numbering.

  > Note: rather than using just numbers, it is better to also encode the mechanism and cycle (or year) to guarantee long-term uniqueness and consistency. Bad examples would be using `5` and `6` as there may be many 5th recommendations across different mechanisms and cycles, a good example would be `CRC-2017-5` and `CRC-2017-6` as it will always be unique))

Optional fields (may be omitted in some installations)

- **Full recommendation text**: The original recommendation text in full length, allows entering a shorter and less technical public title (see above).
- **Government response**: The response given for UPR recommendations, one of 'Accepted' or 'Noted'. Will default to 'Accepted' for other recommendations as implicitly assumed.
- **Government response comment**: Any response comment a government may provide along with the response (UPR only).


For more information see
- **[Explore Recommendations ](/visitors/recommendations.md)**
- **[Manage Recommendations](/managers/recommendations.md)**

---

#### Actions

![](/assets/icon-action.png)

> _Also referred to as_
> - _**Government actions**_
> - _**Implementing actions**_

The **Actions** the Government and partners are doing or planning to implement human rights and achieve the SDGs form the overall National **Implementation Plan**. Actions address the Recommendations (see above) and -if configured- optionally also the SDG Targets (see below).

Required fields:

- **Title**: The action title as defined by the Government
- **No.**: A number that is automatically assigned by the application and serves as a unique identifier

Optional fields (may be omitted in some installations)

- **Description**: A more detailed description of the action.
- **Target date**: The date by when the government aims to have the action completed.
- **Target date comment**: Any comment to further explain the target date.
- **Outcome**: A text field for describing the outcomes, either interim outcomes of ongoing or final outcomes of completed actions.
- **Indicator summary**: A text field for summarising any progress or outcome indicators that may be set up or used to track action progress.


For more information see
- **[Explore Action Implementation Plan](/visitors/actions.md)**
- **[Manage Actions](/managers/actions.md)**


---

#### Indicators

![](/assets/icon-indicators.png)

> _Also referred to as **Progress indicators**_

Each Action and -when configured- optionally also SDG targets should have at least one **Indicator**. Indicators can be set up to measure implementation progress or outcomes. These can also include the SDG indicators specified to measure outcomes related to the SDG targets (see below).

For more information go to **[Explore Indicators](/visitors/indicators.md)**

Required fields:

- **Title**: The indicator name.

Optional fields (may be omitted in some installations)

- **Reference**: Optionally for assigning a user-defined unique identifier - if left blank the application will automatically assign a reference.
- **Description**: The full detailed description of the indicator.
- **Progress report schedule: Due date**: The due date of a required progress report for indicator (one-off, not repeat).
- **Progress report schedule: Start date**: The start date for a series of required progress reports for indicator (repeat).  
- **Progress report schedule: End date**: The end date for a series of required progress reports for indicator (repeat).
- **Progress report schedule: Update frequency**: The update frequency for a series of progress reports for indicator (repeat).
- **Assigned user**: A user responsible for providing progress reports.

For more information see
- **[Explore Indicators](/visitors/indicators.md)**
- **[Manage Indicators](/managers/indicators.md)**

---

#### SDG Targets (optional configuration)

![](/assets/icon-sdg.png)

The **SDG Targets** are the 169 internationally agreed targets to achieve the 17 SDGs (Sustainable Development Goals). For each target one or more SDG indicators have also been defined.

Required fields:

- **Title**: The title (or short title) of an SDG target.
- **Reference**: The SDG target reference e.g. `1.1`

Optional fields (may be omitted in some installations)

- **Description**: An optional detailed description of the SDG target.

> Please note that IMPACT OSS can optionally also be configured without SDGs

For more information see
- **[Explore SDG Targets](/visitors/sdg-targets.md)**
- **[Manage SDG Targets](/managers/sdg-targets.md)**

---

#### Category groups (or taxonomies)

![](/assets/icon-categories.png)

Categories are the ways in which Actions, Recommendations and the SDG Targets are indexed and classified which is useful for searching and filtering, as well as reporting and analysis. IMPACT OSS is pre-configured with multiple groups of categories (technically called **taxonomies**) during installation that each contain multiple **categories** that can be set up by platform managers and administrators (see [Manage Categories](managers/categories.md))

> Please note: you can only add new categories to existing taxonomies (category groupings), but you cannot add new taxonomies. Additional taxonomies or changing how taxonomies are configured can only be set up by the technical site administrator

Category fields (required):

- **Title**: The category name.

Category fields (optional fields, may be omitted in some installations)

- **Short title**: A short name for the category as used for category tags. If left blank application will display an abbreviation of the Title.   
- **Reference**: An optional reference of the category where applicable. Can also be used for forcing sort order (categories are by default ordered by title or reference if provided).
- **Description**: A long description of the category. Can also include any commentary provided.
- **Website**: Any website address that may provide further information about the category.


For more information see
- **[Explore by Category](/visitors/categories.md)**
- **[Manage Categories](/managers/categories.md)**

##### Example Taxonomies

Taxonomies can include global category groups as universally used by the UN and national category groups that are only relevant to a specific state.

> Please note that IMPACT OSS can be configured with many different category groups and individual installations can thus differ significantly

![](/assets/categories.png)  
_Schema of a possible taxonomy configuration, showing category groupings on left and principal entities on the right_

###### Human Rights Mechanisms (or Bodies)

![](/assets/icon-hr-bodies.png)

> _Commonly tag_
> - _Recommendations_
> - _Actions_

This taxonomy covers all different **Human Rights Mechanisms** that can make recommendations to a State on how to implement its human rights obligations. There are several different types of categories which may fall under this taxonomy:

* **Treaty Body Committees**: For each international human rights convention (e.g. Convention on the Rights of the Child) there is an accompanying Treaty Body Committee. The body makes recommendations to each State that has ratified the treaty and it is these recommendations which are entered into the application and are addressed through the National Implementation Plan.
* **Universal Periodic Review**: Every 4.5 years every member of the United Nations undergoes a Universal Periodic Review - a peer to peer review of each country's human rights record. The outcome document contains recommendations which are entered into the database in the same way as recommendations received from the treaty body committees.
* **Special Procedures**: The United Nations has many special procedures mandate holders - either working groups or individuals who are independent experts and who are granted a mandate to examine a particular human rights issue. Arising from these type of visits is a report also containing recommendations, which will be entered into the national Implementation Plan as above.
* **Regional mechanisms**: for some States there may also be relevant regional mechanisms providing recommendations.

---

###### Reporting cycles

![](/assets/icon-cycles.png)

> _Commonly tag_
> - _Recommendations_

Both the treaty body reviews and the Universal Periodic Review are regular and ongoing. The **Reporting Cycles** taxonomy allows recommendations to be classified by specific cycle. E.g. if the user wants to only view recommendations and associated actions from the most recent Universal Periodic Review they can easily select this using the 'Reporting Cycles' category.

---

###### Human rights issues (or 'Themes')

![](/assets/icon-hr-issues.png)

> _Commonly tag_
> - _Recommendations_
> - _Actions_

The Office of the United Nations High Commissioner for Human Rights has developed a [Human Rights Index](http://uhri.ohchr.org/en/) which contains a classification system that is the basis for the **Human Rights Issues** taxonomy. It helps users search by particular area of interest and see what the Government is doing in that field of work.

---

###### Affected persons (or 'Vulnerable groups')

![](/assets/icon-affected-persons.png)

> _Commonly tag_
> - _Recommendations_
> - _Actions_

In the same way that 'Human Rights Issues' allows users to examine particular issues in detail, **Affected Persons** allows the user to do that with a wide range of demographics. This is again based on the United Nations Human Rights Index system.

---

###### Recommendation Clusters (or 'National Themes')

![](/assets/icon-clusters.png)

> _Commonly tag_
> - _Recommendations_
> - _Actions_

Every United nations member State receives hundreds of recommendations from the human rights bodies, the Universal Periodic Review and the Special Procedures. There is often overlap between some of the recommendations and in many case they can be similar or be the same. This can make the management of those recommendations more difficult than it needs to be. The application allows the Government to cluster recommendations into general **Recommendation Clusters** to help alleviate this issue.

Clustering recommendations in this way can not only help to make implementation more manageable but it can also help to identify crossover and eliminate duplication of work and reporting.

---

###### Organisations (or 'Implementing Agencies')

![](/assets/icon-organisations.png)

> _Commonly tag_
> - _Actions_
> - _Users_

The **Organisations** taxonomy lists the Government agencies (and others) carrying out actions contained within the National Implementation Plan. Visitors can use this taxonomy to easily see what work any particular Ministry is doing in the areas of human rights and the SDGs at the click of a button. If your organisation is doing a variety of work related to the actions contained with the National Implementation Plan you can contact the administrator using the 'Contact' link on the website to discuss your involvement.

---

###### Progress status

![](/assets/icon-progress.png)

> _Commonly tag_
> - _Actions_

The **Progress status** taxonomy allows marking Government action progress, either as
- In Progress
- Completed

---

###### Sustainable Development Goals (SDGs)

![](/assets/icon-sdgs.png)

> _Commonly tag_
> - _SDG targets_
> - _Recommendations_

In addition to being a tool which helps track and coordinate implementation a country's human rights obligations, the application also does the same in relation to the **SDGs**. Visitors can therefore click on this taxonomy to explore the SDG Targets in more detail or to look into what actions the Government is taking to achieve the SDGs. The tool helps to draw the links between the work the Government is doing in relation to the SDGs and the work it is doing in relation to human rights, again eliminating duplication and increasing efficiency.

> Note: Depending on the configuration SDGs could also be used to classify Recommendations and/or Actions


---

Explore this manual by **[User type & common use case](/usecases.md)**
