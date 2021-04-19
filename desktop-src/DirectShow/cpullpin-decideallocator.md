---
description: DecideAllocator 方法會使用輸出圖釘來協調配置器。
ms.assetid: 5c04f440-b177-4caa-989f-3aa783c4b348
title: 'CPullPin. DecideAllocator 方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91ffa139b916b1594e0729a0f8d52f07c62eda12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994816"
---
# <a name="cpullpindecideallocator-method"></a><span data-ttu-id="c9705-103">CPullPin. DecideAllocator 方法</span><span class="sxs-lookup"><span data-stu-id="c9705-103">CPullPin.DecideAllocator method</span></span>

<span data-ttu-id="c9705-104">`DecideAllocator`方法會使用輸出圖釘來協調配置器。</span><span class="sxs-lookup"><span data-stu-id="c9705-104">The `DecideAllocator` method negotiates an allocator with the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9705-105">語法</span><span class="sxs-lookup"><span data-stu-id="c9705-105">Syntax</span></span>


```C++
virtual HRESULT DecideAllocator(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="c9705-106">參數</span><span class="sxs-lookup"><span data-stu-id="c9705-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9705-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="c9705-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="c9705-108">輸入釘選配置器之 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面的指標，或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c9705-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface of the input pin's preferred allocator, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c9705-109">*pProps*</span><span class="sxs-lookup"><span data-stu-id="c9705-109">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="c9705-110">選用配置器 [**\_ 屬性**](/windows/win32/api/strmif/ns-strmif-allocator_properties) 結構的指標，其中包含輸入釘選的緩衝區需求。</span><span class="sxs-lookup"><span data-stu-id="c9705-110">Pointer to an optional [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9705-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9705-111">Return value</span></span>

<span data-ttu-id="c9705-112">\_如果成功，則傳回，否則傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c9705-112">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9705-113">備註</span><span class="sxs-lookup"><span data-stu-id="c9705-113">Remarks</span></span>

<span data-ttu-id="c9705-114">這個方法會呼叫 [**IAsyncReader：： RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) 方法來協調配置器。</span><span class="sxs-lookup"><span data-stu-id="c9705-114">This method calls the [**IAsyncReader::RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) method to negotiate an allocator.</span></span> <span data-ttu-id="c9705-115">它會將 *pAlloc* 參數直接傳遞給 **RequestAllocator** 方法。</span><span class="sxs-lookup"><span data-stu-id="c9705-115">It passes the *pAlloc* parameter directly to the **RequestAllocator** method.</span></span> <span data-ttu-id="c9705-116">如果 *pProps* 為非 **Null**，它會將 *pProps* 參數傳遞至 **RequestAllocator** ;否則，它會建立具有三個64K 緩衝區預設要求的配置器 **\_ 屬性** 結構。</span><span class="sxs-lookup"><span data-stu-id="c9705-116">It passes the *pProps* parameter to **RequestAllocator** if *pProps* is non-**NULL**; otherwise, it creates an **ALLOCATOR\_PROPERTIES** structure with a default request of three 64K buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9705-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9705-117">Requirements</span></span>



| <span data-ttu-id="c9705-118">需求</span><span class="sxs-lookup"><span data-stu-id="c9705-118">Requirement</span></span> | <span data-ttu-id="c9705-119">值</span><span class="sxs-lookup"><span data-stu-id="c9705-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9705-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c9705-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c9705-121"><dt>Pullpin。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9705-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="c9705-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="c9705-122">Library</span></span><br/> | <dl> <span data-ttu-id="c9705-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c9705-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9705-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9705-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9705-125">**CPullPin 類別**</span><span class="sxs-lookup"><span data-stu-id="c9705-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> <dt>

[<span data-ttu-id="c9705-126">**CPullPin：： Connect**</span><span class="sxs-lookup"><span data-stu-id="c9705-126">**CPullPin::Connect**</span></span>](cpullpin-connect.md)
</dt> </dl>

 

 




