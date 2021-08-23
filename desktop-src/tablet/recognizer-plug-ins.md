---
description: 辨識器外掛程式是一種物件，可監視筆勢、手寫或其他物件的 tablet 畫筆移動。
ms.assetid: 764a327e-1da0-487f-9245-b6a4f3f43502
title: 辨識器外掛程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b64f8f9b63cdbdc7309e7d9bd303ecce7a6b59b2e3b3c0cde976d1d6eefdf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091521"
---
# <a name="recognizer-plug-ins"></a>辨識器外掛程式

辨識器外掛程式是一種物件，可監視筆勢、手寫或其他物件的 tablet 畫筆移動。

## <a name="system-gestures"></a>系統手勢

[**RealTimeStylus**](realtimestylus-class.md)物件可識別系統手勢。 **RealTimeStylus** 物件會將 [SystemGestureData](/previous-versions/ms824019(v=msdn.10))物件新增至 [StylusQueues](/previous-versions/ms824786(v=msdn.10))佇列，以回應完成手勢的資料，例如 [SystemGesture](/previous-versions/bb345349(v=vs.100))的 [StylusUpData](/previous-versions/ms824057(v=msdn.10))物件。 如需詳細資訊，請參閱 [外掛程式資料和 RealTimeStylus 類別](plug-in-data-and-the-realtimestylus-class.md)。

## <a name="the-gesturerecognizer-object"></a>GestureRecognizer 物件

[**GestureRecognizer**](gesturerecognizer-class.md)物件會實 [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)和 [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)介面。 **GestureRecognizer** 物件可識別應用程式手勢。 就內部而言， **GestureRecognizer** 物件會使用 Microsoft 手勢辨識器來執行手勢辨識。

當 [**GestureRecognizer**](gesturerecognizer-class.md) 物件辨識手勢時，它會將自訂手寫筆資料新增至 [StylusQueues](/previous-versions/ms824786(v=msdn.10)) 佇列，以回應筆劃的 [StylusUpData](/previous-versions/ms824057(v=msdn.10)) 物件。 [CustomStylusData](/previous-versions/ms575208(v=vs.100))物件的[CustomDataId](/previous-versions/ms824748(v=msdn.10))屬性設定為[GestureRecognitionDataGuid](/previous-versions/ms826344(v=msdn.10))值，而 CustomStylusData 物件的[Data](/previous-versions/ms824749(v=msdn.10))屬性包含[GestureRecognitionData](/previous-versions/ms824594(v=msdn.10))物件。

下圖說明 [**GestureRecognizer**](gesturerecognizer-class.md) 物件如何將資料新增至 tablet 畫筆資料。

![gesturerecognizer 資料流程的圖例](images/c4c77c33-deee-49d0-84bc-12612575ec66.gif)

在此圖中，以字母 "SD" 表示 [StylusDownData](/previous-versions/ms824107(v=msdn.10))物件，而圓形 "P" 代表已新增至 [**RealTimeStylus**](realtimestylus-class.md)物件輸出佇列且尚未傳送至非同步外掛程式集合的 [PacketsData](/previous-versions/ms824590(v=msdn.10))物件。 以字母 "SU" 表示 [StylusUpData](/previous-versions/ms824057(v=msdn.10)) 物件，此物件目前正在 **處理的物件** 。 它會傳送至同步的外掛程式集合，然後放在輸出佇列中。 圓形「GR」表示自訂手寫筆資料，由 [**GestureRecognizer**](gesturerecognizer-class.md) 外掛程式新增至輸入佇列，以回應與「SU」相關聯的手寫筆上傳通知。 自訂手寫筆資料的字母 "GR" 接著會傳遞至同步的外掛程式，然後再傳遞至輸出佇列，然後再處理下一個 tablet 畫筆資料。 空的圓形代表在輸出佇列中加入未來 tablet 畫筆資料的位置。

根據預設， [**GestureRecognizer**](gesturerecognizer-class.md) 物件只會辨識單一筆劃手勢;不過， **GestureRecognizer** 物件可以設定為辨識 multistroke 手勢。 針對 multistroke 手勢， [CustomStylusData](/previous-versions/ms575208(v=vs.100)) 物件會加入至 [StylusQueues](/previous-versions/ms824786(v=msdn.10)) 佇列，以回應筆勢最後筆劃的 [StylusUpData](/previous-versions/ms824057(v=msdn.10)) 物件。 辨識 multistroke 手勢時，您可能會收到重迭筆劃集合的通知。 例如，第一個和第二個筆劃會被辨識為一個手勢，而第二個筆劃本身可能會被辨識為手勢。 如需 multistroke 手勢辨識的詳細資訊，請參閱 **GestureRecognizer** 類別和 [MaxStrokeCount](/previous-versions/ms826053(v=msdn.10)) 屬性。

如果您使用 [**GestureRecognizer**](gesturerecognizer-class.md) 物件進行 multistroke 手勢辨識，則可以使用串聯的 [**realtimestylus**](realtimestylus-class.md) 模型並將 **GestureRecognizer** 物件附加至次要 **RealTimeStylus** 物件，以達到最佳效能。 如需串聯式 **realtimestylus** 模型的詳細資訊，請參閱 [串聯的 realtimestylus 模型](the-cascaded-realtimestylus-model.md)。

### <a name="special-considerations"></a>特殊考慮

下列清單描述使用 [**GestureRecognizer**](gesturerecognizer-class.md) 物件時應考慮的其他重點。

-   您不應該將 [**GestureRecognizer**](gesturerecognizer-class.md) 物件附加至一個以上的 [**RealTimeStylus**](realtimestylus-class.md) 物件。 一旦已啟用 **GestureRecognizer** 物件附加的兩個 **RealTimeStylus** 物件，就會發生下列情況。
    -   [**GestureRecognizer**](gesturerecognizer-class.md)物件會擲回例外狀況，以回應其 RealTimeStylusEnabled 方法的第二次呼叫。
    -   已啟用的第二個 [**RealTimeStylus**](realtimestylus-class.md) 物件會產生 [ErrorData](/previous-versions/ms824740(v=msdn.10)) 物件，並在該錯誤的外掛程式集合中通知剩餘的外掛程式。
    -   [**GestureRecognizer**](gesturerecognizer-class.md)物件會停止辨識手勢。
-   當呼叫 [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10))方法時，如果將 *guid* 參數設定為 [StylusInput](/previous-versions/ms826344(v=msdn.10)) [**，則會**](realtimestylus-class.md)擲回例外狀況（ (guid) 的全域唯一識別碼）。
-   [**GestureRecognizer**](gesturerecognizer-class.md)物件會實作為元件物件模型 (COM) 包裝函式，而且您無法直接呼叫其 [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)或 [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)介面方法。 如需 COM 執行和 [**RealTimeStylus**](realtimestylus-class.md) 物件的詳細資訊，請參閱 [StylusInput Api 的執行附注](implementation-notes-for-the-stylusinput-apis.md)。

## <a name="custom-gesture-recognition"></a>自訂手勢辨識

您可以透過下列方式建立可辨識手寫、手勢或其他物件的自訂辨識器外掛程式：

-   將筆劃資訊傳遞給現有的辨識 [器](/previous-versions/ms829434(v=msdn.10)) 物件，並使用 [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) 方法將結果新增至 tablet 畫筆資料串流。
-   在您的外掛程式內執行辨識，並使用 [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) 方法將結果新增至 tablet 畫筆資料串流。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用程式手勢](application-gestures.md)
</dt> <dt>

[系統手勢](system-gestures.md)
</dt> <dt>

[滑鼠訊息和系統事件的時間軸](timeline-of-mouse-messages-and-system-events.md)
</dt> </dl>

 

 
