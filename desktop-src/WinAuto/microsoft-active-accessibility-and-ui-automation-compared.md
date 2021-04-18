---
title: Microsoft Active Accessibility 和消費者介面自動化比較
description: 本主題提供 Microsoft Active Accessibility 和消費者介面自動化之間的主要差異摘要。
ms.assetid: ba963e53-6fb8-4bc1-8883-62547f52b0e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c90c4bffd0646aea592e19adc51ca020b2c90d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965439"
---
# <a name="microsoft-active-accessibility-and-ui-automation-compared"></a>Microsoft Active Accessibility 和消費者介面自動化比較

Windows 自動化 API 是由兩種技術所組成： Microsoft Active Accessibility 和 Microsoft 消費者介面自動化。 Microsoft Active Accessibility 是舊版的協助工具技術，以 Windows 95 的平臺增益集的形式導入，而消費者介面自動化是較新且更強大的技術，可克服 Microsoft Active Accessibility 的固有限制。

本主題提供 Microsoft Active Accessibility 和消費者介面自動化之間的主要差異摘要。 它包含下列各節：

-   [基本設計原則](#basic-design-principles)
-   [屬性和控制項模式](#properties-and-control-patterns)
-   [MSAA 角色和消費者介面自動化控制項模式](#msaa-roles-and-ui-automation-control-patterns)
-   [物件模型流覽](#object-model-navigation)
-   [物件模型擴充性](#object-model-extensibility)
-   [從 MSAA 轉換](#transitioning-from-msaa)
-   [選擇 Microsoft Active Accessibility、消費者介面自動化或 IAccessibleEx](#choosing-microsoft-active-accessibility-ui-automation-or-iaccessibleex)
    -   [新的應用程式和控制項](#new-applications-and-controls)
    -   [現有的 Microsoft Active Accessibility 實現](#existing-microsoft-active-accessibility-implementations)
-   [相關主題](#related-topics)

## <a name="basic-design-principles"></a>基本設計原則

雖然 Microsoft Active Accessibility 和消費者介面自動化是兩種不同的技術，但基本的設計原則很類似。 這兩種技術的目的是要公開有關 Windows 應用程式中所使用 UI 元素的豐富資訊。 協助工具工具的開發人員可以使用這項資訊來建立軟體，讓具有視覺、聽力或動作障礙的人更容易存取在 Windows 上執行的應用程式。

Microsoft Active Accessibility 和消費者介面自動化都會將 UI 物件模型公開為以階層樹狀結構（根目錄在桌面上）。 Microsoft Active Accessibility 將個別的 UI 元素表示為 *可存取的物件*，而消費者介面自動化將它們表示為 *Automation 元素*。 兩者都是以 *用戶端* 形式來參考協助工具工具或軟體自動化程式。 不過，Microsoft Active Accessibility 指的是應用程式或控制項提供協助工具的 UI 做為 *伺服器*，而消費者介面自動化則是 *提供者*。

## <a name="properties-and-control-patterns"></a>屬性和控制項模式

Microsoft Active Accessibility 提供單一元件物件模型 (COM) 介面，以及一組固定且較小的屬性集。 消費者介面自動化提供一組更豐富的屬性，以及一組稱為 *控制項模式* 的擴充介面，以 Microsoft Active Accessibility 不能的方式操作可存取的物件。

如需詳細資訊，請參閱 [消費者介面自動化屬性總覽](uiauto-propertiesoverview.md) 和 [消費者介面自動化控制項模式總覽](uiauto-controlpatternsoverview.md)。

## <a name="msaa-roles-and-ui-automation-control-patterns"></a>MSAA 角色和消費者介面自動化控制項模式

Microsoft 在設計 Microsoft Active Accessibility 物件模型時，與 Windows 95 的發行時間大約相同。 此模型是以10年前定義的「角色」為基礎，而且您無法支援新的 UI 行為或合併兩個或多個角色。 例如，沒有文字物件模型可協助輔助技術處理複雜的 web 內容。 消費者介面自動化藉由引進可讓物件支援多個角色的控制項模式，而消費者介面自動化的 [text](uiauto-implementingtextandtextrange.md) 控制項模式提供完整的文字物件模型，來克服這些限制。

## <a name="object-model-navigation"></a>物件模型流覽

Microsoft Active Accessibility 的另一項限制包括導覽物件模型。 Microsoft Active Accessibility 將 UI 表示為可存取物件的階層架構。 用戶端會使用可從可存取物件取得的介面和方法，從一個可存取的物件流覽至另一個物件。 伺服器可以使用 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的屬性，或使用標準 [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) COM 介面，來公開可存取物件的子系。 但是，用戶端必須能夠處理任何伺服器的這兩種方法。 這種混淆表示用戶端實作者的額外工作，以及伺服器實施者的可存取物件模型。

消費者介面自動化將 UI 表示為 Automation 元素的階層式樹狀結構，並提供單一介面來導覽樹狀結構。 用戶端可以藉由範圍和篩選來自訂樹狀結構中的元素。

## <a name="object-model-extensibility"></a>物件模型擴充性

在不中斷或變更 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) COM 介面規格的情況下，無法擴充 Microsoft Active Accessibility 屬性和函式。 結果是無法透過物件模型公開新的控制項行為。它往往是靜態的。

使用消費者介面自動化時，應用程式開發人員可以在建立新的 UI 元素時引進自訂屬性、控制項模式和事件，以描述新的元素。 如需詳細資訊，請參閱 [自訂屬性、事件和控制項模式](uiauto-custompropertieseventscontrolpatterns.md)。

## <a name="transitioning-from-msaa"></a>從 MSAA 轉換

Windows Automation API 架構提供從 Microsoft Active Accessibility 伺服器轉換至消費者介面自動化提供者的支援。 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)介面可支援將特定消費者介面自動化屬性和控制項模式新增至舊版 Microsoft Active Accessibility 伺服器，而不需要重寫整個執行。 **IAccessibleEx** 介面也可讓同進程 Microsoft Active Accessibility 用戶端直接存取消費者介面自動化提供者介面，而不是透過消費者介面自動化用戶端介面。 如需詳細資訊，請參閱 [IAccessibleEx 介面](iaccessibleex.md)。

## <a name="choosing-microsoft-active-accessibility-ui-automation-or-iaccessibleex"></a>選擇 Microsoft Active Accessibility、消費者介面自動化或 IAccessibleEx

本節可協助您決定要使用哪一種 Windows 自動化 API 解決方案來實行輔助技術產品，或讓輔助技術產品可以存取您的應用程式。

### <a name="new-applications-and-controls"></a>新的應用程式和控制項

如果您正在開發新的應用程式或控制項，Microsoft 建議使用消費者介面自動化。 雖然 Microsoft Active Accessibility 可以更輕鬆地在短期內進行，但這項技術的固有限制（例如其過時的物件模型，以及無法支援新的 UI 行為或合併角色）會讓長期更困難且更昂貴。 當新的控制項引進時，這些限制會特別明顯。

消費者介面自動化物件模型比較容易使用，而且比 Microsoft Active Accessibility 更有彈性。 UI 自動化專案會反映使用者介面的演進，而開發人員可以定義自訂的消費者介面自動化控制項模式、屬性和事件。

Microsoft Active Accessibility 通常會在進程不足的用戶端執行緩慢。 為了改善效能，協助工具工具程式的開發人員通常會選擇在目標應用程式處理常式中連結和執行其程式：非常困難和具風險的方法。 對於跨進程用戶端來說，消費者介面自動化更容易執行，並提供更好的效能和可靠性。

### <a name="existing-microsoft-active-accessibility-implementations"></a>現有的 Microsoft Active Accessibility 實現

如果您要更新以 Microsoft Active Accessibility 為基礎的現有應用程式或控制項，請考慮藉由執行 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 介面來新增消費者介面自動化的支援。 首先，請確定您的應用程式或控制項符合下列需求：

-   Microsoft Active Accessibility 伺服器的可存取物件階層的基準，必須妥善地組織，而且沒有錯誤。 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 無法修正現有可存取物件階層的問題。
-   您的 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 執行必須符合 Microsoft Active Accessibility 規格和消費者介面自動化規格。 Microsoft 提供一組用來驗證這兩種規格合規性的工具。 如需詳細資訊，請參閱 [測試控管](testing-tools.md)。

如果不符合上述任一需求，請考慮以原生方式來執行消費者介面自動化。 如果有需要，您可以保留舊版 Microsoft Active Accessibility 伺服器執行，以提供回溯相容性。 從消費者介面自動化用戶端的觀點來看，消費者介面自動化提供者與可正確執行 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 的 Microsoft Active Accessibility 伺服器之間沒有任何差異。

如需詳細資訊，請參閱 [IAccessibleEx 介面](iaccessibleex.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Automation API 總覽](windows-automation-api-overview.md)
</dt> <dt>

[Microsoft Active Accessibility](microsoft-active-accessibility.md)
</dt> <dt>

[使用者介面自動化](entry-uiauto-win32.md)
</dt> <dt>

[IAccessibleEx 介面](iaccessibleex.md)
</dt> </dl>

 

 