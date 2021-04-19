---
description: 當串流執行緒即將結束時，會呼叫 OnThreadDestroy 方法。
ms.assetid: a484b6d2-bce6-4a42-9176-2a6ce374e28b
title: 'CSourceStream. OnThreadDestroy 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadDestroy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e7377ce11955d7121a33311d390464e042b98f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994987"
---
# <a name="csourcestreamonthreaddestroy-method"></a><span data-ttu-id="ed830-103">CSourceStream. OnThreadDestroy 方法</span><span class="sxs-lookup"><span data-stu-id="ed830-103">CSourceStream.OnThreadDestroy method</span></span>

<span data-ttu-id="ed830-104">`OnThreadDestroy`當串流執行緒即將結束時，會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="ed830-104">The `OnThreadDestroy` method is called when the streaming thread is about to exit.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed830-105">語法</span><span class="sxs-lookup"><span data-stu-id="ed830-105">Syntax</span></span>


```C++
virtual HRESULT OnThreadDestroy();
```



## <a name="parameters"></a><span data-ttu-id="ed830-106">參數</span><span class="sxs-lookup"><span data-stu-id="ed830-106">Parameters</span></span>

<span data-ttu-id="ed830-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="ed830-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ed830-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="ed830-108">Return value</span></span>

<span data-ttu-id="ed830-109">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="ed830-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed830-110">備註</span><span class="sxs-lookup"><span data-stu-id="ed830-110">Remarks</span></span>

<span data-ttu-id="ed830-111">Thread 程式 [**CSourceStream：： ThreadProc**](csourcestream-threadproc.md)會在結束之前呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="ed830-111">The thread procedure, [**CSourceStream::ThreadProc**](csourcestream-threadproc.md), calls this method before it exits.</span></span> <span data-ttu-id="ed830-112">方法不會在基類中執行任何動作;它可供衍生類別覆寫。</span><span class="sxs-lookup"><span data-stu-id="ed830-112">The method does nothing in the base class; it is available for the derived class to override.</span></span> <span data-ttu-id="ed830-113">如果衍生類別傳回錯誤碼，執行緒就會結束併發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="ed830-113">If the derived class returns an error code, the thread exits with an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed830-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed830-114">Requirements</span></span>



| <span data-ttu-id="ed830-115">需求</span><span class="sxs-lookup"><span data-stu-id="ed830-115">Requirement</span></span> | <span data-ttu-id="ed830-116">值</span><span class="sxs-lookup"><span data-stu-id="ed830-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed830-117">標頭</span><span class="sxs-lookup"><span data-stu-id="ed830-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ed830-118"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="ed830-118"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ed830-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="ed830-119">Library</span></span><br/> | <dl> <span data-ttu-id="ed830-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ed830-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed830-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed830-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed830-122">**CSourceStream 類別**</span><span class="sxs-lookup"><span data-stu-id="ed830-122">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




