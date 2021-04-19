---
description: DecideBufferSize 方法會設定緩衝區需求。
ms.assetid: 1f7a3424-18ba-4a10-b09f-947ee8585ffa
title: 'CBaseOutputPin. DecideBufferSize 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dcb3328b56a7e203575a3abbaab64cda6a9b87f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984828"
---
# <a name="cbaseoutputpindecidebuffersize-method"></a><span data-ttu-id="71ae4-103">CBaseOutputPin. DecideBufferSize 方法</span><span class="sxs-lookup"><span data-stu-id="71ae4-103">CBaseOutputPin.DecideBufferSize method</span></span>

<span data-ttu-id="71ae4-104">`DecideBufferSize`方法會設定緩衝區需求。</span><span class="sxs-lookup"><span data-stu-id="71ae4-104">The `DecideBufferSize` method sets the buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="71ae4-105">語法</span><span class="sxs-lookup"><span data-stu-id="71ae4-105">Syntax</span></span>


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="71ae4-106">參數</span><span class="sxs-lookup"><span data-stu-id="71ae4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71ae4-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="71ae4-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="71ae4-108">配置器的 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="71ae4-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="71ae4-109">*ppropInputRequest*</span><span class="sxs-lookup"><span data-stu-id="71ae4-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="71ae4-110">配置器 [**\_ 屬性**](/windows/win32/api/strmif/ns-strmif-allocator_properties) 結構的指標，其中包含輸入釘選的緩衝區需求。</span><span class="sxs-lookup"><span data-stu-id="71ae4-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span> <span data-ttu-id="71ae4-111">如果輸入的 pin 沒有任何需求，呼叫端應該在呼叫方法之前，先零出此結構的成員。</span><span class="sxs-lookup"><span data-stu-id="71ae4-111">If the input pin does not have any requirements, the caller should zero out the members of this structure before calling the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71ae4-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="71ae4-112">Return value</span></span>

<span data-ttu-id="71ae4-113">\_如果成功，則傳回，否則會傳回表示錯誤原因的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="71ae4-113">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="71ae4-114">備註</span><span class="sxs-lookup"><span data-stu-id="71ae4-114">Remarks</span></span>

<span data-ttu-id="71ae4-115">在您的衍生類別中覆寫這個方法。</span><span class="sxs-lookup"><span data-stu-id="71ae4-115">Override this method in your derived class.</span></span> <span data-ttu-id="71ae4-116">呼叫 [**IMemAllocator：： SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) 方法，以指定您的緩衝區需求。</span><span class="sxs-lookup"><span data-stu-id="71ae4-116">Call the [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) method to specify your buffer requirements.</span></span> <span data-ttu-id="71ae4-117">一般而言，衍生類別會接受輸入 pin 的緩衝區需求，但不需要。</span><span class="sxs-lookup"><span data-stu-id="71ae4-117">Typically, the derived class will honor the input pin's buffer requirements, but it is not required to.</span></span>

## <a name="requirements"></a><span data-ttu-id="71ae4-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="71ae4-118">Requirements</span></span>



| <span data-ttu-id="71ae4-119">需求</span><span class="sxs-lookup"><span data-stu-id="71ae4-119">Requirement</span></span> | <span data-ttu-id="71ae4-120">值</span><span class="sxs-lookup"><span data-stu-id="71ae4-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71ae4-121">標頭</span><span class="sxs-lookup"><span data-stu-id="71ae4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="71ae4-122"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="71ae4-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="71ae4-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="71ae4-123">Library</span></span><br/> | <dl> <span data-ttu-id="71ae4-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="71ae4-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71ae4-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71ae4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71ae4-126">**CBaseOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="71ae4-126">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




