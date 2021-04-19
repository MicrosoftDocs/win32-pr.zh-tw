---
description: CAutoUsingOutputPin 類別會取得並釋放 CDynamicOutputPin 物件的存取權。
ms.assetid: 4ded5d18-4b14-4574-ad1f-73b886a51fac
title: 'CAutoUsingOutputPin 類別 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b664267ce2ff0dbbeeba8bc74708c9c67e185ae4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993615"
---
# <a name="cautousingoutputpin-class"></a><span data-ttu-id="3436d-103">CAutoUsingOutputPin 類別</span><span class="sxs-lookup"><span data-stu-id="3436d-103">CAutoUsingOutputPin class</span></span>

<span data-ttu-id="3436d-104">**CAutoUsingOutputPin** 類別會取得並釋放 [**CDynamicOutputPin**](cdynamicoutputpin.md)物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="3436d-104">The **CAutoUsingOutputPin** class obtains and releases access to a [**CDynamicOutputPin**](cdynamicoutputpin.md) object.</span></span>

<span data-ttu-id="3436d-105">**CAutoUsingOutputPin** 具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3436d-105">**CAutoUsingOutputPin** has these types of members:</span></span>



| <span data-ttu-id="3436d-106">公用方法</span><span class="sxs-lookup"><span data-stu-id="3436d-106">Public Methods</span></span>                                                           | <span data-ttu-id="3436d-107">Description</span><span class="sxs-lookup"><span data-stu-id="3436d-107">Description</span></span>                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="3436d-108">**CAutoUsingOutputPin**</span><span class="sxs-lookup"><span data-stu-id="3436d-108">**CAutoUsingOutputPin**</span></span>](cautousingoutputpin-cautousingoutputpin.md)   | <span data-ttu-id="3436d-109">函式方法。</span><span class="sxs-lookup"><span data-stu-id="3436d-109">Constructor method.</span></span> <span data-ttu-id="3436d-110">取得指定之 pin 的存取權。</span><span class="sxs-lookup"><span data-stu-id="3436d-110">Obtains access to the specified pin.</span></span> |
| [<span data-ttu-id="3436d-111">**~ CAutoUsingOutputPin**</span><span class="sxs-lookup"><span data-stu-id="3436d-111">**~CAutoUsingOutputPin**</span></span>](cautousingoutputpin--cautousingoutputpin.md) | <span data-ttu-id="3436d-112">函式方法。</span><span class="sxs-lookup"><span data-stu-id="3436d-112">Destructor method.</span></span> <span data-ttu-id="3436d-113">取得指定之 pin 的存取權。</span><span class="sxs-lookup"><span data-stu-id="3436d-113">Obtains access to the specified pin.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="3436d-114">備註</span><span class="sxs-lookup"><span data-stu-id="3436d-114">Remarks</span></span>

<span data-ttu-id="3436d-115">在 [**CDynamicOutputPin**](cdynamicoutputpin.md)上呼叫特定方法時，呼叫端必須取得 pin 的存取權，然後釋放該存取權。</span><span class="sxs-lookup"><span data-stu-id="3436d-115">When certain methods are called on [**CDynamicOutputPin**](cdynamicoutputpin.md), the caller must obtain access to the pin and then release that access.</span></span> <span data-ttu-id="3436d-116">為了取得存取權，呼叫端會使用 [**CDynamicOutputPin：： StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="3436d-116">To obtain access, the caller uses the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method.</span></span> <span data-ttu-id="3436d-117">若要釋放存取權，則會呼叫 [**CDynamicOutputPin：： StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="3436d-117">To release access, it calls the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method.</span></span> <span data-ttu-id="3436d-118">**CAutoUsingOutputPin** 類別是一個 helper 類別，可在其函式和函式方法中處理這些工作。</span><span class="sxs-lookup"><span data-stu-id="3436d-118">The **CAutoUsingOutputPin** class is a helper class that handles these tasks in its constructor and destructor methods.</span></span> <span data-ttu-id="3436d-119">下列程式碼範例顯示如何使用這個類別：</span><span class="sxs-lookup"><span data-stu-id="3436d-119">The following code example shows how to use this class:</span></span>


```
CDynamicOutputPin *pPin;
HRESULT hr = S_OK;  // Important! Initialize to S_OK.

// TODO: Obtain a pointer to the pin (not shown).

// Scope for lock.
{
    // Hold lock on pin.
    CAutoUsingOutputPin UsingPin(pPin, &hr)

    if (SUCCEEDED(hr)) 
    {

        // Safe to use the pin.
        hr = pPin->Deliver(pSample);

    }

} // Object goes out of scope here.

// No longer safe to use the pin.
```



## <a name="requirements"></a><span data-ttu-id="3436d-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="3436d-120">Requirements</span></span>



| <span data-ttu-id="3436d-121">需求</span><span class="sxs-lookup"><span data-stu-id="3436d-121">Requirement</span></span> | <span data-ttu-id="3436d-122">值</span><span class="sxs-lookup"><span data-stu-id="3436d-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3436d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="3436d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="3436d-124"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3436d-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3436d-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="3436d-125">Library</span></span><br/> | <dl> <span data-ttu-id="3436d-126"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3436d-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3436d-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3436d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3436d-128">基類參考</span><span class="sxs-lookup"><span data-stu-id="3436d-128">Base Class Reference</span></span>](base-class-reference.md)
</dt> </dl>

 

 




