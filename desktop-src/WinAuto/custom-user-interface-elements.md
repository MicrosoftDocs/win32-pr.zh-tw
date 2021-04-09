---
title: 自訂消費者介面元素
description: 伺服器開發人員會根據應用程式的 UI 來設計可存取的物件。
ms.assetid: d9453fb0-9b4a-4103-81e3-1255091255a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b32a086b977a1737a17206261aaaa94faa754d93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839532"
---
# <a name="custom-user-interface-elements"></a>自訂消費者介面元素

伺服器開發人員會根據應用程式的 UI 來設計可存取的物件。 由於 [Active Accessibility 代表系統提供的使用者介面](appendix-a--supported-user-interface-elements-reference.md) 專案（例如清單方塊、功能表和列數控制項）來執行 IAccessible 介面，因此您只需要針對下列種類的自訂 UI 元素來執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面：

-   藉由註冊應用程式定義的視窗類別所建立的自訂控制項
-   直接在螢幕上繪製沒有相關 **HWND** 的自訂控制項
-   自訂控制項，例如 Microsoft ActiveX 和 JAVA 控制項
-   應用程式用戶端視窗中尚未公開的控制項或物件

只要您遵循用 [來公開自訂消費者介面元素的快捷方式](shortcuts-for-exposing-custom-user-interface-elements.md)中所討論的指導方針，就可以存取主控描繪控制項和功能表。 如果您遵循這些指導方針，就不需要針對主控描繪的控制項和功能表，執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面。

在大部分的情況下，可以存取 superclass 和子類別化控制項，因為系統會處理控制項的基本功能。 但是，如果 superclass 或子類別控制項大幅修改系統提供之控制項的行為，則您必須執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面。 如需詳細資訊，請參閱 [根據系統控制項公開控制項](exposing-controls-based-on-system-controls.md)。

如果應用程式只使用系統提供的使用者介面元素，則不需要執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)，除了其用戶端視窗以外。 例如，包含文字編輯器（不是使用編輯控制項來執行）的應用程式，會將文字行公開為可存取的物件。 請注意，Microsoft Active Accessibility 會自動將 [編輯] 和 [rich edit] 控制項中的文字公開為控制項之 [ [**值**](value-property.md) ] 屬性中的單一文字字串。

 

 




