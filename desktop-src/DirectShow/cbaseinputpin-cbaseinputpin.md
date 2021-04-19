---
description: 函式方法。
ms.assetid: a853813d-cdf6-4cb4-8288-62685a883b56
title: 'CBaseInputPin. CBaseInputPin (Amfilter. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.CBaseInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 554c768f2cb99fda77aa87cfc916580b948da0ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993611"
---
# <a name="cbaseinputpincbaseinputpin-constructor"></a><span data-ttu-id="f259d-103">CBaseInputPin. CBaseInputPin 函數</span><span class="sxs-lookup"><span data-stu-id="f259d-103">CBaseInputPin.CBaseInputPin constructor</span></span>

<span data-ttu-id="f259d-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="f259d-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f259d-105">語法</span><span class="sxs-lookup"><span data-stu-id="f259d-105">Syntax</span></span>


```C++
CBaseInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pPinName
);
```



## <a name="parameters"></a><span data-ttu-id="f259d-106">參數</span><span class="sxs-lookup"><span data-stu-id="f259d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f259d-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="f259d-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="f259d-108">包含物件之偵錯工具名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="f259d-108">String containing the debug name of the object.</span></span> <span data-ttu-id="f259d-109">如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md)。</span><span class="sxs-lookup"><span data-stu-id="f259d-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="f259d-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="f259d-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="f259d-111">建立此釘選之篩選準則的指標。</span><span class="sxs-lookup"><span data-stu-id="f259d-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="f259d-112">*pLock*</span><span class="sxs-lookup"><span data-stu-id="f259d-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="f259d-113">[**CCritSec**](ccritsec.md)鎖定的指標，用來序列化狀態變更。</span><span class="sxs-lookup"><span data-stu-id="f259d-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="f259d-114">這可以是與 filter lock [**CBaseFilter：： m \_ pLock**](cbasefilter-m-plock.md)相同的重要區段。</span><span class="sxs-lookup"><span data-stu-id="f259d-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="f259d-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="f259d-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="f259d-116">變數的指標，此變數會接收 **HRESULT** 值，指出方法的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="f259d-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="f259d-117">*pPinName*</span><span class="sxs-lookup"><span data-stu-id="f259d-117">*pPinName*</span></span> 
</dt> <dd>

<span data-ttu-id="f259d-118">包含 pin 名稱的寬字元字串 (也用來作為 pin 識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="f259d-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f259d-119">備註</span><span class="sxs-lookup"><span data-stu-id="f259d-119">Remarks</span></span>

<span data-ttu-id="f259d-120">所有參數都會直接傳遞至 [**CBasePin**](cbasepin-cbasepin.md) 的函式。</span><span class="sxs-lookup"><span data-stu-id="f259d-120">All of the parameters are passed directly to the [**CBasePin**](cbasepin-cbasepin.md) constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="f259d-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f259d-121">Requirements</span></span>



| <span data-ttu-id="f259d-122">需求</span><span class="sxs-lookup"><span data-stu-id="f259d-122">Requirement</span></span> | <span data-ttu-id="f259d-123">值</span><span class="sxs-lookup"><span data-stu-id="f259d-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f259d-124">標頭</span><span class="sxs-lookup"><span data-stu-id="f259d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f259d-125"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f259d-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f259d-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="f259d-126">Library</span></span><br/> | <dl> <span data-ttu-id="f259d-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f259d-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f259d-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f259d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f259d-129">**CBaseInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="f259d-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




