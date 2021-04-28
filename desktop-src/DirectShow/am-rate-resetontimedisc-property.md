---
description: AM_RATE_ResetOnTimeDisc 屬性-適用于 Windows Vista 和更新版本。
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: 'AM_RATE_ResetOnTimeDisc 屬性 (Dvdmedia) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e867bff1f344e80ffd06c9c40276515f2cd4920c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096606"
---
# <a name="am_rate_resetontimedisc-property"></a><span data-ttu-id="a1eea-103">AM \_ RATE \_ ResetOnTimeDisc 屬性</span><span class="sxs-lookup"><span data-stu-id="a1eea-103">AM\_RATE\_ResetOnTimeDisc Property</span></span>

<span data-ttu-id="a1eea-104">適用于 Windows Vista 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="a1eea-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="a1eea-105">此屬性會查詢當解碼器收到具有不連續旗標的範例時，是否將輸出時間戳記重新同步處理至輸入時間戳記。</span><span class="sxs-lookup"><span data-stu-id="a1eea-105">This property queries whether the decoder resynchronizes the output time stamps to the input time stamps when the decoder receives a sample with the discontinuity flag.</span></span>

<span data-ttu-id="a1eea-106">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="a1eea-106">This property is read/write.</span></span>



| <span data-ttu-id="a1eea-107">標籤</span><span class="sxs-lookup"><span data-stu-id="a1eea-107">Label</span></span> | <span data-ttu-id="a1eea-108">值</span><span class="sxs-lookup"><span data-stu-id="a1eea-108">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="a1eea-109">屬性集 GUID</span><span class="sxs-lookup"><span data-stu-id="a1eea-109">Property Set GUID</span></span> | <span data-ttu-id="a1eea-110">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="a1eea-110">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="a1eea-111">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="a1eea-111">Property ID</span></span>       | <span data-ttu-id="a1eea-112">AM \_ RATE \_ ResetOnTimeDisc</span><span class="sxs-lookup"><span data-stu-id="a1eea-112">AM\_RATE\_ResetOnTimeDisc</span></span>     |
| <span data-ttu-id="a1eea-113">資料類型</span><span class="sxs-lookup"><span data-stu-id="a1eea-113">Data Type</span></span>         | <span data-ttu-id="a1eea-114">**Dword**</span><span class="sxs-lookup"><span data-stu-id="a1eea-114">**DWORD**</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="a1eea-115">備註</span><span class="sxs-lookup"><span data-stu-id="a1eea-115">Remarks</span></span>

<span data-ttu-id="a1eea-116">這個屬性支援流暢的速率變更。</span><span class="sxs-lookup"><span data-stu-id="a1eea-116">This property supports smooth rate changes.</span></span> <span data-ttu-id="a1eea-117">如果這個屬性的值為 **TRUE** ，且解碼器收到具有 AM 範例 TIMEDISCONTINUITY 旗標的輸入範例 \_ \_ ，則已解碼的框架應該具有與輸入框架相同的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="a1eea-117">If the value of this property is **TRUE** and the decoder receives an input sample with the AM\_SAMPLE\_TIMEDISCONTINUITY flag, the decoded frame should have the same time stamp as the input frame.</span></span>

<span data-ttu-id="a1eea-118">若要取出 AM \_ 範例 \_ TIMEDISCONTINUITY 旗標，請在範例上呼叫 [**IMediaSample2：： GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) 。</span><span class="sxs-lookup"><span data-stu-id="a1eea-118">To retrieve the AM\_SAMPLE\_TIMEDISCONTINUITY flag, call [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) on the sample.</span></span> <span data-ttu-id="a1eea-119">旗標是設定在 [**AM \_ sample2.xml \_ 屬性**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)結構的 **dwSampleFlags** 成員中。</span><span class="sxs-lookup"><span data-stu-id="a1eea-119">The flag is set in the **dwSampleFlags** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

<span data-ttu-id="a1eea-120">如需詳細資訊，請參閱 [Windows Vista 中的 DVD 播放增強功能](dvd-playback-enhancements-in-windows-vista.md)。</span><span class="sxs-lookup"><span data-stu-id="a1eea-120">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1eea-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1eea-121">Requirements</span></span>



| <span data-ttu-id="a1eea-122">需求</span><span class="sxs-lookup"><span data-stu-id="a1eea-122">Requirement</span></span> | <span data-ttu-id="a1eea-123">值</span><span class="sxs-lookup"><span data-stu-id="a1eea-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1eea-124">標頭</span><span class="sxs-lookup"><span data-stu-id="a1eea-124">Header</span></span><br/> | <dl> <span data-ttu-id="a1eea-125"><dt>Dvdmedia。h</dt></span><span class="sxs-lookup"><span data-stu-id="a1eea-125"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1eea-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1eea-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1eea-127">**速率變更屬性集**</span><span class="sxs-lookup"><span data-stu-id="a1eea-127">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




