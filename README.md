# Firefox Bookmarks to Excel

This project makes it possible to read bookmarks from a Firefox `bookmarks.json` file and export them to an `Excel file`. It uses Python and Pandas to process the data.
I created it for practice and training purposes. It is useful to easily organize, edit and analyze your Firefox bookmarks. You can customize it and also use for Chrome bookmarks.

The **goal** of this project is to read the `bookmarks.json` file of the Firefox browser and make the information contained therein usable for further processing. The data should be flexibly usable and details of the saved bookmarks should be recorded. In addition, the folder path to each individual bookmark should be displayed.
The `bookmarks.json` file saves the structure of the bookmarks in the Firefox browser and contains all relevant information for further processing. Once exported, it requires a suitable method to read and display the data in a meaningful way.
I decided to use Python and Pandas to solve this task.
This project should not only help to prepare the information from the file, but also to improve the understanding and handling of JSON files.
I am using a Jupyter notebook to process and analyze the data.


## Requirements
- Python 3.x
- Dependencies from `requirements.txt`

## Installation
1. clone the repository (or download the files).
2. install the dependencies:
   ```bash
   pip install -r requirements.txt

## Information on the course of the project
1. **Import required libraries**  
   First, all the required Python libraries were imported, including `pandas` for data processing and standard libraries such as `json` and `datetime`.

2. **Read in the JSON file**  
   The `bookmarks.json` file, which stores the Firefox bookmarks in JSON format, was read in and converted into a Python data structure (dictionary).

3. **Examine and understand the structure of the file**  
   To analyze the nested structure of the bookmarks, the file was examined step by step, especially with regard to folders and subfolders.

4. **Extract bookmarks and observe folder structure**  
   The bookmarks were recursively extracted from the JSON data structure, taking into account the hierarchy of folders and subfolders.

5. **Include relevant fields in the DataFrame**  
   All required information such as `title`, `uri`, `iconUri`, `dateAdded` and `lastModified` was collected and included in a `DataFrame`.

6. **Recursive searching of the JSON structure**  
   A recursive approach was used to traverse the entire tree structure of the bookmarks to ensure that deeply nested entries were also taken into account.

7. **Add folder path as column**  
   For each bookmark, the full folder path within the Firefox bookmark structure was determined and added as an additional column.

8. **Creating a DataFrame with all information**  
   A `DataFrame` has been created that clearly displays all relevant information.

9. **Save DataFrame in an Excel file**  
   The finished `DataFrame` has been exported to an Excel file. Alternatively, another format such as CSV could also be used.

10. **Solve the datetime problem**  
    The timestamps (`dateAdded` and `lastModified`) in the JSON file were stored as Unix epoch values. These were converted into readable date formats in order to be displayed correctly in the Excel file.