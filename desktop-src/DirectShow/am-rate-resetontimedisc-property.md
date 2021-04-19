---
description: 適用于 Windows Vista 和更新版本。
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: 'AM_RATE_ResetOnTimeDisc 屬性 (Dvdmedia) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c26763d32513652a08d38b52bf6fb745d3d321
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984769"
---
# <a name="am_rate_resetontimedisc-property"></a><span data-ttu-id="55e8d-103">AM \_ RATE \_ ResetOnTimeDisc 屬性</span><span class="sxs-lookup"><span data-stu-id="55e8d-103">AM\_RATE\_ResetOnTimeDisc Property</span></span>

<span data-ttu-id="55e8d-104">適用于 Windows Vista 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="55e8d-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="55e8d-105">此屬性會查詢當解碼器收到具有不連續旗標的範例時，是否將輸出時間戳記重新同步處理至輸入時間戳記。</span><span class="sxs-lookup"><span data-stu-id="55e8d-105">This property queries whether the decoder resynchronizes the output time stamps to the input time stamps when the decoder receives a sample with the discontinuity flag.</span></span>

<span data-ttu-id="55e8d-106">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="55e8d-106">This property is read/write.</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="55e8d-107">屬性集 GUID</span><span class="sxs-lookup"><span data-stu-id="55e8d-107">Property Set GUID</span></span> | <span data-ttu-id="55e8d-108">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="55e8d-108">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="55e8d-109">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="55e8d-109">Property ID</span></span>       | <span data-ttu-id="55e8d-110">AM \_ RATE \_ ResetOnTimeDisc</span><span class="sxs-lookup"><span data-stu-id="55e8d-110">AM\_RATE\_ResetOnTimeDisc</span></span>     |
| <span data-ttu-id="55e8d-111">資料類型</span><span class="sxs-lookup"><span data-stu-id="55e8d-111">Data Type</span></span>         | <span data-ttu-id="55e8d-112">**Dword**</span><span class="sxs-lookup"><span data-stu-id="55e8d-112">**DWORD**</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="55e8d-113">備註</span><span class="sxs-lookup"><span data-stu-id="55e8d-113">Remarks</span></span>

<span data-ttu-id="55e8d-114">這個屬性支援流暢的速率變更。</span><span class="sxs-lookup"><span data-stu-id="55e8d-114">This property supports smooth rate changes.</span></span> <span data-ttu-id="55e8d-115">如果這個屬性的值為 **TRUE** ，且解碼器收到具有 AM 範例 TIMEDISCONTINUITY 旗標的輸入範例 \_ \_ ，則已解碼的框架應該具有與輸入框架相同的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="55e8d-115">If the value of this property is **TRUE** and the decoder receives an input sample with the AM\_SAMPLE\_TIMEDISCONTINUITY flag, the decoded frame should have the same time stamp as the input frame.</span></span>

<span data-ttu-id="55e8d-116">若要取出 AM \_ 範例 \_ TIMEDISCONTINUITY 旗標，請在範例上呼叫 [**IMediaSample2：： GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) 。</span><span class="sxs-lookup"><span data-stu-id="55e8d-116">To retrieve the AM\_SAMPLE\_TIMEDISCONTINUITY flag, call [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) on the sample.</span></span> <span data-ttu-id="55e8d-117">旗標是設定在 [**AM \_ sample2.xml \_ 屬性**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)結構的 **dwSampleFlags** 成員中。</span><span class="sxs-lookup"><span data-stu-id="55e8d-117">The flag is set in the **dwSampleFlags** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

<span data-ttu-id="55e8d-118">如需詳細資訊，請參閱 [Windows Vista 中的 DVD 播放增強功能](dvd-playback-enhancements-in-windows-vista.md)。</span><span class="sxs-lookup"><span data-stu-id="55e8d-118">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55e8d-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="55e8d-119">Requirements</span></span>



| <span data-ttu-id="55e8d-120">需求</span><span class="sxs-lookup"><span data-stu-id="55e8d-120">Requirement</span></span> | <span data-ttu-id="55e8d-121">值</span><span class="sxs-lookup"><span data-stu-id="55e8d-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="55e8d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="55e8d-122">Header</span></span><br/> | <dl> <span data-ttu-id="55e8d-123"><dt>Dvdmedia。h</dt></span><span class="sxs-lookup"><span data-stu-id="55e8d-123"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55e8d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55e8d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55e8d-125">**速率變更屬性集**</span><span class="sxs-lookup"><span data-stu-id="55e8d-125">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




