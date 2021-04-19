---
description: DeliverBeginFlush 方法會要求連接的輸入 pin，以開始進行清除作業。
ms.assetid: eafc3835-7696-480b-abc8-154938e19b15
title: 'CDynamicOutputPin. DeliverBeginFlush 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverBeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 242394a327b63fcc901b08f572096bf2f42238b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993353"
---
# <a name="cdynamicoutputpindeliverbeginflush-method"></a><span data-ttu-id="0ce41-103">CDynamicOutputPin. DeliverBeginFlush 方法</span><span class="sxs-lookup"><span data-stu-id="0ce41-103">CDynamicOutputPin.DeliverBeginFlush method</span></span>

<span data-ttu-id="0ce41-104">`DeliverBeginFlush`方法會要求連接的輸入 pin，以開始進行清除操作。</span><span class="sxs-lookup"><span data-stu-id="0ce41-104">The `DeliverBeginFlush` method requests the connected input pin to begin a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ce41-105">語法</span><span class="sxs-lookup"><span data-stu-id="0ce41-105">Syntax</span></span>


```C++
HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="0ce41-106">參數</span><span class="sxs-lookup"><span data-stu-id="0ce41-106">Parameters</span></span>

<span data-ttu-id="0ce41-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0ce41-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ce41-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="0ce41-108">Return value</span></span>

<span data-ttu-id="0ce41-109">\_如果成功，則傳回，否則會傳回指出失敗原因的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="0ce41-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ce41-110">備註</span><span class="sxs-lookup"><span data-stu-id="0ce41-110">Remarks</span></span>

<span data-ttu-id="0ce41-111">這個方法會覆寫 [**CBaseOutputPin：:D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="0ce41-111">This method overrides the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span> <span data-ttu-id="0ce41-112">它會設定 [**CDynamicOutputPin：： m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="0ce41-112">It sets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ce41-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ce41-113">Requirements</span></span>



| <span data-ttu-id="0ce41-114">需求</span><span class="sxs-lookup"><span data-stu-id="0ce41-114">Requirement</span></span> | <span data-ttu-id="0ce41-115">值</span><span class="sxs-lookup"><span data-stu-id="0ce41-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ce41-116">標頭</span><span class="sxs-lookup"><span data-stu-id="0ce41-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0ce41-117"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0ce41-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0ce41-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="0ce41-118">Library</span></span><br/> | <dl> <span data-ttu-id="0ce41-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0ce41-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ce41-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ce41-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ce41-121">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="0ce41-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




