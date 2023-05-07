# title: Password Protected Compressed File Extraction Via 7Zip
id: b717b8fd-6467-4d7d-b3d3-27f9a463af77
status: experimental
description: Detects usage of 7zip utilities (7z.exe, 7za.exe and 7zr.exe) to extract password protected zip files.
references:
    - https://blog.cyble.com/2022/06/07/bumblebee-loader-on-the-rise/
author: Nasreddine Bencherchali (Nextron Systems)
date: 2023/03/10
tags:
    - attack.collection
    - attack.t1560.001
logsource:
    category: process_creation
    product: windows
detection:
    selection_img:
        - Description|contains: '7-Zip'
        - Image|endswith:
            - '\7z.exe'
            - '\7zr.exe'
            - '\7za.exe'
        - OriginalFileName:
            - '7z.exe'
            - '7za.exe'
    selection_password:
        CommandLine|contains|all:
            - ' -p'
            - ' x '
            - ' -o'
    condition: all of selection_*
falsepositives:
    - Legitimate activity is expected since extracting files with a password can be common in some environement.
level: medium
