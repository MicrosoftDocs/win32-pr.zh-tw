---
description: HRESULT 值，指出物件是否會接受範例。 如果值為 S \_ OK，則物件會接受範例。 否則，它會拒絕範例。
ms.assetid: e05d4d2e-cc3e-4b83-8531-bc4bd6d665ac
title: 'COutputQueue：： m_hr 成員 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hr
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b786afa24f974d5eab7e13062105f26386da1c30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978685"
---
# <a name="coutputqueuem_hr-member"></a><span data-ttu-id="ee039-105">COutputQueue：： m \_ hr 成員</span><span class="sxs-lookup"><span data-stu-id="ee039-105">COutputQueue::m\_hr member</span></span>

<span data-ttu-id="ee039-106">**HRESULT** 值，指出物件是否會接受範例。</span><span class="sxs-lookup"><span data-stu-id="ee039-106">**HRESULT** value that indicates whether the object will accept samples.</span></span> <span data-ttu-id="ee039-107">如果值為 S \_ OK，則物件會接受範例。</span><span class="sxs-lookup"><span data-stu-id="ee039-107">If the value is S\_OK, the object will accept samples.</span></span> <span data-ttu-id="ee039-108">否則，它會拒絕範例。</span><span class="sxs-lookup"><span data-stu-id="ee039-108">Otherwise, it rejects samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee039-109">語法</span><span class="sxs-lookup"><span data-stu-id="ee039-109">Syntax</span></span>


```C++
HRESULT m_hr;
```



## <a name="remarks"></a><span data-ttu-id="ee039-110">備註</span><span class="sxs-lookup"><span data-stu-id="ee039-110">Remarks</span></span>

<span data-ttu-id="ee039-111">此成員變數用來協調執行緒之間的活動。</span><span class="sxs-lookup"><span data-stu-id="ee039-111">This member variable is used to coordinate activities across threads.</span></span> <span data-ttu-id="ee039-112">如果下游輸入 pin 拒絕範例，或物件開始排清，此值會設為 \_ FALSE 或錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ee039-112">If the downstream input pin rejects a sample, or if the object begins flushing, the value is set to S\_FALSE or an error code.</span></span> <span data-ttu-id="ee039-113">在排清完成之前，或在呼叫 [**COutputQueue：： Reset**](coutputqueue-reset.md) 方法之前，物件將不會提供任何更多的範例。</span><span class="sxs-lookup"><span data-stu-id="ee039-113">The object will not deliver any more samples until flushing is complete, or until the [**COutputQueue::Reset**](coutputqueue-reset.md) method is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee039-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee039-114">Requirements</span></span>



| <span data-ttu-id="ee039-115">需求</span><span class="sxs-lookup"><span data-stu-id="ee039-115">Requirement</span></span> | <span data-ttu-id="ee039-116">值</span><span class="sxs-lookup"><span data-stu-id="ee039-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee039-117">標頭</span><span class="sxs-lookup"><span data-stu-id="ee039-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ee039-118"><dt>Outputq (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ee039-118"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ee039-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="ee039-119">Library</span></span><br/> | <dl> <span data-ttu-id="ee039-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ee039-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee039-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee039-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee039-122">**COutputQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="ee039-122">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




