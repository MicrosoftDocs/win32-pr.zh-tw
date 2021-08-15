---
description: 效能 Dll OpenPerformanceData 函式會接受字串引數做為輸入。
ms.assetid: 8ec0ea45-5789-4801-b486-555779a7303e
title: 正在建立其他登錄專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ad9fe960713a481ba5a9b8f4b73e11bdbdd4d9fe9474b04b994e373ce8e1bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683968"
---
# <a name="creating-other-registry-entries"></a>正在建立其他登錄專案

效能 DLL 的 [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) 函式會接受字串引數做為輸入。 若要提供開啟函式的輸入字串，請在您的 **服務** 索引鍵下包含 **連結** 索引鍵。 **連結** 索引鍵包含 **匯出** 值。 將 **匯出** 的值資料設定為您要傳遞至開啟函式的輸入字串。 **匯出** 的資料類型為 **REG \_ 多重 \_ SZ**。

如果未定義 **匯出** (**匯出** 是選擇性的) ，則系統會將 **Null** 傳遞給您的 [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) 函數。

一般而言，如果有多個應用程式共用相同的效能 DLL，則每個應用程式都會包含 **連結** 索引鍵和 **匯出** 值，以提供內容給呼叫 DLL 的應用程式。

以下顯示登錄專案：

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name-1
               \Linkage
                  Export = app-1 context strings
               \Performance
                  Library = perfctrs.dll
            \application-name-2
               \Linkage
                  Export = app-2 context strings
               \Performance
                  Library = perfctrs.dll
```

根據預設，效能 DLL 的 [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) 和 [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) 函數必須在10000毫秒內傳回。 如果沒有，系統就不會使用 DLL 傳回的資料。 應用程式可以藉由指定 **開啟的超時時間** 或 **收集 timeout** 登錄值（如下列範例所示 ），來增加或減少超時值。

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name
               \Performance
                  Open Timeout = Timeout value for your open function, in milliseconds
                  Collect Timeout = Timeout value for your collect function, in milliseconds
```

若要取得某些應用程式的效能資料 (使用 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函式) 傳回計數器的應用程式，則必須使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函數來開啟與應用程式相關聯的裝置。 在此情況下， **CreateFile** 中指定的名稱也必須安裝在登錄的 DOS 裝置節點中，如下所示：

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \Session Manager
               \DOS Devices
```

 

 
