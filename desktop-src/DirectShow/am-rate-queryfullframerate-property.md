---
description: 此屬性會查詢解碼器所支援的最大全畫面播放速率。 這個屬性的資料型別是 AM \_ QueryRate 結構。
ms.assetid: 98808ed4-6d34-437b-9729-9cc805bc81f0
title: 'AM_RATE_QueryFullFrameRate 屬性 (Dvdmedia) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2c99564caa09253198b101a3e2467ec88c7e34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993558"
---
# <a name="am_rate_queryfullframerate-property"></a><span data-ttu-id="f85e2-104">AM \_ RATE \_ QueryFullFrameRate 屬性</span><span class="sxs-lookup"><span data-stu-id="f85e2-104">AM\_RATE\_QueryFullFrameRate Property</span></span>

<span data-ttu-id="f85e2-105">此屬性會查詢解碼器所支援的最大全畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="f85e2-105">This property queries the decoder for the maximum full-frame rate that the decoder supports.</span></span> <span data-ttu-id="f85e2-106">這個屬性的資料型別是 **AM \_ QueryRate** 結構。</span><span class="sxs-lookup"><span data-stu-id="f85e2-106">The data type for this property is an **AM\_QueryRate** structure.</span></span>

<span data-ttu-id="f85e2-107">這個屬性是針對這個屬性集的1.1 版所定義;請參閱 [**AM \_ RATE \_ UseRateVersion**](am-rate-userateversion-property.md)。</span><span class="sxs-lookup"><span data-stu-id="f85e2-107">This property is defined for version 1.1 of this property set; see [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md).</span></span>



|                   |                                       |
|-------------------|---------------------------------------|
| <span data-ttu-id="f85e2-108">屬性集 GUID</span><span class="sxs-lookup"><span data-stu-id="f85e2-108">Property Set GUID</span></span> | <span data-ttu-id="f85e2-109">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="f85e2-109">AM\_KSPROPSETID\_TSRateChange</span></span>         |
| <span data-ttu-id="f85e2-110">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="f85e2-110">Property ID</span></span>       | <span data-ttu-id="f85e2-111">AM \_ RATE \_ QueryFullFrameRate 屬性</span><span class="sxs-lookup"><span data-stu-id="f85e2-111">AM\_RATE\_QueryFullFrameRate Property</span></span> |
| <span data-ttu-id="f85e2-112">資料類型</span><span class="sxs-lookup"><span data-stu-id="f85e2-112">Data Type</span></span>         | [<span data-ttu-id="f85e2-113">**AM \_ QueryRate**</span><span class="sxs-lookup"><span data-stu-id="f85e2-113">**AM\_QueryRate**</span></span>](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_queryrate) |



 

## <a name="remarks"></a><span data-ttu-id="f85e2-114">備註</span><span class="sxs-lookup"><span data-stu-id="f85e2-114">Remarks</span></span>

<span data-ttu-id="f85e2-115">如果播放速率超過解碼器的最大速率，來源篩選會傳送連續樣本的群組（以不連續分隔）。</span><span class="sxs-lookup"><span data-stu-id="f85e2-115">If the playback rate exceeds the decoder's maximum rate, the source filter sends groups of continuous samples separated by discontinuities.</span></span> <span data-ttu-id="f85e2-116">時間戳記會跳到不連續。</span><span class="sxs-lookup"><span data-stu-id="f85e2-116">The time stamps jump across the discontinuities.</span></span> <span data-ttu-id="f85e2-117">即使播放速率是在解碼器的最大速率內，來源篩選也可能這樣做，因為可能會有其他因素，例如磁片 IO，這會限制完整的播放速率。</span><span class="sxs-lookup"><span data-stu-id="f85e2-117">The source filter might do this even if the playback rate is within the decoder's maximum rate, because there may be other factors, such as disk IO, that limit the full playback rate.</span></span>

## <a name="requirements"></a><span data-ttu-id="f85e2-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="f85e2-118">Requirements</span></span>



| <span data-ttu-id="f85e2-119">需求</span><span class="sxs-lookup"><span data-stu-id="f85e2-119">Requirement</span></span> | <span data-ttu-id="f85e2-120">值</span><span class="sxs-lookup"><span data-stu-id="f85e2-120">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f85e2-121">標頭</span><span class="sxs-lookup"><span data-stu-id="f85e2-121">Header</span></span><br/> | <dl> <span data-ttu-id="f85e2-122"><dt>Dvdmedia。h</dt></span><span class="sxs-lookup"><span data-stu-id="f85e2-122"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f85e2-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f85e2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f85e2-124">**速率變更屬性集**</span><span class="sxs-lookup"><span data-stu-id="f85e2-124">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




