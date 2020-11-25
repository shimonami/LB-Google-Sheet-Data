<a href="https://twitch.tv/sexyguchi" target=_blank>
  <img src="https://img.shields.io/twitch/status/sexyguchi?color=blueviolet&label=twitch.com%2Fsexyguchi&logo=twitch&logoColor=white&style=for-the-badge" alt="follow us!">
</a>

# LB-Google-Sheet-Data
A plugin to get Google Sheet data on Lioran Board

### How to Install
- :exclamation::exclamation::exclamation: **Download [this file](https://drive.google.com/file/d/1Q0aMc29CVsIJw1rQ0ki69BA9NEo4bjCL).**
- Move it to your LioranBoard `extension` folder.
- Start your `LioranBoard receiver`.
- Click on `Install Extension`.
- Select `Google Sheet Data` and your `tsl_transmitter`.
- Done :tada:

### Requirements
To use this extension, you need a `Google API key`. To generate it go to this [link](https://developers.google.com/sheets/api/quickstart/js), click on `Enable the Google Sheets API`.

On the modal set any name (you can use `Lioran Board` for reference) and click in `Next`.

Close the modal after it's done and click on `Create API key`.

Input the same name that you used before (`Lioran Board`, for reference) and copy the value that will appear on the modal.

If you lost your key somehow, you can get it on this [link](https://console.developers.google.com/apis/credentials) and click on this icon:
![image](https://user-images.githubusercontent.com/29884217/100128940-b0540800-2e5f-11eb-9966-83c2659ce456.png)

To use this extension, you need to change your Google Sheet from `Restricted` to
![image](https://user-images.githubusercontent.com/29884217/100136552-f4e4a100-2e69-11eb-9a4b-b6cd58098621.png)

### Parameters
This extension follows this [api documentation](https://developers.google.com/sheets/api/reference/rest/v4/spreadsheets.values/get):

- `api_key`: your google API Key.
- `sheet_id`: your google sheet id (without `/`).
  - You can get it on your Google Sheet url:
  ![image](https://user-images.githubusercontent.com/29884217/100136870-599ffb80-2e6a-11eb-84de-61e6751649d7.png)
- `range`: a range of your google sheet cells.
- `dimension`: possible values are `ROWS` or `COLUMNS`.
- `render`: possible values are `FORMATTED_VALUE`, `UNFORMATTED_VALUE` and `FORMULA`.
- `row_number`: which `row` or `column` you are getting the data.

All those data are sent to a stack called `SheetValuesStack` on `LioranBoard`.

### Demo
On [this spreadsheet](https://docs.google.com/spreadsheets/d/1bjfq4M6efTgkt4bXsQMlYLVcJtqQzCmB9XN6wdpfq4o/), this button
![image](https://user-images.githubusercontent.com/29884217/100136275-98818180-2e69-11eb-8a0f-5d8bc19d4233.png)

will produce this result

![image](https://user-images.githubusercontent.com/29884217/100136361-b6e77d00-2e69-11eb-8882-be09235e5e07.png)
