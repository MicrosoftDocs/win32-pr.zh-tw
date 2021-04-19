---
description: 封鎖直到執行緒結束為止。
ms.assetid: 1ee547b5-cd73-4ce8-8e66-c2062714d0f0
title: 'CMsgThread. WaitForThreadExit 方法 (Msgthrd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.WaitForThreadExit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8b48573c4297a2d5d5d008eba88fd8ea437333c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990291"
---
# <a name="cmsgthreadwaitforthreadexit-method"></a><span data-ttu-id="87d9f-103">CMsgThread. WaitForThreadExit 方法</span><span class="sxs-lookup"><span data-stu-id="87d9f-103">CMsgThread.WaitForThreadExit method</span></span>

<span data-ttu-id="87d9f-104">封鎖直到執行緒結束為止。</span><span class="sxs-lookup"><span data-stu-id="87d9f-104">Blocks until the thread exits.</span></span>

## <a name="syntax"></a><span data-ttu-id="87d9f-105">語法</span><span class="sxs-lookup"><span data-stu-id="87d9f-105">Syntax</span></span>


```C++
BOOL WaitForThreadExit(
   LPDWORD lpdwExitCode
);
```



## <a name="parameters"></a><span data-ttu-id="87d9f-106">參數</span><span class="sxs-lookup"><span data-stu-id="87d9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87d9f-107">*lpdwExitCode*</span><span class="sxs-lookup"><span data-stu-id="87d9f-107">*lpdwExitCode*</span></span> 
</dt> <dd>

<span data-ttu-id="87d9f-108">執行緒所傳回之結束代碼的指標。</span><span class="sxs-lookup"><span data-stu-id="87d9f-108">Pointer to the exit code returned by the thread.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87d9f-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="87d9f-109">Return value</span></span>

<span data-ttu-id="87d9f-110">傳回 **TRUE** 或 **FALSE**，其意義取決於提供覆寫 [**CMsgThread：： ThreadMessageProc**](cmsgthread-threadmessageproc.md) 成員函式和呼叫成員函式的類別。</span><span class="sxs-lookup"><span data-stu-id="87d9f-110">Returns either **TRUE** or **FALSE**, the meaning of which is determined by the class supplying the overridden [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) member function and the calling member function.</span></span>

## <a name="remarks"></a><span data-ttu-id="87d9f-111">備註</span><span class="sxs-lookup"><span data-stu-id="87d9f-111">Remarks</span></span>

<span data-ttu-id="87d9f-112">在完成衍生類別的終結之前，請確定背景工作執行緒已完全結束：否則，在您的動態連結程式庫 (DLL) 從進程的位址空間卸載之後，執行緒仍可能會執行。</span><span class="sxs-lookup"><span data-stu-id="87d9f-112">Ensure that the worker thread has exited completely before completing the destruction of your derived class; otherwise, the thread might still execute after your dynamic-link library (DLL) has been unloaded from the address space of the process.</span></span> <span data-ttu-id="87d9f-113">即使要結束的唯一指令是單一傳回指令，但這會造成例外狀況。</span><span class="sxs-lookup"><span data-stu-id="87d9f-113">Even if the only instruction left to exit is a single-return instruction, this would cause an exception.</span></span> <span data-ttu-id="87d9f-114">確保執行緒已結束的唯一可靠方法，是使用傳送至 [**CMsgThread：:P utthreadmsg**](cmsgthread-putthreadmsg.md)) 成員函式的私下協商 [**CMsg**](cmsg.md)物件，來指示執行緒結束 (，然後再呼叫這個成員函式。</span><span class="sxs-lookup"><span data-stu-id="87d9f-114">The only reliable way to ensure that the thread has exited is to signal the thread to exit (using a privately negotiated [**CMsg**](cmsg.md) object sent to the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function) and then call this member function.</span></span> <span data-ttu-id="87d9f-115">您應該在衍生類別的函式中進行這項作業。</span><span class="sxs-lookup"><span data-stu-id="87d9f-115">You should do this in the destructor for your derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="87d9f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="87d9f-116">Requirements</span></span>



| <span data-ttu-id="87d9f-117">需求</span><span class="sxs-lookup"><span data-stu-id="87d9f-117">Requirement</span></span> | <span data-ttu-id="87d9f-118">值</span><span class="sxs-lookup"><span data-stu-id="87d9f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87d9f-119">標頭</span><span class="sxs-lookup"><span data-stu-id="87d9f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="87d9f-120"><dt>Msgthrd (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="87d9f-120"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="87d9f-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="87d9f-121">Library</span></span><br/> | <dl> <span data-ttu-id="87d9f-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="87d9f-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87d9f-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87d9f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87d9f-124">**CMsgThread 類別**</span><span class="sxs-lookup"><span data-stu-id="87d9f-124">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




