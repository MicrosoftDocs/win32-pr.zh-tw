---
description: ThreadProc 方法是執行緒程式。
ms.assetid: 2d991f15-afea-4843-bc68-aeb5ca69d28b
title: 'CAMThread. ThreadProc 方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7081a7f7e1cd84a6bf8d482aa7dddf7a48b39f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990725"
---
# <a name="camthreadthreadproc-method"></a><span data-ttu-id="bd19d-103">CAMThread. ThreadProc 方法</span><span class="sxs-lookup"><span data-stu-id="bd19d-103">CAMThread.ThreadProc method</span></span>

<span data-ttu-id="bd19d-104">`ThreadProc`方法是執行緒程式。</span><span class="sxs-lookup"><span data-stu-id="bd19d-104">The `ThreadProc` method is the thread procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd19d-105">語法</span><span class="sxs-lookup"><span data-stu-id="bd19d-105">Syntax</span></span>


```C++
virtual DWORD ThreadProc() = 0;
```



## <a name="parameters"></a><span data-ttu-id="bd19d-106">參數</span><span class="sxs-lookup"><span data-stu-id="bd19d-106">Parameters</span></span>

<span data-ttu-id="bd19d-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="bd19d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bd19d-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="bd19d-108">Return value</span></span>

<span data-ttu-id="bd19d-109">傳回由衍生類別定義其意義的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="bd19d-109">Returns a **DWORD** value whose meaning is defined by the derived class.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd19d-110">備註</span><span class="sxs-lookup"><span data-stu-id="bd19d-110">Remarks</span></span>

<span data-ttu-id="bd19d-111">這是單純的虛擬方法。</span><span class="sxs-lookup"><span data-stu-id="bd19d-111">This is a pure virtual method.</span></span> <span data-ttu-id="bd19d-112">在您的衍生類別中執行此方法，以提供執行緒程式。</span><span class="sxs-lookup"><span data-stu-id="bd19d-112">Implement this method in your derived class to supply a thread procedure.</span></span> <span data-ttu-id="bd19d-113">當 [**CAMThread：： Create**](camthread-create.md) 方法建立執行緒時，它會提供 [**CAMThread：： InitialThreadProc**](camthread-initialthreadproc.md) 方法的位址，然後再呼叫您的 ThreadProc 方法。</span><span class="sxs-lookup"><span data-stu-id="bd19d-113">When the [**CAMThread::Create**](camthread-create.md) method creates a thread, it gives the address of the [**CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) method, which in turn calls your ThreadProc method.</span></span>

<span data-ttu-id="bd19d-114">一般來說，您的 ThreadProc 方法會進入迴圈，藉由呼叫 [**CAMThread：： GetRequest**](camthread-getrequest.md) 或 [**CAMThread：： CheckRequest**](camthread-checkrequest.md) 方法) 和處理資料來抓取要求 (。</span><span class="sxs-lookup"><span data-stu-id="bd19d-114">Typically, your ThreadProc method will enter a loop that retrieves requests (by calling the [**CAMThread::GetRequest**](camthread-getrequest.md) or [**CAMThread::CheckRequest**](camthread-checkrequest.md) methods) and processes data.</span></span>

<span data-ttu-id="bd19d-115">當此方法傳回時，就會結束執行緒。</span><span class="sxs-lookup"><span data-stu-id="bd19d-115">When this method returns, the thread exits.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd19d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd19d-116">Requirements</span></span>



| <span data-ttu-id="bd19d-117">需求</span><span class="sxs-lookup"><span data-stu-id="bd19d-117">Requirement</span></span> | <span data-ttu-id="bd19d-118">值</span><span class="sxs-lookup"><span data-stu-id="bd19d-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd19d-119">標頭</span><span class="sxs-lookup"><span data-stu-id="bd19d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="bd19d-120"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="bd19d-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="bd19d-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="bd19d-121">Library</span></span><br/> | <dl> <span data-ttu-id="bd19d-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="bd19d-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd19d-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd19d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd19d-124">**CAMThread 類別**</span><span class="sxs-lookup"><span data-stu-id="bd19d-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




