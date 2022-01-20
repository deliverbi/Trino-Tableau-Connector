# Trino-Tableau-Connector
Trino Tableau Connector - 368 + Works with all versions of Trino + Their are 2  Connector zips uploaded, One for SSL Entain and One for Default Trino . The files can be edited with any text editor and are quite simple to understand. Manifest is the main file. You can remove SSL properties from the following files.

`connectionBuilder`
`connectionProperties`


## Create a folder to store the connector code.

Create a directory for Tableau connectors in the following location:
### For Tableau Desktop:
- Mac: `/connector`
- Windows: `C:\connector`
### For Tableau Server:
- Linux: `/connector`
- Windows: `c:\conector`

`Tableau Connector NON SSL Standard Trino Connections - tableau_trino_jdbc_connector.zip`
Within folder created above unzip the code for the Tableau Connector (tableau_trino_jdbc_connector.zip). Once unzipped you will see a parent folder inside you will find the files required for the connector to work.


`Tableau Connector FOR SSL Connections - tableau_entain_trino_jdbc_connector.zip`
Within folder created above unzip the code for the Tableau Connector (tableau_entain_trino_jdbc_connector.zip). Once unzipped you will see a parent folder inside you will find the files required for the connector to work.


## Download Trino Driver and place in Tableau drivers directory
Driver can be downloaded from the trino website here is an example link : https://repo1.maven.org/maven2/io/trino/trino-jdbc/368/trino-jdbc-368.jar

Move the driver (jar) file to following location:
- Windows: `c:\Program File\Tableau\Drivers`
- Mac: `~/Library/Tableau/Drivers`
- Linux: `/opt/tableau/tableau_driver/jdbc`

## Launch Trino and You will see your new custom Connector called : Trino JDBC by Entain for SSL and Trino JDBC by Trino for Default.

You should launch Tableau so it will load custom Drivers. Refer to Tableau documentation examples below for windows.


Open a Command Prompt --:
- MAC:

```
/Applications/Tableau\ Desktop\ 2019.1.app/Contents/MacOS/Tableau -DConnectPluginsPath=/connector/
```

- Windows:

```
CD c:\Program Files\Tableau\Tableau {VERSION}\bin\
tableau.exe -DConnectPluginsPath=C:\connector
```

Shortcut can also be created in windows like the following

Windows Tableau ShortCut :
```
"C:\Program Files\Tableau\Tableau [version]\bin\tableau.exe" -DConnectPluginsPath=C:\connector
```


Enjoy. Remeber their are other ways as per above to launch Tableau and store connector files . Please experiment.

DeliverBI Team
