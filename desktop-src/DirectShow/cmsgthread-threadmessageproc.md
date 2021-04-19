---
description: 處理要求。 這是單純的虛擬成員函式。
ms.assetid: ffdbc287-ca17-44e4-b00a-d72a2367f510
title: 'CMsgThread. ThreadMessageProc 方法 (Msgthrd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ThreadMessageProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf47eb63a6f9d8fe4921985bb64567de6678b44c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990700"
---
# <a name="cmsgthreadthreadmessageproc-method"></a><span data-ttu-id="68739-104">CMsgThread. ThreadMessageProc 方法</span><span class="sxs-lookup"><span data-stu-id="68739-104">CMsgThread.ThreadMessageProc method</span></span>

<span data-ttu-id="68739-105">處理要求。</span><span class="sxs-lookup"><span data-stu-id="68739-105">Processes requests.</span></span> <span data-ttu-id="68739-106">這是單純的虛擬成員函式。</span><span class="sxs-lookup"><span data-stu-id="68739-106">This is a pure virtual member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="68739-107">語法</span><span class="sxs-lookup"><span data-stu-id="68739-107">Syntax</span></span>


```C++
virtual LRESULT ThreadMessageProc(
   UINT     uMsg,
   DWORD    dwFlags,
   LPVOID   lpParam,
   CAMEvent *pEvent
);
```



## <a name="parameters"></a><span data-ttu-id="68739-108">參數</span><span class="sxs-lookup"><span data-stu-id="68739-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68739-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="68739-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="68739-110">要求代碼。</span><span class="sxs-lookup"><span data-stu-id="68739-110">Request code.</span></span>

</dd> <dt>

<span data-ttu-id="68739-111">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="68739-111">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="68739-112">要要求的選擇性旗標參數。</span><span class="sxs-lookup"><span data-stu-id="68739-112">Optional flag parameter to request.</span></span>

</dd> <dt>

<span data-ttu-id="68739-113">*lpParam*</span><span class="sxs-lookup"><span data-stu-id="68739-113">*lpParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68739-114">額外資料或傳回資料區塊的選擇性指標。</span><span class="sxs-lookup"><span data-stu-id="68739-114">Optional pointer to extra data or a return data block.</span></span>

</dd> <dt>

<span data-ttu-id="68739-115">*pEvent*</span><span class="sxs-lookup"><span data-stu-id="68739-115">*pEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="68739-116">事件物件的選擇性指標。</span><span class="sxs-lookup"><span data-stu-id="68739-116">Optional pointer to an event object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68739-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="68739-117">Return value</span></span>

<span data-ttu-id="68739-118">任何非零傳回都會導致執行緒結束。</span><span class="sxs-lookup"><span data-stu-id="68739-118">Any nonzero return causes the thread to exit.</span></span> <span data-ttu-id="68739-119">除非最近處理過結束要求，否則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="68739-119">Returns zero unless an exit request has been processed recently.</span></span>

## <a name="remarks"></a><span data-ttu-id="68739-120">備註</span><span class="sxs-lookup"><span data-stu-id="68739-120">Remarks</span></span>

<span data-ttu-id="68739-121">您必須在衍生類別中覆寫此純虛擬函式。</span><span class="sxs-lookup"><span data-stu-id="68739-121">This pure virtual function must be overridden in your derived class.</span></span> <span data-ttu-id="68739-122">針對 [**CMsgThread：:P utthreadmsg**](cmsgthread-putthreadmsg.md) 成員函式的呼叫所排入佇列的每個要求，都會呼叫此函式一次。</span><span class="sxs-lookup"><span data-stu-id="68739-122">It will be called once for each request queued by a call to the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function.</span></span>

<span data-ttu-id="68739-123">成員函式會定義四個參數。</span><span class="sxs-lookup"><span data-stu-id="68739-123">The member function defines the four parameters.</span></span> <span data-ttu-id="68739-124">通常，使用 *uMsg* 參數來表示要求，而其他三個參數將會是選擇性的額外參數。</span><span class="sxs-lookup"><span data-stu-id="68739-124">Typically, use the *uMsg* parameter to indicate the request, and the other three parameters will be optional additional parameters.</span></span> <span data-ttu-id="68739-125">如果您的應用程式需要，呼叫應用程式可以在 *pEvent* 參數中提供 [**CAMEvent**](camevent.md)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="68739-125">The calling application can supply a pointer to a [**CAMEvent**](camevent.md) object in the *pEvent* parameter if your application requires it.</span></span> <span data-ttu-id="68739-126">您必須在處理事件之後設定這個事件，方法是使用如下的運算式：</span><span class="sxs-lookup"><span data-stu-id="68739-126">You must set this event after processing the event by using an expression such as:</span></span>


```C++
pEvent->SetEvent
```



<span data-ttu-id="68739-127">您必須在旁邊設定一個要求碼，告知工作者執行緒結束。</span><span class="sxs-lookup"><span data-stu-id="68739-127">One request code must be set aside to tell the worker thread to exit.</span></span> <span data-ttu-id="68739-128">收到此要求時，從這個成員函式傳回1。</span><span class="sxs-lookup"><span data-stu-id="68739-128">Upon receiving this request, return 1 from this member function.</span></span> <span data-ttu-id="68739-129">如果您不想讓背景工作執行緒結束，則傳回0。</span><span class="sxs-lookup"><span data-stu-id="68739-129">Return 0 if you do not want the worker thread to exit.</span></span>

## <a name="requirements"></a><span data-ttu-id="68739-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="68739-130">Requirements</span></span>



| <span data-ttu-id="68739-131">需求</span><span class="sxs-lookup"><span data-stu-id="68739-131">Requirement</span></span> | <span data-ttu-id="68739-132">值</span><span class="sxs-lookup"><span data-stu-id="68739-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68739-133">標頭</span><span class="sxs-lookup"><span data-stu-id="68739-133">Header</span></span><br/>  | <dl> <span data-ttu-id="68739-134"><dt>Msgthrd (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="68739-134"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="68739-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="68739-135">Library</span></span><br/> | <dl> <span data-ttu-id="68739-136"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="68739-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68739-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68739-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68739-138">**CMsgThread 類別**</span><span class="sxs-lookup"><span data-stu-id="68739-138">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




