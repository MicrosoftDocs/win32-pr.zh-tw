---
description: CTransformOutputPin. DecideBufferSize 方法-DecideBufferSize 方法會設定緩衝區需求。
ms.assetid: cdf9e384-623e-46a6-b123-d881fe21fb09
title: 'CTransformOutputPin. DecideBufferSize 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bc84eaf5e95a19436de5429ce018352cdaa286e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084836"
---
# <a name="ctransformoutputpindecidebuffersize-method"></a><span data-ttu-id="cd1d3-103">CTransformOutputPin. DecideBufferSize 方法</span><span class="sxs-lookup"><span data-stu-id="cd1d3-103">CTransformOutputPin.DecideBufferSize method</span></span>

<span data-ttu-id="cd1d3-104">`DecideBufferSize`方法會設定緩衝區需求。</span><span class="sxs-lookup"><span data-stu-id="cd1d3-104">The `DecideBufferSize` method sets the buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd1d3-105">語法</span><span class="sxs-lookup"><span data-stu-id="cd1d3-105">Syntax</span></span>


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
);
```



## <a name="parameters"></a><span data-ttu-id="cd1d3-106">參數</span><span class="sxs-lookup"><span data-stu-id="cd1d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd1d3-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="cd1d3-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="cd1d3-108">配置器的 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="cd1d3-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="cd1d3-109">*ppropInputRequest*</span><span class="sxs-lookup"><span data-stu-id="cd1d3-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="cd1d3-110">指向配置 [**器 \_ 屬性**](/windows/win32/api/strmif/ns-strmif-allocator_properties) 結構的指標，其中包含輸入釘選的緩衝區需求。</span><span class="sxs-lookup"><span data-stu-id="cd1d3-110">Pointer an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd1d3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="cd1d3-111">Return value</span></span>

<span data-ttu-id="cd1d3-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="cd1d3-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd1d3-113">備註</span><span class="sxs-lookup"><span data-stu-id="cd1d3-113">Remarks</span></span>

<span data-ttu-id="cd1d3-114">這個方法會覆寫 [**CBaseOutputPin：:D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="cd1d3-114">This method overrides the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) method.</span></span> <span data-ttu-id="cd1d3-115">它會呼叫篩選準則的純虛擬 [**CTransformFilter：:D ecidebuffersize**](ctransformfilter-decidebuffersize.md) 方法，該方法必須是篩選準則的衍生類別。</span><span class="sxs-lookup"><span data-stu-id="cd1d3-115">It calls the filter's pure virtual [**CTransformFilter::DecideBufferSize**](ctransformfilter-decidebuffersize.md) method, which the filter's derived class must implement.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd1d3-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd1d3-116">Requirements</span></span>



| <span data-ttu-id="cd1d3-117">需求</span><span class="sxs-lookup"><span data-stu-id="cd1d3-117">Requirement</span></span> | <span data-ttu-id="cd1d3-118">值</span><span class="sxs-lookup"><span data-stu-id="cd1d3-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd1d3-119">標頭</span><span class="sxs-lookup"><span data-stu-id="cd1d3-119">Header</span></span><br/>  | <dl> <span data-ttu-id="cd1d3-120"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="cd1d3-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cd1d3-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="cd1d3-121">Library</span></span><br/> | <dl> <span data-ttu-id="cd1d3-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="cd1d3-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




