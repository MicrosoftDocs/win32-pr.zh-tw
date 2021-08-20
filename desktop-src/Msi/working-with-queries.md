---
description: 因為安裝程式使用關係資料庫，所以有一些函數可讓結構化查詢語言 (SQL)  (SQL) 資料庫的查詢。 下列程式描述如何使用 SQL 來查詢資料庫。
ms.assetid: 1b8fd935-4964-4875-801b-cc6765b16924
title: 使用查詢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b6ea5a2f0b962b195fde531216f4b57fd5834162e31c1e34fc9ff1dd3695df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942123"
---
# <a name="working-with-queries"></a>使用查詢

因為安裝程式使用關係資料庫，所以有一些函數可讓結構化查詢語言 (SQL)  (SQL) 資料庫的查詢。 下列程式描述如何使用 SQL 來查詢資料庫。

**使用 SQL 查詢資料庫**

1.  藉由呼叫 [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa)函數，以適當的 SQL 語句開啟 [**View**](view-object.md)物件。

    [**View**](view-object.md)物件是將查詢套用至一組資料表所建立的邏輯資料表。 SQL 的查詢必須遵守安裝程式所提供的[SQL 語法](sql-syntax.md)。 這個 SQL 語句可以包含在 **View** 物件執行之前未指定的參數標記。

2.  藉由呼叫 [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute)函數來執行 [**View**](view-object.md)物件。
3.  藉由呼叫 [**MsiViewFetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch)函式，從 [**View**](view-object.md)物件取出下一筆記錄。
4.  藉由呼叫 [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify)函數來修改 [**View**](view-object.md)物件。

    您也可以藉由傳遞適當的旗標，以 [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) 驗證資料。 如果 **MsiViewModify** \_ 從驗證要求傳回錯誤的 \_ 資料無效，則基礎資料已損毀。

5.  藉由呼叫 [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)函數，取得 [**View**](view-object.md)物件的詳細錯誤資訊。
6.  藉由呼叫 [**MsiViewClose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose)函數來關閉 [**View**](view-object.md)物件。

如需詳細資訊，請參閱[使用 SQL 和腳本的資料庫查詢範例](examples-of-database-queries-using-sql-and-script.md)。

 

 



