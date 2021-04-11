---
description: 效能計數器類型會指定取得計算的效能計數器所需的公式。 這些是 Windows 效能監視所使用的相同計數器類型。
ms.assetid: d4a9feca-80a2-4ce5-b4d7-4e83ef951c08
ms.tgt_platform: multiple
title: WMI 效能計數器類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ac0d2c8afb1499fec44c983364b5e3278b864
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115032"
---
# <a name="wmi-performance-counter-types"></a><span data-ttu-id="31d5c-104">WMI 效能計數器類型</span><span class="sxs-lookup"><span data-stu-id="31d5c-104">WMI Performance Counter Types</span></span>

<span data-ttu-id="31d5c-105">性能 [計數器類型](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) 會指定取得計算的效能計數器所需的公式。</span><span class="sxs-lookup"><span data-stu-id="31d5c-105">The performance [counter type](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) designates a formula required to obtain calculated performance counters.</span></span> <span data-ttu-id="31d5c-106">這些是 Windows [效能監視](/windows/desktop/PerfCtrs/performance-counters-portal)所使用的相同計數器類型。</span><span class="sxs-lookup"><span data-stu-id="31d5c-106">These are the same counter types used by Windows [Performance Monitoring](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span> <span data-ttu-id="31d5c-107">在 WMI 效能類別中，計數器類型公式的原始資料來自 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 類別，而且計算結果是在對應 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) 類別的相同名稱屬性中找到。</span><span class="sxs-lookup"><span data-stu-id="31d5c-107">In WMI performance classes, the raw data for the counter type formula comes from a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class and the calculated result is found in the same-named property of a corresponding [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) class.</span></span>

<span data-ttu-id="31d5c-108">計數器類型會顯示為 [**win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)類別中屬性的 **CounterType** 限定詞，以及 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)類別中屬性的 **CookingType** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="31d5c-108">Counter types appear as the **CounterType** qualifier for properties in [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes, and as the **CookingType** qualifier for properties in [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes.</span></span>

<span data-ttu-id="31d5c-109">例如， [**win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md)類別中的 **AvgDiskBytesPerRead** 屬性是 class [**Win32 \_ AvgDiskBytesPerRead \_ PerfFormattedData \_ PerfDisk**](./retrieving-raw-and-formatted-performance-data.md)中 **LogicalDisk** 屬性的原始資料來源，其中包含與系統監視器中所顯示相同的資料。</span><span class="sxs-lookup"><span data-stu-id="31d5c-109">For example, the **AvgDiskBytesPerRead** property in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class is the raw data source for the **AvgDiskBytesPerRead** property in the class [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), which contains the same data as shown in System Monitor.</span></span>

<span data-ttu-id="31d5c-110">下列清單依功能類型組織計數器類型描述：</span><span class="sxs-lookup"><span data-stu-id="31d5c-110">The following list organizes counter type descriptions by functional type:</span></span>

-   [<span data-ttu-id="31d5c-111">基底計數器類型</span><span class="sxs-lookup"><span data-stu-id="31d5c-111">Base Counter Types</span></span>](base-counter-types.md)
-   [<span data-ttu-id="31d5c-112">基本演算法計數器類型</span><span class="sxs-lookup"><span data-stu-id="31d5c-112">Basic Algorithm Counter Types</span></span>](basic-algorithm-counter-types.md)
-   [<span data-ttu-id="31d5c-113">計數器演算法計數器類型</span><span class="sxs-lookup"><span data-stu-id="31d5c-113">Counter Algorithm Counter Types</span></span>](counter-algorithm-counter-types.md)
-   [<span data-ttu-id="31d5c-114">Noncomputational 計數器類型</span><span class="sxs-lookup"><span data-stu-id="31d5c-114">Noncomputational Counter Types</span></span>](noncomputational-counter-types.md)
-   [<span data-ttu-id="31d5c-115">精確度計時器演算法計數器類型</span><span class="sxs-lookup"><span data-stu-id="31d5c-115">Precision Timer Algorithm Counter Types</span></span>](precision-timer-algorithm-counter-types.md)
-   [<span data-ttu-id="31d5c-116">佇列長度演算法計數器類型</span><span class="sxs-lookup"><span data-stu-id="31d5c-116">Queue-length Algorithm Counter Types</span></span>](queue-length-algorithm-counter-types.md)
-   [<span data-ttu-id="31d5c-117">統計計數器類型</span><span class="sxs-lookup"><span data-stu-id="31d5c-117">Statistical Counter Types</span></span>](statistical-counter-types.md)
-   [<span data-ttu-id="31d5c-118">計時器演算法計數器類型</span><span class="sxs-lookup"><span data-stu-id="31d5c-118">Timer Algorithm Counter Types</span></span>](timer-algorithm-counter-types.md)

 

 
