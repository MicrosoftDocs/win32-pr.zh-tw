---
description: CAMEvent。 CAMEvent 函式-函數方法。
ms.assetid: 35c9ac07-8756-42b1-beeb-5f0e79466742
title: 'CAMEvent. CAMEvent (Wxutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cdd37ba72d9467c16d46b2aec3ec40c206466eaf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096528"
---
# <a name="cameventcamevent-constructor"></a><span data-ttu-id="131e2-103">CAMEvent. CAMEvent 函數</span><span class="sxs-lookup"><span data-stu-id="131e2-103">CAMEvent.CAMEvent constructor</span></span>

<span data-ttu-id="131e2-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="131e2-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="131e2-105">語法</span><span class="sxs-lookup"><span data-stu-id="131e2-105">Syntax</span></span>


```C++
CAMEvent(
   BOOL    fManualReset,
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="131e2-106">參數</span><span class="sxs-lookup"><span data-stu-id="131e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="131e2-107">*fManualReset*</span><span class="sxs-lookup"><span data-stu-id="131e2-107">*fManualReset*</span></span> 
</dt> <dd>

<span data-ttu-id="131e2-108">布林值，指定物件是否為手動重設事件或自動重設事件。</span><span class="sxs-lookup"><span data-stu-id="131e2-108">Boolean value that specifies whether the object is a manual-reset event or an auto-reset event.</span></span> <span data-ttu-id="131e2-109">若 **為 TRUE**，表示物件是手動重設事件。</span><span class="sxs-lookup"><span data-stu-id="131e2-109">If **TRUE**, the object is a manual-reset event.</span></span> <span data-ttu-id="131e2-110">否則，它會是自動重設事件。</span><span class="sxs-lookup"><span data-stu-id="131e2-110">Otherwise, it is an auto-reset event.</span></span>

</dd> <dt>

<span data-ttu-id="131e2-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="131e2-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="131e2-112">**HRESULT** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="131e2-112">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="131e2-113">如果函式失敗，此參數會收到錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="131e2-113">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="131e2-114">如果發生這種情況，則物件不是處於有效的狀態。</span><span class="sxs-lookup"><span data-stu-id="131e2-114">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="131e2-115">為了與舊版 strmbase 回溯相容，此參數預設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="131e2-115">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="131e2-116">不過，最好是傳遞非 **Null** 值，讓呼叫端可以檢查物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="131e2-116">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="131e2-117">備註</span><span class="sxs-lookup"><span data-stu-id="131e2-117">Remarks</span></span>

<span data-ttu-id="131e2-118">事件會以未收到信號狀態開始。</span><span class="sxs-lookup"><span data-stu-id="131e2-118">The event begins in a nonsignaled state.</span></span>

<span data-ttu-id="131e2-119">使用自動重設事件， [**CAMEvent：： Wait**](camevent-wait.md) 方法會在方法傳回時，將事件重設為未收到信號。</span><span class="sxs-lookup"><span data-stu-id="131e2-119">With an auto-reset event, the [**CAMEvent::Wait**](camevent-wait.md) method resets the event to nonsignaled when the method returns.</span></span> <span data-ttu-id="131e2-120">若使用手動重設事件，事件會保持為信號，直到您呼叫 [**CAMEvent：： reset**](camevent-reset.md) 方法為止。</span><span class="sxs-lookup"><span data-stu-id="131e2-120">With a manual-reset event, the event remains signaled until you call the [**CAMEvent::Reset**](camevent-reset.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="131e2-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="131e2-121">Requirements</span></span>



| <span data-ttu-id="131e2-122">需求</span><span class="sxs-lookup"><span data-stu-id="131e2-122">Requirement</span></span> | <span data-ttu-id="131e2-123">值</span><span class="sxs-lookup"><span data-stu-id="131e2-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="131e2-124">標頭</span><span class="sxs-lookup"><span data-stu-id="131e2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="131e2-125"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="131e2-125"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="131e2-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="131e2-126">Library</span></span><br/> | <dl> <span data-ttu-id="131e2-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="131e2-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="131e2-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="131e2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="131e2-129">**CAMEvent 類別**</span><span class="sxs-lookup"><span data-stu-id="131e2-129">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




