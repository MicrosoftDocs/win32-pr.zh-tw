---
description: CTransformInputPin. EndFlush 方法-EndFlush 方法會結束清除作業。 這個方法會實 IPin：： EndFlush 方法。
ms.assetid: ebc70df3-e99d-4292-990b-99b79ff06461
title: 'CTransformInputPin. EndFlush 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5e080b4531d05160bebd42a68145842c4783bea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095056"
---
# <a name="ctransforminputpinendflush-method"></a><span data-ttu-id="1add3-104">CTransformInputPin. EndFlush 方法</span><span class="sxs-lookup"><span data-stu-id="1add3-104">CTransformInputPin.EndFlush method</span></span>

<span data-ttu-id="1add3-105">`EndFlush`方法會結束清除作業。</span><span class="sxs-lookup"><span data-stu-id="1add3-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="1add3-106">這個方法會實 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 方法。</span><span class="sxs-lookup"><span data-stu-id="1add3-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1add3-107">語法</span><span class="sxs-lookup"><span data-stu-id="1add3-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="1add3-108">參數</span><span class="sxs-lookup"><span data-stu-id="1add3-108">Parameters</span></span>

<span data-ttu-id="1add3-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="1add3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1add3-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="1add3-110">Return value</span></span>

<span data-ttu-id="1add3-111">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="1add3-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1add3-112">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="1add3-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="1add3-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1add3-113">Return code</span></span>                                                                                           | <span data-ttu-id="1add3-114">Description</span><span class="sxs-lookup"><span data-stu-id="1add3-114">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="1add3-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="1add3-115"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="1add3-116">成功。</span><span class="sxs-lookup"><span data-stu-id="1add3-116">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="1add3-117"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="1add3-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="1add3-118">輸出 pin 未連接。</span><span class="sxs-lookup"><span data-stu-id="1add3-118">Output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1add3-119">備註</span><span class="sxs-lookup"><span data-stu-id="1add3-119">Remarks</span></span>

<span data-ttu-id="1add3-120">這個方法會呼叫篩選準則的 [**CTransformFilter：： EndFlush**](ctransformfilter-endflush.md) 方法，以傳遞下游的呼叫。</span><span class="sxs-lookup"><span data-stu-id="1add3-120">This method calls the filter's [**CTransformFilter::EndFlush**](ctransformfilter-endflush.md) method to deliver the call downstream.</span></span> <span data-ttu-id="1add3-121">然後，它會呼叫釘選的 [**CBaseInputPin：： EndFlush**](cbaseinputpin-endflush.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="1add3-121">Then it calls the pin's [**CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1add3-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="1add3-122">Requirements</span></span>



| <span data-ttu-id="1add3-123">需求</span><span class="sxs-lookup"><span data-stu-id="1add3-123">Requirement</span></span> | <span data-ttu-id="1add3-124">值</span><span class="sxs-lookup"><span data-stu-id="1add3-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1add3-125">標頭</span><span class="sxs-lookup"><span data-stu-id="1add3-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1add3-126"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1add3-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1add3-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="1add3-127">Library</span></span><br/> | <dl> <span data-ttu-id="1add3-128"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="1add3-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




