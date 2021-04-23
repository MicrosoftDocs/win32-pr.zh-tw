---
description: DVD 導覽器會使用此屬性來通知解碼器，導覽器會在其傳遞給解碼器的範例上設定正確的時間戳記。
ms.assetid: f04e8291-734f-483e-b756-5362beb68d9c
title: 'AM_RATE_CorrectTS 屬性 (Dvdmedia) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c65b613f892708dc210af2ca2a05efb74785fb
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910296"
---
# <a name="am_rate_correctts-property"></a><span data-ttu-id="6bed7-103">AM \_ RATE \_ CorrectTS 屬性</span><span class="sxs-lookup"><span data-stu-id="6bed7-103">AM\_RATE\_CorrectTS Property</span></span>

<span data-ttu-id="6bed7-104">DVD 導覽器會使用此屬性來通知解碼器，導覽器會在其傳遞給解碼器的範例上設定正確的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="6bed7-104">The DVD Navigator uses this property to inform the decoder that the Navigator is setting the correct time stamps on the samples it delivers to the decoder.</span></span>



| <span data-ttu-id="6bed7-105">標籤</span><span class="sxs-lookup"><span data-stu-id="6bed7-105">Label</span></span> | <span data-ttu-id="6bed7-106">值</span><span class="sxs-lookup"><span data-stu-id="6bed7-106">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="6bed7-107">屬性集 GUID</span><span class="sxs-lookup"><span data-stu-id="6bed7-107">Property Set GUID</span></span> | <span data-ttu-id="6bed7-108">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="6bed7-108">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="6bed7-109">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="6bed7-109">Property ID</span></span>       | <span data-ttu-id="6bed7-110">AM \_ RATE \_ CorrectTS</span><span class="sxs-lookup"><span data-stu-id="6bed7-110">AM\_RATE\_CorrectTS</span></span>           |
| <span data-ttu-id="6bed7-111">資料類型</span><span class="sxs-lookup"><span data-stu-id="6bed7-111">Data Type</span></span>         | <span data-ttu-id="6bed7-112">**LONG**</span><span class="sxs-lookup"><span data-stu-id="6bed7-112">**LONG**</span></span>                      |



 

## <a name="remarks"></a><span data-ttu-id="6bed7-113">備註</span><span class="sxs-lookup"><span data-stu-id="6bed7-113">Remarks</span></span>

<span data-ttu-id="6bed7-114">當播放速率是1.0 以外的時間時，較舊版本的 DVD Navigator 未設定正確的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="6bed7-114">Earlier versions of the DVD Navigator did not set the correct time stamps when the playback rate was something other than 1.0.</span></span> <span data-ttu-id="6bed7-115">許多的解碼器都能解決此問題，方法是忽略倒轉或向前快轉期間的時間戳記，並估計正確的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="6bed7-115">Many decoders work around this problem by ignoring the time stamps during rewind or fast forward, and estimating the correct presentation times.</span></span>

<span data-ttu-id="6bed7-116">這些問題已在目前的 DVD 導覽器版本中修正。</span><span class="sxs-lookup"><span data-stu-id="6bed7-116">These problems have been corrected in the current version of the DVD Navigator.</span></span> <span data-ttu-id="6bed7-117">為了與現有的解碼器具有回溯相容性，DVD 導覽器會藉由在 \_ \_ 具有 **TRUE** 值的解碼器上設定 AM RATE CorrectTS 屬性，來指出時間戳記是否正確。</span><span class="sxs-lookup"><span data-stu-id="6bed7-117">For backward compatibility with existing decoders, the DVD Navigator indicates that the time stamps are correct by setting the AM\_RATE\_CorrectTS property on the decoder with the value **TRUE**.</span></span> <span data-ttu-id="6bed7-118">當設定這個屬性時，解碼器應該使用實際的時間戳記，而不是估計呈現時間。</span><span class="sxs-lookup"><span data-stu-id="6bed7-118">When this property is set, the decoder should use the actual time stamps, instead of estimating the presentation times.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bed7-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="6bed7-119">Requirements</span></span>



| <span data-ttu-id="6bed7-120">需求</span><span class="sxs-lookup"><span data-stu-id="6bed7-120">Requirement</span></span> | <span data-ttu-id="6bed7-121">值</span><span class="sxs-lookup"><span data-stu-id="6bed7-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6bed7-122">標頭</span><span class="sxs-lookup"><span data-stu-id="6bed7-122">Header</span></span><br/> | <dl> <span data-ttu-id="6bed7-123"><dt>Dvdmedia。h</dt></span><span class="sxs-lookup"><span data-stu-id="6bed7-123"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bed7-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6bed7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bed7-125">**速率變更屬性集**</span><span class="sxs-lookup"><span data-stu-id="6bed7-125">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




