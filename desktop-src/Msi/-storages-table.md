---
description: '[ \_ 儲存體] 資料表會列出內嵌的 OLE 資料儲存體。 這是臨時表，只有在 SQL 語句參考時才會建立。'
ms.assetid: b2f2907d-6966-4b63-9589-c1580f8db574
title: _Storages 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27995dd61c7d25100fc0e1ae2297695e361f44f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849006"
---
# <a name="_storages-table"></a>\_儲存體資料表

[ \_ 儲存體] 資料表會列出內嵌的 OLE 資料儲存體。 這是臨時表，只有在 SQL 語句參考時才會建立。



| Column | 類型                 | 答案 | Nullable |
|--------|----------------------|-----|----------|
| Name   | [Text](text.md)     | Y   | N        |
| 資料   | [二進位](binary.md) | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>名字
</dt> <dd>

識別儲存體的唯一索引鍵。 名稱的長度上限是31個字元。

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>資料
</dt> <dd>

未格式化的二進位資料。

</dd> </dl>

## <a name="remarks"></a>備註

若要將 OLE 儲存體加入至資料庫，請在 [儲存體] 資料表中建立新記錄，並在 [名稱] 資料 \_ 行中輸入儲存體的名稱。 使用 [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) 將資料複製到此記錄的資料行。 最後，使用 [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) 將記錄插入至 [ \_ 儲存體] 資料表。

無法從儲存體資料表讀取資料 \_ 。 不過，您 \_ 可以查詢儲存體資料表來檢查特定儲存體是否存在。 這表示，您無法將 OLE 儲存體從某個資料庫移至另一個資料庫。 您必須改為將原始儲存體檔案匯入至新的資料庫。若要刪除 OLE 儲存區，請提取包含二進位資料的記錄，將儲存資料表中的資料行設定 \_ 為 null，然後更新記錄。 替代方法是只使用 [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) 或一般 SQL 查詢來刪除記錄。

若要重新命名 OLE 儲存區，請更新記錄的名稱資料行。

如果使用 SQL (ALTER TABLE 將保留放在此資料表上 <table> 保留) 或加入具有保留的資料行，必須使用免費發行資料表。 在資料表發行或認可之前，不會寫入儲存體。

 

 



