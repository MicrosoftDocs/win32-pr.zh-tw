---
description: StreamingThreadUsingOutputPin 方法會判斷任何執行緒是否正在執行釘選的串流作業。
ms.assetid: b6432a11-4e8b-4eb4-ad8e-aaff9398641b
title: 'CDynamicOutputPin. StreamingThreadUsingOutputPin 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StreamingThreadUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 797dcb94e227861642de2a05e6edf24f675bb4e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990965"
---
# <a name="cdynamicoutputpinstreamingthreadusingoutputpin-method"></a><span data-ttu-id="39795-103">CDynamicOutputPin. StreamingThreadUsingOutputPin 方法</span><span class="sxs-lookup"><span data-stu-id="39795-103">CDynamicOutputPin.StreamingThreadUsingOutputPin method</span></span>

<span data-ttu-id="39795-104">StreamingThreadUsingOutputPin 方法會判斷任何執行緒是否正在執行釘選的串流作業。</span><span class="sxs-lookup"><span data-stu-id="39795-104">The StreamingThreadUsingOutputPin method determines whether any thread is performing a streaming operation on the pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="39795-105">語法</span><span class="sxs-lookup"><span data-stu-id="39795-105">Syntax</span></span>


```C++
virtual bool StreamingThreadUsingOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="39795-106">參數</span><span class="sxs-lookup"><span data-stu-id="39795-106">Parameters</span></span>

<span data-ttu-id="39795-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="39795-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="39795-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="39795-108">Return value</span></span>

<span data-ttu-id="39795-109">如果執行緒正在釘選上執行資料流程作業，則傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="39795-109">Returns **TRUE** if a thread is performing a streaming operation on the pin.</span></span> <span data-ttu-id="39795-110">否則，會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="39795-110">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="39795-111">備註</span><span class="sxs-lookup"><span data-stu-id="39795-111">Remarks</span></span>

<span data-ttu-id="39795-112">如果有任何執行緒成功從 [**CDynamicOutputPin：： StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) 方法傳回，而且尚未對 [**CDynamicOutputPin：： StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) 方法進行對應的呼叫，這個方法會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="39795-112">If any threads have successfully returned from the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method and have not made a corresponding call to the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method, this method returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="39795-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="39795-113">Requirements</span></span>



| <span data-ttu-id="39795-114">需求</span><span class="sxs-lookup"><span data-stu-id="39795-114">Requirement</span></span> | <span data-ttu-id="39795-115">值</span><span class="sxs-lookup"><span data-stu-id="39795-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39795-116">標頭</span><span class="sxs-lookup"><span data-stu-id="39795-116">Header</span></span><br/>  | <dl> <span data-ttu-id="39795-117"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="39795-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="39795-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="39795-118">Library</span></span><br/> | <dl> <span data-ttu-id="39795-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="39795-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39795-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39795-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39795-121">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="39795-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




