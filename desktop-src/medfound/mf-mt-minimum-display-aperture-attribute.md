---
description: 定義顯示光圈，也就是包含有效影像資料的影片框架區域。
ms.assetid: 86a7509b-c690-49c2-bbe4-8b02d64c307c
title: 'MF_MT_MINIMUM_DISPLAY_APERTURE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d13252378422081044d7f2cb21e5a31098702a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972872"
---
# <a name="mf_mt_minimum_display_aperture-attribute"></a><span data-ttu-id="ecbd3-103">MF \_ MT \_ 最小 \_ 顯示 \_ 光圈屬性</span><span class="sxs-lookup"><span data-stu-id="ecbd3-103">MF\_MT\_MINIMUM\_DISPLAY\_APERTURE attribute</span></span>

<span data-ttu-id="ecbd3-104">定義顯示光圈，也就是包含有效影像資料的影片框架區域。</span><span class="sxs-lookup"><span data-stu-id="ecbd3-104">Defines the display aperture, which is the region of a video frame that contains valid image data.</span></span>

## <a name="data-type"></a><span data-ttu-id="ecbd3-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="ecbd3-105">Data type</span></span>

<span data-ttu-id="ecbd3-106">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="ecbd3-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="ecbd3-107">備註</span><span class="sxs-lookup"><span data-stu-id="ecbd3-107">Remarks</span></span>

<span data-ttu-id="ecbd3-108">屬性值是 [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) 結構。</span><span class="sxs-lookup"><span data-stu-id="ecbd3-108">The attribute value is an [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) structure.</span></span>

<span data-ttu-id="ecbd3-109">最小顯示光圈是包含信號有效部分的區域。</span><span class="sxs-lookup"><span data-stu-id="ecbd3-109">The minimum display aperture is the region that contains the valid portion of the signal.</span></span> <span data-ttu-id="ecbd3-110">光圈外面的圖元包含不正確資料，不應該顯示。</span><span class="sxs-lookup"><span data-stu-id="ecbd3-110">The pixels outside the aperture contain invalid data and should not be displayed.</span></span>

<span data-ttu-id="ecbd3-111">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="ecbd3-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecbd3-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="ecbd3-112">Requirements</span></span>



| <span data-ttu-id="ecbd3-113">需求</span><span class="sxs-lookup"><span data-stu-id="ecbd3-113">Requirement</span></span> | <span data-ttu-id="ecbd3-114">值</span><span class="sxs-lookup"><span data-stu-id="ecbd3-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ecbd3-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ecbd3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ecbd3-116">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ecbd3-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="ecbd3-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ecbd3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ecbd3-118">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ecbd3-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="ecbd3-119">標頭</span><span class="sxs-lookup"><span data-stu-id="ecbd3-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecbd3-120"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="ecbd3-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecbd3-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ecbd3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecbd3-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="ecbd3-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ecbd3-123">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="ecbd3-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="ecbd3-124">圖片外觀比例</span><span class="sxs-lookup"><span data-stu-id="ecbd3-124">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> <dt>

[<span data-ttu-id="ecbd3-125">影片媒體類型</span><span class="sxs-lookup"><span data-stu-id="ecbd3-125">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="ecbd3-126">**IMFAttributes：： GetBlob**</span><span class="sxs-lookup"><span data-stu-id="ecbd3-126">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="ecbd3-127">**IMFAttributes：： SetBlob**</span><span class="sxs-lookup"><span data-stu-id="ecbd3-127">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="ecbd3-128">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="ecbd3-128">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="ecbd3-129">**MF \_ MT \_ 幾何 \_ 光圈**</span><span class="sxs-lookup"><span data-stu-id="ecbd3-129">**MF\_MT\_GEOMETRIC\_APERTURE**</span></span>](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="ecbd3-130">**MF \_ MT \_ 平移 \_ 掃描 \_ 光圈**</span><span class="sxs-lookup"><span data-stu-id="ecbd3-130">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




