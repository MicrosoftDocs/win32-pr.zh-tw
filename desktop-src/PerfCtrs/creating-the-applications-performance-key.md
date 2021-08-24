---
description: 支援效能計數器的應用程式在服務金鑰下必須有效能金鑰。 下列範例顯示您必須為此索引鍵包含的值。
ms.assetid: b6cdf130-699f-49bd-97b6-a580818b3fab
title: 建立應用程式效能金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c149e8142b892edeb43f5459fe68bc6ad4b7453118c64cb2e288bb334c054fff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144031"
---
# <a name="creating-the-applications-performance-key"></a>建立應用程式的效能金鑰

支援效能計數器的應用程式在 **服務** 金鑰下必須有 **效能** 金鑰。 下列範例顯示您必須為此索引鍵包含的值。

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name
               \Performance
                  Library = Name of your performance DLL
                  Open = Name of your Open function in your DLL
                  Collect = Name of your Collect function in your DLL
                  Close = Name of your Close function in your DLL
```

連結 **庫** 值提供效能 dll 的名稱，而 **開啟**、 **收集** 和 **關閉** 值則提供從效能 dll 匯出的函式名稱。 這些值的資料類型是 **REG \_ SZ**。 當取用者要求效能資料時，系統會使用這些值來決定要載入哪些效能 Dll，以及要呼叫哪些 DLL 函數。

連結 **庫** 值可以包含 dll 名稱或 dll 的完整路徑。 如果您使用 **REG \_ EXPAND \_ SZ** 資料類型 for **Library**，您可以在路徑中指定環境變數。

應用程式的服務金鑰必須先存在，您才能執行 **lodctr** 以載入計數器名稱和說明字串。

如需您可以建立的其他登錄值（例如指定 [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) 和 [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) 函數的超時值），請參閱 [建立其他登錄專案](creating-other-registry-entries.md)。

 

 
