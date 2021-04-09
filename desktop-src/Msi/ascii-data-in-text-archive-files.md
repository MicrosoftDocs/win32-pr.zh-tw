---
description: 當僅包含 ASCII 字元的資料表匯出到文字封存檔案時，idt 檔案會遵守基本的封存檔案格式。
ms.assetid: 105d2b85-c6e1-4719-83b4-1693c14ef4f4
title: 壓縮檔案中的 ASCII 資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d43deeb7918b75a71770ab9d09535972f6e8bb4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848964"
---
# <a name="ascii-data-in-text-archive-files"></a>壓縮檔案中的 ASCII 資料

當僅包含 ASCII 字元的資料表匯出到 [文字](text-archive-files.md)封存檔案時，idt 檔案會遵守基本的封存檔案 [格式](archive-file-format.md)。 如果資料表包含非 ASCII 資訊，封存檔案的格式會擴充以包含字碼頁資訊。

## <a name="text-archive-files-that-contain-only-ascii-characters"></a>只包含 ASCII 字元的壓縮檔案

當僅包含 ASCII 字元的資料表匯出到封存檔案時，idt 檔案會是基本的封存 [檔案格式](archive-file-format.md)。 資料表中的每個資料流程都會匯出為副檔名為 ibd 的檔案。 Ibd 檔案會儲存在與資料表同名的資料夾中。 例如，請考慮匯出下列 [二進位](binary-table.md) 資料表。



| Name  | 資料      |
|-------|-----------|
| 書籍 | Ibd |
| Cars  | 車輛. ibd  |



 

匯出此資料表之後的目錄結構如下所示。 資料庫資料表中的資訊會匯出為 idt。 系統會將兩個二進位資料串流匯出至 ibd 和 ibd 儲存在名為 Binary 的資料夾中。

``` syntax
Binary.idt
[Binary]
    Books.ibd
    Cars.ibd
```

Idt 封存檔案是基本的封存檔案 [格式](archive-file-format.md) ，看起來會如下所示。

``` syntax
Name Data
s72 v0
Binary  Name
Books   Books.ibd
Cars    Cars.ibd
```

## <a name="text-archive-files-that-contain-non--ascii-characters"></a>包含非 ASCII 字元的文字保存檔案

如果檔案包含非 ASCII 資料，則會擴充 idt 檔案的基本封存 [檔案格式](archive-file-format.md) ，以包含字碼頁資訊。 Idt 資料表中的第三個數據列是數值字碼頁，後面接著以 tab 分隔的資料表名稱和主鍵資料行名稱。

> [!Note]  
> 包含非 ASCII 資訊的 idt 檔案應該以 ASCII 格式儲存。 例如，文字封存檔案可以包含編碼為 UTF-8 的資料行和資料表名稱，但封存檔案本身應該是 ASCII。

 

下列當地語系化為法文的 ActionText 資料表會包含非 ASCII 資訊。 用於法文字串的數值字碼頁為1252。



| 動作    | 描述                                  | 範本 |
|-----------|----------------------------------------------|----------|
| 通告 | 發行集 d'informations sur l'application |          |



 

匯出的封存檔案（ActionText. idt）如下所示。

``` syntax
Action   Description Template
s72 L0  L0
1252    ActionText  Action
Advertise   Publication d'informations sur l'application
```

> [!Note]  
> 如果文字保存檔案包含非 ASCII 資料，封存檔案就會包含字碼頁資訊。 具有字碼頁資訊的封存檔案只能匯回至該確切字碼頁的資料庫，或匯入至非語言相關的資料庫中。 如果是中性語言的資料庫，則字碼頁會設定為封存檔案的字碼頁。 如需 Windows Installer 如何處理字碼頁的詳細資訊，請參閱 [ (Windows Installer) 中的字碼頁處理 ](code-page-handling-windows-installer-.md)小節。

 

 

 



