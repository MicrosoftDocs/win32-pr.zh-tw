---
description: 在 IMFTransform 上，指定硬體編碼器所支援的最大巨大區塊處理速率（每秒巨大區塊）。
ms.assetid: 1AA41DE3-C37C-41BA-9549-5F12373DDB3B
title: 'MF_VIDEO_MAX_MB_PER_SEC 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbee009b50daee074241c11750e9d25240cda153
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971052"
---
# <a name="mf_video_max_mb_per_sec-attribute"></a><span data-ttu-id="cb362-103">MF \_ VIDEO \_ 最 \_ 大 \_ 每 \_ 秒 MB 數屬性</span><span class="sxs-lookup"><span data-stu-id="cb362-103">MF\_VIDEO\_MAX\_MB\_PER\_SEC attribute</span></span>

<span data-ttu-id="cb362-104">在 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)上，指定硬體編碼器所支援的最大巨大區塊處理速率（每秒巨大區塊）。</span><span class="sxs-lookup"><span data-stu-id="cb362-104">Specifies, on [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform), the maximum macroblock processing rate, in macroblocks per second, that is supported by the hardware encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="cb362-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="cb362-105">Data type</span></span>

<span data-ttu-id="cb362-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="cb362-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="cb362-107">備註</span><span class="sxs-lookup"><span data-stu-id="cb362-107">Remarks</span></span>

<span data-ttu-id="cb362-108">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="cb362-108">This is a read-only attribute.</span></span>

<span data-ttu-id="cb362-109">**H.264/AVC 編碼器：**</span><span class="sxs-lookup"><span data-stu-id="cb362-109">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="cb362-110">這個屬性會受到下列屬性的影響：</span><span class="sxs-lookup"><span data-stu-id="cb362-110">This attribute is affected by the following properties:</span></span>

-   <span data-ttu-id="cb362-111">[MF \_MT \_ 影片 \_ 層級](mf-mt-video-level.md) (是 [MF \_ MT \_ MPEG2 \_ 層級](mf-mt-mpeg2-level-attribute.md) 的別名) </span><span class="sxs-lookup"><span data-stu-id="cb362-111">[MF\_MT\_VIDEO\_LEVEL](mf-mt-video-level.md) (which is an alias of [MF\_MT\_MPEG2\_LEVEL](mf-mt-mpeg2-level-attribute.md))</span></span>
-   [<span data-ttu-id="cb362-112">CODECAPI \_ AVEncCommonQualityVsSpeed</span><span class="sxs-lookup"><span data-stu-id="cb362-112">CODECAPI\_AVEncCommonQualityVsSpeed</span></span>](../directshow/avenccommonqualityvsspeed-property.md)
-   [<span data-ttu-id="cb362-113">CODECAPI \_ AVEncMPVDefaultBPictureCount</span><span class="sxs-lookup"><span data-stu-id="cb362-113">CODECAPI\_AVEncMPVDefaultBPictureCount</span></span>](../directshow/avencmpvdefaultbpicturecount-property.md)

<span data-ttu-id="cb362-114">如果有 [MF \_ MT \_ 影片 \_ 層級](mf-mt-video-level.md) 屬性，編碼器應該會傳回指定層級所支援的最高位元速率和解析度的處理速率。</span><span class="sxs-lookup"><span data-stu-id="cb362-114">If the [MF\_MT\_VIDEO\_LEVEL](mf-mt-video-level.md) attribute is present, the encoder should return the processing rate for the highest bitrate and resolution supported at the specified level.</span></span> <span data-ttu-id="cb362-115">如果 \_ \_ 不存在 MF MT 影片 \_ 層級屬性，則應使用預設層級4。</span><span class="sxs-lookup"><span data-stu-id="cb362-115">If the MF\_MT\_VIDEO\_LEVEL attribute is not present then it should use a default level of 4.</span></span>

<span data-ttu-id="cb362-116">如果已設定 [CODECAPI \_ AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) ICodecAPI 屬性，編碼器應該會傳回與此屬性所設定之值相對應的處理速率。</span><span class="sxs-lookup"><span data-stu-id="cb362-116">If the [CODECAPI\_AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) ICodecAPI property has been set, the encoder should return the processing rate corresponding to the value set for this property.</span></span> <span data-ttu-id="cb362-117">如果 CODECAPI \_ AVEncCommonQualityVsSpeed 屬性不存在，則應該使用預設值0，這應該是最快的處理模式。</span><span class="sxs-lookup"><span data-stu-id="cb362-117">If the CODECAPI\_AVEncCommonQualityVsSpeed attribute is not present, then it should use a default value of 0 which should be the fastest processing mode.</span></span>

<span data-ttu-id="cb362-118">如果 [CODECAPI \_ AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md) ICodecAPI 屬性已設定為有效且支援的值，則編碼器應該會傳回與此屬性所設定之值相對應的處理速率。</span><span class="sxs-lookup"><span data-stu-id="cb362-118">If the [CODECAPI\_AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md) ICodecAPI property has been set to a valid and supported value, the encoder should return the processing rate corresponding the value set for this property.</span></span> <span data-ttu-id="cb362-119">如果 CODECAPI \_ AVEncMPVDefaultBPictureCount 屬性不是 presen，則應該使用預設值 0 B 的框架。</span><span class="sxs-lookup"><span data-stu-id="cb362-119">If the CODECAPI\_AVEncMPVDefaultBPictureCount attribute is not presen,t then it should use a default value of 0 B frames.</span></span>

<span data-ttu-id="cb362-120">應用程式只能使用較低的28位。</span><span class="sxs-lookup"><span data-stu-id="cb362-120">Only the lower 28 bits should be used by an application.</span></span> <span data-ttu-id="cb362-121">較高的4bits 會保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="cb362-121">The upper 4bits are reserved for future use.</span></span> <span data-ttu-id="cb362-122">應用程式應該忽略上面的4位，而且 MFTs 應該將前4位設定為0。</span><span class="sxs-lookup"><span data-stu-id="cb362-122">Applications should ignore the upper 4 bits and MFTs should set the upper 4 bits to 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb362-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb362-123">Requirements</span></span>



| <span data-ttu-id="cb362-124">需求</span><span class="sxs-lookup"><span data-stu-id="cb362-124">Requirement</span></span> | <span data-ttu-id="cb362-125">值</span><span class="sxs-lookup"><span data-stu-id="cb362-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cb362-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb362-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cb362-127">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb362-127">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="cb362-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb362-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cb362-129">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb362-129">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="cb362-130">標頭</span><span class="sxs-lookup"><span data-stu-id="cb362-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb362-131"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="cb362-131"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb362-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb362-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb362-133">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="cb362-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
