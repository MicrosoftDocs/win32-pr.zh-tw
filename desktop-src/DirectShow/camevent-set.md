---
description: Set 方法會為事件發出信號。
ms.assetid: dfcb1601-aa65-47f5-ae3c-f13fcd7b1398
title: 'CAMEvent： Set 方法 (Wxutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9caeed17d42d121ae9263bf6c1fcd011ed573c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978452"
---
# <a name="cameventset-method"></a><span data-ttu-id="206bf-103">CAMEvent 方法</span><span class="sxs-lookup"><span data-stu-id="206bf-103">CAMEvent.Set method</span></span>

<span data-ttu-id="206bf-104">方法會為 `Set` 事件發出信號。</span><span class="sxs-lookup"><span data-stu-id="206bf-104">The `Set` method signals the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="206bf-105">語法</span><span class="sxs-lookup"><span data-stu-id="206bf-105">Syntax</span></span>


```C++
void Set();
```



## <a name="parameters"></a><span data-ttu-id="206bf-106">參數</span><span class="sxs-lookup"><span data-stu-id="206bf-106">Parameters</span></span>

<span data-ttu-id="206bf-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="206bf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="206bf-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="206bf-108">Return value</span></span>

<span data-ttu-id="206bf-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="206bf-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="206bf-110">備註</span><span class="sxs-lookup"><span data-stu-id="206bf-110">Remarks</span></span>

<span data-ttu-id="206bf-111">此行為取決於物件是否為自動重設事件或手動重設事件：</span><span class="sxs-lookup"><span data-stu-id="206bf-111">The behavior depends on whether the object is an auto-reset event or a manual-reset event:</span></span>

-   <span data-ttu-id="206bf-112">**自動重設**：如果有任何執行緒正在等候此事件，則會釋放一個執行緒，並重設該事件。</span><span class="sxs-lookup"><span data-stu-id="206bf-112">**Auto-reset**: If any threads are waiting on this event, one thread is released and the event is reset.</span></span> <span data-ttu-id="206bf-113">如果沒有任何執行緒正在等候此事件，事件會維持為信號。</span><span class="sxs-lookup"><span data-stu-id="206bf-113">If no threads are waiting on this event, the event remains signaled.</span></span>
-   <span data-ttu-id="206bf-114">**手動重設**：會釋放所有等候此事件的執行緒。</span><span class="sxs-lookup"><span data-stu-id="206bf-114">**Manual-reset**: All the threads waiting on this event are released.</span></span> <span data-ttu-id="206bf-115">事件仍會收到信號。</span><span class="sxs-lookup"><span data-stu-id="206bf-115">The event remains signaled.</span></span>

## <a name="requirements"></a><span data-ttu-id="206bf-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="206bf-116">Requirements</span></span>



| <span data-ttu-id="206bf-117">需求</span><span class="sxs-lookup"><span data-stu-id="206bf-117">Requirement</span></span> | <span data-ttu-id="206bf-118">值</span><span class="sxs-lookup"><span data-stu-id="206bf-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="206bf-119">標頭</span><span class="sxs-lookup"><span data-stu-id="206bf-119">Header</span></span><br/>  | <dl> <span data-ttu-id="206bf-120"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="206bf-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="206bf-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="206bf-121">Library</span></span><br/> | <dl> <span data-ttu-id="206bf-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="206bf-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="206bf-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="206bf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="206bf-124">**CAMEvent 類別**</span><span class="sxs-lookup"><span data-stu-id="206bf-124">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




