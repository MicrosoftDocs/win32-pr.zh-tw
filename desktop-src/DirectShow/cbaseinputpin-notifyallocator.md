---
description: NotifyAllocator 方法會指定連接的配置器。 這個方法會實 IMemInputPin：： NotifyAllocator 方法。
ms.assetid: 16167bd5-2d33-4329-87ec-6a6c578e0060
title: 'CBaseInputPin. NotifyAllocator 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce5bc3cfe165b1adb6b5b970ca43d31c8ace98f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993450"
---
# <a name="cbaseinputpinnotifyallocator-method"></a><span data-ttu-id="74e4e-104">CBaseInputPin. NotifyAllocator 方法</span><span class="sxs-lookup"><span data-stu-id="74e4e-104">CBaseInputPin.NotifyAllocator method</span></span>

<span data-ttu-id="74e4e-105">方法會指定連接的配置器 `NotifyAllocator` 。</span><span class="sxs-lookup"><span data-stu-id="74e4e-105">The `NotifyAllocator` method specifies an allocator for the connection.</span></span> <span data-ttu-id="74e4e-106">這個方法會實 [**IMemInputPin：： NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) 方法。</span><span class="sxs-lookup"><span data-stu-id="74e4e-106">This method implements the [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="74e4e-107">語法</span><span class="sxs-lookup"><span data-stu-id="74e4e-107">Syntax</span></span>


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a><span data-ttu-id="74e4e-108">參數</span><span class="sxs-lookup"><span data-stu-id="74e4e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74e4e-109">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="74e4e-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="74e4e-110">配置器的 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="74e4e-110">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="74e4e-111">*bReadOnly*</span><span class="sxs-lookup"><span data-stu-id="74e4e-111">*bReadOnly*</span></span> 
</dt> <dd>

<span data-ttu-id="74e4e-112">旗標，指定此配置器的樣本是否為唯讀。</span><span class="sxs-lookup"><span data-stu-id="74e4e-112">Flag that specifies whether samples from this allocator are read-only.</span></span> <span data-ttu-id="74e4e-113">若 **為 TRUE**，則表示範例是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="74e4e-113">If **TRUE**, samples are read-only.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74e4e-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="74e4e-114">Return value</span></span>

<span data-ttu-id="74e4e-115">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="74e4e-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="74e4e-116">備註</span><span class="sxs-lookup"><span data-stu-id="74e4e-116">Remarks</span></span>

<span data-ttu-id="74e4e-117">在 pin 連接期間，輸出釘選會選擇配置器，並呼叫這個方法來通知輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="74e4e-117">During the pin connection, the output pin chooses an allocator and calls this method to notify the input pin.</span></span> <span data-ttu-id="74e4e-118">輸出 pin 可以使用 [**IMemInputPin：： GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) 方法中所建議之輸入 pin 的配置器，也可以提供自己的配置器。</span><span class="sxs-lookup"><span data-stu-id="74e4e-118">The output pin can use the allocator that the input pin proposed in the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method, or it can provide its own allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="74e4e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="74e4e-119">Requirements</span></span>



| <span data-ttu-id="74e4e-120">需求</span><span class="sxs-lookup"><span data-stu-id="74e4e-120">Requirement</span></span> | <span data-ttu-id="74e4e-121">值</span><span class="sxs-lookup"><span data-stu-id="74e4e-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74e4e-122">標頭</span><span class="sxs-lookup"><span data-stu-id="74e4e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="74e4e-123"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="74e4e-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="74e4e-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="74e4e-124">Library</span></span><br/> | <dl> <span data-ttu-id="74e4e-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="74e4e-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74e4e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74e4e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74e4e-127">**CBaseInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="74e4e-127">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




