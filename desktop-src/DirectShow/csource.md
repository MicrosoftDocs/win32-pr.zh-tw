---
description: CSource 類別是用來執行來源篩選準則的基類。 衍生自 CSource 的篩選包含一或多個衍生自 CSourceStream 類別的輸出圖釘。 每個輸出釘選都會建立會將媒體範例推送至下游的背景工作執行緒。
ms.assetid: 25bd0334-4ad1-48ed-93f9-b36c13a280a3
title: 'CSource 類別 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4fcecbd1973c54e30c9bf1251bed174aa4a469f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989660"
---
# <a name="csource-class"></a><span data-ttu-id="29af1-105">CSource 類別</span><span class="sxs-lookup"><span data-stu-id="29af1-105">CSource class</span></span>

![csource 類別階層](images/source01.png)

<span data-ttu-id="29af1-107">**CSource** 類別是用來執行來源篩選準則的基類。</span><span class="sxs-lookup"><span data-stu-id="29af1-107">The **CSource** class is a base class for implementing source filters.</span></span> <span data-ttu-id="29af1-108">衍生自 **CSource** 的篩選包含一或多個衍生自 [**CSourceStream**](csourcestream.md) 類別的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="29af1-108">A filter derived from **CSource** contains one or more output pins derived from the [**CSourceStream**](csourcestream.md) class.</span></span> <span data-ttu-id="29af1-109">每個輸出釘選都會建立會將媒體範例推送至下游的背景工作執行緒。</span><span class="sxs-lookup"><span data-stu-id="29af1-109">Each output pin creates a worker thread that pushes media samples downstream.</span></span>

> [!Note]  
> <span data-ttu-id="29af1-110">**CSource** 類別是設計來支援資料流程的推送模型。</span><span class="sxs-lookup"><span data-stu-id="29af1-110">The **CSource** class is designed to support the push model for data flow.</span></span> <span data-ttu-id="29af1-111">此類別不建議用來建立檔案讀取器篩選。</span><span class="sxs-lookup"><span data-stu-id="29af1-111">This class is not recommended for creating file-reader filters.</span></span> <span data-ttu-id="29af1-112">檔案讀取器應該透過 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 介面支援提取模型。</span><span class="sxs-lookup"><span data-stu-id="29af1-112">File readers should support the pull model, through the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span> <span data-ttu-id="29af1-113">如需詳細資訊，請參閱 [篩選開發人員的](data-flow-for-filter-developers.md)資料流程。</span><span class="sxs-lookup"><span data-stu-id="29af1-113">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

 



| <span data-ttu-id="29af1-114">受保護的成員變數</span><span class="sxs-lookup"><span data-stu-id="29af1-114">Protected Member Variables</span></span>                     | <span data-ttu-id="29af1-115">Description</span><span class="sxs-lookup"><span data-stu-id="29af1-115">Description</span></span>                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="29af1-116">**m \_ iPins**</span><span class="sxs-lookup"><span data-stu-id="29af1-116">**m\_iPins**</span></span>](csource-m-ipins.md)            | <span data-ttu-id="29af1-117">篩選器上的釘選數目。</span><span class="sxs-lookup"><span data-stu-id="29af1-117">Number of pins on the filter.</span></span>                                |
| [<span data-ttu-id="29af1-118">**m \_ paStreams**</span><span class="sxs-lookup"><span data-stu-id="29af1-118">**m\_paStreams**</span></span>](csource-m-pastreams.md)    | <span data-ttu-id="29af1-119">Pin 的陣列。</span><span class="sxs-lookup"><span data-stu-id="29af1-119">Array of pins.</span></span>                                               |
| [<span data-ttu-id="29af1-120">**m \_ cStateLock**</span><span class="sxs-lookup"><span data-stu-id="29af1-120">**m\_cStateLock**</span></span>](csource-m-cstatelock.md)  | <span data-ttu-id="29af1-121">保護篩選狀態的重要區段物件。</span><span class="sxs-lookup"><span data-stu-id="29af1-121">Critical section object that protects the filter state.</span></span>      |
| <span data-ttu-id="29af1-122">公用方法</span><span class="sxs-lookup"><span data-stu-id="29af1-122">Public Methods</span></span>                                 | <span data-ttu-id="29af1-123">Description</span><span class="sxs-lookup"><span data-stu-id="29af1-123">Description</span></span>                                                  |
| [<span data-ttu-id="29af1-124">**CSource**</span><span class="sxs-lookup"><span data-stu-id="29af1-124">**CSource**</span></span>](csource-csource.md)             | <span data-ttu-id="29af1-125">函式方法。</span><span class="sxs-lookup"><span data-stu-id="29af1-125">Constructor method.</span></span>                                          |
| [<span data-ttu-id="29af1-126">**~ CSource**</span><span class="sxs-lookup"><span data-stu-id="29af1-126">**~CSource**</span></span>](csource--csource.md)           | <span data-ttu-id="29af1-127">函式方法。</span><span class="sxs-lookup"><span data-stu-id="29af1-127">Destructor method.</span></span>                                           |
| [<span data-ttu-id="29af1-128">**GetPinCount**</span><span class="sxs-lookup"><span data-stu-id="29af1-128">**GetPinCount**</span></span>](csource-getpincount.md)     | <span data-ttu-id="29af1-129">抓取篩選上的釘選數目。</span><span class="sxs-lookup"><span data-stu-id="29af1-129">Retrieves the number of pins on the filter.</span></span>                  |
| [<span data-ttu-id="29af1-130">**GetPin**</span><span class="sxs-lookup"><span data-stu-id="29af1-130">**GetPin**</span></span>](csource-getpin.md)               | <span data-ttu-id="29af1-131">捕獲 pin。</span><span class="sxs-lookup"><span data-stu-id="29af1-131">Retrieves a pin.</span></span>                                             |
| [<span data-ttu-id="29af1-132">**pStateLock**</span><span class="sxs-lookup"><span data-stu-id="29af1-132">**pStateLock**</span></span>](csource--pstatelock.md)      | <span data-ttu-id="29af1-133">抓取篩選準則的重要區段物件的指標。</span><span class="sxs-lookup"><span data-stu-id="29af1-133">Retrieves a pointer to the filter's critical section object.</span></span> |
| [<span data-ttu-id="29af1-134">**AddPin**</span><span class="sxs-lookup"><span data-stu-id="29af1-134">**AddPin**</span></span>](csource-addpin.md)               | <span data-ttu-id="29af1-135">將新的輸出圖釘新增至篩選準則。</span><span class="sxs-lookup"><span data-stu-id="29af1-135">Adds a new output pin to the filter.</span></span>                         |
| [<span data-ttu-id="29af1-136">**RemovePin**</span><span class="sxs-lookup"><span data-stu-id="29af1-136">**RemovePin**</span></span>](csource-removepin.md)         | <span data-ttu-id="29af1-137">從篩選中移除指定的 pin。</span><span class="sxs-lookup"><span data-stu-id="29af1-137">Removes a specified pin from the filter.</span></span>                     |
| [<span data-ttu-id="29af1-138">**FindPinNumber**</span><span class="sxs-lookup"><span data-stu-id="29af1-138">**FindPinNumber**</span></span>](csource-findpinnumber.md) | <span data-ttu-id="29af1-139">抓取篩選上指定之圖釘的數目。</span><span class="sxs-lookup"><span data-stu-id="29af1-139">Retrieves the number of a specified pin on the filter.</span></span>       |
| <span data-ttu-id="29af1-140">IBaseFilter 方法</span><span class="sxs-lookup"><span data-stu-id="29af1-140">IBaseFilter Methods</span></span>                            | <span data-ttu-id="29af1-141">Description</span><span class="sxs-lookup"><span data-stu-id="29af1-141">Description</span></span>                                                  |
| [<span data-ttu-id="29af1-142">**FindPin**</span><span class="sxs-lookup"><span data-stu-id="29af1-142">**FindPin**</span></span>](csource-findpin.md)             | <span data-ttu-id="29af1-143">使用指定的識別碼抓取 pin。</span><span class="sxs-lookup"><span data-stu-id="29af1-143">Retrieves the pin with the specified identifier.</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="29af1-144">備註</span><span class="sxs-lookup"><span data-stu-id="29af1-144">Remarks</span></span>

<span data-ttu-id="29af1-145">若要執行輸出釘選，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="29af1-145">To implement an output pin, do the following:</span></span>

-   <span data-ttu-id="29af1-146">從 [**CSourceStream**](csourcestream.md)衍生類別。</span><span class="sxs-lookup"><span data-stu-id="29af1-146">Derive a class from [**CSourceStream**](csourcestream.md).</span></span>
-   <span data-ttu-id="29af1-147">覆寫 [**CSourceStream：： GetMediaType**](csourcestream-getmediatype.md) 方法，可能是 [**CSourceStream：： CheckMediaType**](csourcestream-checkmediatype.md) 方法，它會驗證 pin 的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="29af1-147">Override the [**CSourceStream::GetMediaType**](csourcestream-getmediatype.md) method and possibly the [**CSourceStream::CheckMediaType**](csourcestream-checkmediatype.md) method, which validate media types for the pin.</span></span>
-   <span data-ttu-id="29af1-148">執行 [**CBaseOutputPin：:D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) 方法，這會傳回 pin 的緩衝區需求。</span><span class="sxs-lookup"><span data-stu-id="29af1-148">Implement the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) method, which returns the pin's buffer requirements.</span></span>
-   <span data-ttu-id="29af1-149">執行 [**CSourceStream：： FillBuffer**](csourcestream-fillbuffer.md) 方法，以資料填入媒體範例緩衝區。</span><span class="sxs-lookup"><span data-stu-id="29af1-149">Implement the [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md) method, which fills a media sample buffer with data.</span></span>

<span data-ttu-id="29af1-150">若要執行篩選準則，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="29af1-150">To implement the filter, do the following:</span></span>

-   <span data-ttu-id="29af1-151">從 **CSource** 衍生類別。</span><span class="sxs-lookup"><span data-stu-id="29af1-151">Derive a class from **CSource**.</span></span>
-   <span data-ttu-id="29af1-152">在此函式中，建立一個或多個衍生自 [**CSourceStream**](csourcestream.md)的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="29af1-152">In the constructor, create one or more output pins derived from [**CSourceStream**](csourcestream.md).</span></span> <span data-ttu-id="29af1-153">Pin 會在其函式方法中自動將自己新增至篩選器，並在其函式方法中移除本身。</span><span class="sxs-lookup"><span data-stu-id="29af1-153">The pins automatically add themselves to the filter in their constructor methods, and remove themselves in their destructor methods.</span></span>

<span data-ttu-id="29af1-154">若要同步處理多個執行緒之間的篩選狀態，請呼叫 [**CSource：:P statelock**](csource--pstatelock.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="29af1-154">To synchronize the filter state among multiple threads, call the [**CSource::pStateLock**](csource--pstatelock.md) method.</span></span> <span data-ttu-id="29af1-155">這個方法會將指標傳回至篩選狀態重要區段。</span><span class="sxs-lookup"><span data-stu-id="29af1-155">This method returns a pointer to the filter-state critical section.</span></span> <span data-ttu-id="29af1-156">使用 [**CAutoLock**](cautolock.md) 類別來保存重要區段。</span><span class="sxs-lookup"><span data-stu-id="29af1-156">Use the [**CAutoLock**](cautolock.md) class to hold the critical section.</span></span> <span data-ttu-id="29af1-157">從 pin，您可以從釘選的 [**CBasePin：： m \_ pFilter**](cbasepin-m-pfilter.md)成員變數存取 **pStateLock** ，如下所示：</span><span class="sxs-lookup"><span data-stu-id="29af1-157">From a pin, you can access **pStateLock** from the pin's [**CBasePin::m\_pFilter**](cbasepin-m-pfilter.md) member variable, as follows:</span></span>


```
CAutoLock lock(m_pFilter->pStateLock());
```



## <a name="requirements"></a><span data-ttu-id="29af1-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="29af1-158">Requirements</span></span>



| <span data-ttu-id="29af1-159">需求</span><span class="sxs-lookup"><span data-stu-id="29af1-159">Requirement</span></span> | <span data-ttu-id="29af1-160">值</span><span class="sxs-lookup"><span data-stu-id="29af1-160">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29af1-161">標頭</span><span class="sxs-lookup"><span data-stu-id="29af1-161">Header</span></span><br/>  | <dl> <span data-ttu-id="29af1-162"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="29af1-162"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="29af1-163">程式庫</span><span class="sxs-lookup"><span data-stu-id="29af1-163">Library</span></span><br/> | <dl> <span data-ttu-id="29af1-164"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="29af1-164"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29af1-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29af1-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29af1-166">寫入來源篩選</span><span class="sxs-lookup"><span data-stu-id="29af1-166">Writing Source Filters</span></span>](writing-source-filters.md)
</dt> </dl>

 

 




