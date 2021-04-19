---
description: CRenderedInputPin 類別是用來在轉譯器上執行輸入釘選的基類。
ms.assetid: 644dc6ef-eefa-4dfa-a27e-cab690b6e1db
title: 'CRenderedInputPin 類別 (Amextra) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3fc00b4aa0ce1fc6c8a93fb2fbda2118ad6bb40e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998844"
---
# <a name="crenderedinputpin-class"></a><span data-ttu-id="ff845-103">CRenderedInputPin 類別</span><span class="sxs-lookup"><span data-stu-id="ff845-103">CRenderedInputPin class</span></span>

![crenderedinputpin 類別階層](images/rbase04.png)

<span data-ttu-id="ff845-105">**CRenderedInputPin** 類別是用來在轉譯器上執行輸入釘選的基類。</span><span class="sxs-lookup"><span data-stu-id="ff845-105">The **CRenderedInputPin** class is a base class for implementing an input pin on a renderer.</span></span> <span data-ttu-id="ff845-106">這個類別是針對並非衍生自 [**CBaseRenderer**](cbaserenderer.md) 類別的轉譯器篩選所設計。</span><span class="sxs-lookup"><span data-stu-id="ff845-106">This class is designed for renderer filters that do not derive from the [**CBaseRenderer**](cbaserenderer.md) class.</span></span> <span data-ttu-id="ff845-107"> (衍生自 **CBaseRenderer** 的篩選器應該使用輸入 Pin 的 [**CRendererInputPin**](crendererinputpin.md) 類別。 ) </span><span class="sxs-lookup"><span data-stu-id="ff845-107">(Filters that derive from **CBaseRenderer** should use the [**CRendererInputPin**](crendererinputpin.md) class for the input pin.)</span></span>

<span data-ttu-id="ff845-108">若要使用這個類別，您必須至少執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="ff845-108">To use this class, you must do at least the following:</span></span>

-   <span data-ttu-id="ff845-109">宣告繼承 **CRenderedInputPin** 的新 pin 類別。</span><span class="sxs-lookup"><span data-stu-id="ff845-109">Declare a new pin class that inherits **CRenderedInputPin**.</span></span>
-   <span data-ttu-id="ff845-110">在您的 pin 類別中，宣告重要區段物件以保存串流鎖定。</span><span class="sxs-lookup"><span data-stu-id="ff845-110">In your pin class, declare a critical section object to hold the streaming lock.</span></span> <span data-ttu-id="ff845-111">您可以針對此用途使用 [**CCritSec**](ccritsec.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="ff845-111">You can use the [**CCritSec**](ccritsec.md) class for this purpose.</span></span> <span data-ttu-id="ff845-112">如需詳細資訊，請參閱 [執行緒和重要區段](threads-and-critical-sections.md)。</span><span class="sxs-lookup"><span data-stu-id="ff845-112">For more information, see [Threads and Critical Sections](threads-and-critical-sections.md).</span></span>
-   <span data-ttu-id="ff845-113">覆寫 [**CRenderedInputPin：： EndOfStream**](crenderedinputpin-endofstream.md) 以保存串流鎖定。</span><span class="sxs-lookup"><span data-stu-id="ff845-113">Override [**CRenderedInputPin::EndOfStream**](crenderedinputpin-endofstream.md) to hold the streaming lock.</span></span>
-   <span data-ttu-id="ff845-114">執行 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)、 [**CBasePin：： CheckMediaType**](cbasepin-checkmediatype.md)和 [**CBasePin：： GetMediaType**](cbasepin-getmediatype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="ff845-114">Implement the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md), and [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) methods.</span></span>
-   <span data-ttu-id="ff845-115">在篩選準則中，請執行 [**CBaseFilter：： GetPin**](cbasefilter-getpin.md) 來傳回您的 pin 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="ff845-115">In your filter, implement [**CBaseFilter::GetPin**](cbasefilter-getpin.md) to return an instance of your pin class.</span></span>

<span data-ttu-id="ff845-116">您可以在具有多個輸入釘選的轉譯器中使用這個類別。</span><span class="sxs-lookup"><span data-stu-id="ff845-116">You can use this class in a renderer that has more than one input pin.</span></span> <span data-ttu-id="ff845-117">此類別會繼承 [**CBaseInputPin**](cbaseinputpin.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="ff845-117">This class inherits the [**CBaseInputPin**](cbaseinputpin.md) class.</span></span>



| <span data-ttu-id="ff845-118">受保護的成員變數</span><span class="sxs-lookup"><span data-stu-id="ff845-118">Protected Member Variables</span></span>                                            | <span data-ttu-id="ff845-119">Description</span><span class="sxs-lookup"><span data-stu-id="ff845-119">Description</span></span>                                                                                                  |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff845-120">**m \_ bAtEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="ff845-120">**m\_bAtEndOfStream**</span></span>](crenderedinputpin-m-batendofstream.md)       | <span data-ttu-id="ff845-121">指出是否已到達資料流程的結尾。</span><span class="sxs-lookup"><span data-stu-id="ff845-121">Indicates whether the end of the stream was reached.</span></span>                                                         |
| [<span data-ttu-id="ff845-122">**m \_ bCompleteNotified**</span><span class="sxs-lookup"><span data-stu-id="ff845-122">**m\_bCompleteNotified**</span></span>](crenderedinputpin-m-bcompletenotified.md) | <span data-ttu-id="ff845-123">指出釘選是否已將 [**EC \_ 完成**](ec-complete.md) 事件傳送至篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="ff845-123">Indicates whether the pin has sent an [**EC\_COMPLETE**](ec-complete.md) event to the Filter Graph Manager.</span></span> |
| <span data-ttu-id="ff845-124">公用方法</span><span class="sxs-lookup"><span data-stu-id="ff845-124">Public Methods</span></span>                                                        | <span data-ttu-id="ff845-125">Description</span><span class="sxs-lookup"><span data-stu-id="ff845-125">Description</span></span>                                                                                                  |
| [<span data-ttu-id="ff845-126">**使用中**</span><span class="sxs-lookup"><span data-stu-id="ff845-126">**Active**</span></span>](crenderedinputpin-active.md)                            | <span data-ttu-id="ff845-127">通知釘選篩選現在已啟用。</span><span class="sxs-lookup"><span data-stu-id="ff845-127">Notifies the pin that the filter is now active.</span></span>                                                              |
| [<span data-ttu-id="ff845-128">**CRenderedInputPin**</span><span class="sxs-lookup"><span data-stu-id="ff845-128">**CRenderedInputPin**</span></span>](crenderedinputpin-crenderedinputpin.md)      | <span data-ttu-id="ff845-129">函式方法。</span><span class="sxs-lookup"><span data-stu-id="ff845-129">Constructor method.</span></span>                                                                                          |
| [<span data-ttu-id="ff845-130">**執行**</span><span class="sxs-lookup"><span data-stu-id="ff845-130">**Run**</span></span>](crenderedinputpin-run.md)                                  | <span data-ttu-id="ff845-131">通知釘選篩選現在正在執行。</span><span class="sxs-lookup"><span data-stu-id="ff845-131">Notifies the pin that the filter is now running.</span></span>                                                             |
| <span data-ttu-id="ff845-132">IPin 方法</span><span class="sxs-lookup"><span data-stu-id="ff845-132">IPin Methods</span></span>                                                          | <span data-ttu-id="ff845-133">Description</span><span class="sxs-lookup"><span data-stu-id="ff845-133">Description</span></span>                                                                                                  |
| [<span data-ttu-id="ff845-134">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="ff845-134">**EndFlush**</span></span>](crenderedinputpin-endflush.md)                        | <span data-ttu-id="ff845-135">結束清除操作。</span><span class="sxs-lookup"><span data-stu-id="ff845-135">Ends a flush operation.</span></span>                                                                                      |
| [<span data-ttu-id="ff845-136">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="ff845-136">**EndOfStream**</span></span>](crenderedinputpin-endofstream.md)                  | <span data-ttu-id="ff845-137">通知 pin，在篩選器收到新的執行命令之前，不需要額外的資料。</span><span class="sxs-lookup"><span data-stu-id="ff845-137">Notifies the pin that no additional data is expected until the filter receives a new run command.</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="ff845-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff845-138">Requirements</span></span>



| <span data-ttu-id="ff845-139">需求</span><span class="sxs-lookup"><span data-stu-id="ff845-139">Requirement</span></span> | <span data-ttu-id="ff845-140">值</span><span class="sxs-lookup"><span data-stu-id="ff845-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff845-141">標頭</span><span class="sxs-lookup"><span data-stu-id="ff845-141">Header</span></span><br/>  | <dl> <span data-ttu-id="ff845-142"><dt>Amextra (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ff845-142"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ff845-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="ff845-143">Library</span></span><br/> | <dl> <span data-ttu-id="ff845-144"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ff845-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




