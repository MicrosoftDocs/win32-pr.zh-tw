---
description: 指定是否啟用 pan/掃描模式。
ms.assetid: 9e8746c6-13a4-4cf7-9748-82223d9529fa
title: 'MF_MT_PAN_SCAN_ENABLED 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b347c898ce827ff37796a9698e843f6321db8a1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513164"
---
# <a name="mf_mt_pan_scan_enabled-attribute"></a><span data-ttu-id="73324-103">\_ \_ 已啟用 MF MT PAN \_ 掃描的 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="73324-103">MF\_MT\_PAN\_SCAN\_ENABLED attribute</span></span>

<span data-ttu-id="73324-104">指定是否啟用 pan/掃描模式。</span><span class="sxs-lookup"><span data-stu-id="73324-104">Specifies whether pan/scan mode is enabled.</span></span>

## <a name="data-type"></a><span data-ttu-id="73324-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="73324-105">Data type</span></span>

<span data-ttu-id="73324-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="73324-106">**UINT32**</span></span>

<span data-ttu-id="73324-107">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="73324-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="73324-108">備註</span><span class="sxs-lookup"><span data-stu-id="73324-108">Remarks</span></span>

<span data-ttu-id="73324-109">如果此屬性為 **TRUE**，則只會顯示影片的移動流覽/掃描區域。</span><span class="sxs-lookup"><span data-stu-id="73324-109">If this attribute is **TRUE**, only the pan/scan region of the video should be displayed.</span></span> <span data-ttu-id="73324-110">「移動流覽/掃描」區域是由 [**MF \_ MT \_ pan \_ 掃描 \_ 光圈**](mf-mt-pan-scan-aperture-attribute.md) 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="73324-110">The pan/scan region is specified by the [**MF\_MT\_PAN\_SCAN\_APERTURE**](mf-mt-pan-scan-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="73324-111">如果這個屬性為 **FALSE** 或未設定，則會顯示影片的整個顯示光圈。</span><span class="sxs-lookup"><span data-stu-id="73324-111">If this attribute is **FALSE** or not set, the entire display aperture of the video should be displayed.</span></span> <span data-ttu-id="73324-112">顯示光圈是由 [**MF \_ MT \_ 最小 \_ 顯示 \_ 光圈**](mf-mt-minimum-display-aperture-attribute.md) 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="73324-112">The display aperture is specified by the [**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**](mf-mt-minimum-display-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="73324-113">如果您將此屬性設定為 **TRUE**，也請設定 [ [**MF MT 移動 \_ \_ \_ 流覽 \_**](mf-mt-pan-scan-aperture-attribute.md) ] 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="73324-113">If you set this attribute to **TRUE**, also set the value of the [**MF\_MT\_PAN\_SCAN\_APERTURE**](mf-mt-pan-scan-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="73324-114">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="73324-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="73324-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="73324-115">Requirements</span></span>



| <span data-ttu-id="73324-116">需求</span><span class="sxs-lookup"><span data-stu-id="73324-116">Requirement</span></span> | <span data-ttu-id="73324-117">值</span><span class="sxs-lookup"><span data-stu-id="73324-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="73324-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73324-118">Minimum supported client</span></span><br/> | <span data-ttu-id="73324-119">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73324-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="73324-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73324-120">Minimum supported server</span></span><br/> | <span data-ttu-id="73324-121">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73324-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="73324-122">標頭</span><span class="sxs-lookup"><span data-stu-id="73324-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="73324-123"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="73324-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73324-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73324-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73324-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="73324-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="73324-126">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="73324-126">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="73324-127">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="73324-127">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="73324-128">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="73324-128">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="73324-129">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="73324-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="73324-130">圖片外觀比例</span><span class="sxs-lookup"><span data-stu-id="73324-130">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> </dl>

 

 




