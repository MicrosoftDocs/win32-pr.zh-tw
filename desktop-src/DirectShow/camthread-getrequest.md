---
description: GetRequest 方法會等候下一個要求。
ms.assetid: 9f275ee6-cb78-455a-b924-7337c8d2a6dd
title: 'CAMThread. GetRequest 方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 506707bc78583fd9729ad28fb5507b82bee5e670
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978777"
---
# <a name="camthreadgetrequest-method"></a><span data-ttu-id="75c31-103">CAMThread. GetRequest 方法</span><span class="sxs-lookup"><span data-stu-id="75c31-103">CAMThread.GetRequest method</span></span>

<span data-ttu-id="75c31-104">`GetRequest`方法會等候下一個要求。</span><span class="sxs-lookup"><span data-stu-id="75c31-104">The `GetRequest` method waits for the next request.</span></span>

## <a name="syntax"></a><span data-ttu-id="75c31-105">語法</span><span class="sxs-lookup"><span data-stu-id="75c31-105">Syntax</span></span>


```C++
DWORD GetRequest();
```



## <a name="parameters"></a><span data-ttu-id="75c31-106">參數</span><span class="sxs-lookup"><span data-stu-id="75c31-106">Parameters</span></span>

<span data-ttu-id="75c31-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="75c31-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="75c31-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="75c31-108">Return value</span></span>

<span data-ttu-id="75c31-109">傳回衍生類別所定義的值。</span><span class="sxs-lookup"><span data-stu-id="75c31-109">Returns a value that is defined by the derived class.</span></span>

## <a name="remarks"></a><span data-ttu-id="75c31-110">備註</span><span class="sxs-lookup"><span data-stu-id="75c31-110">Remarks</span></span>

<span data-ttu-id="75c31-111">這個方法會封鎖，直到另一個執行緒呼叫 [**CAMThread：： CallWorker**](camthread-callworker.md) 方法為止。</span><span class="sxs-lookup"><span data-stu-id="75c31-111">This method blocks until another thread calls the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span> <span data-ttu-id="75c31-112">然後，它會傳回傳遞給 CallWorker 的參數。</span><span class="sxs-lookup"><span data-stu-id="75c31-112">Then it returns the parameter that was passed to CallWorker.</span></span> <span data-ttu-id="75c31-113">呼叫 [**CAMThread：： Reply**](camthread-reply.md) 方法以釋放要求的執行緒。</span><span class="sxs-lookup"><span data-stu-id="75c31-113">Call the [**CAMThread::Reply**](camthread-reply.md) method to release the requesting thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="75c31-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="75c31-114">Requirements</span></span>



| <span data-ttu-id="75c31-115">需求</span><span class="sxs-lookup"><span data-stu-id="75c31-115">Requirement</span></span> | <span data-ttu-id="75c31-116">值</span><span class="sxs-lookup"><span data-stu-id="75c31-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75c31-117">標頭</span><span class="sxs-lookup"><span data-stu-id="75c31-117">Header</span></span><br/>  | <dl> <span data-ttu-id="75c31-118"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="75c31-118"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="75c31-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="75c31-119">Library</span></span><br/> | <dl> <span data-ttu-id="75c31-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="75c31-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75c31-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75c31-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75c31-122">**CAMThread 類別**</span><span class="sxs-lookup"><span data-stu-id="75c31-122">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




