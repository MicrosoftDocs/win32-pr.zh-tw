---
description: DecideAllocator 方法會選取記憶體配置器。
ms.assetid: cdc15b0e-ea1b-43aa-9267-95fa9db56ed5
title: 'CBaseOutputPin. DecideAllocator 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e587562341118b904803302f0fd7249ebf8e507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990064"
---
# <a name="cbaseoutputpindecideallocator-method"></a><span data-ttu-id="a8894-103">CBaseOutputPin. DecideAllocator 方法</span><span class="sxs-lookup"><span data-stu-id="a8894-103">CBaseOutputPin.DecideAllocator method</span></span>

<span data-ttu-id="a8894-104">`DecideAllocator`方法會選取記憶體配置器。</span><span class="sxs-lookup"><span data-stu-id="a8894-104">The `DecideAllocator` method selects a memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8894-105">語法</span><span class="sxs-lookup"><span data-stu-id="a8894-105">Syntax</span></span>


```C++
virtual HRESULT DecideAllocator(
   IMemInputPin  *pPin,
   IMemAllocator **pAlloc
);
```



## <a name="parameters"></a><span data-ttu-id="a8894-106">參數</span><span class="sxs-lookup"><span data-stu-id="a8894-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8894-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="a8894-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="a8894-108">輸入釘選 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="a8894-108">Pointer to the input pin's [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="a8894-109">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="a8894-109">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="a8894-110">接收配置器之 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面指標的變數位址。</span><span class="sxs-lookup"><span data-stu-id="a8894-110">Address of a variable that receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8894-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a8894-111">Return value</span></span>

<span data-ttu-id="a8894-112">\_如果成功，則傳回，否則會傳回表示錯誤原因的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="a8894-112">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8894-113">備註</span><span class="sxs-lookup"><span data-stu-id="a8894-113">Remarks</span></span>

<span data-ttu-id="a8894-114">在 pin 連線程式結束時，會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="a8894-114">This method is called at the end of the pin connection process.</span></span> <span data-ttu-id="a8894-115">它會執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="a8894-115">It performs the following steps:</span></span>

1.  <span data-ttu-id="a8894-116">呼叫 [**IMemInputPin：： GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) 方法，以取得輸入釘選的緩衝區需求（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="a8894-116">Calls the [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) method to retrieve the input pin's buffer requirements, if any.</span></span>
2.  <span data-ttu-id="a8894-117">呼叫 [**IMemInputPin：： GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) 方法，以從輸入 pin 要求配置器。</span><span class="sxs-lookup"><span data-stu-id="a8894-117">Calls the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method to request an allocator from the input pin.</span></span> <span data-ttu-id="a8894-118">如果輸入 pin 未提供配置器，輸出釘選會藉由呼叫 [**CBaseOutputPin：： InitAllocator**](cbaseoutputpin-initallocator.md) 類別方法來建立一個配置器。</span><span class="sxs-lookup"><span data-stu-id="a8894-118">If the input pin does not provide an allocator, the output pin creates one by calling the [**CBaseOutputPin::InitAllocator**](cbaseoutputpin-initallocator.md) class method.</span></span>
3.  <span data-ttu-id="a8894-119">呼叫 [**CBaseOutputPin：:D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) 類別方法，它會設定配置器屬性。</span><span class="sxs-lookup"><span data-stu-id="a8894-119">Calls the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) class method, which sets the allocator properties.</span></span> <span data-ttu-id="a8894-120">這是純虛擬方法;衍生的類別必須加以執行。</span><span class="sxs-lookup"><span data-stu-id="a8894-120">This is a pure virtual method; the derived class must implement it.</span></span>
4.  <span data-ttu-id="a8894-121">呼叫 [**IMemInputPin：： NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) 方法，這會通知所使用配置器的輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="a8894-121">Calls the [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method, which notifies the input pin of the allocator being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8894-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8894-122">Requirements</span></span>



| <span data-ttu-id="a8894-123">需求</span><span class="sxs-lookup"><span data-stu-id="a8894-123">Requirement</span></span> | <span data-ttu-id="a8894-124">值</span><span class="sxs-lookup"><span data-stu-id="a8894-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8894-125">標頭</span><span class="sxs-lookup"><span data-stu-id="a8894-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a8894-126"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a8894-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a8894-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="a8894-127">Library</span></span><br/> | <dl> <span data-ttu-id="a8894-128"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a8894-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8894-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8894-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8894-130">**CBaseOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="a8894-130">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




