---
description: CTransInPlaceFilter. DecideBufferSize 方法-DecideBufferSize 方法會設定輸出釘選的緩衝區需求。
ms.assetid: f1ddc39e-dcd5-4a44-8a8e-e384692408e1
title: 'CTransInPlaceFilter. DecideBufferSize 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b3ffb3ec7b1ef59c6e7f3d49e39fbe69e8cc1c08
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094826"
---
# <a name="ctransinplacefilterdecidebuffersize-method"></a><span data-ttu-id="96993-103">CTransInPlaceFilter. DecideBufferSize 方法</span><span class="sxs-lookup"><span data-stu-id="96993-103">CTransInPlaceFilter.DecideBufferSize method</span></span>

<span data-ttu-id="96993-104">`DecideBufferSize`方法會設定輸出釘選的緩衝區需求。</span><span class="sxs-lookup"><span data-stu-id="96993-104">The `DecideBufferSize` method sets the output pin's buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="96993-105">語法</span><span class="sxs-lookup"><span data-stu-id="96993-105">Syntax</span></span>


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProperties
);
```



## <a name="parameters"></a><span data-ttu-id="96993-106">參數</span><span class="sxs-lookup"><span data-stu-id="96993-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96993-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="96993-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="96993-108">輸出釘選所使用之 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="96993-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) object used by the output pin.</span></span>

</dd> <dt>

<span data-ttu-id="96993-109">*pProperties*</span><span class="sxs-lookup"><span data-stu-id="96993-109">*pProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="96993-110">依配置器 [**\_ 屬性**](/windows/win32/api/strmif/ns-strmif-allocator_properties) 結構所指定的計數、大小和對齊所要求配置器屬性的指標。</span><span class="sxs-lookup"><span data-stu-id="96993-110">Pointer to the requested allocator properties for count, size, and alignment, as specified by the [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96993-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="96993-111">Return value</span></span>

<span data-ttu-id="96993-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="96993-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="96993-113">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="96993-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="96993-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="96993-114">Return code</span></span>                                                                            | <span data-ttu-id="96993-115">Description</span><span class="sxs-lookup"><span data-stu-id="96993-115">Description</span></span>        |
|----------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="96993-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="96993-116"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="96993-117">Success</span><span class="sxs-lookup"><span data-stu-id="96993-117">Success</span></span><br/> |
| <dl> <span data-ttu-id="96993-118"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="96993-118"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="96993-119">失敗</span><span class="sxs-lookup"><span data-stu-id="96993-119">Failure</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="96993-120">備註</span><span class="sxs-lookup"><span data-stu-id="96993-120">Remarks</span></span>

<span data-ttu-id="96993-121">當 **CTransInPlaceFilter** 類別需要提供緩衝區大小給下游篩選準則時，就會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="96993-121">This method is called when the **CTransInPlaceFilter** class needs to provide a buffer size to the downstream filter.</span></span> <span data-ttu-id="96993-122">如果 **CTransInPlaceFilter** 篩選已連接上游，則會使用上游連接上的配置器屬性。</span><span class="sxs-lookup"><span data-stu-id="96993-122">If the **CTransInPlaceFilter** filter is already connected upstream, it uses the allocator properties on the upstream pin connection.</span></span> <span data-ttu-id="96993-123">否則，它會將緩衝區大小設定為1個位元組，以做為暫時的預留位置值。</span><span class="sxs-lookup"><span data-stu-id="96993-123">Otherwise, it sets the buffer size to 1 byte as a temporary place-holder value.</span></span> <span data-ttu-id="96993-124">當上游篩選連接時， **CTransInPlaceFilter** 類別會重新配置下游配置器。</span><span class="sxs-lookup"><span data-stu-id="96993-124">When the upstream filter connects, the **CTransInPlaceFilter** class renegotiates the downstream allocator.</span></span> <span data-ttu-id="96993-125">如需此類別中 pin 連接程式的詳細資訊，請參閱 [**CTransInPlaceFilter 類別**](ctransinplacefilter.md)。</span><span class="sxs-lookup"><span data-stu-id="96993-125">For more information about the pin connection process in this class, see [**CTransInPlaceFilter Class**](ctransinplacefilter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="96993-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="96993-126">Requirements</span></span>



| <span data-ttu-id="96993-127">需求</span><span class="sxs-lookup"><span data-stu-id="96993-127">Requirement</span></span> | <span data-ttu-id="96993-128">值</span><span class="sxs-lookup"><span data-stu-id="96993-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96993-129">標頭</span><span class="sxs-lookup"><span data-stu-id="96993-129">Header</span></span><br/>  | <dl> <span data-ttu-id="96993-130"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="96993-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="96993-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="96993-131">Library</span></span><br/> | <dl> <span data-ttu-id="96993-132"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="96993-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96993-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96993-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96993-134">**CTransInPlaceFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="96993-134">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




