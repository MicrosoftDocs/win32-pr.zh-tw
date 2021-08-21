---
description: '\_Columns 資料表是包含資料行目錄的唯讀系統資料表。 它會列出所有資料表的資料行。 您可以查詢此資料表，以找出指定的資料行是否存在。'
ms.assetid: 1ddde4e2-90a9-4dd8-a4f9-b6802d0b11cf
title: _Columns 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7cbb603c077d7873cdfbea88070e555902883ba579b422627b2581aca04745b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640473"
---
# <a name="_columns-table"></a>\_Columns 資料表

\_Columns 資料表是包含資料行目錄的唯讀系統資料表。 它會列出所有資料表的資料行。 您可以查詢此資料表，以找出指定的資料行是否存在。

\_Columns 資料表具有下列資料行。



| Column | 類型                   | 答案 | Nullable |
|--------|------------------------|-----|----------|
| 資料表  | [Text](text.md)       | Y   | N        |
| 數字 | [整數](integer.md) | Y   | N        |
| Name   | [Text](text.md)       | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>表
</dt> <dd>

包含資料行之資料表的名稱。

</dd> <dt>

<span id="Number"></span><span id="number"></span><span id="NUMBER"></span>數量
</dt> <dd>

資料表內資料行的順序。

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>名字
</dt> <dd>

資料行名稱。

</dd> </dl>

## <a name="remarks"></a>備註

因為 \_ Columns 資料表是無法透過 SQL 查詢修改的系統資料表，所以您無法使用 [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa)函數或 [**PrimaryKeys 屬性**](database-primarykeys.md)取得主鍵。

只有持續性資料行會儲存在 \_ columns 資料表中。 若要判斷暫存資料行是否存在，必須針對資料表使用 SELECT 語句來建立一個 view \* ，然後使用 MSICOLINFO NAMES 選項來迴圈處理 [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) 函式所傳回之記錄中的所有欄位 \_ 。

 

 



