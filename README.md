# cloudtechnology
from pytrends.request import TrendReq  
pytrends = TrendReq()  
pytrends.build_payload(["data science", "machine learning"], timeframe='2020-01-01 2025-01-01', geo='US')  
data = pytrends.interest_over_time()  


plt.figure(figsize=(12,6))  
sns.lineplot(data=data)  
plt.title("Google Search Trends Over Time")  
plt.xlabel("Date")  
plt.ylabel("Search Interest")  
plt.legend(data.columns)  
plt.show()  


