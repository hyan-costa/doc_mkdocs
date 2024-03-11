# Api AVM gateway documentation (MkDocs)

To run the application, it is necessary to create the virtual environment within the `docs/api_avm_gateway` directory.
``` bash
   python3 -m venv venv
```
``` bash
   source venv/bin/activate 
```

## Install Dependencies

1. run the following command:

 ``` bash
 pip install -r requirements.txt
 ```


## Run the Application

 ``` bash
 mkdocs serve
 ```

## *OBS:*
   after editing some .md file, run the following command:
``` bash
mkdocs build
```