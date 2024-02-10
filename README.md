# Selenium Project

Selenium/Flask/REST API

The program named "filamentStock.py" contains the Selenium code, scraping through a website, Bambu Lab, which I frequently use for my 3D printing side hobby. It scans through each item, after navigating to the correct page, and appends the data to a temporary dictionary. Afterwards, it adds the data to a JSON file, and then it compares this new JSON file ("filaments_dict.json") with an older JSON file ("prev_filaments_dict.json"), adding the new information to the previous file and outputting the info to the terminal. This ensures that there is a JSON file with the up to date information, and also has a safe point in case the program were to somehow fail or bug.

The program named "my_api.py" is the REST API, created using Flask. It is performant and responds to certain queries when prompted using CRUD operations. For example, if the user types "/filament?name=PLA Basic" in the link, it will show the data for the filament with the name "PLA Basic". If the JSON file has been modified, then there is a commented out section of code which will edit the database with the new information.
