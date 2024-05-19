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


Prompt engineering is applied to the Large Language Models, specifically Gemini, GPT-3.5, and GPT-4, to perform the task of classification. Google’s Gemini a multimodal custom LLM designed for efficiency and built upon the foundation of Google's PaLM 2 model. ChatGPT3.5 is based on OpenAI's proprietary generative pre-trained transformer (GPT) model family, specifically GPT-3.5 and ChatGPT4 is based on the GPT-4 architecture which is a further development of GPT model.

The performance evaluation for each prompt in LLMs is crucial to understand model strength of detecting phishing. As the goal of this study is to classify whether URL is phishing or legitimate, the performance metrics that are calculated:
Accuracy which is the ratio of correctly predicted URL to the total URLs, Precision is the ratio of correctly predicted positive observations which is correctly identified phishing URLs to the total predicted phishing observations, Recall is defined as the ratio of correctly predicted positive observations to all actual positives, referred as sensitivity, and F1 score that provides balanced view of performance as it considers both false positives and false negatives


**Results**

The output of each prompt technique shows that Zero shot-Gemini (49 legitimate and 51 phishing) shows similar count as ‘Actual Status’ (50 legitimate and 50 phishing).Other similar count by classification shows by Zero Shot-ChatGPT3.5 (52 legitimate and 48 phishing), and Role Play-Gemini (54 legitimate and 46 phishing) prompt. The major count differences shows by One shot ChatGPT-4 method with 67 legitimate and only 33 phishing followed by Role play and Zero shot ChatGPT-4 with 65 legitimate and 35 phishing.

<p align="center">
  <img src="https://github.com/hossiq/image/blob/main/Data Count By LLM.png?raw=true" alt="Feature Importance Plot" />
</p>

The count of how many is detected in each classification is not alone a suitable metric to conclude which technique is better.

Following results show that ZeroShot-ChatGPT3.5 outperforming all other methods, achieving the highest accuracy and F1 score at 96%, indicating exceptional overall effectiveness in detecting phishing URLs. One Shot and Zero Shot-ChatGPT4 resulted in the lowest precision across all LLMs, indicating a tendency to misclassify some legitimate URLs as phishing.

<p align="center">
  <img src="https://github.com/hossiq/image/blob/main/Eval_Metrics_PromptEngineering_LLMS.PNG?raw=true" alt="Feature Importance Plot" />
</p>

Similar performance is shown in the following radar plot that ChatGPT3.5-based methods tend to form larger areas within the chart, indicating their overall stronger performance in URL classification tasks when compared to the methods based on other LLMs.

<p align="center">
  <img src="https://github.com/hossiq/image/blob/main/Radar Plot Metrics.png?raw=true" alt="Feature Importance Plot" />
</p>

The performance for prompt techniques across all LLM’s outlined that Chain of Thought(CoT) is the best to detect URL’s classification with 86% accuracy and 87% F1 score followed by One shot technique with 86% F1 score.

<p align="center">
  <img src="https://github.com/hossiq/image/blob/main/Eval_Metrics_PromptEngineeringS.PNG?raw=true" alt="Feature Importance Plot" />
</p>

The lowest precision is shown in Few shot prompting (77%) suggesting it might misclassify some legitimate URLs as phishing while CoT and Zero shot method provided highest precision of 81%. Role-playing and One-Shot prompting achieved a balance between accuracy and
precision, both scoring around 84% and 80% respectively. The lowest recall by Zero shot signifies that it might potentially missing some phishing attempts.

Following table shows the performance of various Large Language Models (LLMs) in detecting phishing URLs using different prompt methods and ChatGPT3.5 has the best ability to classify URL’s with the score of 90% and 91% for accuracy and F1, respectively. Also, ChatGPT3.5 shows near perfect recall performance with 98% score shows the confidence to not to misclassify phishing URLs, effectively identifies both phishing and legitimate URLs.

<p align="center">
  <img src="https://github.com/hossiq/image/blob/main/LLMS performance.PNG?raw=true" alt="Feature Importance Plot" />
</p>

While both ChatGPT4 and Gemini achieved similar accuracy (81%), their precision falls short (75% and 78% respectively), suggesting they might misclassify some legitimate URLs as phishing attempts compared to ChatGPT 3.5 (86% precision). Gemini has the lowest recall
(86%) among other models, potentially missing a higher proportion of phishing URLs from the dataset.

The aggregated results for all prompts and models highlight the average accuracy for detecting phishing URLs 84%, demonstrating a good overall ability to identify phishing attempts. However, the average precision of 80% indicates some models might misclassify legitimate URLs as phishing.

<p align="center">
  <img src="https://github.com/hossiq/image/blob/main/Overall Metrics.PNG?raw=true" alt="Feature Importance Plot" />
</p>


**Conclusion**

This study explored the potential of prompt engineering to enhance Large Language Model (LLM) based phishing URL detection. The report considered a dataset with 50 ‘phishing’ and 50 ‘legitimate’ URL’s and five different prompt engineering techniques namely Zero-Shot, One-Shot, Few-Shot, Chain of Thoughts (CoT), and Role-Playing utilizing three LLM models ChatGPT 3.5, ChatGPT 4, and Gemini. Zero Shot-ChatGPT3.5 performed the best across all evaluation metrics with top F1 scores of 96% ,while Zero Shot-Gemini had the lowest performance with the lowest F1 Score of 77%. ChatGPT3.5 performed the best across all evaluation metrics with top f1 scores of 91% in all techniques while Gemini shows the lowest performance of 82% f1 score. Chain-of-Thoughts (CoT) method shows best performances combining all LLM’s with 86% accuracy while Few Shot accuracy is the lowest with 81%. The overall performance of various Large Language Models in detecting phishing URLs, averaged across all prompt techniques, demonstrates a solid Accuracy of 84%, Precision of 80%, high Recall of 92%, and an F1 Score of 85%, indicating that these models are effective at identifying legitimate URLs while maintaining a good balance between precision and recall.



**References**

Lee, P., Bubeck, S. & Petro, J. Benefits, Limits, and Risks of GPT-4 as an AI Chatbot for Medicine. N. Engl. J. Med. 388, 1233–1239 (2023).
Fouad T; Ali C; Prompt Engineering or Fine-Tuning? A Case Study on Phishing Detection with Large Language Models. Mach. Learn. Knowl. Extr. 2024, 6(1), 367-384; https://doi.org/10.3390/make6010018
OpenAI. (2023). GPT-4: Scaling Language Models through Prompt Engineering. OpenAI Blog. https://cdn.openai.com/papers/gpt-4.pdf
Li Wang, Xi Chen, XiangWen Deng, Hao Wen, MingKe You, WeiZhi Liu, Qi Li , Jian Li (2024). Prompt engineering in consistency and reliability with the evidence-

