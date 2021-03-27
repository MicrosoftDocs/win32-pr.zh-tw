---
title: 軟體層
description: Direct3D 11 執行時間是使用圖層來建立，從核心的基本功能開始，並在外部層建立選擇性和開發人員協助工具。 本節說明每個圖層的功能。
ms.assetid: c545983c-5351-42a9-82e5-deea73aa035f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb05658860e678e8020392cb046a634e3b03c7c2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104507927"
---
# <a name="software-layers"></a><span data-ttu-id="8b72b-104">軟體層</span><span class="sxs-lookup"><span data-stu-id="8b72b-104">Software Layers</span></span>

<span data-ttu-id="8b72b-105">Direct3D 11 執行時間是使用圖層來建立，從核心的基本功能開始，並在外部層建立選擇性和開發人員協助工具。</span><span class="sxs-lookup"><span data-stu-id="8b72b-105">The Direct3D 11 runtime is constructed with layers, starting with the basic functionality at the core and building optional and developer-assist functionality in outer layers.</span></span> <span data-ttu-id="8b72b-106">本節說明每個圖層的功能。</span><span class="sxs-lookup"><span data-stu-id="8b72b-106">This section describes the functionality of each layer.</span></span>

<span data-ttu-id="8b72b-107">一般來說，圖層會加入功能，但不會修改現有的行為。</span><span class="sxs-lookup"><span data-stu-id="8b72b-107">As a general rule, layers add functionality, but do not modify existing behavior.</span></span> <span data-ttu-id="8b72b-108">例如，除了要具現化的調試層之外，核心函式的傳回值也會與所具現化的調試層有相同的傳回值。</span><span class="sxs-lookup"><span data-stu-id="8b72b-108">For example, core functions will have the same return values independent of the debug layer being instantiated, although additional debug output may be provided if the debug layer is instantiated.</span></span>

<span data-ttu-id="8b72b-109">若要在建立裝置時建立圖層，請呼叫 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) 或 [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) ，並提供一或多個 [**D3D11 \_ 建立 \_ 裝置 \_ 旗**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) 標值。</span><span class="sxs-lookup"><span data-stu-id="8b72b-109">To create layers when a device is created, call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) and supply one or more [**D3D11\_CREATE\_DEVICE\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) values.</span></span>

<span data-ttu-id="8b72b-110">Direct3D 11 提供下列執行時間層級：</span><span class="sxs-lookup"><span data-stu-id="8b72b-110">Direct3D 11 provides the following runtime layers:</span></span>

-   [<span data-ttu-id="8b72b-111">核心層</span><span class="sxs-lookup"><span data-stu-id="8b72b-111">Core Layer</span></span>](#core-layer)
-   [<span data-ttu-id="8b72b-112">Debug 圖層</span><span class="sxs-lookup"><span data-stu-id="8b72b-112">Debug Layer</span></span>](#debug-layer)
-   [<span data-ttu-id="8b72b-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="8b72b-113">Related topics</span></span>](#related-topics)

## <a name="core-layer"></a><span data-ttu-id="8b72b-114">核心層</span><span class="sxs-lookup"><span data-stu-id="8b72b-114">Core Layer</span></span>

<span data-ttu-id="8b72b-115">核心層預設為存在;在 API 和設備磁碟機之間提供非常精簡的對應，將高頻率呼叫的額外負荷降至最低。</span><span class="sxs-lookup"><span data-stu-id="8b72b-115">The core layer exists by default; providing a very thin mapping between the API and the device driver, minimizing overhead for high-frequency calls.</span></span> <span data-ttu-id="8b72b-116">因為核心層是效能不可或缺的，所以它只會執行重大驗證。</span><span class="sxs-lookup"><span data-stu-id="8b72b-116">As the core layer is essential for performance, it only performs critical validation.</span></span> <span data-ttu-id="8b72b-117">其餘層是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="8b72b-117">The remaining layers are optional.</span></span>

## <a name="debug-layer"></a><span data-ttu-id="8b72b-118">Debug 圖層</span><span class="sxs-lookup"><span data-stu-id="8b72b-118">Debug Layer</span></span>

<span data-ttu-id="8b72b-119">Debug 層提供大量的額外參數和一致性驗證 (例如驗證著色器連結和資源系結、驗證參數一致性，以及報告錯誤描述) 。</span><span class="sxs-lookup"><span data-stu-id="8b72b-119">The debug layer provides extensive additional parameter and consistency validation (such as validating shader linkage and resource binding, validating parameter consistency, and reporting error descriptions).</span></span>

<span data-ttu-id="8b72b-120">若要建立支援 debug 層的裝置，您必須安裝 (的 DirectX SDK，才能取得 D3D11SDKLayers.dll) ，然後在呼叫 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice)函式或 [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)函式時，指定 **D3D11 \_ 建立 \_ 裝置的 \_ 調試** 程式旗標。</span><span class="sxs-lookup"><span data-stu-id="8b72b-120">To create a device that supports the debug layer, you must install the DirectX SDK (to get D3D11SDKLayers.dll), and then specify the **D3D11\_CREATE\_DEVICE\_DEBUG** flag when calling the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function or the [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) function.</span></span> <span data-ttu-id="8b72b-121">如果您在啟用調試層的情況下執行應用程式，應用程式將會大幅降低。</span><span class="sxs-lookup"><span data-stu-id="8b72b-121">If you run your application with the debug layer enabled, the application will be substantially slower.</span></span> <span data-ttu-id="8b72b-122">但是，為了確保您的應用程式在出貨之前已清除錯誤和警告，請使用 debug 層。</span><span class="sxs-lookup"><span data-stu-id="8b72b-122">But, to ensure that your application is clean of errors and warnings before you ship it, use the debug layer.</span></span> <span data-ttu-id="8b72b-123">如需詳細資訊，請參閱 [使用 debug layer 來偵測應用程式](using-the-debug-layer-to-test-apps.md)。</span><span class="sxs-lookup"><span data-stu-id="8b72b-123">For more info, see [Using the debug layer to debug apps](using-the-debug-layer-to-test-apps.md).</span></span>


> [!Note]  
> <span data-ttu-id="8b72b-124">若為 windows 7 （具有 Windows 7 的平臺更新 (KB2670838) 或 Windows 8 x）若要建立支援 debug 層的裝置，請安裝 (的 Windows 軟體開發套件) SDK Windows 8 以取得 D3D11 \_1SDKLayers.dll。</span><span class="sxs-lookup"><span data-stu-id="8b72b-124">For Windows 7 with Platform Update for Windows 7 (KB2670838) or Windows 8.x, to create a device that supports the debug layer, install the Windows Software Development Kit (SDK) for Windows 8.x to get D3D11\_1SDKLayers.dll.</span></span>


> [!Note]  
> <span data-ttu-id="8b72b-125">針對 Windows 10，若要建立支援 debug 層的裝置，請啟用 [圖形工具] 選用功能。</span><span class="sxs-lookup"><span data-stu-id="8b72b-125">For Windows 10, to create a device that supports the debug layer, enable the "Graphics Tools" optional feature.</span></span> <span data-ttu-id="8b72b-126">移至 [設定] 面板中的 [系統、應用程式 & 功能]、[管理選擇性功能]、[新增功能]，然後尋找 [圖形工具]。</span><span class="sxs-lookup"><span data-stu-id="8b72b-126">Go to the Settings panel, under System, Apps & features, Manage optional Features, Add a feature, and then look for "Graphics Tools".</span></span>


> [!Note]  
> <span data-ttu-id="8b72b-127">如需有關如何從遠端偵測 DirectX 應用程式的詳細資訊，請參閱 [從遠端偵錯 directx 應用程式](/windows/desktop/direct3dtools/debugging-directx-apps-remotely)。</span><span class="sxs-lookup"><span data-stu-id="8b72b-127">For info about how to debug DirectX apps remotely, see [Debugging DirectX apps remotely](/windows/desktop/direct3dtools/debugging-directx-apps-remotely).</span></span>

 

<span data-ttu-id="8b72b-128">或者，您也可以使用 directx SDK 隨附的 [directx 主控台](/previous-versions//bb219725(v=vs.85)) 來啟用/停用偵錯工具旗標。</span><span class="sxs-lookup"><span data-stu-id="8b72b-128">Alternately, you can enable/disable the debug flag using the [DirectX Control Panel](/previous-versions//bb219725(v=vs.85)) included as part of the DirectX SDK.</span></span>

<span data-ttu-id="8b72b-129">當 debug 圖層列出記憶體流失時，它會輸出物件介面指標清單及其易記名稱。</span><span class="sxs-lookup"><span data-stu-id="8b72b-129">When the debug layer lists memory leaks, it outputs a list of object interface pointers along with their friendly names.</span></span> <span data-ttu-id="8b72b-130">預設的易記名稱是「 &lt; 未命名」 &gt; 。</span><span class="sxs-lookup"><span data-stu-id="8b72b-130">The default friendly name is "&lt;unnamed&gt;".</span></span> <span data-ttu-id="8b72b-131">您可以使用 [**ID3D11DeviceChild：： SetPrivateData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicechild-setprivatedata) 方法以及 D3Dcommon 中的 **WKPDID \_ D3DDebugObjectName** GUID 來設定易記名稱。</span><span class="sxs-lookup"><span data-stu-id="8b72b-131">You can set the friendly name by using the [**ID3D11DeviceChild::SetPrivateData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicechild-setprivatedata) method and the **WKPDID\_D3DDebugObjectName** GUID that is in D3Dcommon.h.</span></span> <span data-ttu-id="8b72b-132">例如，若要以 SDKLayer 名稱 mytexture.jpg 命名 pTexture，請使用下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="8b72b-132">For example, to name pTexture with a SDKLayer name of mytexture.jpg, use the following code:</span></span>


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



<span data-ttu-id="8b72b-133">一般而言，您應該從生產版本編譯這些呼叫。</span><span class="sxs-lookup"><span data-stu-id="8b72b-133">Typically, you should compile these calls out of your production version.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b72b-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="8b72b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b72b-135">裝置</span><span class="sxs-lookup"><span data-stu-id="8b72b-135">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 