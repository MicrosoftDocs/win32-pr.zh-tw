---
description: 函式方法。
ms.assetid: e8cb5f1d-171f-4bf8-8ab6-6e547c4678d2
title: 'CBasePin. CBasePin (Amfilter. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CBasePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd4883d3d8e906e1da2f377344b735037c5e5cd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996480"
---
# <a name="cbasepincbasepin-constructor"></a><span data-ttu-id="6e81c-103">CBasePin. CBasePin 函數</span><span class="sxs-lookup"><span data-stu-id="6e81c-103">CBasePin.CBasePin constructor</span></span>

<span data-ttu-id="6e81c-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="6e81c-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e81c-105">語法</span><span class="sxs-lookup"><span data-stu-id="6e81c-105">Syntax</span></span>


```C++
CBasePin(
   TCHAR         *pObjectName,
   CBaseFilter   *pFilter,
   CCritSec      *pLock,
   HRESULT       *phr,
   LPCWSTR       pName,
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a><span data-ttu-id="6e81c-106">參數</span><span class="sxs-lookup"><span data-stu-id="6e81c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e81c-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="6e81c-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="6e81c-108">包含物件之偵錯工具名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="6e81c-108">String containing the debug name for the object.</span></span> <span data-ttu-id="6e81c-109">如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md)。</span><span class="sxs-lookup"><span data-stu-id="6e81c-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e81c-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="6e81c-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="6e81c-111">建立此釘選之篩選準則的指標。</span><span class="sxs-lookup"><span data-stu-id="6e81c-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="6e81c-112">*pLock*</span><span class="sxs-lookup"><span data-stu-id="6e81c-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="6e81c-113">[**CCritSec**](ccritsec.md)鎖定的指標，用來序列化狀態變更。</span><span class="sxs-lookup"><span data-stu-id="6e81c-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="6e81c-114">可以是與 filter lock [**CBaseFilter：： m \_ pLock**](cbasefilter-m-plock.md)相同的重要區段。</span><span class="sxs-lookup"><span data-stu-id="6e81c-114">Can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e81c-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="6e81c-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="6e81c-116">變數的指標，此變數會接收 **HRESULT** 值，指出方法的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="6e81c-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="6e81c-117">在建立物件之前，將值初始化為「 \_ 確定」。</span><span class="sxs-lookup"><span data-stu-id="6e81c-117">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="6e81c-118">只有在發生錯誤時，才會變更此值。</span><span class="sxs-lookup"><span data-stu-id="6e81c-118">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="6e81c-119">*pName*</span><span class="sxs-lookup"><span data-stu-id="6e81c-119">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="6e81c-120">包含 pin 名稱的寬字元字串。</span><span class="sxs-lookup"><span data-stu-id="6e81c-120">Wide-character string containing the name of the pin.</span></span> <span data-ttu-id="6e81c-121">如需詳細資訊，請參閱 [**CBasePin：： QueryPinInfo**](cbasepin-querypininfo.md)。</span><span class="sxs-lookup"><span data-stu-id="6e81c-121">For more information, see [**CBasePin::QueryPinInfo**](cbasepin-querypininfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e81c-122">*dir*</span><span class="sxs-lookup"><span data-stu-id="6e81c-122">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="6e81c-123">指定釘選方向的 [**釘選 \_ 方向**](/windows/win32/api/strmif/ne-strmif-pin_direction) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="6e81c-123">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumeration specifying the direction of the pin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e81c-124">備註</span><span class="sxs-lookup"><span data-stu-id="6e81c-124">Remarks</span></span>

<span data-ttu-id="6e81c-125">*PLock* 所指定的重要區段會將釘選的狀態序列化，包括其線上狀態、配置器的選擇、媒體類型，以及排清作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="6e81c-125">The critical section specified by *pLock* serializes the pin's state, including its connection status, choice of allocator, media type, and the status of flush operations.</span></span> <span data-ttu-id="6e81c-126">請勿使用這個重要區段來序列化串流作業。</span><span class="sxs-lookup"><span data-stu-id="6e81c-126">Do not use this critical section to serialize streaming operations.</span></span> <span data-ttu-id="6e81c-127">如需詳細資訊，請參閱 [篩選圖形中的](data-flow-in-the-filter-graph.md)資料流程。</span><span class="sxs-lookup"><span data-stu-id="6e81c-127">For more information, see [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).</span></span>

<span data-ttu-id="6e81c-128">篩選可能會在其函式方法中建立釘選，因此在此時， *pFilter* 指標可能不會參考有效的物件。</span><span class="sxs-lookup"><span data-stu-id="6e81c-128">A filter might create pins in its constructor method, so at this point the *pFilter* pointer might not refer to a valid object.</span></span> <span data-ttu-id="6e81c-129">儲存指標，但不要在釘選的函式內進行取值。</span><span class="sxs-lookup"><span data-stu-id="6e81c-129">Store the pointer, but do not dereference it while inside the pin's constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e81c-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e81c-130">Requirements</span></span>



| <span data-ttu-id="6e81c-131">需求</span><span class="sxs-lookup"><span data-stu-id="6e81c-131">Requirement</span></span> | <span data-ttu-id="6e81c-132">值</span><span class="sxs-lookup"><span data-stu-id="6e81c-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e81c-133">標頭</span><span class="sxs-lookup"><span data-stu-id="6e81c-133">Header</span></span><br/>  | <dl> <span data-ttu-id="6e81c-134"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6e81c-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6e81c-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="6e81c-135">Library</span></span><br/> | <dl> <span data-ttu-id="6e81c-136"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6e81c-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e81c-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e81c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e81c-138">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="6e81c-138">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




