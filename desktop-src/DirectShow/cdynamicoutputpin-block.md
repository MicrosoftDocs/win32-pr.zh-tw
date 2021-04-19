---
description: Block 方法會封鎖或解除封鎖來自釘選的資料流程。 這個方法會實 IPinFlowControl：： Block 方法。
ms.assetid: 8281cd8c-7543-42b5-9a4a-11bdfcb659e3
title: 'CDynamicOutputPin： Block 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Block
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b10e9dfd43f3ad98adf8f6abb0eb7c2223d5970
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978514"
---
# <a name="cdynamicoutputpinblock-method"></a><span data-ttu-id="947f0-104">CDynamicOutputPin Block 方法</span><span class="sxs-lookup"><span data-stu-id="947f0-104">CDynamicOutputPin.Block method</span></span>

<span data-ttu-id="947f0-105">`Block`方法會封鎖或解除封鎖來自釘選的資料流程。</span><span class="sxs-lookup"><span data-stu-id="947f0-105">The `Block` method blocks or unblocks the flow of data from the pin.</span></span> <span data-ttu-id="947f0-106">這個方法會實 [**IPinFlowControl：： Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) 方法。</span><span class="sxs-lookup"><span data-stu-id="947f0-106">This method implements the [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="947f0-107">語法</span><span class="sxs-lookup"><span data-stu-id="947f0-107">Syntax</span></span>


```C++
HRESULT Block(
   DWORD  dwBlockFlags,
   HANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="947f0-108">參數</span><span class="sxs-lookup"><span data-stu-id="947f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="947f0-109">*dwBlockFlags*</span><span class="sxs-lookup"><span data-stu-id="947f0-109">*dwBlockFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="947f0-110">指出是否要封鎖或解除封鎖 pin 的旗標。</span><span class="sxs-lookup"><span data-stu-id="947f0-110">Flag that indicates whether to block or unblock the pin.</span></span> <span data-ttu-id="947f0-111">必須為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="947f0-111">Must be one of the following values:</span></span>

<span data-ttu-id="947f0-112">零：解除封鎖來自 pin 的資料流程。</span><span class="sxs-lookup"><span data-stu-id="947f0-112">Zero: Unblock data flow from the pin.</span></span>

<span data-ttu-id="947f0-113">AM \_ 釘選 \_ 流程 \_ 控制 \_ 區塊：封鎖來自 PIN 的資料流程。</span><span class="sxs-lookup"><span data-stu-id="947f0-113">AM\_PIN\_FLOW\_CONTROL\_BLOCK: Block data flow from the pin.</span></span>

</dd> <dt>

<span data-ttu-id="947f0-114">*hEvent*</span><span class="sxs-lookup"><span data-stu-id="947f0-114">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="947f0-115">事件物件的控制碼，或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="947f0-115">Handle to an event object, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="947f0-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="947f0-116">Return value</span></span>

<span data-ttu-id="947f0-117">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="947f0-117">Returns an **HRESULT** value.</span></span> <span data-ttu-id="947f0-118">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="947f0-118">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="947f0-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="947f0-119">Return code</span></span>                                                                                                                    | <span data-ttu-id="947f0-120">Description</span><span class="sxs-lookup"><span data-stu-id="947f0-120">Description</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="947f0-121"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="947f0-121"><dt>**S\_FALSE**</dt></span></span> </dl>                                        | <span data-ttu-id="947f0-122">Pin 已解除封鎖。</span><span class="sxs-lookup"><span data-stu-id="947f0-122">Pin is already unblocked.</span></span><br/>                     |
| <dl> <span data-ttu-id="947f0-123"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="947f0-123"><dt>**S\_OK**</dt></span></span> </dl>                                           | <span data-ttu-id="947f0-124">成功。</span><span class="sxs-lookup"><span data-stu-id="947f0-124">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="947f0-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="947f0-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                   | <span data-ttu-id="947f0-126">無效引數。</span><span class="sxs-lookup"><span data-stu-id="947f0-126">Invalid argument.</span></span><br/>                             |
| <dl> <span data-ttu-id="947f0-127"><dt>**VFW \_ E \_ PIN \_ 已 \_ 封鎖**</dt></span><span class="sxs-lookup"><span data-stu-id="947f0-127"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED**</dt></span></span> </dl>                   | <span data-ttu-id="947f0-128">Pin 已在另一個執行緒上遭到封鎖。</span><span class="sxs-lookup"><span data-stu-id="947f0-128">Pin is already blocked on another thread.</span></span><br/>     |
| <dl> <span data-ttu-id="947f0-129"><dt>**\_ \_ \_ \_ \_ \_ 此執行緒上已封鎖 \_ VFW E PIN**</dt></span><span class="sxs-lookup"><span data-stu-id="947f0-129"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED\_ON\_THIS\_THREAD**</dt></span></span> </dl> | <span data-ttu-id="947f0-130">呼叫執行緒上已封鎖 Pin。</span><span class="sxs-lookup"><span data-stu-id="947f0-130">Pin is already blocked on the calling thread.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="947f0-131">備註</span><span class="sxs-lookup"><span data-stu-id="947f0-131">Remarks</span></span>

<span data-ttu-id="947f0-132">如需此方法的詳細資訊，請參閱 [**IPinFlowControl：： Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block)。</span><span class="sxs-lookup"><span data-stu-id="947f0-132">For more information about this method, see [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block).</span></span> <span data-ttu-id="947f0-133">就內部而言，這個方法會呼叫下列其中一種受保護的方法：</span><span class="sxs-lookup"><span data-stu-id="947f0-133">Internally, this method calls one of the following protected methods:</span></span>

-   <span data-ttu-id="947f0-134">區塊 (非同步) ： [ **CDynamicOutputPin：： AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)</span><span class="sxs-lookup"><span data-stu-id="947f0-134">Block (asynchronous): [**CDynamicOutputPin::AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)</span></span>
-   <span data-ttu-id="947f0-135">封鎖 (同步) ： [ **CDynamicOutputPin：： SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)</span><span class="sxs-lookup"><span data-stu-id="947f0-135">Block (synchronous): [**CDynamicOutputPin::SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)</span></span>
-   <span data-ttu-id="947f0-136">解除封鎖： [ **CDynamicOutputPin：： UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)</span><span class="sxs-lookup"><span data-stu-id="947f0-136">Unblock: [**CDynamicOutputPin::UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)</span></span>

<span data-ttu-id="947f0-137">解除封鎖一律會以同步方式執行。</span><span class="sxs-lookup"><span data-stu-id="947f0-137">Unblocking is always performed synchronously.</span></span>

## <a name="requirements"></a><span data-ttu-id="947f0-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="947f0-138">Requirements</span></span>



| <span data-ttu-id="947f0-139">需求</span><span class="sxs-lookup"><span data-stu-id="947f0-139">Requirement</span></span> | <span data-ttu-id="947f0-140">值</span><span class="sxs-lookup"><span data-stu-id="947f0-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="947f0-141">標頭</span><span class="sxs-lookup"><span data-stu-id="947f0-141">Header</span></span><br/>  | <dl> <span data-ttu-id="947f0-142"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="947f0-142"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="947f0-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="947f0-143">Library</span></span><br/> | <dl> <span data-ttu-id="947f0-144"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="947f0-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="947f0-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="947f0-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="947f0-146">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="947f0-146">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




