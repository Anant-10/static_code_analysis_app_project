Welcome to the Static Code Analysis App! This application allows you to analyze your code for various static code analysis metrics, visualize reserved words and identifiers, and explore the abstract syntax tree (AST) of your code.
![App Screenshot]()


Features
Code Analysis: Analyze raw static code analysis metrics such as maintainability index, cyclomatic complexity, and Halstead metrics.
Visualization of Reserved Words and Identifiers: Generate bar charts, word clouds, and pie charts for reserved words and identifiers in your code.
Abstract Syntax Tree (AST) Analysis: View the AST of your code in JSON format.

Requirements
Python 3.6 or higher
Streamlit
Radon
WordCloud
Matplotlib
Altair
Plotly
Pandas

### Explanation of the Code

The `Static Code Analysis App` is built using Streamlit and Radon for analyzing and visualizing various static code metrics. Here is a brief explanation of the code:

1. Import Necessary Packages:
   - `streamlit`: For creating the web application.
   - `radon`: For static code analysis metrics.
   - `app_utils`: Custom utility functions for the application.
   - `wordcloud`: For generating word clouds.
   - `matplotlib`, `altair`, `plotly.express`: For data visualization.
   - `pandas`: For handling data in DataFrame format.

2. Utility Functions:
   - `convert_to_df(mydict)`: Converts a dictionary to a pandas DataFrame for easier handling and visualization.
   - `plot_wordcloud(docx)`: Generates and displays a word cloud from the given text.

3. Main Function (`main()`):
   - Sets the title of the Streamlit app.
   - Creates a form to input the code for analysis.
   - Defines tabs for different types of analysis: Code Analysis, Reserved Words, Identifiers, and AST (Abstract Syntax Tree).

4. Code Analysis Tab:
   - Displays the original code.
   - Shows raw static code analysis metrics like maintainability index, cyclomatic complexity, and Halstead metrics.
   - Uses Radon to calculate these metrics and displays them in a structured format.

5. Reserved Words Tab:
   - Converts the frequency of reserved words in the code to a DataFrame.
   - Visualizes the reserved words using Altair bar charts, word clouds, and Plotly pie charts.

6. Identifiers Tab:
   - Similar to the Reserved Words tab, but focuses on identifiers in the code.
   - Uses Altair for bar charts and word clouds for visualization.

7. AST Tab:
   - Parses the code to generate its Abstract Syntax Tree (AST).
   - Displays the AST in JSON format for better readability and understanding of the code structure.

8. Execution:
   - The `main()` function is called when the script is executed, running the Streamlit app and displaying the user interface for code analysis.

This application provides a comprehensive set of tools for analyzing static code metrics, visualizing key elements like reserved words and identifiers, and understanding the structure of the code through its AST.
