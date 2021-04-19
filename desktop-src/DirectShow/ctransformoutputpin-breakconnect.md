---
description: BreakConnect 方法會從連接釋放 pin。
ms.assetid: bf68aca3-93e5-4f9d-9980-1a5eed1513f5
title: 'CTransformOutputPin. BreakConnect 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 316806b89adf6493f32125da488990151f0916b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989594"
---
# <a name="ctransformoutputpinbreakconnect-method"></a><span data-ttu-id="8606c-103">CTransformOutputPin. BreakConnect 方法</span><span class="sxs-lookup"><span data-stu-id="8606c-103">CTransformOutputPin.BreakConnect method</span></span>

<span data-ttu-id="8606c-104">`BreakConnect`方法會從連接釋放 pin。</span><span class="sxs-lookup"><span data-stu-id="8606c-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8606c-105">語法</span><span class="sxs-lookup"><span data-stu-id="8606c-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="8606c-106">參數</span><span class="sxs-lookup"><span data-stu-id="8606c-106">Parameters</span></span>

<span data-ttu-id="8606c-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="8606c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8606c-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="8606c-108">Return value</span></span>

<span data-ttu-id="8606c-109">傳回 S \_ OK 或其他 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="8606c-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8606c-110">備註</span><span class="sxs-lookup"><span data-stu-id="8606c-110">Remarks</span></span>

<span data-ttu-id="8606c-111">這個方法會覆寫 [**CBaseOutputPin：： BreakConnect**](cbaseoutputpin-breakconnect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="8606c-111">This method overrides the [**CBaseOutputPin::BreakConnect**](cbaseoutputpin-breakconnect.md) method.</span></span> <span data-ttu-id="8606c-112">它會呼叫篩選器的 [**CTransformFilter：： BreakConnect**](ctransformfilter-breakconnect.md) 方法，它會 \_ 在基類中傳回 s OK。</span><span class="sxs-lookup"><span data-stu-id="8606c-112">It calls the filter's [**CTransformFilter::BreakConnect**](ctransformfilter-breakconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="8606c-113">衍生的類別可以覆寫 **CTransformFilter：： BreakConnect** 方法。</span><span class="sxs-lookup"><span data-stu-id="8606c-113">The derived class can override the **CTransformFilter::BreakConnect** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8606c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8606c-114">Requirements</span></span>



| <span data-ttu-id="8606c-115">需求</span><span class="sxs-lookup"><span data-stu-id="8606c-115">Requirement</span></span> | <span data-ttu-id="8606c-116">值</span><span class="sxs-lookup"><span data-stu-id="8606c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8606c-117">標頭</span><span class="sxs-lookup"><span data-stu-id="8606c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8606c-118"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8606c-118"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8606c-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="8606c-119">Library</span></span><br/> | <dl> <span data-ttu-id="8606c-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8606c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




