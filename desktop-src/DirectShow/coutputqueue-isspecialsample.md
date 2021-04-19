---
description: IsSpecialSample 方法會判斷佇列資料是否為控制訊息。
ms.assetid: 33d9c7a2-3046-45a5-a9f5-8f33a03bbcdd
title: 'COutputQueue. IsSpecialSample 方法 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsSpecialSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc57847d6a977c740bbf50bae220a89b0ed6fab1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995646"
---
# <a name="coutputqueueisspecialsample-method"></a><span data-ttu-id="32b4e-103">COutputQueue. IsSpecialSample 方法</span><span class="sxs-lookup"><span data-stu-id="32b4e-103">COutputQueue.IsSpecialSample method</span></span>

<span data-ttu-id="32b4e-104">`IsSpecialSample`方法會判斷佇列資料是否為控制訊息。</span><span class="sxs-lookup"><span data-stu-id="32b4e-104">The `IsSpecialSample` method determines whether queued data is a control message.</span></span>

## <a name="syntax"></a><span data-ttu-id="32b4e-105">語法</span><span class="sxs-lookup"><span data-stu-id="32b4e-105">Syntax</span></span>


```C++
BOOL IsSpecialSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="32b4e-106">參數</span><span class="sxs-lookup"><span data-stu-id="32b4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32b4e-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="32b4e-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="32b4e-108">佇列中專案的指標。</span><span class="sxs-lookup"><span data-stu-id="32b4e-108">Pointer to an item in the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32b4e-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="32b4e-109">Return value</span></span>

<span data-ttu-id="32b4e-110">如果 *pSample* 是控制訊息，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="32b4e-110">Returns **TRUE** if *pSample* is a control message, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="32b4e-111">備註</span><span class="sxs-lookup"><span data-stu-id="32b4e-111">Remarks</span></span>

<span data-ttu-id="32b4e-112">[**COutputQueue：： QueueSample**](coutputqueue-queuesample.md)方法除了媒體範例之外，還可以接收控制訊息。</span><span class="sxs-lookup"><span data-stu-id="32b4e-112">The [**COutputQueue::QueueSample**](coutputqueue-queuesample.md) method can receive control messages in addition to media samples.</span></span> <span data-ttu-id="32b4e-113">控制訊息是已定義的常數 (轉換成長的 \_ PTR 類型) ，指示執行緒執行動作。</span><span class="sxs-lookup"><span data-stu-id="32b4e-113">A control message is a defined constant (cast to a LONG\_PTR type) that instructs the thread to perform an action.</span></span> <span data-ttu-id="32b4e-114">控制訊息不包含媒體資料。</span><span class="sxs-lookup"><span data-stu-id="32b4e-114">Control messages do not contain media data.</span></span> <span data-ttu-id="32b4e-115">如需詳細資訊，請參閱 **COutputQueue：： QueueSample**。</span><span class="sxs-lookup"><span data-stu-id="32b4e-115">For more information, see **COutputQueue::QueueSample**.</span></span>

## <a name="requirements"></a><span data-ttu-id="32b4e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="32b4e-116">Requirements</span></span>



| <span data-ttu-id="32b4e-117">需求</span><span class="sxs-lookup"><span data-stu-id="32b4e-117">Requirement</span></span> | <span data-ttu-id="32b4e-118">值</span><span class="sxs-lookup"><span data-stu-id="32b4e-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32b4e-119">標頭</span><span class="sxs-lookup"><span data-stu-id="32b4e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="32b4e-120"><dt>Outputq (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="32b4e-120"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="32b4e-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="32b4e-121">Library</span></span><br/> | <dl> <span data-ttu-id="32b4e-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="32b4e-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32b4e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32b4e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32b4e-124">**COutputQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="32b4e-124">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




