---
description: SetProperties 方法會指定要配置的緩衝區數目和每個緩衝區的大小。 這個方法會實 IMemAllocator：： SetProperties 方法。
ms.assetid: f53c22a4-c01d-4d2f-81f0-bedf8f2ae5f0
title: 'CBaseAllocator. SetProperties 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 000da3ee359ad727e3af972fc4aa6d0dbbb9133e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987833"
---
# <a name="cbaseallocatorsetproperties-method"></a><span data-ttu-id="2a23a-104">CBaseAllocator. SetProperties 方法</span><span class="sxs-lookup"><span data-stu-id="2a23a-104">CBaseAllocator.SetProperties method</span></span>

<span data-ttu-id="2a23a-105">`SetProperties`方法會指定要配置的緩衝區數目和每個緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="2a23a-105">The `SetProperties` method specifies the number of buffers to allocate and the size of each buffer.</span></span> <span data-ttu-id="2a23a-106">這個方法會實 [**IMemAllocator：： SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) 方法。</span><span class="sxs-lookup"><span data-stu-id="2a23a-106">This method implements the [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a23a-107">語法</span><span class="sxs-lookup"><span data-stu-id="2a23a-107">Syntax</span></span>


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a><span data-ttu-id="2a23a-108">參數</span><span class="sxs-lookup"><span data-stu-id="2a23a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a23a-109">*pRequest*</span><span class="sxs-lookup"><span data-stu-id="2a23a-109">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="2a23a-110">配置器 [**\_ 屬性**](/windows/win32/api/strmif/ns-strmif-allocator_properties) 結構的指標，其中包含緩衝區需求。</span><span class="sxs-lookup"><span data-stu-id="2a23a-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the buffer requirements.</span></span>

</dd> <dt>

<span data-ttu-id="2a23a-111">*pActual*</span><span class="sxs-lookup"><span data-stu-id="2a23a-111">*pActual*</span></span> 
</dt> <dd>

<span data-ttu-id="2a23a-112">配置器 **\_ 屬性** 結構的指標，此結構會接收實際的緩衝區屬性。</span><span class="sxs-lookup"><span data-stu-id="2a23a-112">Pointer to an **ALLOCATOR\_PROPERTIES** structure that receives the actual buffer properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a23a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2a23a-113">Return value</span></span>

<span data-ttu-id="2a23a-114">傳回下列其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="2a23a-114">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="2a23a-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2a23a-115">Return code</span></span>                                                                                                 | <span data-ttu-id="2a23a-116">Description</span><span class="sxs-lookup"><span data-stu-id="2a23a-116">Description</span></span>                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="2a23a-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2a23a-117"><dt>**S\_OK**</dt></span></span> </dl>                        | <span data-ttu-id="2a23a-118">成功。</span><span class="sxs-lookup"><span data-stu-id="2a23a-118">Success.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="2a23a-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="2a23a-119"><dt>**E\_POINTER**</dt></span></span> </dl>                   | <span data-ttu-id="2a23a-120">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="2a23a-120">**NULL** pointer argument.</span></span><br/>                                 |
| <dl> <span data-ttu-id="2a23a-121"><dt>**VFW \_ E \_ 已 \_ 認可**</dt></span><span class="sxs-lookup"><span data-stu-id="2a23a-121"><dt>**VFW\_E\_ALREADY\_COMMITTED**</dt></span></span> </dl>   | <span data-ttu-id="2a23a-122">當篩選準則為作用中時，無法變更配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="2a23a-122">Cannot change allocated memory while the filter is active.</span></span><br/> |
| <dl> <span data-ttu-id="2a23a-123"><dt>**VFW \_ E \_ BADALIGN**</dt></span><span class="sxs-lookup"><span data-stu-id="2a23a-123"><dt>**VFW\_E\_BADALIGN**</dt></span></span> </dl>             | <span data-ttu-id="2a23a-124">指定了不正確對齊方式。</span><span class="sxs-lookup"><span data-stu-id="2a23a-124">An invalid alignment was specified.</span></span><br/>                        |
| <dl> <span data-ttu-id="2a23a-125"><dt>**未處理的 VFW \_ E \_ 緩衝區 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2a23a-125"><dt>**VFW\_E\_BUFFERS\_OUTSTANDING**</dt></span></span> </dl> | <span data-ttu-id="2a23a-126">一或多個緩衝區仍在使用中。</span><span class="sxs-lookup"><span data-stu-id="2a23a-126">One or more buffers are still active.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="2a23a-127">備註</span><span class="sxs-lookup"><span data-stu-id="2a23a-127">Remarks</span></span>

<span data-ttu-id="2a23a-128">這個方法會指定緩衝區需求，但不會配置任何緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2a23a-128">This method specifies the buffer requirements, but does not allocate any buffers.</span></span> <span data-ttu-id="2a23a-129">呼叫 [**CBaseAllocator：： Commit**](cbaseallocator-commit.md) 方法以配置緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2a23a-129">Call the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method to allocate buffers.</span></span>

<span data-ttu-id="2a23a-130">呼叫端會配置兩個配置器 \_ 屬性結構。</span><span class="sxs-lookup"><span data-stu-id="2a23a-130">The caller allocates two ALLOCATOR\_PROPERTIES structures.</span></span> <span data-ttu-id="2a23a-131">*PRequest* 參數包含呼叫端的緩衝區需求，包括緩衝區數目和每個緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="2a23a-131">The *pRequest* parameter contains the caller's buffer requirements, including the number of buffers and the size of each buffer.</span></span> <span data-ttu-id="2a23a-132">當方法傳回時， *pActual* 參數會包含實際的緩衝區屬性（由配置器所設定）。</span><span class="sxs-lookup"><span data-stu-id="2a23a-132">When the method returns, the *pActual* parameter contains the actual buffer properties, as set by the allocator.</span></span> <span data-ttu-id="2a23a-133">在基類中，假設方法成功，則實際的屬性一律會符合要求的屬性。</span><span class="sxs-lookup"><span data-stu-id="2a23a-133">In the base class, assuming that the method succeeds, the actual properties always match the requested properties.</span></span> <span data-ttu-id="2a23a-134">衍生類別可能會覆寫此行為。</span><span class="sxs-lookup"><span data-stu-id="2a23a-134">Derived classes might override this behavior.</span></span>

<span data-ttu-id="2a23a-135">配置器不得認可，且不能有未處理的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2a23a-135">The allocator must not be committed, and must not have outstanding buffers.</span></span> <span data-ttu-id="2a23a-136">在基類中，對齊必須等於1。</span><span class="sxs-lookup"><span data-stu-id="2a23a-136">In the base class, the alignment must equal 1.</span></span> <span data-ttu-id="2a23a-137">[**CMemAllocator**](cmemallocator.md)類別會覆寫這項需求。</span><span class="sxs-lookup"><span data-stu-id="2a23a-137">The [**CMemAllocator**](cmemallocator.md) class overrides this requirement.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a23a-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a23a-138">Requirements</span></span>



| <span data-ttu-id="2a23a-139">需求</span><span class="sxs-lookup"><span data-stu-id="2a23a-139">Requirement</span></span> | <span data-ttu-id="2a23a-140">值</span><span class="sxs-lookup"><span data-stu-id="2a23a-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a23a-141">標頭</span><span class="sxs-lookup"><span data-stu-id="2a23a-141">Header</span></span><br/>  | <dl> <span data-ttu-id="2a23a-142"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2a23a-142"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2a23a-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="2a23a-143">Library</span></span><br/> | <dl> <span data-ttu-id="2a23a-144"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2a23a-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a23a-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a23a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a23a-146">**CBaseAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="2a23a-146">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




