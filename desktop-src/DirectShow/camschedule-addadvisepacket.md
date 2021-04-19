---
description: AddAdvisePacket 方法會將建議要求新增至暫止的要求清單。
ms.assetid: 138d8404-7d28-47cc-91b4-4733a113ac7a
title: 'CAMSchedule. AddAdvisePacket 方法 (Dsschedule .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.AddAdvisePacket
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dd9586b09586c12f1a30f45b512336831372295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999272"
---
# <a name="camscheduleaddadvisepacket-method"></a><span data-ttu-id="3d6bf-103">CAMSchedule. AddAdvisePacket 方法</span><span class="sxs-lookup"><span data-stu-id="3d6bf-103">CAMSchedule.AddAdvisePacket method</span></span>

<span data-ttu-id="3d6bf-104">`AddAdvisePacket`方法會將建議要求新增至暫止的要求清單。</span><span class="sxs-lookup"><span data-stu-id="3d6bf-104">The `AddAdvisePacket` method adds an advise request to the list of pending requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d6bf-105">語法</span><span class="sxs-lookup"><span data-stu-id="3d6bf-105">Syntax</span></span>


```C++
DWORD_PTR AddAdvisePacket(
  [ref] const REFERENCE_TIME &time1,
  [ref] const REFERENCE_TIME &time2,
              HANDLE         hNotify,
              BOOL           bPeriodic
);
```



## <a name="parameters"></a><span data-ttu-id="3d6bf-106">參數</span><span class="sxs-lookup"><span data-stu-id="3d6bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d6bf-107">*time1* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="3d6bf-107">*time1* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="3d6bf-108">建議的要求時間。</span><span class="sxs-lookup"><span data-stu-id="3d6bf-108">Requested time for the advise.</span></span>

</dd> <dt>

<span data-ttu-id="3d6bf-109">*time2* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="3d6bf-109">*time2* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="3d6bf-110">針對週期性建議要求，這是通知之間的時間。</span><span class="sxs-lookup"><span data-stu-id="3d6bf-110">For periodic advise requests, the time between notifications.</span></span> <span data-ttu-id="3d6bf-111">如果 *bPeriodic* 為 **FALSE**，則會忽略此參數。</span><span class="sxs-lookup"><span data-stu-id="3d6bf-111">This parameter is ignored if *bPeriodic* is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="3d6bf-112">*hNotify*</span><span class="sxs-lookup"><span data-stu-id="3d6bf-112">*hNotify*</span></span> 
</dt> <dd>

<span data-ttu-id="3d6bf-113">如果 *bPeriodic* 為 **TRUE**，則為信號的控制碼，如果 *bPeriodic* 為 **FALSE**，則處理事件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3d6bf-113">Handle to a semaphore if *bPeriodic* is **TRUE**, or handle to an event if *bPeriodic* is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="3d6bf-114">*bPeriodic*</span><span class="sxs-lookup"><span data-stu-id="3d6bf-114">*bPeriodic*</span></span> 
</dt> <dd>

<span data-ttu-id="3d6bf-115">指定是否要新增定期通知或單次通知的布林值。</span><span class="sxs-lookup"><span data-stu-id="3d6bf-115">Boolean value that specifies whether to add a periodic notification or a one-shot notification.</span></span> <span data-ttu-id="3d6bf-116">若 **為 TRUE**，則會定期通知; *time2* 參數會指定通知之間的時間。</span><span class="sxs-lookup"><span data-stu-id="3d6bf-116">If **TRUE**, the notification is periodic; the *time2* parameter specifies the time between notifications.</span></span> <span data-ttu-id="3d6bf-117">若 **為 FALSE**，則只會出現一次通知。</span><span class="sxs-lookup"><span data-stu-id="3d6bf-117">If **FALSE**, the notification occurs only once.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d6bf-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="3d6bf-118">Return value</span></span>

<span data-ttu-id="3d6bf-119">傳回「cookie」 )  (「建議」要求的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3d6bf-119">Returns an identifier for the advise request (the "cookie").</span></span> <span data-ttu-id="3d6bf-120">如果方法失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="3d6bf-120">If the method fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d6bf-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d6bf-121">Requirements</span></span>



| <span data-ttu-id="3d6bf-122">需求</span><span class="sxs-lookup"><span data-stu-id="3d6bf-122">Requirement</span></span> | <span data-ttu-id="3d6bf-123">值</span><span class="sxs-lookup"><span data-stu-id="3d6bf-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d6bf-124">標頭</span><span class="sxs-lookup"><span data-stu-id="3d6bf-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3d6bf-125"><dt>Dsschedule (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3d6bf-125"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="3d6bf-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="3d6bf-126">Library</span></span><br/> | <dl> <span data-ttu-id="3d6bf-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3d6bf-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d6bf-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d6bf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d6bf-129">**CAMSchedule 類別**</span><span class="sxs-lookup"><span data-stu-id="3d6bf-129">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




