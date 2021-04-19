---
description: GetAllocatorRequirements 方法會抓取輸入 pin 所要求的配置器屬性。
ms.assetid: 81564924-6d5b-4b2a-b549-e3f358f18371
title: 'CBaseInputPin. GetAllocatorRequirements 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0239d226ea57ed5953fa65b925eeffaa0b13df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990552"
---
# <a name="cbaseinputpingetallocatorrequirements-method"></a><span data-ttu-id="cb7bd-103">CBaseInputPin. GetAllocatorRequirements 方法</span><span class="sxs-lookup"><span data-stu-id="cb7bd-103">CBaseInputPin.GetAllocatorRequirements method</span></span>

<span data-ttu-id="cb7bd-104">方法會抓取 `GetAllocatorRequirements` 輸入 pin 所要求的配置器屬性。</span><span class="sxs-lookup"><span data-stu-id="cb7bd-104">The `GetAllocatorRequirements` method retrieves the allocator properties requested by the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb7bd-105">語法</span><span class="sxs-lookup"><span data-stu-id="cb7bd-105">Syntax</span></span>


```C++
HRESULT GetAllocatorRequirements(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="cb7bd-106">參數</span><span class="sxs-lookup"><span data-stu-id="cb7bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb7bd-107">*pProps*</span><span class="sxs-lookup"><span data-stu-id="cb7bd-107">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="cb7bd-108">配置器 [**\_ 屬性**](/windows/win32/api/strmif/ns-strmif-allocator_properties) 結構的指標，該結構會填入需求。</span><span class="sxs-lookup"><span data-stu-id="cb7bd-108">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure, which is filled in with the requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb7bd-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="cb7bd-109">Return value</span></span>

<span data-ttu-id="cb7bd-110">傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="cb7bd-110">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb7bd-111">備註</span><span class="sxs-lookup"><span data-stu-id="cb7bd-111">Remarks</span></span>

<span data-ttu-id="cb7bd-112">當輸出釘選初始化記憶體配置器時，它可以呼叫這個方法來判斷輸入的 pin 是否有任何緩衝區需求。</span><span class="sxs-lookup"><span data-stu-id="cb7bd-112">When an output pin initializes a memory allocator, it can call this method to determine whether the input pin has any buffer requirements.</span></span> <span data-ttu-id="cb7bd-113">如需詳細資訊，請參閱 [**CBaseOutputPin：:D ecideallocator**](cbaseoutputpin-decideallocator.md)。</span><span class="sxs-lookup"><span data-stu-id="cb7bd-113">For more information, see [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md).</span></span>

<span data-ttu-id="cb7bd-114">您可以選擇是否要執行此方法。</span><span class="sxs-lookup"><span data-stu-id="cb7bd-114">Implementing this method is optional.</span></span> <span data-ttu-id="cb7bd-115">如果篩選準則有特定的對齊或首碼需求，請覆寫這個方法。</span><span class="sxs-lookup"><span data-stu-id="cb7bd-115">If the filter has specific alignment or prefix requirements, override this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb7bd-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb7bd-116">Requirements</span></span>



| <span data-ttu-id="cb7bd-117">需求</span><span class="sxs-lookup"><span data-stu-id="cb7bd-117">Requirement</span></span> | <span data-ttu-id="cb7bd-118">值</span><span class="sxs-lookup"><span data-stu-id="cb7bd-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb7bd-119">標頭</span><span class="sxs-lookup"><span data-stu-id="cb7bd-119">Header</span></span><br/>  | <dl> <span data-ttu-id="cb7bd-120"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="cb7bd-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cb7bd-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="cb7bd-121">Library</span></span><br/> | <dl> <span data-ttu-id="cb7bd-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="cb7bd-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb7bd-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb7bd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb7bd-124">**CBaseInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="cb7bd-124">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




