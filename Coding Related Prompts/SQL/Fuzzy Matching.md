**Environment Context (Fuzzy Matching SQL)**

*   **Business Use Case:** [What is the reason you need to perform a fuzzy match? e.g., data cleaning, product matching, address verification, name matching, etc.]
*   **SQL Flavor:** [Specify your SQL environment. This is crucial as fuzzy matching functions and syntax can vary significantly. e.g., MySQL, PostgreSQL, SQL Server, Oracle, etc.]
*   **Fuzzy Match Goal:** [What are you trying to achieve with the fuzzy match? e.g., find similar product names, identify potentially duplicate customer records, correct misspelled addresses, etc.]

**Query Creation Workflow (Fuzzy Matching)**

**Cycle Overview**

**1. Start Phase: Defining the Fuzzy Match Problem**

*   **Describe the data you are working with and what you want to fuzzy match.**  For example: "I have a table of product names and I want to find products that are similar to 'Apple iPhone 13' even if there are slight variations in spelling or wording."
*   **Engage with clarifying questions to understand the specifics of the fuzzy match:**
    *   **Which columns are involved in the fuzzy match?** (e.g., "product_name" column in "products" table, "customer_address" column in "customers" table).
    *   **What type of fuzzy match are you looking for?** (e.g.,  similarity in spelling, phonetic similarity, approximate matching based on keywords, etc.)
    *   **What is your tolerance for "fuzziness"?** (e.g., how many differences are acceptable to consider a match? Do you need to rank results by similarity?)
    *   **Do you have example values for the column you want to match, and what are some examples of values that should be considered a "fuzzy match"?** (This is very helpful to understand the nuances of your data.)
    *   **What is the desired output?** (e.g.,  return all rows that are fuzzy matches to a specific value, find pairs of rows that are fuzzy matches of each other, etc.)

**2. Refining Phase: Exploring Fuzzy Matching Techniques and Functions**

*   **Based on your SQL Flavor and the type of fuzzy match you need, we'll explore relevant SQL functions and techniques.**  This might include:
    *   **`LIKE` operator with wildcards (`%`, `_`):** For basic pattern matching.
    *   **`SOUNDEX` or `DIFFERENCE` functions:** For phonetic matching (available in some SQL dialects).
    *   **`LEVENSHTEIN DISTANCE` or similar string distance functions:** To calculate the edit distance between strings (often requires extensions or user-defined functions in some SQL flavors).
    *   **Full-Text Search capabilities:** If your SQL environment supports it, this can be very powerful for keyword-based fuzzy matching.
    *   **Trigram or N-gram similarity:**  More advanced techniques, sometimes available as extensions or custom functions.

*   **Suggest potential SQL functions or techniques that are suitable for your use case and SQL Flavor.**
*   **Request more information or examples if needed to choose the best approach.**  For example, if you mention "similar product names," we might ask for examples of product names and what you consider "similar" to help choose the right fuzzy matching method.

**3. Creating the Fuzzy Match Query**

*   **Upon receiving the prompt "QUERY" from you:**
    *   Construct the SQL query using the chosen fuzzy matching technique and the information gathered.
    *   Adhere to the specified SQL flavor and syntax.
    *   If necessary, provide example queries using different techniques if there are multiple options or if the best approach is unclear.
    *   Present the query to you for execution and testing.

**Useful Information (Fuzzy Matching in SQL)**

*   **Fuzzy matching is not an exact science.** The "best" approach often depends on the specific data, the desired level of accuracy, and performance requirements.
*   **Performance can be a concern with fuzzy matching, especially on large datasets.**  Some techniques are more computationally expensive than others.
*   **Thresholds and parameters are often needed** to control the level of fuzziness.  For example, with Levenshtein distance, you might need to decide on a maximum distance to consider as a match.
*   **SQL Flavor matters greatly.**  Functions and syntax for fuzzy matching vary significantly across different database systems.

**Available "Tables" (for Fuzzy Matching - Metaphorical)**

*   **Your Data Tables:** The actual tables containing the data you want to fuzzy match. Please describe these tables and the relevant columns as we proceed.
*   **SQL Documentation for your Flavor:** We'll be referencing this to find available fuzzy matching functions.
*   **Example Data:** Providing example data is extremely helpful for testing and refining the fuzzy match query.

**Notes (Fuzzy Matching)**

*   We will focus on finding a balance between accuracy, performance, and complexity of the SQL query.
*   We may need to iterate and try different approaches to find the best fuzzy match solution for your specific needs.

**Okay, please provide the "Environment Context" for your fuzzy match query and describe the data and problem you are trying to solve. Let's start building your fuzzy matching SQL!**