---
description: 函式方法。
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
ms.openlocfilehash: b0b0a4dde858811a75347105b9fccd2f499c4faa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982650"
---
# <a name="camthreadcamthread-destructor"></a><span data-ttu-id="0e737-103">CAMThread. ~ CAMThread 的函式</span><span class="sxs-lookup"><span data-stu-id="0e737-103">CAMThread.~CAMThread destructor</span></span>

<span data-ttu-id="0e737-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="0e737-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e737-105">語法</span><span class="sxs-lookup"><span data-stu-id="0e737-105">Syntax</span></span>


```C++
virtual ~CAMThread();
```



## <a name="remarks"></a><span data-ttu-id="0e737-106">備註</span><span class="sxs-lookup"><span data-stu-id="0e737-106">Remarks</span></span>

<span data-ttu-id="0e737-107">此函式會呼叫 [**CAMThread：： Close**](camthread-close.md) 方法，這會等候執行緒結束。</span><span class="sxs-lookup"><span data-stu-id="0e737-107">The destructor calls the [**CAMThread::Close**](camthread-close.md) method, which waits for the thread to exit.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e737-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e737-108">Requirements</span></span>



| <span data-ttu-id="0e737-109">需求</span><span class="sxs-lookup"><span data-stu-id="0e737-109">Requirement</span></span> | <span data-ttu-id="0e737-110">值</span><span class="sxs-lookup"><span data-stu-id="0e737-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e737-111">標頭</span><span class="sxs-lookup"><span data-stu-id="0e737-111">Header</span></span><br/>  | <dl> <span data-ttu-id="0e737-112"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0e737-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0e737-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="0e737-113">Library</span></span><br/> | <dl> <span data-ttu-id="0e737-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0e737-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e737-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e737-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e737-116">**CAMThread 類別**</span><span class="sxs-lookup"><span data-stu-id="0e737-116">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




