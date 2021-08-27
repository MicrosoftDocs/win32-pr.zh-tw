---
description: ICE88 會驗證 Windows Installer 封裝中是否存在 IniFile 資料表的 DirProperty 資料行中所參考的目錄。
ms.assetid: 9bb253fd-e231-4016-807d-3b1068ecff68
title: ICE88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cb49ce6cb4363cfe89879f6e72b7ce801c063ea2b278c03dacf5cbadacddce9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105218"
---
# <a name="ice88"></a>ICE88

ICE88 會驗證 Windows Installer 封裝中是否存在[IniFile 資料表](inifile-table.md)的 DirProperty 資料行中所參考的目錄。 如果 DirProperty 值不代表目錄、AppSearch 或屬性資料表中的屬性、特定的 [系統資料夾屬性](property-reference.md)，或由類型51自訂動作所設定的屬性，ICE88 就會發出警告。

ICE88 會掃描下列資料表和屬性。

-   [目錄資料表](directory-table.md)
-   [AppSearch 資料表](appsearch-table.md)
-   [屬性工作表](property-table.md)
-   [CustomAction 資料表](customaction-table.md) ，其中自訂動作是 [自訂動作類型 51](custom-action-type-51.md)
-   [**ProgramFilesFolder 屬性**](programfilesfolder.md)
-   [**CommonFilesFolder 屬性**](commonfilesfolder.md)
-   [**SystemFolder 屬性**](systemfolder.md)
-   [**ProgramFiles64Folder 屬性**](programfiles64folder.md)
-   [**CommonFiles64Folder 屬性**](commonfiles64folder.md)
-   [**System64Folder 屬性**](system64folder.md)

## <a name="result"></a>結果

ICE88 會張貼下列警告。



| ICE88 警告                                                                                                                                                                  | 描述                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 在 IniFile 資料表專案中 (IniFile =) \[ 3 \] \[ \] ：在目錄/屬性/AppSearch/CA Type51 資料表中找不到 DirProperty = 1，而且它不是其中一個安裝程式屬性。 | ICE88 會針對 IniFile 資料表中的每一筆記錄，讀取 DirProperty 資料行中的值。 ICE88 會掃描 [目錄資料表](directory-table.md)、 [AppSearch 資料表](appsearch-table.md)和 [屬性工作表](property-table.md) 中的值，也會掃描安裝程式所設定的屬性清單。 如果在掃描中找不到值，ICE88 會張貼此警告。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



