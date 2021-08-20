---
description: '\_資料流程資料表會列出內嵌的 OLE 資料流程。 這是臨時表，只有在 SQL 語句參考時才會建立。'
ms.assetid: 1e30472d-6ba5-410a-a81b-07ed225dcb69
title: _Streams 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23f3796a3abb402027dc9985991a6ba673f5381d8f35657e7d80b0714c40f1e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013336"
---
# <a name="_streams-table"></a>\_資料流程資料表

\_資料流程資料表會列出內嵌的 OLE 資料流程。 這是臨時表，只有在 SQL 語句參考時才會建立。



| Column | 類型                 | 答案 | Nullable |
|--------|----------------------|-----|----------|
| 名稱   | [Text](text.md)     | Y   | N        |
| 資料   | [二進位](binary.md) | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>名字
</dt> <dd>

識別資料流程的唯一索引鍵。 名稱的長度上限為62個字元。

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>資料
</dt> <dd>

未格式化的二進位資料。

</dd> </dl>

## <a name="remarks"></a>備註

若要複製 OLE 資料流程 (例如， [二進位](binary.md) 資料類型的物件) 從檔案複製到資料庫、在資料流程資料表中建立記錄，並將資料流程的 \_ 名稱輸入此記錄的名稱資料行中，然後使用 [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama)將資料從檔案複製到資料行。 使用 [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) 將新的記錄插入資料表中。

若要讀取內嵌于資料庫中的二進位資料流程，請使用 SQL 查詢來尋找和提取包含二進位資料的記錄。 使用 [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) 將二進位資料讀入緩衝區。

若要將二進位資料流程從某個資料庫移至另一個資料庫，請先將資料匯出到檔案。 使用 SQL 查詢來尋找檔案中的資料流程，並使用 [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama)將檔案中的資料複製到 \_ 第二個資料庫之資料流程資料表的資料行。 這可確保每個資料庫都有自己的二進位資料複本。 您無法將二進位資料從某個資料庫移至另一個資料庫，只要使用第一個資料庫的資料提取記錄，然後將它插入第二個資料庫即可。

若要刪除資料流程，請先提取記錄，並將資料行設定為 null，然後再更新記錄。 另一種方法是從資料表中移除記錄，使用 [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify)或一般 SQL 查詢來刪除記錄。 如果資料流程已從資料表中刪除，則不應將資料流程提取到記錄中。

若要重新命名 OLE 資料流程，請更新記錄的 [名稱] 資料行。

如果使用 SQL (ALTER table 來放置此資料表的保留 <table> 保留) 或加入具有保留的資料行，必須使用免費發行資料表。 在資料表發行或認可之前，不會寫入資料流程。

 

 



