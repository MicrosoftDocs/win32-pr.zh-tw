---
description: ThreadProc 方法是工作者執行緒的執行緒程式。 這個方法會實作為純虛擬 CAMThread：： ThreadProc 方法。
ms.assetid: 8e66b609-d795-45a8-8fe5-774c659ee350
title: 'CSourceStream. ThreadProc 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6dc7d08643cc0ca76d3d05f0b9090f30200eb181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987020"
---
# <a name="csourcestreamthreadproc-method"></a><span data-ttu-id="2a94b-104">CSourceStream. ThreadProc 方法</span><span class="sxs-lookup"><span data-stu-id="2a94b-104">CSourceStream.ThreadProc method</span></span>

<span data-ttu-id="2a94b-105">`ThreadProc`方法是工作者執行緒的執行緒程式。</span><span class="sxs-lookup"><span data-stu-id="2a94b-105">The `ThreadProc` method is the thread procedure for the worker thread.</span></span> <span data-ttu-id="2a94b-106">這個方法會實作為純虛擬 [**CAMThread：： ThreadProc**](camthread-threadproc.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="2a94b-106">This method implements the pure virtual [**CAMThread::ThreadProc**](camthread-threadproc.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a94b-107">語法</span><span class="sxs-lookup"><span data-stu-id="2a94b-107">Syntax</span></span>


```C++
virtual DWORD ThreadProc();
```



## <a name="parameters"></a><span data-ttu-id="2a94b-108">參數</span><span class="sxs-lookup"><span data-stu-id="2a94b-108">Parameters</span></span>

<span data-ttu-id="2a94b-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2a94b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2a94b-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="2a94b-110">Return value</span></span>

<span data-ttu-id="2a94b-111">如果執行緒已成功完成，則傳回0，否則會傳回1。</span><span class="sxs-lookup"><span data-stu-id="2a94b-111">Returns 0 if the thread completed successfully or 1 otherwise.</span></span> <span data-ttu-id="2a94b-112">如果傳回值為1，可能仍會配置執行緒的資源。</span><span class="sxs-lookup"><span data-stu-id="2a94b-112">If the return value is 1, the thread's resources might still be allocated.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a94b-113">備註</span><span class="sxs-lookup"><span data-stu-id="2a94b-113">Remarks</span></span>

<span data-ttu-id="2a94b-114">這個方法會呼叫 [**CAMThread：： GetRequest**](camthread-getrequest.md) 方法，無限期等候執行緒要求。</span><span class="sxs-lookup"><span data-stu-id="2a94b-114">This method waits indefinitely for thread requests, by calling the [**CAMThread::GetRequest**](camthread-getrequest.md) method.</span></span> <span data-ttu-id="2a94b-115">如果它收到 [**CSourceStream：： Run**](csourcestream-run.md) 或 [**CSourceStream：:P ause**](csourcestream-pause.md) 要求，它會呼叫 [**CSourceStream：:D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="2a94b-115">If it receives a [**CSourceStream::Run**](csourcestream-run.md) or [**CSourceStream::Pause**](csourcestream-pause.md) request, it calls the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span> <span data-ttu-id="2a94b-116">**DoBufferProcessingLoop** 方法會推送資料，直到收到 [**CSourceStream：： Stop**](csourcestream-stop.md)要求為止。</span><span class="sxs-lookup"><span data-stu-id="2a94b-116">The **DoBufferProcessingLoop** method pushes data until it receives a [**CSourceStream::Stop**](csourcestream-stop.md) request.</span></span> <span data-ttu-id="2a94b-117">執行緒程式會在收到 [**CSourceStream：： Exit**](csourcestream-exit.md) 要求時結束。</span><span class="sxs-lookup"><span data-stu-id="2a94b-117">The thread procedure exits when it receives a [**CSourceStream::Exit**](csourcestream-exit.md) request.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a94b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a94b-118">Requirements</span></span>



| <span data-ttu-id="2a94b-119">需求</span><span class="sxs-lookup"><span data-stu-id="2a94b-119">Requirement</span></span> | <span data-ttu-id="2a94b-120">值</span><span class="sxs-lookup"><span data-stu-id="2a94b-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a94b-121">標頭</span><span class="sxs-lookup"><span data-stu-id="2a94b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2a94b-122"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="2a94b-122"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="2a94b-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="2a94b-123">Library</span></span><br/> | <dl> <span data-ttu-id="2a94b-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2a94b-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a94b-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a94b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a94b-126">**CSourceStream 類別**</span><span class="sxs-lookup"><span data-stu-id="2a94b-126">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




