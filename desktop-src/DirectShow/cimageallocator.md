---
description: CImageAllocator 類別會執行管理與 GDI 裝置無關點陣圖 (Dib) 的配置器。 這個類別衍生自 CBaseAllocator 類別。 它會建立使用 CImageSample 類別所執行的媒體範例。
ms.assetid: edda34a5-3916-4a41-9e2f-a19f12df0947
title: 'CImageAllocator 類別 (Winutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea37dfe8cbbc7baf90e6065f0c54af1a60c3284b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989710"
---
# <a name="cimageallocator-class"></a><span data-ttu-id="44dc6-105">CImageAllocator 類別</span><span class="sxs-lookup"><span data-stu-id="44dc6-105">CImageAllocator class</span></span>

![cimageallocator 類別階層](images/wutil04.png)

<span data-ttu-id="44dc6-107">`CImageAllocator`類別會執行管理與 GDI 裝置無關點陣圖 (dib) 的配置器。</span><span class="sxs-lookup"><span data-stu-id="44dc6-107">The `CImageAllocator` class implements an allocator that manages GDI device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="44dc6-108">這個類別衍生自 [**CBaseAllocator**](cbaseallocator.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="44dc6-108">This class derives from the [**CBaseAllocator**](cbaseallocator.md) class.</span></span> <span data-ttu-id="44dc6-109">它會建立使用 [**CImageSample**](cimagesample.md) 類別所執行的媒體範例。</span><span class="sxs-lookup"><span data-stu-id="44dc6-109">It creates media samples that are implemented using the [**CImageSample**](cimagesample.md) class.</span></span>

<span data-ttu-id="44dc6-110">配置器是由兩個連接的 pin 所共用，但一律由連接中的其中一個篩選準則所擁有。</span><span class="sxs-lookup"><span data-stu-id="44dc6-110">An allocator is shared by two connected pins, but is always owned by one of the filters in the connection.</span></span> <span data-ttu-id="44dc6-111">使用的篩選準則必須追蹤配置器 `CImageAllocator` 是否由本身或其他篩選器提供。</span><span class="sxs-lookup"><span data-stu-id="44dc6-111">A filter that uses `CImageAllocator` must keep track of whether the allocator was provided by itself or by the other filter.</span></span> <span data-ttu-id="44dc6-112">如果配置器是由本身提供的，則擁有篩選器可以依賴配置器的所有媒體範例都是 **CImageSample** 物件的事實。</span><span class="sxs-lookup"><span data-stu-id="44dc6-112">If the allocator was provided by itself, the owning filter can rely on the fact that all media samples from the allocator are **CImageSample** objects.</span></span> <span data-ttu-id="44dc6-113">因此，它可以使用 **CImageSample** 物件來取得 DIB （儲存在 [**DIBDATA**](dibdata.md) 結構中）的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="44dc6-113">It can therefore use the **CImageSample** object to obtain information about the DIB, which is stored in a [**DIBDATA**](dibdata.md) structure.</span></span>

<span data-ttu-id="44dc6-114">當媒體類型變更時，擁有篩選應呼叫 **NotifyMediaType** 。</span><span class="sxs-lookup"><span data-stu-id="44dc6-114">The owning filter should call **NotifyMediaType** whenever the media type changes.</span></span>



| <span data-ttu-id="44dc6-115">受保護的成員變數</span><span class="sxs-lookup"><span data-stu-id="44dc6-115">Protected Member Variables</span></span>                                     | <span data-ttu-id="44dc6-116">Description</span><span class="sxs-lookup"><span data-stu-id="44dc6-116">Description</span></span>                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="44dc6-117">**m \_ pFilter**</span><span class="sxs-lookup"><span data-stu-id="44dc6-117">**m\_pFilter**</span></span>](cimageallocator-m-pfilter.md)                | <span data-ttu-id="44dc6-118">擁有篩選準則的指標。</span><span class="sxs-lookup"><span data-stu-id="44dc6-118">Pointer to the owning filter.</span></span>                                            |
| [<span data-ttu-id="44dc6-119">**m \_ pMediaType**</span><span class="sxs-lookup"><span data-stu-id="44dc6-119">**m\_pMediaType**</span></span>](cimageallocator-m-pmediatype.md)          | <span data-ttu-id="44dc6-120">目前媒體類型的指標。</span><span class="sxs-lookup"><span data-stu-id="44dc6-120">Pointer to the current media type.</span></span>                                       |
| <span data-ttu-id="44dc6-121">保護方法</span><span class="sxs-lookup"><span data-stu-id="44dc6-121">Protected Methods</span></span>                                              | <span data-ttu-id="44dc6-122">Description</span><span class="sxs-lookup"><span data-stu-id="44dc6-122">Description</span></span>                                                              |
| [<span data-ttu-id="44dc6-123">**配置**</span><span class="sxs-lookup"><span data-stu-id="44dc6-123">**Alloc**</span></span>](cimageallocator-alloc.md)                         | <span data-ttu-id="44dc6-124">配置緩衝區的記憶體。</span><span class="sxs-lookup"><span data-stu-id="44dc6-124">Allocates memory for the buffers.</span></span>                                        |
| [<span data-ttu-id="44dc6-125">**CheckSizes**</span><span class="sxs-lookup"><span data-stu-id="44dc6-125">**CheckSizes**</span></span>](cimageallocator-checksizes.md)               | <span data-ttu-id="44dc6-126">針對目前的媒體類型檢查配置器屬性。</span><span class="sxs-lookup"><span data-stu-id="44dc6-126">Checks allocator properties against the current media type.</span></span>              |
| [<span data-ttu-id="44dc6-127">**CreateDIB**</span><span class="sxs-lookup"><span data-stu-id="44dc6-127">**CreateDIB**</span></span>](cimageallocator-createdib.md)                 | <span data-ttu-id="44dc6-128">建立 DIB。</span><span class="sxs-lookup"><span data-stu-id="44dc6-128">Creates a DIB.</span></span>                                                           |
| [<span data-ttu-id="44dc6-129">**CreateImageSample**</span><span class="sxs-lookup"><span data-stu-id="44dc6-129">**CreateImageSample**</span></span>](cimageallocator-createimagesample.md) | <span data-ttu-id="44dc6-130">建立媒體範例。</span><span class="sxs-lookup"><span data-stu-id="44dc6-130">Creates a media sample.</span></span> <span data-ttu-id="44dc6-131">虛擬。</span><span class="sxs-lookup"><span data-stu-id="44dc6-131">Virtual.</span></span>                                         |
| [<span data-ttu-id="44dc6-132">**免費**</span><span class="sxs-lookup"><span data-stu-id="44dc6-132">**Free**</span></span>](cimageallocator-free.md)                           | <span data-ttu-id="44dc6-133">釋放所有緩衝區記憶體。</span><span class="sxs-lookup"><span data-stu-id="44dc6-133">Releases all of the buffer memory.</span></span>                                       |
| <span data-ttu-id="44dc6-134">公用方法</span><span class="sxs-lookup"><span data-stu-id="44dc6-134">Public Methods</span></span>                                                 | <span data-ttu-id="44dc6-135">Description</span><span class="sxs-lookup"><span data-stu-id="44dc6-135">Description</span></span>                                                              |
| [<span data-ttu-id="44dc6-136">**CImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="44dc6-136">**CImageAllocator**</span></span>](cimageallocator-cimageallocator.md)     | <span data-ttu-id="44dc6-137">函式方法。</span><span class="sxs-lookup"><span data-stu-id="44dc6-137">Constructor method.</span></span>                                                      |
| [<span data-ttu-id="44dc6-138">**NotifyMediaType**</span><span class="sxs-lookup"><span data-stu-id="44dc6-138">**NotifyMediaType**</span></span>](cimageallocator-notifymediatype.md)     | <span data-ttu-id="44dc6-139">通知物件目前的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="44dc6-139">Informs the object of the current media type.</span></span>                            |
| <span data-ttu-id="44dc6-140">IMemAllocator 方法</span><span class="sxs-lookup"><span data-stu-id="44dc6-140">IMemAllocator Methods</span></span>                                          | <span data-ttu-id="44dc6-141">Description</span><span class="sxs-lookup"><span data-stu-id="44dc6-141">Description</span></span>                                                              |
| [<span data-ttu-id="44dc6-142">**SetProperties**</span><span class="sxs-lookup"><span data-stu-id="44dc6-142">**SetProperties**</span></span>](cimageallocator-setproperties.md)         | <span data-ttu-id="44dc6-143">指定要配置的緩衝區數目和每個緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="44dc6-143">Specifies the number of buffers to allocate and the size of each buffer.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="44dc6-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="44dc6-144">Requirements</span></span>



| <span data-ttu-id="44dc6-145">需求</span><span class="sxs-lookup"><span data-stu-id="44dc6-145">Requirement</span></span> | <span data-ttu-id="44dc6-146">值</span><span class="sxs-lookup"><span data-stu-id="44dc6-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44dc6-147">標頭</span><span class="sxs-lookup"><span data-stu-id="44dc6-147">Header</span></span><br/>  | <dl> <span data-ttu-id="44dc6-148"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="44dc6-148"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="44dc6-149">程式庫</span><span class="sxs-lookup"><span data-stu-id="44dc6-149">Library</span></span><br/> | <dl> <span data-ttu-id="44dc6-150"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="44dc6-150"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44dc6-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44dc6-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44dc6-152">**CDrawImage 類別**</span><span class="sxs-lookup"><span data-stu-id="44dc6-152">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




