---
description: 步驟3A。
ms.assetid: 774fcb12-8928-4667-8ef6-dce86717cc29
title: 步驟3A。 執行 CheckInputType 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5eb6ff440838d7a4b65b586e5dba963ff254eef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988941"
---
# <a name="step-3a-implement-the-checkinputtype-method"></a><span data-ttu-id="55597-104">步驟3A。</span><span class="sxs-lookup"><span data-stu-id="55597-104">Step 3A.</span></span> <span data-ttu-id="55597-105">執行 CheckInputType 方法</span><span class="sxs-lookup"><span data-stu-id="55597-105">Implement the CheckInputType Method</span></span>

<span data-ttu-id="55597-106">這是 [撰寫轉換篩選](writing-transform-filters.md)之教學課程的步驟3a。</span><span class="sxs-lookup"><span data-stu-id="55597-106">This is step 3A of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="55597-107">當上游篩選準則向轉換篩選器提出媒體類型時，就會呼叫 [**CTransformFilter：： CheckInputType**](ctransformfilter-checkinputtype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="55597-107">The [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method is called when the upstream filter proposes a media type to the transform filter.</span></span> <span data-ttu-id="55597-108">這個方法會採用 [**CMediaType**](cmediatype.md) 物件的指標，這是 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的精簡型包裝函式。</span><span class="sxs-lookup"><span data-stu-id="55597-108">This method takes a pointer to a [**CMediaType**](cmediatype.md) object, which is a thin wrapper for the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="55597-109">在這個方法中，您應該檢查 **AM \_ 媒體 \_ 類型** 結構的每個相關欄位，包括格式區塊中的欄位。</span><span class="sxs-lookup"><span data-stu-id="55597-109">In this method, you should examine every relevant field of the **AM\_MEDIA\_TYPE** structure, including the fields in the format block.</span></span> <span data-ttu-id="55597-110">您可以使用 **CMediaType** 中定義的存取子方法，或直接參考結構成員。</span><span class="sxs-lookup"><span data-stu-id="55597-110">You can use the accessor methods defined in **CMediaType**, or reference the structure members directly.</span></span> <span data-ttu-id="55597-111">如果有任何欄位無效，則傳回 \_ \_ \_ 不接受的 VFW E 類型 \_ 。</span><span class="sxs-lookup"><span data-stu-id="55597-111">If any field is not valid, return VFW\_E\_TYPE\_NOT\_ACCEPTED.</span></span> <span data-ttu-id="55597-112">如果整個媒體類型都有效，請返回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="55597-112">If the entire media type is valid, return S\_OK.</span></span>

<span data-ttu-id="55597-113">例如，在 RLE 編碼器篩選器中，輸入類型必須是8位或4位未壓縮的 RGB 影片。</span><span class="sxs-lookup"><span data-stu-id="55597-113">For example, in the RLE encoder filter, the input type must be 8-bit or 4-bit uncompressed RGB video.</span></span> <span data-ttu-id="55597-114">由於篩選準則必須將它們轉換成較低的位深度，而 DirectShow 已經為該用途提供 [色彩空間轉換器](color-space-converter-filter.md) 篩選，因此不支援其他輸入格式，例如16或24位 RGB。</span><span class="sxs-lookup"><span data-stu-id="55597-114">There is no reason to support other input formats, such as 16- or 24-bit RGB, because the filter would have to convert them to a lower bit depth, and DirectShow already provides a [Color Space Converter](color-space-converter-filter.md) filter for that purpose.</span></span> <span data-ttu-id="55597-115">下列範例假設編碼器支援8位的影片，但不支援4位的影片：</span><span class="sxs-lookup"><span data-stu-id="55597-115">The following example assumes that the encoder supports 8-bit video but not 4-bit video:</span></span>


```C++
HRESULT CRleFilter::CheckInputType(const CMediaType *mtIn)
{
    if ((mtIn->majortype != MEDIATYPE_Video) ||
        (mtIn->subtype != MEDIASUBTYPE_RGB8) ||
        (mtIn->formattype != FORMAT_VideoInfo) || 
        (mtIn->cbFormat < sizeof(VIDEOINFOHEADER)))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    VIDEOINFOHEADER *pVih = 
        reinterpret_cast<VIDEOINFOHEADER*>(mtIn->pbFormat);
    if ((pVih->bmiHeader.biBitCount != 8) ||
        (pVih->bmiHeader.biCompression != BI_RGB))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Check the palette table.
    if (pVih->bmiHeader.biClrUsed > PALETTE_ENTRIES(pVih))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    DWORD cbPalette = pVih->bmiHeader.biClrUsed * sizeof(RGBQUAD);
    if (mtIn->cbFormat < sizeof(VIDEOINFOHEADER) + cbPalette)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Everything is good.
    return S_OK;
}
```



<span data-ttu-id="55597-116">在此範例中，方法會先檢查主要類型和子類型。</span><span class="sxs-lookup"><span data-stu-id="55597-116">In this example, the method first checks the major type and subtype.</span></span> <span data-ttu-id="55597-117">然後，它會檢查格式類型，以確保格式區塊是 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構。</span><span class="sxs-lookup"><span data-stu-id="55597-117">Then it checks the format type, to make sure the format block is a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span> <span data-ttu-id="55597-118">篩選也可以支援 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)，但在此情況下，將沒有真正的好處。</span><span class="sxs-lookup"><span data-stu-id="55597-118">The filter could also support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2), but in this case there would be no real benefit.</span></span> <span data-ttu-id="55597-119">**VIDEOINFOHEADER2** 結構新增了交錯和非正方形圖元的支援，這些圖元不太可能與8位的影片相關。</span><span class="sxs-lookup"><span data-stu-id="55597-119">The **VIDEOINFOHEADER2** structure adds support for interlacing and non-square pixels, which are not likely to be relevant in 8-bit video.</span></span>

<span data-ttu-id="55597-120">如果格式類型正確，此範例會檢查 **VIDEOINFOHEADER** 結構的 **biBitCount** 和 **biCompression** 成員，以確認格式為8位未壓縮的 RGB。</span><span class="sxs-lookup"><span data-stu-id="55597-120">If the format type is correct, the example checks the **biBitCount** and **biCompression** members of the **VIDEOINFOHEADER** structure, to verify that the format is 8-bit uncompressed RGB.</span></span> <span data-ttu-id="55597-121">如這個範例所示，您必須強制轉換</span><span class="sxs-lookup"><span data-stu-id="55597-121">As this example shows, you must coerce the</span></span>


```C++
pbFormat
```



<span data-ttu-id="55597-122">以格式類型為基礎的正確結構指標。</span><span class="sxs-lookup"><span data-stu-id="55597-122">pointer to the correct structure, based on the format type.</span></span> <span data-ttu-id="55597-123">在轉換指標之前，請務必先檢查格式類型 GUID (**formattype**) 和格式區塊 (**cbFormat**) 的大小。</span><span class="sxs-lookup"><span data-stu-id="55597-123">Always check the format type GUID (**formattype**) and the size of the format block (**cbFormat**) before casting the pointer.</span></span>

<span data-ttu-id="55597-124">此範例也會確認調色板專案的數目與位深度相容，而且格式區塊夠大，足以容納調色板專案。</span><span class="sxs-lookup"><span data-stu-id="55597-124">The example also verifies that the number of palette entries is compatible with the bit depth and the format block is large enough to hold the palette entries.</span></span> <span data-ttu-id="55597-125">如果上述所有資訊都正確無誤，則方法會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="55597-125">If all of this information is correct, the method returns S\_OK.</span></span>

<span data-ttu-id="55597-126">下一 [步：步驟3b：執行 GetMediaType 方法](step-3b--implement-the-getmediatype-method.md)。</span><span class="sxs-lookup"><span data-stu-id="55597-126">Next: [Step 3B. Implement the GetMediaType Method](step-3b--implement-the-getmediatype-method.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="55597-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="55597-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55597-128">撰寫 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="55597-128">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



