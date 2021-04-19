---
description: SetPopEvent 方法會指定當物件從佇列中移除範例時發出信號的事件。
ms.assetid: 147a09b9-14d3-4739-843a-1bfb19d2d052
title: 'COutputQueue. SetPopEvent 方法 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SetPopEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 764abf76265fce66c5798923ca1fa522edd682af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992790"
---
# <a name="coutputqueuesetpopevent-method"></a><span data-ttu-id="003de-103">COutputQueue. SetPopEvent 方法</span><span class="sxs-lookup"><span data-stu-id="003de-103">COutputQueue.SetPopEvent method</span></span>

<span data-ttu-id="003de-104">`SetPopEvent`方法會指定當物件從佇列中移除範例時，會發出信號的事件。</span><span class="sxs-lookup"><span data-stu-id="003de-104">The `SetPopEvent` method specifies an event that is signaled whenever the object removes a sample from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="003de-105">語法</span><span class="sxs-lookup"><span data-stu-id="003de-105">Syntax</span></span>


```C++
void SetPopEvent(
   HANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="003de-106">參數</span><span class="sxs-lookup"><span data-stu-id="003de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="003de-107">*hEvent*</span><span class="sxs-lookup"><span data-stu-id="003de-107">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="003de-108">呼叫端所建立之事件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="003de-108">Handle to an event created by the caller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="003de-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="003de-109">Return value</span></span>

<span data-ttu-id="003de-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="003de-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="003de-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="003de-111">Requirements</span></span>



| <span data-ttu-id="003de-112">需求</span><span class="sxs-lookup"><span data-stu-id="003de-112">Requirement</span></span> | <span data-ttu-id="003de-113">值</span><span class="sxs-lookup"><span data-stu-id="003de-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="003de-114">標頭</span><span class="sxs-lookup"><span data-stu-id="003de-114">Header</span></span><br/>  | <dl> <span data-ttu-id="003de-115"><dt>Outputq (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="003de-115"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="003de-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="003de-116">Library</span></span><br/> | <dl> <span data-ttu-id="003de-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="003de-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="003de-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="003de-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="003de-119">**COutputQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="003de-119">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




