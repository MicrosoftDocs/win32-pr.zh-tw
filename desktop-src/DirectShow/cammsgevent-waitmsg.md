---
description: WaitMsg 方法會在分派傳送的訊息時，等候事件收到信號。
ms.assetid: 5cab98ca-f9f3-4c7c-9ce2-8e16109d8fbb
title: 'CAMMsgEvent. WaitMsg 方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.WaitMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9622e962f130a082a5c1206367f4850cebb6ce02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999190"
---
# <a name="cammsgeventwaitmsg-method"></a><span data-ttu-id="9cc17-103">CAMMsgEvent. WaitMsg 方法</span><span class="sxs-lookup"><span data-stu-id="9cc17-103">CAMMsgEvent.WaitMsg method</span></span>

<span data-ttu-id="9cc17-104">`WaitMsg`方法會在分派傳送的訊息時，等候事件收到信號。</span><span class="sxs-lookup"><span data-stu-id="9cc17-104">The `WaitMsg` method waits for the event to be signaled, while dispatching sent messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cc17-105">語法</span><span class="sxs-lookup"><span data-stu-id="9cc17-105">Syntax</span></span>


```C++
BOOL WaitMsg(
   DWORD dwTimeOut = INFINITE
);
```



## <a name="parameters"></a><span data-ttu-id="9cc17-106">參數</span><span class="sxs-lookup"><span data-stu-id="9cc17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cc17-107">*dwTimeOut*</span><span class="sxs-lookup"><span data-stu-id="9cc17-107">*dwTimeOut*</span></span> 
</dt> <dd>

<span data-ttu-id="9cc17-108">選擇性超時值（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9cc17-108">Optional time-out value, in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cc17-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="9cc17-109">Return value</span></span>

<span data-ttu-id="9cc17-110">如果事件已收到信號，則傳回 **TRUE** ; 如果發生超時，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="9cc17-110">Returns **TRUE** if the event is signaled, or **FALSE** if the time-out occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cc17-111">備註</span><span class="sxs-lookup"><span data-stu-id="9cc17-111">Remarks</span></span>

<span data-ttu-id="9cc17-112">這個方法會呼叫 PeekMessage 函數來處理訊息。</span><span class="sxs-lookup"><span data-stu-id="9cc17-112">This method calls the PeekMessage function to process messages.</span></span> <span data-ttu-id="9cc17-113">如果您的執行緒需要在等候事件時處理訊息，請呼叫這個方法，而不是 [**CAMEvent：： Wait**](camevent-wait.md) 。</span><span class="sxs-lookup"><span data-stu-id="9cc17-113">Call this method instead of [**CAMEvent::Wait**](camevent-wait.md) if your thread needs to process messages while waiting for an event.</span></span> <span data-ttu-id="9cc17-114">如果執行緒沒有處理訊息，而另一個執行緒傳送訊息，則可能會發生鎖死。</span><span class="sxs-lookup"><span data-stu-id="9cc17-114">If the thread does not process messages and another thread sends a message, deadlock could occur.</span></span>

<span data-ttu-id="9cc17-115">例如，假設您建立執行緒，然後封鎖直到執行緒初始化為止。</span><span class="sxs-lookup"><span data-stu-id="9cc17-115">For example, suppose you create a thread and then block until the thread initializes.</span></span> <span data-ttu-id="9cc17-116">如果執行緒藉由呼叫 SendMessage 函式，將訊息傳送至您的視窗，則會產生鎖死。</span><span class="sxs-lookup"><span data-stu-id="9cc17-116">If the thread sends a message to your window by calling the SendMessage function, it will result in a deadlock.</span></span> <span data-ttu-id="9cc17-117">這是因為在處理訊息之前，SendMessage 不會傳回。</span><span class="sxs-lookup"><span data-stu-id="9cc17-117">This is because SendMessage does not return until the message has been processed.</span></span> <span data-ttu-id="9cc17-118">呼叫 WaitMsg 可讓 SendMessage 呼叫傳回，防止鎖死。</span><span class="sxs-lookup"><span data-stu-id="9cc17-118">Calling WaitMsg allows the SendMessage call to return, preventing the deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cc17-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="9cc17-119">Requirements</span></span>



| <span data-ttu-id="9cc17-120">需求</span><span class="sxs-lookup"><span data-stu-id="9cc17-120">Requirement</span></span> | <span data-ttu-id="9cc17-121">值</span><span class="sxs-lookup"><span data-stu-id="9cc17-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cc17-122">標頭</span><span class="sxs-lookup"><span data-stu-id="9cc17-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9cc17-123"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9cc17-123"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9cc17-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="9cc17-124">Library</span></span><br/> | <dl> <span data-ttu-id="9cc17-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9cc17-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cc17-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9cc17-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cc17-127">**CAMMsgEvent 類別**</span><span class="sxs-lookup"><span data-stu-id="9cc17-127">**CAMMsgEvent Class**</span></span>](cammsgevent.md)
</dt> </dl>

 

 




