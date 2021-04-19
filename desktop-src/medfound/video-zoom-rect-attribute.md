---
description: 指定增強型影片轉譯器 (EVR) 的影片混音器來源矩形。 來源矩形是混音器 blits 至目的地介面之影片框架的一部分。
ms.assetid: 4364ff87-816e-4b64-b5e9-c53dd6c9bb33
title: 'VIDEO_ZOOM_RECT 屬性 (Evr) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dda4efca5beab844baf3b3f53074d6b3012e8621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969241"
---
# <a name="video_zoom_rect-attribute"></a><span data-ttu-id="3dd65-104">影片 \_ 縮放 \_ 矩形屬性</span><span class="sxs-lookup"><span data-stu-id="3dd65-104">VIDEO\_ZOOM\_RECT attribute</span></span>

<span data-ttu-id="3dd65-105">指定 [增強型影片](enhanced-video-renderer.md) 轉譯器 (EVR) 的影片混音器來源矩形。</span><span class="sxs-lookup"><span data-stu-id="3dd65-105">Specifies the source rectangle for video mixer of the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="3dd65-106">來源矩形是混音器 blits 至目的地介面之影片框架的一部分。</span><span class="sxs-lookup"><span data-stu-id="3dd65-106">The source rectangle is the portion of the video frame that the mixer blits to the destination surface.</span></span>

## <a name="data-type"></a><span data-ttu-id="3dd65-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="3dd65-107">Data type</span></span>

<span data-ttu-id="3dd65-108">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="3dd65-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="3dd65-109">備註</span><span class="sxs-lookup"><span data-stu-id="3dd65-109">Remarks</span></span>

<span data-ttu-id="3dd65-110">這個屬性的值是 [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) 結構。</span><span class="sxs-lookup"><span data-stu-id="3dd65-110">The value of this attribute is an [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) structure.</span></span>

<span data-ttu-id="3dd65-111">來源矩形的定義是相對於正規化座標系統，其中的整個影片畫面格都會佔用座標 {0，0，1，1} 的矩形。</span><span class="sxs-lookup"><span data-stu-id="3dd65-111">The source rectangle is defined relative to a normalized coordinate system, in which the entire video frame occupies a rectangle with coordinates {0, 0, 1, 1}.</span></span> <span data-ttu-id="3dd65-112">來源矩形必須放在影片框架內;來源矩形的座標範圍 (0 ... 1) 。</span><span class="sxs-lookup"><span data-stu-id="3dd65-112">The source rectangle must fit within the video frame; the coordinates of the source rectangle have a range of (0...1).</span></span>

<span data-ttu-id="3dd65-113">標準 EVR 展示者會在混音器上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="3dd65-113">The standard EVR presenter sets this attribute on the mixer.</span></span> <span data-ttu-id="3dd65-114">若要設定屬性，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="3dd65-114">To set the attribute, do the following:</span></span>

1.  <span data-ttu-id="3dd65-115">在混音器上呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) ，以取得混音器的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="3dd65-115">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the mixer, to get the mixer's attribute store.</span></span>
2.  <span data-ttu-id="3dd65-116">呼叫 [**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob) ，以在混音器上設定 **影片 \_ 縮放 \_ RECT** 屬性。</span><span class="sxs-lookup"><span data-stu-id="3dd65-116">Call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob) to set the **VIDEO\_ZOOM\_RECT** attribute on the mixer.</span></span> <span data-ttu-id="3dd65-117">此值為 [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) 結構。</span><span class="sxs-lookup"><span data-stu-id="3dd65-117">The value is an [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) structure.</span></span>

<span data-ttu-id="3dd65-118">在自訂 EVR 展示者中，您可以使用這個屬性來執行 [**IMFVideoDisplayControl：： SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) 方法。</span><span class="sxs-lookup"><span data-stu-id="3dd65-118">In a custom EVR presenter, you can use this attribute to implement the [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) method.</span></span> <span data-ttu-id="3dd65-119">如需詳細資訊，請參閱 [來源和目的地矩形](how-to-write-an-evr-presenter.md)。</span><span class="sxs-lookup"><span data-stu-id="3dd65-119">For more information, see [Source and Destination Rectangles](how-to-write-an-evr-presenter.md).</span></span>

<span data-ttu-id="3dd65-120">這個屬性的 GUID 常數是從 strmiids 匯出。</span><span class="sxs-lookup"><span data-stu-id="3dd65-120">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="3dd65-121">範例</span><span class="sxs-lookup"><span data-stu-id="3dd65-121">Examples</span></span>

<span data-ttu-id="3dd65-122">下列範例會設定混音器上的來源矩形。</span><span class="sxs-lookup"><span data-stu-id="3dd65-122">The following example sets the source rectangle on the mixer.</span></span>


```C++
HRESULT SetMixerSourceRect(IMFTransform *pMixer, const MFVideoNormalizedRect& nrcSource)
{
    if (pMixer == NULL)
    {
        return E_POINTER;
    }

    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMixer->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetBlob(VIDEO_ZOOM_RECT, (const UINT8*)&nrcSource, sizeof(nrcSource));
        pAttributes->Release();
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="3dd65-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="3dd65-123">Requirements</span></span>



| <span data-ttu-id="3dd65-124">需求</span><span class="sxs-lookup"><span data-stu-id="3dd65-124">Requirement</span></span> | <span data-ttu-id="3dd65-125">值</span><span class="sxs-lookup"><span data-stu-id="3dd65-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3dd65-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3dd65-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3dd65-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3dd65-127">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3dd65-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3dd65-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3dd65-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3dd65-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3dd65-130">標頭</span><span class="sxs-lookup"><span data-stu-id="3dd65-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dd65-131"><dt>Evr。h</dt></span><span class="sxs-lookup"><span data-stu-id="3dd65-131"><dt>Evr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dd65-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3dd65-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dd65-133">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="3dd65-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3dd65-134">增強的影片轉譯器屬性</span><span class="sxs-lookup"><span data-stu-id="3dd65-134">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="3dd65-135">如何撰寫 EVR 展示者</span><span class="sxs-lookup"><span data-stu-id="3dd65-135">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> <dt>

[<span data-ttu-id="3dd65-136">**IMFAttributes：： GetBlob**</span><span class="sxs-lookup"><span data-stu-id="3dd65-136">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="3dd65-137">**IMFAttributes：： SetBlob**</span><span class="sxs-lookup"><span data-stu-id="3dd65-137">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> </dl>

 

 




