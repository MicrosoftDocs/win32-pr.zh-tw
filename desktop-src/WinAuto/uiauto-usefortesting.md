---
title: 使用 UI 自動化進行自動化測試
description: 本總覽說明 Microsoft 消費者介面自動化如何作為在自動化測試案例中以程式設計方式存取的架構。
ms.assetid: 192162f9-55bf-4111-9f15-c0d3b5af2ab7
keywords:
- 用戶端，消費者介面自動化自動化測試
- 用戶端，自動化測試
- 用戶端，測試
- 用戶端，自動化測試控管
- 適用于自動化測試的用戶端、消費者介面自動化工具
- 用戶端，消費者介面自動化測試
- 消費者介面自動化，自動化測試
- 消費者介面自動化，測試
- 消費者介面自動化，自動化測試的工具
- 自動化的測試
- 自動化測試的工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8055a024c31df615125f2b8b64251a7b3c6eafb6f271c1890e1f49264350c10c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861198"
---
# <a name="using-ui-automation-for-automated-testing"></a>使用 UI 自動化進行自動化測試

本總覽說明 Microsoft 消費者介面自動化如何作為在自動化測試案例中以程式設計方式存取的架構。

消費者介面自動化提供統一的物件模型，可讓所有 UI 架構以可存取且輕鬆的自動化方式公開複雜且豐富的功能。

消費者介面自動化是以 Microsoft Active Accessibility 的後續發展而成，這是一種架構，旨在提供可供存取控制項和應用程式的解決方案。 Microsoft Active Accessibility 不是以測試自動化為考慮而設計，雖然它會因為存取範圍和自動化的類似需求而演進至該角色。 消費者介面自動化的設計目的是為了提供適用于自動化測試的強大功能，以及提供更精確的協助工具解決方案。 例如，Microsoft Active Accessibility 依賴單一介面來公開 UI 的相關資訊，並收集輔助技術產品所需的資訊;消費者介面自動化分隔兩個模型。

提供者和用戶端都必須執行消費者介面自動化，才能做為自動化測試控管。 消費者介面自動化提供者是應用程式，例如 Microsoft Word、Microsoft Excel，以及以 Windows 作業系統為基礎的其他協力廠商應用程式或控制項。 使用者介面自動化用戶端則包括自動化測試指令碼和輔助技術應用程式。

本主題包含下列各節。

-   [提供者中的消費者介面自動化](#ui-automation-in-providers)
-   [用戶端中的消費者介面自動化](#ui-automation-in-clients)
    -   [以程式設計方式存取](#programmatic-access)
-   [測試自動化的主要屬性](#key-properties-for-test-automation)
-   [相關工具和技術](#related-tools-and-technologies)
-   [相關主題](#related-topics)

## <a name="ui-automation-in-providers"></a>提供者中的消費者介面自動化

若要將使用者介面的元素自動化，開發人員必須查看終端使用者可以使用標準鍵盤和滑鼠互動來執行 UI 物件的動作。 識別出這些按鍵動作之後，就應該在控制項上執行鏡像功能和 UI 元素行為的消費者介面自動化控制項模式。 例如，使用者與下拉式方塊控制項的互動通常牽涉到展開和折迭下拉式方塊，以顯示或隱藏專案清單、從清單中選取專案，或透過鍵盤輸入加入新值。

藉由其他協助工具模式，開發人員必須直接從個別按鈕、功能或其他控制項收集資訊。 每個控制項類型都有數十個次要變化。 換句話說，即使按鈕的10個變化運作方式相同，且執行相同的函式，它們都必須視為唯一的控制項。 無法得知這些控制項是否功能對等。 已開發消費者介面自動化控制項模式來代表這些常見的控制項行為。 如需詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。

如果沒有消費者介面自動化所提供之控制項模式的統一模型，測試控管和開發人員就必須有架構特定的資訊，才能在該架構中公開屬性和控制行為。 因為有數個不同的 UI 架構可同時存在於 Windows 作業系統中，包括 Microsoft Win32、Windows Forms 和 Windows Presentation Foundation (WPF) ，所以使用看似類似的控制項測試多個應用程式可能會是個很困難的工作。 例如，下表列出取出與按鈕控制項相關聯之名稱或文字所需的架構特定屬性名稱，並顯示對等的消費者介面自動化屬性。



| 控制項類型 | UI 架構 | 架構特定屬性 | 消費者介面自動化屬性 |
|--------------|--------------|-----------------------------|------------------------|
| Button       | WPF          | Content                     | Name 屬性          |
| Button       | Win32        | 標題                     | Name 屬性          |
| 映像        | HTML         | alt                         | Name 屬性          |



 

消費者介面自動化提供者負責將其控制項的架構特定屬性對應至相等的消費者介面自動化屬性。 如需有關在提供者中執行消費者介面自動化的詳細資訊，請參閱 [消費者介面自動化提供者程式設計人員手冊](uiauto-providerportal.md)。 如需有關如何執行控制項模式的詳細資訊，請參閱實 [消費者介面自動化控制項模式](uiauto-implementinguiautocontrolpatterns.md)。

## <a name="ui-automation-in-clients"></a>用戶端中的消費者介面自動化

自動化測試控管和案例的目標是可一致且可重複操作的 UI。 例如，這可能牽涉到單元測試特定控制項，以及記錄和執行測試腳本，以逐一查看一組控制項上的一連串泛型動作。

自動化應用程式的複雜之處是，將測試與動態目標同步處理的困難，例如，顯示目前正在執行之應用程式清單的清單方塊控制項，例如 Windows 工作管理員。 因為清單方塊中的專案會在測試應用程式的控制項之外動態更新，所以嘗試在清單方塊中重複選取特定專案時，不可能發生任何一致性。 當您嘗試在測試應用程式的控制項以外的 UI 中重複簡單的焦點變更時，可能會發生類似的問題。

### <a name="programmatic-access"></a>程式設計存取

程式設計存取能夠透過程式碼，模擬由傳統滑鼠和鍵盤輸入所公開的任何互動和體驗。 消費者介面自動化可透過五個元件進行程式設計存取：

-   消費者介面自動化樹狀結構有助於流覽 UI 的結構。 樹狀結構是從 **HWND** 的集合所建立。 如需詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。
-   Automation 元素是 UI 中的個別元件。 這些通常可以比 **HWND** 更細微。
-   Automation 屬性提供有關 UI 元素的特定資訊。 如需詳細資訊，請參閱 [UI Automation Properties Overview](uiauto-propertiesoverview.md)。
-   控制項模式定義控制項功能的特定層面，可以包含屬性、方法、事件和結構資訊。 如需詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。
-   自動化事件會提供事件通知和資訊。 如需詳細資訊，請參閱 [UI Automation Events Overview](uiauto-eventsoverview.md)。

## <a name="key-properties-for-test-automation"></a>測試自動化的主要屬性

在 UI 中唯一識別並接著找到任何控制項的功能，可提供自動化測試應用程式在該 UI 上操作的基礎。 下表說明用戶端和提供者用來識別及尋找控制項的消費者介面自動化屬性。



| 屬性     | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AutomationId | 可唯一區分 automation 元素與其同級。 不需要支援 AutomationId 屬性。 如果有的話，在應用程式的任何實例中，專案的 AutomationId 屬性都會相同，無論當地語言為何。 雖然 AutomationId 屬性在同一個同級元素之間是唯一的，但在整個桌面中可能不是唯一的。 例如，應用程式的多個實例或 Microsoft Windows 檔案總管中的多個資料夾檢視可能包含具有相同 AutomationIdProperty 的元素，例如 "SystemMenuBar"。 用戶端不應該針對其他應用程式所公開的 AutomationIds 做出任何假設。 AutomationId 不保證會在應用程式的不同版本或組建之間保持穩定。 |
| ControlType  | 識別自動化項目所代表的控制項類型。 重要的資訊可以從對控制項類型的了解加以推斷。 如需詳細資訊，請參閱 [UI Automation Control Types Overview](uiauto-controltypesoverview.md)。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 名稱         | 識別或解釋 automation 元素目的的文字字串。 它應該謹慎使用，因為它可以當地語系化。 名稱屬性不是在同級之間的唯一識別碼。 針對測試自動化，用戶端應該改用 AutomationId 屬性或 RuntimeId 屬性。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| RuntimeId    | 整數的陣列，表示 automation 元素的識別碼。 識別碼在桌面上是唯一的，但保證只有產生它的桌面 UI 才是唯一的。 您可以在一段時間內重複使用識別碼。 使用 [**IUIAutomation：： CompareElements**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-compareelements) 來判斷目前具有特定執行時間識別碼的元素是否為先前具有該識別碼的相同元素。 此外，RuntimeId 屬性的格式可能會變更。 它應該被視為不透明的值，而且只用于比較。例如，判斷 automation 元素是否在快取中。                                                                                                                       |



 

## <a name="related-tools-and-technologies"></a>相關工具和技術

[檢查](inspect-objects.md) (Inspect.exe) 是一種以 Windows 為基礎的工具，可用來收集提供者和用戶端開發和偵錯工具的消費者介面自動化資訊。 檢查包含在 Windows 軟體開發套件 (SDK) 中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[消費者介面自動化安全性考慮](uiauto-securityoverview.md)
</dt> </dl>

 

 




