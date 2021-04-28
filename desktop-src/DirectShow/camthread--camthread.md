---
description: CAMThread. ~ CAMThread 的函式-函式方法。
ms.assetid: eed6c566-8a03-4a97-9d99-8e500ce2954c
title: 'CAMThread. ~ CAMThread (Wxutil 的函式) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.~CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 84a40205fc93677f20256676ad09a18357d46acb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096436"
---
# <a name="camthreadcamthread-destructor"></a><span data-ttu-id="f2299-103">CAMThread. ~ CAMThread 的函式</span><span class="sxs-lookup"><span data-stu-id="f2299-103">CAMThread.~CAMThread destructor</span></span>

<span data-ttu-id="f2299-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="f2299-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2299-105">語法</span><span class="sxs-lookup"><span data-stu-id="f2299-105">Syntax</span></span>


```C++
virtual ~CAMThread();
```



## <a name="remarks"></a><span data-ttu-id="f2299-106">備註</span><span class="sxs-lookup"><span data-stu-id="f2299-106">Remarks</span></span>

<span data-ttu-id="f2299-107">此函式會呼叫 [**CAMThread：： Close**](camthread-close.md) 方法，這會等候執行緒結束。</span><span class="sxs-lookup"><span data-stu-id="f2299-107">The destructor calls the [**CAMThread::Close**](camthread-close.md) method, which waits for the thread to exit.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2299-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2299-108">Requirements</span></span>



| <span data-ttu-id="f2299-109">需求</span><span class="sxs-lookup"><span data-stu-id="f2299-109">Requirement</span></span> | <span data-ttu-id="f2299-110">值</span><span class="sxs-lookup"><span data-stu-id="f2299-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2299-111">標頭</span><span class="sxs-lookup"><span data-stu-id="f2299-111">Header</span></span><br/>  | <dl> <span data-ttu-id="f2299-112"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f2299-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f2299-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="f2299-113">Library</span></span><br/> | <dl> <span data-ttu-id="f2299-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f2299-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2299-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2299-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2299-116">**CAMThread 類別**</span><span class="sxs-lookup"><span data-stu-id="f2299-116">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




