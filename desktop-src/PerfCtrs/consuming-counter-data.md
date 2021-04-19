---
description: 您可以使用下列其中一個介面來取用效能資料：效能資料協助程式 (PDH) 介面，此介面可提供第1版和第2版效能計數器提供者之資料的高階存取權。登錄介面，可為效能計數器提供者的資料提供低層級的存取權。效能程式庫介面，可直接存取第2版效能計數器提供者的資料。PDH 介面比登錄介面更容易使用，建議用於大部分的效能資料收集工作。 PDH 介面基本上是登錄介面所提供功能的較高層級抽象概念。 只有當您無法使用 PDH 抽象層函式時，才能使用 [效能程式庫] 介面。
ms.assetid: a42f6cdd-47e9-4f43-aeaf-37a5abb0fa36
title: 使用計數器資料
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: c8c50b29d8f898f544b021f7fe3f3fd0d4a2094e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982425"
---
# <a name="consuming-counter-data"></a><span data-ttu-id="4dadf-105">使用計數器資料</span><span class="sxs-lookup"><span data-stu-id="4dadf-105">Consuming Counter Data</span></span>

<span data-ttu-id="4dadf-106">想要讀取及使用 Windows 效能計數器資料的程式，可以使用適用于此案例的數個介面之一。</span><span class="sxs-lookup"><span data-stu-id="4dadf-106">Programs that want to read and make use of Windows Performance Counter data can use one of several interfaces as appropriate for the scenario.</span></span>

- <span data-ttu-id="4dadf-107">腳本可以使用 [WMI 效能計數器類別](/windows/desktop/WmiSdk/monitoring-performance-data) 或 [TypePerf](/windows-server/administration/windows-commands/typeperf) 工具。</span><span class="sxs-lookup"><span data-stu-id="4dadf-107">Scripts can use the [WMI Performance Counter Classes](/windows/desktop/WmiSdk/monitoring-performance-data) or the [TypePerf](/windows-server/administration/windows-commands/typeperf) tool.</span></span>
- <span data-ttu-id="4dadf-108">.NET 程式可以使用 [PerformanceCounter 類別](/dotnet/api/system.diagnostics.performancecounter)。</span><span class="sxs-lookup"><span data-stu-id="4dadf-108">.NET programs can use the [PerformanceCounter Class](/dotnet/api/system.diagnostics.performancecounter).</span></span>
- <span data-ttu-id="4dadf-109">[效能資料協助程式 (PDH) 程式庫](using-the-pdh-functions-to-consume-counter-data.md)可透過 Win32 (C/c + +) API，提供 V1 和 V2 效能計數器提供者的資料高階存取權。</span><span class="sxs-lookup"><span data-stu-id="4dadf-109">The [Performance Data Helper (PDH) library](using-the-pdh-functions-to-consume-counter-data.md) provides high-level access to data from both V1 and V2 performance counter providers via a Win32 (C/C++) API.</span></span>
- <span data-ttu-id="4dadf-110">登錄 [介面](using-the-registry-functions-to-consume-counter-data.md) 可讓您透過特殊登錄機碼來存取 V1 和 V2 效能計數器提供者的資料 `HKEY_PERFORMANCE_DATA` 。</span><span class="sxs-lookup"><span data-stu-id="4dadf-110">The [registry interface](using-the-registry-functions-to-consume-counter-data.md) provides access to data from both V1 and V2 performance counter providers via the special `HKEY_PERFORMANCE_DATA` registry key.</span></span>
- <span data-ttu-id="4dadf-111">[PerfLib v2 取用者](using-the-perflib-functions-to-consume-counter-data.md)函式可透過 Win32 (C/c + +) API，從 V2 效能計數器提供者提供低層級的資料存取。</span><span class="sxs-lookup"><span data-stu-id="4dadf-111">The [PerfLib V2 Consumer functions](using-the-perflib-functions-to-consume-counter-data.md) provide low-level access to data from V2 performance counter providers via a Win32 (C/C++) API.</span></span>

<span data-ttu-id="4dadf-112">建議使用 PDH 介面進行大部分的 C/c + + 效能資料收集工作，因為它比登錄和 PerfLib 介面更容易使用。</span><span class="sxs-lookup"><span data-stu-id="4dadf-112">The PDH interface is recommended for most C/C++ performance data collection tasks because it is easier to use than the registry and PerfLib interfaces.</span></span>
