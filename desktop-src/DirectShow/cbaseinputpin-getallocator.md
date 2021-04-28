---
description: CBaseInputPin. GetAllocator 方法-GetAllocator 方法會抓取此 pin 提議的記憶體配置器。 這個方法會實 IMemInputPin：： GetAllocator 方法。
ms.assetid: 07bc77f8-a877-4403-b424-20bda715a818
title: 'CBaseInputPin. GetAllocator 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72aaf6bb4c1ff8bf108086a8a42a618267c4bc06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099707"
---
# <a name="cbaseinputpingetallocator-method"></a><span data-ttu-id="3fcb4-104">CBaseInputPin. GetAllocator 方法</span><span class="sxs-lookup"><span data-stu-id="3fcb4-104">CBaseInputPin.GetAllocator method</span></span>

<span data-ttu-id="3fcb4-105">方法會抓取 `GetAllocator` 此 pin 提議的記憶體配置器。</span><span class="sxs-lookup"><span data-stu-id="3fcb4-105">The `GetAllocator` method retrieves the memory allocator proposed by this pin.</span></span> <span data-ttu-id="3fcb4-106">這個方法會實 [**IMemInputPin：： GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) 方法。</span><span class="sxs-lookup"><span data-stu-id="3fcb4-106">This method implements the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fcb4-107">語法</span><span class="sxs-lookup"><span data-stu-id="3fcb4-107">Syntax</span></span>


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="3fcb4-108">參數</span><span class="sxs-lookup"><span data-stu-id="3fcb4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fcb4-109">*ppAllocator*</span><span class="sxs-lookup"><span data-stu-id="3fcb4-109">*ppAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="3fcb4-110">接收配置器之 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面指標的變數位址。</span><span class="sxs-lookup"><span data-stu-id="3fcb4-110">Address of a variable that receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fcb4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3fcb4-111">Return value</span></span>

<span data-ttu-id="3fcb4-112">\_如果成功，則傳回 [確定]，或從 **CoCreateInstance** 函數傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3fcb4-112">Returns S\_OK if successful, or an error code from the **CoCreateInstance** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fcb4-113">備註</span><span class="sxs-lookup"><span data-stu-id="3fcb4-113">Remarks</span></span>

<span data-ttu-id="3fcb4-114">這個方法會建立 [**CMemAllocator**](cmemallocator.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="3fcb4-114">This method creates a [**CMemAllocator**](cmemallocator.md) object.</span></span> <span data-ttu-id="3fcb4-115">如果您的篩選器使用來自下游 pin 或自訂配置器的配置器，請覆寫這個方法。</span><span class="sxs-lookup"><span data-stu-id="3fcb4-115">Override this method if your filter uses an allocator from a downstream pin, or a custom allocator.</span></span>

<span data-ttu-id="3fcb4-116">如果方法成功，則 **IMemAllocator** 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="3fcb4-116">If the method succeeds, the **IMemAllocator** interface has an outstanding reference count.</span></span> <span data-ttu-id="3fcb4-117">當您完成時，請務必放開。</span><span class="sxs-lookup"><span data-stu-id="3fcb4-117">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fcb4-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3fcb4-118">Requirements</span></span>



| <span data-ttu-id="3fcb4-119">需求</span><span class="sxs-lookup"><span data-stu-id="3fcb4-119">Requirement</span></span> | <span data-ttu-id="3fcb4-120">值</span><span class="sxs-lookup"><span data-stu-id="3fcb4-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fcb4-121">標頭</span><span class="sxs-lookup"><span data-stu-id="3fcb4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3fcb4-122"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3fcb4-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3fcb4-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="3fcb4-123">Library</span></span><br/> | <dl> <span data-ttu-id="3fcb4-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3fcb4-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fcb4-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3fcb4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fcb4-126">**CBaseInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="3fcb4-126">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




