---
description: 支援效能計數器的應用程式在服務金鑰下必須有效能金鑰。 下列範例顯示您必須為此索引鍵包含的值。
ms.assetid: b6cdf130-699f-49bd-97b6-a580818b3fab
title: 建立應用程式效能金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d39fb89f7f5feb4e34284b541775b5c093a6bfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983496"
---
# <a name="creating-the-applications-performance-key"></a><span data-ttu-id="a6bb5-104">建立應用程式的效能金鑰</span><span class="sxs-lookup"><span data-stu-id="a6bb5-104">Creating the Application's Performance Key</span></span>

<span data-ttu-id="a6bb5-105">支援效能計數器的應用程式在 **服務** 金鑰下必須有 **效能** 金鑰。</span><span class="sxs-lookup"><span data-stu-id="a6bb5-105">An application that supports performance counters must have a **Performance** key under the **Services** key.</span></span> <span data-ttu-id="a6bb5-106">下列範例顯示您必須為此索引鍵包含的值。</span><span class="sxs-lookup"><span data-stu-id="a6bb5-106">The following example shows the values that you must include for this key.</span></span>

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

<span data-ttu-id="a6bb5-107">連結 **庫** 值提供效能 dll 的名稱，而 **開啟**、 **收集** 和 **關閉** 值則提供從效能 dll 匯出的函式名稱。</span><span class="sxs-lookup"><span data-stu-id="a6bb5-107">The **Library** value provides the name of the performance DLL, and the **Open**, **Collect**, and **Close** values provide the names of the functions exported from the performance DLL.</span></span> <span data-ttu-id="a6bb5-108">這些值的資料類型是 **REG \_ SZ**。</span><span class="sxs-lookup"><span data-stu-id="a6bb5-108">The data type of these values is **REG\_SZ**.</span></span> <span data-ttu-id="a6bb5-109">當取用者要求效能資料時，系統會使用這些值來決定要載入哪些效能 Dll，以及要呼叫哪些 DLL 函數。</span><span class="sxs-lookup"><span data-stu-id="a6bb5-109">When a consumer requests performance data, the system uses these values to determine which performance DLLs to load and which DLL functions to call.</span></span>

<span data-ttu-id="a6bb5-110">連結 **庫** 值可以包含 dll 名稱或 dll 的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="a6bb5-110">The **Library** value can contain the DLL name or a full path to the DLL.</span></span> <span data-ttu-id="a6bb5-111">如果您使用 **REG \_ EXPAND \_ SZ** 資料類型 for **Library**，您可以在路徑中指定環境變數。</span><span class="sxs-lookup"><span data-stu-id="a6bb5-111">If you use the **REG\_EXPAND\_SZ** data type for **Library**, you can specify environment variables in your path.</span></span>

<span data-ttu-id="a6bb5-112">應用程式的服務金鑰必須先存在，您才能執行 **lodctr** 以載入計數器名稱和說明字串。</span><span class="sxs-lookup"><span data-stu-id="a6bb5-112">The application's service key must exist before you can run **lodctr** to load your counter names and help strings.</span></span>

<span data-ttu-id="a6bb5-113">如需您可以建立的其他登錄值（例如指定 [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) 和 [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) 函數的超時值），請參閱 [建立其他登錄專案](creating-other-registry-entries.md)。</span><span class="sxs-lookup"><span data-stu-id="a6bb5-113">For additional registry values that you can create, such as specifying time out values for the [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) and [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) functions, see [Creating Other Registry Entries](creating-other-registry-entries.md).</span></span>

 

 
