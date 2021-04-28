---
description: CTransformFilter. DecideBufferSize 方法-DecideBufferSize 方法會設定輸出釘選的緩衝區需求。
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
ms.openlocfilehash: f3276170f1256bba41aa075b0e5f06fb7becbcd2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095146"
---
# <a name="ctransformfilterdecidebuffersize-method"></a><span data-ttu-id="8dbf3-103">CTransformFilter. DecideBufferSize 方法</span><span class="sxs-lookup"><span data-stu-id="8dbf3-103">CTransformFilter.DecideBufferSize method</span></span>

<span data-ttu-id="8dbf3-104">`DecideBufferSize`方法會設定輸出釘選的緩衝區需求。</span><span class="sxs-lookup"><span data-stu-id="8dbf3-104">The `DecideBufferSize` method sets the output pin's buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dbf3-105">語法</span><span class="sxs-lookup"><span data-stu-id="8dbf3-105">Syntax</span></span>


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="8dbf3-106">參數</span><span class="sxs-lookup"><span data-stu-id="8dbf3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dbf3-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="8dbf3-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="8dbf3-108">輸出釘選器上 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="8dbf3-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface on the output pin's allocator.</span></span>

</dd> <dt>

<span data-ttu-id="8dbf3-109">*ppropInputRequest*</span><span class="sxs-lookup"><span data-stu-id="8dbf3-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="8dbf3-110">配置器 [**\_ 屬性**](/windows/win32/api/strmif/ns-strmif-allocator_properties) 結構的指標，其中包含來自下游輸入圖釘的緩衝區需求。</span><span class="sxs-lookup"><span data-stu-id="8dbf3-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains buffer requirements from the downstream input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dbf3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="8dbf3-111">Return value</span></span>

<span data-ttu-id="8dbf3-112">傳回 S \_ OK 或其他 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="8dbf3-112">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8dbf3-113">備註</span><span class="sxs-lookup"><span data-stu-id="8dbf3-113">Remarks</span></span>

<span data-ttu-id="8dbf3-114">輸出釘選的 [**CTransformOutputPin：:D ecidebuffersize**](ctransformoutputpin-decidebuffersize.md) 方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="8dbf3-114">The output pin's [**CTransformOutputPin::DecideBufferSize**](ctransformoutputpin-decidebuffersize.md) method calls this method.</span></span> <span data-ttu-id="8dbf3-115">衍生的類別必須執行此方法。</span><span class="sxs-lookup"><span data-stu-id="8dbf3-115">The derived class must implement this method.</span></span> <span data-ttu-id="8dbf3-116">如需詳細資訊，請參閱 [**CBaseOutputPin：:D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md)。</span><span class="sxs-lookup"><span data-stu-id="8dbf3-116">For more information, see [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8dbf3-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="8dbf3-117">Requirements</span></span>



| <span data-ttu-id="8dbf3-118">需求</span><span class="sxs-lookup"><span data-stu-id="8dbf3-118">Requirement</span></span> | <span data-ttu-id="8dbf3-119">值</span><span class="sxs-lookup"><span data-stu-id="8dbf3-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dbf3-120">標頭</span><span class="sxs-lookup"><span data-stu-id="8dbf3-120">Header</span></span><br/>  | <dl> <span data-ttu-id="8dbf3-121"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8dbf3-121"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8dbf3-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="8dbf3-122">Library</span></span><br/> | <dl> <span data-ttu-id="8dbf3-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8dbf3-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8dbf3-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8dbf3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dbf3-125">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="8dbf3-125">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




