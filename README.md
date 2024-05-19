# Prompt-Engineering-using-LLMs
Phishing URL Detection with Prompt Engineering using Large Language Models

**Background**

Phishing attacks are a form of social engineering where attackers attempt to deceive victims into revealing sensitive information or clicking on malicious links and it remains a persistent threat in the digital landscape, causing significant financial losses and data breaches. Phishing has become increasingly sophisticated, making it challenging to distinguish legitimate URLs from fraudulent ones.
Recently, Large Language Models (LLMs) have been making significant impacts on various tasks including Machine Learning(ML) application development. These models are notable due to the use of vast amount of training datasets from diverse fields that the models are trained; and demonstrating impressive adaptability and performance across industries and regular human life.

**Objective**

This project aim to assess whether LLMs can provide a more efficient yet effective alternative to detect phishing URLs.
A new technique called prompt engineering which involves crafting specific input prompts to guide the LLM toward desired outputs without modifying the model itself can be utilized to detect phishing.

**Methodology**

> **Data Collection**
       
       The phishing dataset is collected from Mendeley Data (https://data.mendeley.com/datasets/c2gw7fy2j4/3) which has a total of 11,430 URL samples, and each URL is accompanied by 88 extracted features including a status column to classify the URLs. This project randomly selected 100 URLs with balanced classification, comprising 50 legitimate and 50 phishing URLs. A python script is used to randomly sample the dataset.

      
> **Prompt Engineering**
      Prompt engineering refers to the process of carefully crafting prompts to elicit desired responses from an LLM such as ChatGPT, Google Gemini, etc. This study carefully evaluated and selected following prompts to apply in LLMs for URL detection:
Role playing prompt: Act as a cybersecurity analyst tasked with identifying phishing attempts from a list of URLs. Analyze each of the following URL and determine if it's likely phishing (phishing) or a legitimate website (legitimate)
Zero shot prompt: Determine if the following URL is likely phishing or legitimate
One shot prompt: Classify following URL as phishing or legitimate . An example of legitimate URL is http://www.thefreedictionary.com/portal
Few shot prompt: Here are some examples of URLs and whether they are legitimate or phishing: 1. legitimate: http://www.dictionary.com/browse/commander 2.phishing:http://onager.co.kr/wp-admin/excel2/index.php 3. legitimate: https://www.ideo.com/jobs 4. phishing: https://ecb9547832.nxcli.net/assest/EX/adobe/index.php?email=ruby.jiang@bicworld.com . Are the following URL legitimate or phishing?
Chain of Thoughts (CoT) prompt: Determine if the following URL's are phishing or legitimate by acting as a thorough analyst. Follow a structured approach, starting with subdomain analysis to identify generic terms, hyphens, or underscores that might indicate phishing. Next, verify the domain name matches the purported organization and ensure the top-level domain aligns with the content. Inspect the URL for unusual characters, typos, or suspicious patterns, and then search the web for information about the URL and organization to assess their reputation and context. Cross-check the URL's characteristics with known phishing patterns and indicators of compromise, and finally, provide a clear justification for your conclusion on whether the URL is likely phishing or legitimate.




