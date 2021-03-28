---
title: 如何建立變形裝置
description: 本主題說明如何建立可執行高速度軟體轉譯器的變形裝置。
ms.assetid: 6daf661e-bc24-4b90-83a7-031acb57cf87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deda409971d22f46132a1cb9b008d3dd1eb7c407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990966"
---
# <a name="how-to-create-a-warp-device"></a><span data-ttu-id="3c82e-103">如何：建立變形裝置</span><span class="sxs-lookup"><span data-stu-id="3c82e-103">How To: Create a WARP Device</span></span>

<span data-ttu-id="3c82e-104">本主題說明如何建立可執行高速度軟體轉譯器的變形裝置。</span><span class="sxs-lookup"><span data-stu-id="3c82e-104">This topic shows how to create a WARP device that implements a high speed software rasterizer.</span></span> <span data-ttu-id="3c82e-105">若要建立變形裝置，只要指定您要建立的裝置將使用變形驅動程式。</span><span class="sxs-lookup"><span data-stu-id="3c82e-105">To create a WARP device, simply specify that the device you are creating will use a WARP driver.</span></span> <span data-ttu-id="3c82e-106">此範例會同時建立裝置和交換鏈。</span><span class="sxs-lookup"><span data-stu-id="3c82e-106">This example creates a device and a swap chain at the same time.</span></span>

<span data-ttu-id="3c82e-107">**建立變形裝置**</span><span class="sxs-lookup"><span data-stu-id="3c82e-107">**To create a WARP device**</span></span>

1.  <span data-ttu-id="3c82e-108">定義交換鏈的初始參數。</span><span class="sxs-lookup"><span data-stu-id="3c82e-108">Define initial parameters for a swap chain.</span></span>
    ```
        DXGI_SWAP_CHAIN_DESC sd;
        ZeroMemory( &sd, sizeof( sd ) );
        sd.BufferCount = 1;
        sd.BufferDesc.Width = 640;
        sd.BufferDesc.Height = 480;
        sd.BufferDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
        sd.BufferDesc.RefreshRate.Numerator = 60;
        sd.BufferDesc.RefreshRate.Denominator = 1;
        sd.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        sd.OutputWindow = g_hWnd;
        sd.SampleDesc.Count = 1;
        sd.SampleDesc.Quality = 0;
        sd.Windowed = TRUE;
    ```

    

2.  <span data-ttu-id="3c82e-109">要求可執行應用程式所需功能的功能層級。</span><span class="sxs-lookup"><span data-stu-id="3c82e-109">Request a feature level that implements the features your application will need.</span></span> <span data-ttu-id="3c82e-110">您可以成功地為功能層級 **d3d 功能層 \_ 級 \_ \_ \_ 2 1** 到 **D3D \_ 功能 \_ 層級 \_ 10 \_ 1** 建立變形裝置，並從所有功能等級的 Windows 8 開始。</span><span class="sxs-lookup"><span data-stu-id="3c82e-110">A WARP device can be successfully created for feature levels **D3D\_FEATURE\_LEVEL\_9\_1** through **D3D\_FEATURE\_LEVEL\_10\_1** and starting with Windows 8 for all feature levels.</span></span>

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_10_1;
    ```

    

    <span data-ttu-id="3c82e-111">請參閱 [**D3D \_ 功能 \_ 層級**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) 列舉中的功能層級詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="3c82e-111">See more about feature levels in the [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumeration.</span></span>

3.  <span data-ttu-id="3c82e-112">藉由呼叫 [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)來建立裝置。</span><span class="sxs-lookup"><span data-stu-id="3c82e-112">Create the device by calling [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>


```
    HRESULT hr = S_OK;
    if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                    D3D_DRIVER_TYPE_WARP,
                    NULL, 
                    0,
                    &FeatureLevels, 
                    1, 
                    D3D11_SDK_VERSION, 
                    &sd, 
                    &g_pSwapChain, 
                    &g_pd3dDevice, 
                    &FeatureLevel,
                    &g_pImmediateContext )))
    {
        return hr;
    }
```



<span data-ttu-id="3c82e-113">您將需要使用來自 [**D3D \_ 驅動程式 \_ 類型**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) 列舉的變形驅動程式類型來提供 API 呼叫。</span><span class="sxs-lookup"><span data-stu-id="3c82e-113">You will need to supply the API call with the WARP driver type from the [**D3D\_DRIVER\_TYPE**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) enumeration.</span></span> <span data-ttu-id="3c82e-114">方法成功之後，它會傳回交換連結口、裝置介面、驅動程式所授與的功能等級指標，以及立即內容介面。</span><span class="sxs-lookup"><span data-stu-id="3c82e-114">After the method succeeds, it will return a swap chain interface, a device interface, a pointer to the feature level that was granted by the driver, and an immediate context interface.</span></span>

<span data-ttu-id="3c82e-115">如需有關在特定功能層級上建立變形裝置之限制的詳細資訊，請參閱 [建立變形和參照裝置的限制](overviews-direct3d-11-devices-limitations.md)。</span><span class="sxs-lookup"><span data-stu-id="3c82e-115">For information about limitations creating a WARP device on certain feature levels, see [Limitations Creating WARP and Reference Devices](overviews-direct3d-11-devices-limitations.md).</span></span>

## <a name="new-for-windows-8"></a><span data-ttu-id="3c82e-116">Windows 8 的新</span><span class="sxs-lookup"><span data-stu-id="3c82e-116">New for Windows 8</span></span>

<span data-ttu-id="3c82e-117">當電腦的主要顯示器介面卡是「Microsoft 基本顯示器介面卡」 (變形介面卡) 時，該電腦也會有第二張介面卡。</span><span class="sxs-lookup"><span data-stu-id="3c82e-117">When a computer's primary display adapter is the "Microsoft Basic Display Adapter" (WARP adapter), that computer also has a second adapter.</span></span> <span data-ttu-id="3c82e-118">第二張介面卡是僅限轉譯的裝置，沒有顯示輸出。</span><span class="sxs-lookup"><span data-stu-id="3c82e-118">This second adapter is the render-only device that has no display outputs.</span></span> <span data-ttu-id="3c82e-119">如需僅限轉譯裝置的詳細資訊，請參閱 [關於列舉介面卡的 Windows 8 中的新資訊](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi)。</span><span class="sxs-lookup"><span data-stu-id="3c82e-119">For more info about the render-only device, see [new info in Windows 8 about enumerating adapters](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c82e-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="3c82e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c82e-121">裝置</span><span class="sxs-lookup"><span data-stu-id="3c82e-121">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="3c82e-122">如何使用 Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="3c82e-122">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 