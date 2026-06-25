---
title: Creating Line Graphs
parent: Introduction to Power BI 
layout: home
staff:
    - name: Kelly Schultz
      link: https://library.utoronto.ca/staff/kelly-schultz
maintainer:
    - name: Kelly Schultz
      link: https://library.utoronto.ca/staff/kelly-schultz
created_date: 2025-09-05
nav_order: 2
---
## Creating Line Graphs

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

**Technique:** [Data Visualization](https://mdlutoronto.github.io/tutorials-search/?technique=Data+Visualization) \| **Tools:** [Power BI](https://mdlutoronto.github.io/tutorials-search/?tool=Power+BI) \| **Data Format:** [Statistics](https://mdlutoronto.github.io/tutorials-search/?dataFormat=Statistics)