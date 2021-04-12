---
description: 您可以使用筆墨收集器 (InkCollector、InkOverlay 或 InkPicture) ，直接存取預設的 Microsoft 手勢辨識器。若要使用筆墨收集器來存取手勢辨識器：將筆墨收集器的 CollectionMode 屬性設定為 InkAndGesture 模式或 GestureOnly 模式。 CollectionMode = CollectionMode. GestureOnly;選擇您想要支援的手勢 SetGestureStatus (ApplicationGesture. AllGestures，true) ; 會執行接收手勢通知的事件處理常式。 在事件處理常式中，您必須執行對應至每個收到事件的動作。附注混合模式僅支援單一筆觸手勢。 手勢模式支援多個筆觸手勢。 inkOverlay + = 新 InkCollectorGestureEventHandler (inkOverlay \_ 手勢) ; 在 InkAndGesture 模式中，每個個別筆劃都會傳送至 Microsoft 手勢辨識器。 如果它被辨識為您已啟用的手勢，則會傳送事件通知。 如果應用程式接受事件通知，則會清除筆觸。 如果應用程式不接受通知，或是筆劃無法辨識為手勢，則筆觸會儲存在筆跡物件中。在 GestureOnly 模式中，筆劃會以筆劃前後的超時來分隔。 在超時時間內收集的筆劃會傳送至辨識器。 如果筆劃被辨識為您已啟用的手勢，則會傳送事件通知。 應用程式可能會接受或拒絕事件，並影響對應的動作。 在僅限手勢模式中，筆劃永遠不會儲存在筆跡物件中。
ms.assetid: 3f5f00a3-1f2c-4fa2-9738-bc5fb56e2208
title: 僅使用 Microsoft 手勢辨識器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80504e8b32c0b9596936bb4f07d029cd4ea8ddbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847977"
---
# <a name="using-the-microsoft-gesture-recognizer-only"></a><span data-ttu-id="fc4ce-113">僅使用 Microsoft 手勢辨識器</span><span class="sxs-lookup"><span data-stu-id="fc4ce-113">Using the Microsoft Gesture Recognizer Only</span></span>

<span data-ttu-id="fc4ce-114">您可以使用筆墨收集器 ([**InkCollector**](inkcollector-class.md)、 [**InkOverlay**](inkoverlay-class.md)或 [InkPicture](inkpicture-control-reference.md)) ，直接存取預設的 Microsoft 手勢辨識器。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-114">You can use an ink collector ([**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md), or [InkPicture](inkpicture-control-reference.md)) to access the default Microsoft gesture recognizer directly.</span></span>

<span data-ttu-id="fc4ce-115">若要使用筆墨收集器來存取手勢辨識器：</span><span class="sxs-lookup"><span data-stu-id="fc4ce-115">To use an ink collector to access the gesture recognizer:</span></span>

-   <span data-ttu-id="fc4ce-116">將筆墨收集器的 [**CollectionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) 屬性設定為 **InkAndGesture** 模式或 **GestureOnly** 模式。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-116">Set the [**CollectionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) property of the ink collector to either **InkAndGesture** mode or **GestureOnly** mode.</span></span>

`inkOverlay.CollectionMode = CollectionMode.GestureOnly;`

-   <span data-ttu-id="fc4ce-117">選擇您想要支援的手勢。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-117">Choose the gesture that you want to support.</span></span>

`inkOverlay.SetGestureStatus(ApplicationGesture.AllGestures, true);`

-   <span data-ttu-id="fc4ce-118">執行接收手勢通知的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-118">Implement an event handler that receives gesture notifications.</span></span> <span data-ttu-id="fc4ce-119">在事件處理常式中，您必須執行對應至每個收到事件的動作。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-119">In the event handler, you need to implement the action corresponding to each event received.</span></span>
    > [!Note]  
    > <span data-ttu-id="fc4ce-120">混合模式僅支援單一筆觸手勢。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-120">Mixed mode supports only single-stroke gestures.</span></span> <span data-ttu-id="fc4ce-121">手勢模式支援多個筆觸手勢。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-121">Gesture mode supports multiple stroke gestures.</span></span>

     

`inkOverlay.Gesture += new InkCollectorGestureEventHandler(inkOverlay_Gesture);`

<span data-ttu-id="fc4ce-122">在 **InkAndGesture** 模式中，每個個別筆劃都會傳送至 Microsoft 手勢辨識器。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-122">In **InkAndGesture** mode, each individual stroke is sent to the Microsoft gesture recognizer.</span></span> <span data-ttu-id="fc4ce-123">如果它被辨識為您已啟用的手勢，則會傳送事件通知。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-123">If it is recognized as a gesture that you have enabled, an event notification is sent.</span></span> <span data-ttu-id="fc4ce-124">如果應用程式接受事件通知，則會清除筆觸。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-124">If the application accepts the event notification, the stroke is erased.</span></span> <span data-ttu-id="fc4ce-125">如果應用程式不接受通知，或是筆劃無法辨識為手勢，則筆觸會儲存在 [**筆跡**](inkdisp-class.md) 物件中。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-125">If the application does not accept the notification or if the stroke is not recognized to be a gesture, the stroke is stored in the [**Ink**](inkdisp-class.md) object.</span></span>

<span data-ttu-id="fc4ce-126">在 **GestureOnly** 模式中，筆劃會以筆劃前後的超時來分隔。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-126">In **GestureOnly** mode, the strokes are delimited by timeouts before and after the strokes.</span></span> <span data-ttu-id="fc4ce-127">在超時時間內收集的筆劃會傳送至辨識器。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-127">The strokes collected within the timeout are sent to the recognizer.</span></span> <span data-ttu-id="fc4ce-128">如果筆劃被辨識為您已啟用的手勢，則會傳送事件通知。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-128">If the strokes are recognized as a gesture that you have enabled, an event notification is sent.</span></span> <span data-ttu-id="fc4ce-129">應用程式可能會接受或拒絕事件，並影響對應的動作。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-129">The application may accept or reject the event, effecting the corresponding action or not.</span></span> <span data-ttu-id="fc4ce-130">在僅限手勢模式中，筆劃永遠不會儲存在 [**筆跡**](inkdisp-class.md) 物件中。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-130">In gesture-only mode, the strokes are never saved in the [**Ink**](inkdisp-class.md) object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc4ce-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="fc4ce-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="fc4ce-132">[InkCollector. CollectionMode](/previous-versions/ms836497(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="fc4ce-132">[Microsoft.Ink.InkCollector.CollectionMode](/previous-versions/ms836497(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="fc4ce-133">[CollectionMode。](/previous-versions/ms833092(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="fc4ce-133">[Microsoft.Ink.InkOverlay.CollectionMode](/previous-versions/ms833092(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="fc4ce-134">[InkPicture. CollectionMode](/previous-versions/ms582182(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="fc4ce-134">[Microsoft.Ink.InkPicture.CollectionMode](/previous-versions/ms582182(v=vs.100))</span></span>
</dt> </dl>

 

 
