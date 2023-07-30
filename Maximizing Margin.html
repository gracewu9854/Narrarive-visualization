
<html>
<head>
  <title>Unraveling Profits: Exploring AmazingMart's Path to Enhanced Margins</title>
  <!-- Add D3.js library -->
  <script src="https://d3js.org/d3.v5.min.js"></script>
  <style>
    .dot{
      stroke: #0000;
    }
    /* Tooltip styling */
    #tooltip {
      position: absolute;
      opacity: 0;
      background-color: #f9f9f9;
      padding: 5px;
      border: solid #ccc 1px;
      border-radius: 3px;
    }
    /* Scene styling */
    #scene1, #scene2,#scene3 {
      display: none;
    }
    #scene1.active, #scene2.active,#scene3.active {
      display: block;
    }
  </style>
</head>
<body>
  <!-- Scene 1 -->
  <div id="scene1" class="active">
    <h1>Unraveling Profits: Exploring AmazingMart's Path to Enhanced Margins</h1>
    
    <p>In the competitive world of retail, understanding the nuances of sales data is key to unlocking greater profits. This visualization journey delves into the AmazingMart dataset, a rich trove of transaction details encompassing sales, discounts, and shipping methods across European countries.</p>
  
    <p>Our primary focus is to dissect and understand the factors that influence AmazingMart's margins, the lifeblood of profitability. We explore sales over time, investigate the impact of discounts on profit, and examine the role of shipping methods in shaping the bottom line. By the end of this journey, we aim to piece together a strategic narrative that could serve as a compass for AmazingMart to maximize its margins.</p>
  
    <p>Through this interactive visualization, we invite you to join us in this data exploration endeavor, where each dot and line tells a part of AmazingMart's ongoing story. With the power of data visualization, we can see beyond the numbers and uncover strategies that could push AmazingMart towards even greater success.</p>
    
    <!-- Date Range Filter -->
    <label for="start-date">Start Date:</label>
    <input type="month" id="start-date">
    <label for="end-date">End Date:</label>
    <input type="month" id="end-date">
    <br>
    
    <!-- SVG container for the graph -->
    <svg width="700" height="400" id="graph"></svg>
  
    <div id="tooltip">
      <span id="date"></span>
      <br/>
      <span id="sales"></span>
    </div>
  
    <script>
      // Create the SVG container for the graph
      const svg = d3.select('#graph'),
            margin = { top: 30, right: 20, bottom: 40, left: 50 },
            width = +svg.attr('width') - margin.left - margin.right,
            height = +svg.attr('height') - margin.top - margin.bottom,
            g = svg.append('g').attr('transform', 'translate(' + margin.left + ',' + margin.top + ')');
  
      // Scales for x and y axes
      const x = d3.scaleTime().range([0, width]),
            y = d3.scaleLinear().range([height, 0]);
  
      const tooltip = d3.select("#tooltip");
  
      // Function to fetch the data and render the graph
      d3.csv('https://raw.githubusercontent.com/gracewu9854/Narrarive-visualization/main/monthly_sales.csv', function(d) {
        // Convert 'order_month' to 'YYYY-MM' format
        const monthYear = d.order_month.split('-'); // Split '13-Nov' into ['13', 'Nov']
        const year = '20' + monthYear[0]; // Assuming '13' corresponds to '2013'
        const month = monthYear[1];
  
        d.order_date = year + '-' + month;
        d.sales = +d.sales; // Convert sales to a number
        return d;
      }).then(function(dataset) {
  
        // Calculate the minimum and maximum 'order_date' values in the dataset
        const minDate = d3.min(dataset, d => new Date(d.order_date));
        const maxDate = d3.max(dataset, d => new Date(d.order_date));
  
        // Set the default filter to the entire time range
        document.getElementById('start-date').value = minDate.toISOString().substr(0, 7);
        document.getElementById('end-date').value = maxDate.toISOString().substr(0, 7);
  
        // Set the domains of x and y scales
        x.domain([minDate, maxDate]);
        y.domain([0, d3.max(dataset, d => d.sales)]);
  
        // Define the line after the data is loaded and parsed
        const line = d3.line()
          .x(d => x(new Date(d.order_date)))
          .y(d => y(d.sales));
  
        // Append the line to the graph
        g.append('path')
          .data([dataset])
          .attr('class', 'line')
          .attr('fill', 'none')
          .attr('stroke', 'steelblue')
          .attr('stroke-width', 2)
          .attr('d', line);
  
        // Append dots for each data point
        g.selectAll(".dot")
          .data(dataset)
          .enter().append("circle") 
          .attr("class", "dot") 
          .attr("cx", function(d) { return x(new Date(d.order_date)) })
          .attr("cy", function(d) { return y(d.sales) })
          .attr("r", 5)
          .on("mouseover", function(d) {
              tooltip.style("opacity", 1)
                     .style("left", (d3.event.pageX + 10) + "px") 
                     .style("top", (d3.event.pageY - 10) + "px");
              d3.select("#date").text("Date: " + d.order_date);
              d3.select("#sales").text("Sales: " + d.sales);
          })
          .on("mouseout", function() {
              tooltip.style("opacity", 0);
          });
  
        // Append x and y axes
        g.append('g')
          .attr('class', 'x-axis')
          .attr('transform', 'translate(0,' + height + ')')
          .call(d3.axisBottom(x));
        g.append('g')
          .attr('class', 'y-axis')
          .call(d3.axisLeft(y));

        // Annotations

        // Highlight the importance of sales trends
        g.append('text')
          .attr('class', 'annotation')
          .attr('x', width / 2)
          .attr('y', -10)
          .attr('text-anchor', 'middle')
          .text('Notice the Seasonal Sales Patterns');
          
 

        // Highlight the importance of maximizing margins
        g.append('text')
          .attr('class', 'annotation')
          .attr('x', width / 2)
          .attr('y', height + 35)
          .attr('text-anchor', 'middle')
          .text('Enhanced Margins Lead to Greater Profitability');
  
        // Function to update the graph based on the selected date range
        function updateGraph() {
          const startDate = new Date(document.getElementById('start-date').value);
          const endDate = new Date(document.getElementById('end-date').value);
  
          // Filter the dataset based on the selected date range
          const filteredData = dataset.filter(
            d => new Date(d.order_date) >= startDate && new Date(d.order_date) <= endDate
          );
  
          // Update the x domain with the filtered date range
          x.domain([startDate, endDate]);
  
          // Update the line and x, y axes
          g.select('.line').data([filteredData]).attr('d', line);
          g.select('.x-axis').call(d3.axisBottom(x));
          g.select('.y-axis').call(d3.axisLeft(y));
  
          // Update the dots with tooltips
          const dots = g.selectAll(".dot")
                        .data(filteredData, function(d) { return d.order_date; });

          dots.enter().append("circle")
              .attr("class", "dot")
              .attr("r", 5)
              .merge(dots)
              .attr("cx", function(d) { return x(new Date(d.order_date)); })
              .attr("cy", function(d) { return y(d.sales); })
              .on("mouseover", function(d) {
                  // ... (existing tooltip code)
              })
              .on("mouseout", function() {
                  // ... (existing tooltip code)
              });

      dots.exit().remove();
    
        }
  
        // Attach event listeners to the date inputs
        document.getElementById('start-date').addEventListener('change', updateGraph);
        document.getElementById('end-date').addEventListener('change', updateGraph);
  
        // Initial graph rendering
        updateGraph();
      });
    
    </script>
  
    <h2>Understanding the Profits</h2>  
    <p>Through the previous visualization, we've taken a deep dive into AmazingMart's sales over time, and we've seen how our performance varies by month. But sales data only tells part of the story. To truly gauge our business performance, we need to examine profitability.</p>
    
    <p>Starting from here, we will embark on a new journey of exploration, trying to understand the profit landscape. What is the divide between profitable and non-profitable transactions? Which products are most profitable, and which are draining our resources? With the help of further visualizations, we will answer these crucial questions.</p>
  
    <p>As we proceed, we will maintain the same design and color schemes to make our analysis consistent and easy to understand. So, let's set sail on this new journey, and unravel the hidden secrets of AmazingMart's profitability...</p>
  

    <button id="next-to-scene2">Next Scene</button>
  </div>

  <!-- Scene 2 -->
  <div id="scene2">
    <h1>Scene 2: Exploring the Divide: Profitable vs. Non-Profitable Transactions</h1>
    <p>In this scene, we delve deeper into the financial anatomy of our business through the lens of each transaction. Through our interactive scatterplot, we examine the relationship between sales and profits, visualizing each transaction as an individual point.</p>
    
    <div id="scatterPlotContainer"></div>

    <div id="filterDiv">
      <label for="categoryFilter">Select a category:</label>
      <select id="categoryFilter"></select>
      
      <label for="subcategoryFilter">Select a sub-category:</label>
      <select id="subcategoryFilter"></select>
    </div>
    
    <script>
      // Load data from the CSV file
      d3.csv("https://raw.githubusercontent.com/gracewu9854/Narrarive-visualization/main/AmazingMart.csv").then(function (data) {
        // Convert data values from strings to numbers
        data.forEach(function (d) {
          d.sales = +d.sales;
          d.profit = +d.profit;
        });
    
        // Set the dimensions and margins for the plot
        const margin = { top: 30, right: 30, bottom: 40, left: 40 };
        const width = 600 - margin.left - margin.right;
        const height = 400 - margin.top - margin.bottom;
    
        // Create an SVG element that will contain the scatter plot
        const svg = d3.select("#scatterPlotContainer")
          .append("svg")
          .attr("width", width + margin.left + margin.right)
          .attr("height", height + margin.top + margin.bottom)
          .append("g")
          .attr("transform", `translate(${margin.left}, ${margin.top})`);
    
        // Create scales for x and y axes
        const xScale = d3.scaleLinear().domain([0, d3.max(data, (d) => d.sales)]).range([0, width]);
        const yScale = d3.scaleLinear().domain([d3.min(data, (d) => d.profit), d3.max(data, (d) => d.profit)]).range([height, 0]);
    
        // Create x and y axes
        const xAxis = d3.axisBottom(xScale);
        const yAxis = d3.axisLeft(yScale);
    
        // Append x and y axes to the SVG
        svg.append("g").attr("transform", `translate(0, ${height})`).call(xAxis);
        svg.append("g").call(yAxis);
        
        // Annotations
        // Create a separate 'g' element for annotations
        const annotationsG = svg.append('g');

        // Highlight the importance of the scatter plot
        annotationsG.append('text')
          .attr('class', 'annotation')
          .attr('x', width / 2)
          .attr('y', -10)
          .attr('text-anchor', 'middle')
          .text('Explore the Relationship Between Sales and Profits');

        // Add a yellow highlight behind the text
        annotationsG.insert('rect', 'text')
          .attr('x', width / 2 - 200)
          .attr('y', -25)
          .attr('width', 400)
          .attr('height', 20)
          .attr('fill', 'yellow');

        // Highlight the importance of the interactive filters
        annotationsG.append('text')
          .attr('class', 'annotation')
          .attr('x', width / 2)
          .attr('y', height + 35)
          .attr('text-anchor', 'middle')
          .text('Use the Filters to Explore Specific Categories and Sub-Categories');
        
          // Function to update the plot based on the selected category and sub-category
        function updatePlot(selectedCategory, selectedSubCategory) {
          // Filter the data based on the selected category and sub-category
          let filteredData = data;
          if (selectedCategory !== "All") {
            filteredData = filteredData.filter(d => d.Category === selectedCategory);
          }
          if (selectedSubCategory !== "All") {
            filteredData = filteredData.filter(d => d['Sub-Category'] === selectedSubCategory);
          }
    
          // Create circles for each data point and bind data to them
          const circles = svg.selectAll("circle").data(filteredData);
    
          // Remove any existing circles
          circles.exit().remove();
    
          // Update the circle positions and colors for existing and new circles
          circles.enter().append("circle")
            .merge(circles)
            .attr("cx", d => xScale(d.sales))
            .attr("cy", d => yScale(d.profit))
            .attr("r", 5) // Adjust the circle radius as needed
            .style("fill", function (d) {
              // Assign a different color to each category
              if (d.Category === "Office Supplies") return "blue";
              else if (d.Category === "Furniture") return "green";
              else if (d.Category === "Technology") return "red";
            });
    
          // Add tooltips to show the data values on mouseover
          circles.append("title")
            .text(d => `Sales: ${d.sales}, Profit: ${d.profit}, Category: ${d.Category}, Sub-Category: ${d['Sub-Category']}`);
        }
    
        // Initialize the dropdowns
        const categories = ["All", "Office Supplies", "Furniture", "Technology"];
        const subcategories = ["All", "Paper", "Bookcases", "Art", "Storage", "Fasteners", "Chairs", "Tables", "Labels", "Binders", "Machines", "Phones", "Appliances", "Supplies", "Copiers", "Envelopes", "Accessories", "Furnishings"];
    
        d3.select("#categoryFilter")
          .selectAll("option")
          .data(categories)
          .enter()
          .append("option")
          .text(d => d)
          .attr("value", d => d);
    
        d3.select("#subcategoryFilter")
          .selectAll("option")
          .data(subcategories)
          .enter()
          .append("option")
          .text(d => d)
          .attr("value", d => d);
    
        d3.select("#categoryFilter").on("change", function () {
          const selectedCategory = d3.select(this).property("value");
          const selectedSubCategory = d3.select("#subcategoryFilter").property("value");
          updatePlot(selectedCategory, selectedSubCategory);
        });
    
        d3.select("#subcategoryFilter").on("change", function () {
          const selectedCategory = d3.select("#categoryFilter").property("value");
          const selectedSubCategory = d3.select(this).property("value");
          updatePlot(selectedCategory, selectedSubCategory);
        });
    
        // Initialize the plot with all data points
        updatePlot("All", "All");
      });
    </script>
    <h2>Unleashing Opportunities: Strategies for Margin Improvement</h2>  

    <p>With the insights gained from Scene 2, we have unraveled the complex dynamics of AmazingMart's profit landscape. We've identified the disparity between profitable and non-profitable transactions, and even pinpointed specific sub-categories that might be adversely affecting our profit margins. But these discoveries are only half the story. The next crucial step is to translate these insights into actionable strategies for profit enhancement.</p>
    
    <p>In this scene, we will explore various strategies and their potential impact on our margins. We'll use interactive visualizations and predictive models to simulate different scenarios and gauge the likely outcomes of various strategic decisions. You'll be able to manipulate variables such as costs, pricing, and more to understand their potential impact on our profit margins.</p>
    
    <p>As we embark on this new journey, our visualizations will continue to follow the same design and color scheme to maintain consistency and ease of understanding. So, let's dive in and uncover the wealth of opportunities that lie ahead for AmazingMart...</p>
    
  
    <button id="back-to-scene1">Back</button>
    <button id="next-to-scene3">Next Scene</button>
  </div>
  <div id="scene3">
    <h1>Scene 3: Conclusion</h1>
    <p>Welcome to Scene 3. This is where we finalize our findings and provide strategic recommendations for AmazingMart.</p>
    <p>Our interactive visualization below allows you to explore sales performance by category within a chosen time frame. As you interact with the visualization, consider the potential impact of seasonal patterns on AmazingMart's sales. By understanding which product categories perform best at different times of the year, AmazingMart can better strategize its marketing and sales efforts.</p>
    <p>Select your desired start and end dates. Once the dates are chosen, a pie chart will appear. Each slice of the pie represents a different product category at AmazingMart. The size of the slice corresponds to the total sales of that category within your selected time period.</p>
    
    <p>Pay particular attention to the variations in category sales across different seasons. This analysis will allow you to identify which product categories are most popular during different seasons, providing valuable insights for AmazingMart's marketing and inventory management strategies.</p>
    <p>By leveraging these insights, AmazingMart can enhance its sales performance and profitability, ensuring the right products are prioritized at the right times.</p>
    <div id="dateFilterDiv">
      <label for="startDate">Select start date:</label>
      <input type="date" id="startDate">
      <label for="endDate">Select end date:</label>
      <input type="date" id="endDate">
    </div>
    
    <div id="pieChartContainer"></div>
    <!-- Add a tooltip div -->
    <div id="tooltip" style="position: absolute; opacity: 0;"></div>
    <!-- Add a div for the legend -->
    <div id="legend"></div>
    <script>
      // Load data from the CSV file
      d3.csv("https://raw.githubusercontent.com/gracewu9854/Narrarive-visualization/main/AmazingMart.csv", function (d) {
        // Convert 'order_date' to date format
        const parseDate = d3.timeParse("%m/%d/%Y");
        d.order_date = parseDate(d.order_date);
        d.sales = +d.sales; // Convert sales to a number
        return d;
      }).then(function (dataset) {
        // Function to update the pie chart based on the selected date range
        function updatePieChart(startDate, endDate) {
          // Clear the previous pie chart
          d3.select("#pieChartContainer").html("");
          
          // Filter the dataset based on the selected date range
          const filteredData = dataset.filter(
            d => d.order_date >= startDate && d.order_date <= endDate
          );
  
          // Group the data by category and calculate total sales for each category
          const nestedData = d3.nest()
            .key(d => d.Category)
            .rollup(values => d3.sum(values, d => d.sales))
            .entries(filteredData);
          const salesByCategory = nestedData.map(d => ({
            category: d.key,
            totalSales: d.value
          }));
  
          // Filter out any NaN values for totalSales
          const validSalesByCategory = salesByCategory.filter(d => !isNaN(d.totalSales));
      
          // Set up the pie chart dimensions
          const width = 400;
          const height = 400;
          const radius = 150
      
          // Create the pie chart layout
          const pie = d3.pie()
            .value(d => d.totalSales)
            .sort(null);
      
          // Create the color scale for the pie chart
          const colorScale = d3.scaleOrdinal(d3.schemeCategory10);
      
          // Create an SVG element for the pie chart
          const svg = d3.select("#pieChartContainer")
            .append("svg")
            .attr("width", width)
            .attr("height", height)
            .append("g")
            .attr("transform", `translate(${width / 2}, ${height / 2})`);
      
          // Create the pie chart slices
          const slices = svg.selectAll("path")
            .data(pie(validSalesByCategory))
            .enter()
            .append("path")
            .attr("d", d3.arc().innerRadius(0).outerRadius(radius))
            .attr("fill", d => colorScale(d.data.category))
            // Add tooltip on mouseover
            .on("mouseover", function(d) {
              d3.select("#tooltip")
                .style("left", d3.event.pageX + "px")
                .style("top", d3.event.pageY + "px")
                .style("opacity", 1)
                .html(`${d.data.category}: ${d.data.totalSales} (${(d.data.totalSales / d3.sum(validSalesByCategory, d => d.totalSales) * 100).toFixed(2)}%)`);
            })
            // Remove tooltip on mouseout
            .on("mouseout", function(d) {
              d3.select("#tooltip")
                .style("opacity", 0);
            });
  
          // Create the legend
          const legend = d3.select("#legend")
            .html("")
            .selectAll("div")
            .data(validSalesByCategory)
            .enter()
            .append("div")
            .style("display", "flex")
            .style("align-items", "center")
            .style("margin-bottom", "10px");
      
          legend.append("div")
            .style("width", "20px")
            .style("height", "20px")
            .style("background-color", d => colorScale(d.category));
      
          legend.append("div")
            .text(d => d.category)
            .style("margin-left", "10px");
        }
      
        // Create a parse function for the input dates
        const parseInputDate = d3.timeParse("%Y-%m-%d");
      
        // Attach event listeners to the date inputs
        document.getElementById('startDate').addEventListener('change', function () {
          const startDate = parseInputDate(document.getElementById('startDate').value);
          const endDate = parseInputDate(document.getElementById('endDate').value);
          updatePieChart(startDate, endDate);
        });
      
        document.getElementById('endDate').addEventListener('change', function () {
          const startDate = parseInputDate(document.getElementById('startDate').value);
          const endDate = parseInputDate(document.getElementById('endDate').value);
          updatePieChart(startDate, endDate);
        });
      
        // Initial pie chart rendering with the full data range
        const initialStartDate = d3.min(dataset, d => d.order_date);
        const initialEndDate = d3.max(dataset, d => d.order_date);
        document.getElementById('startDate').value = d3.timeFormat("%Y-%m-%d")(initialStartDate);
        document.getElementById('endDate').value = d3.timeFormat("%Y-%m-%d")(initialEndDate);
        updatePieChart(initialStartDate, initialEndDate);
      });
    </script>
    <button id="back-to-scene2">Back</button>
  </div>
  
  
  
  
  <script>
    document.getElementById('next-to-scene2').addEventListener('click', function() {
      // Hide Scene 1 and Show Scene 2
      document.getElementById('scene1').classList.remove('active');
      document.getElementById('scene2').classList.add('active');
    });

    document.getElementById('next-to-scene3').addEventListener('click', function() {
      // Hide Scene 2 and Show Scene 3
      document.getElementById('scene2').classList.remove('active');
      document.getElementById('scene3').classList.add('active');
    });

    document.getElementById('back-to-scene1').addEventListener('click', function() {
      // Hide Scene 2 and Show Scene 1
      document.getElementById('scene2').classList.remove('active');
      document.getElementById('scene1').classList.add('active');
    });

    document.getElementById('back-to-scene2').addEventListener('click', function() {
      // Hide Scene 3 and Show Scene 2
      document.getElementById('scene3').classList.remove('active');
      document.getElementById('scene2').classList.add('active');
    });
  </script>
  
</body>
</html>
