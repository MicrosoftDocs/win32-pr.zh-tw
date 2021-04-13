---
title: System-Level 和 Object-Level 事件
description: Microsoft Active Accessibility 使用三個類別的 WinEvents 系統層級、物件層級和主控台。
ms.assetid: 3333fe6c-38cd-4e7e-be4b-94c9f824e7e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d14a0469527a7654dd3e323adb47d650866ca9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300579"
---
# <a name="system-level-and-object-level-events"></a>System-Level 和 Object-Level 事件

Microsoft Active Accessibility 使用三個 WinEvents 類別： *系統層級*、 *物件層級* 和 *主控台*。 每一個都有下列對應的 [事件常](event-constants.md) 數值：

-   以事件系統開頭的事件常數 \_ 可識別系統層級事件。 這些事件會說明影響系統中所有應用程式的情況。
-   以 EVENT 物件開頭的事件常數會 \_ 識別物件層級的事件。 這些事件與某個應用程式內物件特定的情況有關。
-   以事件主控台開頭的事件常數 \_ 可識別主控台層級的事件。 這些事件表示主控台視窗中的變更。

事件的系統層級和物件層級類別都是由作業系統和伺服器應用程式所產生。 作業系統會針對下列案例產生系統層級和物件層級的事件：

-   有關焦點變更的全系統通知
-   啟用變更
-   關於系統提供物件的事件，例如通用控制項

伺服器應用程式會針對複寫系統物件的自訂物件產生系統層級事件，例如自訂功能表和捲軸。

伺服器應用程式通常會產生物件層級的事件，以便變更其所包含的可存取物件，例如物件建立、損毀和選取。

雖然系統會產生 [**視窗**](window.md) 物件的物件層級事件，但是伺服器也必須針對視窗中包含的每個可存取物件傳送物件層級事件。 例如，如果伺服器應用程式註冊應用程式定義的視窗類別來建立自訂控制項，系統就會為包含自訂控制項的視窗產生物件層級的事件。伺服器會產生可存取物件的物件層級事件，以提供控制項的相關資訊。

伺服器只會針對其實 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的自訂控制項，產生物件層級事件。 如需詳細資訊，請參閱 [自訂消費者介面元素](custom-user-interface-elements.md)。

 

 




