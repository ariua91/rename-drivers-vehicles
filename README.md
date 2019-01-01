# rename-drivers-vehicles
Using VF API, make changes to Drivers &amp; Vehicles

## Usage

1. Fill out `Files/Sample Excel.xlsx` in with the data that you want to update in VF.
2. In `config_settings.py`
    - change the File Name (IMPORT_FN)
    - pick an appropriate Environment (ENV) (staging/production)
3. Login to VF and get a `COOKIE`
4. `python -i rename.py`
    - Paste the cookie when prompted
    - Type `N` to skip vehicle or driver update when prompted
5. Error handling only via console log and making a new list / dict with all the error attributes
    - Explore `driver_error_list` or `vehicle_error_dict` for the full details
    
## Improvements

1. Error Handling is super hacky
2. Change Working Hours is super hacky
    - There is no error handling for the WH Get
    - This is completely hardcoded the the client's WH use case. Ideally should be more general, a simple start would be the second value in the excel rather than in the dict, but the current way is easer for me to manage for now
