---
description: 函式方法。
ms.assetid: e697e377-6407-4316-9f04-fe3bdb814175
title: 'CBaseAllocator. CBaseAllocator (Amfilter. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98a1ba1163058f92fba666177d0ff82331dd528c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985933"
---
# <a name="cbaseallocatorcbaseallocator-constructor"></a><span data-ttu-id="3bb1f-103">CBaseAllocator. CBaseAllocator 函數</span><span class="sxs-lookup"><span data-stu-id="3bb1f-103">CBaseAllocator.CBaseAllocator constructor</span></span>

<span data-ttu-id="3bb1f-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="3bb1f-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bb1f-105">語法</span><span class="sxs-lookup"><span data-stu-id="3bb1f-105">Syntax</span></span>


```C++
CBaseAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   BOOL      bEvent = TRUE,
   BOOL      fEnableReleaseCallback = FALSE
);
```



## <a name="parameters"></a><span data-ttu-id="3bb1f-106">參數</span><span class="sxs-lookup"><span data-stu-id="3bb1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bb1f-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="3bb1f-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="3bb1f-108">字串的指標，其中包含配置器的偵錯工具名稱。</span><span class="sxs-lookup"><span data-stu-id="3bb1f-108">Pointer to a string containing the debug name of the allocator.</span></span> <span data-ttu-id="3bb1f-109">如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md)。</span><span class="sxs-lookup"><span data-stu-id="3bb1f-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="3bb1f-110">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="3bb1f-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="3bb1f-111">這個物件之擁有者的指標。</span><span class="sxs-lookup"><span data-stu-id="3bb1f-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="3bb1f-112">如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="3bb1f-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="3bb1f-113">否則，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3bb1f-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3bb1f-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="3bb1f-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="3bb1f-115">**HRESULT** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="3bb1f-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="3bb1f-116">建立物件之前，請先將值設定為 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="3bb1f-116">Set the value to S\_OK before creating the object.</span></span> <span data-ttu-id="3bb1f-117">如果此函式失敗，則會將值設定為錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3bb1f-117">If the constructor fails, the value is set to an error code.</span></span>

</dd> <dt>

<span data-ttu-id="3bb1f-118">*bEvent*</span><span class="sxs-lookup"><span data-stu-id="3bb1f-118">*bEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="3bb1f-119">指出是否要建立信號的布林值。</span><span class="sxs-lookup"><span data-stu-id="3bb1f-119">Boolean value indicating whether to create a semaphore.</span></span> <span data-ttu-id="3bb1f-120">若 **為 TRUE**，配置器會建立信號 ([**CBaseAllocator：： m \_ hSem**](cbaseallocator-m-hsem.md)) ，只要範例變成可用，就會收到信號。</span><span class="sxs-lookup"><span data-stu-id="3bb1f-120">If **TRUE**, the allocator creates a semaphore ([**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md)), which is signaled whenever a sample becomes available.</span></span> <span data-ttu-id="3bb1f-121">如果您要執行不需要信號的衍生類別，請將值設定為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="3bb1f-121">Set the value to **FALSE** if you are implementing a derived class that does not require a semaphore.</span></span>

</dd> <dt>

<span data-ttu-id="3bb1f-122">*fEnableReleaseCallback*</span><span class="sxs-lookup"><span data-stu-id="3bb1f-122">*fEnableReleaseCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="3bb1f-123">指出是否已啟用發行回呼機制的布林值。</span><span class="sxs-lookup"><span data-stu-id="3bb1f-123">Boolean value indicating whether the release callback mechanism is enabled.</span></span> <span data-ttu-id="3bb1f-124">如果您想要提供回呼介面（當釋放緩衝區時呼叫），請將此值設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="3bb1f-124">Set the value to **TRUE** if you want to supply a callback interface, which is called when buffers are released.</span></span> <span data-ttu-id="3bb1f-125">藉由呼叫 [**CBaseAllocator：： SetNotify**](cbaseallocator-setnotify.md) 方法來指定回呼。</span><span class="sxs-lookup"><span data-stu-id="3bb1f-125">Specify the callback by calling the [**CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3bb1f-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="3bb1f-126">Requirements</span></span>



| <span data-ttu-id="3bb1f-127">需求</span><span class="sxs-lookup"><span data-stu-id="3bb1f-127">Requirement</span></span> | <span data-ttu-id="3bb1f-128">值</span><span class="sxs-lookup"><span data-stu-id="3bb1f-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bb1f-129">標頭</span><span class="sxs-lookup"><span data-stu-id="3bb1f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3bb1f-130"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3bb1f-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3bb1f-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="3bb1f-131">Library</span></span><br/> | <dl> <span data-ttu-id="3bb1f-132"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3bb1f-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bb1f-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3bb1f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bb1f-134">**CBaseAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="3bb1f-134">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




