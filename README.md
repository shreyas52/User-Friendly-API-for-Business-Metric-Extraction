# User-Friendly-API-for-Business-Metric-Extraction
LLM-powered application that takes user queries related to company performance metrics and converts them into a structured JSON format.



Requirements:
1. Use llama-3.1-8b-instant model from https://console.groq.com/

2. The application should be able to extract the following information from user queries:

    - Entity: The company name mentioned in the query (e.g., Flipkart, Amazon).

    - Parameter: The performance metric mentioned in the query (e.g., GMV, revenue, profit).

    - Start Date: The start date of the time period for which the metric is requested.

    - End Date: The end date of the time period for which the metric is requested.

3. If the user query does not explicitly mention the start date and/or end date, assume the following defaults:

    - Start Date: Today's date minus one year.

    - End Date: Today's date.

4. The extracted information should be converted into a JSON format with the following structure:

https://storage.tally.so/967f1bec-cbbe-45a9-b4a5-aa1b0d202b81/Screenshot-2024-05-02-at-6.23.10-PM.png
5. If the user query mentions multiple companies or requests a comparison, the JSON output should include multiple objects, one for each company mentioned.
6. The start date and end date should be converted to the ISO 8601 format (YYYY-MM-DD) before including them in the JSON output.
7. Use a combination of LLM calls and Python code to accomplish the task. The LLM can be used to understand the user query and extract relevant information, while Python can be used for data manipulation and JSON conversion.
