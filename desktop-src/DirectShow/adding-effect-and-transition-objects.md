---
description: 新增效果和轉換物件
ms.assetid: fe82392f-33e2-432a-a6e3-710e475547b3
title: 新增效果和轉換物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6d33ed27faa0c69a755a17c72d9c5b136a4670
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025680"
---
# <a name="adding-effect-and-transition-objects"></a><span data-ttu-id="708be-103">新增效果和轉換物件</span><span class="sxs-lookup"><span data-stu-id="708be-103">Adding Effect and Transition Objects</span></span>

<span data-ttu-id="708be-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="708be-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="708be-105">在 DES 中，效果或轉換會以兩個物件表示：</span><span class="sxs-lookup"><span data-stu-id="708be-105">In DES, an effect or transition is represented with two objects:</span></span>

-   <span data-ttu-id="708be-106">*時間軸物件* 代表時間軸內的效果或轉換。</span><span class="sxs-lookup"><span data-stu-id="708be-106">A *timeline object* represents the effect or transition within the timeline.</span></span> <span data-ttu-id="708be-107">為了效果，timeline 物件支援 [**IAMTimelineEffect**](iamtimelineeffect.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="708be-107">For effects, the timeline object supports the [**IAMTimelineEffect**](iamtimelineeffect.md) interface.</span></span> <span data-ttu-id="708be-108">針對轉換，它支援 [**IAMTimelineTrans**](iamtimelinetrans.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="708be-108">For transitions, it supports the [**IAMTimelineTrans**](iamtimelinetrans.md) interface.</span></span> <span data-ttu-id="708be-109">這兩種類型都支援 [**IAMTimelineObj**](iamtimelineobj.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="708be-109">Both types support the [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>
-   <span data-ttu-id="708be-110">子 *物件是一種物件* ，可針對效果或轉換來執行資料處理。</span><span class="sxs-lookup"><span data-stu-id="708be-110">The *subobject* is an object that implements the data processing for the effect or transition.</span></span> <span data-ttu-id="708be-111">時間軸物件會保存子物件的指標。</span><span class="sxs-lookup"><span data-stu-id="708be-111">The timeline object holds a pointer to the subobject.</span></span>

<span data-ttu-id="708be-112">若要新增效果或轉換，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="708be-112">To add an effect or transition, perform the following steps.</span></span>

<span data-ttu-id="708be-113">**1. 建立時間軸物件**</span><span class="sxs-lookup"><span data-stu-id="708be-113">**1. Create the Timeline Object**</span></span>

<span data-ttu-id="708be-114">若要建立時程表物件，請呼叫 [**IAMTimeline：： CreateEmptyNode**](iamtimeline-createemptynode.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="708be-114">To create the timeline object, call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span> <span data-ttu-id="708be-115">為效果設定等於 **時間軸 \_ 主要 \_ 類型 \_ 效果** 的類型，或轉換的 **時間軸 \_ 主要 \_ 類型 \_ 轉換** 。</span><span class="sxs-lookup"><span data-stu-id="708be-115">Set the type equal to **TIMELINE\_MAJOR\_TYPE\_EFFECT** for an effect, or **TIMELINE\_MAJOR\_TYPE\_TRANSITION** for a transition.</span></span>

<span data-ttu-id="708be-116">下列範例會建立一個轉換物件：</span><span class="sxs-lookup"><span data-stu-id="708be-116">The following example creates a transition object:</span></span>


```C++
IAMTimelineObj *pTransObj = NULL;
pTimeline->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);
```



<span data-ttu-id="708be-117">**2. 指定子物件**</span><span class="sxs-lookup"><span data-stu-id="708be-117">**2. Specify the Subobject**</span></span>

<span data-ttu-id="708be-118">時間軸物件會作為另一個物件的包裝函 *式，稱為子物件，它* 會執行實際工作。</span><span class="sxs-lookup"><span data-stu-id="708be-118">The timeline object acts as a wrapper for another object, called the *subobject*, which does the real work.</span></span> <span data-ttu-id="708be-119">子物件會執行資料轉換，以產生所需的效果或轉換。</span><span class="sxs-lookup"><span data-stu-id="708be-119">The subobject implements a data transform that produces the desired effect or transition.</span></span> <span data-ttu-id="708be-120">如需 DES 提供的轉換和效果清單，請參閱 [轉換和效果](transitions-and-effects.md)。</span><span class="sxs-lookup"><span data-stu-id="708be-120">For a list of transitions and effects supplied with DES, see [Transitions and Effects](transitions-and-effects.md).</span></span>

<span data-ttu-id="708be-121">若要設定子物件，請在時間軸物件上呼叫 [**IAMTimelineObj：： SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) 方法，並傳遞類別識別碼 (子物件的 CLSID) 。</span><span class="sxs-lookup"><span data-stu-id="708be-121">To set the subobject, call the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method on the timeline object, passing it the class identifier (CLSID) of the subobject.</span></span> <span data-ttu-id="708be-122">DirectShow 提供可供您用來取得 CLSID 的影片效果和影片轉換的列舉值。</span><span class="sxs-lookup"><span data-stu-id="708be-122">DirectShow provides an enumerator for video effects and video transitions, which you can use to obtain the CLSID.</span></span> <span data-ttu-id="708be-123">如需詳細資訊，請參閱 [列舉效果和轉換](enumerating-effects-and-transitions.md)。</span><span class="sxs-lookup"><span data-stu-id="708be-123">For more information, see [Enumerating Effects and Transitions](enumerating-effects-and-transitions.md).</span></span>

<span data-ttu-id="708be-124">下列範例會將「 [SMPTE](smpte-wipe-transition.md) 抹除」轉換設定為子物件：</span><span class="sxs-lookup"><span data-stu-id="708be-124">The following example sets the [SMPTE Wipe Transition](smpte-wipe-transition.md) as the subobject :</span></span>


```C++
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe
```



<span data-ttu-id="708be-125">**3. 設定開始和停止時間**</span><span class="sxs-lookup"><span data-stu-id="708be-125">**3. Set the Start and Stop Times**</span></span>

<span data-ttu-id="708be-126">若要設定開始和停止時間，請呼叫 [**IAMTimelineObj：： SetStartStop**](iamtimelineobj-setstartstop.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="708be-126">To set the start and stop times, call the [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md) method.</span></span> <span data-ttu-id="708be-127">這些時間相對於父物件的開始時間。</span><span class="sxs-lookup"><span data-stu-id="708be-127">These times are relative to the start time of the parent object.</span></span> <span data-ttu-id="708be-128">效果可能會在相同的物件內重迭，但無法轉換。</span><span class="sxs-lookup"><span data-stu-id="708be-128">Effects can overlap within the same object, but transitions cannot.</span></span>

<span data-ttu-id="708be-129">下列範例會將開始時間設定為5秒，並將停止時間設定為10秒：</span><span class="sxs-lookup"><span data-stu-id="708be-129">The following example sets the start time to 5 seconds and the stop time to 10 seconds:</span></span>


```C++
const REFERENCE_TIME ONE_SECOND = 10000000
hr = pTransObj->SetStartStop(5 * ONE_SECOND, 10 * ONE_SECOND);
```



<span data-ttu-id="708be-130">轉譯轉換時，每個畫面格的轉換進度會根據 **進度** 屬性來計算，該屬性會正規化為0.0 到1.0 的範圍。</span><span class="sxs-lookup"><span data-stu-id="708be-130">When a transition is rendered, the progress of the transition at each frame is calculated based on a **Progress** property, which is normalized to a range of 0.0 to 1.0.</span></span> <span data-ttu-id="708be-131">DES 會使用每個畫面格的開始時間來計算進度值。</span><span class="sxs-lookup"><span data-stu-id="708be-131">DES uses the start time of each frame to calculate the progress value.</span></span> <span data-ttu-id="708be-132">這表示，如果轉換停止時間等於來源停止時間，則 **進度** 值絕對不會達到1.0，因為最後一個畫面格的開始時間與停止時間稍微不同。</span><span class="sxs-lookup"><span data-stu-id="708be-132">This means if the transition stop time is equal to the source stop time, the **Progress** value will never reach exactly 1.0, because the start time of the last frame is slightly than the stop time.</span></span> <span data-ttu-id="708be-133">若要讓轉換達到1.0，請將轉換停止時間設定為至少一個早于來源停止時間的畫面格。</span><span class="sxs-lookup"><span data-stu-id="708be-133">To make the transition reach 1.0, set the transition stop time to be at least one frame earlier than the source stop time.</span></span>

<span data-ttu-id="708be-134">**4. 將物件插入至時間軸**</span><span class="sxs-lookup"><span data-stu-id="708be-134">**4. Insert the Object into the Timeline**</span></span>

<span data-ttu-id="708be-135">若要將物件插入至時間軸，請根據物件類型，在父系上呼叫下列其中一種方法：</span><span class="sxs-lookup"><span data-stu-id="708be-135">To insert the object into the timeline, call one of the following methods on the parent, depending on the object type:</span></span>

-   <span data-ttu-id="708be-136">效果： [ **IAMTimelineEffectable：： EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)</span><span class="sxs-lookup"><span data-stu-id="708be-136">Effects: [**IAMTimelineEffectable::EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)</span></span>
-   <span data-ttu-id="708be-137">轉換： [ **IAMTimelineTransable：： TransAdd**](iamtimelinetransable-transadd.md)</span><span class="sxs-lookup"><span data-stu-id="708be-137">Transitions: [**IAMTimelineTransable::TransAdd**](iamtimelinetransable-transadd.md)</span></span>

<span data-ttu-id="708be-138">在 [**IAMTimelineEffectable：： EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md) 方法中，您必須指定效果的優先順序。</span><span class="sxs-lookup"><span data-stu-id="708be-138">In the [**IAMTimelineEffectable::EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md) method, you must specify the priority of the effect.</span></span> <span data-ttu-id="708be-139">當效果在相同物件上重迭時，會依優先順序套用。</span><span class="sxs-lookup"><span data-stu-id="708be-139">When effects overlap on the same object, they are applied in order of priority.</span></span> <span data-ttu-id="708be-140">音量信封音訊效果是例外狀況;如需詳細資訊，請參閱 [音量信封效果](volume-envelope-effect.md) 參考。</span><span class="sxs-lookup"><span data-stu-id="708be-140">The Volume Envelope audio effect is an exception; see the [Volume Envelope Effect](volume-envelope-effect.md) reference for details.</span></span> <span data-ttu-id="708be-141">在組合內，所有音訊播放軌都會在套用該組合的音訊效果之前進行混合。</span><span class="sxs-lookup"><span data-stu-id="708be-141">Within a composition, all audio tracks are mixed before the audio effects for that composition are applied.</span></span>

<span data-ttu-id="708be-142">因為轉換在相同物件上不能重迭，所以它們沒有優先權值。</span><span class="sxs-lookup"><span data-stu-id="708be-142">Because transitions cannot overlap on the same object, they do not have a priority value.</span></span>

<span data-ttu-id="708be-143">下列範例會將轉換物件新增至追蹤：</span><span class="sxs-lookup"><span data-stu-id="708be-143">The following example adds the transition object to a track:</span></span>


```C++
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
```



<span data-ttu-id="708be-144">此範例會查詢 [**IAMTimelineTransable**](iamtimelinetransable.md) 介面的 track 物件，然後再呼叫 AddTrans。</span><span class="sxs-lookup"><span data-stu-id="708be-144">The example queries the track object for the [**IAMTimelineTransable**](iamtimelinetransable.md) interface before calling AddTrans.</span></span>

<span data-ttu-id="708be-145">**5. 設定屬性**</span><span class="sxs-lookup"><span data-stu-id="708be-145">**5. Set Properties**</span></span>

<span data-ttu-id="708be-146">許多效果和轉換都支援自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="708be-146">Many effects and transitions support custom properties.</span></span> <span data-ttu-id="708be-147">如需詳細資訊，請參閱 [設定效果和轉換的屬性](setting-properties-on-effects-and-transitions.md)。</span><span class="sxs-lookup"><span data-stu-id="708be-147">For information, see [Setting Properties on Effects and Transitions](setting-properties-on-effects-and-transitions.md).</span></span>

<span data-ttu-id="708be-148">範例</span><span class="sxs-lookup"><span data-stu-id="708be-148">Example</span></span>

<span data-ttu-id="708be-149">下列程式碼範例會將 [SMPTE 抹除轉換](smpte-wipe-transition.md) 新增至追蹤。它會假設播放軌物件已經存在於時間軸中。</span><span class="sxs-lookup"><span data-stu-id="708be-149">The following code example adds a [SMPTE Wipe Transition](smpte-wipe-transition.md) to a track. It assumes that the track object already exists in the timeline.</span></span>


```C++
IAMTimeline *pTL;
IAMTimelineTrack *pTrack;

// Create timeline with track (not shown).

// Create the transition object. 
IAMTimelineObj *pTransObj = NULL;
hr = pTL->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);

// Set the subobject. 
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe

// Set the start and stop times. 
hr = pTransObj->SetStartStop(50000000, 100000000);

// Insert the transition object into the timeline. 
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
pTransObj->Release();
```



## <a name="related-topics"></a><span data-ttu-id="708be-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="708be-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="708be-151">使用效果和轉換</span><span class="sxs-lookup"><span data-stu-id="708be-151">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



