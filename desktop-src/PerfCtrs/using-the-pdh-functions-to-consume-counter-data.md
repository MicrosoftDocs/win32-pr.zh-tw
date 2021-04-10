---
description: 您可以使用 PDH 函數來收集效能資料。
ms.assetid: 2510480e-cfea-4f7c-af0b-6d229c150c91
title: 使用 PDH 函數來使用計數器資料
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 431bf160ef6ca54b4a37363d7fe6ed48bb25d953
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849276"
---
# <a name="using-the-pdh-functions-to-consume-counter-data"></a><span data-ttu-id="ce846-103">使用 PDH 函數來使用計數器資料</span><span class="sxs-lookup"><span data-stu-id="ce846-103">Using the PDH Functions to Consume Counter Data</span></span>

<span data-ttu-id="ce846-104">使用 PDH 函數收集效能資料。</span><span class="sxs-lookup"><span data-stu-id="ce846-104">Use the PDH functions to collect performance data.</span></span> <span data-ttu-id="ce846-105">PDH 函數比登錄 [功能](using-the-registry-functions-to-consume-counter-data.md) 更容易使用，而且可用來存取 V1 和 V2 提供者的計數器資料。</span><span class="sxs-lookup"><span data-stu-id="ce846-105">The PDH functions are easier to use than the [registry functions](using-the-registry-functions-to-consume-counter-data.md) and can be used to access counter data both V1 and V2 providers.</span></span> <span data-ttu-id="ce846-106">PDH 有 Api 可收集目前的效能資料、將效能資料儲存至記錄檔，以及從記錄檔讀取資料。</span><span class="sxs-lookup"><span data-stu-id="ce846-106">PDH has APIs for collecting current performance data, saving performance data to log files, and reading data from log files.</span></span>

> [!Note]
> <span data-ttu-id="ce846-107">如果您要撰寫 Windows OneCore 的應用程式，則無法使用效能資料協助程式抽象層函式。</span><span class="sxs-lookup"><span data-stu-id="ce846-107">You cannot use the Performance Data Helper abstraction-layer functions if you are writing Windows OneCore apps.</span></span> <span data-ttu-id="ce846-108">相反地，請使用 [PerfLib V2 取用者](using-the-perflib-functions-to-consume-counter-data.md)函式。</span><span class="sxs-lookup"><span data-stu-id="ce846-108">Instead, use [PerfLib V2 Consumer functions](using-the-perflib-functions-to-consume-counter-data.md).</span></span>

<span data-ttu-id="ce846-109">PDH 是高階 API，可簡化收集效能計數器資料的工作。</span><span class="sxs-lookup"><span data-stu-id="ce846-109">PDH is a high-level API that simplifies collecting performance counter data.</span></span> <span data-ttu-id="ce846-110">它有助於查詢剖析、中繼資料快取、比對樣本之間的實例、計算原始值的格式化值、從記錄檔讀取資料，以及將資料儲存至記錄檔。</span><span class="sxs-lookup"><span data-stu-id="ce846-110">It helps with query parsing, metadata caching, matching up instances between samples, computing formatted values from raw values, reading data from log files, and saving data to log files.</span></span> <span data-ttu-id="ce846-111">當從 **V1 提供者** 收集資料時，PDH 會自動使用登錄 [功能](using-the-registry-functions-to-consume-counter-data.md)，並在從 **v2 提供** 者收集資料時使用 [v2 取用者](using-the-perflib-functions-to-consume-counter-data.md)函式。</span><span class="sxs-lookup"><span data-stu-id="ce846-111">PDH automatically uses the [registry functions](using-the-registry-functions-to-consume-counter-data.md) when collecting data from **V1 providers** and it uses the [V2 Consumer functions](using-the-perflib-functions-to-consume-counter-data.md) when collecting data from **V2 providers**.</span></span>

<span data-ttu-id="ce846-112">若要使用 PDH 函數收集效能資料，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="ce846-112">To collect performance data using the PDH functions, perform the following steps.</span></span>

1. [<span data-ttu-id="ce846-113">建立查詢</span><span class="sxs-lookup"><span data-stu-id="ce846-113">Create a query</span></span>](creating-a-query.md)
2. [<span data-ttu-id="ce846-114">將計數器新增至查詢</span><span class="sxs-lookup"><span data-stu-id="ce846-114">Add counters to the query</span></span>](creating-a-query.md)
3. [<span data-ttu-id="ce846-115">收集效能資料</span><span class="sxs-lookup"><span data-stu-id="ce846-115">Collect the performance data</span></span>](collecting-performance-data.md)
4. [<span data-ttu-id="ce846-116">顯示效能資料</span><span class="sxs-lookup"><span data-stu-id="ce846-116">Display the performance data</span></span>](displaying-performance-data.md)
5. [<span data-ttu-id="ce846-117">關閉查詢</span><span class="sxs-lookup"><span data-stu-id="ce846-117">Close the query</span></span>](creating-a-query.md)

<span data-ttu-id="ce846-118">您可以從即時來源或記錄檔收集效能資料。</span><span class="sxs-lookup"><span data-stu-id="ce846-118">You can collect performance data from either real-time sources or log files.</span></span> <span data-ttu-id="ce846-119">如需如何將效能資料寫入記錄檔的詳細資訊，請參閱 [使用記錄](working-with-log-files.md)檔。</span><span class="sxs-lookup"><span data-stu-id="ce846-119">For more information on how to write performance data to log files, see [Working with Log Files](working-with-log-files.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ce846-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce846-120">See also</span></span>

- [<span data-ttu-id="ce846-121">收集效能資料</span><span class="sxs-lookup"><span data-stu-id="ce846-121">Collecting Performance Data</span></span>](collecting-performance-data.md)
- [<span data-ttu-id="ce846-122">流覽計數器</span><span class="sxs-lookup"><span data-stu-id="ce846-122">Browsing Counters</span></span>](browsing-counters.md)
- [<span data-ttu-id="ce846-123">檢查 PDH 介面傳回值</span><span class="sxs-lookup"><span data-stu-id="ce846-123">Checking PDH Interface Return Values</span></span>](checking-pdh-interface-return-values.md)
- [<span data-ttu-id="ce846-124">範例</span><span class="sxs-lookup"><span data-stu-id="ce846-124">Examples</span></span>](examples.md)
