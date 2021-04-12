---
description: 概述使用 StylusInput 應用程式開發介面 (Api) 來設計應用程式的考慮。
ms.assetid: cb68a6bb-dd38-4dfb-bbbb-b5d846e5aa0a
title: StylusInput API 的設計考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff526d8e073f00156730d79ea2caf1a02c5e5af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320451"
---
# <a name="design-considerations-for-the-stylusinput-api"></a>StylusInput API 的設計考慮

以下是 StylusInput API 的設計考慮。

-   當畫筆處於關閉狀態時，您可以更新 [ [**RealTimeStylus**](realtimestylus-class.md) ] 物件的 [**WindowInputRectangle**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle)屬性，以及 [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))物件的 [**ClipRectangle**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_cliprectangle)屬性。 當您想要在應用程式收集筆墨時擁有動態繪圖區域時，這會很有用。
-   為了將外掛程式程式碼的重複使用和維護優化，外掛程式不應該直接呼叫應用程式，但應該使用 managed 程式碼) 中的 [**CustomStylusData**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-customstylusdataadded) ([CustomeStylusData](/previous-versions/ms824747(v=msdn.10)) 物件來與應用程式進行通訊。
-   已排序 [**RealTimeStylus**](realtimestylus-class.md) 物件的外掛程式集合。 外掛程式在這些集合中的相對位置可能非常重要。 例如，可能會在動態轉譯器外掛程式之前，將修改封包資訊的外掛程式加入至同步的外掛程式集合。
-   應謹慎使用將自訂手寫筆資料新增至 tablet 畫筆資料串流的功能。 只有當另一個外掛程式需要在資料流程中接收這項資訊時，才使用此功能。 此外，請避免加入自訂手寫筆資料，以回應傳入外掛程式的其他自訂手寫筆資料，因為這可以建立無限迴圈。
-   啟用 [**RealTimeStylus**](realtimestylus-class.md) 物件時，可以修改外掛程式集合;不過，這可能會讓應用程式的行為難以預測。 當啟用了 **realtimestylus** 物件時，加入外掛程式時， **realtimestylus** 物件會呼叫外掛程式的 StylusInput. IStylusSyncPlugin。 在 managed 程式碼) 中， [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled)方法 ([IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10))或 [StylusInput. IStylusAsyncPlugin 方法。](/previous-versions/ms824775(v=msdn.10)) 當在啟用 **RealTimeStylus** 物件時移除外掛程式時， **realtimestylus** 物件會呼叫外掛程式的 [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled)方法， (StylusInput 的 managed 程式碼中的 [IStylusSyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10))或 StylusInput. IStylusAsyncPlugin 方法) 。 [](/previous-versions/ms824774(v=msdn.10)) 這可讓外掛程式維持適當的狀態，而不需要檢查 **RealTimeStylus** 物件的 [**Enabled**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_enabled)屬性。當您在啟用 **RealTimeStylus** 物件時加入外掛程式時，外掛程式所接收的外掛程式資料可能不會包含足夠的資訊，以充分建立初始資料的內容。 例如，新加入的外掛程式可能會開始從中間筆劃的畫筆接收封包資料。 同樣地，當啟用 **RealTimeStylus** 物件時移除外掛程式時，外掛程式所收到的外掛程式資料可能不足以完成處理資料。
    > [!Note]  
    > 若要取得整體穩定性，請在呼叫其 [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) 或 [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) 方法時重設外掛程式的內部狀態。

     

-   如果外掛程式修改附加的外掛程式集合，則 [**RealTimeStylus**](realtimestylus-class.md) 物件會擲回例外狀況。 只有當外掛程式 **以該集合** 的成員身分呼叫它時，才會發生這種情況。

 

 
