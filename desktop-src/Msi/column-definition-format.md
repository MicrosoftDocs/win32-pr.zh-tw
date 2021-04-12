---
description: View 物件的 MsiViewGetColumnInfo 和 ColumnInfo 屬性會使用下列格式來描述資料庫資料行定義。
ms.assetid: 77379664-26f2-4c1d-8c44-d9be2376efa9
title: 資料行定義格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e43e7f70c942fda32bf5003571fa687250e971d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193125"
---
# <a name="column-definition-format"></a>資料行定義格式

[**View**](view-object.md)物件的 [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo)和 [**ColumnInfo 屬性**](view-columninfo.md)會使用下列格式來描述資料庫資料行定義。 每個資料行都是由函數或屬性所傳回之對應記錄欄位中的字串所描述。 定義字串是由代表資料類型的單一字母所組成，後面接著資料行的寬度 (字元（如果適用的話），否則) 。 寬度為零會指定未系結的寬度 (例如，長文字欄位和資料流程) 。 大寫字母表示資料行中允許 null 值。



| 資料行描述項 | 定義字串                 |
|-------------------|-----------------------------------|
| ！?                | 字串，變數長度 (？ = 1-255)  |
| s0                | 字串、可變長度           |
| i2                | Short 整數                     |
| i4                | 長整數                      |
| v0                | 二進位資料流程                     |
| G？                | 暫存字串 (？ = 0-255)         |
| J？                | 暫存整數 (？ = 0，1，2，4)      |
| O0                | 暫存物件                  |



 

用來描述資料行的字串與 CREATE 和 ALTER 所使用的 SQL 查詢字串具有下列關聯性。 如需詳細資訊，請參閱 [SQL 語法](sql-syntax.md)。



| 傳回值 | SQL 語法                |
|----------------|---------------------------|
| s0             | LONGCHAR                  |
| l0             | LONGCHAR 可當地語系化      |
| ！ \#           | CHAR (\#)                   |
| ！ \#           | 字元 (\#)              |
| 我 \#           | 可當地語系化的 CHAR (\#)       |
| 我 \#           |  () 可當地語系化的字元 \# |
| i2             | SHORT                     |
| i2             | INT                       |
| i2             | INTEGER                   |
| i4             | LONG                      |
| v0             | OBJECT                    |



 

如果字母不是大寫，則應該附加非 Null 的 SQL 語句。



| 傳回值 | SQL 語法        |
|----------------|-------------------|
| s0             | LONGCHAR 不可為 Null |



 

安裝程式不會在內部將資料行的長度限制為數據行定義格式所指定的值。 如果在欄位中輸入的資料超過指定的資料行長度，封裝就無法通過 [封裝驗證](package-validation.md)。 若要在這種情況下通過驗證，則必須變更資料或資料庫架構。 變更標準資料表之資料行長度的唯一方法是使用 [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)匯出資料表、編輯匯出的 idt 檔案，然後使用 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)匯入資料表。 作者無法變更標準資料表中任何資料行的資料行資料類型、null 屬性或當地語系化屬性。 作者可以使用具有任何資料行屬性的資料行來建立自訂資料表。

使用 [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) 將參考資料庫合併到目標資料庫時，資料行名稱、主鍵數目和資料行資料類型必須相符。 **MsiDatabaseMerge** 會忽略當地語系化和資料行長度屬性。 如果參考資料庫中的資料行長度為0或大於該資料行在目標資料庫中的長度， **MsiDatabaseMerge** 會將目標資料庫中的資料行長度增加到參考資料庫中的長度。

使用 Mergmod.dll 版本2.0 時，將合併模組的應用程式寫入 .msi 檔案時，絕對不會變更資料行的長度或現有資料庫資料表的資料行類型。 但是，如果模組將新的資料行加入至資料表，以便加入資料行，則合併模組的應用程式可以變更現有資料庫資料表的架構。 使用小於2.0 版的 Mergemod.dll 版本時，合併模組的應用程式永遠不會變更資料行的長度，而且永遠不會變更目標資料庫的架構。

 

 



