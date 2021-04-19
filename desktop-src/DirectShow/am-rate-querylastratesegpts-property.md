---
description: 此屬性會查詢在最近排入佇列之速率變更開始時間的解碼器，不論其在速率變更佇列中的位置為何。
ms.assetid: 3c7006e7-48fd-4df8-b446-8ee2b024278b
title: 'AM_RATE_QueryLastRateSegPTS 屬性 (Dvdmedia) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 024ac26d8307dc9b8ff8e16603dfcc61b0704390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993205"
---
# <a name="am_rate_querylastratesegpts-property"></a><span data-ttu-id="90508-103">AM \_ RATE \_ QueryLastRateSegPTS 屬性</span><span class="sxs-lookup"><span data-stu-id="90508-103">AM\_RATE\_QueryLastRateSegPTS Property</span></span>

<span data-ttu-id="90508-104">此屬性會查詢在最近排入佇列之速率變更開始時間的解碼器，不論其在速率變更佇列中的位置為何。</span><span class="sxs-lookup"><span data-stu-id="90508-104">This property queries the decoder for the start time of the rate change that was queued most recently, regardless of its position in the rate-change queue.</span></span>

<span data-ttu-id="90508-105">這個屬性是針對這個屬性集的1.1 版所定義;請參閱 [**AM \_ RATE \_ UseRateVersion**](am-rate-userateversion-property.md)。</span><span class="sxs-lookup"><span data-stu-id="90508-105">This property is defined for version 1.1 of this property set; see [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md).</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="90508-106">屬性集 GUID</span><span class="sxs-lookup"><span data-stu-id="90508-106">Property Set GUID</span></span> | <span data-ttu-id="90508-107">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="90508-107">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="90508-108">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="90508-108">Property ID</span></span>       | <span data-ttu-id="90508-109">AM \_ RATE \_ QueryLastRateSegPTS</span><span class="sxs-lookup"><span data-stu-id="90508-109">AM\_RATE\_QueryLastRateSegPTS</span></span> |
| <span data-ttu-id="90508-110">資料類型</span><span class="sxs-lookup"><span data-stu-id="90508-110">Data Type</span></span>         | <span data-ttu-id="90508-111">**參考 \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="90508-111">**REFERENCE\_TIME**</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="90508-112">備註</span><span class="sxs-lookup"><span data-stu-id="90508-112">Remarks</span></span>

<span data-ttu-id="90508-113">來源篩選器可以使用此屬性來同步處理數個音訊和影片串流之間的速率變更。</span><span class="sxs-lookup"><span data-stu-id="90508-113">The source filter can use this property to synchronize rate changes across several audio and video streams.</span></span>

## <a name="requirements"></a><span data-ttu-id="90508-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="90508-114">Requirements</span></span>



| <span data-ttu-id="90508-115">需求</span><span class="sxs-lookup"><span data-stu-id="90508-115">Requirement</span></span> | <span data-ttu-id="90508-116">值</span><span class="sxs-lookup"><span data-stu-id="90508-116">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90508-117">標頭</span><span class="sxs-lookup"><span data-stu-id="90508-117">Header</span></span><br/> | <dl> <span data-ttu-id="90508-118"><dt>Dvdmedia。h</dt></span><span class="sxs-lookup"><span data-stu-id="90508-118"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90508-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90508-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90508-120">**速率變更屬性集**</span><span class="sxs-lookup"><span data-stu-id="90508-120">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




