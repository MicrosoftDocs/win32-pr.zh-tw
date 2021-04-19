---
description: TriggerThread 方法會喚醒處理排程的背景工作執行緒。
ms.assetid: 296a6b59-fc52-4f5e-8a19-6b534a253a6e
title: 'CBaseReferenceClock. TriggerThread 方法 (Refclock .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.TriggerThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f18b4f7dee15ea95046091da006f537830fcbb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979553"
---
# <a name="cbasereferenceclocktriggerthread-method"></a><span data-ttu-id="f8152-103">CBaseReferenceClock. TriggerThread 方法</span><span class="sxs-lookup"><span data-stu-id="f8152-103">CBaseReferenceClock.TriggerThread method</span></span>

<span data-ttu-id="f8152-104">`TriggerThread`方法會喚醒處理排程的背景工作執行緒。</span><span class="sxs-lookup"><span data-stu-id="f8152-104">The `TriggerThread` method wakes up the worker thread that handles scheduling.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8152-105">語法</span><span class="sxs-lookup"><span data-stu-id="f8152-105">Syntax</span></span>


```C++
void TriggerThread();
```



## <a name="parameters"></a><span data-ttu-id="f8152-106">參數</span><span class="sxs-lookup"><span data-stu-id="f8152-106">Parameters</span></span>

<span data-ttu-id="f8152-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f8152-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8152-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="f8152-108">Return value</span></span>

<span data-ttu-id="f8152-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f8152-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8152-110">備註</span><span class="sxs-lookup"><span data-stu-id="f8152-110">Remarks</span></span>

<span data-ttu-id="f8152-111">時鐘會使用在適當時間呼叫 [**CAMSchedule：： Advise**](camschedule-advise.md) 方法的背景工作執行緒。</span><span class="sxs-lookup"><span data-stu-id="f8152-111">The clock uses a worker thread that calls the [**CAMSchedule::Advise**](camschedule-advise.md) method at appropriate times.</span></span> <span data-ttu-id="f8152-112">衍生的類別可以呼叫 `TriggerThread` 喚醒執行緒。</span><span class="sxs-lookup"><span data-stu-id="f8152-112">The derived class can call `TriggerThread` to wake up the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8152-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8152-113">Requirements</span></span>



| <span data-ttu-id="f8152-114">需求</span><span class="sxs-lookup"><span data-stu-id="f8152-114">Requirement</span></span> | <span data-ttu-id="f8152-115">值</span><span class="sxs-lookup"><span data-stu-id="f8152-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8152-116">標頭</span><span class="sxs-lookup"><span data-stu-id="f8152-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f8152-117"><dt>Refclock (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f8152-117"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f8152-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="f8152-118">Library</span></span><br/> | <dl> <span data-ttu-id="f8152-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f8152-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8152-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8152-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8152-121">**CBaseReferenceClock 類別**</span><span class="sxs-lookup"><span data-stu-id="f8152-121">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




