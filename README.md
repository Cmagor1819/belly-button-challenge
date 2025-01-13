# belly-button-challenge

# Objective:

In this assignment, you will build an interactive dashboard to explore the Belly Button Biodiversity datasetLinks to an external site., which catalogs the microbes that colonize human navels.

The dataset reveals that a small handful of microbial species (also called operational taxonomic units, or OTUs, in the study) were present in more than 70% of people, while the rest were relatively rare.

### HTML File:

This file contains the structure and creates the content of the webpage, including all of the hyperlinks that are needed and all of the JavaScript integrations.

### App.js

This files purpose is to build the metadata panel, build both the bar and bubble charts, the function to run on page load, and a function for event listener when a new sample is selected.

In this file we start with building the metadata panel by fetching the metadata field, filtering the metadata, appending new tags for each key-value in the filter, and finalizing the panel.

### Bubble chart:

Next we start building both the charts starting with the bubble chart. We need to fetch the samples field and store it, filter that data, fetch the (otu_ids, otu_labels, sample_values), and build the bubble. Finaly, we render the chart and plot it.

### Bar chart:

For the bar chart we start by fetching the samples, apply a filter based on name_one, slicing and reversing the data, and building the chart. We also added a hovertext inside the layout object.

### Init function:

For this section we start by fetching the names field, using d3 to select `#selDataset`, appending new options for each sample name, retrieving the first sample, and building the charts & metadata.

### Event listener function:

For this final section we build out charts and metadata each time a new sample selected and then we initialize the dashboard.

### I got/referenced the following lines of code from Xpert Learning Assistan/GitHub:

* Object.entries(first_result).forEach(([key, value]) =>{
      console.log(key,value);
      panel.append("h6").text(`${key}:${value}`);
    });
  
* let sample_values1 = first_result.sample_values.slice(0,10);
    let otu_ids1 = first_result.otu_ids.slice(0,10);
    let otu_labels1 = first_result.otu_labels.slice(0,10);

* y: otu_ids1.map(item => `OTU ${item}`).reverse(),

* let samplesFiltered = sampleData.filter(result => result.id == sample);
    

