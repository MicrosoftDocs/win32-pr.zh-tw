---
description: CBaseRendererInputPin 類別會為 CBaseRenderer 類別實作為輸入的 pin。 除非另有說明，否則這個類別中的方法會委派至 CBaseRenderer 類別上的對應方法。
ms.assetid: da3e6aba-c2cc-4fd4-b382-fc4bc7fef774
title: 'CRendererInputPin 類別 (Renbase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ec48b31170b2233f211e7e72de81d8792ae9160
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000994"
---
# <a name="crendererinputpin-class"></a><span data-ttu-id="1ac49-104">CRendererInputPin 類別</span><span class="sxs-lookup"><span data-stu-id="1ac49-104">CRendererInputPin class</span></span>

![crendererinput 釘選類別階層](images/rbase01.png)

<span data-ttu-id="1ac49-106">**CBaseRendererInputPin** 類別會為 [**CBaseRenderer**](cbaserenderer.md)類別實作為輸入的 pin。</span><span class="sxs-lookup"><span data-stu-id="1ac49-106">The **CBaseRendererInputPin** class implements an input pin for the [**CBaseRenderer**](cbaserenderer.md) class.</span></span> <span data-ttu-id="1ac49-107">除非另有說明，否則這個類別中的方法會委派至 **CBaseRenderer** 類別上的對應方法。</span><span class="sxs-lookup"><span data-stu-id="1ac49-107">Except where noted, the methods in this class delegate to corresponding methods on the **CBaseRenderer** class.</span></span>



| <span data-ttu-id="1ac49-108">受保護的成員變數</span><span class="sxs-lookup"><span data-stu-id="1ac49-108">Protected Member Variables</span></span>                                       | <span data-ttu-id="1ac49-109">Description</span><span class="sxs-lookup"><span data-stu-id="1ac49-109">Description</span></span>                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ac49-110">**m \_ pRenderer**</span><span class="sxs-lookup"><span data-stu-id="1ac49-110">**m\_pRenderer**</span></span>](crendererinputpin-m-prenderer.md)            | <span data-ttu-id="1ac49-111">篩選準則的指標。</span><span class="sxs-lookup"><span data-stu-id="1ac49-111">Pointer to the filter.</span></span>                                                                 |
| <span data-ttu-id="1ac49-112">公用方法</span><span class="sxs-lookup"><span data-stu-id="1ac49-112">Public Methods</span></span>                                                   | <span data-ttu-id="1ac49-113">Description</span><span class="sxs-lookup"><span data-stu-id="1ac49-113">Description</span></span>                                                                            |
| [<span data-ttu-id="1ac49-114">**CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="1ac49-114">**CRendererInputPin**</span></span>](crendererinputpin-crendererinputpin.md) | <span data-ttu-id="1ac49-115">函式方法。</span><span class="sxs-lookup"><span data-stu-id="1ac49-115">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="1ac49-116">**BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="1ac49-116">**BreakConnect**</span></span>](crendererinputpin-breakconnect.md)           | <span data-ttu-id="1ac49-117">在中斷連接時新增自訂程式碼。</span><span class="sxs-lookup"><span data-stu-id="1ac49-117">Adds customized code upon breaking a connection.</span></span>                                       |
| [<span data-ttu-id="1ac49-118">**CompleteConnect**</span><span class="sxs-lookup"><span data-stu-id="1ac49-118">**CompleteConnect**</span></span>](crendererinputpin-completeconnect.md)     | <span data-ttu-id="1ac49-119">完成連接。</span><span class="sxs-lookup"><span data-stu-id="1ac49-119">Completes the connection.</span></span>                                                              |
| [<span data-ttu-id="1ac49-120">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="1ac49-120">**CheckMediaType**</span></span>](crendererinputpin-checkmediatype.md)       | <span data-ttu-id="1ac49-121">判斷 pin 是否可以支援特定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="1ac49-121">Determines if the pin can support a specific media type.</span></span>                               |
| [<span data-ttu-id="1ac49-122">**使用中**</span><span class="sxs-lookup"><span data-stu-id="1ac49-122">**Active**</span></span>](crendererinputpin-active.md)                       | <span data-ttu-id="1ac49-123">將釘選切換為作用中的 (已暫停或正在執行) 模式。</span><span class="sxs-lookup"><span data-stu-id="1ac49-123">Switches the pin to the active (paused or running) mode.</span></span>                               |
| [<span data-ttu-id="1ac49-124">**非使用中**</span><span class="sxs-lookup"><span data-stu-id="1ac49-124">**Inactive**</span></span>](crendererinputpin-inactive.md)                   | <span data-ttu-id="1ac49-125">將釘選切換為非使用中狀態，並釋放配置器的記憶體。</span><span class="sxs-lookup"><span data-stu-id="1ac49-125">Switches the pin to an inactive state and releases the memory of the allocator.</span></span>        |
| [<span data-ttu-id="1ac49-126">**SetMediaType**</span><span class="sxs-lookup"><span data-stu-id="1ac49-126">**SetMediaType**</span></span>](crendererinputpin-setmediatype.md)           | <span data-ttu-id="1ac49-127">設定釘選的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="1ac49-127">Sets the media type of the pin.</span></span>                                                        |
| [<span data-ttu-id="1ac49-128">**分配器**</span><span class="sxs-lookup"><span data-stu-id="1ac49-128">**Allocator**</span></span>](crendererinputpin-allocator.md)                 | <span data-ttu-id="1ac49-129">捕獲預設記憶體配置器的指標。</span><span class="sxs-lookup"><span data-stu-id="1ac49-129">Retrieves a pointer to the default memory allocator.</span></span>                                   |
| <span data-ttu-id="1ac49-130">IPin 方法</span><span class="sxs-lookup"><span data-stu-id="1ac49-130">IPin Methods</span></span>                                                     | <span data-ttu-id="1ac49-131">Description</span><span class="sxs-lookup"><span data-stu-id="1ac49-131">Description</span></span>                                                                            |
| [<span data-ttu-id="1ac49-132">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="1ac49-132">**QueryId**</span></span>](crendererinputpin-queryid.md)                     | <span data-ttu-id="1ac49-133">抓取 pin 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1ac49-133">Retrieves an identifier for the pin.</span></span>                                                   |
| [<span data-ttu-id="1ac49-134">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="1ac49-134">**EndOfStream**</span></span>](crendererinputpin-endofstream.md)             | <span data-ttu-id="1ac49-135">通知 pin，在發出新的執行命令之前，不需要額外的資料。</span><span class="sxs-lookup"><span data-stu-id="1ac49-135">Informs the pin that no additional data is expected until a new run command is issued.</span></span> |
| [<span data-ttu-id="1ac49-136">**BeginFlush**</span><span class="sxs-lookup"><span data-stu-id="1ac49-136">**BeginFlush**</span></span>](crendererinputpin-beginflush.md)               | <span data-ttu-id="1ac49-137">通知 pin 開始進行清除作業。</span><span class="sxs-lookup"><span data-stu-id="1ac49-137">Informs the pin to begin a flush operation.</span></span>                                            |
| [<span data-ttu-id="1ac49-138">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="1ac49-138">**EndFlush**</span></span>](crendererinputpin-endflush.md)                   | <span data-ttu-id="1ac49-139">通知 pin 結束清除作業。</span><span class="sxs-lookup"><span data-stu-id="1ac49-139">Informs the pin to end a flush operation.</span></span>                                              |
| <span data-ttu-id="1ac49-140">IMemInputPin 方法</span><span class="sxs-lookup"><span data-stu-id="1ac49-140">IMemInputPin Methods</span></span>                                             | <span data-ttu-id="1ac49-141">Description</span><span class="sxs-lookup"><span data-stu-id="1ac49-141">Description</span></span>                                                                            |
| [<span data-ttu-id="1ac49-142">**收到**</span><span class="sxs-lookup"><span data-stu-id="1ac49-142">**Receive**</span></span>](crendererinputpin-receive.md)                     | <span data-ttu-id="1ac49-143">從資料流程抓取下一個資料區塊。</span><span class="sxs-lookup"><span data-stu-id="1ac49-143">Retrieves the next block of data from the stream.</span></span>                                      |



 

## <a name="requirements"></a><span data-ttu-id="1ac49-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ac49-144">Requirements</span></span>



| <span data-ttu-id="1ac49-145">需求</span><span class="sxs-lookup"><span data-stu-id="1ac49-145">Requirement</span></span> | <span data-ttu-id="1ac49-146">值</span><span class="sxs-lookup"><span data-stu-id="1ac49-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ac49-147">標頭</span><span class="sxs-lookup"><span data-stu-id="1ac49-147">Header</span></span><br/>  | <dl> <span data-ttu-id="1ac49-148"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1ac49-148"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1ac49-149">程式庫</span><span class="sxs-lookup"><span data-stu-id="1ac49-149">Library</span></span><br/> | <dl> <span data-ttu-id="1ac49-150"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="1ac49-150"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




