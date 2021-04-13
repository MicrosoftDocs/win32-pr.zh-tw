---
title: Direct3D 9Ex 改善
description: 本主題說明 Windows 7 新增的翻轉模式支援，以及其在 Direct3D 9Ex 和桌面視窗管理員中相關聯的現有統計資料。
ms.assetid: cb92a162-57eb-4aee-af7a-c8ece37075a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42eef10b6caaa959cb750f073c97a0f665384463
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376229"
---
# <a name="direct3d-9ex-improvements"></a><span data-ttu-id="d467f-103">Direct3D 9Ex 改善</span><span class="sxs-lookup"><span data-stu-id="d467f-103">Direct3D 9Ex improvements</span></span>

<span data-ttu-id="d467f-104">本主題說明 Windows 7 新增的翻轉模式支援，以及其在 Direct3D 9Ex 和桌面視窗管理員中相關聯的現有統計資料。</span><span class="sxs-lookup"><span data-stu-id="d467f-104">This topic describes Windows 7's added support for Flip Mode Present and its associated present statistics in Direct3D 9Ex and Desktop Window Manager.</span></span> <span data-ttu-id="d467f-105">目標應用程式包括以影片或畫面播放速率為基礎的展示應用程式。</span><span class="sxs-lookup"><span data-stu-id="d467f-105">Target applications include video or frame rate-based presentation applications.</span></span> <span data-ttu-id="d467f-106">使用 Direct3D 9Ex Flip 模式的應用程式，可以在啟用 DWM 時減少系統資源載入。</span><span class="sxs-lookup"><span data-stu-id="d467f-106">Applications that use Direct3D 9Ex Flip Mode Present reduce the system resource load when DWM is enabled.</span></span> <span data-ttu-id="d467f-107">呈現與翻轉模式相關聯的統計資料增強功能，可讓 Direct3D 9Ex 應用程式藉由提供即時意見反應和修正機制，更有效地控制簡報的速率。</span><span class="sxs-lookup"><span data-stu-id="d467f-107">Present statistics enhancements associated with Flip Mode Present enable Direct3D 9Ex applications to better control the rate of presentation by providing real-time feedback and correction mechanisms.</span></span> <span data-ttu-id="d467f-108">內含範例資源的詳細說明和指標。</span><span class="sxs-lookup"><span data-stu-id="d467f-108">Detailed explanations and pointers to sample resources are included.</span></span>

<span data-ttu-id="d467f-109">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="d467f-109">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d467f-110">適用于 Windows 7 的 Direct3D 9Ex 改進功能</span><span class="sxs-lookup"><span data-stu-id="d467f-110">What's Improved about Direct3D 9Ex for Windows 7</span></span>](#whats-improved-about-direct3d-9ex-for-windows-7)
-   [<span data-ttu-id="d467f-111">Direct3D 9EX 翻轉模式簡報</span><span class="sxs-lookup"><span data-stu-id="d467f-111">Direct3D 9EX Flip Mode Presentation</span></span>](#direct3d-9ex-flip-mode-presentation)
-   [<span data-ttu-id="d467f-112">程式設計模型和 Api</span><span class="sxs-lookup"><span data-stu-id="d467f-112">Programming Model and APIs</span></span>](#programming-model-and-apis)
    -   [<span data-ttu-id="d467f-113">如何加入 Direct3D 9Ex Flip 模型</span><span class="sxs-lookup"><span data-stu-id="d467f-113">How to Opt Into the Direct3D 9Ex Flip Model</span></span>](#how-to-opt-into-the-direct3d-9ex-flip-model)
    -   [<span data-ttu-id="d467f-114">Direct3D 9Ex Flip 模型應用程式的設計指導方針</span><span class="sxs-lookup"><span data-stu-id="d467f-114">Design Guidelines for Direct3D 9Ex Flip Model Applications</span></span>](#design-guidelines-for-direct3d-9ex-flip-model-applications)
    -   [<span data-ttu-id="d467f-115">Direct3D 9Ex Flip 模型應用程式的框架同步處理</span><span class="sxs-lookup"><span data-stu-id="d467f-115">Frame Synchronization of Direct3D 9Ex Flip Model Applications</span></span>](#frame-synchronization-of-direct3d-9ex-flip-model-applications)
    -   [<span data-ttu-id="d467f-116">當 DWM 關閉時，視窗化應用程式的框架同步處理</span><span class="sxs-lookup"><span data-stu-id="d467f-116">Frame Synchronization for Windowed Applications When DWM is Off</span></span>](#frame-synchronization-for-windowed-applications-when-dwm-is-off)
-   [<span data-ttu-id="d467f-117">Direct3D 9Ex Flip 模型的逐步解說和目前的統計資料範例</span><span class="sxs-lookup"><span data-stu-id="d467f-117">Walk-Through of a Direct3D 9Ex Flip Model and Present Statistics Sample</span></span>](#walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample)
    -   [<span data-ttu-id="d467f-118">框架同步處理的程式設計建議摘要</span><span class="sxs-lookup"><span data-stu-id="d467f-118">Summary of Programming Recommendations for Frame Synchronization</span></span>](#summary-of-programming-recommendations-for-frame-synchronization)
-   [<span data-ttu-id="d467f-119">Direct3D 9Ex 改進的結論</span><span class="sxs-lookup"><span data-stu-id="d467f-119">Conclusion about Direct3D 9Ex Improvements</span></span>](#conclusion-about-direct3d-9ex-improvements)
-   [<span data-ttu-id="d467f-120">呼叫動作</span><span class="sxs-lookup"><span data-stu-id="d467f-120">Call to Action</span></span>](#call-to-action)
-   [<span data-ttu-id="d467f-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="d467f-121">Related topics</span></span>](#related-topics)

## <a name="whats-improved-about-direct3d-9ex-for-windows-7"></a><span data-ttu-id="d467f-122">適用于 Windows 7 的 Direct3D 9Ex 改進功能</span><span class="sxs-lookup"><span data-stu-id="d467f-122">What's Improved about Direct3D 9Ex for Windows 7</span></span>

<span data-ttu-id="d467f-123">Direct3D 9Ex 的翻轉模式展示是在 Direct3D 9Ex 中呈現影像的改良模式，可有效率地將轉譯的影像交給 Windows 7 桌面視窗管理員 (DWM) 以進行撰寫。</span><span class="sxs-lookup"><span data-stu-id="d467f-123">Flip Mode Presentation of Direct3D 9Ex is an improved mode of presenting images in Direct3D 9Ex that efficiently hands off rendered images to Windows 7 Desktop Window Manager (DWM) for composition.</span></span> <span data-ttu-id="d467f-124">從 Windows Vista 開始，DWM 撰寫了整個桌面。</span><span class="sxs-lookup"><span data-stu-id="d467f-124">Beginning in Windows Vista, DWM composes the entire Desktop.</span></span> <span data-ttu-id="d467f-125">啟用 DWM 時，視窗模式應用程式會使用名為 Blt 模式的方法，將其內容顯示在桌面上， (或 Blt 模型) 。</span><span class="sxs-lookup"><span data-stu-id="d467f-125">When DWM is enabled, windowed mode applications present their contents on the Desktop by using a method called Blt Mode Present to DWM (or Blt Model).</span></span> <span data-ttu-id="d467f-126">使用 Blt 模型時，DWM 會針對桌面組合維護一份 Direct3D 9Ex 呈現的表面。</span><span class="sxs-lookup"><span data-stu-id="d467f-126">With Blt Model, DWM maintains a copy of the Direct3D 9Ex rendered surface for Desktop composition.</span></span> <span data-ttu-id="d467f-127">當應用程式更新時，新的內容會透過 blt 複製到 DWM 介面。</span><span class="sxs-lookup"><span data-stu-id="d467f-127">When the application updates, the new content is copied to the DWM surface through a blt.</span></span> <span data-ttu-id="d467f-128">針對包含 Direct3D 和 GDI 內容的應用程式，GDI 資料也會複製到 DWM 介面上。</span><span class="sxs-lookup"><span data-stu-id="d467f-128">For applications that contain Direct3D and GDI content, the GDI data is also copied onto the DWM surface.</span></span>

<span data-ttu-id="d467f-129">在 Windows 7 中提供、DWM 的翻轉模式 (或翻轉模型) 是一種新的表示方法，基本上可讓您在視窗模式應用程式和 DWM 之間傳遞應用程式介面的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d467f-129">Available in Windows 7, Flip Mode Present to DWM (or Flip Model) is a new presentation method that essentially enables passing handles of application surfaces between windowed mode applications and DWM.</span></span> <span data-ttu-id="d467f-130">除了儲存資源，Flip 模型還支援增強的目前統計資料。</span><span class="sxs-lookup"><span data-stu-id="d467f-130">In addition to saving resources, Flip Model supports enhanced present statistics.</span></span>

<span data-ttu-id="d467f-131">目前的統計資料是應用程式可用來同步處理影片和音訊串流以及從影片播放問題中復原的畫面格時間資訊。</span><span class="sxs-lookup"><span data-stu-id="d467f-131">Present statistics are frame-timing information that applications can use to synchronize video and audio streams and recover from video playback glitches.</span></span> <span data-ttu-id="d467f-132">[目前的統計資料] 中的畫面格時間資訊可讓應用程式調整其影片畫面的呈現率，以提供更流暢的簡報。</span><span class="sxs-lookup"><span data-stu-id="d467f-132">The frame-timing information in present statistics allows applications to adjust the presentation rate of their video frames for smoother presentation.</span></span> <span data-ttu-id="d467f-133">在 Windows Vista 中，如果 DWM 針對桌面電腦群組合維護了一個對應的框架介面複本，則應用程式可以使用 DWM 提供的統計資料。</span><span class="sxs-lookup"><span data-stu-id="d467f-133">In Windows Vista, where DWM maintains a corresponding copy of the frame surface for Desktop composition, applications can use present statistics provided by DWM.</span></span> <span data-ttu-id="d467f-134">在 Windows 7 中，針對現有的應用程式，這種取得目前統計資料的方法仍會提供。</span><span class="sxs-lookup"><span data-stu-id="d467f-134">This method of obtaining present statistics will still be available in Windows 7 for existing applications.</span></span>

<span data-ttu-id="d467f-135">在 Windows 7 中，採用 Flip 模型的 Direct3D 9Ex 型應用程式應該使用 D3D9Ex Api 來取得目前的統計資料。</span><span class="sxs-lookup"><span data-stu-id="d467f-135">In Windows 7, Direct3D 9Ex-based applications that adopt Flip Model should use D3D9Ex APIs to obtain present statistics.</span></span> <span data-ttu-id="d467f-136">啟用 DWM 時，視窗模式和全螢幕獨佔模式 Direct3D 9Ex 應用程式在使用翻轉模型時，可能會預期出現相同的統計資料資訊。</span><span class="sxs-lookup"><span data-stu-id="d467f-136">When DWM is enabled, windowed mode and full-screen exclusive mode Direct3D 9Ex applications can expect the same present statistics information when using Flip Model.</span></span> <span data-ttu-id="d467f-137">Direct3D 9Ex Flip 模型目前的統計資料可讓應用程式即時查詢目前的統計資料，而不是在畫面上顯示畫面格之後：相同的現有統計資料資訊可供視窗模式 Flip-Model 啟用的應用程式作為全螢幕應用程式;D3D9Ex Api 中新增的旗標，可讓 Flip 模型應用程式有效地在呈現時捨棄延遲的畫面格。</span><span class="sxs-lookup"><span data-stu-id="d467f-137">Direct3D 9Ex Flip Model present statistics enable applications to query for present statistics in real time, rather than after the frame has been shown on screen; the same present statistics information is available for windowed-mode Flip-Model enabled applications as full-screen applications; an added flag in D3D9Ex APIs allows Flip Model applications to effectively discard late frames at presentation time.</span></span>

<span data-ttu-id="d467f-138">以 Windows 7 為目標的新影片或以畫面播放速率為基礎的簡報應用程式應該使用 Direct3D 9Ex Flip 模型。</span><span class="sxs-lookup"><span data-stu-id="d467f-138">Direct3D 9Ex Flip Model should be used by new video or frame rate-based presentation applications that target Windows 7.</span></span> <span data-ttu-id="d467f-139">由於 DWM 與 Direct3D 9Ex 執行時間之間的同步處理，使用翻轉模型的應用程式應指定2到 4 backbuffers，以確保呈現順暢。</span><span class="sxs-lookup"><span data-stu-id="d467f-139">Because of the synchronization between DWM and the Direct3D 9Ex runtime, applications that use Flip Model should specify between 2 to 4 backbuffers to ensure smooth presentation.</span></span> <span data-ttu-id="d467f-140">使用目前統計資料資訊的應用程式，將可受益于使用已啟用 Flip 模型的現有統計資料增強功能。</span><span class="sxs-lookup"><span data-stu-id="d467f-140">Those applications that use present statistics information will benefit from using Flip Model enabled present statistics enhancements.</span></span>

## <a name="direct3d-9ex-flip-mode-presentation"></a><span data-ttu-id="d467f-141">Direct3D 9EX 翻轉模式簡報</span><span class="sxs-lookup"><span data-stu-id="d467f-141">Direct3D 9EX Flip Mode Presentation</span></span>

<span data-ttu-id="d467f-142">當 DWM 開啟時，以及當應用程式處於視窗模式時（而非全螢幕獨佔模式），系統上的 Direct3D 9Ex 翻轉模式效能改進相當重要。</span><span class="sxs-lookup"><span data-stu-id="d467f-142">Performance improvements of Direct3D 9Ex Flip Mode Present are significant on the system when DWM is on and when the application is in windowed mode, rather than in full screen exclusive mode.</span></span> <span data-ttu-id="d467f-143">下表和圖例顯示記憶體頻寬使用量的簡化比較，以及選擇翻轉模型與預設使用量 Blt 模型的視窗化應用程式的系統讀取和寫入。</span><span class="sxs-lookup"><span data-stu-id="d467f-143">The following table and illustration show a simplified comparison of memory bandwidth usages and system reads and writes of windowed applications that choose Flip Model versus the default usage Blt Model.</span></span>



| <span data-ttu-id="d467f-144">Blt 模式存在於 DWM</span><span class="sxs-lookup"><span data-stu-id="d467f-144">Blt mode present to DWM</span></span>                                                                                                 | <span data-ttu-id="d467f-145">D3D9Ex 反轉模式存在於 DWM</span><span class="sxs-lookup"><span data-stu-id="d467f-145">D3D9Ex Flip Mode Present to DWM</span></span>                                             |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="d467f-146">1. 應用程式會更新其框架 (寫) </span><span class="sxs-lookup"><span data-stu-id="d467f-146">1. The application updates its frame (Write)</span></span><br/>                                                                 | <span data-ttu-id="d467f-147">1. 應用程式會更新其框架 (寫) </span><span class="sxs-lookup"><span data-stu-id="d467f-147">1. The application updates its frame (Write)</span></span><br/>                     |
| <span data-ttu-id="d467f-148">2. Direct3D runtime 會將介面內容複寫到 DWM 重新導向介面 (讀取、寫入) </span><span class="sxs-lookup"><span data-stu-id="d467f-148">2. Direct3D runtime copies surface contents to a DWM redirection surface (Read, Write)</span></span><br/>                       | <span data-ttu-id="d467f-149">2. Direct3D runtime 將應用程式介面傳遞至 DWM</span><span class="sxs-lookup"><span data-stu-id="d467f-149">2. Direct3D runtime passes the application surface to DWM</span></span><br/>        |
| <span data-ttu-id="d467f-150">3. 在共用表面複製完成之後，DWM 會將應用程式介面轉譯至螢幕 (讀取、寫入) </span><span class="sxs-lookup"><span data-stu-id="d467f-150">3. After the shared surface copy is completed, DWM renders the application surface onto screen (Read, Write)</span></span><br/> | <span data-ttu-id="d467f-151">3. DWM 將應用程式介面轉譯至螢幕 (讀取、寫入) </span><span class="sxs-lookup"><span data-stu-id="d467f-151">3. DWM renders the application surface onto screen (Read, Write)</span></span><br/> |



 

![比較 blt 模型和翻轉模型的圖例](images/blt-flip-mode-present.png)

<span data-ttu-id="d467f-153">Flip 模式存在：減少由 DWM 針對視窗化框架組合所撰寫的讀取和寫入次數，以減少系統記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="d467f-153">Flip Mode Present reduces system memory usage by reducing the number of reads and writes by the Direct3D runtime for the windowed frame composition by DWM.</span></span> <span data-ttu-id="d467f-154">這樣可減少系統電源耗用量和整體的記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="d467f-154">This reduces the system power consumption and overall memory usage.</span></span>

<span data-ttu-id="d467f-155">無論應用程式是在視窗模式或全螢幕獨佔模式中，應用程式都可以利用 Direct3D 9Ex 翻轉模式，在 DWM 開啟時顯示統計資料的增強功能。</span><span class="sxs-lookup"><span data-stu-id="d467f-155">Applications can take advantage of Direct3D 9Ex Flip Mode present statistics enhancements when DWM is on, regardless of whether the application is in windowed mode or in full screen exclusive mode.</span></span>

## <a name="programming-model-and-apis"></a><span data-ttu-id="d467f-156">程式設計模型和 Api</span><span class="sxs-lookup"><span data-stu-id="d467f-156">Programming Model and APIs</span></span>

<span data-ttu-id="d467f-157">新的影片或畫面播放速率：在 Windows 7 上使用 Direct3D 9Ex Api 的測量應用程式，可以利用在 Windows 7 上執行時，由翻轉模式所提供的記憶體和省電以及改良的簡報。</span><span class="sxs-lookup"><span data-stu-id="d467f-157">New video or frame rate-gauging applications that use Direct3D 9Ex APIs on Windows 7 can take advantage of the memory and power savings and of the improved presentation offered by Flip Mode Present when running on Windows 7.</span></span> <span data-ttu-id="d467f-158"> (在舊版 Windows 上執行時，Direct3D 執行時間會將應用程式預設為目前的 Blt 模式。 ) </span><span class="sxs-lookup"><span data-stu-id="d467f-158">(When running on previous Windows versions, the Direct3D runtime defaults the application to Blt Mode Present.)</span></span>

<span data-ttu-id="d467f-159">目前的翻轉模式會要求應用程式在 DWM 開啟時，可以利用即時目前的統計資料意見反應和修正機制。</span><span class="sxs-lookup"><span data-stu-id="d467f-159">Flip Mode Present entails that the application can take advantage of real-time present statistics feedback and correction mechanisms when DWM is on.</span></span> <span data-ttu-id="d467f-160">不過，使用「翻轉」模式的應用程式在使用並行 GDI API 轉譯時，應該要知道有何限制。</span><span class="sxs-lookup"><span data-stu-id="d467f-160">However, applications that use Flip Mode Present should be aware of limitations when they use concurrent GDI API rendering.</span></span>

<span data-ttu-id="d467f-161">您可以修改現有的應用程式，以利用新開發應用程式的相同優點和警告，來利用翻轉模式。</span><span class="sxs-lookup"><span data-stu-id="d467f-161">You can modify existing applications to take advantage of Flip Mode Present, with the same benefits and caveats as the newly developed applications.</span></span>

### <a name="how-to-opt-into-the-direct3d-9ex-flip-model"></a><span data-ttu-id="d467f-162">如何加入 Direct3D 9Ex Flip 模型</span><span class="sxs-lookup"><span data-stu-id="d467f-162">How to Opt Into the Direct3D 9Ex Flip Model</span></span>

<span data-ttu-id="d467f-163">以 Windows 7 為目標的 Direct3D 9Ex 應用程式可以藉由建立具有 [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) 列舉值的交換鏈，加入宣告 Flip 模型。</span><span class="sxs-lookup"><span data-stu-id="d467f-163">Direct3D 9Ex applications that target Windows 7 can opt into the Flip Model by creating the swap chain with the [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) enumeration value.</span></span> <span data-ttu-id="d467f-164">為了加入宣告 Flip 模型，應用程式會指定 [**D3DPRESENT \_ 參數**](/windows/desktop/direct3d9/d3dpresent-parameters) 結構，然後在呼叫 [**IDirect3D9Ex：： CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) API 時，傳遞此結構的指標。</span><span class="sxs-lookup"><span data-stu-id="d467f-164">To opt into the Flip Model, applications specify the [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) structure, and then pass a pointer to this structure when they call the [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) API.</span></span> <span data-ttu-id="d467f-165">本節說明以 Windows 7 為目標的應用程式如何使用 **IDirect3D9Ex：： CreateDeviceEx** 加入宣告 Flip 模型。</span><span class="sxs-lookup"><span data-stu-id="d467f-165">This section describes how applications that target Windows 7 use **IDirect3D9Ex::CreateDeviceEx** to opt into the Flip Model.</span></span> <span data-ttu-id="d467f-166">如需有關 **IDirect3D9Ex：： CreateDeviceEx** API 的詳細資訊，請參閱 **MSDN 上的 IDirect3D9Ex：： CreateDeviceEx**。</span><span class="sxs-lookup"><span data-stu-id="d467f-166">For more information about the **IDirect3D9Ex::CreateDeviceEx** API, see **IDirect3D9Ex::CreateDeviceEx on MSDN**.</span></span>

<span data-ttu-id="d467f-167">為了方便起見，這裡會重複 [**D3DPRESENT \_ 參數**](/windows/desktop/direct3d9/d3dpresent-parameters) 和 [**IDirect3D9Ex：： CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) 的語法。</span><span class="sxs-lookup"><span data-stu-id="d467f-167">For convenience, the syntax of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) and [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) is repeated here.</span></span>

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

``` syntax
typedef struct D3DPRESENT_PARAMETERS {
    UINT BackBufferWidth, BackBufferHeight;
    D3DFORMAT BackBufferFormat;
    UINT BackBufferCount;
    D3DMULTISAMPLE_TYPE MultiSampleType;
    DWORD MultiSampleQuality;
    D3DSWAPEFFECT SwapEffect;
    HWND hDeviceWindow;
    BOOL Windowed;
    BOOL EnableAutoDepthStencil;
    D3DFORMAT AutoDepthStencilFormat;
    DWORD Flags;
    UINT FullScreen_RefreshRateInHz;
    UINT PresentationInterval;
} D3DPRESENT_PARAMETERS, *LPD3DPRESENT_PARAMETERS;
```

<span data-ttu-id="d467f-168">當您修改 Windows 7 的 Direct3D 9Ex 應用程式以加入宣告 Flip 模型時，您應該考慮下列有關 [**D3DPRESENT \_ 參數**](/windows/desktop/direct3d9/d3dpresent-parameters)之指定成員的專案：</span><span class="sxs-lookup"><span data-stu-id="d467f-168">When you modify Direct3D 9Ex applications for Windows 7 to opt into the Flip Model, you should consider the following items about the specified members of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters):</span></span>

<dl> <dt>

<span data-ttu-id="d467f-169">**BackBufferCount**</span><span class="sxs-lookup"><span data-stu-id="d467f-169">**BackBufferCount**</span></span>
</dt> <dd>

<span data-ttu-id="d467f-170">僅 (Windows 7) </span><span class="sxs-lookup"><span data-stu-id="d467f-170">(Windows 7 Only)</span></span>

<span data-ttu-id="d467f-171">當 **SwapEffect** 設定為新的 D3DSWAPEFFECT \_ FLIPEX 交換鏈效果類型時，背景緩衝區計數應等於或大於2，以防止應用程式效能受到 DWM 等候上一個現有緩衝區釋放的結果影響。</span><span class="sxs-lookup"><span data-stu-id="d467f-171">When **SwapEffect** is set to the new D3DSWAPEFFECT\_FLIPEX swap chain effect type, the back buffer count should be equal or greater than 2, to prevent an application performance penalty as a result of waiting on the previous Present buffer to be released by DWM.</span></span>

<span data-ttu-id="d467f-172">當應用程式也使用與 D3DSWAPEFFECT FLIPEX 相關聯的現有統計資料時 \_ ，我們建議您將背景緩衝區計數設定為2到4。</span><span class="sxs-lookup"><span data-stu-id="d467f-172">When the application also uses present statistics associated with D3DSWAPEFFECT\_FLIPEX, we recommend that you set the back buffer count to from 2 to 4.</span></span>

<span data-ttu-id="d467f-173">\_在 Windows Vista 或舊版作業系統上使用 D3DSWAPEFFECT FLIPEX 將會從 [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)傳回失敗。</span><span class="sxs-lookup"><span data-stu-id="d467f-173">Using D3DSWAPEFFECT\_FLIPEX on Windows Vista or previous operating system versions will return fail from [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>

</dd> <dt>

<span data-ttu-id="d467f-174">**SwapEffect**</span><span class="sxs-lookup"><span data-stu-id="d467f-174">**SwapEffect**</span></span>
</dt> <dd>

<span data-ttu-id="d467f-175">僅 (Windows 7) </span><span class="sxs-lookup"><span data-stu-id="d467f-175">(Windows 7 Only)</span></span>

<span data-ttu-id="d467f-176">\_當應用程式採用具有 DWM 的翻轉模式時，新的 D3DSWAPEFFECT FLIPEX 交換鏈效果類型會指定。</span><span class="sxs-lookup"><span data-stu-id="d467f-176">The new D3DSWAPEFFECT\_FLIPEX swap chain effect type designates when an application is adopting Flip Mode Present to DWM.</span></span> <span data-ttu-id="d467f-177">它可讓應用程式更有效率地使用記憶體和電源，也可讓應用程式在視窗模式下利用全螢幕的顯示統計資料。</span><span class="sxs-lookup"><span data-stu-id="d467f-177">It allows the application more efficient usage of memory and power, and also enables the application to take advantage of full-screen present statistics in windowed mode.</span></span> <span data-ttu-id="d467f-178">全螢幕應用程式行為不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="d467f-178">Full-screen application behavior is not affected.</span></span> <span data-ttu-id="d467f-179">如果視窗化設定為 **TRUE** ，且 **SWAPEFFECT** 設定為 D3DSWAPEFFECT \_ FLIPEX，則執行時間會建立一個額外的背景緩衝區，並將任何控制碼都旋轉為在呈現時成為前端緩衝區的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d467f-179">If Windowed is set to **TRUE** and **SwapEffect** is set to D3DSWAPEFFECT\_FLIPEX, the runtime creates one extra back buffer and rotates whichever handle belongs to the buffer that becomes the front buffer at presentation time.</span></span>

</dd> <dt>

<span data-ttu-id="d467f-180">**旗標**</span><span class="sxs-lookup"><span data-stu-id="d467f-180">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="d467f-181">僅 (Windows 7) </span><span class="sxs-lookup"><span data-stu-id="d467f-181">(Windows 7 Only)</span></span>

<span data-ttu-id="d467f-182">如果 **SwapEffect** 設定為新的 [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect)交換鏈效果類型，則無法設定 [D3DPRESENTFLAG 可 \_ 鎖定 \_ 背景緩衝區](/windows/desktop/direct3d9/d3dpresentflag)旗標。</span><span class="sxs-lookup"><span data-stu-id="d467f-182">The [D3DPRESENTFLAG\_LOCKABLE\_BACKBUFFER](/windows/desktop/direct3d9/d3dpresentflag) flag cannot be set if **SwapEffect** is set to the new [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) swap chain effect type.</span></span>

</dd> </dl>

### <a name="design-guidelines-for-direct3d-9ex-flip-model-applications"></a><span data-ttu-id="d467f-183">Direct3D 9Ex Flip 模型應用程式的設計指導方針</span><span class="sxs-lookup"><span data-stu-id="d467f-183">Design Guidelines for Direct3D 9Ex Flip Model Applications</span></span>

<span data-ttu-id="d467f-184">使用下列各節中的指導方針來設計您的 Direct3D 9Ex Flip 模型應用程式。</span><span class="sxs-lookup"><span data-stu-id="d467f-184">Use the guidelines in the following sections to design your Direct3D 9Ex Flip Model applications.</span></span>

### <a name="use-flip-mode-present-in-a-separate-hwnd-from-blt-mode-present"></a><span data-ttu-id="d467f-185">在 Blt 模式的不同 HWND 中使用翻轉模式存在</span><span class="sxs-lookup"><span data-stu-id="d467f-185">Use Flip Mode Present in a Separate HWND from Blt Mode Present</span></span>

<span data-ttu-id="d467f-186">應用程式應該使用存在於其他 Api 未設為目標之 HWND 中的 Direct3D 9Ex Flip 模式，包括 Blt 模式目前的 Direct3D 9Ex、其他版本的 Direct3D 或 GDI。</span><span class="sxs-lookup"><span data-stu-id="d467f-186">Applications should use Direct3D 9Ex Flip Mode Present in an HWND that is not also targeted by other APIs, including Blt Mode Present Direct3D 9Ex, other versions of Direct3D, or GDI.</span></span> <span data-ttu-id="d467f-187">目前可以使用翻轉模式呈現給子視窗;也就是說，當應用程式不會在相同 HWND 中與 Blt 模型混合使用時，可以使用翻轉模型，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="d467f-187">Flip Mode Present can be used to present to child windows; that is, applications can use Flip Model when it is not mixed with Blt Model in the same HWND, as shown in the following illustrations.</span></span>

![direct3d 父視窗和 gdi 子視窗的圖例，每個視窗都有自己的 hwnd](images/parent-d3d.png)

![gdi 父視窗和 direct3d 子視窗的圖例，每個視窗都有自己的 hwnd](images/parent-gdi.png)

<span data-ttu-id="d467f-190">因為 Blt 模型會維護一個額外的介面複本，所以可以透過 Direct3D 和 GDI 的分次更新，將 GDI 和其他 Direct3D 內容新增至相同的 HWND。</span><span class="sxs-lookup"><span data-stu-id="d467f-190">Because Blt Model maintains an additional copy of the surface, GDI and other Direct3D contents can be added to the same HWND through piecemeal updates from Direct3D and GDI.</span></span> <span data-ttu-id="d467f-191">使用翻轉模型，只會顯示已傳遞至 DWM 之 [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) 交換鏈中的 Direct3D 9Ex 內容。</span><span class="sxs-lookup"><span data-stu-id="d467f-191">Using the Flip Model, only Direct3D 9Ex content in [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) swap chains that are passed to DWM will be visible.</span></span> <span data-ttu-id="d467f-192">將會忽略所有其他 Blt 模型 Direct3D 或 GDI 內容更新，如下列圖例所示。</span><span class="sxs-lookup"><span data-stu-id="d467f-192">All other Blt Model Direct3D or GDI content updates will be ignored, as shown in the following illustrations.</span></span>

![當使用 flip 模型，且 direct3d 和 gdi 內容在相同 hwnd 中時，可能不會顯示的 gdi 文字圖例](images/d3d-gdi-same-hwnd.png)

![在啟用 dwm 且應用程式處於視窗模式時的 direct3d 和 gdi 內容圖例](images/d3d-gdinotext-same-hwnd.png)

<span data-ttu-id="d467f-195">因此，您應該針對交換鏈緩衝區介面啟用翻轉模型，其中 Direct3D 9Ex Flip 模型會單獨轉譯成整個 HWND。</span><span class="sxs-lookup"><span data-stu-id="d467f-195">Therefore, Flip Model should be enabled for swap chain buffers surfaces where the Direct3D 9Ex Flip Model alone renders to the entire HWND.</span></span>

### <a name="do-not-use-flip-model-with-gdis-scrollwindow-or-scrollwindowex"></a><span data-ttu-id="d467f-196">請勿搭配 GDI 的 ScrollWindow 或 ScrollWindowEx 使用翻轉模型</span><span class="sxs-lookup"><span data-stu-id="d467f-196">Do Not Use Flip Model with GDI's ScrollWindow or ScrollWindowEx</span></span>

<span data-ttu-id="d467f-197">某些 Direct3D 9Ex 應用程式會在觸發使用者滾動事件時，使用 GDI 的 ScrollWindow 或 ScrollWindowEx 函數來更新視窗內容。</span><span class="sxs-lookup"><span data-stu-id="d467f-197">Some Direct3D 9Ex applications use GDI's ScrollWindow or ScrollWindowEx functions to update window contents when a user scroll event is triggered.</span></span> <span data-ttu-id="d467f-198">ScrollWindow 和 ScrollWindowEx 會在滾動視窗時，在螢幕上執行視窗內容的 blts。</span><span class="sxs-lookup"><span data-stu-id="d467f-198">ScrollWindow and ScrollWindowEx perform blts of window contents on screen as a window is scrolled.</span></span> <span data-ttu-id="d467f-199">這些函式也需要 GDI 和 Direct3D 9Ex 內容的 Blt 模型更新。</span><span class="sxs-lookup"><span data-stu-id="d467f-199">These functions also require Blt Model updates for GDI and Direct3D 9Ex content.</span></span> <span data-ttu-id="d467f-200">使用其中一種函式的應用程式不一定會在應用程式處於視窗模式且已啟用 DWM 的情況下，于畫面上顯示可見的視窗內容滾動。</span><span class="sxs-lookup"><span data-stu-id="d467f-200">Applications that use either function will not necessarily display visible window contents scrolling on screen when the application is in windowed mode and DWM is enabled.</span></span> <span data-ttu-id="d467f-201">建議您不要在應用程式中使用 GDI 的 ScrollWindow 和 ScrollWindowEx Api，而是改為在螢幕上重新繪製其內容以回應滾動。</span><span class="sxs-lookup"><span data-stu-id="d467f-201">We recommend that you not use GDI's ScrollWindow and ScrollWindowEx APIs in your applications, and instead redraw their contents on screen in response to scrolling.</span></span>

### <a name="use-one-d3dswapeffect_flipex-swap-chain-per-hwnd"></a><span data-ttu-id="d467f-202">\_每個 HWND 使用一個 D3DSWAPEFFECT FLIPEX 交換鏈</span><span class="sxs-lookup"><span data-stu-id="d467f-202">Use One D3DSWAPEFFECT\_FLIPEX Swap Chain per HWND</span></span>

<span data-ttu-id="d467f-203">使用翻轉模型的應用程式不應使用以相同 HWND 為目標的多個翻轉模型交換鏈。</span><span class="sxs-lookup"><span data-stu-id="d467f-203">Applications that use Flip Model should not use multiple Flip Model swap chains targeting the same HWND.</span></span>

### <a name="frame-synchronization-of-direct3d-9ex-flip-model-applications"></a><span data-ttu-id="d467f-204">Direct3D 9Ex Flip 模型應用程式的框架同步處理</span><span class="sxs-lookup"><span data-stu-id="d467f-204">Frame Synchronization of Direct3D 9Ex Flip Model Applications</span></span>

<span data-ttu-id="d467f-205">目前的統計資料是媒體應用程式用來同步處理影片和音訊串流以及從影片播放問題中復原的畫面格時間資訊。</span><span class="sxs-lookup"><span data-stu-id="d467f-205">Present statistics are frame timing information that media applications use to synchronize video and audio streams and recover from video playback glitches.</span></span> <span data-ttu-id="d467f-206">若要啟用目前的統計資料可用性，Direct3D 9Ex 應用程式必須確定應用程式傳遞給 [**IDirect3D9Ex：： CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)的 *BehaviorFlags* 參數包含裝置行為旗標 [D3DCREATE \_ enable \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate)。</span><span class="sxs-lookup"><span data-stu-id="d467f-206">To enable present statistics availability, the Direct3D 9Ex application must ensure that the *BehaviorFlags* parameter that the application passes to [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) contains the device behavior flag [D3DCREATE\_ENABLE\_PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate).</span></span>

<span data-ttu-id="d467f-207">為了方便起見， [**IDirect3D9Ex：： CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) 的語法會在此重複。</span><span class="sxs-lookup"><span data-stu-id="d467f-207">For convenience, the syntax of [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) is repeated here.</span></span>

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

<span data-ttu-id="d467f-208">Direct3D 9Ex Flip 模型會加入 [D3DPRESENT \_ FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent) 簡報旗標，以強制執行 [D3DPRESENT \_ 間隔 \_ 立即](/windows/desktop/direct3d9/d3dpresent) 呈現旗標行為。</span><span class="sxs-lookup"><span data-stu-id="d467f-208">Direct3D 9Ex Flip Model adds the [D3DPRESENT\_FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent) presentation flag that enforces the [D3DPRESENT\_INTERVAL\_IMMEDIATE](/windows/desktop/direct3d9/d3dpresent) presentation-flag behavior.</span></span> <span data-ttu-id="d467f-209">Direct3D 9Ex 應用程式會在應用程式傳遞給 IDirect3DDevice9Ex 的 *dwFlags* 參數中指定這些呈現旗標 [**：:P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex)，如下所示。</span><span class="sxs-lookup"><span data-stu-id="d467f-209">The Direct3D 9Ex application specifies these presentation flags in the *dwFlags* parameter that the application passes to [**IDirect3DDevice9Ex::PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex), as shown here.</span></span>

``` syntax
HRESULT PresentEx(
  CONST RECT *pSourceRect,
  CONST RECT *pDestRect,
  HWND hDestWindowOverride,
  CONST RGNDATA *pDirtyRegion,
  DWORD dwFlags
);
```

<span data-ttu-id="d467f-210">當您針對 Windows 7 修改 Direct3D 9Ex 應用程式時，您應該考慮下列有關指定 [D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) 簡報旗標的資訊：</span><span class="sxs-lookup"><span data-stu-id="d467f-210">When you modify your Direct3D 9Ex application for Windows 7, you should consider the following information about the specified [D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) presentation flags:</span></span>

<dl> <dt>

[<span data-ttu-id="d467f-211">D3DPRESENT \_ DONOTFLIP</span><span class="sxs-lookup"><span data-stu-id="d467f-211">D3DPRESENT\_DONOTFLIP</span></span>](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

<span data-ttu-id="d467f-212">此旗標僅適用于全螢幕模式或</span><span class="sxs-lookup"><span data-stu-id="d467f-212">This flag is available only in full-screen mode or</span></span>

<span data-ttu-id="d467f-213">僅 (Windows 7) </span><span class="sxs-lookup"><span data-stu-id="d467f-213">(Windows 7 Only)</span></span>

<span data-ttu-id="d467f-214">當應用程式在 [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)的呼叫中，將 [**D3DPRESENT \_ 參數**](/windows/desktop/direct3d9/d3dpresent-parameters)的 **SwapEffect** 成員設定為 [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) 。</span><span class="sxs-lookup"><span data-stu-id="d467f-214">when the application sets the **SwapEffect** member of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) to [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in a call to [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>

</dd> <dt>

[<span data-ttu-id="d467f-215">D3DPRESENT \_ FORCEIMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="d467f-215">D3DPRESENT\_FORCEIMMEDIATE</span></span>](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

<span data-ttu-id="d467f-216">僅 (Windows 7) </span><span class="sxs-lookup"><span data-stu-id="d467f-216">(Windows 7 Only)</span></span>

<span data-ttu-id="d467f-217">只有當應用程式在 [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)的呼叫中將 [**D3DPRESENT \_ 參數**](/windows/desktop/direct3d9/d3dpresent-parameters)的 **SwapEffect** 成員設定為 [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect)時，才能指定此旗標。</span><span class="sxs-lookup"><span data-stu-id="d467f-217">This flag can be specified only if the application sets the **SwapEffect** member of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) to [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in a call to [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span> <span data-ttu-id="d467f-218">應用程式可以使用此旗標，立即在 DWM 目前的佇列中更新具有數個框架的介面，基本上會略過中繼框架。</span><span class="sxs-lookup"><span data-stu-id="d467f-218">The application can use this flag to immediately update a surface with several frames later in the DWM Present queue, essentially skipping intermediate frames.</span></span>

<span data-ttu-id="d467f-219">啟用視窗 FlipEx 功能的應用程式可以使用此旗標，立即更新具有在 DWM 目前佇列中的框架，並略過中繼框架的介面。</span><span class="sxs-lookup"><span data-stu-id="d467f-219">Windowed FlipEx-enabled applications can use this flag to immediately update a surface with a frame that is later in the DWM Present queue, skipping intermediate frames.</span></span> <span data-ttu-id="d467f-220">如果媒體應用程式想要捨棄已偵測為最晚的畫面格，並在組合時顯示後續的畫面格，這特別有用。</span><span class="sxs-lookup"><span data-stu-id="d467f-220">This is especially useful for media applications that want to discard frames that have been detected as late and present subsequent frames at composition time.</span></span> <span data-ttu-id="d467f-221">[**IDirect3DDevice9Ex：**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) 如果未正確指定此旗標，:P resentex 會傳回不正確參數錯誤。</span><span class="sxs-lookup"><span data-stu-id="d467f-221">[**IDirect3DDevice9Ex::PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) returns invalid parameter error if this flag is improperly specified.</span></span>

</dd> </dl>

<span data-ttu-id="d467f-222">為了取得目前的統計資料資訊，應用程式會呼叫 [**IDirect3DSwapChain9Ex：： GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) API 來取得 [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats)結構。</span><span class="sxs-lookup"><span data-stu-id="d467f-222">To obtain present statistics information, the application obtains the [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure by calling the [**IDirect3DSwapChain9Ex::GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) API.</span></span>

<span data-ttu-id="d467f-223">[**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats)結構包含 [**IDirect3DDevice9Ex：:P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex)呼叫的相關統計資料。</span><span class="sxs-lookup"><span data-stu-id="d467f-223">The [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure contains statistics about [**IDirect3DDevice9Ex::PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) calls.</span></span> <span data-ttu-id="d467f-224">您必須使用 [**IDirect3D9Ex：： CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) 呼叫搭配 [D3DCREATE \_ ENABLE \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) 旗標來建立裝置。</span><span class="sxs-lookup"><span data-stu-id="d467f-224">The device must be created by using a [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) call with the [D3DCREATE\_ENABLE\_PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) flag.</span></span> <span data-ttu-id="d467f-225">否則， [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) 傳回的資料是未定義的。</span><span class="sxs-lookup"><span data-stu-id="d467f-225">Otherwise, the data returned by [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) is undefined.</span></span> <span data-ttu-id="d467f-226">啟用翻轉模型的 Direct3D 9Ex 交換鏈，可提供視窗內和全螢幕模式的統計資訊資訊。</span><span class="sxs-lookup"><span data-stu-id="d467f-226">A Flip-Model-enabled Direct3D 9Ex swap chain provides present statistics information in both windowed and full-screen modes.</span></span>

<span data-ttu-id="d467f-227">針對啟用 Blt 模型的 Direct3D 9Ex 在視窗模式中交換鏈，所有 [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) 結構值都是零。</span><span class="sxs-lookup"><span data-stu-id="d467f-227">For Blt-Model-enabled Direct3D 9Ex swap chains in windowed mode, all [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure values will be zeroes.</span></span>

<span data-ttu-id="d467f-228">針對 FlipEx 目前的統計資料， [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) 會 \_ \_ \_ 在下列情況下傳回 D3DERR 目前的統計資料：</span><span class="sxs-lookup"><span data-stu-id="d467f-228">For FlipEx present statistics, [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) returns D3DERR\_PRESENT\_STATISTICS\_DISJOINT in the following situations:</span></span>

-   <span data-ttu-id="d467f-229">第一次呼叫 [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) ，表示序列的開頭</span><span class="sxs-lookup"><span data-stu-id="d467f-229">First call to [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) ever, which indicates the beginning of a sequence</span></span>
-   <span data-ttu-id="d467f-230">從 on 到 off 的 DWM 轉換</span><span class="sxs-lookup"><span data-stu-id="d467f-230">DWM transition from on to off</span></span>
-   <span data-ttu-id="d467f-231">模式變更：以視窗模式切換至全螢幕或全螢幕到全螢幕轉換</span><span class="sxs-lookup"><span data-stu-id="d467f-231">Mode change: either windowed mode to or from full screen or full screen to full screen transitions</span></span>

<span data-ttu-id="d467f-232">為了方便起見，這裡會重複 [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) 的語法。</span><span class="sxs-lookup"><span data-stu-id="d467f-232">For convenience, the syntax of [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) is repeated here.</span></span>

``` syntax
HRESULT GetPresentStatistics(
  D3DPRESENTSTATS * pPresentationStatistics
);
```

<span data-ttu-id="d467f-233">[**IDirect3DSwapChain9Ex：： GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)方法會傳回最後一個 PresentCount，也就是與交換鏈相關聯之顯示裝置所建立的最後一個成功呼叫的目前識別碼。</span><span class="sxs-lookup"><span data-stu-id="d467f-233">The [**IDirect3DSwapChain9Ex::GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) method returns the last PresentCount, that is, the Present ID of the last successful Present call that was made by a display device that is associated with the swap chain.</span></span> <span data-ttu-id="d467f-234">此存在識別碼是 [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats)結構之 **PresentCount** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="d467f-234">This Present ID is the value of the **PresentCount** member of the [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure.</span></span> <span data-ttu-id="d467f-235">針對啟用 Blt 模型的 Direct3D 9Ex 交換鏈，在視窗模式中，所有 **D3DPRESENTSTATS** 結構值都是零。</span><span class="sxs-lookup"><span data-stu-id="d467f-235">For Blt-Model-enabled Direct3D 9Ex swap chains, while in windowed mode, all **D3DPRESENTSTATS** structure values will be zeroes.</span></span>

<span data-ttu-id="d467f-236">為了方便起見， [**IDirect3DSwapChain9Ex：： GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) 的語法會在此重複。</span><span class="sxs-lookup"><span data-stu-id="d467f-236">For convenience, the syntax of [**IDirect3DSwapChain9Ex::GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) is repeated here.</span></span>

``` syntax
HRESULT GetLastPresentCount(
  UINT * pLastPresentCount
);
```

<span data-ttu-id="d467f-237">當您針對 Windows 7 修改 Direct3D 9Ex 應用程式時，您應該考慮下列有關 [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) 結構的資訊：</span><span class="sxs-lookup"><span data-stu-id="d467f-237">When you modify your Direct3D 9Ex application for Windows 7, you should consider the following information about the [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure:</span></span>

-   <span data-ttu-id="d467f-238">[**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)傳回的 PresentCount 值不會在 [](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) \_ *DONOTWAIT* 參數中指定 D3DPRESENT dwFlags 的 PresentEx 呼叫傳回失敗時進行更新。</span><span class="sxs-lookup"><span data-stu-id="d467f-238">The PresentCount value that [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) returns does not update when a [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) call with D3DPRESENT\_DONOTWAIT specified in the *dwFlags* parameter returns failure.</span></span>
-   <span data-ttu-id="d467f-239">使用 D3DPRESENT DONOTFLIP 呼叫 [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) 時 \_ ， [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) 呼叫會成功，但當應用程式處於視窗模式時，則不會傳回更新的 [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) 結構。</span><span class="sxs-lookup"><span data-stu-id="d467f-239">When [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) is called with D3DPRESENT\_DONOTFLIP, a [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) call succeeds but does not return an updated [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure when the application is in windowed mode.</span></span>
-   <span data-ttu-id="d467f-240">[**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats)中的 **PresentRefreshCount** 與 **SyncRefreshCount** ：</span><span class="sxs-lookup"><span data-stu-id="d467f-240">**PresentRefreshCount** versus **SyncRefreshCount** in [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats):</span></span>
    -   <span data-ttu-id="d467f-241">當應用程式在每個 vsync 上呈現時， **PresentRefreshCount** 等於 **SyncRefreshCount** 。</span><span class="sxs-lookup"><span data-stu-id="d467f-241">**PresentRefreshCount** is equal to **SyncRefreshCount** when the application presents on every vsync.</span></span>
    -   <span data-ttu-id="d467f-242">當提交目前的時間時，會在 vsync 間隔取得 **SyncRefreshCount** ， **SyncQPCTime** 大約是與 vsync 間隔相關聯的時間。</span><span class="sxs-lookup"><span data-stu-id="d467f-242">**SyncRefreshCount** is obtained on the vsync interval when the present was submitted, **SyncQPCTime** is approximately the time associated with the vsync interval.</span></span>

``` syntax
typedef struct _D3DPRESENTSTATS {
    UINT PresentCount;
    UINT PresentRefreshCount;
    UINT SyncRefreshCount;
    LARGE_INTEGER SyncQPCTime;
    LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```

### <a name="frame-synchronization-for-windowed-applications-when-dwm-is-off"></a><span data-ttu-id="d467f-243">當 DWM 關閉時，視窗化應用程式的框架同步處理</span><span class="sxs-lookup"><span data-stu-id="d467f-243">Frame Synchronization for Windowed Applications When DWM is Off</span></span>

<span data-ttu-id="d467f-244">當 DWM 為 off 時，視窗型應用程式會直接顯示到監視器畫面，而不會通過翻轉鏈。</span><span class="sxs-lookup"><span data-stu-id="d467f-244">When DWM is off, windowed applications display directly to the monitor screen without going through a flip chain.</span></span> <span data-ttu-id="d467f-245">在 Windows Vista 中，當 DWM 為 off 時，不支援取得視窗型應用程式的畫面格統計資訊。</span><span class="sxs-lookup"><span data-stu-id="d467f-245">In Windows Vista, there is no support for obtaining frame statistics information for windowed applications when DWM is off.</span></span> <span data-ttu-id="d467f-246">為了維護應用程式不需要 DWM 感知的 API，當 DWM 為 off 時，Windows 7 會傳回視窗型應用程式的框架統計資訊。</span><span class="sxs-lookup"><span data-stu-id="d467f-246">To maintain an API where applications need not be DWM- aware, Windows 7 will return frame statistics information for windowed applications when DWM is off.</span></span> <span data-ttu-id="d467f-247">當 DWM 為 off 時所傳回的框架統計資料只是估計。</span><span class="sxs-lookup"><span data-stu-id="d467f-247">The frame statistics returned when DWM is off are estimations only.</span></span>

## <a name="walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample"></a><span data-ttu-id="d467f-248">Direct3D 9Ex Flip 模型的 Walk-Through 和目前的統計資料範例</span><span class="sxs-lookup"><span data-stu-id="d467f-248">Walk-Through of a Direct3D 9Ex Flip Model and Present Statistics Sample</span></span>

<span data-ttu-id="d467f-249">**加入宣告 FlipEx presentation for Direct3D 9Ex 範例**</span><span class="sxs-lookup"><span data-stu-id="d467f-249">**To opt into FlipEx presentation for Direct3D 9Ex sample**</span></span>

1.  <span data-ttu-id="d467f-250">確定範例應用程式是在 Windows 7 或更新版本的作業系統版本上執行。</span><span class="sxs-lookup"><span data-stu-id="d467f-250">Ensure the sample application is running on Windows 7 or later operating system version.</span></span>
2.  <span data-ttu-id="d467f-251">在 [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)的呼叫中，將 [**D3DPRESENT \_ 參數**](/windows/desktop/direct3d9/d3dpresent-parameters)的 **SwapEffect** 成員設定為 [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) 。</span><span class="sxs-lookup"><span data-stu-id="d467f-251">Set the **SwapEffect** member of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) to [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in a call to [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>


```C++
    OSVERSIONINFO version;
    ZeroMemory(&version, sizeof(version));
    version.dwOSVersionInfoSize = sizeof(version);
    GetVersionEx(&version);
    
    // Sample would run only on Win7 or higher
    // Flip Model present and its associated present statistics behavior are only available on Windows 7 or higher operating system
    bool bIsWin7 = (version.dwMajorVersion > 6) || 
        ((version.dwMajorVersion == 6) && (version.dwMinorVersion >= 1));

    if (!bIsWin7)
    {
        MessageBox(NULL, L"This sample requires Windows 7 or higher", NULL, MB_OK);
        return 0;
    }
```



<span data-ttu-id="d467f-252">**若要同時加入宣告與 Direct3D 9Ex 範例相關聯的現有統計資料 FlipEx**</span><span class="sxs-lookup"><span data-stu-id="d467f-252">**To also opt into FlipEx associated Present Statistics for Direct3D 9Ex sample**</span></span>

-   <span data-ttu-id="d467f-253">Set [D3DCREATE \_ ENABLE \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) in [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)的 *BehaviorFlags* 參數。</span><span class="sxs-lookup"><span data-stu-id="d467f-253">Set [D3DCREATE\_ENABLE\_PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) in the *BehaviorFlags* parameter of [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>


```C++
    // Set up the structure used to create the D3DDevice
    D3DPRESENT_PARAMETERS d3dpp;
    ZeroMemory(&d3dpp, sizeof(d3dpp));

    d3dpp.Windowed = TRUE;
    d3dpp.SwapEffect = D3DSWAPEFFECT_FLIPEX;        // Opts into Flip Model present for D3D9Ex swapchain
    d3dpp.BackBufferFormat = D3DFMT_X8R8G8B8;
    d3dpp.BackBufferWidth = 256;                
    d3dpp.BackBufferHeight = 256;
    d3dpp.BackBufferCount = QUEUE_SIZE;
    d3dpp.PresentationInterval = D3DPRESENT_INTERVAL_ONE;

    g_iWidth = d3dpp.BackBufferWidth;
    g_iHeight = d3dpp.BackBufferHeight;

    // Create the D3DDevice with present statistics enabled - set D3DCREATE_ENABLE_PRESENTSTATS for behaviorFlags parameter
    if(FAILED(g_pD3D->CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                      D3DCREATE_HARDWARE_VERTEXPROCESSING | D3DCREATE_ENABLE_PRESENTSTATS,
                                      &d3dpp, NULL, &g_pd3dDevice)))
    {
        return E_FAIL;
    }
```



<span data-ttu-id="d467f-254">**若要避免，請偵測並從問題中復原**</span><span class="sxs-lookup"><span data-stu-id="d467f-254">**To avoid, detect and recover from glitches**</span></span>

1.  <span data-ttu-id="d467f-255">佇列目前的呼叫：建議的背景緩衝區計數是從2到4。</span><span class="sxs-lookup"><span data-stu-id="d467f-255">Queue Present calls: recommended backbuffer count is from 2 to 4.</span></span>
2.  <span data-ttu-id="d467f-256">Direct3D 9Ex 範例會新增隱含背景緩衝區，實際的目前佇列長度為背景緩衝區計數 + 1。</span><span class="sxs-lookup"><span data-stu-id="d467f-256">Direct3D 9Ex sample adds an implicit backbuffer, actual Present queue length is backbuffer count + 1.</span></span>
3.  <span data-ttu-id="d467f-257">建立協助程式目前的佇列結構，以將所有成功提交的現有識別碼儲存 (PresentCount) 以及相關聯、已計算/預期的 PresentRefreshCount。</span><span class="sxs-lookup"><span data-stu-id="d467f-257">Create helper Present queue structure to store all successfully submitted Present's Present ID (PresentCount) and associated, calculated/expected PresentRefreshCount.</span></span>
4.  <span data-ttu-id="d467f-258">若要偵測出問題發生：</span><span class="sxs-lookup"><span data-stu-id="d467f-258">To detect glitch occurrence:</span></span>

    -   <span data-ttu-id="d467f-259">呼叫 [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d467f-259">Call [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)).</span></span>
    -   <span data-ttu-id="d467f-260">取得 (PresentCount) 的目前識別碼，以及顯示所顯示之統計資料的 vsync 計數 (PresentRefreshCount) 的框架。</span><span class="sxs-lookup"><span data-stu-id="d467f-260">Get the Present ID (PresentCount) and vsync count where the frame is shown (PresentRefreshCount) of the frame whose present statistics is obtained.</span></span>
    -   <span data-ttu-id="d467f-261">在與目前識別碼相關聯的範例程式碼) 中，取出預期的 PresentRefreshCount (TargetRefresh。</span><span class="sxs-lookup"><span data-stu-id="d467f-261">Retrieve the expected PresentRefreshCount (TargetRefresh in sample code) associated with the Present ID.</span></span>
    -   <span data-ttu-id="d467f-262">如果實際的 PresentRefreshCount 晚于預期，就會發生問題。</span><span class="sxs-lookup"><span data-stu-id="d467f-262">If actual PresentRefreshCount is later than expected, a glitch has occurred.</span></span>

5.  <span data-ttu-id="d467f-263">若要從問題中復原：</span><span class="sxs-lookup"><span data-stu-id="d467f-263">To recover from glitch:</span></span>

    -   <span data-ttu-id="d467f-264">計算 \_ 範例程式碼) 中 (g iImmediates 變數略過的框架數目。</span><span class="sxs-lookup"><span data-stu-id="d467f-264">Calculate how many frames to skip (g\_ iImmediates variable in sample code).</span></span>
    -   <span data-ttu-id="d467f-265">以 interval D3DPRESENT FORCEIMMEDIATE 呈現略過的框架 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d467f-265">Present the skipped frames with interval D3DPRESENT\_FORCEIMMEDIATE.</span></span>

<span data-ttu-id="d467f-266">**故障偵測和復原的考慮**</span><span class="sxs-lookup"><span data-stu-id="d467f-266">**Considerations for glitch detection and recovery**</span></span>

1.  <span data-ttu-id="d467f-267">損毀修復會在範例程式碼中使用 N (g \_ iQueueDelay 變數) 出現的呼叫數，其中 N (g \_ iQueueDelay) 等於 g \_ IImmediates 加上目前佇列的長度，也就是：</span><span class="sxs-lookup"><span data-stu-id="d467f-267">Glitch recovery takes N (g\_iQueueDelay variable in sample code) number of Present calls where N (g\_iQueueDelay) equals g\_iImmediates plus length of the Present queue, that is:</span></span>

    -   <span data-ttu-id="d467f-268">略過具有出現間隔的框架 D3DPRESENT \_ FORCEIMMEDIATE，加上</span><span class="sxs-lookup"><span data-stu-id="d467f-268">Skipping frames with Present interval D3DPRESENT\_FORCEIMMEDIATE, plus</span></span>
    -   <span data-ttu-id="d467f-269">需要處理的佇列呈現</span><span class="sxs-lookup"><span data-stu-id="d467f-269">Queued Presents that need to be processed</span></span>

2.  <span data-ttu-id="d467f-270">在範例) 中，將限制設定為問題的 (故障 \_ 修復 \_ 限制。</span><span class="sxs-lookup"><span data-stu-id="d467f-270">Set a limit to the glitch length (GLITCH\_RECOVERY\_LIMIT in sample).</span></span> <span data-ttu-id="d467f-271">如果範例應用程式無法從太長 (（例如，1秒）或在60Hz 監視器) 上的 60 vsyncs 復原，請跳過間歇性的動畫，並重設目前的協助程式佇列。</span><span class="sxs-lookup"><span data-stu-id="d467f-271">If the sample application cannot recover from a glitch that is too long (that is say, 1 second, or 60 vsyncs on 60Hz monitor), jump over the intermittent animation and reset the Present helper queue.</span></span>


```C++
VOID Render()
{
    g_pd3dDevice->Clear(0, NULL, D3DCLEAR_TARGET, D3DCOLOR_XRGB(0, 0, 0), 1.0f, 0);

    g_pd3dDevice->BeginScene();

    // Compute new animation parameters for time and frame based animations

    // Time-based is a difference between base and current SyncRefreshCount
    g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
    // Frame-based is incrementing frame value
    g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;

    RenderBlurredMesh(TRUE);    // Time-based
    RenderBlurredMesh(FALSE);   // Frame-based

    g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;

    DrawText();

    g_pd3dDevice->EndScene();

    // Performs glitch recovery if glitch was detected
    if (g_bGlitchRecovery && (g_iImmediates > 0))
    {
        // If we have present immediates queued as a result of glitch detected, issue forceimmediate Presents for glitch recovery 
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE);
        g_iImmediates--;
        g_iShowingGlitchRecovery = MESSAGE_SHOW;
    }
    // Otherwise, Present normally
    else
    {
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, 0);
    }

    // Add to helper Present queue: PresentID + expected present refresh count of last submitted Present
    UINT PresentCount;
    g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
    g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);
    
    // QueueDelay specifies # Present calls to be processed before another glitch recovery attempt
    if (g_iQueueDelay > 0)
    {
        g_iQueueDelay--;
    }

    if (g_bGlitchRecovery)
    {
        // Additional DONOTFLIP presents for frame conversions, which basically follows the same logic, but without rendering
        for (DWORD i = 0; i < g_iDoNotFlipNum; i++)
        {
            if (g_TargetRefreshCount != -1)
            {
                g_TargetRefreshCount++;
                g_iFrameNumber++;
                g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
                g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;
                g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;
            }
            
            if (g_iImmediates > 0)
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE | D3DPRESENT_DONOTFLIP);
                g_iImmediates--;
            }
            else
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_DONOTFLIP);
            }
            UINT PresentCount;
            g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
            g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);

            if (g_iQueueDelay > 0)
            {
                g_iQueueDelay--;
            }
        }
    }

    // Check Present Stats info for glitch detection 
    D3DPRESENTSTATS PresentStats;

    // Obtain present statistics information for successfully displayed presents
    HRESULT hr = g_pd3dSwapChain->GetPresentStats(&PresentStats);

    if (SUCCEEDED(hr))
    {
        // Time-based update
        g_LastSyncRefreshCount = PresentStats.SyncRefreshCount;
        if ((g_SyncRefreshCount == -1) && (PresentStats.PresentCount != 0))
        {
            // First time SyncRefreshCount is reported, use it as base
            g_SyncRefreshCount = PresentStats.SyncRefreshCount;
        }

        // Fetch frame from the queue...
        UINT TargetRefresh = g_Queue.DequeueFrame(PresentStats.PresentCount);

        // If PresentStats returned a really old frame that we no longer have in the queue, just don't do any glitch detection
        if (TargetRefresh == FRAME_NOT_FOUND)
            return;

        if (g_TargetRefreshCount == -1)
        {
            // This is first time issued frame is confirmed by present stats, so fill target refresh count for all frames in the queue
            g_TargetRefreshCount = g_Queue.FillRefreshCounts(PresentStats.PresentCount, g_SyncRefreshCount);
        } 
        else
        {
            g_TargetRefreshCount++;
            g_iFrameNumber++;

            // To determine whether we're glitching, see if our estimated refresh count is confirmed
            // if the frame is displayed later than the expected vsync count
            if (TargetRefresh < PresentStats.PresentRefreshCount)
            {
                // then, glitch is detected!

                // If glitch is too big, don't bother recovering from it, just jump animation
                if ((PresentStats.PresentRefreshCount - TargetRefresh) > GLITCH_RECOVERY_LIMIT)
                {
                    g_iStartFrame += PresentStats.SyncRefreshCount - g_SyncRefreshCount;
                    ResetAnimation();
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;    
                } 
                // Otherwise, compute number of immediate presents to recover from it -- if we?re not still trying to recover from another glitch
                else if (g_iQueueDelay == 0)
                {
                      // skip frames to catch up to expected refresh count
                    g_iImmediates = PresentStats.PresentRefreshCount - TargetRefresh;
                    // QueueDelay specifies # Present calls before another glitch recovery 
                    g_iQueueDelay = g_iImmediates + QUEUE_SIZE;
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;
                }
            }
            else
            {
                // No glitch, reset glitch count
                g_iGlitchesInaRow = 0;
            }
        }
    }
    else if (hr == D3DERR_PRESENT_STATISTICS_DISJOINT)
    {
        // D3DERR_PRESENT_STATISTICS_DISJOINT means measurements should be started from the scratch (could be caused by mode change or DWM on/off transition)
        ResetAnimation();
    }

    // If we got too many glitches in a row, reduce framerate conversion factor (that is, render less frames)
    if (g_iGlitchesInaRow == FRAMECONVERSION_GLITCH_LIMIT)
    {
        if (g_iDoNotFlipNum < FRAMECONVERSION_LIMIT)
        {
            g_iDoNotFlipNum++;
        }
        g_iGlitchesInaRow = 0;
        g_iShowingDoNotFlipBump = MESSAGE_SHOW;
    }
}
```



<span data-ttu-id="d467f-272">**範例案例**</span><span class="sxs-lookup"><span data-stu-id="d467f-272">**Sample scenario**</span></span>

-   <span data-ttu-id="d467f-273">下圖顯示背景緩衝區計數為4的應用程式。</span><span class="sxs-lookup"><span data-stu-id="d467f-273">The following illustration shows an application with backbuffer count of 4.</span></span> <span data-ttu-id="d467f-274">實際的出現佇列長度為5。</span><span class="sxs-lookup"><span data-stu-id="d467f-274">The actual Present queue length is therefore 5.</span></span>

    ![applicas 轉譯的畫面格和呈現佇列的圖例](images/sample-scenario.png)

    <span data-ttu-id="d467f-276">畫面格 A 的目標是在同步間隔計數為1時進入螢幕上的畫面，但偵測到它顯示于同步間隔計數4。</span><span class="sxs-lookup"><span data-stu-id="d467f-276">Frame A is targeted to go on screen on sync interval count of 1 but was detected that it was shown on sync interval count of 4.</span></span> <span data-ttu-id="d467f-277">因此發生問題。</span><span class="sxs-lookup"><span data-stu-id="d467f-277">Therefore a glitch has occurred.</span></span> <span data-ttu-id="d467f-278">後續3個畫面格會以 D3DPRESENT \_ INTERVAL \_ FORCEIMMEDIATE 呈現。</span><span class="sxs-lookup"><span data-stu-id="d467f-278">Subsequent 3 frames are presented with D3DPRESENT\_INTERVAL\_FORCEIMMEDIATE.</span></span> <span data-ttu-id="d467f-279">在復原之前，問題應該總共有8個出現的呼叫-下一個畫面會根據其目標同步間隔計數來顯示。</span><span class="sxs-lookup"><span data-stu-id="d467f-279">The glitch should take a total of 8 Present calls before it is recovered - the next frame will be shown as per its targeted sync interval count.</span></span>

### <a name="summary-of-programming-recommendations-for-frame-synchronization"></a><span data-ttu-id="d467f-280">框架同步處理的程式設計建議摘要</span><span class="sxs-lookup"><span data-stu-id="d467f-280">Summary of Programming Recommendations for Frame Synchronization</span></span>

-   <span data-ttu-id="d467f-281">建立所有 LastPresentCount 識別碼的備份清單， (透過) [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) 取得的所有識別碼，以及所有提交的相關預估 PresentRefreshCount。</span><span class="sxs-lookup"><span data-stu-id="d467f-281">Create a backup list of all the LastPresentCount IDs (obtained via [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)) and associated estimated PresentRefreshCount of all the Presents submitted.</span></span>
    > [!Note]  
    > <span data-ttu-id="d467f-282">當應用程式使用 D3DPRESENT DONOTFLIP 呼叫 [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) 時 \_ ， [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) 呼叫會成功，但當應用程式處於視窗模式時，則不會傳回更新的 [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) 結構。</span><span class="sxs-lookup"><span data-stu-id="d467f-282">When the application calls [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) with D3DPRESENT\_DONOTFLIP, the [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) call succeeds but does not return an updated [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure when the application is in windowed mode.</span></span>

     

-   <span data-ttu-id="d467f-283">呼叫 [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) 來取得與所顯示的每個畫面格目前識別碼相關聯的實際 PresentRefreshCount，以確保應用程式處理失敗時，會從呼叫傳回。</span><span class="sxs-lookup"><span data-stu-id="d467f-283">Call [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) to obtain the actual PresentRefreshCount associated with each Present ID of frames shown, to make sure that the application handles failure returns from the call.</span></span>
-   <span data-ttu-id="d467f-284">如果實際 PresentRefreshCount 晚于預估 PresentRefreshCount，則會偵測到問題。</span><span class="sxs-lookup"><span data-stu-id="d467f-284">If actual PresentRefreshCount is later than estimated PresentRefreshCount, a glitch is detected.</span></span> <span data-ttu-id="d467f-285">藉由提交延遲的畫面格來彌補 D3DPRESENT \_ FORCEIMMEDIATE。</span><span class="sxs-lookup"><span data-stu-id="d467f-285">Compensate by submitting lagging frames' Present with D3DPRESENT\_FORCEIMMEDIATE.</span></span>
-   <span data-ttu-id="d467f-286">當目前的佇列中有一個畫面格出現時，所有後續排入佇列的框架都會延遲出現。</span><span class="sxs-lookup"><span data-stu-id="d467f-286">When one frame is presented late in the Present queue, all subsequent queued frames will be presented late.</span></span> <span data-ttu-id="d467f-287">D3DPRESENT \_ FORCEIMMEDIATE 將只會更正下一個要在所有已排入佇列的框架之後呈現的畫面格。</span><span class="sxs-lookup"><span data-stu-id="d467f-287">D3DPRESENT\_FORCEIMMEDIATE will correct only the next frame to be presented after all the queued frames.</span></span> <span data-ttu-id="d467f-288">因此，目前的佇列或背景緩衝區計數不應該太長，因此不太能趕上畫面格的問題。</span><span class="sxs-lookup"><span data-stu-id="d467f-288">Therefore, the Present queue or backbuffer count should not be too long -- so there are less frame glitches to catch up with.</span></span> <span data-ttu-id="d467f-289">最佳背景緩衝區計數是2到4。</span><span class="sxs-lookup"><span data-stu-id="d467f-289">The optimal backbuffer count is 2 to 4.</span></span>
-   <span data-ttu-id="d467f-290">如果估計的 PresentRefreshCount 晚于實際的 PresentRefreshCount，則可能發生 DWM 節流。</span><span class="sxs-lookup"><span data-stu-id="d467f-290">If estimated PresentRefreshCount is later than the actual PresentRefreshCount, DWM throttling might have occurred.</span></span> <span data-ttu-id="d467f-291">可能的解決方案如下：</span><span class="sxs-lookup"><span data-stu-id="d467f-291">The following solutions are possible:</span></span>

    -   <span data-ttu-id="d467f-292">減少目前的佇列長度</span><span class="sxs-lookup"><span data-stu-id="d467f-292">reducing Present queue length</span></span>
    -   <span data-ttu-id="d467f-293">使用任何其他方法減少 GPU 記憶體需求，除了減少目前的佇列長度 (也就是降低品質、移除效果等等) </span><span class="sxs-lookup"><span data-stu-id="d467f-293">reducing GPU memory requirements with any other means besides reducing Present Queue length (that is, decreasing quality, removing effects, and so on)</span></span>
    -   <span data-ttu-id="d467f-294">指定 [**DwmEnableMMCSS**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenablemmcss) 以防止一般 DWM 節流</span><span class="sxs-lookup"><span data-stu-id="d467f-294">specifying [**DwmEnableMMCSS**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenablemmcss) to prevent DWM throttling in general</span></span>

-   <span data-ttu-id="d467f-295">在下列案例中，確認應用程式顯示功能和框架統計資料效能：</span><span class="sxs-lookup"><span data-stu-id="d467f-295">Verify application display functionality and frame statistics performance in the following scenarios:</span></span>

    -   <span data-ttu-id="d467f-296">on 和 off 的 DWM</span><span class="sxs-lookup"><span data-stu-id="d467f-296">with DWM on and off</span></span>
    -   <span data-ttu-id="d467f-297">全螢幕專屬和視窗模式</span><span class="sxs-lookup"><span data-stu-id="d467f-297">fullscreen exclusive and windowed modes</span></span>
    -   <span data-ttu-id="d467f-298">較低的功能硬體</span><span class="sxs-lookup"><span data-stu-id="d467f-298">lower capability hardware</span></span>

-   <span data-ttu-id="d467f-299">當應用程式無法從有 D3DPRESENT FORCEIMMEDIATE 的大量 glitched 框架復原時 \_ ，可能會執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="d467f-299">When applications cannot recover from large numbers of glitched frames with D3DPRESENT\_FORCEIMMEDIATE Present, they can potentially perform the following operations:</span></span>

    -   <span data-ttu-id="d467f-300">以較少的工作負載呈現，以降低 CPU 和 GPU 使用量。</span><span class="sxs-lookup"><span data-stu-id="d467f-300">reduce CPU and GPU usage by rendering with less workload.</span></span>
    -   <span data-ttu-id="d467f-301">在影片解碼的情況下，藉由降低品質以及 CPU 和 GPU 使用量來加快解碼的速度。</span><span class="sxs-lookup"><span data-stu-id="d467f-301">in the case of video decode, decode faster by reducing quality and, therefore, CPU and GPU usage.</span></span>

## <a name="conclusion-about-direct3d-9ex-improvements"></a><span data-ttu-id="d467f-302">Direct3D 9Ex 改進的結論</span><span class="sxs-lookup"><span data-stu-id="d467f-302">Conclusion about Direct3D 9Ex Improvements</span></span>

<span data-ttu-id="d467f-303">在 Windows 7 上，在簡報期間顯示影片或量測計畫面播放速率的應用程式，可以選擇切換至 Flip 模型。</span><span class="sxs-lookup"><span data-stu-id="d467f-303">On Windows 7, applications that display video or gauge frame rate during presentation can opt into Flip Model.</span></span> <span data-ttu-id="d467f-304">與 Flip 模型 Direct3D 9Ex 相關聯的目前統計資料改善，可讓應用程式受益于每個畫面播放速率的簡報，並提供即時意見反應來偵測和修復問題。</span><span class="sxs-lookup"><span data-stu-id="d467f-304">The present statistics improvements that are associated with Flip Model Direct3D 9Ex can benefit applications that synchronize presentation per frame rate, with real time feedback for glitch detection and recovery.</span></span> <span data-ttu-id="d467f-305">採用 Direct3D 9Ex Flip 模型的開發人員應該以不同的 HWND 作為目標，將 GDI 內容和畫面播放速率同步處理的目標設為帳戶。</span><span class="sxs-lookup"><span data-stu-id="d467f-305">Developers that adopt the Direct3D 9Ex Flip Model should take targeting a separate HWND from GDI content and frame rate synchronization into account.</span></span> <span data-ttu-id="d467f-306">請參閱本主題中的詳細資料和 MSDN 檔。</span><span class="sxs-lookup"><span data-stu-id="d467f-306">Refer to details in this topic, and MSDN documentation.</span></span> <span data-ttu-id="d467f-307">如需其他檔，請參閱 [MSDN 上的 DirectX 開發人員中心](/previous-versions/windows/apps/hh452744(v=win.10))。</span><span class="sxs-lookup"><span data-stu-id="d467f-307">For additional documentation, see [DirectX Developer Center on MSDN](/previous-versions/windows/apps/hh452744(v=win.10)).</span></span>

## <a name="call-to-action"></a><span data-ttu-id="d467f-308">動作的呼叫</span><span class="sxs-lookup"><span data-stu-id="d467f-308">Call to Action</span></span>

<span data-ttu-id="d467f-309">當您建立嘗試同步處理展示畫面播放速率或從顯示問題中復原的應用程式時，建議您在 Windows 7 上使用 Direct3D 9Ex 翻轉模型及其目前的統計資料。</span><span class="sxs-lookup"><span data-stu-id="d467f-309">We encourage you to use Direct3D 9Ex Flip Model and its present statistics on Windows 7 when you create applications that attempt to synchronize presentation frame rate or recover from display glitches.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d467f-310">相關主題</span><span class="sxs-lookup"><span data-stu-id="d467f-310">Related topics</span></span>

<span data-ttu-id="d467f-311">[MSDN 上的 DirectX 開發人員中心](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="d467f-311">[DirectX Developer Center on MSDN](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
</dt> </dl>