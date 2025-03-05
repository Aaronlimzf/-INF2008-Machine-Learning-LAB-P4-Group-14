# Smart Waste Classification System for Recycling

## Description
The **Smart Waste Classification System** is designed to identify and categorize waste items to determine their recyclability. With increasing waste production, proper waste segregation plays a crucial role in environmental sustainability. This project leverages data-driven classification techniques to improve recycling efforts by accurately distinguishing between different types of waste.

The system classifies waste into six categories:
- **Cardboard** – Used for packaging materials, boxes, and cartons.
- **Glass** – Includes glass bottles, jars, and broken glassware.
- **Metal** – Comprises aluminum cans, tin containers, and metallic scraps.
- **Non-recyclable Waste** – Items that cannot be processed for recycling.
- **Paper** – Newspapers, magazines, office paper, and paperboard.
- **Plastic** – Includes PET bottles, food containers, and plastic packaging.

To achieve high classification accuracy, the project utilizes three machine learning algorithms:
- **Multi-Layer Perceptron (MLP)**
- **Random Forest (RF)**
- **Support Vector Machine (SVM)**  

The system helps users determine whether a waste item is recyclable or not by analyzing images and providing instant feedback. By integrating machine learning and a Telegram bot, it simplifies waste sorting and encourages proper disposal habits, making recycling more accessible and convenient.

---

## Problem Statement
Singapore generates approximately **7.39 million tonnes of waste annually**, yet only **57% is recycled** as of 2022 [(NEA, 2023)](https://www.nea.gov.sg/media/news/news/index/waste-generation-and-recycling-rates-increased-in-2022-as-economic-activity-picked-up). One of the main issues is **improper waste segregation**, where recyclable materials end up in general waste due to human error and lack of awareness.

A major contributor to this problem is the difficulty in **identifying recyclables** at the point of disposal. A 2018 report by the Singapore Environment Council found that **nearly 70% of Singapore residents** lack sufficient knowledge about which plastics can be recycled. Given that plastics are one of the most common waste types, this high percentage suggests that many individuals may also **struggle with identifying recyclability across other materials**, leading to improper waste disposal [(Westford Online, 2023)](https://www.westfordonline.com/blogs/singapores-plastic-predicament-unravelling-the-environmental-challenge/). Contaminated recyclables reduce processing efficiency and increase waste sent to **Semakau Landfill**, which is projected to reach full capacity by **2035** [(Channel News Asia (2024))](https://www.channelnewsasia.com/singapore/semakau-landfill-filling-waste-management-incineration-reduce-reuse-recycle-3909436).

To address this issue, our project introduces a **waste classification system integrated with a Telegram bot**. This allows users to **take a picture of their waste item**, receive an instant classification result, and get guidance on **proper disposal methods**.



---

## Telegram Bot Integration
To make the waste classification system more **accessible and user-friendly**, we integrate it with a **Telegram bot**. Users can **send a photo of a waste item**, and the bot will return:
1. **Predicted Waste Category** (e.g., Plastic, Metal, Cardboard, etc.).
2. **Recyclability Status** – Whether the item should go into the blue recycling bin or general waste.


This approach ensures:
- **Convenience** – Users can access the system anytime via their smartphone.
- **Immediate Feedback** – Reduces uncertainty about what can be recycled.
- **Better Waste Segregation** – Increases correct recycling practices and reduces contamination.

**Example Usage:**
1. User sends a **photo** of a plastic bottle to the Telegram bot.
2. The bot processes the image using the trained **ML model**.
3. The bot replies with:
4. If an item is **non-recyclable**, the bot provides alternative disposal options.

---

## Project Workflow
1. **Image Collection & Preprocessing**
- Waste images were sourced from **Kaggle datasets**.
- Images were resized, normalized, and converted into feature vectors using **VGG16**.

2. **Model Training**
- The dataset was split into **training (80%)** and **testing (20%)** sets.
- Three machine learning models (**MLP, RF, SVM**) were trained for classification.

3. **Model Evaluation**
- The models were tested using **accuracy, precision, recall, and confusion matrix**.
- The best-performing model was selected for deployment.

4. **Telegram Bot Deployment**
- A Python-based bot was developed using **TeleBot (python-telegram-bot library)**.
- The bot is hosted on a server and connected to the trained model.
- Users can interact with the bot via Telegram by sending waste images.

---

## Expected Impact
By implementing this **Telegram waste classification system**, we aim to:

✔ **Reduce improper waste disposal** and improve **recycling accuracy**.  
✔ Provide a **convenient tool** for Singapore residents to make **informed recycling decisions**.  
✔ Support Singapore’s **Green Plan 2030** and **Zero Waste Masterplan** by promoting sustainability.  

This project bridges **technology and environmental conservation**, empowering individuals to contribute to a **greener future** effortlessly.  

---

## References
1. **National Environment Agency (NEA) - Waste Statistics and Recycling Rates (2023)**  
   🔗 [https://www.nea.gov.sg/media/news/news/index/waste-generation-and-recycling-rates-increased-in-2022-as-economic-activity-picked-up](https://www.nea.gov.sg/media/news/news/index/waste-generation-and-recycling-rates-increased-in-2022-as-economic-activity-picked-up)  
   
2. **Channel News Asia (2024) - Semakau Landfill Reaching Capacity & Waste Management Efforts**  
   🔗 [https://www.channelnewsasia.com/singapore/semakau-landfill-filling-waste-management-incineration-reduce-reuse-recycle-3909436](https://www.channelnewsasia.com/singapore/semakau-landfill-filling-waste-management-incineration-reduce-reuse-recycle-3909436)  

3. **SG Green Plan 2030 - Sustainable Waste Management**  
   🔗 [https://www.greenplan.gov.sg/](https://www.greenplan.gov.sg/)  

4. **Westford Online (2023) - Singapore’s Plastic Recycling Challenge**  
   🔗 [https://www.westfordonline.com/blogs/singapores-plastic-predicament-unravelling-the-environmental-challenge/](https://www.westfordonline.com/blogs/singapores-plastic-predicament-unravelling-the-environmental-challenge/)  


---

## License
This project is licensed under the **MIT License**.
