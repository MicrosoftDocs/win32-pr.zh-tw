---
description: 步驟3C。
ms.assetid: e780df46-bf47-4334-b788-05ad8179f051
title: 步驟3C。 執行 CheckTransform 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78148701fc54e73a6970d45fde95d70f4cf0df3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194763"
---
# <a name="step-3c-implement-the-checktransform-method"></a><span data-ttu-id="e5edb-104">步驟3C。</span><span class="sxs-lookup"><span data-stu-id="e5edb-104">Step 3C.</span></span> <span data-ttu-id="e5edb-105">執行 CheckTransform 方法</span><span class="sxs-lookup"><span data-stu-id="e5edb-105">Implement the CheckTransform Method</span></span>

<span data-ttu-id="e5edb-106">這是 [撰寫轉換篩選](writing-transform-filters.md)之教學課程的步驟3c。</span><span class="sxs-lookup"><span data-stu-id="e5edb-106">This is step 3C of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="e5edb-107">衍生自 **CTransInPlaceFilter** 的篩選不需要此步驟。</span><span class="sxs-lookup"><span data-stu-id="e5edb-107">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="e5edb-108">[**CTransformFilter：： CheckTransform**](ctransformfilter-checktransform.md)方法會檢查建議的輸出類型是否與目前的輸入類型相容。</span><span class="sxs-lookup"><span data-stu-id="e5edb-108">The [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method checks if a proposed output type is compatible with the current input type.</span></span> <span data-ttu-id="e5edb-109">如果輸入連接在輸出連接之後重新連接，也會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="e5edb-109">The method is also called if the input pin reconnects after the output pin connects.</span></span>

<span data-ttu-id="e5edb-110">下列範例會驗證格式是否為 RLE8 video;影像尺寸符合輸入格式;和調色板專案相同。</span><span class="sxs-lookup"><span data-stu-id="e5edb-110">The following example verifies whether the format is RLE8 video; the image dimensions match the input format; and the palette entries are the same.</span></span> <span data-ttu-id="e5edb-111">它也會拒絕不符合影像大小的來源和目標矩形。</span><span class="sxs-lookup"><span data-stu-id="e5edb-111">It also rejects source and target rectangles that do not match the image size.</span></span>


```C++
HRESULT CRleFilter::CheckTransform(
    const CMediaType *mtIn, const CMediaType *mtOut)
{
    // Check the major type.
    if (mtOut->majortype != MEDIATYPE_Video)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Check the subtype and format type.
    FOURCCMap fccMap = FCC('MRLE'); 
    if (mtOut->subtype != static_cast<GUID>(fccMap))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    if ((mtOut->formattype != FORMAT_VideoInfo) || 
        (mtOut->cbFormat < sizeof(VIDEOINFOHEADER)))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Compare the bitmap information against the input type.
    ASSERT(mtIn->formattype == FORMAT_VideoInfo);
    BITMAPINFOHEADER *pBmiOut = HEADER(mtOut->pbFormat);
    BITMAPINFOHEADER *pBmiIn = HEADER(mtIn->pbFormat);
    if ((pBmiOut->biPlanes != 1) ||
        (pBmiOut->biBitCount != 8) ||
        (pBmiOut->biCompression != BI_RLE8) ||
        (pBmiOut->biWidth != pBmiIn->biWidth) ||
        (pBmiOut->biHeight != pBmiIn->biHeight))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Compare source and target rectangles.
    RECT rcImg;
    SetRect(&rcImg, 0, 0, pBmiIn->biWidth, pBmiIn->biHeight);
    RECT *prcSrc = &((VIDEOINFOHEADER*)(mtIn->pbFormat))->rcSource;
    RECT *prcTarget = &((VIDEOINFOHEADER*)(mtOut->pbFormat))->rcTarget;
    if (!IsRectEmpty(prcSrc) && !EqualRect(prcSrc, &rcImg))
    {
        return VFW_E_INVALIDMEDIATYPE;
    }
    if (!IsRectEmpty(prcTarget) && !EqualRect(prcTarget, &rcImg))
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the palette table.
    if (pBmiOut->biClrUsed != pBmiIn->biClrUsed)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    DWORD cbPalette = pBmiOut->biClrUsed * sizeof(RGBQUAD);
    if (mtOut->cbFormat < sizeof(VIDEOINFOHEADER) + cbPalette)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    if (0 != memcmp(pBmiOut + 1, pBmiIn + 1, cbPalette))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Everything is good.
    return S_OK;
}
```



<span data-ttu-id="e5edb-112">**Pin 重新連接**</span><span class="sxs-lookup"><span data-stu-id="e5edb-112">**Pin Reconnections**</span></span>

<span data-ttu-id="e5edb-113">應用程式可以中斷連接並重新連接 pin。</span><span class="sxs-lookup"><span data-stu-id="e5edb-113">Applications can disconnect and reconnect pins.</span></span> <span data-ttu-id="e5edb-114">假設應用程式連接這兩個 pin、中斷輸入 pin 的連接，然後使用新的映射大小重新連接輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="e5edb-114">Suppose an application connects both pins, disconnects the input pin, and then reconnects the input pin using a new image size.</span></span> <span data-ttu-id="e5edb-115">在此情況下， **CheckTransform** 會失敗，因為影像的維度不再相符。</span><span class="sxs-lookup"><span data-stu-id="e5edb-115">In that case, **CheckTransform** fails because the dimensions of the image no longer match.</span></span> <span data-ttu-id="e5edb-116">這種行為很合理，雖然篩選也可以嘗試以新的媒體類型來重新連接輸出釘選。</span><span class="sxs-lookup"><span data-stu-id="e5edb-116">This behavior is reasonable, although the filter could also try reconnecting the output pin with a new media type.</span></span>

<span data-ttu-id="e5edb-117">下一 [步：步驟4。設定](step-4--set-allocator-properties.md)配置器屬性。</span><span class="sxs-lookup"><span data-stu-id="e5edb-117">Next: [Step 4. Set Allocator Properties](step-4--set-allocator-properties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5edb-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="e5edb-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5edb-119">重新連接釘選</span><span class="sxs-lookup"><span data-stu-id="e5edb-119">Reconnecting Pins</span></span>](reconnecting-pins.md)
</dt> <dt>

[<span data-ttu-id="e5edb-120">影片轉譯器中的來源和目標矩形</span><span class="sxs-lookup"><span data-stu-id="e5edb-120">Source and Target Rectangles in Video Renderers</span></span>](source-and-target-rectangles-in-video-renderers.md)
</dt> <dt>

[<span data-ttu-id="e5edb-121">撰寫 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="e5edb-121">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



