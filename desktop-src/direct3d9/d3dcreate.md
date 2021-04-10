---
description: 一或多個旗標的組合，可控制裝置的建立行為。
ms.assetid: 91387a2d-3927-4285-a09b-9ce247e6bfdd
title: D3DCREATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14de345d6cb6d164ee5cd3067e1f38ff66d9795d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936395"
---
# <a name="d3dcreate"></a><span data-ttu-id="25bce-103">D3DCREATE</span><span class="sxs-lookup"><span data-stu-id="25bce-103">D3DCREATE</span></span>

<span data-ttu-id="25bce-104">一或多個旗標的組合，可控制裝置的建立行為。</span><span class="sxs-lookup"><span data-stu-id="25bce-104">A combination of one or more flags that control the device create behavior.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="25bce-105">#定義</span><span class="sxs-lookup"><span data-stu-id="25bce-105">#define</span></span></td>
<td><span data-ttu-id="25bce-106">Description</span><span class="sxs-lookup"><span data-stu-id="25bce-106">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="25bce-107">D3DCREATE_ADAPTERGROUP_DEVICE</span><span class="sxs-lookup"><span data-stu-id="25bce-107">D3DCREATE_ADAPTERGROUP_DEVICE</span></span></td>
<td><span data-ttu-id="25bce-108">應用程式會要求裝置驅動此主要介面卡擁有的所有標頭。</span><span class="sxs-lookup"><span data-stu-id="25bce-108">Application asks the device to drive all the heads that this master adapter owns.</span></span> <span data-ttu-id="25bce-109">Nonmaster 介面卡上的旗標不合法。</span><span class="sxs-lookup"><span data-stu-id="25bce-109">The flag is illegal on nonmaster adapters.</span></span> <span data-ttu-id="25bce-110">如果設定此旗標，則傳遞至 <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> 的簡報參數應指向 <a href="d3dpresent-parameters.md"><strong>D3DPRESENT_PARAMETERS</strong></a>的陣列。</span><span class="sxs-lookup"><span data-stu-id="25bce-110">If this flag is set, the presentation parameters passed to <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> should point to an array of <a href="d3dpresent-parameters.md"><strong>D3DPRESENT_PARAMETERS</strong></a>.</span></span> <span data-ttu-id="25bce-111"><strong>D3DPRESENT_PARAMETERS</strong>中的元素數目應等於<a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>結構的 NumberOfAdaptersInGroup 成員所定義的介面卡數目。</span><span class="sxs-lookup"><span data-stu-id="25bce-111">The number of elements in <strong>D3DPRESENT_PARAMETERS</strong> should equal the number of adapters defined by the NumberOfAdaptersInGroup member of the <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a> structure.</span></span> <span data-ttu-id="25bce-112">DirectX 執行時間會以 <strong>D3DCAPS9</strong>的 AdapterOrdinalInGroup 成員所指定的數位順序，將每個元素指派給每個標頭。</span><span class="sxs-lookup"><span data-stu-id="25bce-112">The DirectX runtime will assign each element to each head in the numerical order specified by the AdapterOrdinalInGroup member of <strong>D3DCAPS9</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="25bce-113">D3DCREATE_DISABLE_DRIVER_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="25bce-113">D3DCREATE_DISABLE_DRIVER_MANAGEMENT</span></span></td>
<td><span data-ttu-id="25bce-114">Direct3D 將會管理資源，而不是驅動程式。</span><span class="sxs-lookup"><span data-stu-id="25bce-114">Direct3D will manage resources instead of the driver.</span></span> <span data-ttu-id="25bce-115">對於資源錯誤（例如，視訊記憶體不足），Direct3D 呼叫將不會失敗。</span><span class="sxs-lookup"><span data-stu-id="25bce-115">Direct3D calls will not fail for resource errors such as insufficient video memory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="25bce-116">D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</span><span class="sxs-lookup"><span data-stu-id="25bce-116">D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</span></span></td>
<td><span data-ttu-id="25bce-117">如同 D3DCREATE_DISABLE_DRIVER_MANAGEMENT，Direct3D 將會管理資源，而不是驅動程式。</span><span class="sxs-lookup"><span data-stu-id="25bce-117">Like D3DCREATE_DISABLE_DRIVER_MANAGEMENT, Direct3D will manage resources instead of the driver.</span></span> <span data-ttu-id="25bce-118">不同于 D3DCREATE_DISABLE_DRIVER_MANAGEMENT，D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX 會針對像是視頻記憶體不足的狀況傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="25bce-118">Unlike D3DCREATE_DISABLE_DRIVER_MANAGEMENT, D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX will return errors for conditions such as insufficient video memory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="25bce-119">D3DCREATE_DISABLE_PRINTSCREEN</span><span class="sxs-lookup"><span data-stu-id="25bce-119">D3DCREATE_DISABLE_PRINTSCREEN</span></span></td>
<td><span data-ttu-id="25bce-120">使執行時間不會為 Printscreen、Ctrl-Printscreen 和 Alt-Printscreen 註冊快速鍵，以抓取桌面或視窗內容。</span><span class="sxs-lookup"><span data-stu-id="25bce-120">Causes the runtime not register hotkeys for Printscreen, Ctrl-Printscreen and Alt-Printscreen to capture the desktop or window content.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="25bce-121">Direct3D 9 與 Direct3D 9Ex 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="25bce-121">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="25bce-122">此旗標僅適用于 Direct3D 9Ex。</span><span class="sxs-lookup"><span data-stu-id="25bce-122">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="25bce-123">D3DCREATE_DISABLE_PSGP_THREADING</span><span class="sxs-lookup"><span data-stu-id="25bce-123">D3DCREATE_DISABLE_PSGP_THREADING</span></span></td>
<td><span data-ttu-id="25bce-124">限制對主要應用程式執行緒的計算。</span><span class="sxs-lookup"><span data-stu-id="25bce-124">Restrict computation to the main application thread.</span></span> <span data-ttu-id="25bce-125">如果未設定旗標，則執行時間可能會在背景工作執行緒中執行軟體頂點處理和其他計算，以改善多處理器系統上的效能。</span><span class="sxs-lookup"><span data-stu-id="25bce-125">If the flag is not set, the runtime may perform software vertex processing and other computations in worker thread to improve performance on multi-processor systems.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="25bce-126">Windows XP 與 Windows Vista 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="25bce-126">Differences between Windows XP and Windows Vista:</span></span><br/> <span data-ttu-id="25bce-127">此旗標適用于 Windows Vista、Windows Server 2008 和 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="25bce-127">This flag is available on Windows Vista, Windows Server 2008, and Windows 7.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="25bce-128">D3DCREATE_ENABLE_PRESENTSTATS</span><span class="sxs-lookup"><span data-stu-id="25bce-128">D3DCREATE_ENABLE_PRESENTSTATS</span></span></td>
<td><span data-ttu-id="25bce-129">可收集裝置上目前的統計資料。</span><span class="sxs-lookup"><span data-stu-id="25bce-129">Enables the gathering of present statistics on the device.</span></span> <span data-ttu-id="25bce-130">對 <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>GetPresentStatistics</strong></a> 的呼叫將會傳回有效的資料。</span><span class="sxs-lookup"><span data-stu-id="25bce-130">Calls to <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>GetPresentStatistics</strong></a> will return valid data.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="25bce-131">Direct3D 9 與 Direct3D 9Ex 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="25bce-131">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="25bce-132">此旗標僅適用于 Direct3D 9Ex。</span><span class="sxs-lookup"><span data-stu-id="25bce-132">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="25bce-133">D3DCREATE_FPU_PRESERVE</span><span class="sxs-lookup"><span data-stu-id="25bce-133">D3DCREATE_FPU_PRESERVE</span></span></td>
<td><span data-ttu-id="25bce-134">將 Direct3D 浮點數計算的有效位數設定為呼叫執行緒所使用的有效位數。</span><span class="sxs-lookup"><span data-stu-id="25bce-134">Set the precision for Direct3D floating-point calculations to the precision used by the calling thread.</span></span> <span data-ttu-id="25bce-135">如果您未指定此旗標，Direct3D 預設為單精確度舍入至最接近的模式，原因有兩個：</span><span class="sxs-lookup"><span data-stu-id="25bce-135">If you do not specify this flag, Direct3D defaults to single-precision round-to-nearest mode for two reasons:</span></span>
<ul>
<li><span data-ttu-id="25bce-136">雙精確度模式將會降低 Direct3D 效能。</span><span class="sxs-lookup"><span data-stu-id="25bce-136">Double-precision mode will reduce Direct3D performance.</span></span></li>
<li><span data-ttu-id="25bce-137">Direct3D 的部分假設浮點單位例外狀況是遮罩的;取消遮罩這些例外狀況可能會導致未定義的行為。</span><span class="sxs-lookup"><span data-stu-id="25bce-137">Portions of Direct3D assume floating-point unit exceptions are masked; unmasking these exceptions may result in undefined behavior.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="25bce-138">D3DCREATE_HARDWARE_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="25bce-138">D3DCREATE_HARDWARE_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="25bce-139">指定硬體頂點處理。</span><span class="sxs-lookup"><span data-stu-id="25bce-139">Specifies hardware vertex processing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="25bce-140">D3DCREATE_MIXED_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="25bce-140">D3DCREATE_MIXED_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="25bce-141">指定混合 (軟體和硬體) 頂點處理。</span><span class="sxs-lookup"><span data-stu-id="25bce-141">Specifies mixed (both software and hardware) vertex processing.</span></span> <span data-ttu-id="25bce-142">針對 Windows 10，1607版和更新版本，不建議使用此設定。</span><span class="sxs-lookup"><span data-stu-id="25bce-142">For Windows 10, version 1607 and later, use of this setting is not recommended.</span></span> <span data-ttu-id="25bce-143">請參閱 D3DCREATE_SOFTWARE_VERTEXPROCESSING。</span><span class="sxs-lookup"><span data-stu-id="25bce-143">See D3DCREATE_SOFTWARE_VERTEXPROCESSING.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="25bce-144">D3DCREATE_SOFTWARE_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="25bce-144">D3DCREATE_SOFTWARE_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="25bce-145">指定軟體頂點處理。</span><span class="sxs-lookup"><span data-stu-id="25bce-145">Specifies software vertex processing.</span></span> <span data-ttu-id="25bce-146">針對 Windows 10，1607版和更新版本，不建議使用此設定。</span><span class="sxs-lookup"><span data-stu-id="25bce-146">For Windows 10, version 1607 and later, use of this setting is not recommended.</span></span> <span data-ttu-id="25bce-147">使用 D3DCREATE_HARDWARE_VERTEXPROCESSING。</span><span class="sxs-lookup"><span data-stu-id="25bce-147">Use D3DCREATE_HARDWARE_VERTEXPROCESSING.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="25bce-148">除非硬體頂點處理無法使用，否則不建議在 Windows 10、1607版 (和) 更新版本中使用軟體頂點處理，因為軟體頂點處理的效率大幅減少，同時改善了實施的安全性。</span><span class="sxs-lookup"><span data-stu-id="25bce-148">Unless hardware vertex processing is not available, the usage of software vertex processing is not recommended in Windows 10, version 1607 (and later versions) because the efficiency of software vertex processing was significantly reduced while improving the security of the implementation.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="25bce-149">D3DCREATE_MULTITHREADED</span><span class="sxs-lookup"><span data-stu-id="25bce-149">D3DCREATE_MULTITHREADED</span></span></td>
<td><span data-ttu-id="25bce-150">指出應用程式要求 Direct3D 為多執行緒安全。</span><span class="sxs-lookup"><span data-stu-id="25bce-150">Indicates that the application requests Direct3D to be multithread safe.</span></span> <span data-ttu-id="25bce-151">這會讓 Direct3D 執行緒更頻繁地取得其全域 <a href="/windows/desktop/Sync/critical-section-objects">重要區段</a> 的擁有權，而這可能會降低效能。</span><span class="sxs-lookup"><span data-stu-id="25bce-151">This makes a Direct3D thread take ownership of its global <a href="/windows/desktop/Sync/critical-section-objects">critical section</a> more frequently, which can degrade performance.</span></span> <span data-ttu-id="25bce-152">如果應用程式在一個執行緒中處理視窗訊息，而在另一個執行緒中進行 Direct3D API 呼叫，則應用程式必須在建立裝置時使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="25bce-152">If an application processes window messages in one thread while making Direct3D API calls in another, the application must use this flag when creating the device.</span></span> <span data-ttu-id="25bce-153">您也必須在卸載 d3d9.dll 之前終結此視窗。</span><span class="sxs-lookup"><span data-stu-id="25bce-153">This window must also be destroyed before unloading d3d9.dll.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="25bce-154">D3DCREATE_NOWINDOWCHANGES</span><span class="sxs-lookup"><span data-stu-id="25bce-154">D3DCREATE_NOWINDOWCHANGES</span></span></td>
<td><span data-ttu-id="25bce-155">指出 Direct3D 不得以任何方式改變焦點視窗。</span><span class="sxs-lookup"><span data-stu-id="25bce-155">Indicates that Direct3D must not alter the focus window in any way.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="25bce-156">如果設定此旗標，應用程式必須完全支援所有焦點管理事件，例如 ALT + TAB 和滑鼠點擊事件。</span><span class="sxs-lookup"><span data-stu-id="25bce-156">If this flag is set, the application must fully support all focus management events, such as ALT+TAB and mouse click events.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="25bce-157">D3DCREATE_PUREDEVICE</span><span class="sxs-lookup"><span data-stu-id="25bce-157">D3DCREATE_PUREDEVICE</span></span></td>
<td><span data-ttu-id="25bce-158">指定 Direct3D 不支援 Get \* 呼叫可儲存在狀態欄塊中的任何事物。</span><span class="sxs-lookup"><span data-stu-id="25bce-158">Specifies that Direct3D does not support Get\* calls for anything that can be stored in state blocks.</span></span> <span data-ttu-id="25bce-159">它也會告知 Direct3D 不要提供任何模擬服務來處理頂點。</span><span class="sxs-lookup"><span data-stu-id="25bce-159">It also tells Direct3D not to provide any emulation services for vertex processing.</span></span> <span data-ttu-id="25bce-160">這表示，如果裝置不支援頂點處理，則應用程式只能使用轉換後的頂點。</span><span class="sxs-lookup"><span data-stu-id="25bce-160">This means that if the device does not support vertex processing, then the application can use only post-transformed vertices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="25bce-161">D3DCREATE_SCREENSAVER</span><span class="sxs-lookup"><span data-stu-id="25bce-161">D3DCREATE_SCREENSAVER</span></span></td>
<td><span data-ttu-id="25bce-162">在全螢幕應用程式期間允許螢幕保護裝置。</span><span class="sxs-lookup"><span data-stu-id="25bce-162">Allows screensavers during a fullscreen application.</span></span> <span data-ttu-id="25bce-163">如果沒有這個旗標，Direct3D 將會停用螢幕保護裝置，只要呼叫的應用程式是全螢幕。</span><span class="sxs-lookup"><span data-stu-id="25bce-163">Without this flag, Direct3D will disable screensavers for as long as the calling application is fullscreen.</span></span> <span data-ttu-id="25bce-164">如果呼叫的應用程式已經是螢幕保護裝置，此旗標不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="25bce-164">If the calling application is already a screensaver, this flag has no effect.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="25bce-165">Direct3D 9 與 Direct3D 9Ex 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="25bce-165">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="25bce-166">此旗標僅適用于 Direct3D 9Ex。</span><span class="sxs-lookup"><span data-stu-id="25bce-166">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="25bce-167">D3DCREATE \_ 硬體 \_ VERTEXPROCESSING、D3DCREATE \_ MIXED \_ VERTEXPROCESSING 和 D3DCREATE \_ SOFTWARE \_ VERTEXPROCESSING 都是互斥的旗標。</span><span class="sxs-lookup"><span data-stu-id="25bce-167">D3DCREATE\_HARDWARE\_VERTEXPROCESSING, D3DCREATE\_MIXED\_VERTEXPROCESSING, and D3DCREATE\_SOFTWARE\_VERTEXPROCESSING are mutually exclusive flags.</span></span> <span data-ttu-id="25bce-168">呼叫 [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)時，必須指定至少一個頂點處理旗標。</span><span class="sxs-lookup"><span data-stu-id="25bce-168">At least one of these vertex processing flags must be specified when calling [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).</span></span>

## <a name="constant-information"></a><span data-ttu-id="25bce-169">常數資訊</span><span class="sxs-lookup"><span data-stu-id="25bce-169">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="25bce-170">標頭</span><span class="sxs-lookup"><span data-stu-id="25bce-170">Header</span></span>                   | <span data-ttu-id="25bce-171">D3D9。h</span><span class="sxs-lookup"><span data-stu-id="25bce-171">D3D9.h</span></span>     |
| <span data-ttu-id="25bce-172">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="25bce-172">Minimum operating system</span></span> | <span data-ttu-id="25bce-173">Windows 98</span><span class="sxs-lookup"><span data-stu-id="25bce-173">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="25bce-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="25bce-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25bce-175">Direct3D 常數</span><span class="sxs-lookup"><span data-stu-id="25bce-175">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
