---
description: NotifyThread 方法會通知執行緒佇列包含資料。
ms.assetid: d91cde3f-2876-4fb4-a124-f1460bba2cc9
title: 'COutputQueue. NotifyThread 方法 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.NotifyThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bb5f965bac15e99140955e8ee2519feaadfef85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985964"
---
# <a name="coutputqueuenotifythread-method"></a><span data-ttu-id="5818d-103">COutputQueue. NotifyThread 方法</span><span class="sxs-lookup"><span data-stu-id="5818d-103">COutputQueue.NotifyThread method</span></span>

<span data-ttu-id="5818d-104">`NotifyThread`方法會通知執行緒佇列包含資料。</span><span class="sxs-lookup"><span data-stu-id="5818d-104">The `NotifyThread` method notifies the thread that the queue contains data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5818d-105">語法</span><span class="sxs-lookup"><span data-stu-id="5818d-105">Syntax</span></span>


```C++
void NotifyThread();
```



## <a name="parameters"></a><span data-ttu-id="5818d-106">參數</span><span class="sxs-lookup"><span data-stu-id="5818d-106">Parameters</span></span>

<span data-ttu-id="5818d-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="5818d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5818d-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="5818d-108">Return value</span></span>

<span data-ttu-id="5818d-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5818d-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5818d-110">備註</span><span class="sxs-lookup"><span data-stu-id="5818d-110">Remarks</span></span>

<span data-ttu-id="5818d-111">在呼叫這個方法之前，請先保存重要區段。</span><span class="sxs-lookup"><span data-stu-id="5818d-111">Hold the critical section before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5818d-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="5818d-112">Requirements</span></span>



| <span data-ttu-id="5818d-113">需求</span><span class="sxs-lookup"><span data-stu-id="5818d-113">Requirement</span></span> | <span data-ttu-id="5818d-114">值</span><span class="sxs-lookup"><span data-stu-id="5818d-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5818d-115">標頭</span><span class="sxs-lookup"><span data-stu-id="5818d-115">Header</span></span><br/>  | <dl> <span data-ttu-id="5818d-116"><dt>Outputq (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5818d-116"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5818d-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="5818d-117">Library</span></span><br/> | <dl> <span data-ttu-id="5818d-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="5818d-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5818d-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5818d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5818d-120">**COutputQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="5818d-120">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




