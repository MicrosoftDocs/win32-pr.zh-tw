---
title: 使用 debug 層來對應用程式進行偵錯工具
description: 在此，我們將討論如何啟用 debug 層，以及您可以使用 debug 圖層防止的一些問題。
ms.assetid: 3C2B0A12-FB57-4400-BE39-05ED23F552C7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa3f4748da6893470e3bb6631c4228ec1ae3d48
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671651"
---
# <a name="using-the-debug-layer-to-debug-apps"></a><span data-ttu-id="05eed-103">使用 debug 層來對應用程式進行偵錯工具</span><span class="sxs-lookup"><span data-stu-id="05eed-103">Using the debug layer to debug apps</span></span>

<span data-ttu-id="05eed-104">建議您使用 [debug 層](overviews-direct3d-11-devices-layers.md) 來將您的應用程式進行偵錯工具，以確保這些應用程式的錯誤和警告都已清除。</span><span class="sxs-lookup"><span data-stu-id="05eed-104">We recommend that you use the [debug layer](overviews-direct3d-11-devices-layers.md) to debug your apps to ensure that they are clean of errors and warnings.</span></span> <span data-ttu-id="05eed-105">Debug 層可協助您撰寫 Direct3D 程式碼。</span><span class="sxs-lookup"><span data-stu-id="05eed-105">The debug layer helps you write Direct3D code.</span></span> <span data-ttu-id="05eed-106">此外，當您使用 debug 圖層時，您的產能會增加，因為您可以立即查看其來源的隱匿轉譯錯誤或甚至是黑色畫面的原因。</span><span class="sxs-lookup"><span data-stu-id="05eed-106">In addition, your productivity can increase when you use the debug layer because you can immediately see the causes of obscure rendering errors or even black screens at their source.</span></span> <span data-ttu-id="05eed-107">Debug 層提供許多問題的警告。</span><span class="sxs-lookup"><span data-stu-id="05eed-107">The debug layer provides warnings for many issues.</span></span> <span data-ttu-id="05eed-108">例如，debug 層會針對這些問題提供警告：</span><span class="sxs-lookup"><span data-stu-id="05eed-108">For example, the debug layer provides warnings for these issues:</span></span>

-   <span data-ttu-id="05eed-109">忘記設定材質，但在您的圖元著色器中讀取紋理</span><span class="sxs-lookup"><span data-stu-id="05eed-109">Forgot to set a texture but read from it in your pixel shader</span></span>
-   <span data-ttu-id="05eed-110">輸出深度，但沒有系結的深度樣板狀態</span><span class="sxs-lookup"><span data-stu-id="05eed-110">Output depth but have no depth-stencil state bound</span></span>
-   <span data-ttu-id="05eed-111">材質建立失敗，INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="05eed-111">Texture creation failed with INVALIDARG</span></span>

<span data-ttu-id="05eed-112">在此，我們將討論如何啟用 [debug 層](overviews-direct3d-11-devices-layers.md) ，以及您可以使用 debug 圖層防止的一些問題。</span><span class="sxs-lookup"><span data-stu-id="05eed-112">Here we talk about how to enable the [debug layer](overviews-direct3d-11-devices-layers.md) and some of the issues that you can prevent by using the debug layer.</span></span>

-   [<span data-ttu-id="05eed-113">啟用 debug 圖層</span><span class="sxs-lookup"><span data-stu-id="05eed-113">Enabling the debug layer</span></span>](#enabling-the-debug-layer)
-   [<span data-ttu-id="05eed-114">使用 debug 層防止應用程式發生錯誤</span><span class="sxs-lookup"><span data-stu-id="05eed-114">Preventing errors in your app with the debug layer</span></span>](#preventing-errors-in-your-app-with-the-debug-layer)
    -   [<span data-ttu-id="05eed-115">不要將 Null 指標傳遞給 Map</span><span class="sxs-lookup"><span data-stu-id="05eed-115">Don't pass NULL pointers to Map</span></span>](#dont-pass-null-pointers-to-map)
    -   [<span data-ttu-id="05eed-116">來源和目的地資源內的限制來源方塊</span><span class="sxs-lookup"><span data-stu-id="05eed-116">Confine source box within source and destination resources</span></span>](#confine-source-box-within-source-and-destination-resources)
    -   [<span data-ttu-id="05eed-117">請勿捨棄 DiscardResource 或 DiscardView</span><span class="sxs-lookup"><span data-stu-id="05eed-117">Don't drop DiscardResource or DiscardView</span></span>](#dont-drop-discardresource-or-discardview)
-   [<span data-ttu-id="05eed-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="05eed-118">Related topics</span></span>](#related-topics)

## <a name="enabling-the-debug-layer"></a><span data-ttu-id="05eed-119">啟用 debug 圖層</span><span class="sxs-lookup"><span data-stu-id="05eed-119">Enabling the debug layer</span></span>

<span data-ttu-id="05eed-120">若要啟用 [debug 圖層](overviews-direct3d-11-devices-layers.md)，請在呼叫 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice)函式來建立轉譯裝置時，于 Flags 參數中指定 [**D3D11 \_ 建立 \_ 裝置 \_ 調試**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag)旗 *標*。</span><span class="sxs-lookup"><span data-stu-id="05eed-120">To enable the [debug layer](overviews-direct3d-11-devices-layers.md), specify the [**D3D11\_CREATE\_DEVICE\_DEBUG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) flag in the *Flags* parameter when you call the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function to create the rendering device.</span></span> <span data-ttu-id="05eed-121">此範例程式碼示範如何在您的 Microsoft Visual Studio 專案位於 debug 組建中時啟用 debug 層：</span><span class="sxs-lookup"><span data-stu-id="05eed-121">This example code shows how to enable the debug layer when your Microsoft Visual Studio project is in a debug build:</span></span>


```C++
        UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
#if defined(_DEBUG)
        // If the project is in a debug build, enable the debug layer.
        creationFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif
        // Define the ordering of feature levels that Direct3D attempts to create.
        D3D_FEATURE_LEVEL featureLevels[] =
        {
            D3D_FEATURE_LEVEL_11_1,
            D3D_FEATURE_LEVEL_11_0,
            D3D_FEATURE_LEVEL_10_1,
            D3D_FEATURE_LEVEL_10_0,
            D3D_FEATURE_LEVEL_9_3,
            D3D_FEATURE_LEVEL_9_1
        };

        ComPtr<ID3D11Device> d3dDevice;
        ComPtr<ID3D11DeviceContext> d3dDeviceContext;
        DX::ThrowIfFailed(
            D3D11CreateDevice(
                nullptr,                    // specify nullptr to use the default adapter
                D3D_DRIVER_TYPE_HARDWARE,
                nullptr,                    // specify nullptr because D3D_DRIVER_TYPE_HARDWARE 
                                            // indicates that this function uses hardware
                creationFlags,              // optionally set debug and Direct2D compatibility flags
                featureLevels,
                ARRAYSIZE(featureLevels),
                D3D11_SDK_VERSION,          // always set this to D3D11_SDK_VERSION
                &d3dDevice,
                nullptr,
                &d3dDeviceContext
                )
            );
```



## <a name="preventing-errors-in-your-app-with-the-debug-layer"></a><span data-ttu-id="05eed-122">使用 debug 層防止應用程式發生錯誤</span><span class="sxs-lookup"><span data-stu-id="05eed-122">Preventing errors in your app with the debug layer</span></span>

<span data-ttu-id="05eed-123">如果您誤用 Direct3D 11 API 或傳遞不正確的參數， [debug 層](overviews-direct3d-11-devices-layers.md) 的偵錯工具輸出會報告錯誤或警告。</span><span class="sxs-lookup"><span data-stu-id="05eed-123">If you misuse the Direct3D 11 API or pass bad parameters, the debug output of the [debug layer](overviews-direct3d-11-devices-layers.md) reports an error or a warning.</span></span> <span data-ttu-id="05eed-124">然後您就可以更正錯誤。</span><span class="sxs-lookup"><span data-stu-id="05eed-124">You can then correct your mistake.</span></span> <span data-ttu-id="05eed-125">接下來，我們會探討一些可能導致未定義的行為，或甚至作業系統損毀的程式碼撰寫問題。</span><span class="sxs-lookup"><span data-stu-id="05eed-125">Next, we look at some coding issues that can cause undefined behavior or even the operating system to crash.</span></span> <span data-ttu-id="05eed-126">您可以使用 debug 層來攔截及防止這些問題。</span><span class="sxs-lookup"><span data-stu-id="05eed-126">You can catch and prevent these issues by using the debug layer.</span></span>

### <a name="dont-pass-null-pointers-to-map"></a><span data-ttu-id="05eed-127">不要將 Null 指標傳遞給 Map</span><span class="sxs-lookup"><span data-stu-id="05eed-127">Don't pass NULL pointers to Map</span></span>

<span data-ttu-id="05eed-128">如果您將 **Null** 傳遞給 [**>id3d11devicecoNtext：： Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)方法的 *pResource* 或 *pMappedResource* 參數，則 **對應** 的行為未定義。</span><span class="sxs-lookup"><span data-stu-id="05eed-128">If you pass **NULL** to the *pResource* or *pMappedResource* parameter of the [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) method, the behavior of **Map** is undefined.</span></span> <span data-ttu-id="05eed-129">如果您建立只支援 [核心層](overviews-direct3d-11-devices-layers.md)的裝置，則 **對應** 的無效參數可能會損毀作業系統。</span><span class="sxs-lookup"><span data-stu-id="05eed-129">If you created a device that just supports the [core layer](overviews-direct3d-11-devices-layers.md), invalid parameters to **Map** can crash the operating system.</span></span> <span data-ttu-id="05eed-130">如果您建立了支援 [debug 層](overviews-direct3d-11-devices-layers.md)的裝置，則偵錯工具輸出會在此不正確 **對應** 呼叫上報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="05eed-130">If you created a device that supports the [debug layer](overviews-direct3d-11-devices-layers.md), the debug output reports an error on this invalid **Map** call.</span></span>

### <a name="confine-source-box-within-source-and-destination-resources"></a><span data-ttu-id="05eed-131">來源和目的地資源內的限制來源方塊</span><span class="sxs-lookup"><span data-stu-id="05eed-131">Confine source box within source and destination resources</span></span>

<span data-ttu-id="05eed-132">在 [**>id3d11devicecoNtext：： CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) 方法的呼叫中，來源方塊必須在來源資源內。</span><span class="sxs-lookup"><span data-stu-id="05eed-132">In a call to the [**ID3D11DeviceContext::CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) method, the source box must be within the source resource.</span></span> <span data-ttu-id="05eed-133">目的地位移、 (x、y 和 z) 可讓來源方塊在寫入目的地資源時成為位移，但是來源方塊的維度和位移必須在資源的大小內。</span><span class="sxs-lookup"><span data-stu-id="05eed-133">The destination offsets, (x, y, and z) allow the source box to be offset when writing into the destination resource, but the dimensions of the source box and the offsets must be within the size of the resource.</span></span> <span data-ttu-id="05eed-134">如果您嘗試在目的地資源外部進行複製，或指定的來源方塊大於來源資源，則 **CopySubresourceRegion** 的行為未定義。</span><span class="sxs-lookup"><span data-stu-id="05eed-134">If you try to copy outside the destination resource or specify a source box that is larger than the source resource, the behavior of **CopySubresourceRegion** is undefined.</span></span> <span data-ttu-id="05eed-135">如果您建立了支援 [debug 層](overviews-direct3d-11-devices-layers.md)的裝置，則偵錯工具輸出會在此不正確 **CopySubresourceRegion** 呼叫上報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="05eed-135">If you created a device that supports the [debug layer](overviews-direct3d-11-devices-layers.md), the debug output reports an error on this invalid **CopySubresourceRegion** call.</span></span> <span data-ttu-id="05eed-136">不正確 **CopySubresourceRegion** 參數會造成未定義的行為，而且可能會導致不正確的轉譯、裁剪、不復制或甚至是移除轉譯裝置。</span><span class="sxs-lookup"><span data-stu-id="05eed-136">Invalid parameters to **CopySubresourceRegion** cause undefined behavior and might result in incorrect rendering, clipping, no copy, or even the removal of the rendering device.</span></span>

### <a name="dont-drop-discardresource-or-discardview"></a><span data-ttu-id="05eed-137">請勿捨棄 DiscardResource 或 DiscardView</span><span class="sxs-lookup"><span data-stu-id="05eed-137">Don't drop DiscardResource or DiscardView</span></span>

<span data-ttu-id="05eed-138">除非您正確建立資源，否則執行時間會卸載對 [**ID3D11DeviceCoNtext1：:D iscardresource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) 或 [**ID3D11DeviceCoNtext1：:D iscardview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="05eed-138">The runtime drops a call to [**ID3D11DeviceContext1::DiscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) or [**ID3D11DeviceContext1::DiscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) unless you correctly create the resource.</span></span>

<span data-ttu-id="05eed-139">您傳遞給 [**ID3D11DeviceCoNtext1：:D iscardresource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) 的資源，必須使用 [**D3D11 \_ 使用方式 \_ 預設值**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) 或 [**D3D11 使用方式 \_ \_ 動態**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)建立，否則執行時間會卸載對 **DiscardResource** 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="05eed-139">The resource that you pass to [**ID3D11DeviceContext1::DiscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) must have been created by using [**D3D11\_USAGE\_DEFAULT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) or [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), otherwise the runtime drops the call to **DiscardResource**.</span></span>

<span data-ttu-id="05eed-140">您傳遞給 [**:D ID3D11DeviceCoNtext1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) 的視圖基礎的資源必須使用 [**D3D11 \_ 使用方式 \_ 預設值**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) 或 [**D3D11 \_ 使用方式 \_ 動態**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)建立，否則執行時間會卸載對 **DiscardView** 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="05eed-140">The resource that underlies the view that you pass to [**ID3D11DeviceContext1::DiscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) must have been created using [**D3D11\_USAGE\_DEFAULT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) or [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), otherwise the runtime drops the call to **DiscardView**.</span></span>

<span data-ttu-id="05eed-141">如果您建立了支援 [debug 層](overviews-direct3d-11-devices-layers.md)的裝置，則偵錯工具輸出會報告有關已卸載呼叫的錯誤。</span><span class="sxs-lookup"><span data-stu-id="05eed-141">If you created a device that supports the [debug layer](overviews-direct3d-11-devices-layers.md), the debug output reports an error regarding the dropped call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05eed-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="05eed-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05eed-143">軟體層</span><span class="sxs-lookup"><span data-stu-id="05eed-143">Software Layers</span></span>](overviews-direct3d-11-devices-layers.md)
</dt> </dl>

 

 




