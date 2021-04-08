---
description: 感應器 API 可以提供事件通知。
ms.assetid: 2400619c-ee9c-4662-ae57-6d4bc317e730
title: 關於感應器 API 事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e941dca86d5b7ec3aa9922220c1232b10429f60a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851504"
---
# <a name="about-sensor-api-events"></a>關於感應器 API 事件

感應器 API 可以提供事件通知。

當您透過 [**ISensor：： SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) 或 [**ISensorManager：： SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink)註冊來接收事件時，您必須提供回呼介面的指標。 您必須在程式碼中執行回呼介面的方法。 感應器 API 會定義下列回呼介面：

-   [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents)。 執行此介面以接收來自感應器的事件。 感應器可以通知應用程式有關新資料、感應器狀態變更、感應器中斷連線，以及由感應器製造商定義的自訂事件。
-   [**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents)。 執行此介面以接收來自感應器管理員的事件。 感應器管理員可以在感應器連線時通知您的應用程式，因此可能會可供使用。

您可以再次呼叫 [**SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) 來取消事件通知，這次會透過參數傳遞 **Null** 值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用感應器 API 事件](using-sensor-api-events.md)
</dt> </dl>

 

 
