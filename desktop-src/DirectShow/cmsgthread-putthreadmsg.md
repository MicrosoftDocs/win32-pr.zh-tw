---
description: 將背景工作執行緒執行的要求排在佇列中。
ms.assetid: a854f962-143d-4776-bf98-119d003867df
title: 'CMsgThread. PutThreadMsg 方法 (Msgthrd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.PutThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3445d9af4ec9c7abe6a4401e219fc305e254d555
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000911"
---
# <a name="cmsgthreadputthreadmsg-method"></a><span data-ttu-id="87250-103">CMsgThread. PutThreadMsg 方法</span><span class="sxs-lookup"><span data-stu-id="87250-103">CMsgThread.PutThreadMsg method</span></span>

<span data-ttu-id="87250-104">將背景工作執行緒執行的要求排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="87250-104">Queues a request for execution by the worker thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="87250-105">語法</span><span class="sxs-lookup"><span data-stu-id="87250-105">Syntax</span></span>


```C++
void PutThreadMsg(
   UINT     uMsg,
   DWORD    dwMsgFlags,
   LPVOID   lpMsgParam,
   CAMEvent *pEvent = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="87250-106">參數</span><span class="sxs-lookup"><span data-stu-id="87250-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87250-107">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="87250-107">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="87250-108">要求代碼。</span><span class="sxs-lookup"><span data-stu-id="87250-108">Request code.</span></span>

</dd> <dt>

<span data-ttu-id="87250-109">*dwMsgFlags*</span><span class="sxs-lookup"><span data-stu-id="87250-109">*dwMsgFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="87250-110">選擇性旗標參數。</span><span class="sxs-lookup"><span data-stu-id="87250-110">Optional flags parameter.</span></span>

</dd> <dt>

<span data-ttu-id="87250-111">*lpMsgParam*</span><span class="sxs-lookup"><span data-stu-id="87250-111">*lpMsgParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87250-112">包含額外參數或傳回值之資料區塊的選擇性指標。</span><span class="sxs-lookup"><span data-stu-id="87250-112">Optional pointer to a data block containing additional parameters or return values.</span></span> <span data-ttu-id="87250-113">必須是靜態或堆積配置，而不是自動。</span><span class="sxs-lookup"><span data-stu-id="87250-113">Must be statically or heap-allocated and not automatic.</span></span>

</dd> <dt>

<span data-ttu-id="87250-114">*pEvent*</span><span class="sxs-lookup"><span data-stu-id="87250-114">*pEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="87250-115">事件物件的選擇性指標，會在完成時收到信號。</span><span class="sxs-lookup"><span data-stu-id="87250-115">Optional pointer to an event object to be signaled upon completion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87250-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="87250-116">Return value</span></span>

<span data-ttu-id="87250-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="87250-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="87250-118">備註</span><span class="sxs-lookup"><span data-stu-id="87250-118">Remarks</span></span>

<span data-ttu-id="87250-119">此成員函式會將背景工作執行緒執行的要求排到佇列。</span><span class="sxs-lookup"><span data-stu-id="87250-119">This member function queues a request for execution by the worker thread.</span></span> <span data-ttu-id="87250-120">此成員函式的參數將會在 [**CMsg**](cmsg.md) 物件中排入佇列 (，) 並傳遞給背景工作執行緒的 [**CMsgThread：： ThreadMessageProc**](cmsgthread-threadmessageproc.md) 成員函式。</span><span class="sxs-lookup"><span data-stu-id="87250-120">The parameters of this member function will be queued (in a [**CMsg**](cmsg.md) object) and passed to the [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) member function of the worker thread.</span></span> <span data-ttu-id="87250-121">此成員函式會在將要求排入佇列之後立即傳回，而且不會等候執行緒完成要求。</span><span class="sxs-lookup"><span data-stu-id="87250-121">This member function returns immediately after queuing the request and does not wait for the thread to fulfill the request.</span></span> <span data-ttu-id="87250-122">衍生類別的 **CMsgThread：： ThreadMessageProc** 成員函式會定義四個參數。</span><span class="sxs-lookup"><span data-stu-id="87250-122">The **CMsgThread::ThreadMessageProc** member function of the derived class defines the four parameters.</span></span>

<span data-ttu-id="87250-123">這個成員函式會使用多執行緒安全清單，因此可以安全地從不同的執行緒呼叫這個成員函式。</span><span class="sxs-lookup"><span data-stu-id="87250-123">This member function uses a multithread safe list, so multiple calls to this member function from different threads can be made safely.</span></span>

## <a name="requirements"></a><span data-ttu-id="87250-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="87250-124">Requirements</span></span>



| <span data-ttu-id="87250-125">需求</span><span class="sxs-lookup"><span data-stu-id="87250-125">Requirement</span></span> | <span data-ttu-id="87250-126">值</span><span class="sxs-lookup"><span data-stu-id="87250-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87250-127">標頭</span><span class="sxs-lookup"><span data-stu-id="87250-127">Header</span></span><br/>  | <dl> <span data-ttu-id="87250-128"><dt>Msgthrd (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="87250-128"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="87250-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="87250-129">Library</span></span><br/> | <dl> <span data-ttu-id="87250-130"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="87250-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87250-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87250-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87250-132">**CMsgThread 類別**</span><span class="sxs-lookup"><span data-stu-id="87250-132">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




