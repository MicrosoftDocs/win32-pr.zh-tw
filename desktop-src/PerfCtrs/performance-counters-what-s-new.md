---
description: 本節說明每個版本的效能計數器已新增的新功能。
ms.assetid: 14bdae6c-9dcd-401e-8c43-5391e00cf7e3
title: " (效能計數器的新) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0c1189a185351eabae438a01c6f111952f164e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983493"
---
# <a name="whats-new-with-performance-counters"></a><span data-ttu-id="7c193-103">效能計數器的新功能</span><span class="sxs-lookup"><span data-stu-id="7c193-103">What's New with Performance Counters</span></span>

<span data-ttu-id="7c193-104">本節說明每個版本的效能計數器已新增的新功能。</span><span class="sxs-lookup"><span data-stu-id="7c193-104">This section describes the new features that were added to Performance Counters for each release.</span></span>

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="7c193-105">Windows 7 與 Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7c193-105">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="7c193-106">[CTRPP](ctrpp.md)工具已變更，可改善和簡化程式碼產生。</span><span class="sxs-lookup"><span data-stu-id="7c193-106">The [CTRPP](ctrpp.md) tool was changed to improve and simplify code generation.</span></span> <span data-ttu-id="7c193-107">此工具現在只會產生標頭和資源檔。</span><span class="sxs-lookup"><span data-stu-id="7c193-107">The tool now generates only a header and resource file.</span></span> <span data-ttu-id="7c193-108">如果您想要使用舊的程式碼產生行為 (不建議) ，您可以使用新的 `-legacy` 引數。</span><span class="sxs-lookup"><span data-stu-id="7c193-108">If you want to old code generation behavior (not recommended), you can use the new `-legacy` argument.</span></span>

- <span data-ttu-id="7c193-109">您現在必須指定新的 `-o` 和 `-rc` 引數，分別指定標頭和資源檔的名稱和位置。</span><span class="sxs-lookup"><span data-stu-id="7c193-109">You must now specify the new `-o` and `-rc` arguments that specify the name and location of the header and resource file, respectively.</span></span>
- <span data-ttu-id="7c193-110">您可以使用選擇性的 new `-prefix` 引數，指定要加入至在產生的標頭檔中定義的全域變數和函數開頭的字串。</span><span class="sxs-lookup"><span data-stu-id="7c193-110">You can use the optional new `-prefix` argument to specify a string to add to the beginning of global variables and functions defined in the generated header file.</span></span>
- <span data-ttu-id="7c193-111">如果您必須更新您的計數器資訊清單，使用新的程式碼產生時，就不需要將先前的回呼實作為新產生的程式碼，因為這些回呼不再包含在產生的程式碼中。</span><span class="sxs-lookup"><span data-stu-id="7c193-111">If you have to update your counters manifest, using the new code generation eliminates the need to merge your previous callback implementation with the new generated code since the callbacks are no longer included in the generated code.</span></span>

<span data-ttu-id="7c193-112">`symbol`下列資訊清單元素可使用新的屬性：</span><span class="sxs-lookup"><span data-stu-id="7c193-112">A new `symbol` attribute is available for the following manifest elements:</span></span>

- [<span data-ttu-id="7c193-113">供應商</span><span class="sxs-lookup"><span data-stu-id="7c193-113">provider</span></span>](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element)
- [<span data-ttu-id="7c193-114">counterSet</span><span class="sxs-lookup"><span data-stu-id="7c193-114">counterSet</span></span>](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)
- [<span data-ttu-id="7c193-115">計數器</span><span class="sxs-lookup"><span data-stu-id="7c193-115">counter</span></span>](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element)

<span data-ttu-id="7c193-116">`symbol`[提供者](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element)和[counterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)需要屬性，而且對[counter](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element)而言是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="7c193-116">The `symbol` attribute is required for [provider](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) and [counterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element), and is optional for [counter](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element).</span></span> <span data-ttu-id="7c193-117">屬性可讓您提供符號名稱，讓您在呼叫提供者函式時，用來參考每個元素 (例如，您可以在呼叫 [PerfCreateInstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)) 時使用計數器集合符號名稱。</span><span class="sxs-lookup"><span data-stu-id="7c193-117">The attribute lets you provide a symbolic name that you can use to reference each element when calling the provider functions (for example, you can use the counter set symbolic name when calling [PerfCreateInstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)).</span></span>

## <a name="windows-vista"></a><span data-ttu-id="7c193-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c193-118">Windows Vista</span></span>

<span data-ttu-id="7c193-119">在此版本中，提供計數器資料的效能計數器架構已完全變更。</span><span class="sxs-lookup"><span data-stu-id="7c193-119">The Performance Counters architecture for providing counter data was completely changed for this release.</span></span>

<span data-ttu-id="7c193-120">先前，您已使用 INI 檔案定義您的計數器資料，並已執行可在取用者的進程中執行的效能 DLL，以在取用者要求時提供資料。</span><span class="sxs-lookup"><span data-stu-id="7c193-120">Previously, you used an INI file to define your counter data and you implemented a performance DLL which ran in the consumer's process to provide the data when a consumer requested it.</span></span> <span data-ttu-id="7c193-121">此架構已被取代，不建議用於新的程式碼，因為會有顯著的效能和可靠性問題。</span><span class="sxs-lookup"><span data-stu-id="7c193-121">This architecture is deprecated and is not recommended for new code due to significant performance and reliability issues.</span></span>

<span data-ttu-id="7c193-122">新的架構會使用資訊清單來定義計數器資料，並在提供者的進程中執行程式碼，以在取用者要求時提供資料。</span><span class="sxs-lookup"><span data-stu-id="7c193-122">The new architecture uses a manifest to define the counter data and runs code in the provider's process to provide the data when a consumer requests it.</span></span> <span data-ttu-id="7c193-123">如需其他詳細資訊，請參閱 [使用2.0 版提供計數器資料](providing-counter-data-using-version-2-0.md)。</span><span class="sxs-lookup"><span data-stu-id="7c193-123">For additional details, see [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md).</span></span>

<span data-ttu-id="7c193-124">此版本已新增下列函式：</span><span class="sxs-lookup"><span data-stu-id="7c193-124">The following functions were added for this release:</span></span>

- [<span data-ttu-id="7c193-125">ControlCallback</span><span class="sxs-lookup"><span data-stu-id="7c193-125">ControlCallback</span></span>](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [<span data-ttu-id="7c193-126">PerfCreateInstance</span><span class="sxs-lookup"><span data-stu-id="7c193-126">PerfCreateInstance</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [<span data-ttu-id="7c193-127">PerfDeleteInstance</span><span class="sxs-lookup"><span data-stu-id="7c193-127">PerfDeleteInstance</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [<span data-ttu-id="7c193-128">PerfQueryInstance</span><span class="sxs-lookup"><span data-stu-id="7c193-128">PerfQueryInstance</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [<span data-ttu-id="7c193-129">PerfSetCounterSetInfo</span><span class="sxs-lookup"><span data-stu-id="7c193-129">PerfSetCounterSetInfo</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [<span data-ttu-id="7c193-130">PerfSetULongCounterValue</span><span class="sxs-lookup"><span data-stu-id="7c193-130">PerfSetULongCounterValue</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [<span data-ttu-id="7c193-131">PerfSetULongLongCounterValue</span><span class="sxs-lookup"><span data-stu-id="7c193-131">PerfSetULongLongCounterValue</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [<span data-ttu-id="7c193-132">PerfSetCounterRefValue</span><span class="sxs-lookup"><span data-stu-id="7c193-132">PerfSetCounterRefValue</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [<span data-ttu-id="7c193-133">PerfStartProvider</span><span class="sxs-lookup"><span data-stu-id="7c193-133">PerfStartProvider</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [<span data-ttu-id="7c193-134">PerfStopProvider</span><span class="sxs-lookup"><span data-stu-id="7c193-134">PerfStopProvider</span></span>](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

<span data-ttu-id="7c193-135">此版本已新增下列結構：</span><span class="sxs-lookup"><span data-stu-id="7c193-135">The following structures were added for this release:</span></span>

- [<span data-ttu-id="7c193-136">性能 \_ 計數器身分 \_ 識別</span><span class="sxs-lookup"><span data-stu-id="7c193-136">PERF\_COUNTER\_IDENTITY</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [<span data-ttu-id="7c193-137">性能 \_ 計數器 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="7c193-137">PERF\_COUNTER\_INFO</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [<span data-ttu-id="7c193-138">效能 \_ COUNTERSET \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="7c193-138">PERF\_COUNTERSET\_INFO</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [<span data-ttu-id="7c193-139">效能 \_ COUNTERSET \_ 實例</span><span class="sxs-lookup"><span data-stu-id="7c193-139">PERF\_COUNTERSET\_INSTANCE</span></span>](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)

<span data-ttu-id="7c193-140">如需您在資訊清單中用來定義計數器的 XML 元素清單，請參閱 [效能計數器架構](performance-counters-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="7c193-140">For a list of the XML elements that you use in your manifest to define your counters, see [Performance Counters Schema](performance-counters-schema.md).</span></span>

<span data-ttu-id="7c193-141">如需有關剖析資訊清單並產生您作為提供者起點之程式碼的 CTRPP 前置處理器工具的詳細資訊，請參閱 [CTRPP](ctrpp.md)。</span><span class="sxs-lookup"><span data-stu-id="7c193-141">For information on the CTRPP pre-processor tool that parses your manifest and generates the code that you use as the starting point for your provider, see [CTRPP](ctrpp.md).</span></span>
