# rename-drivers-vehicles
Using VF API, make changes to Drivers &amp; Vehicles

## Usage

1. Fill out `Sample Excel.xlsx` in Files/ with the data that you want to update in VF.
2. In `config_settings.py` change the File Name (IMPORT_FN) and pick an appropriate Environment (ENV) (staging/production)
3. Login to VF and get a `COOKIE`
4. `python rename.py` and paste the cookie when prompted
Type `N` to skip vehicle or driver update when prompted
