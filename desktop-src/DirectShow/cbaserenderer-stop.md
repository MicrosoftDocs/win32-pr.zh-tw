---
description: Stop 方法會停止篩選。
ms.assetid: 80eac207-5db3-4b06-bbae-eca72e37d09d
title: 'CBaseRenderer. Stop 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ddd8194bbf76c4a4311aa90335f94d1e7548a356
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979582"
---
# <a name="cbaserendererstop-method"></a><span data-ttu-id="ecc59-103">CBaseRenderer. Stop 方法</span><span class="sxs-lookup"><span data-stu-id="ecc59-103">CBaseRenderer.Stop method</span></span>

<span data-ttu-id="ecc59-104">`Stop`方法會停止篩選。</span><span class="sxs-lookup"><span data-stu-id="ecc59-104">The `Stop` method stops the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecc59-105">語法</span><span class="sxs-lookup"><span data-stu-id="ecc59-105">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="ecc59-106">參數</span><span class="sxs-lookup"><span data-stu-id="ecc59-106">Parameters</span></span>

<span data-ttu-id="ecc59-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="ecc59-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ecc59-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="ecc59-108">Return value</span></span>

<span data-ttu-id="ecc59-109">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="ecc59-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecc59-110">備註</span><span class="sxs-lookup"><span data-stu-id="ecc59-110">Remarks</span></span>

<span data-ttu-id="ecc59-111">這個方法會覆寫 [**CBaseFilter：： Stop**](cbasefilter-stop.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="ecc59-111">This method overrides the [**CBaseFilter::Stop**](cbasefilter-stop.md) method.</span></span> <span data-ttu-id="ecc59-112">其會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="ecc59-112">It performs the following actions:</span></span>

-   <span data-ttu-id="ecc59-113">呼叫 [**CBaseFilter：： Stop**](cbasefilter-stop.md)。</span><span class="sxs-lookup"><span data-stu-id="ecc59-113">Calls [**CBaseFilter::Stop**](cbasefilter-stop.md).</span></span>
-   <span data-ttu-id="ecc59-114">解除配置器。</span><span class="sxs-lookup"><span data-stu-id="ecc59-114">Decommits the allocator.</span></span> <span data-ttu-id="ecc59-115"> (參閱 [**IMemAllocator：:D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit)。 ) </span><span class="sxs-lookup"><span data-stu-id="ecc59-115">(See [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit).)</span></span>
-   <span data-ttu-id="ecc59-116">取消任何排程的轉譯，並釋放串流執行緒。</span><span class="sxs-lookup"><span data-stu-id="ecc59-116">Cancels any scheduled rendering and releases the streaming thread.</span></span>
-   <span data-ttu-id="ecc59-117">等候任何擱置的 **接收** 呼叫完成。</span><span class="sxs-lookup"><span data-stu-id="ecc59-117">Waits for any pending **Receive** call to complete.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecc59-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="ecc59-118">Requirements</span></span>



| <span data-ttu-id="ecc59-119">需求</span><span class="sxs-lookup"><span data-stu-id="ecc59-119">Requirement</span></span> | <span data-ttu-id="ecc59-120">值</span><span class="sxs-lookup"><span data-stu-id="ecc59-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecc59-121">標頭</span><span class="sxs-lookup"><span data-stu-id="ecc59-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ecc59-122"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ecc59-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ecc59-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="ecc59-123">Library</span></span><br/> | <dl> <span data-ttu-id="ecc59-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ecc59-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecc59-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ecc59-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecc59-126">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="ecc59-126">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




