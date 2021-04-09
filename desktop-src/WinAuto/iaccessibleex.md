---
title: IAccessibleEx 介面
description: 沒有 Microsoft 消費者介面自動化提供者，但會執行 IAccessible 的控制項，可以輕鬆地升級，藉由實 IAccessibleEx 介面來提供一些消費者介面自動化功能。
ms.assetid: 5523156e-c9b8-4aad-b568-f3b3c402d33e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a74e7d464acf18244d91bc69199a56004b20beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092297"
---
# <a name="the-iaccessibleex-interface"></a>IAccessibleEx 介面

沒有 Microsoft 消費者介面自動化提供者，但會執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)的控制項，可以輕鬆地升級，藉由實 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 介面來提供一些消費者介面自動化功能。 這個介面可讓控制項公開消費者介面自動化屬性和控制項模式，而不需要完整地執行消費者介面自動化提供者介面（例如 [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment)）。 若要使用 **IAccessibleEx**、 **IRawElementProviderFragment** 和其他消費者介面自動化介面，請在原始程式碼中包含 UIAutomation .h 標頭檔。

例如，假設有一個具有範圍值的自訂控制項。 控制項的 Microsoft Active Accessibility 伺服器會定義控制項的角色，而且能夠傳回其目前的值。 不過，因為 Microsoft Active Accessibility 不會定義最小和最大屬性，所以伺服器缺少傳回控制項最小值和最大值的方法。 消費者介面自動化的用戶端能夠取得控制項的角色、目前的值和其他 Microsoft Active Accessibility 屬性，因為消費者介面自動化 core 可以透過 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)取得這些屬性。 但是，若沒有物件的 [**system.windows.automation.provider.irangevalueprovider>**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) 介面存取權，消費者介面自動化也無法取得最大值和最小值。

控制項開發人員可以為控制項提供完整的消費者介面自動化提供者，但這表示複製了許多現有的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 執行功能：例如，導覽和通用屬性。 相反地，開發人員可以繼續依賴 **IAccessible** 來提供此功能，同時透過 [**system.windows.automation.provider.irangevalueprovider>**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)新增對控制項特定屬性的支援。

## <a name="in-this-section"></a>本節內容

-   [IAccessibleEx 實施指導方針](iaccessibleex-implementation-guidelines.md)
-   [為提供者執行 IAccessibleEx](implementing-iaccessibleex-for-providers.md)
-   [從用戶端使用 IAccessibleEx](using-iaccessibleex-from-a-client.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[一般基礎結構](common-infrastructure.md)
</dt> </dl>

 

 




