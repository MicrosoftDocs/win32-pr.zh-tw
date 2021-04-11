---
description: 效能 Dll OpenPerformanceData 函式會接受字串引數做為輸入。
ms.assetid: 8ec0ea45-5789-4801-b486-555779a7303e
title: 正在建立其他登錄專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dfc3b46ce642069210df5112eb41cac9a038797
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944263"
---
# <a name="creating-other-registry-entries"></a><span data-ttu-id="a8cc6-103">正在建立其他登錄專案</span><span class="sxs-lookup"><span data-stu-id="a8cc6-103">Creating Other Registry Entries</span></span>

<span data-ttu-id="a8cc6-104">效能 DLL 的 [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) 函式會接受字串引數做為輸入。</span><span class="sxs-lookup"><span data-stu-id="a8cc6-104">The performance DLL's [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) function takes a string argument as input.</span></span> <span data-ttu-id="a8cc6-105">若要提供開啟函式的輸入字串，請在您的 **服務** 索引鍵下包含 **連結** 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a8cc6-105">To provide an input string to your open function, include a **Linkage** key under your **Services** key.</span></span> <span data-ttu-id="a8cc6-106">**連結** 索引鍵包含 **匯出** 值。</span><span class="sxs-lookup"><span data-stu-id="a8cc6-106">The **Linkage** key contains an **Export** value.</span></span> <span data-ttu-id="a8cc6-107">將 **匯出** 的值資料設定為您要傳遞至開啟函式的輸入字串。</span><span class="sxs-lookup"><span data-stu-id="a8cc6-107">Set the value data for **Export** to the input string that you want to pass to your open function.</span></span> <span data-ttu-id="a8cc6-108">**匯出** 的資料類型為 **REG \_ 多重 \_ SZ**。</span><span class="sxs-lookup"><span data-stu-id="a8cc6-108">The data type of **Export** is **REG\_MULTI\_SZ**.</span></span>

<span data-ttu-id="a8cc6-109">如果未定義 **匯出** (**匯出** 是選擇性的) ，則系統會將 **Null** 傳遞給您的 [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="a8cc6-109">If **Export** is not defined (**Export** is optional), the system passes **NULL** to your [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) function.</span></span>

<span data-ttu-id="a8cc6-110">一般而言，如果有多個應用程式共用相同的效能 DLL，則每個應用程式都會包含 **連結** 索引鍵和 **匯出** 值，以提供內容給呼叫 DLL 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a8cc6-110">Typically, if more than one application shares the same performance DLL, each application includes a **Linkage** key and **Export** value to provide context as to which application is calling the DLL.</span></span>

<span data-ttu-id="a8cc6-111">以下顯示登錄專案：</span><span class="sxs-lookup"><span data-stu-id="a8cc6-111">The following shows the registry entries:</span></span>

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

<span data-ttu-id="a8cc6-112">根據預設，效能 DLL 的 [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) 和 [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) 函數必須在10000毫秒內傳回。</span><span class="sxs-lookup"><span data-stu-id="a8cc6-112">By default, the performance DLL's [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) and [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) functions must return within 10,000 milliseconds.</span></span> <span data-ttu-id="a8cc6-113">如果沒有，系統就不會使用 DLL 傳回的資料。</span><span class="sxs-lookup"><span data-stu-id="a8cc6-113">If not, the system does not use the data that the DLL returns.</span></span> <span data-ttu-id="a8cc6-114">應用程式可以藉由指定 **開啟的超時時間** 或 **收集 timeout** 登錄值（如下列範例所示 ），來增加或減少超時值。</span><span class="sxs-lookup"><span data-stu-id="a8cc6-114">The application can increase or decrease the timeout value by specifying an **Open Timeout** or **Collect Timeout** registry value under their **Performance** key as shown in the following example.</span></span>

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

<span data-ttu-id="a8cc6-115">若要取得某些應用程式的效能資料 (使用 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函式) 傳回計數器的應用程式，則必須使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函數來開啟與應用程式相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="a8cc6-115">To obtain the performance data for some applications (those that return counters using the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function), it is necessary to use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open the device associated with the application.</span></span> <span data-ttu-id="a8cc6-116">在此情況下， **CreateFile** 中指定的名稱也必須安裝在登錄的 DOS 裝置節點中，如下所示：</span><span class="sxs-lookup"><span data-stu-id="a8cc6-116">In this case, the name specified in **CreateFile** must also be installed in the DOS Devices node of the registry, as shown here:</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \Session Manager
               \DOS Devices
```

 

 
