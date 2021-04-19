---
description: DVD 導覽器會使用此屬性來通知解碼器，導覽器會在其傳遞給解碼器的範例上設定正確的時間戳記。
ms.assetid: f04e8291-734f-483e-b756-5362beb68d9c
title: 'AM_RATE_CorrectTS 屬性 (Dvdmedia) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa410b079d3de63de364662c7d5465c82814d24a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976161"
---
# <a name="am_rate_correctts-property"></a><span data-ttu-id="e3c74-103">AM \_ RATE \_ CorrectTS 屬性</span><span class="sxs-lookup"><span data-stu-id="e3c74-103">AM\_RATE\_CorrectTS Property</span></span>

<span data-ttu-id="e3c74-104">DVD 導覽器會使用此屬性來通知解碼器，導覽器會在其傳遞給解碼器的範例上設定正確的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="e3c74-104">The DVD Navigator uses this property to inform the decoder that the Navigator is setting the correct time stamps on the samples it delivers to the decoder.</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="e3c74-105">屬性集 GUID</span><span class="sxs-lookup"><span data-stu-id="e3c74-105">Property Set GUID</span></span> | <span data-ttu-id="e3c74-106">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="e3c74-106">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="e3c74-107">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="e3c74-107">Property ID</span></span>       | <span data-ttu-id="e3c74-108">AM \_ RATE \_ CorrectTS</span><span class="sxs-lookup"><span data-stu-id="e3c74-108">AM\_RATE\_CorrectTS</span></span>           |
| <span data-ttu-id="e3c74-109">資料類型</span><span class="sxs-lookup"><span data-stu-id="e3c74-109">Data Type</span></span>         | <span data-ttu-id="e3c74-110">**LONG**</span><span class="sxs-lookup"><span data-stu-id="e3c74-110">**LONG**</span></span>                      |



 

## <a name="remarks"></a><span data-ttu-id="e3c74-111">備註</span><span class="sxs-lookup"><span data-stu-id="e3c74-111">Remarks</span></span>

<span data-ttu-id="e3c74-112">當播放速率是1.0 以外的時間時，較舊版本的 DVD Navigator 未設定正確的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="e3c74-112">Earlier versions of the DVD Navigator did not set the correct time stamps when the playback rate was something other than 1.0.</span></span> <span data-ttu-id="e3c74-113">許多的解碼器都能解決此問題，方法是忽略倒轉或向前快轉期間的時間戳記，並估計正確的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="e3c74-113">Many decoders work around this problem by ignoring the time stamps during rewind or fast forward, and estimating the correct presentation times.</span></span>

<span data-ttu-id="e3c74-114">這些問題已在目前的 DVD 導覽器版本中修正。</span><span class="sxs-lookup"><span data-stu-id="e3c74-114">These problems have been corrected in the current version of the DVD Navigator.</span></span> <span data-ttu-id="e3c74-115">為了與現有的解碼器具有回溯相容性，DVD 導覽器會藉由在 \_ \_ 具有 **TRUE** 值的解碼器上設定 AM RATE CorrectTS 屬性，來指出時間戳記是否正確。</span><span class="sxs-lookup"><span data-stu-id="e3c74-115">For backward compatibility with existing decoders, the DVD Navigator indicates that the time stamps are correct by setting the AM\_RATE\_CorrectTS property on the decoder with the value **TRUE**.</span></span> <span data-ttu-id="e3c74-116">當設定這個屬性時，解碼器應該使用實際的時間戳記，而不是估計呈現時間。</span><span class="sxs-lookup"><span data-stu-id="e3c74-116">When this property is set, the decoder should use the actual time stamps, instead of estimating the presentation times.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3c74-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3c74-117">Requirements</span></span>



| <span data-ttu-id="e3c74-118">需求</span><span class="sxs-lookup"><span data-stu-id="e3c74-118">Requirement</span></span> | <span data-ttu-id="e3c74-119">值</span><span class="sxs-lookup"><span data-stu-id="e3c74-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3c74-120">標頭</span><span class="sxs-lookup"><span data-stu-id="e3c74-120">Header</span></span><br/> | <dl> <span data-ttu-id="e3c74-121"><dt>Dvdmedia。h</dt></span><span class="sxs-lookup"><span data-stu-id="e3c74-121"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3c74-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3c74-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3c74-123">**速率變更屬性集**</span><span class="sxs-lookup"><span data-stu-id="e3c74-123">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




