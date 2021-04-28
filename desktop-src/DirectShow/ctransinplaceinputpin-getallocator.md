---
description: CTransInPlaceInputPin. GetAllocator 方法-GetAllocator 方法會抓取此 pin 提議的記憶體配置器。 這個方法會實 IMemInputPin：： GetAllocator 方法。
ms.assetid: e9db4aa0-4f53-4ca4-babb-5e0215c7c284
title: 'CTransInPlaceInputPin. GetAllocator 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2472630d69119f33653d831386af615718274d99
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084656"
---
# <a name="ctransinplaceinputpingetallocator-method"></a><span data-ttu-id="0765c-104">CTransInPlaceInputPin. GetAllocator 方法</span><span class="sxs-lookup"><span data-stu-id="0765c-104">CTransInPlaceInputPin.GetAllocator method</span></span>

<span data-ttu-id="0765c-105">方法會抓取 `GetAllocator` 此 pin 提議的記憶體配置器。</span><span class="sxs-lookup"><span data-stu-id="0765c-105">The `GetAllocator` method retrieves the memory allocator proposed by this pin.</span></span> <span data-ttu-id="0765c-106">這個方法會實 [**IMemInputPin：： GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) 方法。</span><span class="sxs-lookup"><span data-stu-id="0765c-106">This method implements the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0765c-107">語法</span><span class="sxs-lookup"><span data-stu-id="0765c-107">Syntax</span></span>


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="0765c-108">參數</span><span class="sxs-lookup"><span data-stu-id="0765c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0765c-109">*ppAllocator*</span><span class="sxs-lookup"><span data-stu-id="0765c-109">*ppAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="0765c-110">接收配置器之 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="0765c-110">Receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0765c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0765c-111">Return value</span></span>

<span data-ttu-id="0765c-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="0765c-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0765c-113">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="0765c-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="0765c-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0765c-114">Return code</span></span>                                                                                          | <span data-ttu-id="0765c-115">Description</span><span class="sxs-lookup"><span data-stu-id="0765c-115">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="0765c-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0765c-116"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="0765c-117">成功。</span><span class="sxs-lookup"><span data-stu-id="0765c-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="0765c-118"><dt>**VFW \_ E \_ NO 配置器 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0765c-118"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="0765c-119">沒有配置器可供使用。</span><span class="sxs-lookup"><span data-stu-id="0765c-119">No allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0765c-120">備註</span><span class="sxs-lookup"><span data-stu-id="0765c-120">Remarks</span></span>

<span data-ttu-id="0765c-121">如果篩選的輸出釘選連線，此方法會向下游篩選器的輸入 pin 要求配置器。</span><span class="sxs-lookup"><span data-stu-id="0765c-121">If the filter's output pin is connected, this method requests an allocator from the downstream filter's input pin.</span></span>

<span data-ttu-id="0765c-122">如果篩選的輸出針腳未連接，這個方法會建立暫存配置器。</span><span class="sxs-lookup"><span data-stu-id="0765c-122">If the filter's output pin is not connected, this method creates a temporary allocator.</span></span> <span data-ttu-id="0765c-123">稍後，當輸出連接時，篩選器會重新連接輸入 pin，並重新協商配置器。</span><span class="sxs-lookup"><span data-stu-id="0765c-123">Later, when the output pin is connected, the filter will reconnect the input pin and renegotiate the allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="0765c-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="0765c-124">Requirements</span></span>



| <span data-ttu-id="0765c-125">需求</span><span class="sxs-lookup"><span data-stu-id="0765c-125">Requirement</span></span> | <span data-ttu-id="0765c-126">值</span><span class="sxs-lookup"><span data-stu-id="0765c-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0765c-127">標頭</span><span class="sxs-lookup"><span data-stu-id="0765c-127">Header</span></span><br/>  | <dl> <span data-ttu-id="0765c-128"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0765c-128"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0765c-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="0765c-129">Library</span></span><br/> | <dl> <span data-ttu-id="0765c-130"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0765c-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0765c-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0765c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0765c-132">**CTransInPlaceInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="0765c-132">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




