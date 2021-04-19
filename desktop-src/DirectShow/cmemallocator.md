---
description: 執行支援 IMemAllocator 介面的配置器。
ms.assetid: c40eccef-d915-4bf3-81b2-b20e000718fb
title: 'CMemAllocator 類別 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5adf390b7abf8fcbdb017ecde04bde76bf4bc001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992944"
---
# <a name="cmemallocator-class"></a><span data-ttu-id="757c5-103">CMemAllocator 類別</span><span class="sxs-lookup"><span data-stu-id="757c5-103">CMemAllocator class</span></span>

![cmemallocator 類別階層](images/filter10.png)

<span data-ttu-id="757c5-105">執行支援 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面的配置器。</span><span class="sxs-lookup"><span data-stu-id="757c5-105">Implements an allocator that supports the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="757c5-106">這個類別衍生自 [**CBaseAllocator**](cbaseallocator.md)。</span><span class="sxs-lookup"><span data-stu-id="757c5-106">This class derives from [**CBaseAllocator**](cbaseallocator.md).</span></span> <span data-ttu-id="757c5-107">如需配置器的詳細資訊，請參閱 [**CBaseAllocator**](cbaseallocator.md)的檔。</span><span class="sxs-lookup"><span data-stu-id="757c5-107">For more information about allocators, refer to the documentation for [**CBaseAllocator**](cbaseallocator.md).</span></span>



| <span data-ttu-id="757c5-108">受保護的成員變數</span><span class="sxs-lookup"><span data-stu-id="757c5-108">Protected Member Variables</span></span>                              | <span data-ttu-id="757c5-109">Description</span><span class="sxs-lookup"><span data-stu-id="757c5-109">Description</span></span>                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="757c5-110">**m \_ pBuffer**</span><span class="sxs-lookup"><span data-stu-id="757c5-110">**m\_pBuffer**</span></span>](cmemallocator-m-pbuffer.md)           | <span data-ttu-id="757c5-111">包含緩衝區之記憶體區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="757c5-111">Pointer to the memory block that contains the buffers.</span></span>                   |
| <span data-ttu-id="757c5-112">保護方法</span><span class="sxs-lookup"><span data-stu-id="757c5-112">Protected Methods</span></span>                                       | <span data-ttu-id="757c5-113">Description</span><span class="sxs-lookup"><span data-stu-id="757c5-113">Description</span></span>                                                              |
| [<span data-ttu-id="757c5-114">**自由**</span><span class="sxs-lookup"><span data-stu-id="757c5-114">**Free**</span></span>](cmemallocator-free.md)                      | <span data-ttu-id="757c5-115">預留位置方法;在取消認可操作期間呼叫。</span><span class="sxs-lookup"><span data-stu-id="757c5-115">Placeholder method; called during a decommit operation.</span></span>                  |
| [<span data-ttu-id="757c5-116">**ReallyFree**</span><span class="sxs-lookup"><span data-stu-id="757c5-116">**ReallyFree**</span></span>](cmemallocator-reallyfree.md)          | <span data-ttu-id="757c5-117">釋放緩衝區的記憶體。</span><span class="sxs-lookup"><span data-stu-id="757c5-117">Releases the memory for the buffers.</span></span>                                     |
| [<span data-ttu-id="757c5-118">**配置**</span><span class="sxs-lookup"><span data-stu-id="757c5-118">**Alloc**</span></span>](cmemallocator-alloc.md)                    | <span data-ttu-id="757c5-119">配置緩衝區的記憶體。</span><span class="sxs-lookup"><span data-stu-id="757c5-119">Allocates memory for the buffers.</span></span>                                        |
| <span data-ttu-id="757c5-120">公用方法</span><span class="sxs-lookup"><span data-stu-id="757c5-120">Public Methods</span></span>                                          | <span data-ttu-id="757c5-121">Description</span><span class="sxs-lookup"><span data-stu-id="757c5-121">Description</span></span>                                                              |
| [<span data-ttu-id="757c5-122">**CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="757c5-122">**CMemAllocator**</span></span>](cmemallocator-cmemallocator.md)    | <span data-ttu-id="757c5-123">函式方法。</span><span class="sxs-lookup"><span data-stu-id="757c5-123">Constructor method.</span></span>                                                      |
| [<span data-ttu-id="757c5-124">**~ CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="757c5-124">**~ CMemAllocator**</span></span>](cmemallocator--cmemallocator.md) | <span data-ttu-id="757c5-125">函式方法。</span><span class="sxs-lookup"><span data-stu-id="757c5-125">Destructor method.</span></span>                                                       |
| [<span data-ttu-id="757c5-126">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="757c5-126">**CreateInstance**</span></span>](cmemallocator-createinstance.md)  | <span data-ttu-id="757c5-127">建立 **CMemAllocator** 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="757c5-127">Creates a new instance of the **CMemAllocator** class.</span></span>                   |
| <span data-ttu-id="757c5-128">IMemAllocator 方法</span><span class="sxs-lookup"><span data-stu-id="757c5-128">IMemAllocator Methods</span></span>                                   | <span data-ttu-id="757c5-129">Description</span><span class="sxs-lookup"><span data-stu-id="757c5-129">Description</span></span>                                                              |
| [<span data-ttu-id="757c5-130">**SetProperties**</span><span class="sxs-lookup"><span data-stu-id="757c5-130">**SetProperties**</span></span>](cmemallocator-setproperties.md)    | <span data-ttu-id="757c5-131">指定要配置的緩衝區數目和每個緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="757c5-131">Specifies the number of buffers to allocate and the size of each buffer.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="757c5-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="757c5-132">Requirements</span></span>



| <span data-ttu-id="757c5-133">需求</span><span class="sxs-lookup"><span data-stu-id="757c5-133">Requirement</span></span> | <span data-ttu-id="757c5-134">值</span><span class="sxs-lookup"><span data-stu-id="757c5-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="757c5-135">標頭</span><span class="sxs-lookup"><span data-stu-id="757c5-135">Header</span></span><br/>  | <dl> <span data-ttu-id="757c5-136"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="757c5-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="757c5-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="757c5-137">Library</span></span><br/> | <dl> <span data-ttu-id="757c5-138"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="757c5-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="757c5-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="757c5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="757c5-140">提供自訂配置器</span><span class="sxs-lookup"><span data-stu-id="757c5-140">Providing a Custom Allocator</span></span>](providing-a-custom-allocator.md)
</dt> </dl>

 

 




