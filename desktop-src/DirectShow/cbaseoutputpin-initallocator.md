---
description: InitAllocator 方法會建立記憶體配置器。
ms.assetid: a1fa0ffb-ed43-446d-811e-6c3594743592
title: " (Amfilter 的 CBaseOutputPin.InitAllocator 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.InitAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7e5385671ba4c7fdf1b719f83aafba7d84421bce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993626"
---
# <a name="cbaseoutputpininitallocator-method"></a><span data-ttu-id="59b94-103">CBaseOutputPin.InitAllocator 方法</span><span class="sxs-lookup"><span data-stu-id="59b94-103">CBaseOutputPin.InitAllocator method</span></span>

<span data-ttu-id="59b94-104">`InitAllocator`方法會建立記憶體配置器。</span><span class="sxs-lookup"><span data-stu-id="59b94-104">The `InitAllocator` method creates a memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="59b94-105">語法</span><span class="sxs-lookup"><span data-stu-id="59b94-105">Syntax</span></span>


```C++
virtual HRESULT InitAllocator(
   IMemAllocator **ppAlloc
);
```



## <a name="parameters"></a><span data-ttu-id="59b94-106">參數</span><span class="sxs-lookup"><span data-stu-id="59b94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59b94-107">*ppAlloc*</span><span class="sxs-lookup"><span data-stu-id="59b94-107">*ppAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="59b94-108">接收配置器之 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面指標的變數位址。</span><span class="sxs-lookup"><span data-stu-id="59b94-108">Address of a variable that receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59b94-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="59b94-109">Return value</span></span>

<span data-ttu-id="59b94-110">\_如果成功，則傳回 [確定]，或從 **CoCreateInstance** 函數傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="59b94-110">Returns S\_OK if successful, or an error code from the **CoCreateInstance** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="59b94-111">備註</span><span class="sxs-lookup"><span data-stu-id="59b94-111">Remarks</span></span>

<span data-ttu-id="59b94-112">如果輸入 pin 未提供記憶體配置器， [**CBaseOutputPin：:D ecideallocator**](cbaseoutputpin-decideallocator.md) 方法就會呼叫這個方法來建立配置器。</span><span class="sxs-lookup"><span data-stu-id="59b94-112">If the input pin does not provide a memory allocator, the [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md) method calls this method to create an allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="59b94-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="59b94-113">Requirements</span></span>



| <span data-ttu-id="59b94-114">需求</span><span class="sxs-lookup"><span data-stu-id="59b94-114">Requirement</span></span> | <span data-ttu-id="59b94-115">值</span><span class="sxs-lookup"><span data-stu-id="59b94-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59b94-116">標頭</span><span class="sxs-lookup"><span data-stu-id="59b94-116">Header</span></span><br/>  | <dl> <span data-ttu-id="59b94-117"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="59b94-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="59b94-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="59b94-118">Library</span></span><br/> | <dl> <span data-ttu-id="59b94-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="59b94-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59b94-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59b94-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59b94-121">**CBaseOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="59b94-121">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




