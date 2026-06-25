---
title: Creating Pie Charts
parent: Introduction to Power BI 
layout: home
staff:
    - name: Kelly Schultz
      link: https://library.utoronto.ca/staff/kelly-schultz
maintainer:
    - name: Kelly Schultz
      link: https://library.utoronto.ca/staff/kelly-schultz
created_date: 2025-09-05
nav_order: 3
---
## Creating Pie Charts

1. Okay let’s try loading our own data – this time based on some qualitative humanities data. Power BI is not meant to work directly with text data files, but you can use other better\-suited textual analysis tools to create datasets that you can then visualize in Power BI. What I did was take the freely available text for Shakespeare’s play Romeo and Juliet. I ran it through a free online tool called [Voyant Tools](https://voyant-tools.org/) and it generated a word frequency table that we are now going to use as our dataset. If you want to learn more about textual analysis and visualization tools, such as Voyant, you can take a look at the [Tools & Tutorials](https://mdl.library.utoronto.ca/dataviz/tools-tutorials) page in the [Data Visualization guide](https://mdl.library.utoronto.ca/dataviz/getting-started).
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

**Technique:** [Data Visualization](https://mdlutoronto.github.io/tutorials-search/?technique=Data+Visualization) \| **Tools:** [Power BI](https://mdlutoronto.github.io/tutorials-search/?tool=Power+BI) \| **Data Format:** [Statistics](https://mdlutoronto.github.io/tutorials-search/?dataFormat=Statistics)