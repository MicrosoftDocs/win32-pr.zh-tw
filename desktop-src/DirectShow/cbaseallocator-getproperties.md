---
description: GetProperties 方法會抓取配置器將建立的緩衝區數目，以及緩衝區屬性。 這個方法會實 IMemAllocator：： GetProperties 方法。
ms.assetid: ccee4d69-52fc-4e3c-b6a4-787914708be4
title: 'CBaseAllocator. GetProperties 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abf143b11b6dd67fca6c87f9a31ce69f18951311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994089"
---
# <a name="cbaseallocatorgetproperties-method"></a><span data-ttu-id="c2fc7-104">CBaseAllocator. GetProperties 方法</span><span class="sxs-lookup"><span data-stu-id="c2fc7-104">CBaseAllocator.GetProperties method</span></span>

<span data-ttu-id="c2fc7-105">方法會抓取配置器 `GetProperties` 將建立的緩衝區數目，以及緩衝區屬性。</span><span class="sxs-lookup"><span data-stu-id="c2fc7-105">The `GetProperties` method retrieves the number of buffers that the allocator will create, and the buffer properties.</span></span> <span data-ttu-id="c2fc7-106">這個方法會實 [**IMemAllocator：： GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) 方法。</span><span class="sxs-lookup"><span data-stu-id="c2fc7-106">This method implements the [**IMemAllocator::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2fc7-107">語法</span><span class="sxs-lookup"><span data-stu-id="c2fc7-107">Syntax</span></span>


```C++
HRESULT GetProperties(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="c2fc7-108">參數</span><span class="sxs-lookup"><span data-stu-id="c2fc7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2fc7-109">*pProps*</span><span class="sxs-lookup"><span data-stu-id="c2fc7-109">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="c2fc7-110">配置器 [**\_ 屬性**](/windows/win32/api/strmif/ns-strmif-allocator_properties) 結構的指標，此結構會接收配置器屬性。</span><span class="sxs-lookup"><span data-stu-id="c2fc7-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that receives the allocator properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2fc7-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2fc7-111">Return value</span></span>

<span data-ttu-id="c2fc7-112">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="c2fc7-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2fc7-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2fc7-113">Requirements</span></span>



| <span data-ttu-id="c2fc7-114">需求</span><span class="sxs-lookup"><span data-stu-id="c2fc7-114">Requirement</span></span> | <span data-ttu-id="c2fc7-115">值</span><span class="sxs-lookup"><span data-stu-id="c2fc7-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2fc7-116">標頭</span><span class="sxs-lookup"><span data-stu-id="c2fc7-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c2fc7-117"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c2fc7-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c2fc7-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="c2fc7-118">Library</span></span><br/> | <dl> <span data-ttu-id="c2fc7-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c2fc7-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2fc7-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2fc7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2fc7-121">**CBaseAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="c2fc7-121">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




