---
description: CallWorker 方法會向執行緒發出要求的信號。
ms.assetid: 51431688-bf55-4778-afc0-91b6ab336aa3
title: 'CAMThread. CallWorker 方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CallWorker
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7410fbee4ece729d1579f525731bddaceded1153
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978456"
---
# <a name="camthreadcallworker-method"></a><span data-ttu-id="76bde-103">CAMThread. CallWorker 方法</span><span class="sxs-lookup"><span data-stu-id="76bde-103">CAMThread.CallWorker method</span></span>

<span data-ttu-id="76bde-104">`CallWorker`方法會向執行緒發出要求的信號。</span><span class="sxs-lookup"><span data-stu-id="76bde-104">The `CallWorker` method signals the thread with a request.</span></span>

## <a name="syntax"></a><span data-ttu-id="76bde-105">語法</span><span class="sxs-lookup"><span data-stu-id="76bde-105">Syntax</span></span>


```C++
DWORD CallWorker(
   DWORD dwParam
);
```



## <a name="parameters"></a><span data-ttu-id="76bde-106">參數</span><span class="sxs-lookup"><span data-stu-id="76bde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76bde-107">*dwParam*</span><span class="sxs-lookup"><span data-stu-id="76bde-107">*dwParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76bde-108">要求參數。</span><span class="sxs-lookup"><span data-stu-id="76bde-108">Request parameter.</span></span> <span data-ttu-id="76bde-109">衍生的類別會定義參數的意義。</span><span class="sxs-lookup"><span data-stu-id="76bde-109">The derived class defines the meaning of the parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76bde-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="76bde-110">Return value</span></span>

<span data-ttu-id="76bde-111">傳回衍生類別所定義的值。</span><span class="sxs-lookup"><span data-stu-id="76bde-111">Returns a value that is defined by the derived class.</span></span>

## <a name="remarks"></a><span data-ttu-id="76bde-112">備註</span><span class="sxs-lookup"><span data-stu-id="76bde-112">Remarks</span></span>

<span data-ttu-id="76bde-113">[**CAMThread：： GetRequest**](camthread-getrequest.md)和 [**CAMThread：： CheckRequest**](camthread-checkrequest.md)方法會取出 *dwParam* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="76bde-113">The [**CAMThread::GetRequest**](camthread-getrequest.md) and [**CAMThread::CheckRequest**](camthread-checkrequest.md) methods retrieve the value of the *dwParam* parameter.</span></span> <span data-ttu-id="76bde-114">GetRequest 方法 `CallWorker` 會封鎖，直到呼叫為止。</span><span class="sxs-lookup"><span data-stu-id="76bde-114">The GetRequest method blocks until `CallWorker` is called.</span></span>

<span data-ttu-id="76bde-115">這個方法會封鎖，直到呼叫 [**CAMThread：： Reply**](camthread-reply.md) 方法為止。</span><span class="sxs-lookup"><span data-stu-id="76bde-115">This method blocks until the [**CAMThread::Reply**](camthread-reply.md) method is called.</span></span> <span data-ttu-id="76bde-116">傳回值是指定要回復的參數。</span><span class="sxs-lookup"><span data-stu-id="76bde-116">The return value is the parameter given to Reply.</span></span>

<span data-ttu-id="76bde-117">這個方法會保留 [**CAMThread：： m \_ AccessLock**](camthread-m-accesslock.md) 鎖定以序列化要求。</span><span class="sxs-lookup"><span data-stu-id="76bde-117">This method holds the [**CAMThread::m\_AccessLock**](camthread-m-accesslock.md) lock to serialize requests.</span></span> <span data-ttu-id="76bde-118">因此，請從執行緒本身或線上程內容中執行的任何成員函式，呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="76bde-118">Therefore, do call this method from the thread itself or from any member function that executes in the context of the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="76bde-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="76bde-119">Requirements</span></span>



| <span data-ttu-id="76bde-120">需求</span><span class="sxs-lookup"><span data-stu-id="76bde-120">Requirement</span></span> | <span data-ttu-id="76bde-121">值</span><span class="sxs-lookup"><span data-stu-id="76bde-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76bde-122">標頭</span><span class="sxs-lookup"><span data-stu-id="76bde-122">Header</span></span><br/>  | <dl> <span data-ttu-id="76bde-123"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="76bde-123"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="76bde-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="76bde-124">Library</span></span><br/> | <dl> <span data-ttu-id="76bde-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="76bde-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76bde-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="76bde-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76bde-127">**CAMThread 類別**</span><span class="sxs-lookup"><span data-stu-id="76bde-127">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




