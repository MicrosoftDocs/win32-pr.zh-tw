---
description: DirectX 介面緩衝區
ms.assetid: 2c82c023-4436-4f8a-b896-7f4765f989b3
title: DirectX 介面緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02211d268e23bd7185cd480bee4e4dff297293b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111788"
---
# <a name="directx-surface-buffer"></a><span data-ttu-id="f6081-103">DirectX 介面緩衝區</span><span class="sxs-lookup"><span data-stu-id="f6081-103">DirectX Surface Buffer</span></span>

<span data-ttu-id="f6081-104">DirectX 介面緩衝區物件是管理 Direct3D 介面的媒體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f6081-104">The DirectX surface buffer object is a media buffer that manages a Direct3D surface.</span></span> <span data-ttu-id="f6081-105">若要建立這個物件的實例，請呼叫 [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer) 並傳入 DirectX 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="f6081-105">To create an instance of this object, call [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer) and pass in a pointer to the DirectX surface.</span></span> <span data-ttu-id="f6081-106">DirectX 介面緩衝區會公開下列介面：</span><span class="sxs-lookup"><span data-stu-id="f6081-106">The DirectX surface buffer exposes the following interfaces:</span></span>

-   [<span data-ttu-id="f6081-107">**IMFMediaBuffer**</span><span class="sxs-lookup"><span data-stu-id="f6081-107">**IMFMediaBuffer**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
-   [<span data-ttu-id="f6081-108">**IMF2DBuffer**</span><span class="sxs-lookup"><span data-stu-id="f6081-108">**IMF2DBuffer**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)
-   [<span data-ttu-id="f6081-109">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="f6081-109">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)

<span data-ttu-id="f6081-110">有數種方式可從緩衝區物件存取 surface memory：</span><span class="sxs-lookup"><span data-stu-id="f6081-110">There are several ways to access the surface memory from the buffer object:</span></span>

-   <span data-ttu-id="f6081-111">建議：對緩衝區呼叫 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 。</span><span class="sxs-lookup"><span data-stu-id="f6081-111">Recommended: Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the buffer.</span></span> <span data-ttu-id="f6081-112">使用服務識別碼 **MR \_ 緩衝區 \_ 服務**。</span><span class="sxs-lookup"><span data-stu-id="f6081-112">Use the service identifier **MR\_BUFFER\_SERVICE**.</span></span> <span data-ttu-id="f6081-113">方法會傳回基礎 Direct3D 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="f6081-113">The method returns a pointer to the underlying Direct3D surface.</span></span>
-   <span data-ttu-id="f6081-114">呼叫 [**IMF2DBuffer：： Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d)。</span><span class="sxs-lookup"><span data-stu-id="f6081-114">Call [**IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d).</span></span> <span data-ttu-id="f6081-115">這個方法會直接在介面上呼叫 **IDirect3DSurface9：： LockRect** 。</span><span class="sxs-lookup"><span data-stu-id="f6081-115">This method calls **IDirect3DSurface9::LockRect** directly on the surface.</span></span> <span data-ttu-id="f6081-116">[**IMF2DBuffer：： Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d)方法會在介面上呼叫 **UnlockRect** 。</span><span class="sxs-lookup"><span data-stu-id="f6081-116">The [**IMF2DBuffer::Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d) method calls **UnlockRect** on the surface.</span></span>
-   <span data-ttu-id="f6081-117">呼叫 [**IMFMediaBuffer：： Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock)。</span><span class="sxs-lookup"><span data-stu-id="f6081-117">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span></span> <span data-ttu-id="f6081-118">一般而言，這不是建議的作法，因為它會強制物件從 Direct3D 介面複製記憶體，然後再次返回。</span><span class="sxs-lookup"><span data-stu-id="f6081-118">Generally this is not recommended, because it forces the object to copy memory from the Direct3D surface and then back again.</span></span> <span data-ttu-id="f6081-119">[**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d)方法更有效率。</span><span class="sxs-lookup"><span data-stu-id="f6081-119">The [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) method is more efficient.</span></span>

<span data-ttu-id="f6081-120">如果基礎資料表面無法鎖定，則 [**鎖定**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) 和 [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) 可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="f6081-120">Both [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) and [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) can fail if the underlying surface is not lockable.</span></span> <span data-ttu-id="f6081-121">DirectX 介面緩衝區會針對並非設計來搭配 Direct3D 介面運作的元件，執行這兩種方法。</span><span class="sxs-lookup"><span data-stu-id="f6081-121">The DirectX surface buffer implements these two methods primarily for components that are not designed to work with Direct3D surfaces.</span></span>

<span data-ttu-id="f6081-122">增強型影片轉譯器 (EVR) 在未針對 DirectX Video 加速 (DXVA) 設定解碼器時，會建立 DirectX 介面緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f6081-122">The enhanced video renderer (EVR) creates DirectX surface buffers when the decoder is not configured for DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="f6081-123">如需詳細資訊，請參閱 [**IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator)。</span><span class="sxs-lookup"><span data-stu-id="f6081-123">For more information, see [**IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator).</span></span>

### <a name="obtaining-the-direct3d-surface"></a><span data-ttu-id="f6081-124">取得 Direct3D 介面</span><span class="sxs-lookup"><span data-stu-id="f6081-124">Obtaining the Direct3D Surface</span></span>

<span data-ttu-id="f6081-125">若要從影片範例取得 Direct3D 介面，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="f6081-125">To get a Direct3D surface from a video sample, do the following:</span></span>

1.  <span data-ttu-id="f6081-126">以零的索引值呼叫 [**IMFSample：： GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) 。</span><span class="sxs-lookup"><span data-stu-id="f6081-126">Call [**IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) with an index value of zero.</span></span>
2.  <span data-ttu-id="f6081-127">呼叫 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) 並指定 **MR \_ 緩衝區 \_ 服務** 服務識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6081-127">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) and specify the **MR\_BUFFER\_SERVICE** service identifier.</span></span>

<span data-ttu-id="f6081-128">下列程式碼顯示這些步驟：</span><span class="sxs-lookup"><span data-stu-id="f6081-128">The following code shows these steps:</span></span>


```C++
HRESULT GetD3DSurfaceFromSample(IMFSample *pSample, IDirect3DSurface9 **ppSurface)
{
    *ppSurface = NULL;

    IMFMediaBuffer *pBuffer = NULL;

    HRESULT hr = pSample->GetBufferByIndex(0, &pBuffer);
    if (SUCCEEDED(hr))
    {
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(ppSurface));
        pBuffer->Release();
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="f6081-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="f6081-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6081-130">媒體緩衝區</span><span class="sxs-lookup"><span data-stu-id="f6081-130">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="f6081-131">影片範例</span><span class="sxs-lookup"><span data-stu-id="f6081-131">Video Samples</span></span>](video-samples.md)
</dt> </dl>

 

 



