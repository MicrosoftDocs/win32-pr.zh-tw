---
description: .
ms.assetid: a4508a1e-d68b-4c55-bce4-c8b462134fa1
title: 建立 DXVA-HD 影片表面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 459504a312ec0d59cf3642f528f433ffce8ba094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847641"
---
# <a name="creating-dxva-hd-video-surfaces"></a><span data-ttu-id="aa973-103">建立 DXVA-HD 影片表面</span><span class="sxs-lookup"><span data-stu-id="aa973-103">Creating DXVA-HD Video Surfaces</span></span>

<span data-ttu-id="aa973-104">應用程式必須建立一或多個 Direct3D 介面，以用於輸入畫面。</span><span class="sxs-lookup"><span data-stu-id="aa973-104">The application must create one or more Direct3D surfaces to use for the input frames.</span></span> <span data-ttu-id="aa973-105">這些必須配置於 [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps)結構的 **InputPool** 成員所指定的記憶體集區中。</span><span class="sxs-lookup"><span data-stu-id="aa973-105">These must be allocated in the memory pool specified by the **InputPool** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="aa973-106">您可以使用下列介面類別型：</span><span class="sxs-lookup"><span data-stu-id="aa973-106">The following surface types can be used:</span></span>

-   <span data-ttu-id="aa973-107">藉由呼叫 [**IDXVAHD \_ Device：： CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) 並指定 **DXVAHD \_ 介面 \_ 類型 \_ 影片 \_ 輸入** 或 DXVAHD 介面類別型的 **影片 \_ \_ \_ \_ 輸入 \_ 私人** 介面類別型所建立的視頻界面。</span><span class="sxs-lookup"><span data-stu-id="aa973-107">A video surface created by calling [**IDXVAHD\_Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) and specifying the **DXVAHD\_SURFACE\_TYPE\_VIDEO\_INPUT** or **DXVAHD\_SURFACE\_TYPE\_VIDEO\_INPUT\_PRIVATE** surface type.</span></span> <span data-ttu-id="aa973-108">此介面類別型相當於非畫面的一般表面。</span><span class="sxs-lookup"><span data-stu-id="aa973-108">This surface type is equivalent to an off-screen plain surface.</span></span>
-   <span data-ttu-id="aa973-109">藉由呼叫 [**IDirectXVideoAccelerationService：： CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) 並指定 **DXVA2 \_ VideoDecoderRenderTarget** 介面型別所建立的「解碼器呈現目標介面」。</span><span class="sxs-lookup"><span data-stu-id="aa973-109">A decoder render-target surface, created by calling [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) and specifying the **DXVA2\_VideoDecoderRenderTarget** surface type.</span></span> <span data-ttu-id="aa973-110">此介面類別型用於 DXVA 解碼。</span><span class="sxs-lookup"><span data-stu-id="aa973-110">This surface type is used for DXVA decoding.</span></span>
-   <span data-ttu-id="aa973-111">純螢幕表面。</span><span class="sxs-lookup"><span data-stu-id="aa973-111">An off-screen plain surface.</span></span>

<span data-ttu-id="aa973-112">下列程式碼顯示如何使用 [**CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface)來配置視頻界面：</span><span class="sxs-lookup"><span data-stu-id="aa973-112">The following code shows how to allocate a video surface, using [**CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface):</span></span>


```C++
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
```



## <a name="related-topics"></a><span data-ttu-id="aa973-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="aa973-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa973-114">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="aa973-114">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



