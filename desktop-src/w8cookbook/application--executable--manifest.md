---
title: 應用程式 (可執行檔) 資訊清單
description: 應用程式 (可執行檔) 資訊清單
ms.assetid: F46F33A6-0B2F-4086-9C6D-4AD43C26BCD3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de6f5a1d26af4b8ac6314655013ed56275bf7d73
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104024221"
---
# <a name="app-executable-manifest"></a><span data-ttu-id="8ee86-103">應用程式 (可執行檔) 資訊清單</span><span class="sxs-lookup"><span data-stu-id="8ee86-103">App (executable) manifest</span></span>

## <a name="platforms"></a><span data-ttu-id="8ee86-104">平台</span><span class="sxs-lookup"><span data-stu-id="8ee86-104">Platforms</span></span>

<span data-ttu-id="8ee86-105">**用戶端** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="8ee86-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="8ee86-106">**伺服器** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8ee86-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="8ee86-107">Description</span><span class="sxs-lookup"><span data-stu-id="8ee86-107">Description</span></span>

<span data-ttu-id="8ee86-108">在 Windows 中導入的應用程式 (可執行檔) 資訊清單的相容性區段，可協助作業系統判斷應用程式設計為目標的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="8ee86-108">The compatibility section of the app (executable) manifest introduced in Windows helps the operating system determine the versions of Windows an app was designed to target.</span></span> <span data-ttu-id="8ee86-109">此外，應用程式資訊清單也可讓 Windows 根據應用程式目標的 Windows 版本，提供應用程式預期的行為。</span><span class="sxs-lookup"><span data-stu-id="8ee86-109">Additionally, the app manifest enables Windows to provide the behavior that the app expects based on the version of Windows that the app targeted.</span></span>

<span data-ttu-id="8ee86-110">資訊清單的相容性區段可讓 Windows 將新的行為提供給新建立的軟體，同時維持現有軟體的相容性。</span><span class="sxs-lookup"><span data-stu-id="8ee86-110">The compatibility section of the manifest allows Windows to provide new behavior to newly created software while maintaining the compatibility for existing software.</span></span> <span data-ttu-id="8ee86-111">本節可協助 Windows 在未來的 Windows 版本中提供更佳的相容性。</span><span class="sxs-lookup"><span data-stu-id="8ee86-111">This section helps Windows deliver greater compatibility in future versions of Windows as well.</span></span> <span data-ttu-id="8ee86-112">例如，在 [相容性] 區段中宣告 Windows 8 的應用程式在未來的 Windows 版本中，仍會繼續收到 Windows 8 的行為。</span><span class="sxs-lookup"><span data-stu-id="8ee86-112">For example, an app declaring support for only Windows 8 in the compatibility section will continue to receive Windows 8 behavior in future versions of Windows.</span></span>

## <a name="manifestation"></a><span data-ttu-id="8ee86-113">表現</span><span class="sxs-lookup"><span data-stu-id="8ee86-113">Manifestation</span></span>

<span data-ttu-id="8ee86-114">在資訊清單中沒有相容性區段的應用程式，預設會在 Windows 7 Windows 8 和未來的 Windows 版本上具有 Windows Vista 的行為。</span><span class="sxs-lookup"><span data-stu-id="8ee86-114">Apps without a compatibility section in their manifest will have Windows Vista behavior by default on Windows 7 and Windows 8 and future Windows versions.</span></span> <span data-ttu-id="8ee86-115">請注意，Windows XP 和 Windows Vista 會忽略此資訊清單區段，而且對它們沒有任何影響。</span><span class="sxs-lookup"><span data-stu-id="8ee86-115">Be aware that Windows XP and Windows Vista ignore this manifest section and it has no impact on them.</span></span>

<span data-ttu-id="8ee86-116">這些 Windows 元件會根據相容性區段提供分歧的行為：</span><span class="sxs-lookup"><span data-stu-id="8ee86-116">These Windows components provide divergent behavior based on the compatibility section:</span></span>

<span data-ttu-id="8ee86-117">**遠端程序呼叫 (RPC) 預設執行緒集區**</span><span class="sxs-lookup"><span data-stu-id="8ee86-117">**Remote procedure call (RPC) default thread pool**</span></span>

-   <span data-ttu-id="8ee86-118">Windows 8 和 Windows 7：若要改善擴充性並減少執行緒計數，請將 RPC 切換至 NT 執行緒集區 (預設集區) 。</span><span class="sxs-lookup"><span data-stu-id="8ee86-118">Windows 8 and Windows 7: To improve scalability and reduce thread counts, RPC switched to the NT thread pool (default pool).</span></span> <span data-ttu-id="8ee86-119">針對 Windows Vista，RPC 使用私用執行緒集區：</span><span class="sxs-lookup"><span data-stu-id="8ee86-119">For Windows Vista, RPC used a private thread pool:</span></span>

    -   <span data-ttu-id="8ee86-120">針對 Windows 7 和更新版本的 Windows 所編譯的二進位檔，會使用預設集區。</span><span class="sxs-lookup"><span data-stu-id="8ee86-120">For binaries compiled for Windows 7 and later versions of Windows, the default pool is used.</span></span>
    -   <span data-ttu-id="8ee86-121">如果在 \_ 呼叫任何 RPC API 之前呼叫 I RpcMgmtEnableDedicatedThreadPool，則會使用私用執行緒集區 (Vista 行為) 。</span><span class="sxs-lookup"><span data-stu-id="8ee86-121">If I\_RpcMgmtEnableDedicatedThreadPool is called before any RPC API is called, the private thread pool is used (Vista behavior).</span></span>
    -   <span data-ttu-id="8ee86-122">如果在 \_ RPC 呼叫之後呼叫 I RpcMgmtEnableDedicatedThreadPool，則會使用預設集區，而我的 RpcMgmtEnableDedicatedThreadPool 會傳回 \_ 錯誤1764，且不支援要求的操作。</span><span class="sxs-lookup"><span data-stu-id="8ee86-122">If I\_RpcMgmtEnableDedicatedThreadPool is called after an RPC call, the default pool is used, I\_RpcMgmtEnableDedicatedThreadPool returns the error 1764, and the requested operation is not supported.</span></span>

-   <span data-ttu-id="8ee86-123">Windows Vista (預設) ：針對 Windows Vista 和舊版 Windows 編譯的二進位檔，會使用私用集區。</span><span class="sxs-lookup"><span data-stu-id="8ee86-123">Windows Vista (default): For binaries compiled for Windows Vista and earlier versions of Windows, the private pool is used.</span></span>

<span data-ttu-id="8ee86-124">**DirectDraw 鎖定**</span><span class="sxs-lookup"><span data-stu-id="8ee86-124">**DirectDraw lock**</span></span>

-   <span data-ttu-id="8ee86-125">Windows 8 和 Windows 7：針對 Windows 7 和更新版本的作業系統所顯示的應用程式無法呼叫 DDRAW 中的鎖定 API 來鎖定主要桌面影片緩衝區;這樣做會導致錯誤，並傳回主要複本的 Null 指標。</span><span class="sxs-lookup"><span data-stu-id="8ee86-125">Windows 8 and Windows 7: Apps manifested for Windows 7 and later versions of the operating system cannot call Lock API in DDRAW to lock the primary desktop video buffer; doing so will result in an error, and a NULL pointer for the primary is returned.</span></span> <span data-ttu-id="8ee86-126">即使桌面視窗管理員組合未開啟，仍會強制執行此行為。</span><span class="sxs-lookup"><span data-stu-id="8ee86-126">This behavior is enforced even if Desktop Window Manager Composition is not turned on.</span></span> <span data-ttu-id="8ee86-127">針對 Windows 7 和更新版本宣告相容性的應用程式不能鎖定主要影片緩衝區來呈現。</span><span class="sxs-lookup"><span data-stu-id="8ee86-127">Apps with compatibility declared for Windows 7 and later must not lock the primary video buffer to render.</span></span>
-   <span data-ttu-id="8ee86-128">Windows Vista (預設) ：應用程式可以取得主要影片緩衝區的鎖定，因為繼承應用程式相依于此行為;執行應用程式會關閉桌面視窗管理員。</span><span class="sxs-lookup"><span data-stu-id="8ee86-128">Windows Vista (default): Apps can acquire a lock on the primary video buffer, as legacy apps depend on this behavior; running the app turns off Desktop Window Manager.</span></span>

<span data-ttu-id="8ee86-129">**DirectDraw 位區塊傳輸 (bitblt) 至主要而不需要剪切視窗**</span><span class="sxs-lookup"><span data-stu-id="8ee86-129">**DirectDraw bit-block transfer (bitblt) to primary without clipping window**</span></span>

-   <span data-ttu-id="8ee86-130">Windows 8 和 Windows 7：針對 Windows 7 和更新版本的 Windows 所顯示的應用程式，無法在沒有剪切視窗的情況下執行 bitblt 至主要桌面影片緩衝區;這樣做會導致錯誤，而且不會呈現 bitblt 區域。</span><span class="sxs-lookup"><span data-stu-id="8ee86-130">Windows 8 and Windows 7: Apps manifested for Windows 7 and later versions of Windows are prevented from performing a bitblt to the primary Desktop video buffer without a clipping window; doing so results in an error and the bitblt area will not be rendered.</span></span> <span data-ttu-id="8ee86-131">即使您沒有開啟桌面視窗管理員組合，Windows 仍會強制執行此行為。</span><span class="sxs-lookup"><span data-stu-id="8ee86-131">Windows enforces this behavior even if you do not turn on Desktop Window Manager Composition.</span></span> <span data-ttu-id="8ee86-132">針對 Windows 7 和更新版本宣告相容性的應用程式必須執行 bitblt 至剪切視窗。</span><span class="sxs-lookup"><span data-stu-id="8ee86-132">Apps with compatibility declared for Windows 7 and later must perform a bitblt to a clipping window.</span></span>
-   <span data-ttu-id="8ee86-133">Windows Vista (預設) ：應用程式必須能夠在不使用裁剪視窗的情況下執行 bitblt，因為繼承應用程式相依于此行為;執行此應用程式會關閉桌面視窗管理員。</span><span class="sxs-lookup"><span data-stu-id="8ee86-133">Windows Vista (default): Apps must be able to perform a bitblt to the primary without a clipping window, as legacy apps depend on this behavior; running this app turns off the Desktop Window Manager.</span></span>

<span data-ttu-id="8ee86-134">**GetOverlappedResult API**</span><span class="sxs-lookup"><span data-stu-id="8ee86-134">**GetOverlappedResult API**</span></span>

-   <span data-ttu-id="8ee86-135">Windows 8 和 Windows 7：解決競爭條件，其中使用 **GetOverlappedResult** 的多執行緒應用程式可以在不重設重迭結構中的事件的情況下傳回，而導致下一次呼叫此函式會提前傳回。</span><span class="sxs-lookup"><span data-stu-id="8ee86-135">Windows 8 and Windows 7: Resolves a race condition where a multithreaded app using **GetOverlappedResult** can return without resetting the event in the overlapped structure, causing the next call to this function to return prematurely.</span></span>
-   <span data-ttu-id="8ee86-136">Windows Vista (預設) ：提供應用程式可能相依的競爭條件行為。</span><span class="sxs-lookup"><span data-stu-id="8ee86-136">Windows Vista (default): Provides the behavior with the race condition that apps might have a dependency on.</span></span> <span data-ttu-id="8ee86-137">必須在 Windows 7 行為之前避免此競爭的應用程式應該等候重迭的事件，並在收到信號時，呼叫 GetOverlappedResult 和 bWait = = FALSE。</span><span class="sxs-lookup"><span data-stu-id="8ee86-137">Apps that must avoid this race prior to the Windows 7 behavior should wait on the overlapped event and, when signaled, call GetOverlappedResult with bWait == FALSE.</span></span>

<span data-ttu-id="8ee86-138">**高對比模式中的 Shell 主題狀態**</span><span class="sxs-lookup"><span data-stu-id="8ee86-138">**Shell themes status in high contrast mode**</span></span>

-   <span data-ttu-id="8ee86-139">Windows 8：在高對比模式下，傳回實際的主題狀態。</span><span class="sxs-lookup"><span data-stu-id="8ee86-139">Windows 8: Returns the real theming status for when in high contrast mode.</span></span>
-   <span data-ttu-id="8ee86-140">Windows 7：因為 DWM 仍在開啟，所以在高對比模式中，會將主題傳回為無法使用。</span><span class="sxs-lookup"><span data-stu-id="8ee86-140">Windows 7: Returns theming as unavailable when in high contrast mode because DWM is still on.</span></span>
-   <span data-ttu-id="8ee86-141">Windows Vista (預設) ：在高對比模式中，因為 DWM 仍在開啟，所以會傳回無法使用的主題。</span><span class="sxs-lookup"><span data-stu-id="8ee86-141">Windows Vista (default): Returns theming as unavailable when in high contrast mode because DWM is still on.</span></span>

<span data-ttu-id="8ee86-142">**Shell iPersistFile：： Save 方法**</span><span class="sxs-lookup"><span data-stu-id="8ee86-142">**Shell iPersistFile::Save method**</span></span>

-   <span data-ttu-id="8ee86-143">Windows 8： CShellLink：： Save 現在會判斷是否以相對路徑引數呼叫 IPersistFile 處理常式，如果是，則會失敗。</span><span class="sxs-lookup"><span data-stu-id="8ee86-143">Windows 8: CShellLink::Save now determines if the IPersistFile handler is called with a relative path argument and fails the call if it is.</span></span>

    <span data-ttu-id="8ee86-144">描述此行為的 [公開檔](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) 指出路徑引數必須是絕對路徑：</span><span class="sxs-lookup"><span data-stu-id="8ee86-144">The [public documentation](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) describing this behavior indicates that path argument has to be an absolute path:</span></span>

-   <span data-ttu-id="8ee86-145">Windows 7 和舊版 (預設) ： CShellLink：： Save 無法判斷 iPersistFile 處理常式是否傳送相對路徑檢查，並允許應用程式繼續使用絕對或相對路徑。</span><span class="sxs-lookup"><span data-stu-id="8ee86-145">Windows 7 and earlier (default): CShellLink::Save does not determine if the iPersistFile handler sends a relative path check and allows apps to continue working with absolute or relative paths.</span></span>

<span data-ttu-id="8ee86-146">**程式相容性助理 (PCA)**</span><span class="sxs-lookup"><span data-stu-id="8ee86-146">**Program Compatibility Assistant (PCA)**</span></span>

-   <span data-ttu-id="8ee86-147">Windows 8：具有相容性區段的應用程式不會取得 PCA 緩和措施。</span><span class="sxs-lookup"><span data-stu-id="8ee86-147">Windows 8: Apps with the compatibility section do not get the PCA mitigation.</span></span>
-   <span data-ttu-id="8ee86-148">Windows 7：此檔) 所述的 Windows 8 (變更的潛在相容性問題，會追蹤具有相容性區段的應用程式。</span><span class="sxs-lookup"><span data-stu-id="8ee86-148">Windows 7: Apps with the compatibility section are tracked for potential compatibility issues for Windows 8 changes (described in this document).</span></span>
-   <span data-ttu-id="8ee86-149">Windows Vista (預設) ：在某些特定情況下無法正確安裝或在執行時間損毀的應用程式會讓 PCA 受到緩和。</span><span class="sxs-lookup"><span data-stu-id="8ee86-149">Windows Vista (default): Apps that fail to install properly or crash during runtime under some specific circumstances get the PCA mitigation.</span></span> <span data-ttu-id="8ee86-150">如需詳細資訊，請參閱 Resources 區段。</span><span class="sxs-lookup"><span data-stu-id="8ee86-150">For more info, see the Resources section.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="8ee86-151">運用功能功能</span><span class="sxs-lookup"><span data-stu-id="8ee86-151">Leveraging feature capabilities</span></span>

<span data-ttu-id="8ee86-152">使用作業系統支援的最新相容性資訊來更新應用程式資訊清單。</span><span class="sxs-lookup"><span data-stu-id="8ee86-152">Update the app manifest with the latest compatibility info for operating system support.</span></span> <span data-ttu-id="8ee86-153">本節描述資訊清單的新增專案：</span><span class="sxs-lookup"><span data-stu-id="8ee86-153">This section describes the additions to the manifest:</span></span>

<span data-ttu-id="8ee86-154">**命名空間：** 相容性。 v1 (xmlns = "urn：架構-microsoft-com：相容性 v1" >) </span><span class="sxs-lookup"><span data-stu-id="8ee86-154">**Namespace:** Compatibility.v1 (xmlns="urn:schemas-microsoft-com:compatibility.v1">)</span></span>

<span data-ttu-id="8ee86-155">**區段名稱：** (新區段的相容性) </span><span class="sxs-lookup"><span data-stu-id="8ee86-155">**Section name:** Compatibility (new section)</span></span>

<span data-ttu-id="8ee86-156">**SupportedOS：** 支援的作業系統 GUID-對應至受支援作業系統的 Guid 如下：</span><span class="sxs-lookup"><span data-stu-id="8ee86-156">**SupportedOS:** GUID of supported operating system - The GUIDs that map to the supported operating systems are:</span></span>

-   <span data-ttu-id="8ee86-157">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span><span class="sxs-lookup"><span data-stu-id="8ee86-157">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span></span>

    <span data-ttu-id="8ee86-158">針對 **Windows Vista**：這是 switchback 內容的預設值</span><span class="sxs-lookup"><span data-stu-id="8ee86-158">for **Windows Vista**: This is the default value for the switchback context</span></span>

-   <span data-ttu-id="8ee86-159">{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</span><span class="sxs-lookup"><span data-stu-id="8ee86-159">{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</span></span>

    <span data-ttu-id="8ee86-160">針對 **Windows 7**：在應用程式資訊清單中設定此值的應用程式會取得 Windows 7 行為</span><span class="sxs-lookup"><span data-stu-id="8ee86-160">for **Windows 7**: Apps that set this value in the app manifest get the Windows 7 behavior</span></span>

-   <span data-ttu-id="8ee86-161">{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}</span><span class="sxs-lookup"><span data-stu-id="8ee86-161">{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}</span></span>

    <span data-ttu-id="8ee86-162">針對 **Windows 8**：在應用程式資訊清單中設定此值的應用程式會取得 Windows 8 行為</span><span class="sxs-lookup"><span data-stu-id="8ee86-162">for **Windows 8**: Apps that set this value in the application manifest get the Windows 8 behavior</span></span>

<span data-ttu-id="8ee86-163">Microsoft 會視需要產生並張貼未來 Windows 版本的 Guid。</span><span class="sxs-lookup"><span data-stu-id="8ee86-163">Microsoft will generate and post GUIDs for future Windows versions as needed.</span></span>

<span data-ttu-id="8ee86-164">已更新之資訊清單的 XML 範例：</span><span class="sxs-lookup"><span data-stu-id="8ee86-164">An XML example of an updated manifest:</span></span>

> [!Note]  
> <span data-ttu-id="8ee86-165">應用程式資訊清單中的屬性和標記名稱會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="8ee86-165">The attribute and tag names in the app manifest are case sensitive.</span></span>

 


```XML
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
<compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
    <application> 
        <!--The ID below indicates app support for Windows Vista -->
        <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--The ID below indicates app support for Windows 7 -->
        <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--The ID below indicates app support for Windows 8 -->
        <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
    </application> 
</compatibility>
</assembly>
```



<span data-ttu-id="8ee86-166">上述範例中所有作業系統的 Guid 都提供下層支援。</span><span class="sxs-lookup"><span data-stu-id="8ee86-166">The GUIDs for all the operating systems in the previous example provide down-level support.</span></span> <span data-ttu-id="8ee86-167">支援多個平臺的應用程式不需要每個平臺都有不同的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="8ee86-167">Apps that support multiple platforms do not need separate manifests for each platform.</span></span>

## <a name="tests"></a><span data-ttu-id="8ee86-168">測試</span><span class="sxs-lookup"><span data-stu-id="8ee86-168">Tests</span></span>

<span data-ttu-id="8ee86-169">應用程式可以指定多個支援的作業系統識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ee86-169">An app can specify multiple supported operating system IDs.</span></span> <span data-ttu-id="8ee86-170">如果您已在該作業系統上測試或正在測試應用程式，則應該新增支援的作業系統識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ee86-170">You should add a supported operating system ID if you have tested, or are in the process of testing, the app on that operating system.</span></span> <span data-ttu-id="8ee86-171">Windows Vista 和先前的作業系統版本不會注意這些專案。</span><span class="sxs-lookup"><span data-stu-id="8ee86-171">Windows Vista and prior operating system versions do not pay attention to these entries.</span></span> <span data-ttu-id="8ee86-172">從 Windows 7 開始，Windows 會在資訊清單中選擇最高版本的 GUID，直到執行中的 Windows 版本，並提供該層級的應用程式支援。</span><span class="sxs-lookup"><span data-stu-id="8ee86-172">Starting with Windows 7, Windows will choose the highest version GUID in the manifest up to the running Windows version, and give the app support at that level.</span></span> <span data-ttu-id="8ee86-173">若要使用新的應用程式資訊清單相容性區段確認應用程式是否正常運作：</span><span class="sxs-lookup"><span data-stu-id="8ee86-173">To verify that the app works with the new app manifest compatibility section:</span></span>

1.  <span data-ttu-id="8ee86-174">使用新的相容性區段和 SupportedOS ID = {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} 測試應用程式，以確保應用程式能夠使用最新的 Windows 8 行為來正常運作。</span><span class="sxs-lookup"><span data-stu-id="8ee86-174">Test the app with the new compatibility section and SupportedOS ID = { 4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} to ensure that the app works properly using the latest Windows 8 behavior.</span></span>
2.  <span data-ttu-id="8ee86-175">使用新的相容性區段和 SupportedOS ID = {35138b9a-5d96-4fbd-8e2d-a2440225f93a} 測試應用程式，以確保應用程式能夠使用 Windows 7 行為正常運作。</span><span class="sxs-lookup"><span data-stu-id="8ee86-175">Test the app with the new compatibility section and SupportedOS ID = {35138b9a-5d96-4fbd-8e2d-a2440225f93a} to ensure that the app works properly using the Windows 7 behavior.</span></span>
3.  <span data-ttu-id="8ee86-176">使用新的相容性區段和 SupportedOS ID = {e2011457-1546-43c5-a5fe-008deee3d3f0} 測試應用程式，以確保應用程式能夠使用 Windows Vista 行為正常運作。</span><span class="sxs-lookup"><span data-stu-id="8ee86-176">Test the app with the new compatibility section and SupportedOS ID = {e2011457-1546-43c5-a5fe-008deee3d3f0} to ensure that the app works properly using the Windows Vista behavior.</span></span>

## <a name="resources"></a><span data-ttu-id="8ee86-177">資源</span><span class="sxs-lookup"><span data-stu-id="8ee86-177">Resources</span></span>

-   [<span data-ttu-id="8ee86-178">QueryActCtxW 函式</span><span class="sxs-lookup"><span data-stu-id="8ee86-178">QueryActCtxW Function</span></span>](../sbscs/application-manifests.md)
-   <span data-ttu-id="8ee86-179">[UAC 資訊清單](/previous-versions/bb756929(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="8ee86-179">[UAC manifest](/previous-versions/bb756929(v=msdn.10))</span></span>
-   [<span data-ttu-id="8ee86-180">Windows 應用程式的應用程式資訊清單</span><span class="sxs-lookup"><span data-stu-id="8ee86-180">Application Manifests for Windows Applications</span></span>](../sbscs/application-manifests.md)
-   [<span data-ttu-id="8ee86-181">桌面視窗管理員 (DWM) </span><span class="sxs-lookup"><span data-stu-id="8ee86-181">Desktop Window Manager (DWM)</span></span>](../dwm/dwm-overview.md)
-   [<span data-ttu-id="8ee86-182">內容不相符更新</span><span class="sxs-lookup"><span data-stu-id="8ee86-182">Context Mismatch Update</span></span>](https://support.microsoft.com/kb/978637)
-   <span data-ttu-id="8ee86-183">[程式相容性助理](/previous-versions/bb756937(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="8ee86-183">[Program Compatibility Assistant](/previous-versions/bb756937(v=msdn.10))</span></span>

 

 