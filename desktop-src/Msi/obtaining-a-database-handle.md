---
description: 使用資料庫之前，您必須先取得其控制碼。
ms.assetid: 53cf73bc-4d52-471c-8384-46d106a36e38
title: 取得資料庫控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec5f37f1abd329d0c51b00839d43ef85784fdad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114324"
---
# <a name="obtaining-a-database-handle"></a>取得資料庫控制碼

使用資料庫之前，您必須先取得其控制碼。

**存取安裝程式資料庫的相關資訊**

1.  以下列兩種方式之一取得資料庫的控制碼：
    -   如果安裝正在進行中，請呼叫 [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase) 函數來取得使用中資料庫的控制碼。
    -   如果安裝不在進行中，請呼叫 [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) 函數來開啟任何指定的資料庫。
2.  開啟資料庫之後，您可以呼叫函式來取得資料庫的相關資訊，或運算元據庫。
    -   藉由呼叫 [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa)函數，建立 **View** 物件並指定開放式資料庫的 SQL 查詢。
    -   藉由呼叫 [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) 函數，取得包含開啟資料庫中之指定資料表之所有主鍵的記錄。
    -   藉由呼叫 [**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate) 函數，檢查開啟資料庫的目前狀態。 您可以使用 **MsiGetDatabaseState** 函式來判斷資料庫的讀取/寫入狀態，或是控制碼是否有效。

 

 



