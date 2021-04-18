---
description: 使用 Microsoft Win32 SuspendThread 函式來暫止執行中線程的操作。
ms.assetid: 07d919a2-797d-47c3-83e3-c8e2d2b2cddd
title: 'CMsgThread. SuspendThread 方法 (Msgthrd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SuspendThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69190015104d712864965e757d82afbdcc852884
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996302"
---
# <a name="cmsgthreadsuspendthread-method"></a><span data-ttu-id="2781f-103">CMsgThread. SuspendThread 方法</span><span class="sxs-lookup"><span data-stu-id="2781f-103">CMsgThread.SuspendThread method</span></span>

<span data-ttu-id="2781f-104">使用 Microsoft Win32 **SuspendThread** 函式來暫止執行中線程的操作。</span><span class="sxs-lookup"><span data-stu-id="2781f-104">Uses the Microsoft Win32 **SuspendThread** function to suspend the operation of a running thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="2781f-105">語法</span><span class="sxs-lookup"><span data-stu-id="2781f-105">Syntax</span></span>


```C++
DWORD SuspendThread();
```



## <a name="parameters"></a><span data-ttu-id="2781f-106">參數</span><span class="sxs-lookup"><span data-stu-id="2781f-106">Parameters</span></span>

<span data-ttu-id="2781f-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2781f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2781f-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="2781f-108">Return value</span></span>

<span data-ttu-id="2781f-109">如果成員函式成功，則傳回值為執行緒的先前暫止計數。</span><span class="sxs-lookup"><span data-stu-id="2781f-109">If the member function succeeds, the return value is the previous suspend count of the thread.</span></span> <span data-ttu-id="2781f-110">如果成員函式失敗，則傳回值為0xFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="2781f-110">If the member function fails, the return value is 0xFFFFFFFF.</span></span> <span data-ttu-id="2781f-111">若要取得延伸錯誤資訊，請呼叫 Microsoft Win32 **GetLastError** 函數。</span><span class="sxs-lookup"><span data-stu-id="2781f-111">To obtain extended error information, call the Microsoft Win32 **GetLastError** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="2781f-112">備註</span><span class="sxs-lookup"><span data-stu-id="2781f-112">Remarks</span></span>

<span data-ttu-id="2781f-113">用戶端執行緒會呼叫這個成員函式，以暫止工作者執行緒的作業。</span><span class="sxs-lookup"><span data-stu-id="2781f-113">The client thread calls this member function to suspend the operation of the worker thread.</span></span> <span data-ttu-id="2781f-114">背景工作執行緒會保持暫止狀態，而且在呼叫 [**CMsgThread：： ResumeThread**](cmsgthread-resumethread.md) 成員函式之前，將不會執行。</span><span class="sxs-lookup"><span data-stu-id="2781f-114">The worker thread remains suspended and will not execute until an additional call to the [**CMsgThread::ResumeThread**](cmsgthread-resumethread.md) member function is made.</span></span>

## <a name="requirements"></a><span data-ttu-id="2781f-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="2781f-115">Requirements</span></span>



| <span data-ttu-id="2781f-116">需求</span><span class="sxs-lookup"><span data-stu-id="2781f-116">Requirement</span></span> | <span data-ttu-id="2781f-117">值</span><span class="sxs-lookup"><span data-stu-id="2781f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2781f-118">標頭</span><span class="sxs-lookup"><span data-stu-id="2781f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2781f-119"><dt>Msgthrd (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2781f-119"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2781f-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="2781f-120">Library</span></span><br/> | <dl> <span data-ttu-id="2781f-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2781f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2781f-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2781f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2781f-123">**CMsgThread 類別**</span><span class="sxs-lookup"><span data-stu-id="2781f-123">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




