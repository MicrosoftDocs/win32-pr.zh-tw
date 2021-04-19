---
description: 配置方法會為緩衝區配置記憶體。 這個方法會覆寫 CBaseAllocator：：分配方法。
ms.assetid: 4a246b4e-93b3-4adb-9f10-6b92d9f479eb
title: 'CImageAllocator 方法 (Winutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7acd13e2d2d09e6e491a2f338aef2fe7564b82b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987200"
---
# <a name="cimageallocatoralloc-method"></a><span data-ttu-id="909a5-104">CImageAllocator 方法</span><span class="sxs-lookup"><span data-stu-id="909a5-104">CImageAllocator.Alloc method</span></span>

<span data-ttu-id="909a5-105">`Alloc`方法會為緩衝區配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="909a5-105">The `Alloc` method allocates memory for the buffers.</span></span> <span data-ttu-id="909a5-106">這個方法會覆寫 [**CBaseAllocator：：分配**](cbaseallocator-alloc.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="909a5-106">This method overrides the [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="909a5-107">語法</span><span class="sxs-lookup"><span data-stu-id="909a5-107">Syntax</span></span>


```C++
HRESULT Alloc();
```



## <a name="parameters"></a><span data-ttu-id="909a5-108">參數</span><span class="sxs-lookup"><span data-stu-id="909a5-108">Parameters</span></span>

<span data-ttu-id="909a5-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="909a5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="909a5-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="909a5-110">Return value</span></span>

<span data-ttu-id="909a5-111">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="909a5-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="909a5-112">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="909a5-112">Possible values include the following.</span></span>



| <span data-ttu-id="909a5-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="909a5-113">Return code</span></span>                                                                                   | <span data-ttu-id="909a5-114">Description</span><span class="sxs-lookup"><span data-stu-id="909a5-114">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="909a5-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="909a5-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="909a5-116">Success</span><span class="sxs-lookup"><span data-stu-id="909a5-116">Success</span></span><br/>             |
| <dl> <span data-ttu-id="909a5-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="909a5-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="909a5-118">記憶體不足</span><span class="sxs-lookup"><span data-stu-id="909a5-118">Insufficient memory</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="909a5-119">備註</span><span class="sxs-lookup"><span data-stu-id="909a5-119">Remarks</span></span>

<span data-ttu-id="909a5-120">當篩選準則認可配置器時， [**CBaseAllocator：： Commit**](cbaseallocator-commit.md) 方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="909a5-120">This method is called by the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method, when the filter commits the allocator.</span></span>

<span data-ttu-id="909a5-121">這個方法會建立媒體範例的清單，這些範例會實作為 [**CImageSample**](cimagesample.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="909a5-121">This method creates a list of media samples, which are implemented as [**CImageSample**](cimagesample.md) objects.</span></span> <span data-ttu-id="909a5-122">每個範例都包含 GDI 與裝置無關的點陣圖（使用 GDI **CreateDIBSection** 函式）。</span><span class="sxs-lookup"><span data-stu-id="909a5-122">Each sample contains a GDI device-independent bitmap, using the GDI **CreateDIBSection** function.</span></span>

<span data-ttu-id="909a5-123">在內部，這個方法會呼叫 [**CImageAllocator：： CreateDIB**](cimageallocator-createdib.md) 來建立每個 DIB，並呼叫 [**CImageAllocator：： CreateImageSample**](cimageallocator-createimagesample.md) 來建立每個範例。</span><span class="sxs-lookup"><span data-stu-id="909a5-123">Internally this method calls [**CImageAllocator::CreateDIB**](cimageallocator-createdib.md) to create each DIB, and [**CImageAllocator::CreateImageSample**](cimageallocator-createimagesample.md) to create each sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="909a5-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="909a5-124">Requirements</span></span>



| <span data-ttu-id="909a5-125">需求</span><span class="sxs-lookup"><span data-stu-id="909a5-125">Requirement</span></span> | <span data-ttu-id="909a5-126">值</span><span class="sxs-lookup"><span data-stu-id="909a5-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="909a5-127">標頭</span><span class="sxs-lookup"><span data-stu-id="909a5-127">Header</span></span><br/>  | <dl> <span data-ttu-id="909a5-128"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="909a5-128"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="909a5-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="909a5-129">Library</span></span><br/> | <dl> <span data-ttu-id="909a5-130"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="909a5-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="909a5-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="909a5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="909a5-132">**CImageAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="909a5-132">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




