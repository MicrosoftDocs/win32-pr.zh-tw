---
description: 回復方法會回復要求。
ms.assetid: 90e91b99-6a1c-46a2-b83d-eba483f1832a
title: 'CAMThread. Reply 方法 (Wxutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Reply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e86e0bc0155e527aa11c26531ae5608e6828362
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995059"
---
# <a name="camthreadreply-method"></a><span data-ttu-id="e9fbb-103">CAMThread. Reply 方法</span><span class="sxs-lookup"><span data-stu-id="e9fbb-103">CAMThread.Reply method</span></span>

<span data-ttu-id="e9fbb-104">`Reply`方法會回復要求。</span><span class="sxs-lookup"><span data-stu-id="e9fbb-104">The `Reply` method replies to a request.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9fbb-105">語法</span><span class="sxs-lookup"><span data-stu-id="e9fbb-105">Syntax</span></span>


```C++
void Reply(
   DWORD dw
);
```



## <a name="parameters"></a><span data-ttu-id="e9fbb-106">參數</span><span class="sxs-lookup"><span data-stu-id="e9fbb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9fbb-107">*dw*</span><span class="sxs-lookup"><span data-stu-id="e9fbb-107">*dw*</span></span> 
</dt> <dd>

<span data-ttu-id="e9fbb-108">要在 [**CAMThread：： CallWorker**](camthread-callworker.md) 方法中傳回的值。</span><span class="sxs-lookup"><span data-stu-id="e9fbb-108">Value to return in the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9fbb-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="e9fbb-109">Return value</span></span>

<span data-ttu-id="e9fbb-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e9fbb-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9fbb-111">備註</span><span class="sxs-lookup"><span data-stu-id="e9fbb-111">Remarks</span></span>

<span data-ttu-id="e9fbb-112">CallWorker 方法會封鎖，直到呼叫這個方法為止。</span><span class="sxs-lookup"><span data-stu-id="e9fbb-112">The CallWorker method blocks until this method is called.</span></span> <span data-ttu-id="e9fbb-113">*Dw* 參數提供 CallWorker 的傳回值。</span><span class="sxs-lookup"><span data-stu-id="e9fbb-113">The *dw* parameter supplies the return value for CallWorker.</span></span> <span data-ttu-id="e9fbb-114">在您抓取要求之後，于執行緒程式中呼叫這個方法，以釋放要求的執行緒。</span><span class="sxs-lookup"><span data-stu-id="e9fbb-114">Call this method in your thread procedure after you retrieve a request, to release the requesting thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9fbb-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9fbb-115">Requirements</span></span>



| <span data-ttu-id="e9fbb-116">需求</span><span class="sxs-lookup"><span data-stu-id="e9fbb-116">Requirement</span></span> | <span data-ttu-id="e9fbb-117">值</span><span class="sxs-lookup"><span data-stu-id="e9fbb-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9fbb-118">標頭</span><span class="sxs-lookup"><span data-stu-id="e9fbb-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e9fbb-119"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e9fbb-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e9fbb-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="e9fbb-120">Library</span></span><br/> | <dl> <span data-ttu-id="e9fbb-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e9fbb-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9fbb-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9fbb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9fbb-123">**CAMThread 類別**</span><span class="sxs-lookup"><span data-stu-id="e9fbb-123">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




