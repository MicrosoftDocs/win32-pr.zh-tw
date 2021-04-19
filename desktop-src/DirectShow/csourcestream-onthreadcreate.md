---
description: 初始化串流執行緒時，會呼叫 OnThreadCreate 方法。
ms.assetid: eeaa0d12-3185-4c97-b481-fc420cfc0897
title: 'CSourceStream. OnThreadCreate 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadCreate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5ae3c210ca81eafa1951fc51301eaf50491357f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992589"
---
# <a name="csourcestreamonthreadcreate-method"></a><span data-ttu-id="b1231-103">CSourceStream. OnThreadCreate 方法</span><span class="sxs-lookup"><span data-stu-id="b1231-103">CSourceStream.OnThreadCreate method</span></span>

<span data-ttu-id="b1231-104">`OnThreadCreate`初始化串流執行緒時，會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="b1231-104">The `OnThreadCreate` method is called when the streaming thread is initialized.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1231-105">語法</span><span class="sxs-lookup"><span data-stu-id="b1231-105">Syntax</span></span>


```C++
virtual HRESULT OnThreadCreate();
```



## <a name="parameters"></a><span data-ttu-id="b1231-106">參數</span><span class="sxs-lookup"><span data-stu-id="b1231-106">Parameters</span></span>

<span data-ttu-id="b1231-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b1231-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b1231-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="b1231-108">Return value</span></span>

<span data-ttu-id="b1231-109">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="b1231-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1231-110">備註</span><span class="sxs-lookup"><span data-stu-id="b1231-110">Remarks</span></span>

<span data-ttu-id="b1231-111">Thread 程式 [**CSourceStream：： ThreadProc**](csourcestream-threadproc.md)會在第一次收到 [**CSourceStream：： Init**](csourcestream-init.md) 要求時呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="b1231-111">The thread procedure, [**CSourceStream::ThreadProc**](csourcestream-threadproc.md), calls this method when it first receives a [**CSourceStream::Init**](csourcestream-init.md) request.</span></span> <span data-ttu-id="b1231-112">方法不會在基類中執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="b1231-112">The method does nothing in the base class.</span></span> <span data-ttu-id="b1231-113">衍生類別可以覆寫這個方法，以執行執行緒初始化。</span><span class="sxs-lookup"><span data-stu-id="b1231-113">The derived class can override this method to perform thread initializations.</span></span> <span data-ttu-id="b1231-114">如果衍生類別傳回錯誤碼，執行緒就會結束併發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="b1231-114">If the derived class returns an error code, the thread exits with an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1231-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1231-115">Requirements</span></span>



| <span data-ttu-id="b1231-116">需求</span><span class="sxs-lookup"><span data-stu-id="b1231-116">Requirement</span></span> | <span data-ttu-id="b1231-117">值</span><span class="sxs-lookup"><span data-stu-id="b1231-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1231-118">標頭</span><span class="sxs-lookup"><span data-stu-id="b1231-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b1231-119"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="b1231-119"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b1231-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="b1231-120">Library</span></span><br/> | <dl> <span data-ttu-id="b1231-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b1231-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1231-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1231-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1231-123">**CSourceStream 類別**</span><span class="sxs-lookup"><span data-stu-id="b1231-123">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




