---
description: 函式方法。
ms.assetid: bf335750-b776-47bc-978d-e84e8b5259f7
title: 'CRenderedInputPin. CRenderedInputPin (Amextra. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.CRenderedInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee1ec8944d56d2aa6f46e59ac5034969ca77ea19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990264"
---
# <a name="crenderedinputpincrenderedinputpin-constructor"></a><span data-ttu-id="57e20-103">CRenderedInputPin. CRenderedInputPin 函數</span><span class="sxs-lookup"><span data-stu-id="57e20-103">CRenderedInputPin.CRenderedInputPin constructor</span></span>

<span data-ttu-id="57e20-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="57e20-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="57e20-105">語法</span><span class="sxs-lookup"><span data-stu-id="57e20-105">Syntax</span></span>


```C++
CRenderedInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="57e20-106">參數</span><span class="sxs-lookup"><span data-stu-id="57e20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57e20-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="57e20-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="57e20-108">包含物件之偵錯工具名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="57e20-108">String containing the debug name of the object.</span></span> <span data-ttu-id="57e20-109">如需詳細資訊，請參閱 [**CBaseObject 類別**](cbaseobject.md)。</span><span class="sxs-lookup"><span data-stu-id="57e20-109">For more information, see [**CBaseObject Class**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="57e20-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="57e20-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="57e20-111">建立此釘選之篩選準則的指標。</span><span class="sxs-lookup"><span data-stu-id="57e20-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="57e20-112">*pLock*</span><span class="sxs-lookup"><span data-stu-id="57e20-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="57e20-113">[**CCritSec**](ccritsec.md)鎖定的指標，用來序列化狀態變更。</span><span class="sxs-lookup"><span data-stu-id="57e20-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="57e20-114">這可以是與 filter lock [**CBaseFilter：： m \_ pLock**](cbasefilter-m-plock.md)相同的重要區段。</span><span class="sxs-lookup"><span data-stu-id="57e20-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="57e20-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="57e20-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="57e20-116">變數的指標，此變數會接收 **HRESULT** 值，指出方法的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="57e20-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="57e20-117">*pName*</span><span class="sxs-lookup"><span data-stu-id="57e20-117">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="57e20-118">包含 pin 名稱的寬字元字串 (也用來作為 pin 識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="57e20-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="57e20-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="57e20-119">Requirements</span></span>



| <span data-ttu-id="57e20-120">需求</span><span class="sxs-lookup"><span data-stu-id="57e20-120">Requirement</span></span> | <span data-ttu-id="57e20-121">值</span><span class="sxs-lookup"><span data-stu-id="57e20-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57e20-122">標頭</span><span class="sxs-lookup"><span data-stu-id="57e20-122">Header</span></span><br/>  | <dl> <span data-ttu-id="57e20-123"><dt>Amextra (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="57e20-123"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="57e20-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="57e20-124">Library</span></span><br/> | <dl> <span data-ttu-id="57e20-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="57e20-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57e20-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57e20-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57e20-127">**CRenderedInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="57e20-127">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




