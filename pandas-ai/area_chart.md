```
import pandas as pd
from pandasai import PandasAI
from pandasai.llm.openai import OpenAI

df = pd.DataFrame({
    "country": ["United States", "United Kingdom", "France", "Germany", "Italy", "Spain", "Canada", "Australia",
                "Japan", "China"],
    "area": [9826675, 242500, 551695, 357022, 301340, 505990, 9984670, 7692024, 377915, 9596961],

})

OPENAI_API_KEY = "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"
llm = OpenAI(api_token=OPENAI_API_KEY)

pandas_ai = PandasAI(llm)

output = pandas_ai.run(df,
                       prompt='Analysis these data with a  chart in ascending order '
                              'and different country different color'
                              'more precise data for the vertical axis'
                       )
print(output)
```
![image](https://github.com/tour987/Python-for-Data-Analysis/assets/107463642/85192d47-2bb5-4078-983c-ba4643433d6e)
