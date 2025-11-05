<img width="1568" height="582" alt="Screenshot 2025-06-23 112037" src="https://github.com/user-attachments/assets/21d1add6-e35c-4a81-9ebb-78a320402e97" />
#AI-Powered Resource Allocation Agent | Automated Team Builder using (n8n) & OpenAI API. 

**Overview**

•	Created a complete N8N workflow to automate the entire process of intelligent team formation based on project needs

• Designed for HR or resource allocation use cases where skill-based team mapping is needed.

• Uses AI Agent API keys to connect with OpenAI for intelligent text processing.

**Key Features**

• Accepts PDF (requirements) and CSV (employee data) uploads via form trigger.

• Extracts and reads both files automatically using Extract from File nodes.

• Uses OpenAI GPT-4.1-mini model integrated via AI Agent node for skill extraction.

• Converts extracted text into a structured JSON format using an Output Parser.

• Matches extracted skills with employee data through a custom JavaScript code node.

• Returns a final JSON object mapping each skill to employees having that skill.

• End-to-end automated process with visual flow execution in n8n.

**Workflow Structure**

1. Form Trigger – collects PDF and CSV files.
2. Extract from File Nodes – read data from uploaded files.
3. Split Out Nodes – separate and manage input data streams.
4. AI Agent Node – processes text to extract skill sets.
5. OpenAI Chat Model Node – connects via API key to GPT-4.1-mini.
6. Structured Output Parser Node – formats AI output into valid JSON.
7. Merge Node – combines parsed AI results with employee data.
8. Code Node – matches employees to skill sets and outputs final mapping.

**OpenAI Integration**

• The AI Agent connects to OpenAI through API credentials stored in n8n.

• Requires setting up OpenAI API Key under Credentials → OpenAI Account.

• The model used: gpt-4.1-mini.

• System prompt ensures AI extracts skillsets accurately in a single-array JSON.

**Input & Output**

• Input: PDF file containing project or job requirements.

• CSV file containing employee details with name and skillset columns.

• Output:JSON mapping skills → employees.
