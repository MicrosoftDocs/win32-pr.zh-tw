---
description: 定義平移/掃描光圈，也就是要在移動 \# 流覽/掃描模式中顯示的 4&215; 3 區域的影片。
ms.assetid: faa577fd-6572-46b9-9c6c-f91c47832cb5
title: 'MF_MT_PAN_SCAN_APERTURE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a798ba96315126daab94ba92e8791bfeac77db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996616"
---
# <a name="mf_mt_pan_scan_aperture-attribute"></a><span data-ttu-id="45549-103">MF \_ MT \_ 平移 \_ 掃描 \_ 光圈屬性</span><span class="sxs-lookup"><span data-stu-id="45549-103">MF\_MT\_PAN\_SCAN\_APERTURE attribute</span></span>

<span data-ttu-id="45549-104">定義平移/掃描光圈，也就是應該以移動流覽/掃描模式顯示的影片4×3區域。</span><span class="sxs-lookup"><span data-stu-id="45549-104">Defines the pan/scan aperture, which is the 4×3 region of video that should be displayed in pan/scan mode.</span></span>

## <a name="data-type"></a><span data-ttu-id="45549-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="45549-105">Data type</span></span>

<span data-ttu-id="45549-106">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="45549-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="45549-107">備註</span><span class="sxs-lookup"><span data-stu-id="45549-107">Remarks</span></span>

<span data-ttu-id="45549-108">屬性值是 [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) 結構。</span><span class="sxs-lookup"><span data-stu-id="45549-108">The attribute value is an [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) structure.</span></span>

<span data-ttu-id="45549-109">這個屬性是用來將寬螢幕影片裁剪為4:3 的外觀比例。</span><span class="sxs-lookup"><span data-stu-id="45549-109">This attribute is used to crop widescreen video to a 4:3 aspect ratio.</span></span> <span data-ttu-id="45549-110">移動流覽/掃描光圈只適用于移動流覽/掃描模式，其可透過將 [ [**MF \_ MT \_ 掃視 \_ 掃描 \_ 已啟用**](mf-mt-pan-scan-enabled-attribute.md) ] 屬性設定為 [ **TRUE**] 來啟用。</span><span class="sxs-lookup"><span data-stu-id="45549-110">The pan/scan aperture is used only in pan/scan mode, which is enabled by setting the [**MF\_MT\_PAN\_SCAN\_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) attribute to **TRUE**.</span></span>

<span data-ttu-id="45549-111">如果未啟用 [移動流覽]/[掃描] 模式，請使用 [顯示光圈] （由 [ [**MF \_ MT \_ 最小 \_ 顯示 \_ 光圈**](mf-mt-minimum-display-aperture-attribute.md) ] 屬性指定）。</span><span class="sxs-lookup"><span data-stu-id="45549-111">If pan/scan mode is not enabled, use the display aperture, specified by the [**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**](mf-mt-minimum-display-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="45549-112">如果未設定此屬性，則會假設平移/掃描光圈是整個影片畫面。</span><span class="sxs-lookup"><span data-stu-id="45549-112">If this attribute is not set, the pan/scan aperture is assumed to be the entire video frame.</span></span>

<span data-ttu-id="45549-113">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="45549-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="45549-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="45549-114">Requirements</span></span>



| <span data-ttu-id="45549-115">需求</span><span class="sxs-lookup"><span data-stu-id="45549-115">Requirement</span></span> | <span data-ttu-id="45549-116">值</span><span class="sxs-lookup"><span data-stu-id="45549-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="45549-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="45549-117">Minimum supported client</span></span><br/> | <span data-ttu-id="45549-118">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="45549-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="45549-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="45549-119">Minimum supported server</span></span><br/> | <span data-ttu-id="45549-120">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="45549-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="45549-121">標頭</span><span class="sxs-lookup"><span data-stu-id="45549-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="45549-122"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="45549-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45549-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="45549-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45549-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="45549-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="45549-125">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="45549-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="45549-126">圖片外觀比例</span><span class="sxs-lookup"><span data-stu-id="45549-126">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> <dt>

[<span data-ttu-id="45549-127">影片媒體類型</span><span class="sxs-lookup"><span data-stu-id="45549-127">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="45549-128">**IMFAttributes：： GetBlob**</span><span class="sxs-lookup"><span data-stu-id="45549-128">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="45549-129">**IMFAttributes：： SetBlob**</span><span class="sxs-lookup"><span data-stu-id="45549-129">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="45549-130">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="45549-130">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="45549-131">**MF \_ MT \_ 幾何 \_ 光圈**</span><span class="sxs-lookup"><span data-stu-id="45549-131">**MF\_MT\_GEOMETRIC\_APERTURE**</span></span>](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="45549-132">**MF \_ MT \_ 最小 \_ 顯示 \_ 光圈**</span><span class="sxs-lookup"><span data-stu-id="45549-132">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="45549-133">**\_已啟用 MF MT \_ PAN \_ 掃描 \_**</span><span class="sxs-lookup"><span data-stu-id="45549-133">**MF\_MT\_PAN\_SCAN\_ENABLED**</span></span>](mf-mt-pan-scan-enabled-attribute.md)
</dt> </dl>

 

 




