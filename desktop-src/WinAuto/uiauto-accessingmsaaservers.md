---
title: 存取 Microsoft Active Accessibility 伺服器
description: 消費者介面自動化 Proxy 的 Microsoft Active Accessibility 是一種軟體元件，可讓 Microsoft 消費者介面自動化用戶端與原生執行 IAccessible 介面的 Microsoft Active Accessibility 伺服器互動。
ms.assetid: 44690b16-4a9d-4e8b-865a-b428ad616b1e
keywords:
- 消費者介面自動化，存取 Active Accessibility
- 消費者介面自動化，Active Accessibility
- 消費者介面自動化 Proxy
- 消費者介面自動化，消費者介面自動化 Proxy
- LegacyIAccessible 控制項模式
- 消費者介面自動化，LegacyIAccessible 控制項模式
- Microsoft Active Accessibility
- Active Accessibility
- 用戶端，存取 Active Accessibility 伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97319028203351cd9f45b39d133fa38727d6861e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021147"
---
# <a name="accessing-microsoft-active-accessibility-servers"></a>存取 Microsoft Active Accessibility 伺服器

消費者介面自動化 Proxy 的 Microsoft Active Accessibility 是一種軟體元件，可讓 Microsoft 消費者介面自動化用戶端與原生執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的 Microsoft Active Accessibility 伺服器互動。 Proxy 支援 [LegacyIAccessible](uiauto-implementinglegacyiaccessible.md) 控制項模式，並為每個偵測到的 Microsoft Active Accessibility 伺服器提供 [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) 介面的實例。 消費者介面自動化用戶端會使用 **IUIAutomationLegacyIAccessiblePattern** 所公開的方法來存取伺服器所支援的 Microsoft Active Accessibility 屬性和物件。

如果消費者介面自動化專案具有基礎 Microsoft Active Accessibility 執行，則用戶端可以藉由將 [**UIA \_ LegacyIAccessiblePatternId**](uiauto-controlpattern-ids.md)控制項模式識別碼傳遞至下列其中一個 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement)方法，來取得元素的 [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern)介面指標：

-   [**GetCachedPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern)
-   [**GetCachedPatternAs**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpatternas)
-   [**GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern)
-   [**GetCurrentPatternAs**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas)

[**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern)介面無法針對以消費者介面自動化為基礎的控制項使用。

[**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern)介面可讓消費者介面自動化用戶端存取 Microsoft Active Accessibility 專案的基礎 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)執行。 不過，介面並不支援消費者介面自動化功能所淘汰或多餘的方法。 例如， **IUIAutomationLegacyIAccessiblePattern** 沒有相當於 [**IAccessible：： accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) 的方法，因為 UI 元素的目前位置可從消費者介面自動化 BoundingRectangle 屬性取得。

[**IUIAutomationLegacyIAccessiblePattern：： GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible)方法可讓用戶端從消費者介面自動化元素取出 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面指標。 您也可以使用 [**IUIAutomation：： ElementFromIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessible) 和 [**IUIAutomation：： ElementFromIAccessibleBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessiblebuildcache) 方法來反轉反向。

如果元素的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面是由 OLEACC.dll 的 proxy 物件或從消費者介面自動化到 Microsoft Active Accessibility 橋接器的 proxy 物件提供，則 [**IUIAutomationLegacyIAccessiblePattern：： GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible)會傳回 **Null** 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[消費者介面自動化和 Active Accessibility](uiauto-msaa.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




