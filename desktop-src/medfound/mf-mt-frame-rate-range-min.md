---
description: 影片捕獲裝置所支援的最小畫面播放速率（以每秒畫面格數為單位）。
ms.assetid: d3725796-f683-4ca1-a37f-22c40fff0b76
title: 'MF_MT_FRAME_RATE_RANGE_MIN 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9692927242eea7ec65b86572db455e610e30c711
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851431"
---
# <a name="mf_mt_frame_rate_range_min-attribute"></a><span data-ttu-id="644f4-103">MF \_ MT \_ 幀 \_ 速率 \_ 範圍 \_ 最小值屬性</span><span class="sxs-lookup"><span data-stu-id="644f4-103">MF\_MT\_FRAME\_RATE\_RANGE\_MIN attribute</span></span>

<span data-ttu-id="644f4-104">影片捕獲裝置所支援的最小畫面播放速率（以每秒畫面格數為單位）。</span><span class="sxs-lookup"><span data-stu-id="644f4-104">The minimum frame rate that is supported by a video capture device, in frames per second.</span></span>

## <a name="data-type"></a><span data-ttu-id="644f4-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="644f4-105">Data type</span></span>

<span data-ttu-id="644f4-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="644f4-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="644f4-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="644f4-107">Get/set</span></span>

<span data-ttu-id="644f4-108">若要取得這個屬性，請呼叫 [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio)。</span><span class="sxs-lookup"><span data-stu-id="644f4-108">To get this attribute, call [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span></span>

<span data-ttu-id="644f4-109">若要設定這個屬性，請呼叫 [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio)。</span><span class="sxs-lookup"><span data-stu-id="644f4-109">To set this attribute, call [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span></span>

## <a name="remarks"></a><span data-ttu-id="644f4-110">備註</span><span class="sxs-lookup"><span data-stu-id="644f4-110">Remarks</span></span>

<span data-ttu-id="644f4-111">畫面播放速率以比例表示。</span><span class="sxs-lookup"><span data-stu-id="644f4-111">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="644f4-112">屬性值的上方32位包含分子，而較低的32位則包含分母。</span><span class="sxs-lookup"><span data-stu-id="644f4-112">The upper 32 bits of the attribute value contain the numerator, and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="644f4-113">例如，如果畫面播放速率是每秒30個畫面格 (fps) ，則比率為30/1。</span><span class="sxs-lookup"><span data-stu-id="644f4-113">For example, if the frame rate is 30 frames per second (fps), the ratio is 30/1.</span></span>

<span data-ttu-id="644f4-114">如果捕捉裝置報告的畫面播放速率下限，媒體來源會在媒體類型上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="644f4-114">If the capture device reports a minimum frame rate, the media source sets this attribute on the media type.</span></span> <span data-ttu-id="644f4-115">[ [MF \_ MT \_ 幀 \_ 速率 \_ 範圍 \_ 最大值](mf-mt-frame-rate-range-max.md) ] 屬性提供最大畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="644f4-115">The maximum frame rate is given in the [MF\_MT\_FRAME\_RATE\_RANGE\_MAX](mf-mt-frame-rate-range-max.md) attribute.</span></span> <span data-ttu-id="644f4-116">裝置不保證可支援此範圍內的每個增量。</span><span class="sxs-lookup"><span data-stu-id="644f4-116">The device is not guaranteed to support every increment within this range.</span></span>

<span data-ttu-id="644f4-117">若要設定裝置的畫面播放速率，請先在媒體類型上修改 [ [**MF \_ MT \_ 幀 \_ 速率**](mf-mt-frame-rate-attribute.md) ] 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="644f4-117">To set the device's frame rate, first modify the value of the [**MF\_MT\_FRAME\_RATE**](mf-mt-frame-rate-attribute.md) attribute on the media type.</span></span> <span data-ttu-id="644f4-118">然後設定媒體來源上的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="644f4-118">Then set the media type on the media source.</span></span>

<span data-ttu-id="644f4-119">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="644f4-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="644f4-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="644f4-120">Requirements</span></span>



| <span data-ttu-id="644f4-121">需求</span><span class="sxs-lookup"><span data-stu-id="644f4-121">Requirement</span></span> | <span data-ttu-id="644f4-122">值</span><span class="sxs-lookup"><span data-stu-id="644f4-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="644f4-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="644f4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="644f4-124">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="644f4-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="644f4-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="644f4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="644f4-126">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="644f4-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="644f4-127">標頭</span><span class="sxs-lookup"><span data-stu-id="644f4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="644f4-128"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="644f4-128"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="644f4-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="644f4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="644f4-130">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="644f4-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="644f4-131">如何設定影片捕獲畫面播放速率</span><span class="sxs-lookup"><span data-stu-id="644f4-131">How to Set the Video Capture Frame Rate</span></span>](how-to-set-the-video-capture-frame-rate.md)
</dt> <dt>

[<span data-ttu-id="644f4-132">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="644f4-132">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="644f4-133">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="644f4-133">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="644f4-134">MF \_ MT \_ 幀 \_ 速率 \_ 範圍 \_ 最大值</span><span class="sxs-lookup"><span data-stu-id="644f4-134">MF\_MT\_FRAME\_RATE\_RANGE\_MAX</span></span>](mf-mt-frame-rate-range-max.md)
</dt> </dl>

 

 




