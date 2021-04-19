---
description: CheckRequest 方法會檢查是否有要求，而不會封鎖。
ms.assetid: 46d0840e-a304-41e3-9016-9f35e404cd30
title: 'CAMThread. CheckRequest 方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a004e0f5303cf6702c03e78c292a6a2d832a489
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982615"
---
# <a name="camthreadcheckrequest-method"></a><span data-ttu-id="3de72-103">CAMThread. CheckRequest 方法</span><span class="sxs-lookup"><span data-stu-id="3de72-103">CAMThread.CheckRequest method</span></span>

<span data-ttu-id="3de72-104">`CheckRequest`方法會檢查是否有要求，而不會封鎖。</span><span class="sxs-lookup"><span data-stu-id="3de72-104">The `CheckRequest` method checks if there is a request, without blocking.</span></span>

## <a name="syntax"></a><span data-ttu-id="3de72-105">語法</span><span class="sxs-lookup"><span data-stu-id="3de72-105">Syntax</span></span>


```C++
BOOL CheckRequest(
   DWORD *pParam
);
```



## <a name="parameters"></a><span data-ttu-id="3de72-106">參數</span><span class="sxs-lookup"><span data-stu-id="3de72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3de72-107">*pParam*</span><span class="sxs-lookup"><span data-stu-id="3de72-107">*pParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3de72-108">變數的指標，此變數會接收最後呼叫 [**CAMThread：： CallWorker**](camthread-callworker.md) 方法時所傳遞的值。</span><span class="sxs-lookup"><span data-stu-id="3de72-108">Pointer to a variable that receives the value passed in the last call to the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3de72-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="3de72-109">Return value</span></span>

<span data-ttu-id="3de72-110">如果有暫止的要求，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="3de72-110">Returns **TRUE** if there is a pending request, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3de72-111">備註</span><span class="sxs-lookup"><span data-stu-id="3de72-111">Remarks</span></span>

<span data-ttu-id="3de72-112">這個方法是 [**CAMThread：： GetRequest**](camthread-getrequest.md) 方法的非封鎖版本。</span><span class="sxs-lookup"><span data-stu-id="3de72-112">This method is a non-blocking version of the [**CAMThread::GetRequest**](camthread-getrequest.md) method.</span></span>

<span data-ttu-id="3de72-113">如果另一個執行緒正在等候呼叫 CallWorker，這個方法會抓取要求參數，並傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="3de72-113">If another thread is waiting on a call to CallWorker, this method retrieves the request parameter and returns **TRUE**.</span></span> <span data-ttu-id="3de72-114">否則，它會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="3de72-114">Otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="3de72-115">如果方法傳回 **TRUE**，則呼叫 [**CAMThread：： Reply**](camthread-reply.md) 方法以釋放要求的執行緒。</span><span class="sxs-lookup"><span data-stu-id="3de72-115">If the method returns **TRUE**, call the [**CAMThread::Reply**](camthread-reply.md) method to release the requesting thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="3de72-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="3de72-116">Requirements</span></span>



| <span data-ttu-id="3de72-117">需求</span><span class="sxs-lookup"><span data-stu-id="3de72-117">Requirement</span></span> | <span data-ttu-id="3de72-118">值</span><span class="sxs-lookup"><span data-stu-id="3de72-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3de72-119">標頭</span><span class="sxs-lookup"><span data-stu-id="3de72-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3de72-120"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3de72-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3de72-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="3de72-121">Library</span></span><br/> | <dl> <span data-ttu-id="3de72-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3de72-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3de72-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3de72-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3de72-124">**CAMThread 類別**</span><span class="sxs-lookup"><span data-stu-id="3de72-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




