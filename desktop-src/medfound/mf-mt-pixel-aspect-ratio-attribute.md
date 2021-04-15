---
description: 影片媒體類型的圖元外觀比例。
ms.assetid: e82cdd22-7d3f-4858-befd-43fa6f9f915e
title: 'MF_MT_PIXEL_ASPECT_RATIO 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50c0d28ea11ba664208fcfe5fc356f1f57f2878e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511728"
---
# <a name="mf_mt_pixel_aspect_ratio-attribute"></a><span data-ttu-id="31841-103">MF \_ MT \_ 圖元 \_ 外觀 \_ 比例屬性</span><span class="sxs-lookup"><span data-stu-id="31841-103">MF\_MT\_PIXEL\_ASPECT\_RATIO attribute</span></span>

<span data-ttu-id="31841-104">影片媒體類型的圖元外觀比例。</span><span class="sxs-lookup"><span data-stu-id="31841-104">Pixel aspect ratio for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="31841-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="31841-105">Data type</span></span>

<span data-ttu-id="31841-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="31841-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="31841-107">備註</span><span class="sxs-lookup"><span data-stu-id="31841-107">Remarks</span></span>

<span data-ttu-id="31841-108">上方的32位包含圖元外觀比例的分子，而較低的32位則包含分母。</span><span class="sxs-lookup"><span data-stu-id="31841-108">The upper 32 bits contain the numerator of the pixel aspect ratio and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="31841-109">分子是外觀比例的水準元件;分母是垂直的元件。</span><span class="sxs-lookup"><span data-stu-id="31841-109">The numerator is the horizontal component of the aspect ratio; the denominator is the vertical component.</span></span>

<span data-ttu-id="31841-110">若要設定此屬性，請使用 [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) 函數。</span><span class="sxs-lookup"><span data-stu-id="31841-110">To set this attribute, use the [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) function.</span></span> <span data-ttu-id="31841-111">若要取得這個屬性，請使用 [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) 函數。</span><span class="sxs-lookup"><span data-stu-id="31841-111">To get this attribute, use the [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) function.</span></span>

<span data-ttu-id="31841-112">圖元外觀比例描述顯示的影片影像中圖元的形狀。</span><span class="sxs-lookup"><span data-stu-id="31841-112">The pixel aspect ratio describes the shape of the pixels in the displayed video image.</span></span> <span data-ttu-id="31841-113">如果影像具有非正方形圖元，請設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="31841-113">Set this attribute if the image has non-square pixels.</span></span> <span data-ttu-id="31841-114">若要在具有正方形圖元的顯示裝置上正確顯示，影像必須以影像的圖元外觀比例反轉。</span><span class="sxs-lookup"><span data-stu-id="31841-114">To display correctly on a display device with square pixels, the image must be scaled by the inverse of the image's pixel aspect ratio.</span></span>

<span data-ttu-id="31841-115">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="31841-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="31841-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="31841-116">Requirements</span></span>



| <span data-ttu-id="31841-117">需求</span><span class="sxs-lookup"><span data-stu-id="31841-117">Requirement</span></span> | <span data-ttu-id="31841-118">值</span><span class="sxs-lookup"><span data-stu-id="31841-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="31841-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31841-119">Minimum supported client</span></span><br/> | <span data-ttu-id="31841-120">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31841-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="31841-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31841-121">Minimum supported server</span></span><br/> | <span data-ttu-id="31841-122">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31841-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="31841-123">標頭</span><span class="sxs-lookup"><span data-stu-id="31841-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="31841-124"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="31841-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31841-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31841-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31841-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="31841-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="31841-127">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="31841-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="31841-128">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="31841-128">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="31841-129">圖片外觀比例</span><span class="sxs-lookup"><span data-stu-id="31841-129">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> </dl>

 

 




