---
description: 若要使用計數器資料，請參閱使用計數器資料。
ms.assetid: fff8bc4a-3d7a-4d70-ba03-347f9f063c84
title: 使用效能計數器
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: abc055a34f0937e056d1d983354fc0a3edf182a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971796"
---
# <a name="using-performance-counters"></a><span data-ttu-id="d1696-103">使用效能計數器</span><span class="sxs-lookup"><span data-stu-id="d1696-103">Using Performance Counters</span></span>

<span data-ttu-id="d1696-104">效能計數器取用 **者** 是收集和利用效能計數器資料的軟體元件。</span><span class="sxs-lookup"><span data-stu-id="d1696-104">Performance counter **consumers** are software components that collect and make use of performance counter data.</span></span> <span data-ttu-id="d1696-105">Microsoft 提供的範例取用者包括效能監視器 (perfmon.exe) 、資源監視器 (resmon.exe) 、記錄管理員 (logman.exe) 和 typeperf.exe。</span><span class="sxs-lookup"><span data-stu-id="d1696-105">Example consumers provided by Microsoft include Performance Monitor (perfmon.exe), Resource Monitor (resmon.exe), Log Manager (logman.exe) and typeperf.exe.</span></span> <span data-ttu-id="d1696-106">協力廠商軟體元件也可以透過效能集合 Api 或 WMI 效能計數器類別收集效能資料。</span><span class="sxs-lookup"><span data-stu-id="d1696-106">Third-party software components may also collect performance data via performance collection APIs or via WMI performance counter classes.</span></span>

<span data-ttu-id="d1696-107">效能計數器 **提供者** 是發佈效能計數器資料的軟體元件。</span><span class="sxs-lookup"><span data-stu-id="d1696-107">Performance counter **providers** are software components that publish performance counter data.</span></span> <span data-ttu-id="d1696-108">效能計數器可以由作業系統元件、設備磁碟機和服務提供。</span><span class="sxs-lookup"><span data-stu-id="d1696-108">Performance counters can be provided by operating system components, device drivers, and services.</span></span> <span data-ttu-id="d1696-109">許多效能計數器都會提供作為 Windows 作業系統的一部分。</span><span class="sxs-lookup"><span data-stu-id="d1696-109">Many performance counters are provided as part of the Windows operating system.</span></span> <span data-ttu-id="d1696-110">協力廠商軟體元件可能會透過效能計數器提供者 Api 提供額外的計數器。</span><span class="sxs-lookup"><span data-stu-id="d1696-110">Additional counters may be provided by third-party software components via the performance counter provider APIs.</span></span>

- <span data-ttu-id="d1696-111">當您想要從系統收集或查看計數器資料時，請使用 [效能計數器工具](performance-counters-tools.md) 。</span><span class="sxs-lookup"><span data-stu-id="d1696-111">Use [Performance Counter Tools](performance-counters-tools.md) when you want to collect or view the counter data from a system.</span></span>
- <span data-ttu-id="d1696-112">當您想要撰寫可從本機系統收集計數器資料的程式時，請使用 [效能計數器取用者 api](consuming-counter-data.md) 。</span><span class="sxs-lookup"><span data-stu-id="d1696-112">Use [Performance Counter Consumer APIs](consuming-counter-data.md) when you want to write a program that collects counter data from the local system.</span></span>
- <span data-ttu-id="d1696-113">當您想要使用 WMI 從本機或遠端系統收集計數器資料時，請使用 [Wmi 效能計數器類別](/windows/desktop/WmiSdk/monitoring-performance-data) 。</span><span class="sxs-lookup"><span data-stu-id="d1696-113">Use [WMI Performance Counter Classes](/windows/desktop/WmiSdk/monitoring-performance-data) when you want to collect counter data from a local or remote system using WMI.</span></span>
- <span data-ttu-id="d1696-114">當您想要從軟體元件發佈效能計數器資料時，請使用 [效能計數器提供者 api](providing-counter-data.md) 。</span><span class="sxs-lookup"><span data-stu-id="d1696-114">Use [Performance Counter Provider APIs](providing-counter-data.md) when you want to publish performance counter data from your software component.</span></span>

## <a name="see-also"></a><span data-ttu-id="d1696-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1696-115">See also</span></span>

[<span data-ttu-id="d1696-116">關於效能計數器</span><span class="sxs-lookup"><span data-stu-id="d1696-116">About Performance Counters</span></span>](about-performance-counters.md)

[<span data-ttu-id="d1696-117">效能計數器參考</span><span class="sxs-lookup"><span data-stu-id="d1696-117">Performance Counters Reference</span></span>](performance-counters-reference.md)
