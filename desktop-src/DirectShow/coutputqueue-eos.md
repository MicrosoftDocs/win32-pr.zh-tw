---
description: EOS 方法會將結束資料流程呼叫傳遞給輸入的 pin。
ms.assetid: 65e8db14-6ca8-4c4f-8bd8-2442f743499e
title: 'COutputQueue 的 Outputq 方法 (. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab05d4ab3f2620c11bd62d566be851e16b28cecd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998650"
---
# <a name="coutputqueueeos-method"></a><span data-ttu-id="e7765-103">COutputQueue. EOS 方法</span><span class="sxs-lookup"><span data-stu-id="e7765-103">COutputQueue.EOS method</span></span>

<span data-ttu-id="e7765-104">方法會將 `EOS` 結束資料流程呼叫傳遞給輸入的 pin。</span><span class="sxs-lookup"><span data-stu-id="e7765-104">The `EOS` method delivers an end-of-stream call to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7765-105">語法</span><span class="sxs-lookup"><span data-stu-id="e7765-105">Syntax</span></span>


```C++
void EOS();
```



## <a name="parameters"></a><span data-ttu-id="e7765-106">參數</span><span class="sxs-lookup"><span data-stu-id="e7765-106">Parameters</span></span>

<span data-ttu-id="e7765-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e7765-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e7765-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="e7765-108">Return value</span></span>

<span data-ttu-id="e7765-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e7765-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7765-110">備註</span><span class="sxs-lookup"><span data-stu-id="e7765-110">Remarks</span></span>

<span data-ttu-id="e7765-111">如果物件使用執行緒，則會將 EOS \_ 封包控制訊息排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="e7765-111">If the object is using a thread, it queues an EOS\_PACKET control message.</span></span> <span data-ttu-id="e7765-112">執行緒會傳遞任何暫止的範例，並在輸入的 pin 上呼叫 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) 方法。</span><span class="sxs-lookup"><span data-stu-id="e7765-112">The thread delivers any pending samples and calls the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method on the input pin.</span></span>

<span data-ttu-id="e7765-113">如果物件未使用執行緒，則會呼叫 [**COutputQueue：： SendAnyway**](coutputqueue-sendanyway.md) 方法來傳遞任何暫止的範例。</span><span class="sxs-lookup"><span data-stu-id="e7765-113">If the object is not using a thread, it calls the [**COutputQueue::SendAnyway**](coutputqueue-sendanyway.md) method to deliver any pending samples.</span></span> <span data-ttu-id="e7765-114">然後，它會在輸入 pin 上呼叫 **IPin：： EndOfStream** 。</span><span class="sxs-lookup"><span data-stu-id="e7765-114">Then it calls **IPin::EndOfStream** on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7765-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7765-115">Requirements</span></span>



| <span data-ttu-id="e7765-116">需求</span><span class="sxs-lookup"><span data-stu-id="e7765-116">Requirement</span></span> | <span data-ttu-id="e7765-117">值</span><span class="sxs-lookup"><span data-stu-id="e7765-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7765-118">標頭</span><span class="sxs-lookup"><span data-stu-id="e7765-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e7765-119"><dt>Outputq (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e7765-119"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e7765-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="e7765-120">Library</span></span><br/> | <dl> <span data-ttu-id="e7765-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e7765-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7765-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7765-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7765-123">**COutputQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="e7765-123">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




