# E-Commerce Advertising Attribution Models

> **Disclaimer: Data Confidentiality**
>
> **Raw data is not disclosed due to corporate confidentiality.**
> The datasets used in this project are not included in this repository. The code provided is for demonstration of the analysis logic, implementation methodology, and model architecture only. It cannot be executed without the original data.

> **Note on Code Implementation**
>
> * **Markov Chain Model**: The `markov_chain.ipynb` included in this repository is a version implemented by **Wang Chao-an**. Please note that the results presented in the final report were generated using a different implementation by **Ng Ka Chon**.
> * **First & Last Touch Models**: The `first_and_last_touch.ipynb` included here is implemented by **Wang Chao-an** and is the exact version used for the analysis in the report.

## Project Overview

This project is the final project for the **Big Data & Business Analytics** course.
Advertising is a crucial component of corporate marketing. Our goal is to analyze advertising sources that successfully convert into sales to identify the most potential advertising paths. This project implements multiple Multi-Touch Attribution (MTA) models to understand the Customer Journey of different brands and formulate optimal advertising budget allocation strategies.

### Core Objectives
* Identify customer journeys and touchpoints for different brands.
* Utilize the **Markov Chain** model to calculate advertising conversion rates and **Removal Effects**.
* Compare the differences between **First Touch**, **Last Touch**, and **Markov Chain** attribution models.
* Provide strategic business recommendations based on the analysis results.

## File Structure

This repository contains the following core analysis notebooks:

| File Name | Description |
| :--- | :--- |
| `markov_chain.ipynb` | **Markov Chain Model Implementation**<br>- Defines States: Start, Conversion, No_Conv, and various ad channels.<br>- Constructs the Transition Probability Matrix.<br>- Calculates the **Removal Effect** to determine the contribution of each channel to conversions.<br>*(Implementation by Wang Chao-an)* |
| `first_and_last_touch.ipynb` | **Rule-Based Attribution Implementation**<br>- **First Touch**: Attributes 100% of the credit to the first touchpoint in the path.<br>- **Last Touch**: Attributes 100% of the credit to the last touchpoint before conversion.<br>- Generates attribution shares and visualizes the data for each channel.<br>*(Implementation by Wang Chao-an)* |

## Methodology

We implemented and compared three attribution models:

1.  **Markov Chain Attribution**
    * Uses probabilistic methods to calculate the probability of users transitioning between different advertising channels.
    * Measures the **Removal Effect**—how much the overall conversion rate would drop if a specific channel were removed—to assess the true value of that channel.

2.  **First Touch Attribution**
    * Emphasizes **Acquisition**, considering the first advertisement that introduced the customer to the funnel as the most important.

3.  **Last Touch Attribution**
    * Emphasizes **Conversion**, considering the final advertisement that directly led to the purchase as the most important.

## Key Findings

We analyzed two different types of shops (Shop #0 and Shop #2) and found the following:

* **Shop #0 (Loyal Customer Oriented):**
    * **Direct Traffic** has an extremely high share, indicating a large number of returning customers or high brand loyalty.
    * To improve advertising effectiveness, strategies should prioritize **Google** and **Affiliate** channels.

* **Shop #2 (Ad-Driven):**
    * In traditional models (First/Last Touch), Direct traffic appears important.
    * However, under the **Markov Chain** model, the weight of Direct traffic drops significantly, while the weights of advertising channels like **System_Inform** and **Affiliate** increase.
    * This suggests that customers for this shop are largely motivated to purchase through advertising stimuli during their journey. Increasing the advertising budget is recommended.

## Team Member of Group 18

* Ng Ka Chon
* Li Hao-hsuan
* Hsu Po-wei
* Wang Chao-an
* Lin Yu-chen
* Tsou Shao-huan

---
*Created: 2024 | Updated & Translated: Oct 2025*