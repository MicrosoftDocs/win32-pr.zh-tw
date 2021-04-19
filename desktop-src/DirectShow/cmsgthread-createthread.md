---
description: 建立執行緒。
ms.assetid: 40785522-dc6e-41af-8b27-9e8875a0dd84
title: 'CMsgThread. CreateThread 方法 (Msgthrd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CreateThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8951995de18158fe4d1e5f84b1d98da701067ab6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987154"
---
# <a name="cmsgthreadcreatethread-method"></a><span data-ttu-id="bbd44-103">CMsgThread. CreateThread 方法</span><span class="sxs-lookup"><span data-stu-id="bbd44-103">CMsgThread.CreateThread method</span></span>

<span data-ttu-id="bbd44-104">建立執行緒。</span><span class="sxs-lookup"><span data-stu-id="bbd44-104">Creates a thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbd44-105">語法</span><span class="sxs-lookup"><span data-stu-id="bbd44-105">Syntax</span></span>


```C++
BOOL CreateThread();
```



## <a name="parameters"></a><span data-ttu-id="bbd44-106">參數</span><span class="sxs-lookup"><span data-stu-id="bbd44-106">Parameters</span></span>

<span data-ttu-id="bbd44-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="bbd44-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bbd44-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="bbd44-108">Return value</span></span>

<span data-ttu-id="bbd44-109">傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="bbd44-109">Returns one of the following values.</span></span>



| <span data-ttu-id="bbd44-110">傳回碼</span><span class="sxs-lookup"><span data-stu-id="bbd44-110">Return code</span></span>                                                                              | <span data-ttu-id="bbd44-111">Description</span><span class="sxs-lookup"><span data-stu-id="bbd44-111">Description</span></span>                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="bbd44-112"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="bbd44-112"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>  | <span data-ttu-id="bbd44-113">已成功建立執行緒。</span><span class="sxs-lookup"><span data-stu-id="bbd44-113">Thread was successfully created.</span></span><br/>     |
| <dl> <span data-ttu-id="bbd44-114"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="bbd44-114"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="bbd44-115">未成功建立執行緒。</span><span class="sxs-lookup"><span data-stu-id="bbd44-115">Thread was not successfully created.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bbd44-116">備註</span><span class="sxs-lookup"><span data-stu-id="bbd44-116">Remarks</span></span>

<span data-ttu-id="bbd44-117">執行緒將會透過 [**CMsgThread：:P utthreadmsg**](cmsgthread-putthreadmsg.md)) 成員函式來迴圈、封鎖直到要求排入佇列 (，然後使用每個訊息來呼叫 [**CMsgThread：： ThreadMessageProc**](cmsgthread-threadmessageproc.md) 成員函式。</span><span class="sxs-lookup"><span data-stu-id="bbd44-117">The thread will loop, blocking until a request is queued (through the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function) and then calling the [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) member function with each message.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbd44-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="bbd44-118">Requirements</span></span>



| <span data-ttu-id="bbd44-119">需求</span><span class="sxs-lookup"><span data-stu-id="bbd44-119">Requirement</span></span> | <span data-ttu-id="bbd44-120">值</span><span class="sxs-lookup"><span data-stu-id="bbd44-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbd44-121">標頭</span><span class="sxs-lookup"><span data-stu-id="bbd44-121">Header</span></span><br/>  | <dl> <span data-ttu-id="bbd44-122"><dt>Msgthrd (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="bbd44-122"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bbd44-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="bbd44-123">Library</span></span><br/> | <dl> <span data-ttu-id="bbd44-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="bbd44-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbd44-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bbd44-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbd44-126">**CMsgThread 類別**</span><span class="sxs-lookup"><span data-stu-id="bbd44-126">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




