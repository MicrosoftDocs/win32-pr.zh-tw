---
description: 應用程式資訊清單
ms.assetid: f022374d-ea3f-477f-9b59-3188b775ed64
title: 應用程式資訊清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80c52b8eb2af87c271151be3d7989f50b2903084
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088586"
---
# <a name="application-manifest"></a><span data-ttu-id="b8ffd-103">應用程式資訊清單</span><span class="sxs-lookup"><span data-stu-id="b8ffd-103">Application Manifest</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="b8ffd-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="b8ffd-104">Affected Platforms</span></span>

<span data-ttu-id="b8ffd-105">**客戶** 端-Windows 7</span><span class="sxs-lookup"><span data-stu-id="b8ffd-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="b8ffd-106">**伺服器** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b8ffd-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="b8ffd-107">功能影響</span><span class="sxs-lookup"><span data-stu-id="b8ffd-107">Feature Impact</span></span>

 <span data-ttu-id="b8ffd-108">**嚴重性** -低</span><span class="sxs-lookup"><span data-stu-id="b8ffd-108">**Severity** - Low</span></span>  
<span data-ttu-id="b8ffd-109">**頻率** -低</span><span class="sxs-lookup"><span data-stu-id="b8ffd-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="b8ffd-110">Description</span><span class="sxs-lookup"><span data-stu-id="b8ffd-110">Description</span></span>

<span data-ttu-id="b8ffd-111">Windows 7 在名為「相容性」的應用程式資訊清單中引進了新的區段。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-111">Windows 7 introduces a new section in the application manifest called "Compatibility."</span></span> <span data-ttu-id="b8ffd-112">本節可協助 Windows 判斷應用程式設計成目標的 Windows 版本，並讓 Windows 根據應用程式的目標 Windows 版本提供應用程式預期的行為。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-112">This section helps Windows determine the versions of Windows that an application was designed to target, and enables Windows to provide the behavior that the application expects based on the version of Windows that the application targeted.</span></span>

<span data-ttu-id="b8ffd-113">相容性區段可讓 Windows 將新的行為提供給新開發人員建立的軟體，同時維持現有軟體的相容性。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-113">The Compatibility section allows Windows to provide new behavior to new developer-created software while maintaining the compatibility for existing software.</span></span> <span data-ttu-id="b8ffd-114">本節也可協助 Windows 在未來的 Windows 版本中提供更佳的相容性。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-114">This section also helps Windows deliver greater compatibility in future versions of Windows as well.</span></span> <span data-ttu-id="b8ffd-115">例如，在 [相容性] 區段中宣告僅支援 Windows 7 的應用程式將會在未來的 Windows 版本中繼續收到 Windows 7 行為。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-115">For example, an application declaring support only for Windows 7 in the Compatibility section will continue to receive Windows 7 behavior in future version of Windows.</span></span>

## <a name="manifestation-of-change"></a><span data-ttu-id="b8ffd-116">變更的表現</span><span class="sxs-lookup"><span data-stu-id="b8ffd-116">Manifestation of Change</span></span>

<span data-ttu-id="b8ffd-117">在其資訊清單中沒有相容性區段的應用程式，預設會在 Windows 7 和未來的 Windows 版本上收到 Windows Vista 行為。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-117">Applications without a Compatibility section in their manifest will receive Windows Vista behavior by default on Windows 7 and future Windows versions.</span></span> <span data-ttu-id="b8ffd-118">請注意，Windows XP 和 Windows Vista 會忽略此資訊清單區段，而不會對它們產生任何影響。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-118">Note that Windows XP and Windows Vista ignore this manifest section and it has no impact on them.</span></span>

<span data-ttu-id="b8ffd-119">下列 Windows 元件會根據 Windows 7 的相容性區段提供分歧的行為：</span><span class="sxs-lookup"><span data-stu-id="b8ffd-119">The following Windows components provide divergent behavior based on the Compatibility section in Windows 7:</span></span>

<span data-ttu-id="b8ffd-120">**RPC 預設執行緒集區**</span><span class="sxs-lookup"><span data-stu-id="b8ffd-120">**RPC Default Thread Pool**</span></span>

-   <span data-ttu-id="b8ffd-121">**Windows 7：** 為了改善擴充性並減少執行緒計數，RPC (預設集區) 切換至 NT 執行緒集區。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-121">**Windows 7:** To improve scalability and reduce thread counts, RPC switched to the NT thread pool (default pool).</span></span> <span data-ttu-id="b8ffd-122">針對 Windows Vista，RPC 使用私用執行緒集區。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-122">For Windows Vista, RPC used a private thread pool.</span></span>
    -   <span data-ttu-id="b8ffd-123">針對針對 Win7 編譯的二進位檔，會使用預設集區</span><span class="sxs-lookup"><span data-stu-id="b8ffd-123">For binaries compiled for Win7 the default pool is used</span></span>
    -   <span data-ttu-id="b8ffd-124">如果在 \_ 呼叫任何 RPC API 之前呼叫 I RpcMgmtEnableDedicatedThreadPool，則會使用私用執行緒集區 (Vista 行為) </span><span class="sxs-lookup"><span data-stu-id="b8ffd-124">If I\_RpcMgmtEnableDedicatedThreadPool is called before any RPC API is called, the private thread pool is used (Vista behavior)</span></span>
    -   <span data-ttu-id="b8ffd-125">如果在 \_ RPC 呼叫之後呼叫 I RpcMgmtEnableDedicatedThreadPool，則會使用預設集區，I \_ RpcMgmtEnableDedicatedThreadPool 會傳回錯誤1764，且不支援要求的作業</span><span class="sxs-lookup"><span data-stu-id="b8ffd-125">If I\_RpcMgmtEnableDedicatedThreadPool is called after an RPC call, the default pool is used, I\_RpcMgmtEnableDedicatedThreadPool returns the error 1764, and the requested operation is not supported</span></span>
-   <span data-ttu-id="b8ffd-126">**Windows Vista (預設) ：** 針對 Windows Vista 和以下所編譯的二進位檔，會使用私用集區。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-126">**Windows Vista (default):** For binaries compiled for Windows Vista and below, the private pool is used.</span></span>

<span data-ttu-id="b8ffd-127">**DirectDraw 鎖定**</span><span class="sxs-lookup"><span data-stu-id="b8ffd-127">**DirectDraw Lock**</span></span>

-   <span data-ttu-id="b8ffd-128">**Windows 7：** 針對 Windows 7 所顯示的應用程式無法呼叫 DDRAW 中的鎖定 API 來鎖定主要桌面影片緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-128">**Windows 7:** Applications manifested for Windows 7 cannot call Lock API in DDRAW to lock the primary Desktop video buffer.</span></span> <span data-ttu-id="b8ffd-129">這樣做會導致錯誤，而且會傳回主要複本的 **Null** 指標。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-129">Doing so will result in error, and **NULL** pointer for the primary will be returned.</span></span> <span data-ttu-id="b8ffd-130">即使桌面視窗管理員組合未開啟，仍會強制執行此行為。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-130">This behavior is enforced even if Desktop Window Manager Composition is not turned on.</span></span> <span data-ttu-id="b8ffd-131">與 Windows 7 相容的應用程式不能鎖定主要影片緩衝區來呈現。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-131">Windows 7 compatible applications must not lock the primary video buffer to render.</span></span>
-   <span data-ttu-id="b8ffd-132">**Windows Vista (預設) ：** 應用程式將能夠在主要影片緩衝區上取得鎖定，因為繼承應用程式相依于此行為。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-132">**Windows Vista (default):** Applications will be able to acquire a lock on the primary video buffer as legacy applications depend on this behavior.</span></span> <span data-ttu-id="b8ffd-133">執行應用程式會關閉桌面視窗管理員。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-133">Running the application turns off Desktop Window Manager.</span></span>

<span data-ttu-id="b8ffd-134">**DirectDraw 位區塊傳輸 (Blt) 至主要未裁剪視窗**</span><span class="sxs-lookup"><span data-stu-id="b8ffd-134">**DirectDraw Bit Block Transfer (Blt) to Primary without Clipping Window**</span></span>

-   <span data-ttu-id="b8ffd-135">**Windows 7：** 針對 Windows 7 所顯示的應用程式無法在沒有剪切視窗的情況下，執行 Blt 的主要桌面影片緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-135">**Windows 7:** Applications manifested for Windows 7 are prevented from performing Blt's to the primary Desktop video buffer without a clipping window.</span></span> <span data-ttu-id="b8ffd-136">這樣做會導致錯誤，而且不會轉譯 Blt 區域。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-136">Doing so will result in error and the Blt area will not be rendered.</span></span> <span data-ttu-id="b8ffd-137">即使您沒有開啟桌面視窗管理員組合，Windows 仍會強制執行此行為。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-137">Windows enforces this behavior even if you do not turn on Desktop Window Manager Composition.</span></span> <span data-ttu-id="b8ffd-138">與 Windows 7 相容的應用程式必須 Blt 至剪輯視窗。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-138">Windows 7 compatible applications must Blt to a clipping window.</span></span>
-   <span data-ttu-id="b8ffd-139">**Windows Vista (預設) ：** 應用程式必須能夠在不使用裁剪視窗的情況下 Blt 至主應用程式，因為繼承應用程式相依于此行為。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-139">**Windows Vista (default):** Applications must be able to Blt to the primary without a clipping window as legacy applications depend on this behavior.</span></span> <span data-ttu-id="b8ffd-140">執行此應用程式會關閉桌面視窗管理員。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-140">Running this application turns off the Desktop Window Manager.</span></span>

<span data-ttu-id="b8ffd-141">**GetOverlappedResult API**</span><span class="sxs-lookup"><span data-stu-id="b8ffd-141">**GetOverlappedResult API**</span></span>

-   <span data-ttu-id="b8ffd-142">**Windows 7：** 解決競爭條件，其中使用 GetOverlappedResult 的多執行緒應用程式可以在不重設重迭結構中的事件的情況下傳回，而導致下一次呼叫此函式傳回過早。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-142">**Windows 7:** Resolves a race condition where a multithreaded app using GetOverlappedResult can return without resetting the event in the overlapped structure, causing the next call to this function to return prematurely.</span></span>
-   <span data-ttu-id="b8ffd-143">**Windows Vista (預設) ：** 針對應用程式可能相依的競爭條件提供行為。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-143">**Windows Vista (default):** Provides the behavior with the race condition that applications may have a dependency on.</span></span> <span data-ttu-id="b8ffd-144">如果應用程式想要在 Windows 7 行為之前避免此競爭情形，應等候重迭的事件，並在收到信號時呼叫 GetOverlappedResult，並使用 bWait = = **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-144">Applications wishing to avoid this race prior to the Windows 7 behavior should wait on the overlapped event and when signaled, call GetOverlappedResult with bWait == **FALSE**.</span></span>

<span data-ttu-id="b8ffd-145">**程式相容性助理 (PCA)**</span><span class="sxs-lookup"><span data-stu-id="b8ffd-145">**Program Compatibility Assistant (PCA)**</span></span>

-   <span data-ttu-id="b8ffd-146">**Windows 7：** 具有相容性區段的應用程式不會取得 PCA 的風險降低。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-146">**Windows 7:** Applications with Compatibility section will not get the PCA mitigation.</span></span>
-   <span data-ttu-id="b8ffd-147">**Windows Vista (預設) ：** 在某些特定情況下無法正確安裝或損毀的應用程式，將會降低 PCA 的風險。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-147">**Windows Vista (default):** Applications that fail to install properly or crash during runtime under some specific circumstances will get the PCA mitigation.</span></span> <span data-ttu-id="b8ffd-148">如需詳細資訊，請參閱參考一節。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-148">For more details, see the reference section.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="b8ffd-149">運用功能功能</span><span class="sxs-lookup"><span data-stu-id="b8ffd-149">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="b8ffd-150">使用作業系統支援的最新相容性資訊來更新應用程式資訊清單。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-150">Update the application manifest with the latest Compatibility information for operating system support.</span></span> <span data-ttu-id="b8ffd-151">本節描述資訊清單的新增專案：</span><span class="sxs-lookup"><span data-stu-id="b8ffd-151">The section describes the additions to the manifest:</span></span>

-   <span data-ttu-id="b8ffd-152">**命名空間：** 相容性。 v1 (xmlns = "urn：架構-microsoft-com：相容性 v1" >) </span><span class="sxs-lookup"><span data-stu-id="b8ffd-152">**Namespace:** Compatibility.v1 (xmlns="urn:schemas-microsoft-com:compatibility.v1">)</span></span>

-   <span data-ttu-id="b8ffd-153">**區段名稱：** (新區段的相容性) </span><span class="sxs-lookup"><span data-stu-id="b8ffd-153">**Section Name:** Compatibility (new section)</span></span>

-   <span data-ttu-id="b8ffd-154">**SupportedOS：** 支援的作業系統 GUID-對應至受支援作業系統的 Guid 如下：</span><span class="sxs-lookup"><span data-stu-id="b8ffd-154">**SupportedOS:** GUID of supported operating system - The GUIDs that map to the supported operating systems are:</span></span>

    -   <span data-ttu-id="b8ffd-155">適用于 Windows Vista 的 {e2011457-1546-43c5-a5fe-008deee3d3f0}：這是 switchback 內容的預設值。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-155">{e2011457-1546-43c5-a5fe-008deee3d3f0} for Windows Vista: This is the default value for the switchback context.</span></span>
    -   <span data-ttu-id="b8ffd-156">適用于 Windows 7 的 {35138b9a-5d96-4fbd-8e2d-a2440225f93a}：在應用程式資訊清單中設定此值的應用程式會取得 Windows 7 行為。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-156">{35138b9a-5d96-4fbd-8e2d-a2440225f93a} for Windows 7: Applications that set this value in the application manifest get the Windows 7 behavior.</span></span>

    > [!Note]  
    > <span data-ttu-id="b8ffd-157">Microsoft 會視需要產生並張貼未來 Windows 版本的 Guid。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-157">Microsoft will generate and post GUIDs for future Windows versions as needed.</span></span>

     

<span data-ttu-id="b8ffd-158">以下是更新的資訊清單範例。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-158">The following is an example of an updated manifest.</span></span>

> [!Note]  
> <span data-ttu-id="b8ffd-159">應用程式資訊清單中的屬性和標記名稱會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-159">The attribute and tag names in the application manifest are case sensitive.</span></span>

 


```XML
<?xml version="1.0" encoding="UTF-8" standalone="yes"?> 
  <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--The ID below indicates application support for Windows Vista --> 
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--The ID below indicates application support for Windows 7 --> 
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/> 
      </application> 
    </compatibility>
  </assembly>
```



<span data-ttu-id="b8ffd-160">在上述範例中，為這兩個作業系統新增 Guid 的值是提供下層支援。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-160">The value of adding GUIDs for both operating systems in the above example is to provide down-level support.</span></span> <span data-ttu-id="b8ffd-161">同時支援這兩個平臺的應用程式不需要個別的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-161">Applications that support both platforms would not need separate manifests for each platform.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="b8ffd-162">相容性、效能、可靠性和可用性測試</span><span class="sxs-lookup"><span data-stu-id="b8ffd-162">Compatibility, Performance, Reliability, and Usability Testing</span></span>

1.  <span data-ttu-id="b8ffd-163">使用新的相容性區段測試應用程式，並 `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` 確保應用程式能正常運作，並使用最新的 Windows 7 行為</span><span class="sxs-lookup"><span data-stu-id="b8ffd-163">Test the application with the new compatibility section and `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` to ensure that the application works properly using the latest Windows 7 behavior</span></span>
2.  <span data-ttu-id="b8ffd-164">使用新的相容性區段測試應用程式，並 `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` (或完全沒有本節) ，以確保應用程式在 windows 7 上使用 Windows Vista 行為正常運作</span><span class="sxs-lookup"><span data-stu-id="b8ffd-164">Test the application with the new compatibility section and `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` (or without this section entirely) to ensure that the application works properly using the Windows Vista behaviors on Windows 7</span></span>

## <a name="known-issues"></a><span data-ttu-id="b8ffd-165">已知問題</span><span class="sxs-lookup"><span data-stu-id="b8ffd-165">Known Issues</span></span>

<span data-ttu-id="b8ffd-166">**內容不相符** 應用程式會在 Windows Vista 內容中執行，而不是在執行 Windows 7 或 Windows Server 2008 R2 x64 版本的電腦上的 Windows 7 內容中執行。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-166">**Context Mismatch** An application runs in a Windows Vista context instead of in a Windows 7 context on a computer that is running an x64 edition of either Windows 7 or Windows Server 2008 R2.</span></span>

<span data-ttu-id="b8ffd-167">**解決方案** 所有支援的 x64 版本的 Windows 7 和 Windows Server 2008 R2，以及所有支援的 Itanium 架構版本的 Windows Server 2008 R2 都有更新可修正此錯誤。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-167">**Solution** Updates are available to correct this for all supported x64-based versions of Windows 7 and Windows Server 2008 R2, as well as for all supported Itanium-based versions of Windows Server 2008 R2.</span></span> <span data-ttu-id="b8ffd-168">移至 KB 978637 的 Microsoft 支援服務頁面 [：應用程式會在 Windows Vista 內容中執行，而不是在執行 windows 7 或 Windows Server 2008 R2 x64 版本的電腦上的 windows 7 內容中執行](https://support.microsoft.com/kb/978637) ，以取得其他詳細資料，並下載您系統的正確版本。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-168">Go to the Microsoft Support page for [KB 978637: An application runs in a Windows Vista context instead of in a Windows 7 context on a computer that is running an x64 edition of Windows 7 or of Windows Server 2008 R2](https://support.microsoft.com/kb/978637) for additional details and to download the correct version for your system.</span></span>

<span data-ttu-id="b8ffd-169">**封鎖損毀傾印診斷**</span><span class="sxs-lookup"><span data-stu-id="b8ffd-169">**Crash dump diagnosis blocked**</span></span>

<span data-ttu-id="b8ffd-170">**解決方案** 移至 KB 976038 的 Microsoft 支援服務頁面 [：在64位版本的 Windows 中執行的應用程式](https://support.microsoft.com/kb/976038) 所擲回的例外狀況會被忽略，以取得其他詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b8ffd-170">**Solution** Go to the Microsoft Support page for [KB 976038: Exceptions that are thrown from an application that runs in a 64-bit version of Windows are ignored](https://support.microsoft.com/kb/976038) for additional details.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="b8ffd-171">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="b8ffd-171">Links to Other Resources</span></span>

-   [<span data-ttu-id="b8ffd-172">**QueryActCtxW 函式**</span><span class="sxs-lookup"><span data-stu-id="b8ffd-172">**QueryActCtxW Function**</span></span>](/windows/win32/api/winbase/nf-winbase-queryactctxw)
-   <span data-ttu-id="b8ffd-173">[UAC 資訊清單](/previous-versions/bb756929(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="b8ffd-173">[UAC manifest](/previous-versions/bb756929(v=msdn.10))</span></span>
-   [<span data-ttu-id="b8ffd-174">Windows 應用程式的應用程式資訊清單</span><span class="sxs-lookup"><span data-stu-id="b8ffd-174">Application manifests for Windows applications</span></span>](../sbscs/application-manifests.md)
-   [<span data-ttu-id="b8ffd-175">桌面視窗管理員 (DWM) </span><span class="sxs-lookup"><span data-stu-id="b8ffd-175">Desktop Window Manager (DWM)</span></span>](../dwm/dwm-overview.md)
-   [<span data-ttu-id="b8ffd-176">內容不相符更新</span><span class="sxs-lookup"><span data-stu-id="b8ffd-176">Context Mismatch Update</span></span>](https://support.microsoft.com/kb/978637)

 

 
