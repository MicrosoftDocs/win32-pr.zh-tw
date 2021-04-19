---
description: 系統會使用計數器來收集效能資料。
ms.assetid: d1f1a90c-425a-4606-b86d-2948305ea84a
title: 指定計數器路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f3a92f94b4bf3d2252903d92785f43bb0cac110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983635"
---
# <a name="specifying-a-counter-path"></a><span data-ttu-id="94390-103">指定計數器路徑</span><span class="sxs-lookup"><span data-stu-id="94390-103">Specifying a Counter Path</span></span>

<span data-ttu-id="94390-104">系統會使用計數器來收集效能資料。</span><span class="sxs-lookup"><span data-stu-id="94390-104">The system uses counters to collect performance data.</span></span> <span data-ttu-id="94390-105">每個計數器都會透過其名稱及其路徑或位置來唯一識別。</span><span class="sxs-lookup"><span data-stu-id="94390-105">Each counter is uniquely identified through its name and its path, or location.</span></span> <span data-ttu-id="94390-106">計數器路徑的語法為：</span><span class="sxs-lookup"><span data-stu-id="94390-106">The syntax of a counter path is:</span></span>

``` syntax
\\Computer\PerfObject(ParentInstance/ObjectInstance#InstanceIndex)\Counter
```

<span data-ttu-id="94390-107">Computer 元素會指定您要從中查詢效能資料之電腦的名稱或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="94390-107">The Computer element specifies the name or IP address of the computer from which you want to query performance data.</span></span> <span data-ttu-id="94390-108">如果計數器位於本機電腦上，則電腦名稱稱是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="94390-108">The computer name is optional if the counter is located on the local computer.</span></span>

<span data-ttu-id="94390-109">PerfObject 元素會指定要查詢的效能物件。</span><span class="sxs-lookup"><span data-stu-id="94390-109">The PerfObject element specifies the performance object to query.</span></span> <span data-ttu-id="94390-110">效能物件可以是實體元件，例如處理器、磁片和記憶體，或系統物件（例如進程和執行緒）。</span><span class="sxs-lookup"><span data-stu-id="94390-110">A performance object can be a physical component, such as processors, disks, and memory, or a system object, such as processes and threads.</span></span> <span data-ttu-id="94390-111">每個系統物件都與電腦內的功能性元素相關，並有一組指派給它的標準計數器。</span><span class="sxs-lookup"><span data-stu-id="94390-111">Each system object is related to a functional element within the computer and has a set of standard counters assigned to it.</span></span> <span data-ttu-id="94390-112">每部電腦上可能會安裝一組不同的效能物件和計數器，因為應用程式可以安裝自己的效能物件和計數器。</span><span class="sxs-lookup"><span data-stu-id="94390-112">Each computer may have a different set of performance objects and counters installed on it because applications can install their own performance objects and counters.</span></span> <span data-ttu-id="94390-113">如需電腦上所安裝的效能物件和計數器清單，請參閱您電腦上 [效能] 工具中的 [ **新增計數器** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="94390-113">For a list of the performance objects and counters installed on your computer, see the **Add Counters** dialog box in the Performance tool on your computer.</span></span> <span data-ttu-id="94390-114">這些物件也會列在 [PDH 流覽] 對話方塊中 (查看) [流覽計數器](browsing-counters.md) 。</span><span class="sxs-lookup"><span data-stu-id="94390-114">These objects are also listed in the PDH browse dialog box (see [Browsing Counters](browsing-counters.md)).</span></span> <span data-ttu-id="94390-115">如需系統效能物件和計數器的清單，請參閱 [依物件的計數器](/previous-versions/windows/it-pro/windows-server-2003/cc783073(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="94390-115">For a list of system performance objects and counters, see [Counters by Object](/previous-versions/windows/it-pro/windows-server-2003/cc783073(v=ws.10)).</span></span>

<span data-ttu-id="94390-116">如果有多個物件實例可以存在，ParentInstance、ObjectInstance 和 InstanceIndex 就會包含在路徑中。</span><span class="sxs-lookup"><span data-stu-id="94390-116">The ParentInstance, ObjectInstance, and InstanceIndex are included in the path if multiple instances of the object can exist.</span></span> <span data-ttu-id="94390-117">例如，進程和執行緒是多個實例物件，因為有多個進程或執行緒可以同時執行。</span><span class="sxs-lookup"><span data-stu-id="94390-117">For example, processes and threads are multiple instance objects because more than one process or thread can run at the same time.</span></span> <span data-ttu-id="94390-118">如果物件可以有一個以上的實例，則計數器路徑必須指定物件實例。</span><span class="sxs-lookup"><span data-stu-id="94390-118">If an object can have more than one instance, the counter path must specify an object instance.</span></span>

<span data-ttu-id="94390-119">實例相關元素的格式取決於物件類型。</span><span class="sxs-lookup"><span data-stu-id="94390-119">The format of the instance related elements depends on the object type.</span></span> <span data-ttu-id="94390-120">如果物件具有簡單的實例，則格式只是以括弧括住的實例名稱。</span><span class="sxs-lookup"><span data-stu-id="94390-120">If the object has simple instances, then the format is only the instance name enclosed in parentheses.</span></span> <span data-ttu-id="94390-121">例如：</span><span class="sxs-lookup"><span data-stu-id="94390-121">For example:</span></span>

``` syntax
(Explorer)
```

<span data-ttu-id="94390-122">如果這個物件的實例也需要父實例名稱，則父實例名稱必須在物件實例之前，並以正斜線字元分隔。</span><span class="sxs-lookup"><span data-stu-id="94390-122">If the instance of this object also requires a parent instance name, the parent instance name must come before the object instance and be separated by a forward slash character.</span></span> <span data-ttu-id="94390-123">例如，執行緒屬於進程。</span><span class="sxs-lookup"><span data-stu-id="94390-123">For example, threads belong to processes.</span></span> <span data-ttu-id="94390-124">如果您查詢執行緒物件，您也必須指定它所屬的進程，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="94390-124">If you query a thread object, you must also specify the process to which it belongs as shown in the following example:</span></span>

``` syntax
(Explorer/0)
```

<span data-ttu-id="94390-125">如果物件具有多個具有相同名稱字串的實例，則可以藉由指定前置詞為井字型大小的實例索引，以順序來編制索引。</span><span class="sxs-lookup"><span data-stu-id="94390-125">If the object has multiple instances that have the same name string, they can be indexed sequentially by specifying the instance index prefixed by a pound sign.</span></span> <span data-ttu-id="94390-126">實例索引是以0為基礎。</span><span class="sxs-lookup"><span data-stu-id="94390-126">Instance indexes are 0-based.</span></span> <span data-ttu-id="94390-127">如果您想要查詢第一個實例，請勿包含 \# 0，只要指定實例名稱即可。</span><span class="sxs-lookup"><span data-stu-id="94390-127">If you want to query the first instance, do not include \#0—just specify the instance name.</span></span> <span data-ttu-id="94390-128">若要指定第二個實例，請使用 \# 1; 若要指定第三個實例，請使用 \# 2; 依此類推。</span><span class="sxs-lookup"><span data-stu-id="94390-128">To specify the second instance, use \#1; to specify the third instance, use \#2; and so on.</span></span> <span data-ttu-id="94390-129">例如：</span><span class="sxs-lookup"><span data-stu-id="94390-129">For example:</span></span>

``` syntax
(Explorer/0#1)
```

<span data-ttu-id="94390-130">Counter 元素會指定您想要查詢指定效能物件的效能計數器。</span><span class="sxs-lookup"><span data-stu-id="94390-130">The Counter element specifies the performance counter that you want to query for the given the performance object.</span></span>

<span data-ttu-id="94390-131">PDH 在計數器路徑中使用下列特殊字元。</span><span class="sxs-lookup"><span data-stu-id="94390-131">PDH uses the following special characters in a counter path.</span></span> <span data-ttu-id="94390-132">提供者不應該在其名稱中使用這些字元。</span><span class="sxs-lookup"><span data-stu-id="94390-132">Providers should not use these characters in their names.</span></span> <span data-ttu-id="94390-133">如果提供者使用這些特殊字元，則 PDH 無法剖析完整的計數器路徑以取得計數器和實例名稱。</span><span class="sxs-lookup"><span data-stu-id="94390-133">If a provider uses these special characters, PDH cannot parse the full counter path to obtain the counter and instances names.</span></span>



| <span data-ttu-id="94390-134">字元</span><span class="sxs-lookup"><span data-stu-id="94390-134">Character</span></span> | <span data-ttu-id="94390-135">描述</span><span class="sxs-lookup"><span data-stu-id="94390-135">Description</span></span>                                                |
|-----------|------------------------------------------------------------|
| \\        | <span data-ttu-id="94390-136">電腦、物件和計數器的一般分隔符號。</span><span class="sxs-lookup"><span data-stu-id="94390-136">Generic separator for computer, object, and counter.</span></span>       |
| <span data-ttu-id="94390-137">(</span><span class="sxs-lookup"><span data-stu-id="94390-137">(</span></span>         | <span data-ttu-id="94390-138">實例名稱的開頭。</span><span class="sxs-lookup"><span data-stu-id="94390-138">Beginning of instance name.</span></span>                                |
| <span data-ttu-id="94390-139">)</span><span class="sxs-lookup"><span data-stu-id="94390-139">)</span></span>         | <span data-ttu-id="94390-140">實例名稱的結尾。</span><span class="sxs-lookup"><span data-stu-id="94390-140">Ending of instance name.</span></span>                                   |
| /         | <span data-ttu-id="94390-141">分隔實例和父實例。</span><span class="sxs-lookup"><span data-stu-id="94390-141">Separates instance and parent instance.</span></span>                    |
| <span data-ttu-id="94390-142">\#n</span><span class="sxs-lookup"><span data-stu-id="94390-142">\#n</span></span>       | <span data-ttu-id="94390-143">識別相同名稱之實例的特定出現位置。</span><span class="sxs-lookup"><span data-stu-id="94390-143">Identifies a specific occurrence of a same-named instance.</span></span> |
| \*        | <span data-ttu-id="94390-144">萬用字元。</span><span class="sxs-lookup"><span data-stu-id="94390-144">Wildcard character.</span></span>                                        |



 

<span data-ttu-id="94390-145">下列範例顯示計數器路徑的可能格式：</span><span class="sxs-lookup"><span data-stu-id="94390-145">The following examples show the possible formats for counter paths:</span></span>

-   <span data-ttu-id="94390-146">\\\\電腦 \\ 物件 (父/實例 \# 索引) \\ 計數器</span><span class="sxs-lookup"><span data-stu-id="94390-146">\\\\computer\\object(parent/instance\#index)\\counter</span></span>
-   <span data-ttu-id="94390-147">\\\\\\ (父/實例) 計數器的電腦物件 \\</span><span class="sxs-lookup"><span data-stu-id="94390-147">\\\\computer\\object(parent/instance)\\counter</span></span>
-   <span data-ttu-id="94390-148">\\\\\\ (實例 \# 索引) \\ 計數器的電腦物件</span><span class="sxs-lookup"><span data-stu-id="94390-148">\\\\computer\\object(instance\#index)\\counter</span></span>
-   <span data-ttu-id="94390-149">\\\\\\ (實例) 計數器的電腦物件 \\</span><span class="sxs-lookup"><span data-stu-id="94390-149">\\\\computer\\object(instance)\\counter</span></span>
-   <span data-ttu-id="94390-150">\\\\電腦 \\ 物件 \\ 計數器</span><span class="sxs-lookup"><span data-stu-id="94390-150">\\\\computer\\object\\counter</span></span>
-   <span data-ttu-id="94390-151">\\物件 (父/實例 \# 索引) \\ 計數器</span><span class="sxs-lookup"><span data-stu-id="94390-151">\\object(parent/instance\#index)\\counter</span></span>
-   <span data-ttu-id="94390-152">\\物件 (父/實例) \\ 計數器</span><span class="sxs-lookup"><span data-stu-id="94390-152">\\object(parent/instance)\\counter</span></span>
-   <span data-ttu-id="94390-153">\\物件 (實例 \# 索引) \\ 計數器</span><span class="sxs-lookup"><span data-stu-id="94390-153">\\object(instance\#index)\\counter</span></span>
-   <span data-ttu-id="94390-154">\\物件 (實例) \\ 計數器</span><span class="sxs-lookup"><span data-stu-id="94390-154">\\object(instance)\\counter</span></span>
-   <span data-ttu-id="94390-155">\\物件 \\ 計數器</span><span class="sxs-lookup"><span data-stu-id="94390-155">\\object\\counter</span></span>

## <a name="using-wildcard-characters"></a><span data-ttu-id="94390-156">使用萬用字元</span><span class="sxs-lookup"><span data-stu-id="94390-156">Using wildcard characters</span></span>

<span data-ttu-id="94390-157">計數器路徑只可包含實例名稱的萬用字元，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="94390-157">Counter paths may contain a wildcard character only for the instance name as shown in the following example.</span></span>

``` syntax
\Process(*)\% Processor Time
```

<span data-ttu-id="94390-158">若要將萬用字元展開至包含在電腦上找到的實例或在記錄檔中的計數器路徑清單，請呼叫 [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha)。</span><span class="sxs-lookup"><span data-stu-id="94390-158">To expand the wildcard into a list of counter paths that contain instances found on the computer or in the log file, call [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha).</span></span>

 

 
