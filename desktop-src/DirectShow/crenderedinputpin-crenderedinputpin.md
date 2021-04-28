---
description: CRenderedInputPin。 CRenderedInputPin 函式-函數方法。
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
ms.openlocfilehash: 4bd8e864531604fb36c2abe0bcd57ac5b3a9c869
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085396"
---
# <a name="crenderedinputpincrenderedinputpin-constructor"></a><span data-ttu-id="23a4e-103">CRenderedInputPin. CRenderedInputPin 函數</span><span class="sxs-lookup"><span data-stu-id="23a4e-103">CRenderedInputPin.CRenderedInputPin constructor</span></span>

<span data-ttu-id="23a4e-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="23a4e-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="23a4e-105">語法</span><span class="sxs-lookup"><span data-stu-id="23a4e-105">Syntax</span></span>


```C++
CRenderedInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="23a4e-106">參數</span><span class="sxs-lookup"><span data-stu-id="23a4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23a4e-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="23a4e-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="23a4e-108">包含物件之偵錯工具名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="23a4e-108">String containing the debug name of the object.</span></span> <span data-ttu-id="23a4e-109">如需詳細資訊，請參閱 [**CBaseObject 類別**](cbaseobject.md)。</span><span class="sxs-lookup"><span data-stu-id="23a4e-109">For more information, see [**CBaseObject Class**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="23a4e-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="23a4e-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="23a4e-111">建立此釘選之篩選準則的指標。</span><span class="sxs-lookup"><span data-stu-id="23a4e-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="23a4e-112">*pLock*</span><span class="sxs-lookup"><span data-stu-id="23a4e-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="23a4e-113">[**CCritSec**](ccritsec.md)鎖定的指標，用來序列化狀態變更。</span><span class="sxs-lookup"><span data-stu-id="23a4e-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="23a4e-114">這可以是與 filter lock [**CBaseFilter：： m \_ pLock**](cbasefilter-m-plock.md)相同的重要區段。</span><span class="sxs-lookup"><span data-stu-id="23a4e-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="23a4e-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="23a4e-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="23a4e-116">變數的指標，此變數會接收 **HRESULT** 值，指出方法的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="23a4e-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="23a4e-117">*pName*</span><span class="sxs-lookup"><span data-stu-id="23a4e-117">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="23a4e-118">包含 pin 名稱的寬字元字串 (也用來作為 pin 識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="23a4e-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="23a4e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="23a4e-119">Requirements</span></span>



| <span data-ttu-id="23a4e-120">需求</span><span class="sxs-lookup"><span data-stu-id="23a4e-120">Requirement</span></span> | <span data-ttu-id="23a4e-121">值</span><span class="sxs-lookup"><span data-stu-id="23a4e-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23a4e-122">標頭</span><span class="sxs-lookup"><span data-stu-id="23a4e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="23a4e-123"><dt>Amextra (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="23a4e-123"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="23a4e-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="23a4e-124">Library</span></span><br/> | <dl> <span data-ttu-id="23a4e-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="23a4e-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23a4e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23a4e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23a4e-127">**CRenderedInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="23a4e-127">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




