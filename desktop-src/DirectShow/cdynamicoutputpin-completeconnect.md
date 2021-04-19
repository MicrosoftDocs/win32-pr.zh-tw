---
description: CompleteConnect 方法會完成輸入 pin 的連接。
ms.assetid: c23195e7-8d66-4217-bd59-8889459ce4f1
title: 'CDynamicOutputPin. CompleteConnect 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31afa592701b881d39ab4948514aacfe50b345b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991031"
---
# <a name="cdynamicoutputpincompleteconnect-method"></a><span data-ttu-id="eca56-103">CDynamicOutputPin. CompleteConnect 方法</span><span class="sxs-lookup"><span data-stu-id="eca56-103">CDynamicOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="eca56-104">`CompleteConnect`方法會完成輸入 pin 的連接。</span><span class="sxs-lookup"><span data-stu-id="eca56-104">The `CompleteConnect` method completes a connection to an input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="eca56-105">語法</span><span class="sxs-lookup"><span data-stu-id="eca56-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="eca56-106">參數</span><span class="sxs-lookup"><span data-stu-id="eca56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eca56-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="eca56-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="eca56-108">輸入釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="eca56-108">Pointer to the input pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eca56-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="eca56-109">Return value</span></span>

<span data-ttu-id="eca56-110">\_如果成功，則傳回，否則會傳回指出失敗原因的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="eca56-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="eca56-111">備註</span><span class="sxs-lookup"><span data-stu-id="eca56-111">Remarks</span></span>

<span data-ttu-id="eca56-112">這個方法會覆寫 [**CBaseOutputPin：： CompleteConnect**](cbaseoutputpin-completeconnect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="eca56-112">This method overrides the [**CBaseOutputPin::CompleteConnect**](cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="eca56-113">為了支援動態重新加入，這個方法會在篩選準則為使用中時認可配置器。</span><span class="sxs-lookup"><span data-stu-id="eca56-113">To support dynamic reconnections, this method commits the allocator if the filter is active.</span></span> <span data-ttu-id="eca56-114">在基類中，只有當篩選準則停止時才會發生連接，因此配置器一律會在 [**CBaseOutputPin：： Active**](cbaseoutputpin-active.md) 方法中認可。</span><span class="sxs-lookup"><span data-stu-id="eca56-114">In the base class, connections can occur only when the filter is stopped, so the allocator is always committed in the [**CBaseOutputPin::Active**](cbaseoutputpin-active.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="eca56-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="eca56-115">Requirements</span></span>



| <span data-ttu-id="eca56-116">需求</span><span class="sxs-lookup"><span data-stu-id="eca56-116">Requirement</span></span> | <span data-ttu-id="eca56-117">值</span><span class="sxs-lookup"><span data-stu-id="eca56-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eca56-118">標頭</span><span class="sxs-lookup"><span data-stu-id="eca56-118">Header</span></span><br/>  | <dl> <span data-ttu-id="eca56-119"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="eca56-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="eca56-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="eca56-120">Library</span></span><br/> | <dl> <span data-ttu-id="eca56-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="eca56-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eca56-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eca56-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eca56-123">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="eca56-123">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




