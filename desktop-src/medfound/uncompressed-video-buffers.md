---
description: 未壓縮的影片緩衝區
ms.assetid: be5ec8a8-2d0b-401b-9d05-fdb87ad8c864
title: 未壓縮的影片緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24eda19136bf2dd7bc77f95d0efa6c48ca96e79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978886"
---
# <a name="uncompressed-video-buffers"></a><span data-ttu-id="a60b8-103">未壓縮的影片緩衝區</span><span class="sxs-lookup"><span data-stu-id="a60b8-103">Uncompressed Video Buffers</span></span>

<span data-ttu-id="a60b8-104">本文說明如何使用包含未壓縮影片畫面的媒體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a60b8-104">This article describes how to work with media buffers that contain uncompressed video frames.</span></span> <span data-ttu-id="a60b8-105">依喜好設定的順序，有下列選項可供使用。</span><span class="sxs-lookup"><span data-stu-id="a60b8-105">In order of preference, the following options are available.</span></span> <span data-ttu-id="a60b8-106">並非每個媒體緩衝區都支援每個選項。</span><span class="sxs-lookup"><span data-stu-id="a60b8-106">Not every media buffer supports each option.</span></span>

1.  <span data-ttu-id="a60b8-107">使用基礎 Direct3D 介面。</span><span class="sxs-lookup"><span data-stu-id="a60b8-107">Use the underlying Direct3D surface.</span></span> <span data-ttu-id="a60b8-108"> (僅適用于儲存在 Direct3D 介面中的影片畫面。 ) </span><span class="sxs-lookup"><span data-stu-id="a60b8-108">(Applies only to video frames stored in Direct3D surfaces.)</span></span>
2.  <span data-ttu-id="a60b8-109">使用 [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) 介面。</span><span class="sxs-lookup"><span data-stu-id="a60b8-109">Use the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>
3.  <span data-ttu-id="a60b8-110">使用 [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) 介面。</span><span class="sxs-lookup"><span data-stu-id="a60b8-110">Use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span>

## <a name="use-the-underlying-direct3d-surface"></a><span data-ttu-id="a60b8-111">使用基礎 Direct3D 介面</span><span class="sxs-lookup"><span data-stu-id="a60b8-111">Use the Underlying Direct3D Surface</span></span>

<span data-ttu-id="a60b8-112">影片畫面可能儲存在 Direct3D 介面內。</span><span class="sxs-lookup"><span data-stu-id="a60b8-112">The video frame might be stored inside a Direct3D surface.</span></span> <span data-ttu-id="a60b8-113">若是如此，您可以呼叫 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 或 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) 在媒體緩衝區物件上取得介面指標。</span><span class="sxs-lookup"><span data-stu-id="a60b8-113">If so, you can get a pointer to the surface by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) or [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) on the media buffer object.</span></span> <span data-ttu-id="a60b8-114">使用服務識別碼 MR \_ 緩衝區 \_ 服務。</span><span class="sxs-lookup"><span data-stu-id="a60b8-114">Use the service identifier MR\_BUFFER\_SERVICE.</span></span> <span data-ttu-id="a60b8-115">當存取影片畫面的元件設計為使用 Direct3D 時，建議使用此方法。</span><span class="sxs-lookup"><span data-stu-id="a60b8-115">This approach is recommended when the component accessing the video frame is designed to use Direct3D.</span></span> <span data-ttu-id="a60b8-116">例如，支援 DirectX Video 加速的影片解碼應使用此方法。</span><span class="sxs-lookup"><span data-stu-id="a60b8-116">For example, a video decoder that supports DirectX Video Acceleration should use this approach.</span></span>

<span data-ttu-id="a60b8-117">下列程式碼顯示如何從媒體緩衝區取得 **IDirect3DSurface9** 指標。</span><span class="sxs-lookup"><span data-stu-id="a60b8-117">The following code shows how to get the **IDirect3DSurface9** pointer from a media buffer.</span></span>


```C++
IDirect3DSurface9 *pSurface = NULL;

hr = MFGetService(
    pBuffer, 
    MR_BUFFER_SERVICE,
    __uuidof(IDirect3DSurface9), 
    (void**)&pSurface
    );

if (SUCCEEDED(hr))
{
    // Call IDirect3DSurface9 methods.
}
```



<span data-ttu-id="a60b8-118">下列物件支援 **MR \_ 緩衝區 \_ 服務** 服務：</span><span class="sxs-lookup"><span data-stu-id="a60b8-118">The following objects support the **MR\_BUFFER\_SERVICE** service:</span></span>

-   [<span data-ttu-id="a60b8-119">DirectX 介面緩衝區</span><span class="sxs-lookup"><span data-stu-id="a60b8-119">DirectX Surface Buffer</span></span>](directx-surface-buffer.md)
-   [<span data-ttu-id="a60b8-120">影片範例</span><span class="sxs-lookup"><span data-stu-id="a60b8-120">Video Samples</span></span>](video-samples.md)

## <a name="use-the-imf2dbuffer-interface"></a><span data-ttu-id="a60b8-121">使用 IMF2DBuffer 介面</span><span class="sxs-lookup"><span data-stu-id="a60b8-121">Use the IMF2DBuffer Interface</span></span>

<span data-ttu-id="a60b8-122">如果影片畫面未儲存在 Direct3D 介面內，或元件不是設計成使用 Direct3D，則下一次存取影片框架的建議方式是查詢 [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) 介面的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a60b8-122">If the video frame is not stored inside a Direct3D surface, or the component is not designed to use Direct3D, the next recommended way to access the video frame is to query the buffer for the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span> <span data-ttu-id="a60b8-123">此介面是專為影像資料所設計。</span><span class="sxs-lookup"><span data-stu-id="a60b8-123">This interface is designed specifically for image data.</span></span> <span data-ttu-id="a60b8-124">若要取得這個介面的指標，請呼叫媒體緩衝區上的 **QueryInterface** 。</span><span class="sxs-lookup"><span data-stu-id="a60b8-124">To get a pointer to this interface, call **QueryInterface** on the media buffer.</span></span> <span data-ttu-id="a60b8-125">並非所有媒體緩衝區物件都會公開這個介面。</span><span class="sxs-lookup"><span data-stu-id="a60b8-125">Not all media buffer objects expose this interface.</span></span> <span data-ttu-id="a60b8-126">但是，如果媒體緩衝區確實公開了 **IMF2DBuffer** 介面，您應該使用該介面來存取資料（可能的話），而不是使用 [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)。</span><span class="sxs-lookup"><span data-stu-id="a60b8-126">But if a media buffer does expose the **IMF2DBuffer** interface, you should use that interface to access the data, if possible, rather than using [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer).</span></span> <span data-ttu-id="a60b8-127">您仍然可以使用 **IMFMediaBuffer** 介面，但效率可能較低。</span><span class="sxs-lookup"><span data-stu-id="a60b8-127">You can still use the **IMFMediaBuffer** interface, but it might be less efficient.</span></span>

1.  <span data-ttu-id="a60b8-128">呼叫媒體緩衝區上的 **QueryInterface** 來取得 [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) 介面。</span><span class="sxs-lookup"><span data-stu-id="a60b8-128">Call **QueryInterface** on the media buffer to get the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>
2.  <span data-ttu-id="a60b8-129">呼叫 [**IMF2DBuffer：： Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) 來存取緩衝區的記憶體。</span><span class="sxs-lookup"><span data-stu-id="a60b8-129">Call [**IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) to access the memory for the buffer.</span></span> <span data-ttu-id="a60b8-130">這個方法會傳回最上層圖元的第一個位元組指標。</span><span class="sxs-lookup"><span data-stu-id="a60b8-130">This method returns a pointer to the first byte of the top row of pixels.</span></span> <span data-ttu-id="a60b8-131">它也會傳回影像跨距，也就是從資料列開始到下一個資料列開頭的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="a60b8-131">It also returns the image stride, which is the number of bytes from the start of a row of pixels to the start of the next row.</span></span> <span data-ttu-id="a60b8-132">緩衝區可能會在每個圖元資料列之後包含填補位元組，因此跨距可能會超出影像寬度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a60b8-132">The buffer might contain padding bytes after each row of pixels, so the stride might be wider than the image width in bytes.</span></span> <span data-ttu-id="a60b8-133">如果在記憶體中將影像導向最下層，則 Stride 也可以是負數。</span><span class="sxs-lookup"><span data-stu-id="a60b8-133">Stride can also be negative if the image is oriented bottom-up in memory.</span></span> <span data-ttu-id="a60b8-134">如需詳細資訊，請參閱 [影像 Stride](image-stride.md)。</span><span class="sxs-lookup"><span data-stu-id="a60b8-134">For more information, see [Image Stride](image-stride.md).</span></span>
3.  <span data-ttu-id="a60b8-135">只有當您需要存取記憶體時，才讓緩衝區保持鎖定。</span><span class="sxs-lookup"><span data-stu-id="a60b8-135">Keep the buffer locked only while you need to access the memory.</span></span> <span data-ttu-id="a60b8-136">藉由呼叫 [**IMF2DBuffer：： Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d)來解除鎖定緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a60b8-136">Unlock the buffer by calling [**IMF2DBuffer::Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d).</span></span>

<span data-ttu-id="a60b8-137">並非每個媒體緩衝區都能實行 [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) 介面。</span><span class="sxs-lookup"><span data-stu-id="a60b8-137">Not every media buffer implements the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span> <span data-ttu-id="a60b8-138">如果媒體緩衝區未執行這個介面 (也就是，在步驟 1) 中，緩衝區物件會傳回 E \_ NOINTERFACE，您必須使用 [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) 介面介面（如下所述）。</span><span class="sxs-lookup"><span data-stu-id="a60b8-138">If the media buffer does not implement this interface (that is, the buffer object returns E\_NOINTERFACE in step 1), you must use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface interface, described next.</span></span>

## <a name="use-the-imfmediabuffer-interface"></a><span data-ttu-id="a60b8-139">使用 IMFMediaBuffer 介面</span><span class="sxs-lookup"><span data-stu-id="a60b8-139">Use the IMFMediaBuffer Interface</span></span>

<span data-ttu-id="a60b8-140">如果媒體緩衝區未公開 [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) 介面，請使用 [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) 介面。</span><span class="sxs-lookup"><span data-stu-id="a60b8-140">If a media buffer does not expose the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface, use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span> <span data-ttu-id="a60b8-141">[使用媒體緩衝區](working-with-media-buffers.md)的主題將描述此介面的一般語法。</span><span class="sxs-lookup"><span data-stu-id="a60b8-141">The general semantics of this interface are described in the topic [Working with Media Buffers](working-with-media-buffers.md).</span></span>

1.  <span data-ttu-id="a60b8-142">呼叫媒體緩衝區上的 **QueryInterface** 來取得 [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) 介面。</span><span class="sxs-lookup"><span data-stu-id="a60b8-142">Call **QueryInterface** on the media buffer to get the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span>
2.  <span data-ttu-id="a60b8-143">呼叫 [**IMFMediaBuffer：： Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) 以存取緩衝區記憶體。</span><span class="sxs-lookup"><span data-stu-id="a60b8-143">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to access the buffer memory.</span></span> <span data-ttu-id="a60b8-144">這個方法會傳回緩衝區記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="a60b8-144">This method returns a pointer to the buffer memory.</span></span> <span data-ttu-id="a60b8-145">使用 **鎖定** 方法時，stride 一律是有問題的影片格式最小的 stride，沒有額外的填補位元組。</span><span class="sxs-lookup"><span data-stu-id="a60b8-145">When the **Lock** method is used, the stride is always the minimum stride for the video format in question, with no extra padding bytes.</span></span>
3.  <span data-ttu-id="a60b8-146">只有當您需要存取記憶體時，才讓緩衝區保持鎖定。</span><span class="sxs-lookup"><span data-stu-id="a60b8-146">Keep the buffer locked only while you need to access the memory.</span></span> <span data-ttu-id="a60b8-147">藉由呼叫 [**IMFMediaBuffer：： unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock)來解除鎖定緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a60b8-147">Unlock the buffer by calling [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).</span></span>

<span data-ttu-id="a60b8-148">如果緩衝區公開 [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)，您應該一律避免呼叫 [**IMFMediaBuffer：： Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) ，因為 **Lock** 方法可以強制緩衝區物件進入連續的記憶體區塊，然後再次返回。</span><span class="sxs-lookup"><span data-stu-id="a60b8-148">You should always avoid calling [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) if the buffer exposes [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer), because the **Lock** method can force the buffer object to the video frame into a contiguous memory block and then back again.</span></span> <span data-ttu-id="a60b8-149">另一方面，如果緩衝區不支援 **IMF2DBuffer**，則 **IMFMediaBuffer：： Lock** 可能不會產生複本。</span><span class="sxs-lookup"><span data-stu-id="a60b8-149">On the other hand, if the buffer does not support **IMF2DBuffer**, then **IMFMediaBuffer::Lock** will probably not result in a copy.</span></span>

<span data-ttu-id="a60b8-150">計算媒體類型的最小 stride，如下所示：</span><span class="sxs-lookup"><span data-stu-id="a60b8-150">Calculate the minimum stride from the media type as follows:</span></span>

-   <span data-ttu-id="a60b8-151">最小 stride 可能儲存在 [**MF \_ MT \_ 預設 \_ stride**](mf-mt-default-stride-attribute.md) 屬性中。</span><span class="sxs-lookup"><span data-stu-id="a60b8-151">The minimum stride might be stored in the [**MF\_MT\_DEFAULT\_STRIDE**](mf-mt-default-stride-attribute.md) attribute.</span></span>
-   <span data-ttu-id="a60b8-152">如果未設定 **MF \_ MT \_ 預設 \_ STRIDE** 屬性，請呼叫 [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) 函式來計算最常見影片格式的 STRIDE。</span><span class="sxs-lookup"><span data-stu-id="a60b8-152">If the **MF\_MT\_DEFAULT\_STRIDE** attribute is not set, call the [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) function to calculate the stride for most common video formats.</span></span>
-   <span data-ttu-id="a60b8-153">如果 [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) 函式無法辨識格式，您必須根據格式的定義來計算 stride。</span><span class="sxs-lookup"><span data-stu-id="a60b8-153">If the [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) function does not recognize the format, you must calculate the stride based on the definition of the format.</span></span> <span data-ttu-id="a60b8-154">在此情況下，不會有一般規則;您必須知道格式定義的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a60b8-154">In that case, there is no general rule; you need to know the details of the format definition.</span></span>

<span data-ttu-id="a60b8-155">下列程式碼顯示如何取得最常見影片格式的預設 stride。</span><span class="sxs-lookup"><span data-stu-id="a60b8-155">The following code shows how to get the default stride for the most common video formats.</span></span>


```C++
HRESULT GetDefaultStride(IMFMediaType *pType, LONG *plStride)
{
    LONG lStride = 0;

    // Try to get the default stride from the media type.
    HRESULT hr = pType->GetUINT32(MF_MT_DEFAULT_STRIDE, (UINT32*)&lStride);
    if (FAILED(hr))
    {
        // Attribute not set. Try to calculate the default stride.

        GUID subtype = GUID_NULL;

        UINT32 width = 0;
        UINT32 height = 0;

        // Get the subtype and the image size.
        hr = pType->GetGUID(MF_MT_SUBTYPE, &subtype);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = MFGetStrideForBitmapInfoHeader(subtype.Data1, width, &lStride);
        if (FAILED(hr))
        {
            goto done;
        }

        // Set the attribute for later reference.
        (void)pType->SetUINT32(MF_MT_DEFAULT_STRIDE, UINT32(lStride));
    }

    if (SUCCEEDED(hr))
    {
        *plStride = lStride;
    }

done:
    return hr;
}
```



<span data-ttu-id="a60b8-156">視您的應用程式而定，您可能會事先知道指定的媒體緩衝區是否支援 [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) (例如，如果您已建立緩衝區) 。</span><span class="sxs-lookup"><span data-stu-id="a60b8-156">Depending on your application, you might know in advance whether a given media buffer supports [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) (for example, if you created the buffer).</span></span> <span data-ttu-id="a60b8-157">否則，您必須準備好使用兩個緩衝區介面中的任一個。</span><span class="sxs-lookup"><span data-stu-id="a60b8-157">Otherwise, you must be prepared to use either of the two buffer interfaces.</span></span>

<span data-ttu-id="a60b8-158">下列範例顯示的 helper 類別會隱藏部分詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a60b8-158">The following example shows a helper class that hides some of these details.</span></span> <span data-ttu-id="a60b8-159">此類別具有 LockBuffer 方法，可呼叫 [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) 或 [**鎖定**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) ，並將指標傳回至第一個資料列的開頭。</span><span class="sxs-lookup"><span data-stu-id="a60b8-159">This class has a LockBuffer method that calls either [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) or [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) and returns a pointer to the start of the first row of pixels.</span></span> <span data-ttu-id="a60b8-160"> (此行為符合 **Lock2D** 方法。 ) LockBuffer 方法會採用預設 stride 做為輸入參數，並傳回實際的 stride 作為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="a60b8-160">(This behavior matches the **Lock2D** method.) The LockBuffer method takes the default stride as an input parameter and returns the actual stride as an output parameter.</span></span>


```C++
class CBufferLock
{
public:
    CBufferLock(IMFMediaBuffer *pBuffer) : m_p2DBuffer(NULL), m_bLocked(FALSE)
    {
        m_pBuffer = pBuffer;
        m_pBuffer->AddRef();

        m_pBuffer->QueryInterface(IID_IMF2DBuffer, (void**)&m_p2DBuffer);
    }

    ~CBufferLock()
    {
        UnlockBuffer();
        SafeRelease(&m_pBuffer);
        SafeRelease(&m_p2DBuffer);
    }

    HRESULT LockBuffer(
        LONG  lDefaultStride,    // Minimum stride (with no padding).
        DWORD dwHeightInPixels,  // Height of the image, in pixels.
        BYTE  **ppbScanLine0,    // Receives a pointer to the start of scan line 0.
        LONG  *plStride          // Receives the actual stride.
        )
    {
        HRESULT hr = S_OK;

        // Use the 2-D version if available.
        if (m_p2DBuffer)
        {
            hr = m_p2DBuffer->Lock2D(ppbScanLine0, plStride);
        }
        else
        {
            // Use non-2D version.
            BYTE *pData = NULL;

            hr = m_pBuffer->Lock(&pData, NULL, NULL);
            if (SUCCEEDED(hr))
            {
                *plStride = lDefaultStride;
                if (lDefaultStride < 0)
                {
                    // Bottom-up orientation. Return a pointer to the start of the
                    // last row *in memory* which is the top row of the image.
                    *ppbScanLine0 = pData + abs(lDefaultStride) * (dwHeightInPixels - 1);
                }
                else
                {
                    // Top-down orientation. Return a pointer to the start of the
                    // buffer.
                    *ppbScanLine0 = pData;
                }
            }
        }

        m_bLocked = (SUCCEEDED(hr));

        return hr;
    }
    
    void UnlockBuffer()
    {
        if (m_bLocked)
        {
            if (m_p2DBuffer)
            {
                (void)m_p2DBuffer->Unlock2D();
            }
            else
            {
                (void)m_pBuffer->Unlock();
            }
            m_bLocked = FALSE;
        }
    }

private:
    IMFMediaBuffer  *m_pBuffer;
    IMF2DBuffer     *m_p2DBuffer;

    BOOL            m_bLocked;
};
```



## <a name="related-topics"></a><span data-ttu-id="a60b8-161">相關主題</span><span class="sxs-lookup"><span data-stu-id="a60b8-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a60b8-162">影像 Stride</span><span class="sxs-lookup"><span data-stu-id="a60b8-162">Image Stride</span></span>](image-stride.md)
</dt> <dt>

[<span data-ttu-id="a60b8-163">媒體緩衝區</span><span class="sxs-lookup"><span data-stu-id="a60b8-163">Media Buffers</span></span>](media-buffers.md)
</dt> </dl>

 

 



