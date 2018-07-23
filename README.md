# GDrive Python

![PyPI](https://img.shields.io/pypi/v/pygdrive3.svg)
![PyPI - Python Version](https://img.shields.io/pypi/pyversions/pygdrive3.svg)


## Installing
```sh
$ pip install pygdrive3==0.2.0
```

## Usage
```py
from pygdrive3 import service

drive_service = service.DriveService('./client_secret.json')
drive_service.auth()

folder = drive_service.create_folder('Xesque')
file = drive_service.upload_file('Arquivo Teste', './files/test.pdf', folder)
link = drive_service.anyone_permission(file)

folders = drive_service.list_folders_by_name('Xesque')
files = drive_service.list_files_by_name('Arquivo Teste')

files_from_folder = drive_service.list_files_from_folder_id(folder)
```

## by [Matheus Almeida](https://twitter.com/mat_almeida)

Use Google Drive API v3 with a python interface

# MIT License
