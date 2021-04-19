---
description: SetProperties 方法會指定要配置的緩衝區數目和每個緩衝區的大小。 這個方法會覆寫 CBaseAllocator：： SetProperties 方法。
ms.assetid: 8d419432-a9a7-44fb-b916-8dacd08eb6ec
title: 'CImageAllocator. SetProperties 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c04501fe3511d9cdd45f3513c68082d2ffece0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984818"
---
# <a name="cimageallocatorsetproperties-method"></a><span data-ttu-id="91900-104">CImageAllocator. SetProperties 方法</span><span class="sxs-lookup"><span data-stu-id="91900-104">CImageAllocator.SetProperties method</span></span>

<span data-ttu-id="91900-105">`SetProperties`方法會指定要配置的緩衝區數目和每個緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="91900-105">The `SetProperties` method specifies the number of buffers to allocate and the size of each buffer.</span></span> <span data-ttu-id="91900-106">這個方法會覆寫 [**CBaseAllocator：： SetProperties**](cbaseallocator-setproperties.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="91900-106">This method overrides the [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="91900-107">語法</span><span class="sxs-lookup"><span data-stu-id="91900-107">Syntax</span></span>


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a><span data-ttu-id="91900-108">參數</span><span class="sxs-lookup"><span data-stu-id="91900-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91900-109">*pRequest*</span><span class="sxs-lookup"><span data-stu-id="91900-109">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="91900-110">配置器 [**\_ 屬性**](/windows/win32/api/strmif/ns-strmif-allocator_properties) 結構的指標，其中包含緩衝區需求。</span><span class="sxs-lookup"><span data-stu-id="91900-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the buffer requirements.</span></span>

</dd> <dt>

<span data-ttu-id="91900-111">*pActual*</span><span class="sxs-lookup"><span data-stu-id="91900-111">*pActual*</span></span> 
</dt> <dd>

<span data-ttu-id="91900-112">配置器 **\_ 屬性** 結構的指標，此結構會接收實際的緩衝區屬性。</span><span class="sxs-lookup"><span data-stu-id="91900-112">Pointer to an **ALLOCATOR\_PROPERTIES** structure that receives the actual buffer properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91900-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="91900-113">Return value</span></span>

<span data-ttu-id="91900-114">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="91900-114">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="91900-115">備註</span><span class="sxs-lookup"><span data-stu-id="91900-115">Remarks</span></span>

<span data-ttu-id="91900-116">這個方法會呼叫 [**CImageAllocator：： CheckSizes**](cimageallocator-checksizes.md) 來驗證要求的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="91900-116">This method calls [**CImageAllocator::CheckSizes**](cimageallocator-checksizes.md) to validate the requested buffer size.</span></span> <span data-ttu-id="91900-117">它也會呼叫的基類版本 `SetProperties` 。</span><span class="sxs-lookup"><span data-stu-id="91900-117">It also calls the base-class version of `SetProperties`.</span></span>

## <a name="requirements"></a><span data-ttu-id="91900-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="91900-118">Requirements</span></span>



| <span data-ttu-id="91900-119">需求</span><span class="sxs-lookup"><span data-stu-id="91900-119">Requirement</span></span> | <span data-ttu-id="91900-120">值</span><span class="sxs-lookup"><span data-stu-id="91900-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91900-121">標頭</span><span class="sxs-lookup"><span data-stu-id="91900-121">Header</span></span><br/>  | <dl> <span data-ttu-id="91900-122"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="91900-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="91900-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="91900-123">Library</span></span><br/> | <dl> <span data-ttu-id="91900-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="91900-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91900-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91900-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91900-126">**CImageAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="91900-126">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




