---
description: BreakConnect 方法會從連接釋放 pin。
ms.assetid: a1f299e1-30bf-4d55-84cf-73acccf38151
title: 'CBasePin. BreakConnect 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8964ea76e48e4753f42923663ab45962cd672e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979576"
---
# <a name="cbasepinbreakconnect-method"></a><span data-ttu-id="48706-103">CBasePin. BreakConnect 方法</span><span class="sxs-lookup"><span data-stu-id="48706-103">CBasePin.BreakConnect method</span></span>

<span data-ttu-id="48706-104">`BreakConnect`方法會從連接釋放 pin。</span><span class="sxs-lookup"><span data-stu-id="48706-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="48706-105">語法</span><span class="sxs-lookup"><span data-stu-id="48706-105">Syntax</span></span>


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="48706-106">參數</span><span class="sxs-lookup"><span data-stu-id="48706-106">Parameters</span></span>

<span data-ttu-id="48706-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="48706-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="48706-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="48706-108">Return value</span></span>

<span data-ttu-id="48706-109">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="48706-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="48706-110">備註</span><span class="sxs-lookup"><span data-stu-id="48706-110">Remarks</span></span>

<span data-ttu-id="48706-111">[**CBasePin：:D isconnect**](cbasepin-disconnect.md)方法在 pin 中斷連接期間會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="48706-111">This method is called during pin disconnection by the [**CBasePin::Disconnect**](cbasepin-disconnect.md) method.</span></span> <span data-ttu-id="48706-112">如果 [**CBasePin：： CheckConnect**](cbasepin-checkconnect.md) 方法失敗，也會在嘗試連接期間呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="48706-112">It is also called during a connection attempt if the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method fails.</span></span>

<span data-ttu-id="48706-113">這個方法必須釋放 **CheckConnect** 方法所取得的任何資源。</span><span class="sxs-lookup"><span data-stu-id="48706-113">This method must free any resources that were obtained by the **CheckConnect** method.</span></span> <span data-ttu-id="48706-114">例如，如果 **CheckConnect** 配置記憶體，則 `BreakConnect` 應該釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="48706-114">For example, if **CheckConnect** allocates memory, `BreakConnect` should free the memory.</span></span> <span data-ttu-id="48706-115">如果 **CheckConnect** 查詢介面的連接 pin，則 `BreakConnect` 應該釋放介面。</span><span class="sxs-lookup"><span data-stu-id="48706-115">If **CheckConnect** queries the connecting pin for an interface, `BreakConnect` should free the interface.</span></span>

<span data-ttu-id="48706-116">請注意，您 `BreakConnect` 可以呼叫，而不需要對應的 **CompleteConnect** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="48706-116">Note that `BreakConnect` can be called without a corresponding call to **CompleteConnect**.</span></span> <span data-ttu-id="48706-117">因此，您無法假設先前已呼叫過 **CompleteConnect** 。</span><span class="sxs-lookup"><span data-stu-id="48706-117">Therefore, you cannot assume that **CompleteConnect** has been called previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="48706-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="48706-118">Requirements</span></span>



| <span data-ttu-id="48706-119">需求</span><span class="sxs-lookup"><span data-stu-id="48706-119">Requirement</span></span> | <span data-ttu-id="48706-120">值</span><span class="sxs-lookup"><span data-stu-id="48706-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48706-121">標頭</span><span class="sxs-lookup"><span data-stu-id="48706-121">Header</span></span><br/>  | <dl> <span data-ttu-id="48706-122"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="48706-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="48706-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="48706-123">Library</span></span><br/> | <dl> <span data-ttu-id="48706-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="48706-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48706-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48706-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48706-126">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="48706-126">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




