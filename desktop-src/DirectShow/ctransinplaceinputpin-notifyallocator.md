---
description: CTransInPlaceInputPin. NotifyAllocator 方法-NotifyAllocator 方法會指定連接的配置器。 這個方法會實 IMemInputPin：： NotifyAllocator 方法。
ms.assetid: adc1c5b6-99da-4140-b644-7b98f6b8bad4
title: 'CTransInPlaceInputPin. NotifyAllocator 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca15be5dc1893a393e6052832cc7522f27355eeb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094746"
---
# <a name="ctransinplaceinputpinnotifyallocator-method"></a><span data-ttu-id="b0f04-104">CTransInPlaceInputPin. NotifyAllocator 方法</span><span class="sxs-lookup"><span data-stu-id="b0f04-104">CTransInPlaceInputPin.NotifyAllocator method</span></span>

<span data-ttu-id="b0f04-105">方法會指定連接的配置器 `NotifyAllocator` 。</span><span class="sxs-lookup"><span data-stu-id="b0f04-105">The `NotifyAllocator` method specifies an allocator for the connection.</span></span> <span data-ttu-id="b0f04-106">這個方法會實 [**IMemInputPin：： NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) 方法。</span><span class="sxs-lookup"><span data-stu-id="b0f04-106">This method implements the [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0f04-107">語法</span><span class="sxs-lookup"><span data-stu-id="b0f04-107">Syntax</span></span>


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a><span data-ttu-id="b0f04-108">參數</span><span class="sxs-lookup"><span data-stu-id="b0f04-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0f04-109">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="b0f04-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f04-110">配置器的 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="b0f04-110">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="b0f04-111">*bReadOnly*</span><span class="sxs-lookup"><span data-stu-id="b0f04-111">*bReadOnly*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f04-112">旗標，指定此配置器的樣本是否為唯讀。</span><span class="sxs-lookup"><span data-stu-id="b0f04-112">Flag that specifies whether samples from this allocator are read-only.</span></span> <span data-ttu-id="b0f04-113">若 **為 TRUE**，則表示範例是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="b0f04-113">If **TRUE**, samples are read-only.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0f04-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="b0f04-114">Return value</span></span>

<span data-ttu-id="b0f04-115">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="b0f04-115">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b0f04-116">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="b0f04-116">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="b0f04-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b0f04-117">Return code</span></span>                                                                               | <span data-ttu-id="b0f04-118">Description</span><span class="sxs-lookup"><span data-stu-id="b0f04-118">Description</span></span>                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="b0f04-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="b0f04-119"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="b0f04-120">Success</span><span class="sxs-lookup"><span data-stu-id="b0f04-120">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="b0f04-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="b0f04-121"><dt>**E\_FAIL**</dt></span></span> </dl>    | <span data-ttu-id="b0f04-122">失敗</span><span class="sxs-lookup"><span data-stu-id="b0f04-122">Failure</span></span><br/>                   |
| <dl> <span data-ttu-id="b0f04-123"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="b0f04-123"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="b0f04-124">**Null** 指標引數</span><span class="sxs-lookup"><span data-stu-id="b0f04-124">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b0f04-125">備註</span><span class="sxs-lookup"><span data-stu-id="b0f04-125">Remarks</span></span>

<span data-ttu-id="b0f04-126">篩選準則會嘗試針對兩個 pin 連接使用相同的配置器。</span><span class="sxs-lookup"><span data-stu-id="b0f04-126">The filter attempts to use the same allocator for both pin connections.</span></span>

-   <span data-ttu-id="b0f04-127">如果輸出針腳未連接，則輸入 pin 會自動接受配置器。</span><span class="sxs-lookup"><span data-stu-id="b0f04-127">If the output pin is not connected, the input pin automatically accepts the allocator.</span></span> <span data-ttu-id="b0f04-128">當輸出連接時，篩選器會重新連接輸入的 pin。</span><span class="sxs-lookup"><span data-stu-id="b0f04-128">When the output pin is connected, the filter will reconnect the input pin.</span></span> <span data-ttu-id="b0f04-129">屆時，篩選器會再試一次使用單一配置器。</span><span class="sxs-lookup"><span data-stu-id="b0f04-129">At that point, the filter will try again to use a single allocator.</span></span>
-   <span data-ttu-id="b0f04-130">如果輸出連接已連線，則輸入插針會接受配置器。</span><span class="sxs-lookup"><span data-stu-id="b0f04-130">If the output pin is connected, the input pin accepts the allocator.</span></span> <span data-ttu-id="b0f04-131">輸出釘選也會使用相同的配置器。</span><span class="sxs-lookup"><span data-stu-id="b0f04-131">The output pin also uses the same allocator.</span></span> <span data-ttu-id="b0f04-132">它會呼叫 `NotifyAllocator` 下游輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="b0f04-132">It calls `NotifyAllocator` on the downstream input pin.</span></span>

<span data-ttu-id="b0f04-133">先前的案例有下列例外狀況：</span><span class="sxs-lookup"><span data-stu-id="b0f04-133">The previous case has the following exception:</span></span>

-   <span data-ttu-id="b0f04-134">如果建議的配置器是唯讀的 (也就是說， *bReadOnly* 參數為 **TRUE**) 而且篩選準則需要修改範例，則篩選準則必須使用兩個不同的配置器。</span><span class="sxs-lookup"><span data-stu-id="b0f04-134">If the proposed allocator is read-only (that is, the *bReadOnly* parameter is **TRUE**) and the filter needs to modify the samples, then the filter must use two different allocators.</span></span> <span data-ttu-id="b0f04-135">在此情況下，如果上游篩選器打算使用下游篩選器的配置器，則方法會傳回 E \_ FAIL。</span><span class="sxs-lookup"><span data-stu-id="b0f04-135">In this case, if the upstream filter is proposing to use the downstream filter's allocator, the method returns E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0f04-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0f04-136">Requirements</span></span>



| <span data-ttu-id="b0f04-137">需求</span><span class="sxs-lookup"><span data-stu-id="b0f04-137">Requirement</span></span> | <span data-ttu-id="b0f04-138">值</span><span class="sxs-lookup"><span data-stu-id="b0f04-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0f04-139">標頭</span><span class="sxs-lookup"><span data-stu-id="b0f04-139">Header</span></span><br/>  | <dl> <span data-ttu-id="b0f04-140"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b0f04-140"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b0f04-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="b0f04-141">Library</span></span><br/> | <dl> <span data-ttu-id="b0f04-142"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b0f04-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0f04-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0f04-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0f04-144">**CTransInPlaceInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="b0f04-144">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




