---
title: 控制 COM) 的事件 (
description: 除了提供屬性和方法之外，控制項也提供輸出介面來通知其用戶端事件。
ms.assetid: e7085bc0-c087-4cc8-9c69-ba05b0923b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b987202cb4e4e635a947ed60e9f947cc428f0aaaacb3d27c27d60ad536b636
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119243628"
---
# <a name="control-events-com"></a>控制 COM) 的事件 (

除了提供屬性和方法之外，控制項也提供輸出介面來通知其用戶端事件。 用戶端必須支援這些事件的處理。 如需可連線物件如何運作的詳細資訊，請參閱 [COM 中的事件和](events-in-com-and-connectable-objects.md) 可連接的物件。

控制項可以針對不同目的支援不同的輸出介面。 所有輸出介面都會標示為控制項類型資訊中的來源介面，但只有一個會標示為預設值，表示它是主要的輸出介面。

容器可支援一個或多個由控制項定義的連出介面。 控制項應該準備好處理只提供某些輸出介面支援的容器。

控制項支援四種類型的事件：

-   要求事件。 控制項會要求其用戶端的許可權，藉由呼叫輸出介面中的方法來進行某個動作，進而觸發要求事件。 用戶端會在控制項呼叫的方法中，透過布林值 out 參數來對控制項發出信號。 因此，用戶端可以防止控制項執行動作。
-   之前的事件。 控制項會通知其用戶端，它會藉由呼叫輸出介面中的方法來進行某個動作，進而觸發 before 事件。 用戶端沒有機會可以防止該動作，但它可以採取任何必要的步驟，並指定即將發生的動作。
-   After 事件之後。 控制項會通知其用戶端，它只會在輸出介面中呼叫方法來完成某項工作，進而觸發 after 事件。 同樣地，用戶端無法取消此動作，但它可以採取必要的步驟，並提供所發生的動作。
-   進行事件。 控制項會觸發 do 事件，以允許其用戶端覆寫控制項的動作，並提供一些替代或補充動作。 通常，控制項針對 do 事件所呼叫的方法，有許多參數可與用戶端協商將會發生的動作。

下列 dispid 是針對控制項可支援的標準事件所定義： Click、DblClick、KeyDown、KeyPress、KeyUp、MouseMove、MouseUp 和 Error。 所有這些標準事件都有負的 DISPID 值，表示其標準狀態。

以 **TRUE** 呼叫 [**IOleControl：： FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents)方法時，會告知控制項容器是否會從控制項中處理事件，直到再次以 **FALSE** 呼叫 **FreezeEvents** 為止。 在這段時間內，控制權無法相依于實際處理任何事件的容器。 如果必須處理事件，控制項應該將事件排入佇列，以便在以 **FALSE** 呼叫 **FreezeEvents** 時引發事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ActiveX控制](activex-controls.md)
</dt> </dl>

 

 




