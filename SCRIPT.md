# How to upload API script to your Hosting

⭐⭐⭐⭐⭐

_Thank you for your order, please consider to give your feedback if you have time._

## Get API script

[Follow vide tutorial](https://youtube.com)

After completion of order you will receive a PHP script, which contains codes that's return **TOTAL** and **CIRCULATING** supply of your token.

Login to your hosting file manager, you can you any hosting that support PHP.
I'm using [Hostinger](https://hostinger.in?REFERRALCODE=1SANJITHACK71) in my case to deploy API script.

Follow instructions shown in the image. In future UI may be changed.

![Hosting File Manager](https://user-images.githubusercontent.com/35589762/227582033-7840a9e0-ba89-4c14-bf26-2495acc58435.png)*_Hostinger File Manager_*

- Click on `File Manager` highlighted red color.
- It will redirect you to your website `File Manager`

![Public HTML Folder](https://user-images.githubusercontent.com/35589762/227583103-d49f265e-63df-4981-ab9d-119afab4c830.png)*_Hostinger Public HTML_*

- There will be a folder named `pulic_html` , open that folder.
- Now you are at root of your website.
- We need to create a folder or directory for our PHP API code.
- In my case I have created folder named `/api`
- Follow below instructions to create folder

![Create folder](https://user-images.githubusercontent.com/35589762/227584194-03dc7b56-f9aa-4c64-bb19-7fd7e8073676.png)*_Hostinger create new Folder_*

- Click on `New Folder` highlighted in red color.
- A new popup will appear.

![Creatting Folder](https://user-images.githubusercontent.com/35589762/227584952-bf34940c-9a70-4590-831e-c6964f49b942.png)*_Creating Folder_*

- Click on `CREATE` highlighted in red.
- Now you will be inside `/api` folder, if not then open the folder you have created.
- Then we need to upload the API script, to upload you need to click the the upside arrow on right-top on your file manager.
- Follow image instructions

![Uploading new API script](https://user-images.githubusercontent.com/35589762/227586106-046f2001-760e-4f61-9b43-c5198880d7ca.png)*_Uploading API script_*

![Select upload file](https://user-images.githubusercontent.com/35589762/227586735-eb24b653-e146-4963-ab71-674e2ed5fa8d.png)*_Select upload file_*

- Locate API script where you have downloaded and saved from Fiverr.

![script select](https://user-images.githubusercontent.com/35589762/227587071-e0cb989b-88b1-4f06-b66f-2038fa8942b1.png)*_Select script to upload_*

![Script uploaded](https://user-images.githubusercontent.com/35589762/227587561-bd4a75ec-8878-490c-a53e-c74f6519c754.png)*_Script has been uploaded_*

- `Kaboom!` you have just successfully deployed your API script on your hosting.
- Now we need to find out our endpoint which returns, `TOTAL` and `CIRCULATING` supply.
- Let's take an example. If your website domain is:
```
https://example.com/
```
- And the folder you created previously was `/api` then, you can call API by:

```
https://example.com/api
```

- If you see it returns a message in `JSON` formate something like this:


```json
{"status":200,"contractAddress":"0x796a4503b444a71b331c9556bef0815237ddeabc","decimal":18,"symbol":"oDOGE"}
```

- To access `TOTAL` and `CIRCULATING` supply API endpoint, we will pass a query parameter named `q` in this way, here is the available query

| Query      | Description |
| ----------- | ----------- |
| maxcoins      | It returns the maximum supply of token without burn |
| totalcoins   | It returns total supply of your token with burn or without burn |
| circulating | It returns the circulating supply of your token |

- API endpoint for `TOTAL SUPPLY`:
```
https://example.com/api/?q=totalcoins
```

- API endpoint for `CIRCULATING SUPPLY`:
```
https://example.com/api/?q=circulating
```

## How token supply are calculated?

According to [Coinmarketcap's documentation](https://support.coinmarketcap.com/hc/en-us/articles/360043396252-Supply-Circulating-Total-Max-)

- `Max supply`: Is the number of maximum token
- `Total supply`: Max supply - burn tokens
- `Circulating supply`: Total supply - (Wallet hold by team/developers)

I have tried my best to describe set-up process. If you have any query please feel free to ask:

```
https://fiverr.com/sanjithacks
```






