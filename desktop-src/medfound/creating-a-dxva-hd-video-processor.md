---
description: 建立 DXVA-HD 視頻處理器
ms.assetid: 43a97dc8-19b3-412c-a015-339099bf4f6c
title: 建立 DXVA-HD 視頻處理器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e89c5a361335f83296eec538a5a6a710b9e19604
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102596"
---
# <a name="creating-a-dxva-hd-video-processor"></a><span data-ttu-id="8d76e-103">建立 DXVA-HD 視頻處理器</span><span class="sxs-lookup"><span data-stu-id="8d76e-103">Creating a DXVA-HD Video Processor</span></span>

<span data-ttu-id="8d76e-104">Microsoft DirectX Video 加速 High Definition (DXVA-HD) 使用兩個主要介面：</span><span class="sxs-lookup"><span data-stu-id="8d76e-104">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) uses two primary interfaces:</span></span>

-   <span data-ttu-id="8d76e-105">[**IDXVAHD \_裝置**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device)。</span><span class="sxs-lookup"><span data-stu-id="8d76e-105">[**IDXVAHD\_Device**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device).</span></span> <span data-ttu-id="8d76e-106">代表 DXVA-HD 裝置。</span><span class="sxs-lookup"><span data-stu-id="8d76e-106">Represents the DXVA-HD device.</span></span> <span data-ttu-id="8d76e-107">使用此介面來查詢裝置功能，並建立視頻處理器。</span><span class="sxs-lookup"><span data-stu-id="8d76e-107">Use this interface to query the device capabilities and create the video processor.</span></span>
-   <span data-ttu-id="8d76e-108">[**IDXVAHD \_VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor)。</span><span class="sxs-lookup"><span data-stu-id="8d76e-108">[**IDXVAHD\_VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor).</span></span> <span data-ttu-id="8d76e-109">代表一組影片處理功能。</span><span class="sxs-lookup"><span data-stu-id="8d76e-109">Represents a set of video processing capabilities.</span></span> <span data-ttu-id="8d76e-110">使用此介面來執行影片處理 array.blit。</span><span class="sxs-lookup"><span data-stu-id="8d76e-110">Use this interface to perform the video processing blit.</span></span>

<span data-ttu-id="8d76e-111">在接下來的程式碼中，假設下列全域變數：</span><span class="sxs-lookup"><span data-stu-id="8d76e-111">In the code that follows, the following global variables are assumed:</span></span>


```C++
IDirect3D9Ex            *g_pD3D = NULL;     
IDirect3DDevice9Ex      *g_pD3DDevice = NULL;   // Direct3D device.
IDXVAHD_Device          *g_pDXVAHD = NULL;      // DXVA-HD device.
IDXVAHD_VideoProcessor  *g_pDXVAVP = NULL;      // DXVA-HD video processor.
IDirect3DSurface9       *g_pSurface = NULL;     // Video surface.
        
const D3DFORMAT     RENDER_TARGET_FORMAT = D3DFMT_X8R8G8B8;
const D3DFORMAT     VIDEO_FORMAT         = D3DFMT_X8R8G8B8; 
const UINT          VIDEO_FPS            = 60;
const UINT          VIDEO_WIDTH          = 640;
const UINT          VIDEO_HEIGHT         = 480;
```



<span data-ttu-id="8d76e-112">若要建立 DXVA-HD 視頻處理器：</span><span class="sxs-lookup"><span data-stu-id="8d76e-112">To create a DXVA-HD video processor:</span></span>

1.  <span data-ttu-id="8d76e-113">以影片內容的描述填入 [**DXVAHD \_ CONTENT \_ DESC**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc) 結構。</span><span class="sxs-lookup"><span data-stu-id="8d76e-113">Fill in a [**DXVAHD\_CONTENT\_DESC**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc) structure with a description of the video content.</span></span> <span data-ttu-id="8d76e-114">驅動程式會使用這項資訊做為提示，以優化視頻處理器的功能。</span><span class="sxs-lookup"><span data-stu-id="8d76e-114">The driver uses this information as a hint to optimize the capabilities of the video processor.</span></span> <span data-ttu-id="8d76e-115">結構未包含完整的格式描述。</span><span class="sxs-lookup"><span data-stu-id="8d76e-115">The structure does not contain a complete format description.</span></span>
    ```C++
        DXVAHD_RATIONAL fps = { VIDEO_FPS, 1 }; 

        DXVAHD_CONTENT_DESC desc;

        desc.InputFrameFormat = DXVAHD_FRAME_FORMAT_PROGRESSIVE;
        desc.InputFrameRate = fps;
        desc.InputWidth = VIDEO_WIDTH;
        desc.InputHeight = VIDEO_HEIGHT;
        desc.OutputFrameRate = fps;
        desc.OutputWidth = VIDEO_WIDTH;
        desc.OutputHeight = VIDEO_HEIGHT;
    ```

    

2.  <span data-ttu-id="8d76e-116">呼叫 [**DXVAHD \_ CreateDevice**](/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice) 來建立 DXVA-HD 裝置。</span><span class="sxs-lookup"><span data-stu-id="8d76e-116">Call [**DXVAHD\_CreateDevice**](/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice) to create the DXVA-HD device.</span></span> <span data-ttu-id="8d76e-117">此函式會傳回 [**IDXVAHD \_ 裝置**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="8d76e-117">This function returns a pointer to the [**IDXVAHD\_Device**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device) interface.</span></span>
    ```C++
        hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc, DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
            NULL, &pDXVAHD);
    ```

    

3.  <span data-ttu-id="8d76e-118">呼叫 [**IDXVAHD \_ Device：： GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps)。</span><span class="sxs-lookup"><span data-stu-id="8d76e-118">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps).</span></span> <span data-ttu-id="8d76e-119">這個方法會以裝置功能填入 [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) 結構中。</span><span class="sxs-lookup"><span data-stu-id="8d76e-119">This method fills in a [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure with the device capabilities.</span></span> <span data-ttu-id="8d76e-120">如果您需要特定的影片處理功能（例如 luma 鍵控或映射篩選），請使用此結構來檢查其可用性。</span><span class="sxs-lookup"><span data-stu-id="8d76e-120">If you require specific video processing features, such as luma keying or image filtering, check their availability by using this structure.</span></span>
    ```C++
        DXVAHD_VPDEVCAPS caps;

        hr = pDXVAHD->GetVideoProcessorDeviceCaps(&caps);
    ```

    

4.  <span data-ttu-id="8d76e-121">檢查 DXVA-HD 裝置是否支援您需要的輸入影片格式。</span><span class="sxs-lookup"><span data-stu-id="8d76e-121">Check whether the DXVA-HD device supports the input video formats that you require.</span></span> <span data-ttu-id="8d76e-122">[檢查支援的 DXVA-HD 格式](checking-supported-dxva-hd-formats.md)的主題會更詳細地說明此步驟。</span><span class="sxs-lookup"><span data-stu-id="8d76e-122">The topic [Checking Supported DXVA-HD Formats](checking-supported-dxva-hd-formats.md) describes this step in more detail.</span></span>
5.  <span data-ttu-id="8d76e-123">檢查 DXVA-HD 裝置是否支援您所需的輸出格式。</span><span class="sxs-lookup"><span data-stu-id="8d76e-123">Check whether the DXVA-HD device supports the output format that you require.</span></span> <span data-ttu-id="8d76e-124">[檢查支援的 DXVA-HD 格式](checking-supported-dxva-hd-formats.md)一節會更詳細地說明此步驟。</span><span class="sxs-lookup"><span data-stu-id="8d76e-124">The section [Checking Supported DXVA-HD Formats](checking-supported-dxva-hd-formats.md) describes this step in more detail.</span></span>
6.  <span data-ttu-id="8d76e-125">配置 [**DXVAHD \_ VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="8d76e-125">Allocate an array of [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structures.</span></span> <span data-ttu-id="8d76e-126">必須配置的陣列元素數目是由在步驟3中取得之 [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps)結構的 **VideoProcessorCount** 成員所指定。</span><span class="sxs-lookup"><span data-stu-id="8d76e-126">The number of array elements that must be allocated is given by the **VideoProcessorCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure, obtained in step 3.</span></span>
    ```C++
        // Create the array of video processor caps. 
        
        DXVAHD_VPCAPS *pVPCaps = 
            new (std::nothrow) DXVAHD_VPCAPS[ caps.VideoProcessorCount ];

        if (pVPCaps == NULL)
        {
            return E_OUTOFMEMORY;
        }
    ```

    

7.  <span data-ttu-id="8d76e-127">每個 [**DXVAHD \_ VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) 結構都代表不同的視頻處理器。</span><span class="sxs-lookup"><span data-stu-id="8d76e-127">Each [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structure represents a distinct video processor.</span></span> <span data-ttu-id="8d76e-128">您可以執行此陣列的迴圈，以探索每部視頻處理器的功能。</span><span class="sxs-lookup"><span data-stu-id="8d76e-128">You can loop through this array to discover the capabilities of each video processor.</span></span> <span data-ttu-id="8d76e-129">此結構包含影片處理器之去交錯、電影和畫面播放速率轉換功能的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8d76e-129">The structure includes information about the deinterlacing, telecine, and frame-rate conversion capabilities of the video processor.</span></span>
8.  <span data-ttu-id="8d76e-130">選取要建立的視頻處理器。</span><span class="sxs-lookup"><span data-stu-id="8d76e-130">Select a video processor to create.</span></span> <span data-ttu-id="8d76e-131">[**DXVAHD \_ VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps)結構的 **VPGuid** 成員包含可唯一識別視頻處理器的 GUID。</span><span class="sxs-lookup"><span data-stu-id="8d76e-131">The **VPGuid** member of the [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structure contains a GUID that uniquely identifies the video processor.</span></span> <span data-ttu-id="8d76e-132">將此 GUID 傳遞給 [**IDXVAHD \_ Device：： CreateVideoProcessor**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor) 方法。</span><span class="sxs-lookup"><span data-stu-id="8d76e-132">Pass this GUID to the [**IDXVAHD\_Device::CreateVideoProcessor**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor) method.</span></span> <span data-ttu-id="8d76e-133">方法會傳回 [**IDXVAHD \_ VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor) 指標。</span><span class="sxs-lookup"><span data-stu-id="8d76e-133">The method returns an [**IDXVAHD\_VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor) pointer.</span></span>
    ```C++
        HRESULT hr = pDXVAHD->GetVideoProcessorCaps(
            caps.VideoProcessorCount, pVPCaps);
    ```

    

9.  <span data-ttu-id="8d76e-134">（選擇性）呼叫 [**IDXVAHD \_ Device：： CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) 來建立輸入影片表面的陣列。</span><span class="sxs-lookup"><span data-stu-id="8d76e-134">Optionally, call [**IDXVAHD\_Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) to create an array of input video surfaces.</span></span>

<span data-ttu-id="8d76e-135">下列程式碼範例顯示完整的步驟順序：</span><span class="sxs-lookup"><span data-stu-id="8d76e-135">The following code example shows the complete sequence of steps:</span></span>


```C++
// Initializes the DXVA-HD video processor.

// NOTE: The following example makes some simplifying assumptions:
//
// 1. There is a single input stream.
// 2. The input frame rate matches the output frame rate.
// 3. No advanced DXVA-HD features are needed, such as luma keying or IVTC.
// 4. The application uses a single input video surface.

HRESULT InitializeDXVAHD()
{
    if (g_pD3DDevice == NULL)
    {
        return E_FAIL;
    }

    HRESULT hr = S_OK;

    IDXVAHD_Device          *pDXVAHD = NULL;
    IDXVAHD_VideoProcessor  *pDXVAVP = NULL;
    IDirect3DSurface9       *pSurf = NULL;

    DXVAHD_RATIONAL fps = { VIDEO_FPS, 1 }; 

    DXVAHD_CONTENT_DESC desc;

    desc.InputFrameFormat = DXVAHD_FRAME_FORMAT_PROGRESSIVE;
    desc.InputFrameRate = fps;
    desc.InputWidth = VIDEO_WIDTH;
    desc.InputHeight = VIDEO_HEIGHT;
    desc.OutputFrameRate = fps;
    desc.OutputWidth = VIDEO_WIDTH;
    desc.OutputHeight = VIDEO_HEIGHT;

#ifdef USE_SOFTWARE_PLUGIN    
    HMODULE hSWPlugin = LoadLibrary(L"C:\\dxvahdsw.dll");

    PDXVAHDSW_Plugin pSWPlugin = (PDXVAHDSW_Plugin)GetProcAddress(hSWPlugin, "DXVAHDSW_Plugin");

    hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc,DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
        pSWPlugin, &pDXVAHD);
#else
    hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc, DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
        NULL, &pDXVAHD);
#endif
    if (FAILED(hr))
    {
        goto done;
    }

    DXVAHD_VPDEVCAPS caps;

    hr = pDXVAHD->GetVideoProcessorDeviceCaps(&caps);
    if (FAILED(hr))
    {
        goto done;
    }

    // Check whether the device supports the input and output formats.

    hr = CheckInputFormatSupport(pDXVAHD, caps, VIDEO_FORMAT);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CheckOutputFormatSupport(pDXVAHD, caps, RENDER_TARGET_FORMAT);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the VP device.
    hr = CreateVPDevice(pDXVAHD, caps, &pDXVAVP);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the video surface for the primary video stream.
    hr = pDXVAHD->CreateVideoSurface(
        VIDEO_WIDTH,
        VIDEO_HEIGHT,
        VIDEO_FORMAT,
        caps.InputPool,
        0,  // Usage
        DXVAHD_SURFACE_TYPE_VIDEO_INPUT,
        1,      // Number of surfaces to create
        &pSurf, // Array of surface pointers
        NULL
        );

    if (FAILED(hr))
    {
        goto done;
    }


    g_pDXVAHD = pDXVAHD;
    g_pDXVAHD->AddRef();

    g_pDXVAVP = pDXVAVP;
    g_pDXVAVP->AddRef();

    g_pSurface = pSurf;
    g_pSurface->AddRef();

done:
    SafeRelease(&pDXVAHD);
    SafeRelease(&pDXVAVP);
    SafeRelease(&pSurf);
    return hr;
}
```



<span data-ttu-id="8d76e-136">此範例中顯示的 CreateVPDevice 函式會建立影片處理器 (步驟5– 7) ：</span><span class="sxs-lookup"><span data-stu-id="8d76e-136">The CreateVPDevice function show in this example creates the video processor (steps 5–7):</span></span>


```C++
// Creates a DXVA-HD video processor.

HRESULT CreateVPDevice(
    IDXVAHD_Device          *pDXVAHD,
    const DXVAHD_VPDEVCAPS& caps,
    IDXVAHD_VideoProcessor  **ppDXVAVP
    )
{
    // Create the array of video processor caps. 
    
    DXVAHD_VPCAPS *pVPCaps = 
        new (std::nothrow) DXVAHD_VPCAPS[ caps.VideoProcessorCount ];

    if (pVPCaps == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pDXVAHD->GetVideoProcessorCaps(
        caps.VideoProcessorCount, pVPCaps);

    // At this point, an application could loop through the array and examine
    // the capabilities. For purposes of this example, however, we simply
    // create the first video processor in the list.

    if (SUCCEEDED(hr))
    {
        // The VPGuid member contains the GUID that identifies the video 
        // processor.

        hr = pDXVAHD->CreateVideoProcessor(&pVPCaps[0].VPGuid, ppDXVAVP);
    }

    delete [] pVPCaps;
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="8d76e-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="8d76e-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d76e-138">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="8d76e-138">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



