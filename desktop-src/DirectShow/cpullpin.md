---
description: CPullPin 類別可支援透過 IAsyncReader 介面提取資料的輸入圖釘。
ms.assetid: 33a6c342-3896-41f8-b32d-01db3eed003e
title: 'CPullPin 類別 (Pullpin) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3039f97ca7fda43e4ecc6bd4eae05fff2ce90e55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978451"
---
# <a name="cpullpin-class"></a><span data-ttu-id="423cb-103">CPullPin 類別</span><span class="sxs-lookup"><span data-stu-id="423cb-103">CPullPin class</span></span>

![cpullpin 類別階層](images/pulpin01.png)

<span data-ttu-id="423cb-105">`CPullPin`類別可支援透過 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader)介面提取資料的輸入圖釘。</span><span class="sxs-lookup"><span data-stu-id="423cb-105">The `CPullPin` class provides support for input pins that pull data through the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span> <span data-ttu-id="423cb-106">如果您正在執行使用提取模型來要求上游篩選器資料的篩選，請使用這個類別。</span><span class="sxs-lookup"><span data-stu-id="423cb-106">Use this class if you are implementing a filter that uses the pull model to request data from the upstream filter.</span></span> <span data-ttu-id="423cb-107">如需詳細資訊，請參閱篩選圖形和提取模型中的資料流程。</span><span class="sxs-lookup"><span data-stu-id="423cb-107">For more information, see Data Flow in the Filter Graph and Pull Model.</span></span>

<span data-ttu-id="423cb-108">這個類別不會衍生自 **CBasePin** 或實作為 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面，而某些方法名稱會與 **IPin** 衝突，因此最適合用來做為 pin 內的 helper 物件。</span><span class="sxs-lookup"><span data-stu-id="423cb-108">This class does not derive from **CBasePin** or implement the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface, and some of the method names clash with **IPin**, so it is best used as a helper object inside your pin.</span></span> <span data-ttu-id="423cb-109">若要使用此類別，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="423cb-109">To use this class, do the following:</span></span>

1.  <span data-ttu-id="423cb-110">從衍生一個 helper 類別 `CPullPin` ，並從 **CBasePin** 衍生一個輸入圖釘類別。</span><span class="sxs-lookup"><span data-stu-id="423cb-110">Derive a helper class from `CPullPin`, and derive an input pin class from **CBasePin**.</span></span> <span data-ttu-id="423cb-111">將物件的實例宣告 `CPullPin` 為釘選類別的成員變數。</span><span class="sxs-lookup"><span data-stu-id="423cb-111">Declare an instance of the `CPullPin` object as a member variable of the pin class.</span></span>
2.  <span data-ttu-id="423cb-112">覆寫 [**CBasePin：： CheckConnect**](cbasepin-checkconnect.md) 方法以呼叫 [**CPullPin：： Connect**](cpullpin-connect.md)。</span><span class="sxs-lookup"><span data-stu-id="423cb-112">Override the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method to call [**CPullPin::Connect**](cpullpin-connect.md).</span></span> <span data-ttu-id="423cb-113">這個方法會查詢另一個 pin 以進行 **IAsyncReader**。</span><span class="sxs-lookup"><span data-stu-id="423cb-113">This method queries the other pin for **IAsyncReader**.</span></span>
3.  <span data-ttu-id="423cb-114">覆寫 [**CBasePin：： BreakConnect**](cbasepin-breakconnect.md) 方法以呼叫 [**CPullPin：:D isconnect**](cpullpin-disconnect.md)。</span><span class="sxs-lookup"><span data-stu-id="423cb-114">Override the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method to call [**CPullPin::Disconnect**](cpullpin-disconnect.md).</span></span>
4.  <span data-ttu-id="423cb-115">覆寫 [**CBasePin：： active**](cbasepin-active.md) 方法以呼叫 [**CPullPin：： active**](cpullpin-active.md)。</span><span class="sxs-lookup"><span data-stu-id="423cb-115">Override the [**CBasePin::Active**](cbasepin-active.md) method to call [**CPullPin::Active**](cpullpin-active.md).</span></span> <span data-ttu-id="423cb-116">這個方法會啟動從上游篩選器提取樣本的背景工作執行緒。</span><span class="sxs-lookup"><span data-stu-id="423cb-116">This method starts up a worker thread that pulls samples from the upstream filter.</span></span> <span data-ttu-id="423cb-117">當釘選連線時，您可以指定是否要讓工作者執行緒建立異步或同步讀取要求。</span><span class="sxs-lookup"><span data-stu-id="423cb-117">When the pins connect, you can specify whether you want the worker thread to make asynchronous or synchronous read requests.</span></span>
5.  <span data-ttu-id="423cb-118">覆寫 [**CBasePin：：非**](cbasepin-inactive.md) 使用中方法，以呼叫 [**CPullPin：：非**](cpullpin-inactive.md)使用中。</span><span class="sxs-lookup"><span data-stu-id="423cb-118">Override the [**CBasePin::Inactive**](cbasepin-inactive.md) method to call [**CPullPin::Inactive**](cpullpin-inactive.md).</span></span> <span data-ttu-id="423cb-119">這個方法會關閉背景工作執行緒。</span><span class="sxs-lookup"><span data-stu-id="423cb-119">This method shuts down the worker thread.</span></span>
6.  <span data-ttu-id="423cb-120">執行純虛擬 [**CPullPin：： Receive**](cpullpin-receive.md) 方法來處理傳入範例，並將其傳遞至下游。</span><span class="sxs-lookup"><span data-stu-id="423cb-120">Implement the pure virtual [**CPullPin::Receive**](cpullpin-receive.md) method to process incoming samples and deliver them downstream.</span></span>
7.  <span data-ttu-id="423cb-121">若要設定停止和開始位置，或要搜尋資料流程，請呼叫 [**CPullPin：： seek**](cpullpin-seek.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="423cb-121">To set the stop and start positions, or to seek the stream, call the [**CPullPin::Seek**](cpullpin-seek.md) method.</span></span> <span data-ttu-id="423cb-122">這個方法會暫停背景工作執行緒，並清除篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="423cb-122">This method pauses the worker thread and flushes the filter graph.</span></span>
8.  <span data-ttu-id="423cb-123">依照這些方法的備註所述，執行純虛擬 [**CPullPin：： EndOfStream**](cpullpin-endofstream.md)、 [**CPullPin：： BeginFlush**](cpullpin-beginflush.md)和 [**CPullPin：： EndFlush**](cpullpin-endflush.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="423cb-123">Implement the pure virtual [**CPullPin::EndOfStream**](cpullpin-endofstream.md), [**CPullPin::BeginFlush**](cpullpin-beginflush.md), and [**CPullPin::EndFlush**](cpullpin-endflush.md) methods, as described in the remarks for those methods.</span></span>
9.  <span data-ttu-id="423cb-124">執行純虛擬 [**CPullPin：： OnError**](cpullpin-onerror.md) 方法來處理串流錯誤。</span><span class="sxs-lookup"><span data-stu-id="423cb-124">Implement the pure virtual [**CPullPin::OnError**](cpullpin-onerror.md) method to handle streaming errors.</span></span>



| <span data-ttu-id="423cb-125">Public 成員變數</span><span class="sxs-lookup"><span data-stu-id="423cb-125">Public Member Variables</span></span>                             | <span data-ttu-id="423cb-126">Description</span><span class="sxs-lookup"><span data-stu-id="423cb-126">Description</span></span>                                                                           |
|-----------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="423cb-127">**m \_ pAlloc**</span><span class="sxs-lookup"><span data-stu-id="423cb-127">**m\_pAlloc**</span></span>](cpullpin-m-palloc.md)              | <span data-ttu-id="423cb-128">記憶體配置器之 **IMemAllocator** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="423cb-128">Pointer to the **IMemAllocator** interface of the memory allocator.</span></span>                   |
| <span data-ttu-id="423cb-129">公用方法</span><span class="sxs-lookup"><span data-stu-id="423cb-129">Public Methods</span></span>                                      | <span data-ttu-id="423cb-130">Description</span><span class="sxs-lookup"><span data-stu-id="423cb-130">Description</span></span>                                                                           |
| [<span data-ttu-id="423cb-131">**使用中**</span><span class="sxs-lookup"><span data-stu-id="423cb-131">**Active**</span></span>](cpullpin-active.md)                   | <span data-ttu-id="423cb-132">建立從輸出釘選提取資料的背景工作執行緒。</span><span class="sxs-lookup"><span data-stu-id="423cb-132">Creates a worker thread that pulls data from the output pin.</span></span>                          |
| [<span data-ttu-id="423cb-133">**AlignDown**</span><span class="sxs-lookup"><span data-stu-id="423cb-133">**AlignDown**</span></span>](cpullpin-aligndown.md)             | <span data-ttu-id="423cb-134">將值截斷為指定的對齊界限。</span><span class="sxs-lookup"><span data-stu-id="423cb-134">Truncates a value to a specified alignment boundary.</span></span>                                  |
| [<span data-ttu-id="423cb-135">**AlignUp**</span><span class="sxs-lookup"><span data-stu-id="423cb-135">**AlignUp**</span></span>](cpullpin-alignup.md)                 | <span data-ttu-id="423cb-136">將值四捨五入到指定的對齊界限。</span><span class="sxs-lookup"><span data-stu-id="423cb-136">Rounds a value up to a specified alignment boundary.</span></span>                                  |
| [<span data-ttu-id="423cb-137">**連接**</span><span class="sxs-lookup"><span data-stu-id="423cb-137">**Connect**</span></span>](cpullpin-connect.md)                 | <span data-ttu-id="423cb-138">完成輸出釘選的連接。</span><span class="sxs-lookup"><span data-stu-id="423cb-138">Completes a connection to the output pin.</span></span>                                             |
| [<span data-ttu-id="423cb-139">**CPullPin**</span><span class="sxs-lookup"><span data-stu-id="423cb-139">**CPullPin**</span></span>](cpullpin-cpullpin.md)               | <span data-ttu-id="423cb-140">函式方法。</span><span class="sxs-lookup"><span data-stu-id="423cb-140">Constructor method.</span></span>                                                                   |
| [<span data-ttu-id="423cb-141">**~ CPullPin**</span><span class="sxs-lookup"><span data-stu-id="423cb-141">**~CPullPin**</span></span>](cpullpin--cpullpin.md)             | <span data-ttu-id="423cb-142">函式方法。</span><span class="sxs-lookup"><span data-stu-id="423cb-142">Destructor method.</span></span> <span data-ttu-id="423cb-143">虛擬。</span><span class="sxs-lookup"><span data-stu-id="423cb-143">Virtual.</span></span>                                                           |
| [<span data-ttu-id="423cb-144">**DecideAllocator**</span><span class="sxs-lookup"><span data-stu-id="423cb-144">**DecideAllocator**</span></span>](cpullpin-decideallocator.md) | <span data-ttu-id="423cb-145">使用輸出圖釘協調配置器。</span><span class="sxs-lookup"><span data-stu-id="423cb-145">Negotiates an allocator with the output pin.</span></span> <span data-ttu-id="423cb-146">虛擬。</span><span class="sxs-lookup"><span data-stu-id="423cb-146">Virtual.</span></span>                                 |
| [<span data-ttu-id="423cb-147">**中斷連線**</span><span class="sxs-lookup"><span data-stu-id="423cb-147">**Disconnect**</span></span>](cpullpin-disconnect.md)           | <span data-ttu-id="423cb-148">使用輸出圖釘 Beaks 連接。</span><span class="sxs-lookup"><span data-stu-id="423cb-148">Beaks the connection with the output pin.</span></span>                                             |
| [<span data-ttu-id="423cb-149">**持續時間**</span><span class="sxs-lookup"><span data-stu-id="423cb-149">**Duration**</span></span>](cpullpin-duration.md)               | <span data-ttu-id="423cb-150">捕獲資料流程的持續時間。</span><span class="sxs-lookup"><span data-stu-id="423cb-150">Retrieves the duration of the stream.</span></span>                                                 |
| [<span data-ttu-id="423cb-151">**System.diagnostics.symbolstore.isymbolbinder1.getreader**</span><span class="sxs-lookup"><span data-stu-id="423cb-151">**GetReader**</span></span>](cpullpin-getreader.md)             | <span data-ttu-id="423cb-152">傳回輸出釘選 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="423cb-152">Returns a pointer to the output pin's [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span> |
| [<span data-ttu-id="423cb-153">**非使用中**</span><span class="sxs-lookup"><span data-stu-id="423cb-153">**Inactive**</span></span>](cpullpin-inactive.md)               | <span data-ttu-id="423cb-154">關閉從輸出圖釘提取資料的背景工作執行緒。</span><span class="sxs-lookup"><span data-stu-id="423cb-154">Shuts down the worker thread that pulls data from the output pin.</span></span>                     |
| [<span data-ttu-id="423cb-155">**Seek**</span><span class="sxs-lookup"><span data-stu-id="423cb-155">**Seek**</span></span>](cpullpin-seek.md)                       | <span data-ttu-id="423cb-156">設定資料流程的開始和停止位置。</span><span class="sxs-lookup"><span data-stu-id="423cb-156">Sets the start and stop positions of the stream.</span></span>                                      |
| <span data-ttu-id="423cb-157">純虛擬方法</span><span class="sxs-lookup"><span data-stu-id="423cb-157">Pure Virtual Methods</span></span>                                | <span data-ttu-id="423cb-158">Description</span><span class="sxs-lookup"><span data-stu-id="423cb-158">Description</span></span>                                                                           |
| [<span data-ttu-id="423cb-159">**BeginFlush**</span><span class="sxs-lookup"><span data-stu-id="423cb-159">**BeginFlush**</span></span>](cpullpin-beginflush.md)           | <span data-ttu-id="423cb-160">通知擁有篩選以排清下游篩選。</span><span class="sxs-lookup"><span data-stu-id="423cb-160">Informs the owning filter to flush the downstream filters.</span></span>                            |
| [<span data-ttu-id="423cb-161">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="423cb-161">**EndFlush**</span></span>](cpullpin-endflush.md)               | <span data-ttu-id="423cb-162">通知擁有篩選結束清除作業。</span><span class="sxs-lookup"><span data-stu-id="423cb-162">Informs the owning filter to end a flush operation.</span></span>                                   |
| [<span data-ttu-id="423cb-163">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="423cb-163">**EndOfStream**</span></span>](cpullpin-endofstream.md)         | <span data-ttu-id="423cb-164">在物件傳遞最後一個範例之後呼叫。</span><span class="sxs-lookup"><span data-stu-id="423cb-164">Called after the object delivers the last sample.</span></span>                                     |
| [<span data-ttu-id="423cb-165">**OnError**</span><span class="sxs-lookup"><span data-stu-id="423cb-165">**OnError**</span></span>](cpullpin-onerror.md)                 | <span data-ttu-id="423cb-166">在串流處理期間發生錯誤時呼叫。</span><span class="sxs-lookup"><span data-stu-id="423cb-166">Called if an error occurs during streaming.</span></span>                                           |
| [<span data-ttu-id="423cb-167">**收到**</span><span class="sxs-lookup"><span data-stu-id="423cb-167">**Receive**</span></span>](cpullpin-receive.md)                 | <span data-ttu-id="423cb-168">當物件從輸出圖釘接收媒體範例時呼叫。</span><span class="sxs-lookup"><span data-stu-id="423cb-168">Called when the object receives a media sample from the output pin.</span></span>                   |



 

## <a name="requirements"></a><span data-ttu-id="423cb-169">規格需求</span><span class="sxs-lookup"><span data-stu-id="423cb-169">Requirements</span></span>



| <span data-ttu-id="423cb-170">需求</span><span class="sxs-lookup"><span data-stu-id="423cb-170">Requirement</span></span> | <span data-ttu-id="423cb-171">值</span><span class="sxs-lookup"><span data-stu-id="423cb-171">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="423cb-172">標頭</span><span class="sxs-lookup"><span data-stu-id="423cb-172">Header</span></span><br/>  | <dl> <span data-ttu-id="423cb-173"><dt>Pullpin (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="423cb-173"><dt>Pullpin.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="423cb-174">程式庫</span><span class="sxs-lookup"><span data-stu-id="423cb-174">Library</span></span><br/> | <dl> <span data-ttu-id="423cb-175"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="423cb-175"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




