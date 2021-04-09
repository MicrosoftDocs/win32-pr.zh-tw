---
description: Windows Installer 資料庫的文字封存檔案會 idt 副檔名。
ms.assetid: 91d81fb2-3a41-477a-85c2-e68bfe482b9c
title: 封存檔案格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaf39383b961c305bf621793784332342f369a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848967"
---
# <a name="archive-file-format"></a>封存檔案格式

Windows Installer 資料庫的 [文字](text-archive-files.md) 封存檔案會 idt 副檔名。 將整個資料庫匯出至保存檔案時，資料庫中的每個資料表都有個別的 idt 檔案。 如果資料表包含資料流程資料行，資料表中的每個資料流程都會以副檔名為 ibd 的檔案來表示。 Ibd 檔案會儲存在與資料表同名的資料夾中。

## <a name="idt-file-format"></a>idt 檔案格式

只包含 ASCII 字元之匯出資料庫資料表的 idt 檔案具有下列基本格式。

-   第一個資料列包含以定位字元分隔的資料表資料行名稱。
-   第二個數據列包含以定位字元分隔的資料行定義。
-   如果檔案只包含 ASCII 資料，則第三個數據列是以 tab 分隔的資料表名稱和主鍵資料行名稱。
-   檔案中的其餘資料列代表資料表中的資料列，資料行是以定位字元分隔。

> [!Note]  
> 如果檔案包含非 ASCII 資料，則第三個數據列是數值字碼頁，後面接著資料表名稱和主鍵資料行名稱，並以定位字元分隔。 包含非 ASCII 資訊的 idt 檔案應該以 ASCII 格式儲存。 例如，文字封存檔案可以包含編碼為 UTF-8 的資料行和資料表名稱，但封存檔案本身應該是 ASCII。 請參閱 [文字保存檔案中的 ASCII 資料](ascii-data-in-text-archive-files.md)一節。

 

> [!Note]  
> 特殊的[ \_ ForceCodepage](-forcecodepage.md)和[ \_ SummaryInformation](-summaryinformation.md) idt 檔會使用擴充格式。 如需 \_ 其格式的說明，請參閱 ForceCodepage 和 \_ SummaryInformation 一節。

 

## <a name="column-definitions"></a>資料行定義

資料行定義是以字元表示。

-   第一個字元表示資料行類型。 小寫字母表示不可為 null 的資料行，而大寫字母表示資料行可以包含 null 值。

    | 字元 | 意義                   |
    |-----------|---------------------------|
    | s、S      | 字串資料行             |
    | l、L      | 可當地語系化的字串資料行 |
    | v、V      | 二進位資料行             |
    | i、I      | 整數資料行            |

    

     

-   第二個字元表示資料行資料大小。

    > [!Note]  
    > Windows Installer 實際上不會使用指定的資料行大小來限制可在字串資料列欄位中輸入的字串大小。 不過，有些撰寫工具會使用指定的資料行大小來限制有效字串的大小。 建議輸入任何資料行中的字串符合指定的大小需求。

     

    

    | 資料行定義 | 意義                                    |
    |-------------------|--------------------------------------------|
    | s255              | 不可為 Null 的字串資料行 255 long        |
    | L50               | 可為 null 的可當地語系化字串資料行 50 long |
    | i2，I2            | Short 整數資料行                       |
    | i4、I4            | 長整數資料行                        |

    

     

## <a name="control-character-translation"></a>控制字元轉譯

將資料表匯出到文字封存檔案會轉譯控制字元，以避免與檔案分隔符號發生衝突。 寫入 idt 檔案時，控制字元會轉譯如下。



| 控制字元 | Idt 中的翻譯 | 意義         |
|-------------------|---------------------|-----------------|
| NULL              | 21                  | Null            |
| BS                | 27                  | 背面空間      |
| HT                | 16                  | 索引標籤             |
| 如果                | 25                  | 換行字元       |
| FF                | 24                  | 表單摘要       |
| CR                | 17                  | 回車 |



 

 

 



