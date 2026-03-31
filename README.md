# WeRateDogs Twitter Contest Project

**Data Analyst Project** – Wrangled, cleaned, and analyzed WeRateDogs Twitter contest data to uncover breed popularity trends and support shelter-adoption awareness.

**Business Problem**  
The WeRateDogs contest on Twitter aimed to raise awareness about shelter dogs in the US (≈1.1 million dogs enter shelters annually but do not get adopted). The goal was to highlight popular breeds and top-scoring dogs to encourage potential pet parents to adopt.

**What I Did**  
- Gathered data from three sources:  
  1. Twitter archive CSV (`twitter-archive-enhanced.csv`)  
  2. Udacity-hosted image-prediction TSV (downloaded with Requests)  
  3. Twitter API via Tweepy (JSON data saved to TXT)  
- Imported all files into Pandas DataFrames.  
- Assessed for quality and tidiness issues (9 quality + 2 tidiness).  
- Completed cleaning (made a copy of the data first):  
  - Merged CSV and TSV on tweet_id (resolved tidiness issue and kept only tweets with pictures).  
  - Removed retweets (filtered rows with retweeted_status_id).  
  - Removed non-dog entries (kept only rows where at least one of p1_dog, p2_dog, p3_dog was True).  
  - Updated incomplete/“None” dog names to NaN.  
  - Standardized breed columns (p1, p2, p3) to lowercase.  
  - Converted p1_dog, p2_dog, p3_dog columns from float back to bool.  
  - Changed ID columns (status_id, tweet_id, user_id) from int to string.  
  - Dropped extraneous columns (doggo, floofer, pupper, puppo).  
- Saved the cleaned dataset as `twitter_archive_master.csv`.

**Key Findings & Insights**  
1. Top 5 most commonly entered breeds: golden_retriever (267), labrador_retriever (267), chihuahua (179), pembroke (139), cardigan (112).  
2. Top 5 highest-scoring dog breeds:  
   1. Pomeranian / Chow  
   2. Golden Retriever / Tibetan Mastiff / Labrador Retriever  
   3. Clumber / Cocker Spaniel / Lhasa  
   4. Kuvasz / Samoyed / Great Pyrenees  
   5. Lakeland Terrier / Airedale  
3. Lowest-rated breeds also identified (mixes including border collie, great dane, etc.) to highlight under-appreciated dogs.  

**Visualization**  
Bar chart showing the top 5 most commonly entered breeds (included in notebook and final report).

**Project Deliverables** (all files in this repo)  
- `wrangle_act.md` – full Jupyter notebook with code, cleaning steps, analysis, and visualization  
- `wrangle_report.pdf` – detailed wrangling and cleaning process  
- `act_report.pdf` – final analysis, breed rankings, and bar chart  

**Tools Used**  
Python, Pandas, Requests, Tweepy, Matplotlib

**How to Explore**  
Open `wrangle_act.md` (or the original .ipynb if you still have it) to see every step from gathering through visualization.

See this project in my main portfolio: https://github.com/AutumnsData/autumns.portfolio
