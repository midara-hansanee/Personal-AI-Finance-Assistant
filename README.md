# Personal-AI-Finance-Assistant
An ai agent that build for financial advices
Personal Finance Coach AI
Overview
The Personal Finance Coach AI is a user-friendly web application built with Gradio to help users manage their finances. It allows users to set savings goals, estimate savings based on income and expenses, and get financial advice through an intuitive chatbot interface. The app features a modern, clean design with a blue-themed UI, making money management accessible and engaging.
Features

Tracks Financial Goals: Set and manage savings goals (e.g., vacation, car) with amounts and timelines.
Estimates Savings: Calculate potential savings using monthly income and expenses.
Provides Financial Advice: Answer questions on budgeting, investing, and more.
Modern UI: Clean, centered layout with rounded buttons and a scrollable chatbot, styled with custom CSS and Gradio's Soft theme.
Robust Functionality: Persists user data during sessions, parses commands, handles errors, and supports extensibility.

Installation

Clone the Repository:
git clone https://github.com/your-username/personal-finance-coach-ai.git
cd personal-finance-coach-ai


Install Dependencies:Ensure Python 3.8+ is installed, then install required packages:
pip install gradio

Note: The FinanceAgent class and its dependencies (e.g., user_interaction, reset_chat) are assumed to be defined in your codebase. Install any additional libraries as needed.

Run the Application:Execute the main script:
python finance_coach_ui.py

Set share=False in the demo.launch() function for local testing to avoid public sharing.


Usage

Launch the App: Run the script to open the Gradio UI in your browser.
Interact with the AI:
Set Goals: Enter commands like add goal vacation 1000 12 to save for a $1,000 vacation over 12 months.
List Goals: Type list goals to view all saved goals.
Estimate Savings: Use estimate savings 3000 1500 to calculate savings from $3,000 income and $1,500 expenses.
Ask Questions: Type questions like "How do I budget?" for financial advice.


Use Buttons:
Send: Submit your input to the chatbot.
Reset Chat: Clear the conversation and reset the agent’s state.



Example Commands

add goal car 5000 24 - Set a goal to save $5,000 for a car in 24 months.
list goals - Display all saved goals.
estimate savings 2500 1800 - Estimate savings from $2,500 income and $1,800 expenses.
What’s the best way to save for retirement? - Get financial advice.

Technical Details

State Management: Uses gr.State to persist the FinanceAgent instance, storing goals in a data structure (e.g., list or dictionary).
Command Parsing: The user_interaction function parses commands and handles free-form questions via NLP or predefined logic.
Chatbot Integration: gr.Chatbot displays conversational history, updated dynamically by user_interaction.
Error Handling: Try-except block ensures robust UI launch; FinanceAgent handles invalid inputs with user-friendly messages.
UI Styling: Custom CSS and gr.themes.Soft() create a modern, blue-themed interface with rounded corners and a 400px chatbot window.
Modular Functions: user_interaction processes inputs; reset_chat clears history and resets the agent.
Extensibility: Supports adding complex calculations or API integrations for real-time financial data.

Project Structure
personal-finance-coach-ai/
├── finance_coach_ui.py  # Main Gradio UI script
├── README.md            # Project documentation
└── [other files]        # Add FinanceAgent class, user_interaction, reset_chat, etc.

Notes

The FinanceAgent class, user_interaction, and reset_chat functions are not included in the provided code. Ensure they are implemented in your project.
Update dependencies as needed for FinanceAgent (e.g., NLP libraries or financial APIs).
For local testing, set share=False in demo.launch() to avoid public exposure.

Contributing
Contributions are welcome! Please submit a pull request or open an issue for suggestions, bug reports, or feature requests.
License
This project is licensed under the MIT License. See the LICENSE file for details.
Acknowledgments
Built with Gradio for a seamless web interface. Inspired by the need for accessible personal finance tools.
