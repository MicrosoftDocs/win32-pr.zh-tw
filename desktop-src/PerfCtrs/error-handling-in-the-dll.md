---
description: 使用事件記錄來記錄效能 DLL 中發生的錯誤。
ms.assetid: 61bc4fa1-8185-4e07-a3b5-4bd357f0f75a
title: DLL 中的錯誤處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a64dcfdf360a1dcc2301b5496d3f4630631cd7bfbc3fffb0e2cd5408120351
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517468"
---
# <a name="error-handling-in-the-dll"></a>DLL 中的錯誤處理

使用事件記錄來記錄效能 DLL 中發生的錯誤。 記錄錯誤事件有助於針對在開發期間和安裝之後提供效能資料的應用程式進行疑難排解。 您應該限制 [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) 函式中發生的錯誤記錄量，因為資料收集可能很頻繁。

如果 [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) 函數發生問題，系統會將下列錯誤記錄到事件記錄檔。 如果發生下列其中一個錯誤，系統就不會再次呼叫效能 DLL。 相反地，DLL 已卸載。

-   **PERFLIB \_找 \_ \_ 不 \_ 到開啟** 的程式—當 DLL 中定義的程式名稱在 DLL 中找不到匯出的函式時，就會進行記錄。 當 DLL 或服務未正確安裝，或函式名稱已重新命名而未更新安裝程式時，通常就會發生這種情況。
-   **PERFLIB \_開啟 \_ 程式 \_ 失敗**：當 OPEN 程式傳回錯誤狀態，而不是錯誤成功時所記錄 \_ 。 如果發生這種情況，DLL 應該也輸入一個事件記錄檔專案，以描述造成失敗的狀況。
-   **PERFLIB \_OPEN \_ procedure \_ 例外** 狀況—在 open 程式遇到未處理的例外狀況時記錄。 這通常是因為 open 程式發生非預期的錯誤狀況。

 

 
