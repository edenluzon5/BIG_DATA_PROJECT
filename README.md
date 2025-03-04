# Analyzing Discourse on Israel and Judaism across Reddit Communities

## Overview
This project analyzes discussions across four Reddit communities focused on Israel and Judaism, using a combination of **topic modeling, named entity recognition (NER), sentiment analysis, and network analysis**. The analysis covers **October 2023 to November 2024** and focuses on **r/Israel**, **r/Jewish**, **r/Judaism**, and **r/ReformJews**, exploring how online discourse reflects **identity, political polarization, historical memory, and responses to real-world events**.

---

## Research Objectives
- Identify **main topics** discussed in each subreddit.
- Detect **key entities** (people, places, events) shaping conversations.
- Track **sentiment trends** over time and across events.
- Identify **leading users** who drive conversations and measure their influence.
- Analyze how real-world events impact **online sentiment and activity**.

---

## Methodology
### Topic Modeling (LDA)
- Applied **Latent Dirichlet Allocation (LDA)** to uncover core topics in posts.
- Topics were selected based on **coherence scores**, resulting in **8 main topics**.
- Comments were classified into these topics to capture **full conversation context**.

### Named Entity Recognition (NER)
- Used **spaCy** to extract and classify entities into:
    - **GPE** (Countries/Regions)
    - **PERSON** (Individuals)
    - **ORG** (Organizations)
    - **DATE** (Dates/Holidays)
    - **EVENT** (Wars/Protests)
- Built **entity co-occurrence networks** to reveal connections between key actors and events.

### Sentiment & Temporal Analysis
- Computed daily sentiment using **VADER**, optimized for social media text.
- Created time series of **post volume** and **average sentiment**.
- Identified extreme dates with sharp sentiment drops or posting spikes.
- For these dates, applied **BERTopic** to detect **event-specific topics**.

### Leadership & Network Analysis
- Calculated a **leadership score** per user, based on:
    - Posts, Comments, Upvotes, Replies.
- Built a **reply network** showing how top users interact.
- Measured **polarization** using "we/they" language and combined this with **average sentiment** to understand user roles.

---

## Key Findings
- Discussions are dominated by **conflict, religious identity, antisemitism, and global crises**.
- Events like **October 7** and the **Iran-Israel missile exchange** caused sentiment crashes and posting surges.
- Top users split into two profiles: **polarized political influencers** and **cultural/religious community builders**.
- Entity networks show tightly connected clusters linking **Israel, Hamas, Biden, and Iran**, highlighting **geopolitical focus**.
- Historical events like **World War II** regularly appear, showing that **historical framing** shapes modern discourse.
- The **Jewish** subreddit peaked on **May 1, 2024**, due to **real-world antisemitic incidents**, showing how **offline crises directly impact online discourse**.

---

## Tools & Technologies
- ## Data Source
The data was collected using Reddit's API, with subreddit selection inspired by the resource provided in:  
[arctic_shift - download_links.md](https://github.com/ArthurHeitmann/arctic_shift/blob/master/download_links.md).
- NLP: **spaCy**, **VADER**, **BERTopic**, **pyLDAvis**
- Visualization: **matplotlib**, **seaborn**, **NetworkX**, **folium**
- Analysis: **pandas**, **numpy**, **scikit-learn**

---
