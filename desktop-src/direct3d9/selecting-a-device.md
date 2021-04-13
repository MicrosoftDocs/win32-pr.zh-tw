---
description: 應用程式可以查詢硬體來偵測支援的 Direct3D 裝置類型。 本節包含有關列舉顯示配接器和選取 Direct3D 裝置的主要工作資訊。
ms.assetid: d140b90c-3a20-49f4-883b-662b6c05dcea
title: 選取 (Direct3D 9) 的裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdfa1faf38007f00959ac7263b4538954044688
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510352"
---
# <a name="selecting-a-device-direct3d-9"></a><span data-ttu-id="4ba22-104">選取 (Direct3D 9) 的裝置</span><span class="sxs-lookup"><span data-stu-id="4ba22-104">Selecting a Device (Direct3D 9)</span></span>

<span data-ttu-id="4ba22-105">應用程式可以查詢硬體來偵測支援的 Direct3D 裝置類型。</span><span class="sxs-lookup"><span data-stu-id="4ba22-105">Applications can query hardware to detect the supported Direct3D device types.</span></span> <span data-ttu-id="4ba22-106">本節包含有關列舉顯示配接器和選取 Direct3D 裝置的主要工作資訊。</span><span class="sxs-lookup"><span data-stu-id="4ba22-106">This section contains information about the primary tasks involved in enumerating display adapters and selecting Direct3D devices.</span></span>

<span data-ttu-id="4ba22-107">應用程式必須執行一系列的工作，才能選取適當的 Direct3D 裝置。</span><span class="sxs-lookup"><span data-stu-id="4ba22-107">An application must perform a series of tasks to select an appropriate Direct3D device.</span></span> <span data-ttu-id="4ba22-108">請注意，下列步驟適用于全螢幕應用程式，在大部分情況下，視窗型應用程式可以略過這些步驟。</span><span class="sxs-lookup"><span data-stu-id="4ba22-108">Note that the following steps are intended for a full-screen application and that, in most cases, a windowed application can skip most of these steps.</span></span>

1.  <span data-ttu-id="4ba22-109">一開始，應用程式必須列舉系統上的顯示器介面卡。</span><span class="sxs-lookup"><span data-stu-id="4ba22-109">Initially, the application must enumerate the display adapters on the system.</span></span> <span data-ttu-id="4ba22-110">介面卡是一種實體硬體。</span><span class="sxs-lookup"><span data-stu-id="4ba22-110">An adapter is a physical piece of hardware.</span></span> <span data-ttu-id="4ba22-111">請注意，圖形配接器可能包含一個以上的介面卡，如同雙指標顯示器。</span><span class="sxs-lookup"><span data-stu-id="4ba22-111">Note that the graphics card might contain more than a single adapter, as is the case with a dual-headed display.</span></span> <span data-ttu-id="4ba22-112">不在意多重監視器支援的應用程式可以忽略此步驟，並將 D3DADAPTER \_ 預設值傳遞至步驟2中的 [**IDirect3D9：： EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) 方法。</span><span class="sxs-lookup"><span data-stu-id="4ba22-112">Applications that are not concerned with multi-monitor support can disregard this step, and pass D3DADAPTER\_DEFAULT to the [**IDirect3D9::EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) method in step 2.</span></span>
2.  <span data-ttu-id="4ba22-113">針對每個介面卡，應用程式會藉由呼叫 [**IDirect3D9：： EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)來列舉支援的顯示模式。</span><span class="sxs-lookup"><span data-stu-id="4ba22-113">For each adapter, the application enumerates the supported display modes by calling [**IDirect3D9::EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span>
3.  <span data-ttu-id="4ba22-114">如有需要，應用程式會藉由呼叫 [**IDirect3D9：： CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)，在每個列舉顯示模式中檢查硬體加速是否存在，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="4ba22-114">If required, the application checks for the presence of hardware acceleration in each enumerated display mode by calling [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype), as shown in the following code example.</span></span> <span data-ttu-id="4ba22-115">請注意，這只是 **IDirect3D9：： CheckDeviceType**; 的其中一種可能用途如需詳細資訊，請參閱 [判斷 (Direct3D 9) 的硬體支援](determining-hardware-support.md)。</span><span class="sxs-lookup"><span data-stu-id="4ba22-115">Note that this is only one of the possible uses for **IDirect3D9::CheckDeviceType**; for details, see [Determining Hardware Support (Direct3D 9)](determining-hardware-support.md).</span></span>
    ```
    D3DPRESENT_PARAMETERS Params;
    // Initialize values for D3DPRESENT_PARAMETERS members. 

    Params.BackBufferFormat = D3DFMT_X1R5G5B5; 

    if(FAILED(m_pD3D->CheckDeviceType(Device.m_uAdapter, 
                      Device.m_DevType, 
                      Params.BackBufferFormat, Params.BackBufferFormat, 
                      FALSE))) 
        return E_FAIL;
    ```

    

4.  <span data-ttu-id="4ba22-116">應用程式會藉由呼叫 [**IDirect3D9：： GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) 方法，在此介面卡上檢查裝置的所需功能層級。</span><span class="sxs-lookup"><span data-stu-id="4ba22-116">The application checks for the desired level of functionality for the device on this adapter by calling the [**IDirect3D9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) method.</span></span> <span data-ttu-id="4ba22-117">透過 [**IDirect3D9：： CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)驗證，在所有顯示模式中，此方法所傳回的功能保證會是固定的裝置。</span><span class="sxs-lookup"><span data-stu-id="4ba22-117">The capability returned by this method is guaranteed to be constant for a device across all display modes, verified by [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype).</span></span>
5.  <span data-ttu-id="4ba22-118">裝置一律會轉譯成裝置所支援之列舉顯示模式的格式表面。</span><span class="sxs-lookup"><span data-stu-id="4ba22-118">Devices can always render to surfaces of the format of an enumerated display mode that is supported by the device.</span></span> <span data-ttu-id="4ba22-119">如果應用程式需要轉譯成不同格式的介面，則可以呼叫 [**IDirect3D9：： CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)。</span><span class="sxs-lookup"><span data-stu-id="4ba22-119">If the application is required to render to a surface of a different format, it can call [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span></span> <span data-ttu-id="4ba22-120">如果裝置可以轉譯成格式，則保證 [**IDirect3D9：： GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) 所傳回的所有功能都適用。</span><span class="sxs-lookup"><span data-stu-id="4ba22-120">If the device can render to the format, then it is guaranteed that all capabilities returned by [**IDirect3D9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) are applicable.</span></span>
6.  <span data-ttu-id="4ba22-121">最後，應用程式可以使用 [**IDirect3D9：： CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) 方法，判斷是否支援轉譯格式的取樣技術，例如全場景消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="4ba22-121">Lastly, the application can determine if multisampling techniques, such as full-scene antialiasing, are supported for a render format by using the [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) method.</span></span>

<span data-ttu-id="4ba22-122">完成上述步驟之後，應用程式應該會有可運作的顯示模式清單。</span><span class="sxs-lookup"><span data-stu-id="4ba22-122">After completing the preceding steps, the application should have a list of display modes in which it can operate.</span></span> <span data-ttu-id="4ba22-123">最後一個步驟是確認有足夠的可用裝置可存取記憶體，以容納所需的緩衝區和消除鋸齒數目。</span><span class="sxs-lookup"><span data-stu-id="4ba22-123">The final step is to verify that enough device-accessible memory is available to accommodate the required number of buffers and antialiasing.</span></span> <span data-ttu-id="4ba22-124">這是必要的測試，因為模式和取樣率組合的記憶體耗用量無法進行預測，而不需要進行驗證。</span><span class="sxs-lookup"><span data-stu-id="4ba22-124">This test is necessary because the memory consumption for the mode and multisample combination is impossible to predict without verifying it.</span></span> <span data-ttu-id="4ba22-125">此外，某些顯示器介面卡架構可能不會有固定數量的裝置可存取記憶體。</span><span class="sxs-lookup"><span data-stu-id="4ba22-125">Moreover, some display adapter architectures might not have a constant amount of device-accessible memory.</span></span> <span data-ttu-id="4ba22-126">這表示，應用程式應該能夠在進入全螢幕模式時，回報非影片記憶體失敗。</span><span class="sxs-lookup"><span data-stu-id="4ba22-126">This means that an application should be able to report out-of-video-memory failures when going into full-screen mode.</span></span> <span data-ttu-id="4ba22-127">一般而言，應用程式應該從它提供給使用者的模式清單中移除全螢幕模式，或者應該藉由減少背景緩衝區的數目或使用較不復雜的多層式技術來嘗試消耗較少的記憶體。</span><span class="sxs-lookup"><span data-stu-id="4ba22-127">Typically, an application should remove full-screen mode from the list of modes that it offers to a user, or it should attempt to consume less memory by reducing the number of back buffers or by using a less complex multisampling technique.</span></span>

<span data-ttu-id="4ba22-128">視窗型應用程式會執行一組類似的工作。</span><span class="sxs-lookup"><span data-stu-id="4ba22-128">A windowed application performs a similar set of tasks.</span></span>

1.  <span data-ttu-id="4ba22-129">它會決定視窗的工作區所涵蓋的桌面矩形。</span><span class="sxs-lookup"><span data-stu-id="4ba22-129">It determines the desktop rectangle covered by the client area of the window.</span></span>
2.  <span data-ttu-id="4ba22-130">它會列舉介面卡，並尋找其監視器涵蓋用戶端區域的介面卡。</span><span class="sxs-lookup"><span data-stu-id="4ba22-130">It enumerates adapters, looking for the adapter whose monitor covers the client area.</span></span> <span data-ttu-id="4ba22-131">如果用戶端區域是由一個以上的介面卡所擁有，則應用程式可以選擇獨立驅動每個介面卡，或驅動單一介面卡，並讓 Direct3D 在簡報時將圖元從一個裝置傳輸到另一個裝置。</span><span class="sxs-lookup"><span data-stu-id="4ba22-131">If the client area is owned by more than one adapter, then the application can choose to drive each adapter independently, or to drive a single adapter and have Direct3D transfer pixels from one device to another at presentation.</span></span> <span data-ttu-id="4ba22-132">應用程式也可以略過兩個先前的步驟，並使用 D3DADAPTER \_ 預設介面卡。</span><span class="sxs-lookup"><span data-stu-id="4ba22-132">The application can also disregard two preceding steps and use the D3DADAPTER\_DEFAULT adapter.</span></span> <span data-ttu-id="4ba22-133">請注意，當視窗放置於次要監視器時，這可能會導致較慢的作業。</span><span class="sxs-lookup"><span data-stu-id="4ba22-133">Note that this might result in slower operation when the window is placed on a secondary monitor.</span></span>
3.  <span data-ttu-id="4ba22-134">應用程式應該呼叫 [**IDirect3D9：： CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype) ，以判斷裝置是否可以在桌面圖案中支援轉譯為指定格式的背景緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4ba22-134">The application should call [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype) to determine if the device can support rendering to a back buffer of the specified format while in desktop mode.</span></span> <span data-ttu-id="4ba22-135">您可以使用 [**IDirect3D9：： GetAdapterDisplayMode**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode)來判斷桌面顯示格式，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="4ba22-135">[**IDirect3D9::GetAdapterDisplayMode**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode) can be used to determine the desktop display format, as shown in the following code example.</span></span>
    ```
    D3DPRESENT_PARAMETERS Params;
    // Initialize values for D3DPRESENT_PARAMETERS members. 

    // Use the current display mode.
    D3DDISPLAYMODE mode;

    if(FAILED(m_pD3D->GetAdapterDisplayMode(Device.m_uAdapter , &mode)))
        return E_FAIL;

    Params.BackBufferFormat = mode.Format;

    if(FAILED(m_pD3D->CheckDeviceType(Device.m_uAdapter, Device.m_DevType, 
    Params.BackBufferFormat, Params.BackBufferFormat, FALSE)))
        return E_FAIL;
    ```

    

## <a name="related-topics"></a><span data-ttu-id="4ba22-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="4ba22-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ba22-137">Direct3D 裝置</span><span class="sxs-lookup"><span data-stu-id="4ba22-137">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
