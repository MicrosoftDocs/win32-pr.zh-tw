---
description: RegQueryValueEx 函式所抓取資料的格式是以固定長度的標頭結構（效能 \_ 資料區塊）開始 \_ 。
ms.assetid: a68fa617-834c-4ad9-b922-fac3a648ad75
title: 效能資料格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88029634594843a50fd6010993eb6517dce831f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570643"
---
# <a name="performance-data-format"></a><span data-ttu-id="d2cf6-103">效能資料格式</span><span class="sxs-lookup"><span data-stu-id="d2cf6-103">Performance Data Format</span></span>

<span data-ttu-id="d2cf6-104">[**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa)函式所抓取資料的格式是以固定長度的標頭結構（效能 [**\_ 資料 \_ 區塊**](/windows/desktop/api/Winperf/ns-winperf-perf_data_block)）開始。</span><span class="sxs-lookup"><span data-stu-id="d2cf6-104">The format of the data retrieved by the [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) function begins with a fixed-length header structure, [**PERF\_DATA\_BLOCK**](/windows/desktop/api/Winperf/ns-winperf-perf_data_block).</span></span> <span data-ttu-id="d2cf6-105">效能 **\_ 資料 \_ 區塊** 結構描述系統和效能資料。</span><span class="sxs-lookup"><span data-stu-id="d2cf6-105">The **PERF\_DATA\_BLOCK** structure describes the system and the performance data.</span></span> <span data-ttu-id="d2cf6-106">效能 **\_ 資料 \_ 區塊** 結構後面會加上可變長度的可變長度物件資料項目。</span><span class="sxs-lookup"><span data-stu-id="d2cf6-106">The **PERF\_DATA\_BLOCK** structure is followed by variable number of variable-length object data items.</span></span> <span data-ttu-id="d2cf6-107">每個物件專案的標頭包含清單中下一個物件專案的位移。</span><span class="sxs-lookup"><span data-stu-id="d2cf6-107">The header of each object item contains the offset of the next object item in the list.</span></span> <span data-ttu-id="d2cf6-108">下圖顯示基本效能資料結構。</span><span class="sxs-lookup"><span data-stu-id="d2cf6-108">The following diagram shows the basic performance data structure.</span></span>

![效能資料結構](images/perfdata.png)

<span data-ttu-id="d2cf6-110">物件資料項目有兩種格式：一個支援多個實例，另一個則不支援多個實例。</span><span class="sxs-lookup"><span data-stu-id="d2cf6-110">There are two formats for the object data items: one that supports multiple instances, and the other that does not support multiple instances.</span></span>

<span data-ttu-id="d2cf6-111">每個物件資料項目區塊都包含一個效能 [**\_ 物件 \_ 類型**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type) 結構，描述物件的效能資料。</span><span class="sxs-lookup"><span data-stu-id="d2cf6-111">Each object data item block contains a [**PERF\_OBJECT\_TYPE**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type) structure, which describes the performance data for the object.</span></span> <span data-ttu-id="d2cf6-112">**性能 \_ 物件 \_ 類型** 結構後面接著 [**性能 \_ 計數器 \_ 定義**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition)結構的清單，為物件定義的每個計數器各一個。</span><span class="sxs-lookup"><span data-stu-id="d2cf6-112">The **PERF\_OBJECT\_TYPE** structure is followed by a list of [**PERF\_COUNTER\_DEFINITION**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) structures, one for each counter defined for the object.</span></span> <span data-ttu-id="d2cf6-113">對於只有一個實例的物件， **性能 \_ 計數器 \_ 定義** 結構的清單後面會接著一個 [**性能 \_ 計數器 \_ 區塊**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block) 結構，後面接著計數器資料。</span><span class="sxs-lookup"><span data-stu-id="d2cf6-113">For an object with only one instance, the list of **PERF\_COUNTER\_DEFINITION** structures is followed by a single [**PERF\_COUNTER\_BLOCK**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block) structure, followed by the counter data.</span></span> <span data-ttu-id="d2cf6-114">每個 **性能 \_ 計數器 \_ 定義** 結構都包含從 **性能 \_ 計數器 \_ 區塊** 結構開始到對應計數器資料的位移。</span><span class="sxs-lookup"><span data-stu-id="d2cf6-114">Each **PERF\_COUNTER\_DEFINITION** structure contains the offset from the start of the **PERF\_COUNTER\_BLOCK** structure to the corresponding counter data.</span></span> <span data-ttu-id="d2cf6-115">下圖顯示不支援多個實例的效能物件結構。</span><span class="sxs-lookup"><span data-stu-id="d2cf6-115">The following diagram shows the structure of a performance object that does not support multiple instances.</span></span>

![不支援多個實例的效能物件結構](images/perfnoinst.png)

<span data-ttu-id="d2cf6-117">針對支援多個實例的物件類型， [**性能 \_ 計數器 \_ 定義**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) 結構的清單後面會接著實例資訊區塊的清單， (每個實例) 一個。</span><span class="sxs-lookup"><span data-stu-id="d2cf6-117">For an object type that supports multiple instances, the list of [**PERF\_COUNTER\_DEFINITION**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) structures is followed by a list of instance information blocks (one for each instance).</span></span> <span data-ttu-id="d2cf6-118">每個實例資訊區塊都包含一個效能 [**\_ 實例 \_ 定義**](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition) 結構、實例的名稱，以及一個 [**性能 \_ 計數器 \_ 區塊**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block) 結構。</span><span class="sxs-lookup"><span data-stu-id="d2cf6-118">Each instance information block contains a [**PERF\_INSTANCE\_DEFINITION**](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition) structure, the name of the instance, and a [**PERF\_COUNTER\_BLOCK**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block) structure.</span></span> <span data-ttu-id="d2cf6-119">下圖顯示支援兩個實例的效能物件結構。</span><span class="sxs-lookup"><span data-stu-id="d2cf6-119">The following diagram shows the structure of a performance object that supports two instances.</span></span>

![支援兩個實例的效能物件結構](images/perfinst.png)

<span data-ttu-id="d2cf6-121">如需使用位移的範例，請參閱 [顯示物件、實例和計數器名稱](displaying-object-instance-and-counter-names.md)。</span><span class="sxs-lookup"><span data-stu-id="d2cf6-121">For an example that uses the offsets, see [Displaying Object, Instance, and Counter Names](displaying-object-instance-and-counter-names.md).</span></span>

 

 
