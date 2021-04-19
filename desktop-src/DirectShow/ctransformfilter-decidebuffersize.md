---
description: DecideBufferSize 方法會設定輸出 pin 的緩衝區需求。
ms.assetid: 33e41668-b4f6-4142-b22e-2ddfb96332df
title: 'CTransformFilter. DecideBufferSize 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71a506a9c9cd16a014418b24ad3fbd1186d6f48f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000024"
---
# <a name="ctransformfilterdecidebuffersize-method"></a><span data-ttu-id="e1d8e-103">CTransformFilter. DecideBufferSize 方法</span><span class="sxs-lookup"><span data-stu-id="e1d8e-103">CTransformFilter.DecideBufferSize method</span></span>

<span data-ttu-id="e1d8e-104">`DecideBufferSize`方法會設定輸出釘選的緩衝區需求。</span><span class="sxs-lookup"><span data-stu-id="e1d8e-104">The `DecideBufferSize` method sets the output pin's buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1d8e-105">語法</span><span class="sxs-lookup"><span data-stu-id="e1d8e-105">Syntax</span></span>


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="e1d8e-106">參數</span><span class="sxs-lookup"><span data-stu-id="e1d8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1d8e-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="e1d8e-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="e1d8e-108">輸出釘選器上 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="e1d8e-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface on the output pin's allocator.</span></span>

</dd> <dt>

<span data-ttu-id="e1d8e-109">*ppropInputRequest*</span><span class="sxs-lookup"><span data-stu-id="e1d8e-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="e1d8e-110">配置器 [**\_ 屬性**](/windows/win32/api/strmif/ns-strmif-allocator_properties) 結構的指標，其中包含來自下游輸入圖釘的緩衝區需求。</span><span class="sxs-lookup"><span data-stu-id="e1d8e-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains buffer requirements from the downstream input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1d8e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e1d8e-111">Return value</span></span>

<span data-ttu-id="e1d8e-112">傳回 S \_ OK 或其他 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="e1d8e-112">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1d8e-113">備註</span><span class="sxs-lookup"><span data-stu-id="e1d8e-113">Remarks</span></span>

<span data-ttu-id="e1d8e-114">輸出釘選的 [**CTransformOutputPin：:D ecidebuffersize**](ctransformoutputpin-decidebuffersize.md) 方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="e1d8e-114">The output pin's [**CTransformOutputPin::DecideBufferSize**](ctransformoutputpin-decidebuffersize.md) method calls this method.</span></span> <span data-ttu-id="e1d8e-115">衍生的類別必須執行此方法。</span><span class="sxs-lookup"><span data-stu-id="e1d8e-115">The derived class must implement this method.</span></span> <span data-ttu-id="e1d8e-116">如需詳細資訊，請參閱 [**CBaseOutputPin：:D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md)。</span><span class="sxs-lookup"><span data-stu-id="e1d8e-116">For more information, see [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1d8e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1d8e-117">Requirements</span></span>



| <span data-ttu-id="e1d8e-118">需求</span><span class="sxs-lookup"><span data-stu-id="e1d8e-118">Requirement</span></span> | <span data-ttu-id="e1d8e-119">值</span><span class="sxs-lookup"><span data-stu-id="e1d8e-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1d8e-120">標頭</span><span class="sxs-lookup"><span data-stu-id="e1d8e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e1d8e-121"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e1d8e-121"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e1d8e-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="e1d8e-122">Library</span></span><br/> | <dl> <span data-ttu-id="e1d8e-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e1d8e-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1d8e-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1d8e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1d8e-125">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="e1d8e-125">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




