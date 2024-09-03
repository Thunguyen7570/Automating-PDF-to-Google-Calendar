# Automating-PDF-to-Google-Calendar
This project is a Python script that extracts meeting information from a PDF file and converts it into a Google Calendar compatible `.ics` file. This is particularly useful for importing a large number of meetings or events into Google Calendar at once.


# Features

-   **PDF Text Extraction**: Extracts text from the specified PDF file.
-   **Event Data Extraction**: Identifies and extracts event details such as date, time, title, and location using regular expressions.
-   **Google Calendar Integration**: Converts the extracted event information into a `.ics` file that can be imported into Google Calendar.
-   **Timezone Support**: Events are localized to the specified timezone.


## Requirements

-   Python 3.x
-   `pdfplumber` - For extracting text from PDF files.
-   `ics` - For creating `.ics` calendar files.
-   `pytz` - For handling timezone conversions.

## Installation

1.  **Clone the repository:**   
    `git clone https://github.com/yourusername/pdf-to-google-calendar.git
    cd pdf-to-google-calendar` 
    
2.  **Install the required Python packages:**
    `pip install pdfplumber ics pytz`


## Usage
1.  **Specify the path to your PDF file:**
 `pdf_path = r"C:\path\to\your\file.pdf"` 
    
2.  **Run the script to extract text from the PDF and convert it into a Google Calendar file:**
   `python main.py` 
    
3.  **Output:**
    
    -   The script will generate an `.ics` file containing all the meetings/events extracted from the PDF.
    -   The file will be saved in the location specified in the script, e.g: C:\Users\YourName\Desktop\meetings.ics`.
 
  4. **Import the `.ics` file into Google Calendar:**
     -   Open Google Calendar.
     -   Click the gear icon and select "Settings".
     -   In the "Import & export" section, select "Import" and choose the `.ics` file you generated.

## PDF Format Requirements

For the script to properly extract and convert event details from the PDF, the text within the PDF must adhere to a specific format. Below is an example of the expected format for each event in the PDF:

 - [Event Title]   
 - [Date (dd/mm/yyyy)] 
 - [Start Time (hh:mm)]   
 - [End Time (hh:mm)]   
 - [Location]

### Example:
 - Team Meeting   15/09/2024  09:00  10:00  Conference Room A Project
 -  Update 16/09/2024  11:30  12:30  Meeting Room 2 
 - Workshop 17/09/2024  14:00  16:00  Auditorium

