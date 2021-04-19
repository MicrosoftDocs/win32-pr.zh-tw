---
description: SetReconnectWhenActive 方法會指定 pin 是否支援動態重新連接。
ms.assetid: 64776008-5d1b-461c-a446-8cd6124276c0
title: 'CBasePin. SetReconnectWhenActive 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10840ad60c858f69164b19f2460a0039cd332700
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992776"
---
# <a name="cbasepinsetreconnectwhenactive-method"></a><span data-ttu-id="4ddcb-103">CBasePin. SetReconnectWhenActive 方法</span><span class="sxs-lookup"><span data-stu-id="4ddcb-103">CBasePin.SetReconnectWhenActive method</span></span>

<span data-ttu-id="4ddcb-104">`SetReconnectWhenActive`方法會指定 pin 是否支援動態重新連接。</span><span class="sxs-lookup"><span data-stu-id="4ddcb-104">The `SetReconnectWhenActive` method specifies whether the pin supports dynamic reconnections.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ddcb-105">語法</span><span class="sxs-lookup"><span data-stu-id="4ddcb-105">Syntax</span></span>


```C++
void SetReconnectWhenActive(
   bool bCanReconnect
);
```



## <a name="parameters"></a><span data-ttu-id="4ddcb-106">參數</span><span class="sxs-lookup"><span data-stu-id="4ddcb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ddcb-107">*bCanReconnect*</span><span class="sxs-lookup"><span data-stu-id="4ddcb-107">*bCanReconnect*</span></span> 
</dt> <dd>

<span data-ttu-id="4ddcb-108">指定 pin 是否可動態重新連接的布林值。</span><span class="sxs-lookup"><span data-stu-id="4ddcb-108">Boolean value that specifies whether the pin can dynamically reconnect.</span></span> <span data-ttu-id="4ddcb-109">若 **為 TRUE**，則 pin 可以動態重新連接。</span><span class="sxs-lookup"><span data-stu-id="4ddcb-109">If **TRUE**, the pin can dynamically reconnect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ddcb-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ddcb-110">Return value</span></span>

<span data-ttu-id="4ddcb-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4ddcb-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ddcb-112">備註</span><span class="sxs-lookup"><span data-stu-id="4ddcb-112">Remarks</span></span>

<span data-ttu-id="4ddcb-113">根據預設，您必須先停止篩選，才能重新連接其任何 pin。</span><span class="sxs-lookup"><span data-stu-id="4ddcb-113">By default, you must stop a filter before reconnecting any of its pins.</span></span> <span data-ttu-id="4ddcb-114">如果在篩選準則為使用中時，pin 可以重新連接，請以 **TRUE** 的值呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="4ddcb-114">If the pin can reconnect while the filter is active, call this method with a value of **TRUE**.</span></span> <span data-ttu-id="4ddcb-115">如需詳細資訊，請參閱 [動態圖形建築物](dynamic-graph-building.md)。</span><span class="sxs-lookup"><span data-stu-id="4ddcb-115">For more information, see [Dynamic Graph Building](dynamic-graph-building.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ddcb-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ddcb-116">Requirements</span></span>



| <span data-ttu-id="4ddcb-117">需求</span><span class="sxs-lookup"><span data-stu-id="4ddcb-117">Requirement</span></span> | <span data-ttu-id="4ddcb-118">值</span><span class="sxs-lookup"><span data-stu-id="4ddcb-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ddcb-119">標頭</span><span class="sxs-lookup"><span data-stu-id="4ddcb-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4ddcb-120"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4ddcb-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4ddcb-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="4ddcb-121">Library</span></span><br/> | <dl> <span data-ttu-id="4ddcb-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4ddcb-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ddcb-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ddcb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ddcb-124">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="4ddcb-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




