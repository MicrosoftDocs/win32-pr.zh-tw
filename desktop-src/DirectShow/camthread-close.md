---
description: Close 方法會等候執行緒結束，然後釋放其資源。
ms.assetid: 57e27ff7-3665-416e-8a6e-660483c5aed2
title: 'CAMThread. Close 方法 (Wxutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Close
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9cac5ee4a1e1a9cc3fecc8d09096d031e9fc9a63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976197"
---
# <a name="camthreadclose-method"></a><span data-ttu-id="85c88-103">CAMThread. Close 方法</span><span class="sxs-lookup"><span data-stu-id="85c88-103">CAMThread.Close method</span></span>

<span data-ttu-id="85c88-104">`Close`方法會等候執行緒結束，然後釋放其資源。</span><span class="sxs-lookup"><span data-stu-id="85c88-104">The `Close` method waits for the thread to exit, then releases its resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="85c88-105">語法</span><span class="sxs-lookup"><span data-stu-id="85c88-105">Syntax</span></span>


```C++
void Close();
```



## <a name="parameters"></a><span data-ttu-id="85c88-106">參數</span><span class="sxs-lookup"><span data-stu-id="85c88-106">Parameters</span></span>

<span data-ttu-id="85c88-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="85c88-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="85c88-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="85c88-108">Return value</span></span>

<span data-ttu-id="85c88-109">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="85c88-109">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85c88-110">備註</span><span class="sxs-lookup"><span data-stu-id="85c88-110">Remarks</span></span>

<span data-ttu-id="85c88-111">在呼叫這個方法之前，您必須提供方法讓執行緒結束。</span><span class="sxs-lookup"><span data-stu-id="85c88-111">Before calling this method, you must provide a way for the thread to exit.</span></span> <span data-ttu-id="85c88-112">例如，在您的 [**CAMThread：： ThreadProc**](camthread-threadproc.md) 方法中，定義通知執行緒結束的要求。</span><span class="sxs-lookup"><span data-stu-id="85c88-112">For example, in your [**CAMThread::ThreadProc**](camthread-threadproc.md) method, define a request that signals the thread to exit.</span></span> <span data-ttu-id="85c88-113">然後以該值呼叫 [**CAMThread：： CallWorker**](camthread-callworker.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="85c88-113">Then call the [**CAMThread::CallWorker**](camthread-callworker.md) method with that value.</span></span>

<span data-ttu-id="85c88-114">[**~ CAMThread**](camthread--camthread.md)的「函式」方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="85c88-114">The [**~ CAMThread**](camthread--camthread.md) destructor method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="85c88-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="85c88-115">Requirements</span></span>



| <span data-ttu-id="85c88-116">需求</span><span class="sxs-lookup"><span data-stu-id="85c88-116">Requirement</span></span> | <span data-ttu-id="85c88-117">值</span><span class="sxs-lookup"><span data-stu-id="85c88-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85c88-118">標頭</span><span class="sxs-lookup"><span data-stu-id="85c88-118">Header</span></span><br/>  | <dl> <span data-ttu-id="85c88-119"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="85c88-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="85c88-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="85c88-120">Library</span></span><br/> | <dl> <span data-ttu-id="85c88-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="85c88-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85c88-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85c88-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85c88-123">**CAMThread 類別**</span><span class="sxs-lookup"><span data-stu-id="85c88-123">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




