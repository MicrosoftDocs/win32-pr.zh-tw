---
description: 您可以使用筆墨收集器 (InkCollector、InkOverlay 或 InkPicture) ，直接存取預設的 Microsoft 手勢辨識器。若要使用筆墨收集器來存取手勢辨識器：將筆墨收集器的 CollectionMode 屬性設定為 InkAndGesture 模式或 GestureOnly 模式。 CollectionMode = CollectionMode. GestureOnly;選擇您想要支援的手勢 SetGestureStatus (ApplicationGesture. AllGestures，true) ; 會執行接收手勢通知的事件處理常式。 在事件處理常式中，您必須執行對應至每個收到事件的動作。附注混合模式僅支援單一筆觸手勢。 手勢模式支援多個筆觸手勢。 inkOverlay + = 新 InkCollectorGestureEventHandler (inkOverlay \_ 手勢) ; 在 InkAndGesture 模式中，每個個別筆劃都會傳送至 Microsoft 手勢辨識器。 如果它被辨識為您已啟用的手勢，則會傳送事件通知。 如果應用程式接受事件通知，則會清除筆觸。 如果應用程式不接受通知，或是筆劃無法辨識為手勢，則筆觸會儲存在筆跡物件中。在 GestureOnly 模式中，筆劃會以筆劃前後的超時來分隔。 在超時時間內收集的筆劃會傳送至辨識器。 如果筆劃被辨識為您已啟用的手勢，則會傳送事件通知。 應用程式可能會接受或拒絕事件，並影響對應的動作。 在僅限手勢模式中，筆劃永遠不會儲存在筆跡物件中。
ms.assetid: 3f5f00a3-1f2c-4fa2-9738-bc5fb56e2208
title: 僅使用 Microsoft 手勢辨識器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d7b27ae30e0bba98ee2c9db57cc0da2d6491932d0137cc5cd4d2b6f86420ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715175"
---
# <a name="using-the-microsoft-gesture-recognizer-only"></a>僅使用 Microsoft 手勢辨識器

您可以使用筆墨收集器 ([**InkCollector**](inkcollector-class.md)、 [**InkOverlay**](inkoverlay-class.md)或 [InkPicture](inkpicture-control-reference.md)) ，直接存取預設的 Microsoft 手勢辨識器。

若要使用筆墨收集器來存取手勢辨識器：

-   將筆墨收集器的 [**CollectionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) 屬性設定為 **InkAndGesture** 模式或 **GestureOnly** 模式。

`inkOverlay.CollectionMode = CollectionMode.GestureOnly;`

-   選擇您想要支援的手勢。

`inkOverlay.SetGestureStatus(ApplicationGesture.AllGestures, true);`

-   執行接收手勢通知的事件處理常式。 在事件處理常式中，您必須執行對應至每個收到事件的動作。
    > [!Note]  
    > 混合模式僅支援單一筆觸手勢。 手勢模式支援多個筆觸手勢。

     

`inkOverlay.Gesture += new InkCollectorGestureEventHandler(inkOverlay_Gesture);`

在 **InkAndGesture** 模式中，每個個別筆劃都會傳送至 Microsoft 手勢辨識器。 如果它被辨識為您已啟用的手勢，則會傳送事件通知。 如果應用程式接受事件通知，則會清除筆觸。 如果應用程式不接受通知，或是筆劃無法辨識為手勢，則筆觸會儲存在 [**筆跡**](inkdisp-class.md) 物件中。

在 **GestureOnly** 模式中，筆劃會以筆劃前後的超時來分隔。 在超時時間內收集的筆劃會傳送至辨識器。 如果筆劃被辨識為您已啟用的手勢，則會傳送事件通知。 應用程式可能會接受或拒絕事件，並影響對應的動作。 在僅限手勢模式中，筆劃永遠不會儲存在 [**筆跡**](inkdisp-class.md) 物件中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[InkCollector. CollectionMode](/previous-versions/ms836497(v=msdn.10))
</dt> <dt>

[CollectionMode。](/previous-versions/ms833092(v=msdn.10))
</dt> <dt>

[InkPicture. CollectionMode](/previous-versions/ms582182(v=vs.100))
</dt> </dl>

 

 
