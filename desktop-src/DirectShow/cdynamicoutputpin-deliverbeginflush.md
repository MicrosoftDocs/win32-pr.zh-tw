---
description: CDynamicOutputPin. DeliverBeginFlush 方法-DeliverBeginFlush 方法會要求連接的輸入 pin，以開始進行清除操作。
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
ms.openlocfilehash: e4158a3d6191325e8b647e4551133952d623f795
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099316"
---
# <a name="cdynamicoutputpindeliverbeginflush-method"></a><span data-ttu-id="4d887-103">CDynamicOutputPin. DeliverBeginFlush 方法</span><span class="sxs-lookup"><span data-stu-id="4d887-103">CDynamicOutputPin.DeliverBeginFlush method</span></span>

<span data-ttu-id="4d887-104">`DeliverBeginFlush`方法會要求連接的輸入 pin，以開始進行清除操作。</span><span class="sxs-lookup"><span data-stu-id="4d887-104">The `DeliverBeginFlush` method requests the connected input pin to begin a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d887-105">語法</span><span class="sxs-lookup"><span data-stu-id="4d887-105">Syntax</span></span>


```C++
HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="4d887-106">參數</span><span class="sxs-lookup"><span data-stu-id="4d887-106">Parameters</span></span>

<span data-ttu-id="4d887-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4d887-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4d887-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d887-108">Return value</span></span>

<span data-ttu-id="4d887-109">\_如果成功，則傳回，否則會傳回指出失敗原因的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="4d887-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d887-110">備註</span><span class="sxs-lookup"><span data-stu-id="4d887-110">Remarks</span></span>

<span data-ttu-id="4d887-111">這個方法會覆寫 [**CBaseOutputPin：:D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="4d887-111">This method overrides the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span> <span data-ttu-id="4d887-112">它會設定 [**CDynamicOutputPin：： m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="4d887-112">It sets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d887-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d887-113">Requirements</span></span>



| <span data-ttu-id="4d887-114">需求</span><span class="sxs-lookup"><span data-stu-id="4d887-114">Requirement</span></span> | <span data-ttu-id="4d887-115">值</span><span class="sxs-lookup"><span data-stu-id="4d887-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d887-116">標頭</span><span class="sxs-lookup"><span data-stu-id="4d887-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4d887-117"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4d887-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4d887-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="4d887-118">Library</span></span><br/> | <dl> <span data-ttu-id="4d887-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4d887-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d887-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d887-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d887-121">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="4d887-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




