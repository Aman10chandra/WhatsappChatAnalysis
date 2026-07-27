# 💬 WhatsApp Chat Analyzer

A modern, interactive **Streamlit web application** for analyzing WhatsApp chat exports. Gain insights into messaging patterns, user activity, timelines, most common words, and emoji usage for both individual and group chats.

---

## ✨ Features

- **📊 Top Statistics**: Quick metrics for total messages, total words spoken, media files shared, and external links shared.
- **📅 Timelines**:
  - **Monthly Timeline**: Visualize message volume trends month by month.
  - **Daily Timeline**: View daily chat activity over time.
- **🗺️ Activity Maps**:
  - **Most Busy Day**: Find out which day of the week sees the most messages.
  - **Most Busy Month**: Discover peak activity months.
  - **Weekly Activity Heatmap**: Hourly breakdown across days of the week.
- **👥 User Activity Analysis** *(Group Level)*: Identifies top contributors with frequency bar charts and percentage distributions.
- **☁️ WordCloud & Frequent Words**: Generates word clouds and bar charts of top words used, automatically filtering out common stop-words (supports Hinglish & English).
- **😊 Emoji Analysis**: Detailed breakdown and distribution of emojis used in conversations.

---

## 📁 Project Structure

```
.
├── app.py              # Main Streamlit UI application
├── helper.py           # Analytics logic, metrics calculation, and charts
├── preprocessor.py     # Data extraction, regex parsing, and date processing
├── stop_hinglish.txt   # Stop words dictionary for text filtering
├── requirements.txt    # Python package dependencies
├── setup.sh            # Setup script for deployment configuration
├── Procfile            # Process definition file for cloud deployment
└── README.md           # Project documentation
```

---

## 📲 How to Export WhatsApp Chat

To analyze a chat, you need to export your WhatsApp conversation as a `.txt` file:

1. Open the WhatsApp conversation (Individual or Group).
2. Tap the **More Options** menu (three dots on Android) or tap the Contact/Group Name (iOS).
3. Select **Export Chat**.
4. Choose **Without Media** for accurate text analysis.
5. Save or download the exported `.txt` file.

> **Note on Format**: The parser expects timestamps formatted as `DD/MM/YYYY, HH:MM - ` (e.g. `24/01/2023, 14:30 - User: Hello`).

---

## 🚀 Getting Started

### Prerequisites

- **Python 3.8+** installed on your system.

### Installation

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd WhatsappChatAnalysis
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

### Running Locally

Launch the Streamlit app with:

```bash
streamlit run app.py
```

The web app will open automatically in your browser at `http://localhost:8501`.

---

## 🛠️ Built With

- [Streamlit](https://streamlit.io/) - Web framework for data science apps
- [Pandas](https://pandas.pydata.org/) - Data manipulation and analysis
- [Matplotlib](https://matplotlib.org/) & [Seaborn](https://seaborn.pydata.org/) - Data visualization
- [WordCloud](https://github.com/amueller/word_cloud) - Text cloud visualization
- [URLExtract](https://github.com/lykos153/URLExtract) - URL pattern extraction
- [Emoji](https://github.com/carpedm20/emoji/) - Emoji processing

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
