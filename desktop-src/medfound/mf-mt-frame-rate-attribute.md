---
description: 影片媒體類型的畫面播放速率（以每秒畫面格數為單位）。
ms.assetid: 8336559c-06f1-478e-b921-e9eae7425230
title: 'MF_MT_FRAME_RATE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8df2ef4268bd643d9f65eb16c3f7257bcaceb1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104386256"
---
# <a name="mf_mt_frame_rate-attribute"></a><span data-ttu-id="1fef4-103">MF \_ MT \_ 幀 \_ 速率屬性</span><span class="sxs-lookup"><span data-stu-id="1fef4-103">MF\_MT\_FRAME\_RATE attribute</span></span>

<span data-ttu-id="1fef4-104">影片媒體類型的畫面播放速率（以每秒畫面格數為單位）。</span><span class="sxs-lookup"><span data-stu-id="1fef4-104">Frame rate of a video media type, in frames per second.</span></span>

## <a name="data-type"></a><span data-ttu-id="1fef4-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="1fef4-105">Data type</span></span>

<span data-ttu-id="1fef4-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="1fef4-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="1fef4-107">備註</span><span class="sxs-lookup"><span data-stu-id="1fef4-107">Remarks</span></span>

<span data-ttu-id="1fef4-108">畫面播放速率以比例表示。</span><span class="sxs-lookup"><span data-stu-id="1fef4-108">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="1fef4-109">屬性值的上方32位包含分子，而較低的32位則包含分母。</span><span class="sxs-lookup"><span data-stu-id="1fef4-109">The upper 32 bits of the attribute value contain the numerator and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="1fef4-110">例如，如果畫面播放速率是每秒30個畫面格 (fps) ，則比率為30/1。</span><span class="sxs-lookup"><span data-stu-id="1fef4-110">For example, if the frame rate is 30 frames per second (fps), the ratio is 30/1.</span></span> <span data-ttu-id="1fef4-111">如果畫面播放速率是 29.97 fps，則比率為 30000/1001。</span><span class="sxs-lookup"><span data-stu-id="1fef4-111">If the frame rate is 29.97 fps, the ratio is 30,000/1001.</span></span>

<span data-ttu-id="1fef4-112">若要設定此值，請使用 [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) 函數。</span><span class="sxs-lookup"><span data-stu-id="1fef4-112">To set the value, use the [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) function.</span></span> <span data-ttu-id="1fef4-113">若要取得此值，請使用 [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) 函數。</span><span class="sxs-lookup"><span data-stu-id="1fef4-113">To get the value, use the [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) function.</span></span>

<span data-ttu-id="1fef4-114">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="1fef4-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="1fef4-115">範例</span><span class="sxs-lookup"><span data-stu-id="1fef4-115">Examples</span></span>

<span data-ttu-id="1fef4-116">下列範例會設定影片媒體類型的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="1fef4-116">The following example sets the frame rate on a video media type.</span></span>


```
// Helper function to set the frame rate on a video media type.
inline HRESULT SetFrameRate(
    IMFMediaType *pType, 
    UINT32 numerator, 
    UINT32 denominator
    )
{
    return MFSetAttributeRatio(
        pType, 
        MF_MT_FRAME_RATE, 
        numerator, 
        denominator
        );
}
```



<span data-ttu-id="1fef4-117">下列範例會從影片媒體類型取得畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="1fef4-117">The following example gets the frame rate from a video media type.</span></span>


```
// Helper function to get the frame rate from a video media type.
inline HRESULT GetFrameRate(
    IMFMediaType *pType, 
    UINT32 *pNumerator, 
    UINT32 *pDenominator
    )
{
    return MFGetAttributeRatio(
        pType, 
        MF_MT_FRAME_RATE, 
        pNumerator, 
        pDenominator
        );
}
```



## <a name="requirements"></a><span data-ttu-id="1fef4-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="1fef4-118">Requirements</span></span>



| <span data-ttu-id="1fef4-119">需求</span><span class="sxs-lookup"><span data-stu-id="1fef4-119">Requirement</span></span> | <span data-ttu-id="1fef4-120">值</span><span class="sxs-lookup"><span data-stu-id="1fef4-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1fef4-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1fef4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1fef4-122">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1fef4-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="1fef4-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1fef4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1fef4-124">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1fef4-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="1fef4-125">標頭</span><span class="sxs-lookup"><span data-stu-id="1fef4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fef4-126"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="1fef4-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fef4-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1fef4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fef4-128">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="1fef4-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1fef4-129">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="1fef4-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="1fef4-130">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="1fef4-130">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="1fef4-131">**MFAverageTimePerFrameToFrameRate**</span><span class="sxs-lookup"><span data-stu-id="1fef4-131">**MFAverageTimePerFrameToFrameRate**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate)
</dt> <dt>

[<span data-ttu-id="1fef4-132">**MFFrameRateToAverageTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="1fef4-132">**MFFrameRateToAverageTimePerFrame**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe)
</dt> </dl>

 

 




