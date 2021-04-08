---
title: LegacyIAccessible 控制項模式
description: 描述使用 ILegacyIAccessibleProvider 的方針和慣例，包括屬性、方法和事件的相關資訊。
ms.assetid: 4d66b9b8-ddbe-4bbc-b475-72dad1fe9393
keywords:
- 消費者介面自動化，執行 LegacyIAccessible 控制項模式
- 消費者介面自動化，LegacyIAccessible 控制項模式
- 消費者介面自動化、ILegacyIAccessibleProvider
- ILegacyIAccessibleProvider
- 執行消費者介面自動化 LegacyIAccessible 控制項模式
- LegacyIAccessible 控制項模式
- 控制項模式，ILegacyIAccessibleProvider
- 控制模式，消費者介面自動化執行 LegacyIAccessible
- 控制項模式，LegacyIAccessible
- 介面，ILegacyIAccessibleProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cffbd205b072f6f900ea5b5eb5a9f6ddfb5ddc5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674316"
---
# <a name="legacyiaccessible-control-pattern"></a>LegacyIAccessible 控制項模式

描述使用 [**ILegacyIAccessibleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider)的方針和慣例，包括屬性、方法和事件的相關資訊。 Microsoft 消費者介面自動化 Proxy 的 Microsoft Active Accessibility 支援 **LegacyIAccessible** 控制項模式。

應用程式和控制項提供者絕不會執行 [**ILegacyIAccessibleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider) 介面。

**LegacyIAccessible** 控制項模式會公開 [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern)介面給消費者介面自動化用戶端，讓他們能夠存取特定 UI 元素的基礎 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)實作為基礎。 但是， **IUIAutomationLegacyIAccessiblePattern** 不支援已過時的方法，或與消費者介面自動化功能重複的方法。

本主題包含下列幾節：

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [**LegacyIAccessible** 控制項模式的成員](#members-of-the-legacyiaccessible-control-pattern)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

沒有任何應用程式或控制項會執行 [**ILegacyIAccessibleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider)。 消費者介面自動化架構會自動提供原生 Microsoft Active Accessibility 伺服器的提供者執行。

**LegacyIAccessible** 控制項模式不適用於以消費者介面自動化為基礎的控制項。

## <a name="members-of-the-legacyiaccessible-control-pattern"></a>**LegacyIAccessible** 控制項模式的成員

下列屬性、方法和事件是 **LegacyIAccessible** 控制項模式的成員。 附注適用于消費者介面自動化用戶端。



| 成員                                                                        | 成員類型 | 備註                                                                                                                                |
|--------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**ChildId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_childid)                   | 屬性    | 傳回非子物件的 **CHILDID \_ SELF** (0) 。                                                                                |
| [**DefaultAction**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_defaultaction)       | 屬性    | 無                                                                                                                                 |
| [**描述**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_description)           | 屬性    | 無                                                                                                                                 |
| [**説明**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_help)                         | 屬性    | 無                                                                                                                                 |
| [**KeyboardShortcut**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_keyboardshortcut) | 屬性    | 無                                                                                                                                 |
| [**Name**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_name)                         | 屬性    | 無                                                                                                                                 |
| [**角色**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_role)                         | 屬性    | 使用 [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) 函式來取出當地語系化的字串。                                                    |
| [**GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-getselection)         | 方法      | 捕獲 [**IUIAutomationElementArray**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray) 介面指標。                                |
| [**State**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_state)                       | 屬性    | 使用 [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) 函式來取出當地語系化的字串。                                                  |
| [**值**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_value)                       | 屬性    | 無                                                                                                                                 |
| [**DoDefaultAction**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-dodefaultaction)   | 方法      | 無                                                                                                                                 |
| [**GetIAccessible**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-getiaccessible)     | 方法      | 無                                                                                                                                 |
| [**選擇**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-select)                     | 方法      | 選取旗標是 Microsoft Active Accessibility 的 **SELFLAG** 值。 如需詳細資訊，請參閱 [SELFLAG 常數](selflag.md)。 |
| [**SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-setvalue)                 | 方法      | 無                                                                                                                                 |



 

此控制項模式沒有任何相關聯的事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> </dl>

 

 




