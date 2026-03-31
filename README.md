# WeRateDogs Twitter Contest Project

**Data Analyst Project** – Cleaned and analyzed WeRateDogs Twitter contest data to uncover breed popularity trends and support shelter-adoption awareness.

**Business Problem**  
The WeRateDogs contest on Twitter aimed to raise awareness about shelter dogs in the US (≈1.1 million dogs enter shelters annually but do not get adopted). The goal was to highlight popular breeds and top-scoring dogs to encourage potential pet parents to adopt.

**What I Did**  
- Gathered data from three sources: Twitter archive CSV, Udacity-hosted image-prediction TSV (using Requests), and Twitter API via Tweepy (JSON data saved to TXT).  
- Imported all files into Pandas DataFrames.  
- Performed visual and programmatic assessment, identifying issues across multiple tables.  
- Completed 8 targeted cleaning tasks (project limited to these for focus):  
  - Merged CSV and TSV tables (resolved tidiness issue and removed tweets without pictures).  
  - Removed retweets (filtered out any rows with retweeted_status_id).  
  - Removed non-dog entries (kept only rows where at least one of p1_dog, p2_dog, or p3_dog was True).  
  - Updated incomplete/“None” dog names to proper NaN values.  
  - Standardized breed columns (p1, p2, p3) to lowercase.  
  - Converted bool columns (p1_dog, p2_dog, p3_dog) from float back to bool.  
  - Changed ID columns (status_id, tweet_id, user_id) from int to string.  
  - Dropped extraneous columns (doggo, floofer, pupper, puppo).  
- Saved the cleaned dataset as `twitter_archive_master.csv`.

**Key Findings & Insights**  
- Top 5 most commonly entered breeds: Labrador Retriever, Golden Retriever, Chihuahua, Pembroke (Corgi), Cardigan (Corgi).  
- Top 5 highest-scoring dog breeds:  
  1. Pomeranian / Chow  
  2. Golden Retriever / Tibetan Mastiff / Labrador Retriever  
  3. Clumber / Cocker Spaniel / Lhasa  
  4. Kuvasz / Samoyed / Great Pyrenees  
  5. Lakeland Terrier / Airedale  
- Lowest-rated breeds also identified (mixes including border collie, great dane, etc.) to highlight under-appreciated dogs.  
- Created bar chart visualizing the top 5 most common breeds (included in final report).

**Project Deliverables** (view the PDFs in this repo)  
- `wrangle_report.pdf` – full data-gathering and 8-step cleaning process  
- `act_report.pdf` – final analysis, breed rankings, and bar chart  

**Tools Used**  
Python, Pandas, Tweepy, Requests, Jupyter Notebook

**How to Explore**  
1. Download the two PDFs directly from this repo.  
2. See the complete process and final visualizations I delivered for the contest analysis.

See this project in my main portfolio: https://github.com/AutumnsData/autumns.portfolio
