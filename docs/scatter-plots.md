---
title: Creating Scatter Plots
parent: Introduction to Power BI 
layout: home
staff:
    - name: Kelly Schultz
      link: https://library.utoronto.ca/staff/kelly-schultz
maintainer:
    - name: Kelly Schultz
      link: https://library.utoronto.ca/staff/kelly-schultz
created_date: 2025-09-05
nav_order: 4
---
## Creating Scatter Plots

1. Sometimes you have to pull data from multiple sources instead of having it all in one file. Let’s add a couple more datasets, but this time we’re going to match them up or join them together to create one large dataset to work from, using the *Model view* of Power BI.
2. Go to the *Home* menu and select *Get data*. Select *Excel workbook* and choose the *AuthorDataCitationsGrants.xls*. Select the worksheet *AuthorDataMain*. The preview shows you that this dataset contains names of authors, their institutions their countries, and their research interests. And how many citations they’ve received over a few years, and how much grant money they’ve received over a few years. Click on *Load*.

    <img src='/assets/images/%7B63815D84-8F17-4D2E-B371-EED9B0EFAF97%7D.png' alt='Importing own data via the Home menu' title='' width='789' height='856' />

    <img src='/assets/images/%7B2ED42E08-70FE-45F1-ACE0-22D9F9BC8561%7D.png' alt='Importing own data' title='' width='943' height='958' />
3. Go to the *Home* menu and select *Get data* again. Select *Excel workbook* and choose the *AuthorDataExperience.xls*. Select the worksheet *AuthorDataExperience*. The preview shows you that this dataset has just author names along with how many years of experience they have as a researcher. Click on *Load*.

    <img src='/assets/images/%7B523AAD0F-5EFB-42D7-B4D0-904F62D19E08%7D.png' alt='Importing own data' title='' width='920' height='937' />
4. Next, go to the *Model view* by selecting the third icon down on the far left. The window shows us all the datasets we have loaded. For the last two datasets, you will see that the data has been related together based on a common column, *Author*. Power BI detected it automatically and has connected them with an arrow. You can click on the arrow to see the details of the relationship. Now the years of experience data will also be associated with the appropriate authors additional data found in the first table. Sometimes you might have to go to this view and manually connect your tables together, but in this case we don’t need to. If database joins and relationships are new to you, see this article on [relationships and joins](https://help.tableau.com/current/pro/desktop/en-us/datasource_relationships_learnmorepage.htm).

    <img src='/assets/images/image_55.png' alt='Selecting the Model View to see relationships' title='' width='913' height='491' /><img src='/assets/images/image_56.png' alt='Relationship between datasets by the connected arrow' title='' width='1186' height='351' /><img src='/assets/images/image_57.png' alt='Relationship details between datasets (clicking on arow)' title='' width='577' height='651' />
5. Go back to the *Report* view by clicking on the top icon in the far left. Then click on the new page icon at the bottom. Let’s rename this one to “Scatter Plot”.

    <img src='/assets/images/image_46.png' alt='Adding a Scatter Plot report page' title='' width='1204' height='174' />
6. Scatter Plots are great to use to identify if there is any relationship between numeric variables. Let’s see if there is a relationship between *Grants* and *Years of Experience*.
7. Select the *Scatter chart* icon from the *Visualizations* panel and drag the corner to fill the page.

    <img src='/assets/images/%7BF51BFE00-8881-489B-95EF-236FF6BD9827%7D.png' alt='Adding a Scatter Plot and resizing' title='' width='1298' height='766' />
8. Expand the two new datasets listed on the *Data* panel to check your variables, as we did before. Even though there’s no Sigma symbol next to *Years of Experience*, if you click on it to bring up the *Column tools* menu, you will see that the *Data type* is *Whole number*, so it is fine as is. It has just been set not to summarize, as it isn’t needed in this case.

    <img src='/assets/images/image_44.png' alt='Newly added data variables' title='' width='1364' height='644' />
9. Drag the *Years of Experience* variable from the *Data* panel, *AuthorDataExperience* to the *X\-axis, Add data fields here* box on the *Visualizations* panel. Next, drag the *Grants* variable from the *Data* panel, *AuthorDataMain* to the *Y\-axis, Add data fields here* box on the *Visualizations* panel.

    <img src='/assets/images/%7B1DE060E4-E8DB-42FC-A306-F9B4DEA4DD2F%7D.png' alt='Adding data to axes for visualization' title='' width='432' height='970' />
10. First, instead of summing up the *Grant* variable, let’s take the average in this case. Click on the arrow next to *Grants* (in the *Visualizations* panel for Y\-Axis) and select *Average* from the list. You can see other options you can choose when working with numeric variables.

    <img src='/assets/images/%7B59CF78DE-783C-40C1-AEE4-E18DE509B117%7D.png' alt='Changing y-axis settings to Average' title='' width='534' height='805' />
11. If you wanted to add another numeric variable to your scatterplot to turn it into a bubbleplot, you could drag the *Citations* variable from the *Data* panel, *AuthorDataMain* to the *Size, Add data fields here* box on the *Visualizations* panel. Now the bubbles are sized based on the *Sum of Citations*. If we want to remove this, or any variable we drag into a visual, we can click on the X next to that variable name on the *Visualizations* panel. Let’s remove *Sum of Citations* and go back to a scatterplot.

    <img src='/assets/images/image_59.png' alt='Adding Citations to the size parameter to create a bubbleplot' title='' width='1445' height='755' />

    <img src='/assets/images/%7BB0241F1A-026D-4358-A7C0-0A905ABA3F4E%7D.png' alt='Bubble Plot after configuring size parameter' title='' width='1923' height='1069' />

    <img src='/assets/images/image_60.png' alt='Removing the size parameter from our scatter plot' title='' width='1166' height='699' />
12. If you want to add another categorical variable to your scatterplot, you could do so by using different shapes to represent different categories. Drag the *Institution* variable from the *Data* panel, *AuthorDataMain* to the *Legend, Add data fields here* box on the *Visualization* panel. Now you should see that there is a legend, using different colours for different institutions.

    <img src='/assets/images/%7B71C27FF6-8709-47AD-9793-05A5546A71E5%7D.png' alt='Adding the Institution variable as our legend' title='' width='423' height='996' />
13. But when the marks are small, such as the dots in this case, it is helpful to also use different symbols to represent the points. Go to the *Format your visual* section of the *Visualizations* panel. Expand *Markers*, and then expand the *Shape and Color* sections. Right now it is one shape for all the categories in the series. But you can use the dropdown menu to select each category, in this case, each institution, and then select a shape and colour to go with it. Do this for each institution. You don’t need to click on *Okay* or *Apply*; as soon as you pick that category and those shapes and colours for it, it is applied. You should now see these changes in the scatterplot.

    <img src='/assets/images/image_61.png' alt='Modifying the marker symbology by institution' title='' width='150' height='856' />
14. Finally, if you want to add trend lines in Power BI, that is when you would use the icon to the right of the *Format your visual*, which provides analytical options. Click on that icon and then toggle *Trend line* on. You should now see a dashed line showing the trend in the scatterplot.

    <img src='/assets/images/%7BCFE6C54B-C94E-4AA6-BA30-E3BB9665F46B%7D.png' alt='Adding a Trendline to our scatter plot' title='' width='212' height='596' />

    <img src='/assets/images/image_63.png' alt='Sample Scatter Plot of Grants with Trend Line' title='' width='1140' height='639' />

**Technique:** [Data Visualization](https://mdlutoronto.github.io/tutorials-search/?technique=Data+Visualization) \| **Tools:** [Power BI](https://mdlutoronto.github.io/tutorials-search/?tool=Power+BI) \| **Data Format:** [Statistics](https://mdlutoronto.github.io/tutorials-search/?dataFormat=Statistics)