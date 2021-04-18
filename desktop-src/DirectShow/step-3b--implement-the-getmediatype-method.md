---
description: 步驟3B。
ms.assetid: 0ec57083-b192-404a-938f-bc6bb1cf0ddb
title: 步驟3B。 執行 GetMediaType 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab3ee41c6740fc2914f943784c0d51116f90428
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104514328"
---
# <a name="step-3b-implement-the-getmediatype-method"></a><span data-ttu-id="bd83a-104">步驟3B。</span><span class="sxs-lookup"><span data-stu-id="bd83a-104">Step 3B.</span></span> <span data-ttu-id="bd83a-105">執行 GetMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="bd83a-105">Implement the GetMediaType Method</span></span>

<span data-ttu-id="bd83a-106">這是 [撰寫轉換篩選](writing-transform-filters.md)之教學課程的步驟3b。</span><span class="sxs-lookup"><span data-stu-id="bd83a-106">This is step 3B of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="bd83a-107">衍生自 **CTransInPlaceFilter** 的篩選不需要此步驟。</span><span class="sxs-lookup"><span data-stu-id="bd83a-107">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="bd83a-108">[**CTransformFilter：： GetMediaType**](ctransformfilter-getmediatype.md)方法會傳回其中一個篩選器慣用的輸出類型，並依索引編號參考。</span><span class="sxs-lookup"><span data-stu-id="bd83a-108">The [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method returns one of the filter's preferred output types, referenced by index number.</span></span> <span data-ttu-id="bd83a-109">除非已經連接篩選的輸入釘選，否則永遠不會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="bd83a-109">This method is never called unless the filter's input pin is already connected.</span></span> <span data-ttu-id="bd83a-110">因此，您可以從上游連接使用媒體類型來判斷慣用的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="bd83a-110">Therefore, you can use the media type from the upstream connection to determine the preferred output types.</span></span>

<span data-ttu-id="bd83a-111">編碼器通常會提供代表目標格式的單一慣用類型。</span><span class="sxs-lookup"><span data-stu-id="bd83a-111">An encoder typically offers a single preferred type, representing the target format.</span></span> <span data-ttu-id="bd83a-112">這些解碼器通常支援一系列的輸出格式，並以遞減品質或效率的順序提供這些格式。</span><span class="sxs-lookup"><span data-stu-id="bd83a-112">Decoders generally support a range of output formats, and offer them in order of descending quality or efficiency.</span></span> <span data-ttu-id="bd83a-113">例如，清單可能是 UYVY、Y211、RGB-24、RGB-565、RGB-555 和 RGB-8 （依該順序）。</span><span class="sxs-lookup"><span data-stu-id="bd83a-113">For example, the list might be UYVY, Y211, RGB-24, RGB-565, RGB-555, and RGB-8, in that order.</span></span> <span data-ttu-id="bd83a-114">效果篩選可能需要輸出格式和輸入格式之間完全相符。</span><span class="sxs-lookup"><span data-stu-id="bd83a-114">Effect filters may require an exact match between the output format and the input format.</span></span>

<span data-ttu-id="bd83a-115">下列範例會傳回單一輸出型別，這個輸出型別是藉由修改輸入類型來指定 RLE8 壓縮來建立的：</span><span class="sxs-lookup"><span data-stu-id="bd83a-115">The following example returns a single output type, which is constructed by modifying the input type to specify RLE8 compression:</span></span>


```C++
HRESULT CRleFilter::GetMediaType(int iPosition, CMediaType *pMediaType)
{
    ASSERT(m_pInput->IsConnected());
    if (iPosition < 0)
    {
        return E_INVALIDARG;
    }
    if (iPosition == 0)
    {
        HRESULT hr = m_pInput->ConnectionMediaType(pMediaType);
        if (FAILED(hr))
        {
            return hr;
        }
        FOURCCMap fccMap = FCC('MRLE'); 
        pMediaType->subtype = static_cast<GUID>(fccMap);
        pMediaType->SetVariableSize();
        pMediaType->SetTemporalCompression(FALSE);

        ASSERT(pMediaType->formattype == FORMAT_VideoInfo);
        VIDEOINFOHEADER *pVih =
            reinterpret_cast<VIDEOINFOHEADER*>(pMediaType->pbFormat);
        pVih->bmiHeader.biCompression = BI_RLE8;
        pVih->bmiHeader.biSizeImage = DIBSIZE(pVih->bmiHeader); 
        return S_OK;
    }
    // else
    return VFW_S_NO_MORE_ITEMS;
}
```



<span data-ttu-id="bd83a-116">在此範例中，此方法會呼叫 [**IPin：： ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) ，以從輸入的 pin 取得輸入類型。</span><span class="sxs-lookup"><span data-stu-id="bd83a-116">In this example, the method calls [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) to get the input type from the input pin.</span></span> <span data-ttu-id="bd83a-117">然後，它會變更一些欄位以表示壓縮格式，如下所示：</span><span class="sxs-lookup"><span data-stu-id="bd83a-117">Then it changes some of the fields to indicate the compression format, as follows:</span></span>

-   <span data-ttu-id="bd83a-118">它會指派新的子類型 GUID，此 GUID 是使用 [**FOURCCMap**](fourccmap.md) 類別，從 FOURCC 程式碼 ' MRLE ' 所建立。</span><span class="sxs-lookup"><span data-stu-id="bd83a-118">It assigns a new subtype GUID, which is constructed from the FOURCC code 'MRLE', using the [**FOURCCMap**](fourccmap.md) class.</span></span>
-   <span data-ttu-id="bd83a-119">它會呼叫 [**CMediaType：： SetVariableSize**](cmediatype-setvariablesize.md) 方法，它會將 **bFixedSizeSamples** 旗標設為 **FALSE** ，並將 **lSampleSize** 成員設定為零，以指出可變大小的範例。</span><span class="sxs-lookup"><span data-stu-id="bd83a-119">It calls the [**CMediaType::SetVariableSize**](cmediatype-setvariablesize.md) method, which sets the **bFixedSizeSamples** flag to **FALSE** and the **lSampleSize** member to zero, indicating variable-sized samples.</span></span>
-   <span data-ttu-id="bd83a-120">它會呼叫 [**CMediaType：： SetTemporalCompression**](cmediatype-settemporalcompression.md) 方法，其值 **為 FALSE**，表示每個畫面格都是主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="bd83a-120">It calls the [**CMediaType::SetTemporalCompression**](cmediatype-settemporalcompression.md) method with the value **FALSE**, indicating that every frame is a key frame.</span></span> <span data-ttu-id="bd83a-121"> (此欄位僅供參考，所以您可以放心地忽略它。 ) </span><span class="sxs-lookup"><span data-stu-id="bd83a-121">(This field is informational only, so you could safely ignore it.)</span></span>
-   <span data-ttu-id="bd83a-122">它會將 **biCompression** 欄位設定為 BI \_ RLE8。</span><span class="sxs-lookup"><span data-stu-id="bd83a-122">It sets the **biCompression** field to BI\_RLE8.</span></span>
-   <span data-ttu-id="bd83a-123">它會將 **biSizeImage** 欄位設定為影像大小。</span><span class="sxs-lookup"><span data-stu-id="bd83a-123">It sets the **biSizeImage** field to the image size.</span></span>

<span data-ttu-id="bd83a-124">下一 [步：步驟3c：執行 CheckTransform 方法](step-3c--implement-the-checktransform-method.md)。</span><span class="sxs-lookup"><span data-stu-id="bd83a-124">Next: [Step 3C. Implement the CheckTransform Method](step-3c--implement-the-checktransform-method.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd83a-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="bd83a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd83a-126">撰寫 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="bd83a-126">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



