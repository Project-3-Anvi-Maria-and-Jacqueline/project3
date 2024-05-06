### Project 3
#### Anvitha Chaluvadi, Jacqueline Raynolds, and Maria Notarianni

# **<ins>Pricing NFTs Using APIs</ins>**

# Background
In the rapidly growing landscape of Non-Fungible Tokens (NFTs), understanding their pricing dynamics is crucial for both buyers and sellers. However, the pricing of NFTs can be complex, influenced by various factors such as rarity, popularity, and cultural relevance. As such, there is a need for tools and methodologies to assist individuals, especially newcomers, in comprehending NFT pricing trends.

## Installation Instructions
To run the project locally, follow these steps:

1. Install Python 3.x.
2. Install Anaconda Navigator.
3. Clone this repository.
4. Install required Python libraries using `pip install -r requirements.txt`.

## Usage
Data preparation is a critical step in the data analysis and machine learning pipeline. It involves cleaning, transforming, and organizing raw data into a suitable format for analysis or model training. This process enhances the quality and usability of data, ensuring that subsequent analyses or models are accurate and reliable.

The key activities in data preparation include:

- **Data Cleaning**: Identifying and correcting errors, inconsistencies, missing values, and outliers in the data. This step ensures the data is accurate and complete.

- **Data Transformation**: Converting data into a format or structure that is more suitable for analysis. This includes normalizing or scaling numerical data, encoding categorical variables, and creating or modifying features.

- **Data Integration**: Combining data from multiple sources into a coherent dataset. This often involves aligning data formats, resolving data conflicts, and ensuring consistent data definitions.

- **Data Reduction**: Reducing the volume but not the integrity of the data, to focus on relevant information. Techniques include dimensionality reduction, feature selection, and sampling.

- **Data Splitting**: Dividing the dataset into subsets for training and testing models. This is crucial for evaluating the performance of predictive models in a way that is unbiased.

- **Model Training**: Use the prepped data to train machine learning models. Try out different algorithms and tweak features to see what works best. It's akin to practicing and refining a performance before the big show.

- **Model Interpretation**: Understand and explain what the model's predictions mean, look into which features matter most, and check for any biases. Ensure the model's decisions are clear and justified, much like a judge explaining their ruling in court.

Effective data preparation accelerates the data analysis process, improves model accuracy, and leads to more insightful and actionable outcomes.

## Motivation & Summary
**Objective:** 
Our goal is to create a simple tool using machine learning to help people understand how NFT prices work, specifically focusing on the [Pudgy Penguins](https://opensea.io/collection/pudgypenguinscollection) on [OpenSea](https://opensea.io/).

**Method:** 
We're using a technique called machine learning, which is basically teaching a computer to learn patterns from data, to figure out what makes [Pudgy Penguins](https://opensea.io/collection/pudgypenguinscollection) valuable.

**Data Source:** 
We're getting our information from [OpenSea's](https://opensea.io/) data on the [Pudgy Penguins](https://opensea.io/collection/pudgypenguinscollection) collection.

**Flexibility:** 
While we're looking at [Pudgy Penguins](https://opensea.io/collection/pudgypenguinscollection) specifically, this method could be used for other NFT collections too.

**PM Comment:** 
We want to make sure our tool is easy to use, so we're trying to keep things simple and straightforward.

## Pudgy Penguins Overview
[Pudgy Penguins](https://opensea.io/collection/pudgypenguinscollection) is a collection of 8,888 unique NFTs known for their contributions to Web3 innovation through intellectual property and community engagement. These penguins represent values of affection, empathy, and positivity, providing exclusive perks to their owners, such as access to events and special experiences.

- **Volume:** 345,970.149573
- **Sales:** 78,963
- **Average Price:** 4.381421 ETH
- **Number of Owners:** 4,778
- **Market Cap:** 103,268.203657 ETH
- **Floor Price:** 12.5 ETH
- **Floor Price Symbol:** ETH

## Categories
To categorize the traits of [Pudgy Penguins](https://opensea.io/collection/pudgypenguinscollection), we have identified five main categories:
- Background
- Skin
- Body
- Face
- Head

  <p align="center"> <img src = traits.png width =45% height 30%=/> </p>


## APIs Integration
We integrated various APIs to gather comprehensive data for our analysis:
- Opensea APIs
- Traits Summary Counts
- NFT Sales Events
- Individual NFT Information

## Dataframe Components
Our dataframe consists of the following components:
- Events Data
- NFT Token (nft.identifier)
- Closing Date (for ETH comparison)
- Payment Quantity (wei)
- Pagination (50 per page)
- Individual NFT Info
- Traits for Each NFT
- Loop Function for Sampling 50 Sales
- Exporting Data (static) using the `to_csv` command

## Linear Regression Model Evaluation
**R² Explanation:** 
R-squared (R²) explains the extent to which the variance of one variable explains the variance of the second variable. A higher R-squared value indicates a better fit of the model to the data.

**Training Dataset (Descriptive Value)**
- R-squared (R²) Score: 0.6909513484448644
- This suggests that traits strongly describe the price in the training data, with only 30% noise.

<p align="center"> <img src = train_plot.png width =45% height 30%=/> </p>


**Testing Dataset (Predictive Value)**
- R-squared (R²) Score: -1.4725014974827797e+26
  - Unfortunately, the model cannot effectively predict prices in the testing dataset.
  
<p align="center"> <img src = testing_dataset.png width =45% height 30%=/> </p>


## Challenges in Model Performance Assessment
- **Issue:** High dimensionality with limited data points
- **Ideal Scenario:**
  - Increased dataset size
  - Reduced feature space
  - Emphasized need for a significantly larger dataset by Sean

## Future Avenues for Solving This Problem
- Converting ETH-USD
- Fixing API issues
- Isolating traits
  - Consider focusing on the top 10 traits
- Addressing Overfitting:
  - Attempted PCA feature reduction, but the explained variance ratio was low
  - Pulling more data to address overfitting in Linear Regression, but conversion fluctuations in ETH-USD impact outcomes

## Data Sources
The dataset used in this project can be found at [encoded_data.csv](https://github.com/Project-3-Anvi-Maria-and-Jacqueline/project3/blob/main/encoded_data.csv).

## Results
Our linear regression model, despite performing well in describing the relationship between traits and price in the training dataset with an R-squared (R²) score of 0.69, exhibited a significant discrepancy in predicting prices on the testing dataset, yielding a super low R-squared (R²) score of -1.47e+26. While the scatter train plot and dashed line provided insights into the model's effectiveness, showing accurate predictions when points clustered tightly around the line, the wide scattering of points suggested areas for improvement. Therefore, further investigation and improvement are necessary to enhance the model's predictive capabilities.

### <ins>Presentation</ins> 
[Pricing NFTs Using NFTs Presentation](https://docs.google.com/presentation/d/1PGDx3zYDpcDUW4wMAs_VFKhvpY08bwEgjp0JIBRMWXE/edit?usp=sharing)
