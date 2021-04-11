---
description: 提供從畫筆或觸控數位板取得手寫筆事件的存取權。
ms.assetid: a239b53c-7fc9-4211-962a-6cfbe0be4e4c
title: RealTimeStylus 參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9016779c3165bc8fb6e24e5612901a7fd58435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193717"
---
# <a name="realtimestylus-reference"></a>RealTimeStylus 參考

提供從畫筆或觸控數位板取得手寫筆事件的存取權。

## <a name="in-this-section"></a>本節內容

-   [RealTimeStylus 類別和介面](realtimestylus-classes-and-interfaces.md)
-   [RealTimeStylus 列舉](realtimestylus-enumerations.md)
-   [RealTimeStylus 結構](realtimestylus-structures.md)

## <a name="remarks"></a>備註

這個物件會實 [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) COM 介面。

此物件可以透過在 c + + 中呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化。

您可以完全控制、動態轉譯、修改，甚至刪除 [**RealTimeStylus 類別**](realtimestylus-class.md) 物件的同步和非同步外掛程式內的封包資料流程中的資料。

即時手寫筆會提供一種方法來建立 **InkCollecting** 物件，該物件為單一執行緒，且常駐于應用程式 UI 執行緒中。 這個 **InkCollecting** 物件會從佇列存取即時手寫筆資料。 **InkCollecting** 物件與即時手寫筆搭配使用，可讓您即時選取編輯和即時編輯所收集的筆墨資料。 如需詳細資訊，請參閱 [存取和操作手寫筆輸入](accessing-and-manipulating-stylus-input.md)。

使用 [**RealTimeStylus 類別**](realtimestylus-class.md) 物件直接與 tablet 手寫筆資料流程互動，或封鎖即時手寫。 當這些物件的預設行為提供您所需的行為時，請使用 [**InkCollector 類別**](inkcollector-class.md) 物件、 [**InkOverlay 類別**](inkoverlay-class.md) 物件、 [InkPicture 控制項](inkpicture-control-reference.md) 控制項或 [InkEdit 控制項](inkedit-control-reference.md) 控制項。

即時手寫筆事件是在特定視窗輸入矩形內的特定視窗控制碼上。 RealTimeStylusService 可將手寫筆資料傳送至多個 [**RealTimeStylus 類別**](realtimestylus-class.md) 物件。 每個 **RealTimeStylus 類別** 物件都會根據該 **RealTimeStylus 類別** 物件的定義 [**IRealTimeStylus：： WindowInputRectangle 屬性**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle)，接收特定視窗區段的手寫筆資料。 **RealTimeStylus 類別** 物件會取得手寫筆資料，然後透過同步和非同步外掛程式的清單進行處理。

同步外掛程式與非同步外掛程式之間的差異在於它們執行所在的執行緒和呼叫順序。 同步外掛程式是由執行 [**RealTimeStylus 類別**](realtimestylus-class.md) 物件的執行緒呼叫。 每次具現化 **RealTimeStylus 類別** 物件時，都會具現化執行執行緒。 同步外掛程式是在這個新的執行緒上執行，以針對 **RealTimeStylus 類別** 物件的實例來具現化。 非同步外掛程式是在同步外掛程式處理封包資料流程之後，透過 UI 或應用程式執行緒呼叫，並且儲存在輸出佇列中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IDynamicRenderer 介面**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)
</dt> <dt>

[**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)
</dt> <dt>

[**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
</dt> <dt>

[**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)
</dt> </dl>

 

 
