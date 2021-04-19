---
description: ICE32 會驗證 .msi 檔案中的索引鍵和外鍵的大小和資料行定義類型是否相同。
ms.assetid: cc488ec5-e17a-4829-9763-38ba3c33bfde
title: ICE32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d6ff9e4de592ac073050b357aff0c63d984f0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980365"
---
# <a name="ice32"></a>ICE32

ICE32 會驗證 .msi 檔案中的索引鍵和外鍵的大小和資料行定義類型是否相同。 這個 ICE 自訂動作會使用 [ \_ 驗證資料表](-validation-table.md)來進行比較，並使用 [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo)所傳回的定義類型。 如需詳細資訊，請參閱資料 [行定義格式](column-definition-format.md)。

## <a name="result"></a>結果

如果 .msi 檔案包含不同資料行長度或資料行資料類型之索引鍵的任何外鍵，則 ICE32 文章錯誤。

## <a name="example"></a>範例

ICE32 會針對所顯示的範例張貼兩個錯誤：

-   有一個定義的外鍵和索引鍵大小不同。
-   定義的外鍵和索引鍵在其定義類型中有所差異。

[ \_ 驗證資料表](-validation-table.md) (部分) 



| 資料表 | 資料行  | KeyTable | KeyColumn |
|-------|---------|----------|-----------|
| 檔案  | 版本 | 檔案     | 1         |
| 皮 瓣  | Column8 | 皮 瓣     | 1         |



 

 (部分) 的資料行定義



| 資料表 | 資料行  | 類型 | 大小 |
|-------|---------|------|------|
| 檔案  | 檔案    | s    | 72   |
| 檔案  | 版本 | S    | 32   |
| 皮 瓣  | 資料行1 | i    | 2    |
| 皮 瓣  | Column8 | S    | 32   |



 

File 資料表的 [版本] 資料行可以是檔案資料表中另一個檔案的外鍵。 這會發生在隨附的檔案中。 但是，Version 資料行只允許字串長度為32，而 File 資料行允許字串長度為72。 若要修正這個錯誤，請將字串長度變更為相符。

定義的外鍵和索引鍵在其定義類型中有所差異。 傳動表的 Column8 會列為 Column1 的外鍵。 Column8 是一個字串資料行，而 Column1 是一個整數資料行。 必須定義外鍵和索引鍵組，使其資料類型相符。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



