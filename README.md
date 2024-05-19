# Prompt-Engineering-using-LLMs
Phishing URL Detection with Prompt Engineering using Large Language Models

**Background**

Phishing attacks are a form of social engineering where attackers attempt to deceive victims into revealing sensitive information or clicking on malicious links and it remains a persistent threat in the digital landscape, causing significant financial losses and data breaches. Phishing has become increasingly sophisticated, making it challenging to distinguish legitimate URLs from fraudulent ones.
Recently, Large Language Models (LLMs) have been making significant impacts on various tasks including Machine Learning(ML) application development. These models are notable due to the use of vast amount of training datasets from diverse fields that the models are trained; and demonstrating impressive adaptability and performance across industries and regular human life.

**Objective**

This project aim to assess whether LLMs can provide a more efficient yet effective alternative to detect phishing URLs.
A new technique called prompt engineering which involves crafting specific input prompts to guide the LLM toward desired outputs without modifying the model itself can be utilized to detect phishing.

**Methodology**

 The phishing dataset is collected from Mendeley Data (https://data.mendeley.com/datasets/c2gw7fy2j4/3) which has a total of 11,430 URL samples, and each URL is accompanied by 88 extracted features including a status column to classify the URLs. This project randomly selected 100 URLs with balanced classification, comprising 50 legitimate and 50 phishing URLs. A python script is used to randomly sample the dataset.

Prompt engineering refers to the process of carefully crafting prompts to elicit desired responses from an LLM such as ChatGPT, Google Gemini, etc. This study carefully evaluated and selected following prompts to apply in LLMs for URL detection:

<p align="center">
  <img src="https://github.com/hossiq/image/blob/main/Prompts.PNG?raw=true" alt="Feature Importance Plot" />
</p>




