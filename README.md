{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "7739eb75-05ab-43e5-81e3-ea287dfa0513",
   "metadata": {},
   "source": [
    "# 🧮 __Customer Churn Analysis__"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "2a023a17-0b30-487c-871e-c27a6996407a",
   "metadata": {},
   "source": [
    " \n",
    " Understanding why customers leave and identifying retention strategies using data-driven insights.\n"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "b7d523f1-6b8f-4926-9f6e-259f5f72d29b",
   "metadata": {},
   "source": [
    "## 📑 Table of contents"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "13cf5a1c-35d4-4fc7-bdaa-fcc82ae48504",
   "metadata": {},
   "source": [
    "- [Overview](#overview)\n",
    "- [Business Problem](#business-problem)\n",
    "- [Dataset](#dataset)\n",
    "- [Key Features](#key-features)\n",
    "- [Dashboard](#dashboard)\n",
    "- [Tools and Libraries](#tools-and-libraries)\n",
    "- [Project structure](#project-structure)\n",
    "- [How to run the project](#how-to-run-the-project)\n",
    "- [Final Recommendations](#final-recommendations)\n",
    "- [Authors and contacts](#author--contacts)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "0a63c3e0-6218-4a92-a809-b07f8aed2ad1",
   "metadata": {},
   "source": [
    "### 📋Overview"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "4e722a27-dc9d-4be9-8fcd-74d337ccffd1",
   "metadata": {},
   "source": [
    "This project analyzes customer churn behavior in a retail bank.  \n",
    "By exploring patterns across demographics, account details, and engagement metrics,  \n",
    "the goal is to identify key drivers of churn and propose actionable strategies to improve retention.\n"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "a8deec79-42bb-4ac7-b816-89b374577c1e",
   "metadata": {},
   "source": [
    "### 💼 Business Problem\n",
    "- What is the overall churn rate, and how does it trend over time.\n",
    "- How does churn vary by geography (France, Germany, Spain)?\n",
    "- What are the differences in churn rates between male and female customers?\n",
    "- What is the churn rate distribution across different age groups?\n",
    "- How does churn behavior change with tenure?\n",
    "- What percentage of high-balance customers (e.g., >$100K) have churned?\n",
    "- How do churn rates compare across different NumOfProducts?\n",
    "- Are inactive members (IsActiveMember = 0) more likely to churn?\n",
    "- Can we build a KPI dashboard to track churn metrics like average salary,balance, and active users?\n",
    "- What does a customer persona dashboard (churned vs. retained) look like?"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "6eec78ab-d185-43b1-8ec9-c0439c768a1e",
   "metadata": {},
   "source": [
    "### 🗂️ Dataset"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "523dbec6-0b20-4a7f-9490-cbf557987ee6",
   "metadata": {},
   "source": [
    "The dataset used for this analysis is available in the repository. It contains customer information such as demographics, account balance, credit score, and churn status, which are used to explore behavioral patterns and identify churn factors.\n",
    "\n",
    "[Customer-Churn-Records.csv](./customer-churn-record.csv)\n",
    "\n"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "a42c6426-addf-442d-b65e-dbbfb7f0ad94",
   "metadata": {},
   "source": [
    "### 🚀 Key Insights\n",
    "- Middle-aged customers show a higher churn tendency.  \n",
    "- Inactive members and single-product users are more likely to leave.  \n",
    "- High balance but low credit score customers have an elevated churn risk.  \n",
    "- Regional and gender-based variations indicate targeted retention opportunities.\n"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "818575a6-f5f9-4941-ac1e-6b1e0cc73dab",
   "metadata": {},
   "source": [
    "### 🖼️ Dashboard\n",
    "[![Dashboard](dashboard.png)](dashboard.png)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "2eda45f8-2043-4fd5-af9d-ea945228813a",
   "metadata": {},
   "source": [
    "### 🛠️ Tools and Libraries\n",
    "- Python (Pandas, Matplotlib, Seaborn, plotly)\n",
    "- Power BI (Interactive Visualizations)\n",
    "- GitHub"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "50f15765-98f0-4972-8c7e-3d587f1b392a",
   "metadata": {},
   "source": [
    "### 🗂️ Project structure\n",
    "```\n",
    "Customer-Churn-Analysis/\n",
    "│\n",
    "├── 📄 README.md # Project overview and documentation\n",
    "├── 📊 dataset/\n",
    "│ └── Customer-Churn-Records.csv # Dataset used for churn analysis\n",
    "│\n",
    "├── 📓 notebooks/\n",
    "│ └── Customer_Churn_Analysis.ipynb # Jupyter Notebook with data cleaning, EDA, and insights\n",
    "│\n",
    "├── 🖼️ reports/\n",
    "│ └── dashboard.png # Dashboard or visual summary of churn insights\n",
    "│\n",
    "├── 💻 dashboard/\n",
    "│ └── app.py # Interactive dashboard using Dash / Streamlit\n",
    "│\n",
    "└── requirements.txt # List of required Python libraries\n",
    "```"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "b6db3098-463e-4102-88b9-3422801b7a41",
   "metadata": {},
   "source": [
    "\n",
    "---\n",
    "\n",
    "### ⚙️ How to Run the Project\n",
    "\n",
    "Follow these steps to run the analysis or dashboard locally:\n",
    "\n",
    "1. **Clone the repository**\n",
    "   ```bash\n",
    "   git clone https://github.com/your-username/Customer-Churn-Analysis.git\n",
    "   cd Customer-Churn-Analysis\n"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "312f7183-9285-4ea3-8e92-b3f00d8fcb37",
   "metadata": {},
   "source": [
    "### 💡Final Recommendations\n",
    "- The organization should introduce new engagement schemes or retention plans to improve customer loyalty and reduce churn.\n",
    "- The bank might focus on customers with high balances but lower credit scores, as they seem more likely to churn.\n",
    "- Introduce tailored financial products e.g., mortgage refinancing, investment options, or family-oriented savings plans.\n",
    "- Conduct targeted surveys or interviews Understand why this age group is dissatisfied — it could be due to loan rates, customer service, or   product relevance.\n",
    "- Middle-aged users often balance career and family — optimize mobile banking and digital support for convenience.\n",
    "- Promote relevant offers (e.g., credit cards, insurance, or investment plans) to existing single-product customers.\n",
    "- The bank should strengthen customer engagement through personalized communication, loyalty programs, and reactivation campaigns."
   ]
  },
  {
   "cell_type": "markdown",
   "id": "20e37f5e-1230-44de-b6d0-fa691565788c",
   "metadata": {},
   "source": [
    "### Author & Contacts\n",
    "**Suman**  \n",
    "📧 Email: [esuman065@gmail.com](mailto:esuman065@gmail.com)  \n",
    "🌐 GitHub: [Suman437596](https://github.com/Suman437596)\n",
    " 🔗 Linkedln:[Suman Singh](https://www.linkedin.com/in/suman-singh-70262b280/)"
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3 (ipykernel)",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.12.4"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
