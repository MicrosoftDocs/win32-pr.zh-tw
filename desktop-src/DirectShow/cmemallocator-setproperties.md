---
description: SetProperties 方法會指定要配置的緩衝區數目和每個緩衝區的大小。
ms.assetid: 01f63379-1d66-4a72-b87c-de55504b0bb4
title: 'CMemAllocator. SetProperties 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8505916245cca81fdd84132e4523fe9dd03b971b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000833"
---
# <a name="cmemallocatorsetproperties-method"></a><span data-ttu-id="a5fe0-103">CMemAllocator. SetProperties 方法</span><span class="sxs-lookup"><span data-stu-id="a5fe0-103">CMemAllocator.SetProperties method</span></span>

<span data-ttu-id="a5fe0-104">`SetProperties`方法會指定要配置的緩衝區數目和每個緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="a5fe0-104">The `SetProperties` method specifies the number of buffers to allocate and the size of each buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5fe0-105">語法</span><span class="sxs-lookup"><span data-stu-id="a5fe0-105">Syntax</span></span>


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a><span data-ttu-id="a5fe0-106">參數</span><span class="sxs-lookup"><span data-stu-id="a5fe0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5fe0-107">*pRequest*</span><span class="sxs-lookup"><span data-stu-id="a5fe0-107">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="a5fe0-108">配置器 [**\_ 屬性**](/windows/win32/api/strmif/ns-strmif-allocator_properties) 結構的指標，其中包含緩衝區需求。</span><span class="sxs-lookup"><span data-stu-id="a5fe0-108">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the buffer requirements.</span></span>

</dd> <dt>

<span data-ttu-id="a5fe0-109">*pActual*</span><span class="sxs-lookup"><span data-stu-id="a5fe0-109">*pActual*</span></span> 
</dt> <dd>

<span data-ttu-id="a5fe0-110">配置器 **\_ 屬性** 結構的指標，此結構會接收實際的緩衝區屬性。</span><span class="sxs-lookup"><span data-stu-id="a5fe0-110">Pointer to an **ALLOCATOR\_PROPERTIES** structure that receives the actual buffer properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5fe0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a5fe0-111">Return value</span></span>

<span data-ttu-id="a5fe0-112">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="a5fe0-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="a5fe0-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a5fe0-113">Return code</span></span>                                                                                                 | <span data-ttu-id="a5fe0-114">Description</span><span class="sxs-lookup"><span data-stu-id="a5fe0-114">Description</span></span>                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="a5fe0-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="a5fe0-115"><dt>**S\_OK**</dt></span></span> </dl>                        | <span data-ttu-id="a5fe0-116">成功。</span><span class="sxs-lookup"><span data-stu-id="a5fe0-116">Success.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="a5fe0-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="a5fe0-117"><dt>**E\_POINTER**</dt></span></span> </dl>                   | <span data-ttu-id="a5fe0-118">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="a5fe0-118">**NULL** pointer argument.</span></span><br/>                                 |
| <dl> <span data-ttu-id="a5fe0-119"><dt>**VFW \_ E \_ 已 \_ 認可**</dt></span><span class="sxs-lookup"><span data-stu-id="a5fe0-119"><dt>**VFW\_E\_ALREADY\_COMMITTED**</dt></span></span> </dl>   | <span data-ttu-id="a5fe0-120">當篩選準則為作用中時，無法變更配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="a5fe0-120">Cannot change allocated memory while the filter is active.</span></span><br/> |
| <dl> <span data-ttu-id="a5fe0-121"><dt>**VFW \_ E \_ BADALIGN**</dt></span><span class="sxs-lookup"><span data-stu-id="a5fe0-121"><dt>**VFW\_E\_BADALIGN**</dt></span></span> </dl>             | <span data-ttu-id="a5fe0-122">指定了不正確對齊方式。</span><span class="sxs-lookup"><span data-stu-id="a5fe0-122">An invalid alignment was specified.</span></span><br/>                        |
| <dl> <span data-ttu-id="a5fe0-123"><dt>**未處理的 VFW \_ E \_ 緩衝區 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5fe0-123"><dt>**VFW\_E\_BUFFERS\_OUTSTANDING**</dt></span></span> </dl> | <span data-ttu-id="a5fe0-124">一或多個緩衝區仍在使用中。</span><span class="sxs-lookup"><span data-stu-id="a5fe0-124">One or more buffers are still active.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="a5fe0-125">備註</span><span class="sxs-lookup"><span data-stu-id="a5fe0-125">Remarks</span></span>

<span data-ttu-id="a5fe0-126">這個方法會覆寫 [**CBaseAllocator：： SetProperties**](cbaseallocator-setproperties.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="a5fe0-126">This method overrides the [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method.</span></span>

<span data-ttu-id="a5fe0-127">由配置器 **\_ 屬性** 結構的 **cbAlign** 成員所指定的緩衝區對齊，必須是2的乘冪。</span><span class="sxs-lookup"><span data-stu-id="a5fe0-127">The buffer alignment, specified by the **cbAlign** member of the **ALLOCATOR\_PROPERTIES** structure, must be an even power of two.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5fe0-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5fe0-128">Requirements</span></span>



| <span data-ttu-id="a5fe0-129">需求</span><span class="sxs-lookup"><span data-stu-id="a5fe0-129">Requirement</span></span> | <span data-ttu-id="a5fe0-130">值</span><span class="sxs-lookup"><span data-stu-id="a5fe0-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5fe0-131">標頭</span><span class="sxs-lookup"><span data-stu-id="a5fe0-131">Header</span></span><br/>  | <dl> <span data-ttu-id="a5fe0-132"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a5fe0-132"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a5fe0-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="a5fe0-133">Library</span></span><br/> | <dl> <span data-ttu-id="a5fe0-134"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a5fe0-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5fe0-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5fe0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5fe0-136">**CMemAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="a5fe0-136">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




