---
description: 定義影片媒體類型的幾何光圈。
ms.assetid: a2489ba1-f322-4b63-a479-0d9879c30a8c
title: 'MF_MT_GEOMETRIC_APERTURE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e194408dd8b6bf4a4dac717c7d41aaecbb06f306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943782"
---
# <a name="mf_mt_geometric_aperture-attribute"></a><span data-ttu-id="5e572-103">MF \_ MT \_ 幾何 \_ 光圈屬性</span><span class="sxs-lookup"><span data-stu-id="5e572-103">MF\_MT\_GEOMETRIC\_APERTURE attribute</span></span>

<span data-ttu-id="5e572-104">定義影片媒體類型的幾何光圈。</span><span class="sxs-lookup"><span data-stu-id="5e572-104">Defines the geometric aperture for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="5e572-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="5e572-105">Data type</span></span>

<span data-ttu-id="5e572-106">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="5e572-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="5e572-107">備註</span><span class="sxs-lookup"><span data-stu-id="5e572-107">Remarks</span></span>

<span data-ttu-id="5e572-108">這個屬性的值是 [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) 結構。</span><span class="sxs-lookup"><span data-stu-id="5e572-108">The value of this attribute is an [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) structure.</span></span>

<span data-ttu-id="5e572-109">圖片外觀比例的計算相對於幾何光圈，使用下列公式：圖片外觀比例 = (幾何光圈寬度/幾何光圈高度) ×圖元外觀比例。</span><span class="sxs-lookup"><span data-stu-id="5e572-109">The picture aspect ratio is calculated relative to the geometric aperture, using the following formula: Picture aspect ratio = (geometric aperture width / geometric aperture height) × pixel aspect ratio.</span></span>

<span data-ttu-id="5e572-110">如果未設定此屬性，則會假設幾何光圈是整個影片畫面。</span><span class="sxs-lookup"><span data-stu-id="5e572-110">If this attribute is not set, the geometric aperture is assumed to be the entire video frame.</span></span> <span data-ttu-id="5e572-111">只有當媒體類型描述具有定義之作用中區域的影片標準時，才應該設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="5e572-111">You should set this attribute only when the media type describes a video standard with a defined active area.</span></span>

<span data-ttu-id="5e572-112">例如，在 NTSC 電視中，影片畫面是720×480，其使用區域為704×480和10:11 圖元外觀比例。</span><span class="sxs-lookup"><span data-stu-id="5e572-112">For example, in NTSC television the video frame is 720 × 480 with an active area of 704 × 480 and a 10:11 pixel aspect ratio.</span></span> <span data-ttu-id="5e572-113">產生的圖片具有 (704/480) × (10/11) = 4:3 的外觀比例。</span><span class="sxs-lookup"><span data-stu-id="5e572-113">The resulting picture has an aspect ratio of (704/480) × (10/11) = 4:3.</span></span>

> [!Note]  
> <span data-ttu-id="5e572-114">[增強型影片](enhanced-video-renderer.md)轉譯器的預設展示器 (EVR) 顯示影片的幾何光圈（如有指定）。</span><span class="sxs-lookup"><span data-stu-id="5e572-114">The default presenter for the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) shows the geometric aperture of the video, if specified.</span></span>

 

<span data-ttu-id="5e572-115">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="5e572-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="5e572-116">範例</span><span class="sxs-lookup"><span data-stu-id="5e572-116">Examples</span></span>


```
HRESULT SetGeometricAperture(
    IMFMediaType *pMediaType, 
    const MFVideoArea& area
    )
{
    return pMediaType->SetBlob(
        MF_MT_GEOMETRIC_APERTURE, 
        (UINT8*)&area, 
        sizeof(MFVideoArea)
        );
}
```



## <a name="requirements"></a><span data-ttu-id="5e572-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e572-117">Requirements</span></span>



| <span data-ttu-id="5e572-118">需求</span><span class="sxs-lookup"><span data-stu-id="5e572-118">Requirement</span></span> | <span data-ttu-id="5e572-119">值</span><span class="sxs-lookup"><span data-stu-id="5e572-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5e572-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5e572-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5e572-121">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e572-121">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="5e572-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5e572-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5e572-123">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e572-123">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="5e572-124">標頭</span><span class="sxs-lookup"><span data-stu-id="5e572-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e572-125"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="5e572-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e572-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5e572-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e572-127">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="5e572-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5e572-128">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="5e572-128">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5e572-129">圖片外觀比例</span><span class="sxs-lookup"><span data-stu-id="5e572-129">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> <dt>

[<span data-ttu-id="5e572-130">影片媒體類型</span><span class="sxs-lookup"><span data-stu-id="5e572-130">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="5e572-131">**IMFAttributes：： GetBlob**</span><span class="sxs-lookup"><span data-stu-id="5e572-131">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="5e572-132">**IMFAttributes：： SetBlob**</span><span class="sxs-lookup"><span data-stu-id="5e572-132">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="5e572-133">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="5e572-133">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="5e572-134">**MF \_ MT \_ 最小 \_ 顯示 \_ 光圈**</span><span class="sxs-lookup"><span data-stu-id="5e572-134">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="5e572-135">**MF \_ MT \_ 平移 \_ 掃描 \_ 光圈**</span><span class="sxs-lookup"><span data-stu-id="5e572-135">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




