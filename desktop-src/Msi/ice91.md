---
description: 如果檔案、.ini 檔案或快捷方式檔案已安裝到每個使用者的目錄中，ICE91 會張貼警告。
ms.assetid: 1834d841-b1d9-4646-8057-a41dd88310b6
title: ICE91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f5723369c21894817dacbc1755430a31f17199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988938"
---
# <a name="ice91"></a>ICE91

如果檔案、.ini 檔案或快捷方式檔案已安裝到每個使用者的目錄中，ICE91 會張貼警告。 如果封裝只用于每個使用者 [安裝內容](installation-context.md) 中，而且永遠不會用於個別電腦安裝，則這些警告是無害的。

檔案、.ini 檔或個別使用者目錄中的快捷方式會安裝在特定使用者的設定檔中。 即使使用者設定個別電腦安裝的 [**ALLUSERS**](allusers.md) 屬性、檔案、.ini 檔案或個別使用者目錄中的快捷方式，都不會複製到「所有使用者」設定檔，其他使用者也無法使用。 每個使用者唯一的目錄不會與 **ALLUSERS** 屬性不同。 以下是每個使用者的唯一目錄清單：

-   AppDataFolder
-   FavoritesFolder
-   NetHoodFolder
-   PersonalFolder
-   PrintHoodFolder
-   RecentFolder
-   SendToFolder
-   MyPicturesFolder
-   LocalAppDataFolder

## <a name="result"></a>結果

ICE91 會張貼下列警告。



| ICE91 警告                                                                                                                                                                                                                            | Description                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| 檔案 ' \[ 1 \] ' 將會安裝到每個使用者目錄 ' \[ 2 \] '，而不會因 [**ALLUSERS**](allusers.md) 值而不同。 此檔案不會複製到每個使用者的設定檔中，即使需要每一部電腦安裝也一樣。     | 檔案會安裝到每個使用者的目錄中。 它不會在每部電腦安裝期間安裝到每個使用者的設定檔中。      |
| IniFile ' \[ 1 \] ' 將會安裝到每個使用者目錄 ' \[ 2 \] '，而不會因 [**ALLUSERS**](allusers.md) 值而不同。 此檔案不會複製到每個使用者的設定檔中，即使需要每一部電腦安裝也一樣。  | .Ini 檔案會安裝到每個使用者的目錄中。 它不會在每部電腦安裝期間安裝到每個使用者的設定檔中。 |
| 快捷方式 ' \[ 1 \] ' 將會安裝到每個使用者目錄 ' \[ 2 \] '，而不會因 [**ALLUSERS**](allusers.md) 值而不同。 此檔案不會複製到每個使用者的設定檔中，即使需要每一部電腦安裝也一樣。 | 此快捷方式會安裝到每個使用者的目錄中。 它不會在每部電腦安裝期間安裝到每個使用者的設定檔中。  |



 

## <a name="example"></a>範例

ICE91 會報告下列範例警告：

``` syntax
The file 'File1' will be installed to the per user directory 'MyPicturesFolder' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.

The IniFile 'IniFile1' will be installed to the per user directory 'MyIniDir' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.

The shortcut 'Shortcut1' will be installed to the per user directory 'MyShortcutDir' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.
```

[檔資料表](file-table.md) (部分) 



| 檔案  | 元件\_ |
|-------|-------------|
| File1 | C1          |



 

[元件資料表](component-table.md) (部分)  (部分)  (部分)  (部分) 



| 元件 | 目錄\_ |
|-----------|-------------|
| C1        | MyDir       |



 

[IniFile 資料表](inifile-table.md)



| IniFile  | DirProperty |
|----------|-------------|
| IniFile1 | MyIniDir    |



 

[快速鍵資料表](shortcut-table.md)



| 快速鍵  | 目錄\_   |
|-----------|---------------|
| Shortcut1 | MyShortcutDir |



 

[目錄資料表](directory-table.md)



| 目錄     | 目錄 \_ 父系  |
|---------------|--------------------|
| MyDir         | FavoritesFolder    |
| MyIniDir      | LocalAppDataFolder |
| MyShortcutDir | PersonalFolder     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



