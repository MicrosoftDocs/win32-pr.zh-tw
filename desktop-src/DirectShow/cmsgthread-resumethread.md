---
description: 使用 Microsoft Win32 ResumeThread 函式，在前一次呼叫 CMsgThread：： SuspendThread 成員函式之後，繼續執行背景工作執行緒的操作。
ms.assetid: 5c94a079-5c74-4024-8fb0-71c7ef9c7e73
title: 'CMsgThread. ResumeThread 方法 (Msgthrd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ResumeThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e0a20bb60f4a10a06ef50f58c449496cae8050d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994897"
---
# <a name="cmsgthreadresumethread-method"></a><span data-ttu-id="dfe0c-103">CMsgThread. ResumeThread 方法</span><span class="sxs-lookup"><span data-stu-id="dfe0c-103">CMsgThread.ResumeThread method</span></span>

<span data-ttu-id="dfe0c-104">使用 Microsoft Win32 **ResumeThread** 函式，在前一次呼叫 [**CMsgThread：： SuspendThread**](cmsgthread-suspendthread.md) 成員函式之後，繼續執行背景工作執行緒的操作。</span><span class="sxs-lookup"><span data-stu-id="dfe0c-104">Uses the Microsoft Win32 **ResumeThread** function to continue the operation of the worker thread after a previous call to the [**CMsgThread::SuspendThread**](cmsgthread-suspendthread.md) member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfe0c-105">語法</span><span class="sxs-lookup"><span data-stu-id="dfe0c-105">Syntax</span></span>


```C++
DWORD ResumeThread();
```



## <a name="parameters"></a><span data-ttu-id="dfe0c-106">參數</span><span class="sxs-lookup"><span data-stu-id="dfe0c-106">Parameters</span></span>

<span data-ttu-id="dfe0c-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="dfe0c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dfe0c-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="dfe0c-108">Return value</span></span>

<span data-ttu-id="dfe0c-109">如果成員函式成功，則傳回值為執行緒的先前暫止計數。</span><span class="sxs-lookup"><span data-stu-id="dfe0c-109">If the member function succeeds, the return value is the previous suspend count of the thread.</span></span> <span data-ttu-id="dfe0c-110">如果成員函式失敗，則傳回值為0xFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="dfe0c-110">If the member function fails, the return value is 0xFFFFFFFF.</span></span> <span data-ttu-id="dfe0c-111">若要取得延伸錯誤資訊，請呼叫 Microsoft Win32 **GetLastError** 函數。</span><span class="sxs-lookup"><span data-stu-id="dfe0c-111">To obtain extended error information, call the Microsoft Win32 **GetLastError** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfe0c-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="dfe0c-112">Requirements</span></span>



| <span data-ttu-id="dfe0c-113">需求</span><span class="sxs-lookup"><span data-stu-id="dfe0c-113">Requirement</span></span> | <span data-ttu-id="dfe0c-114">值</span><span class="sxs-lookup"><span data-stu-id="dfe0c-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfe0c-115">標頭</span><span class="sxs-lookup"><span data-stu-id="dfe0c-115">Header</span></span><br/>  | <dl> <span data-ttu-id="dfe0c-116"><dt>Msgthrd (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="dfe0c-116"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dfe0c-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="dfe0c-117">Library</span></span><br/> | <dl> <span data-ttu-id="dfe0c-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="dfe0c-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfe0c-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dfe0c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfe0c-120">**CMsgThread 類別**</span><span class="sxs-lookup"><span data-stu-id="dfe0c-120">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




