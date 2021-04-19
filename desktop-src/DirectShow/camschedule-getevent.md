---
description: GetEvent 方法會抓取事件控制碼，此控制碼可用來在下一個建議時間中通知變更。
ms.assetid: 2548a321-df65-4a5b-9e6a-8bbc031254c7
title: 'CAMSchedule. GetEvent 方法 (Dsschedule .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 360a4b88c8c03d2f04ad55bc65eebf6be3797c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995311"
---
# <a name="camschedulegetevent-method"></a><span data-ttu-id="31a2d-103">CAMSchedule. GetEvent 方法</span><span class="sxs-lookup"><span data-stu-id="31a2d-103">CAMSchedule.GetEvent method</span></span>

<span data-ttu-id="31a2d-104">此 `GetEvent` 方法會抓取事件控制碼，此控制碼可用來在下一個建議時間發出變更。</span><span class="sxs-lookup"><span data-stu-id="31a2d-104">The `GetEvent` method retrieves an event handle, which is used to signal a change in the next advise time.</span></span>

## <a name="syntax"></a><span data-ttu-id="31a2d-105">語法</span><span class="sxs-lookup"><span data-stu-id="31a2d-105">Syntax</span></span>


```C++
HANDLE GetEvent();
```



## <a name="parameters"></a><span data-ttu-id="31a2d-106">參數</span><span class="sxs-lookup"><span data-stu-id="31a2d-106">Parameters</span></span>

<span data-ttu-id="31a2d-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="31a2d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="31a2d-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="31a2d-108">Return value</span></span>

<span data-ttu-id="31a2d-109">傳回事件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="31a2d-109">Returns a handle to an event.</span></span>

## <a name="remarks"></a><span data-ttu-id="31a2d-110">備註</span><span class="sxs-lookup"><span data-stu-id="31a2d-110">Remarks</span></span>

<span data-ttu-id="31a2d-111">如果下一個建議時間變更為其他字組，則如果新的建議要求新增至清單前端，則排程器會發出信號給此事件。</span><span class="sxs-lookup"><span data-stu-id="31a2d-111">If the next advise time changes in other words, if a new advise request is added to the front of the list the scheduler signals this event.</span></span> <span data-ttu-id="31a2d-112">時鐘應該呼叫 [**CAMSchedule：： Advise**](camschedule-advise.md) 方法以判斷下一個建議時間。</span><span class="sxs-lookup"><span data-stu-id="31a2d-112">The clock should call the [**CAMSchedule::Advise**](camschedule-advise.md) method to determine the next advise time.</span></span>

## <a name="requirements"></a><span data-ttu-id="31a2d-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="31a2d-113">Requirements</span></span>



| <span data-ttu-id="31a2d-114">需求</span><span class="sxs-lookup"><span data-stu-id="31a2d-114">Requirement</span></span> | <span data-ttu-id="31a2d-115">值</span><span class="sxs-lookup"><span data-stu-id="31a2d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31a2d-116">標頭</span><span class="sxs-lookup"><span data-stu-id="31a2d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="31a2d-117"><dt>Dsschedule (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="31a2d-117"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="31a2d-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="31a2d-118">Library</span></span><br/> | <dl> <span data-ttu-id="31a2d-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="31a2d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31a2d-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31a2d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31a2d-121">**CAMSchedule 類別**</span><span class="sxs-lookup"><span data-stu-id="31a2d-121">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




