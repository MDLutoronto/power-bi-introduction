---
title: Introduction to Power BI | Map and Data Library
layout: home
description: 
---

# Introduction to Power BI | Map and Data Library

This tutorial outlines the steps taken in the demonstration during the live workshop on an Introduction to Data Visualization Using Power BI. This is a companion tutorial, but can also be used as a stand\-alone introduction to Power BI Desktop.

Table of Contents
-----------------

* [Creating Bar Graphs](#Creating Bar Graphs)
* [Creating Line Graphs](#Creating Line Graphs)
* [Creating Pie Charts](#Creating Pie Charts)
* [Creating Scatter Plots](#Creating Scatter Plots)
* [Saving and Publishing](#Saving and Publishing)

### Set Up and Starting Up

1. Download the 3 example dataset Excel files and save them somewhere on your computer where you can find them, such as your Desktop:
	* [AuthorDataCitationGrants.xlsx](https://maps.library.utoronto.ca/workshops/Tableau2022/AuthorDataCitationsGrants.xlsx)
	* [AuthorDataExperience.xlsx](https://maps.library.utoronto.ca/workshops/Tableau2022/AuthorDataExperience.xlsx)
	* [RomeoAndJulietWordFrequenciesByAct.xlsx](https://maps.library.utoronto.ca/workshops/Tableau2022/RomeoAndJulietWordFrequenciesByAct.xlsx)
2. Make sure you have [Power BI installed](https://mdl.library.utoronto.ca/technology/tutorials/installing-power-bi-desktop).

### 

### Power BI Demo

Open up Power BI.

#### Creating Bar Graphs

1. This first screen gives you an opportunity to load your data from many different file types/formats. But we are going to start with a sample dataset from Power BI first. Click on the *Learn with sample data* tab.

    <img src='/assets/images/%7BE6A1704B-E3E4-432C-9275-8DBD51E3E713%7D.png' alt='Selecting the Learn with sample data option on Power BI home page' title='' width='945' height='572' />
2. In the pop\-up, select *Load sample data* (Power BI may take a few seconds to connect). Select *financials* on the left (to select that sheet of the data) and then click on the *Load* button at the bottom. It is just some standard business data about sales of different products. We’ll talk more about loading in our own data later.

    <img src='/assets/images/%7B90342C3D-FDA7-4D86-835D-53F2529CA77D%7D.png' alt='Learning with Sample Data options, using the Load sample data button' title='' width='841' height='559' /><img src='/assets/images/%7BF2ABB5F7-B5ED-4EEA-9D3C-B899AF003EED%7D.png' alt='Selecting a data source for loading' title='' width='942' height='767' />
3. Let’s look around first before we dive in. On the far right you can see the *Data* panel. If you expand *financials*, you can see all the columns or variables from the dataset we just loaded in. There are symbols next to the variables to help signal if Power BI understands their data type. For example, it often understands the variable to be numeric if there’s a little Sigma (Σ) sign to the left of it (saying it will sum this variable as a default), or for text there’s no symbol, or for a date field there’s a little calendar to the left of it.

    <img src='/assets/images/image_49.png' alt='Data panel in Power BI with different data types for variables' title='' width='1300' height='796' />
4. To the left of the *Data* panel is the *Visualizations* panel, which we will use to build our visualizations, and adjust the formatting of them.

    <img src='/assets/images/image_51.png' alt='Visualizations panel used to create figures and adjust formatting' title='' width='1293' height='793' />
5. To the left of that is a *Filters* panel, which we can use to filter our data. We will look at all of these panels as we work with the tool.

    <img src='/assets/images/image_62.png' alt='Filter panel in Power BI used to configure data filters for visualizations' title='' width='1292' height='791' />
6. At the bottom, you’ll see a tab that says *Page 1*. In Power BI, you create 'report' pages that can have one or more visualizations displayed. These are similar to Excel sheets.

    <img src='/assets/images/%7B3DBA2BCA-84C3-4FCC-8958-A395F3EB9A75%7D.png' alt='Report/Page Navigation in Power Bi' title='' width='939' height='608' />
7. On the far left, there are a few icons that change the view. The default view is the *Report view* where you build your visuals. The icon looks like a bar graph. If you click on the icon below that, we switch to the *Table view*, where you can see the data in a spreadsheet format. If you click on the icon below that, we switch to the *Model view*. If we had loaded in multiple datasets, we could tell Power BI how they were connected to each other through common columns, etc. We will take a look at this view a bit later, when discussing database relationships. For now, let’s go back to the Report view, by clicking on its bar graph icon on the left.

    <img src='/assets/images/image_41.png' alt='Changing view in Power Bi' title='' width='1176' height='783' />
8. Okay, we’ve loaded in some data about a fictional company’s sales, so let’s start by creating some visualizations that are used to make comparisons. Let’s start by making a simple bar graph. To keep track of all the visualizations we’re going to create, let’s rename our pages as we go. Right\-click on *Page 1* at the bottom, select *Rename*, and give it the name “Sales Bar” and press *Enter*. You don’t need to only have one visualization per page, and normally, you don’t – you normally lay out a page with a few visualizations to tell a story. But for now, to simplify things, we will keep it to one visualization per page.

    <img src='/assets/images/%7BF93DC5A0-FEF2-457E-91FE-4ACD20FB85A2%7D.png' alt='Renaming our Report page to "Sales Bar"' title='' width='1095' height='122' />
9. We’re going to create a horizontal bar graph to compare the sales for different products, with products along the y\-axis and sales along the x\-axis. Bar graphs are great for comparing categories, such as products. So, select the horizontal stacked bar chart icon from the *Visualizations* panel (the top left icon). (Note: If you hover over a visual, it tells you its name). Expand the box by dragging the bottom right corner to make it fit the page.

    <img src='/assets/images/%7B0C36FB6D-345B-4EA6-BA8F-0F9B189A68C3%7D.png' alt='Adding a Bar Chart and resizing' title='' width='1230' height='614' />
10. Next, drag the *Sales* variable from the *Data* panel to the *X\-axis*, *Add data fields here* box on the *Visualizations* panel. Then drag the *Product* variable from the *Data* panel to the *Y\-axis*, *Add data fields here* box on the *Visualizations* panel.

    <img src='/assets/images/%7B9BFB4AD1-34A4-4EC0-9D4D-6C89F9D4159F%7D.png' alt='Adding data to axes for visualization via dragging' title='' width='359' height='749' />

    <img src='/assets/images/%7B1608A1A6-4FC9-4AB5-B0FA-DDD0160487E3%7D.png' alt='Default bar chart after adding data' title='' width='1133' height='636' />
11. You can see that when we dragged *Sales*, it automatically summarized it by adding up all the sales values for each product. Right now, it is showing data combined for all of the countries for this global company, but let’s say we just want it to show one of them. We can use the *Filters* panel to filter just this visual, all visuals on this page, or all visuals on all pages, by dragging our variable into the appropriate box that says *Add data fields here*. For example, let’s filter by country for this visual by dragging the *Country* variable from the *Data* panel over to the *Filters* panel, to the *Add data fields here* under the *Filters* *on this visual* heading. You should now see a list of countries we can choose from to filter. Let’s select Canada.

    <img src='/assets/images/%7B5FB6017E-97CF-4BFE-90BF-AA0998DA7A50%7D.png' alt='Adding a filter to our bar chart using the Country variable via dragging' title='' width='813' height='1085' />
12. Now we have a bar graph showing the Sales by Product for Canada.

    <img src='/assets/images/%7B33329E04-AFA1-43BA-94E5-FC23C6E5CE6D%7D.png' alt='Sample Bar Graph: Sum of Sales by Product Canada' title='' width='960' height='500' />
13. Next let’s look at how we can start formatting our visual. On the *Visualizations* panel, you will see 3 icons at the top, just above the available visuals. We’ve been looking at the *Add data to your visual* section (left icon), with the different visualizations to choose from. If we click on the next icon to the right, we are in the *Format your visual* section. Here, for example, we can change the colour of the bars. Click on the *Format your visual* tab and expand *Bars* and choose a colour you like.

    <img src='/assets/images/%7B570881A0-BFB9-4747-AF06-60C45BAF3B1D%7D.png' alt='Formatting the colour of your figure within the Visualizations panel' title='' width='393' height='1068' />
14. The *Data labels* option allows to create and customize labels. We can, for example, turn on *Data labels* using the toggle switch. Expand *Data labels*, and then expand *Options* underneath. We can also adjust the position. For example, using the dropdown menu for *Position*, which currently says *Auto*, change it to *Inside end*, so that the values are labeled within the bar, instead of next to the bar. This provides a cleaner look. But in this case, we have an axis to help users read the bar values, so let’s keep the show *Data labels* toggled off for now for a simpler design.

    <img src='/assets/images/%7B901D001F-77D0-4BCD-B869-E1BA752CAF89%7D.png' alt='Adding Labels to the Data within the Bars' title='' width='203' height='347' /><img src='/assets/images/%7B41C0B98E-7B1D-4ADF-81B3-467712ACFBAC%7D.png' alt='Sample illustration of Data Labels configured with the above settings' title='' width='1130' height='639' />
15. As you can see, there are options to customize a lot of parts of the visualization. You can also customize the axes. For example, expand the X\-axis. Here you can make changes to your axis, such as the range of values. In our case, we’re fine to keep it as *Auto*. But we can change the X\-axis label, though. Let’s change it to say “Sales in US Dollars”. In the X\-axis section, expand the *Title* section underneath and change the title text from Auto to “Sales in US Dollars”. You should see your changes applied to the x\-axis. Also expand *Values* and make the axis labels larger, by changing the font to 12pt.

    <img src='/assets/images/%7B66429E0A-E88A-4105-A961-040DD4AC00A0%7D.png' alt='Configuring the visuals for the x-axis' title='' width='201' height='923' />
16. We can also make the *Product* name labels larger. Expand the *Y\-axis*, and then expand *Values*. Change the font to 12 pt.

    <img src='/assets/images/%7BE1D4E247-FEC2-43DB-86B7-864DFA662704%7D.png' alt='Configuring the font size of our y-axis labels' title='' width='203' height='409' />
17. We can give our visualization a more meaningful title. So far, we’ve been making adjustments in the *Visual* tab. But if you go to the *General* tab, we can expand *Title*. For the *Text*, we can put “Sales by Product for Canada“. We can also change the font to make it a bit larger – say 24 pt. Be careful when making this change, as the *Title* was originally dynamic based on what data was selected. If you adjust the data in the visual later, the title won’t change automatically.

    <img src='/assets/images/%7BF00273E2-CC2E-43C9-AD88-9CB0DFDA333A%7D_0.png' alt='Modifying the General visualization parameters' title='' width='198' height='780' />
18. Finally, right now the bars are sorted by sales. This is good so that you can easily see the top and bottom products in terms of sales. But you can change the sort order. For example, perhaps you want to sort it alphabetically by product name, to make it easier to find a product in the list. Click on the three dots at the top right of the visual. Then select *Sort Axis* and select *Product*. Go back to the *Sort Axis* option and change it to *Sort Ascending*. Now it is in alphabetical order by *Product name*. Now we’re done our first visualization!

<img src='/assets/images/image_42.png' alt='Adjusting the legend for our Bar Chart' title='' width='1173' height='576' />

 

#### Creating Line Graphs

1. Okay, let’s create a new visualization. We need a new page. Click on the *New page* (\+)icon at the bottom of the screen. Rename this one to “Line”.

    <img src='/assets/images/image_43.png' alt='Renaming our Report page to "Line"' title='' width='917' height='206' />
2. We’re going to create a line graph now, which is great to show trends over time. We’re going to create a line graph of change in total profit over time. Select the *Line chart* visual from the *Visualizations* pane. Drag the corner to make it fit the page.

    <img src='/assets/images/%7B0A369C78-1E46-4774-99ED-A52170711D27%7D.png' alt='Adding a Line Chart and resizing' title='' width='1118' height='605' />
3. Next, drag the *Date* variable from the *Data* panel to the *X\-axis*, *Add data fields here* box on the *Visualizations* panel. Click on the drop\-down arrow next to *Date*, and select *Date*, instead of *Date Hierarchy*. The *Date Hierarchy* features allows the user to drill\-down to different levels, like quarters or months, but the way the data is then grouped can be very misleading. I don’t think this is a good feature, so I would suggest you disable it by having Power BI not use hierarchies.

    <img src='/assets/images/%7BB9B22696-8EFE-48D3-8CF5-5A8A55140251%7D.png' alt='Adding data to axes for visualization' title='' width='435' height='935' />

    <img src='/assets/images/image_47.png' alt='Opting for Date instead of Date Hierarchy' title='' width='472' height='344' />
4. Next drag the *Profit* variable from the *Data* panel to the *Y\-axis*, *Add data fields here* box on the *Visualizations* panel.

    <img src='/assets/images/%7B247AA518-D498-4F7B-AE42-C74784691FC8%7D.png' alt='Adding data to axes for visualization' title='' width='435' height='924' /><img src='/assets/images/%7BF3BB691C-2172-4BB8-A0CD-635051F311A6%7D.png' alt='Default line chart after adding data' title='' width='1127' height='638' />
5. It might be useful to see this graph broken down by Products – so basically adding a 3rd variable. The *Product* variable is a categorical variable, so we can assign different coloured lines for each category to display this information on the graph. To do this in Power BI, you drag *Product* from the *Data* panel to the *Legend*, *Add data fields here* box on the *Visualization* panel. Power BI has assigned a qualitative colour palette scheme, assigning different colours to represent our products, but this could make our graph a bit overwhelming as there are a fair few number of products.<img src='/assets/images/%7BC88AF566-3721-46EA-A85C-29F5CC4F657C%7D.png' alt='Adding data to axes for visualization' title='' width='432' height='931' />

    <img src='/assets/images/%7B2D1E1E6E-D42C-44E9-9596-2854262D692A%7D.png' alt='Sample Line Graph after adding Products variable' title='' width='1939' height='1098' />
6. Let’s say you didn’t like these colours for the lines. Go to the *View* menu at the top (Ribbon: File, Home, Insert, etc.). On the left, you should see various colour themes you can apply to your visual. If you hover over the theme, some have “Accessible” in the title, so in theory they should be good colour choices to use if you might have colour blindness in your audience. However, in practice, some of these accessible themes seem to have colours that are hard to distinguish between, even for those without colour blindness. Using a colour blind simulator, such as [Coblis](https://www.color-blindness.com/coblis-color-blindness-simulator/), can more reliably help you with these decisions. Pick a theme to apply it.

    <img src='/assets/images/image_48.png' alt='Selecting a different colour palette for our Line Chart' title='' width='985' height='741' /><img src='/assets/images/image_50.png' alt='Line chart with newly selected colours (City Park)' title='' width='1021' height='590' />
7. Now, when creating visualizations, you always need to figure out what your main message is. What is the story you are trying to tell. So one way to simplify this would be to show a comparison between two particular products of interest. We can do this by dragging *Products* over to the *Filters* panel and selecting two products – let’s pick *Amarilla* and *Montana*. This could tell a story, such as that profit in a few cases seems to run opposite for the two products – one is making a large profit when the other one isn’t. Or that Amarilla has some larger profit spikes than Montana.

    <img src='/assets/images/%7B19D64F9E-4AED-4004-9BA1-F566B8A13C8D%7D.png' alt='Adding data to filters for visualization' title='' width='650' height='945' />

    <img src='/assets/images/image_52.png' alt='Sample Line Graph after selecting Amarilla and Montana for comparison' title='' width='1119' height='543' />
8. Another way we could tell a story, would be to allow the user to filter it themselves based on what products they are interested in – so adding an interactive element. To do that, go back to *Filters* panel, and click on the X next to the *Product* filter to remove it.

    <img src='/assets/images/%7B682FABF4-2875-4414-B1D2-AB13E0295E05%7D.png' alt='Removing the filter variable by selecting X' title='' width='217' height='652' />
9. Instead let’s use something called a slicer to allow the user to select what products they want to see. First, make sure that you don’t have the line graph selected by clicking on the space below the graph. Then select the *Slicer* icon from the *Visualizations* panel (icon has a small funnel in front of a visual). Drag it to the top right of the visual and make the height much smaller as we’re going to turn it into a drop\-down list.

    <img src='/assets/images/%7B8AADEF75-A908-4C72-ADAB-5EC7D4415CA1%7D.png' alt='Adding a slicer to our visualization' title='' width='203' height='587' />

    <img src='/assets/images/image_53.png' alt='Resizing the added slicer to the top-right' title='' width='1038' height='590' />
10. Next, drag the *Product* variable from the *Data* panel to the *Field*, *Add data fields here* box on the *Visualizations* panel.

    <img src='/assets/images/%7BDCE51970-6CD9-46C0-BFE6-F8C6D6F2DDD1%7D.png' alt='Adding data to field for visualization' title='' width='438' height='594' />
11. Go to the *Format your visual* section of the *Visualizations* panel. Expand *Slicer* *settings* and then expand *Options*. Under *Style*, select *Dropdown*.

    <img src='/assets/images/%7B7DA689A1-C3DE-4B4C-A4E4-BB6FDAA1117B%7D.png' alt='Selecting Slicer style' title='' width='208' height='572' />
12. Next, expand *Selection*. Toggle on *Show “Select all”* option. Now use the slicer to filter your graph. Hold down the Ctrl key if you want to select more than one option.

    <img src='/assets/images/%7B129AB44A-9E23-440E-B0BD-3CA91008427D%7D.png' alt='Toggling the Show "Select all" option in the Slicer' title='' width='206' height='463' />
13. If you can’t see the Slicer options, it might be that you have the line graph selected. Just click in the blank space below the group to see everything again. And that’s it, we have our second visual!

    <img src='/assets/images/image_54.png' alt='Sample Line Graph after adding a slicer' title='' width='1033' height='587' />

#### Creating Pie Charts

1. Okay let’s try loading our own data – this time based on some qualitative humanities data. Power BI is not meant to work directly with text data files, but you can use other better\-suited textual analysis tools to create datasets that you can then visualize in Power BI. What I did was take the freely available text for Shakespeare’s play Romeo and Juliet. I ran it through a free online tool called [Voyant Tools](https://voyant-tools.org/) and it generated a word frequency table that we are now going to use as our dataset. If you want to learn more about textual analysis and visualization tools, such as Voyant, you can take a look at the [Tools \& Tutorials](https://mdl.library.utoronto.ca/dataviz/tools-tutorials) page in the [Data Visualization guide](https://mdl.library.utoronto.ca/dataviz/getting-started).
2. Let’s load this word frequency data into Power BI. From the *Home* menu (top ribbon), select *Get Data, Excel Workbook*.

    <img src='/assets/images/%7B63815D84-8F17-4D2E-B371-EED9B0EFAF97%7D.png' alt='Importing own data via the Home menu' title='' width='789' height='856' />
3. Pick *RomeoAndJulietWordFrequenciesByAct.xls* (navigate to where you saved the data). From the data preview window, select the only sheet in the file, *TermFrequenciesByAct*.

    You can see that it is a simple spreadsheet that counts how many times a term/word came up in each act. At the bottom, you’ll see a button that says *Transform Data*. This opens up the Power Query Editor tool where you can do data cleaning tasks, such as cleaning up blank rows or columns, changing a column type to date, and highlighting columns and selecting unpivot to convert from wide format to long format. We don’t need to do those tasks on this dataset, so we’ll leave it as is for now and just click on *Load Data*.

    <img src='/assets/images/%7BF6F4AD1D-FE8C-483A-B3AC-15E6B3111E26%7D.png' alt='Selecting and Loading our own data' title='' width='699' height='727' />
4. Let’s click on new page to get started. Let’s rename this one to “Pie”.

    <img src='/assets/images/image_45.png' alt='Adding a Pie report page' title='' width='1003' height='179' />
5. Let’s first make a simple pie chart to show how many words are in each Act of the play, to see which Act is the longest and shortest and how they contribute to the whole.
6. Before we begin building our visualization, let’s make sure our variables are correct. If we expand our dataset on the *Data* panel and look at what the variable types Power BI has identified in our dataset, you’ll notice that it thinks *Act* is a numeric variable that you can sum, when really it is text in this case (the sections of the play are divided into numbered acts, but you wouldn’t do math with these numbers). So let’s change it. If you click on *Act*, you’ll see at the top a new menu has appeared called *Column tools*. For the *Data Type*, it says *Whole number*, but you can fix it. Click on the dropdown menu arrow and select *Text*.

    <img src='/assets/images/%7B56AAE72B-9749-4FE4-A4B0-345CCD208469%7D.png' alt='Misclassified data type' title='' width='226' height='117' /><img src='/assets/images/%7BA3C4277C-283E-4884-B270-C88BBFE0FB8D%7D.png' alt='Changing column data type for Act' title='' width='840' height='473' />
7. Now we are ready to create a pie chart. Select the *Pie chart* icon from the *Visualizations* panel, and drag the corner so it fills the page.

    <img src='/assets/images/%7B8428DFA5-FA9F-4974-AED2-6F30F3B1D4E7%7D.png' alt='Adding a Pie Chart and resizing' title='' width='1239' height='582' />
8. Drag the *Act* variable from the *Data* panel to the *Legend, Add data fields here* box on the *Visualizations* panel (nothing will display at this point). Next, drag the *Count* variable from the *Data* panel to the *Values, Add data fields here* box on the *Visualizations* panel.

    <img src='/assets/images/%7B8B324F06-AD6C-465B-974C-4F726CAA4589%7D.png' alt='Adding data to our Pie Chart' title='' width='538' height='983' />
9. Next, let’s work with the formatting. It is automatically showing the percentages, which is great, but also showing other information. Let’s have it just display percentages. Go to the *Format your visual* section of the *Visualizations* panel. Expand *Detail labels*, and for *Label contents*, select *Percent of total*.

    <img src='/assets/images/%7BEC13FE02-A388-4B1C-ADFA-547AE21D98DF%7D.png' alt='Selecting Pie Chart Labelling parameter' title='' width='259' height='929' />
10. Expand *Values* and change the font size to 14pt to make the labels more legible. We could also format the percentages to round to whole numbers. Further down under *Values*, change the *Percentage decimal places* to 0\.

    <img src='/assets/images/%7B367C0617-BAE3-4E53-AC73-9F3D9351AF32%7D.png' alt='Pie Chart labelling properties (font, decimals, etc.)' title='' width='263' height='563' />
11. You will notice we also have an issue with the legend not being in order. We can fix this with sorting. Click on the three dots at the top right of the visual. Select *Sort Axis, Act*. Go back to *Sort Axis* and select *Sort ascending*. Now the legend and the slices are in the order the Acts are in the play.

    <img src='/assets/images/%7B861C01B8-B98A-496E-9969-937D14CA6BB4%7D.png' alt='Adjusting the legend for our Pie chart' title='' width='1386' height='674' />
12. We can see the number of words used is quite evenly distributed throughout the acts, but Act 3 uses the most and Act 5 uses the least.

    <img src='/assets/images/%7B72227CE8-F9CE-442F-9252-D8BA6EA2B950%7D.png' alt='Sample Final Pie Chart' title='' width='1127' height='627' />

#### Creating Scatter Plots

1. Sometimes you have to pull data from multiple sources instead of having it all in one file. Let’s add a couple more datasets, but this time we’re going to match them up or join them together to create one large dataset to work from, using the *Model view* of Power BI.
2. Go to the *Home* menu and select *Get data*. Select *Excel workbook* and choose the *AuthorDataCitationsGrants.xls*. Select the worksheet *AuthorDataMain*. The preview shows you that this dataset contains names of authors, their institutions their countries, and their research interests. And how many citations they’ve received over a few years, and how much grant money they’ve received over a few years. Click on *Load*.

    <img src='/assets/images/%7B63815D84-8F17-4D2E-B371-EED9B0EFAF97%7D.png' alt='Importing own data via the Home menu' title='' width='789' height='856' />

    <img src='/assets/images/%7B2ED42E08-70FE-45F1-ACE0-22D9F9BC8561%7D.png' alt='Importing own data' title='' width='943' height='958' />
3. Go to the *Home* menu and select *Get data* again. Select *Excel workbook* and choose the *AuthorDataExperience.xls*. Select the worksheet *AuthorDataExperience*. The preview shows you that this dataset has just author names along with how many years of experience they have as a researcher. Click on *Load*.

    <img src='/assets/images/%7B523AAD0F-5EFB-42D7-B4D0-904F62D19E08%7D.png' alt='Importing own data' title='' width='920' height='937' />
4. Next, go to the *Model view* by selecting the third icon down on the far left. The window shows us all the datasets we have loaded. For the last two datasets, you will see that the data has been related together based on a common column, *Author*. Power BI detected it automatically and has connected them with an arrow. You can click on the arrow to see the details of the relationship. Now the years of experience data will also be associated with the appropriate authors additional data found in the first table. Sometimes you might have to go to this view and manually connect your tables together, but in this case we don’t need to. If database joins and relationships are new to you, see these articles on [relationships](https://help.tableau.com/current/pro/desktop/en-us/datasource_relationships_learnmorepage.htm) and [joins](https://www.codeproject.com/articles/Visual-Representation-of-SQL-Joins).

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

#### Saving and Publishing

1. Now so far we’ve been creating one visualization per page. But normally you use a page to combine a number of visualizations together to present a more complex story than a single visualization can show. You can then also use the *Insert* menu to add text, images, etc. to create a final report.

    <img src='/assets/images/%7B141BCAEB-2AE1-4329-9ECD-B1E50C426CF2%7D.png' alt='Available options in the Insert menu' title='' width='1236' height='211' />
2. Once you’ve created some reports, your last steps are to save and publish them. If you’re working on some visualizations, like we have here, you can save work\-in\-progress as a Power BI Workbook file. Go to the *File* menu and click on *Save*. Give it a name and select where you want to save the file. You can then come back to revisit your work later by reopening it in Power BI.

    <img src='/assets/images/%7BF62E58FC-705B-435A-8DBB-D031AD916659%7D.png' alt='Saving your Power BI Project' title='' width='672' height='920' />
3. It does seem to store the data in the project file, so you can share it with another user(s). But there could be issues if it wants to refresh the data. I have better luck if I share the workbook file and the data files together. If you keep them in the same folder, it should work fine. If the path to the data files changes, go to the dropdown menu for *Transform data* from the *Home* menu and select *Data source* *settings*. Here you can correct the path to the data files, if you’ve moved them.

    <img src='/assets/images/%7B42201B2C-F0F3-4FE1-8C13-F80B1F675A1E%7D.png' alt='Setting a Data source (path to your data)' title='' width='1233' height='541' />
4. You can also export your report as a static PDF. To do so, go to the *File* menu and choose *Export, Export to PDF*. This will save all the pages of your report into one PDF file.

    <img src='/assets/images/%7B8373E66F-1D4C-44B1-A739-B88D6D19CA41%7D.png' alt='Exporting your visualizations as a PDF' title='' width='636' height='653' />
5. Note: As our dashboard, and visualizations can also be interactive, there may be times when you want to publish them to the web so that your users can view them. As a student using the free version of Power BI, unfortunately, your options are limited. Click on *Publish* from the *Home* menu, choose *My workspace*, and click on *Select*. After it uploads, it’ll give you a link to open up the report in the Power BI Service online space. You can view it and interact with it here on the web.

    <img src='/assets/images/image_64.png' alt='Publishing a project online to your workspace' title='' width='516' height='631' /><img src='/assets/images/image_65.png' alt='Online Power BI Report' title='' width='1768' height='892' />
6. You can also use the *Export* option here to export it as a PowerPoint presentation. But again it’ll be static images.

    <img src='/assets/images/image_66.png' alt='Exporting as a PowerPoint in Power BI Online ' title='' width='1045' height='536' />
7. If you have the paid version of Power BI, here is where you would be able to share this report with others, but unfortunately, if you try to click on *Share* as a student, you will get a message saying this is a paid feature. Basically with the free version of Power BI, your only option to share an interactive version of your report, is to share the workbook file and require the recipient to have Power BI as well and view it from within the tool.

    <img src='/assets/images/image_67.png' alt='Sharing Power BI report without subscription' title='' width='911' height='717' />
8. To wrap up, I also just want to show you some examples of what a final Power BI report might look like. You can Google to find lots of good examples online. Here is an example from [Zoom Charts](https://zoomcharts.com/en/microsoft-power-bi-custom-visuals/dashboard-and-report-examples/). When you click on an example you’re interested in, you can not only interact with it, but also download the Power BI workbook file to see how it was done. A great way to learn!

    <img src='/assets/images/image_68.png' alt='Sample Power BI Report on ZoomCharts with download and interact options' title='' width='782' height='542' />

And that’s it!

Technique: [Data Visualization](/technique/data-visualization) \| Tools: [Power BI](/tools/power-bi) \| Data Format: [Statistics](/data-format/statistics)**Date Created:** 2025\-09\-05**Updated:** 2025\-09\-26