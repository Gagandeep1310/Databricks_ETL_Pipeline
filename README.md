We have 3 assets for ETL pipelines in Databricks:
1.**Exploration**: We put the file with exploratory code here to understand raw data before building logic. It is mostly code.
       Examples include: display(df)
                         df.printSchema()
                         Null checks, distributions, basic stats

2. **Transformation:** Here comes the notebook with data clenaing and transformation logic. Converts raw data into clean/usable data. Code (core of pipleine) and not just data.
   Examples include: Handling missing values
                     Filtering rows
                     Creating new columns
                     Joins, aggregations

3. **Utility:** We put helper functions and reusable code here.
   For example: def clean_column_names(df):
                return df.toDF(*[c.lower().replace(" ", "_") for c in df.columns])
