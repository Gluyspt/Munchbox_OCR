# Receipt OCR and formatting
This Python script extracts menu items and quantities from restaurant receipt images using PaddleOCR. It uses Fuzzy Matching to correct OCR errors based on a predefined list of real menu names.

# 1. Setup Environment
It is recommended to use a virtual environment.

'''
# Create environment
python -m venv venv
'''

'''
# Activate environment (Windows)
venv\Scripts\activate
'''

'''
# Activate environment (Mac/Linux)
source venv/bin/activate
'''

# 2. Install Dependencies
Install the required libraries (OpenCV, PaddleOCR, and PaddlePaddle).

'''
pip install opencv-python paddleocr paddlepaddle
'''

# 3. Configuration

A. Add Your Image
Place your receipt image in the project folder. By default, the script looks for:

Folder: test_image/

Filename: sample_bad_image1.jpg

(You can change img_path in line 32 of the code if your file is named differently).

B. Edit Menu List (Crucial)
Open the script and update the real_menus list at the top. This must match the actual items sold in your shop exactly for the auto-correction to work.

'''
real_menus = [
    "Pepsi",
    "Green Tea",
    "Pork Set A",
    # ... add your actual menu items here
]
'''

# 4. Run the Script

'''
python your_script_name.py
'''

5. Output
The script will generate two files:

CSV Report: output_csv/sales_table_v1.csv (Clean list of Item + Quantity).
Debug Image: output_image/layout_detection_v4.jpg (Shows what the AI detected).
