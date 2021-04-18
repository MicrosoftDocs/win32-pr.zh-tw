---
title: 執行 Server-Side 消費者介面自動化提供者
description: 本主題說明如何針對以 c + + 撰寫的自訂控制項，執行伺服器端的 Microsoft 消費者介面自動化提供者。
ms.assetid: c3a919b2-8b8c-4dde-ad71-587f3845a9f5
keywords:
- 消費者介面自動化，伺服器端提供者的執行
- 消費者介面自動化，提供者執行
- 消費者介面自動化，執行伺服器端提供者
- 消費者介面自動化，執行提供者
- 伺服器端提供者，執行
- 伺服器端提供者，介面
- 伺服器端提供者，屬性值
- 伺服器端提供者，事件
- 伺服器端提供者，指派新的父系
- 事件、伺服器端提供者
- 介面、伺服器端提供者
- 提供者，實施
- 執行伺服器端提供者
- 實作提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7fafbb9d03a25eb2e4713330c0622c25d17f9ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965664"
---
# <a name="implement-a-server-side-ui-automation-provider"></a>執行 Server-Side 消費者介面自動化提供者

本主題說明如何針對以 c + + 撰寫的自訂控制項，執行伺服器端的 Microsoft 消費者介面自動化提供者。 它包含下列區段：

-   [提供者介面](#provider-interfaces)
-   [消費者介面自動化提供者的必要功能](#required-functionality-for-ui-automation-providers)
-   [屬性值](#property-values)
-   [來自提供者的事件](#events-from-providers)
-   [提供者導覽](#provider-navigation)
-   [指派新的父系](#assigning-a-new-parent)
-   [提供者重新置放](#provider-repositioning)
-   [中斷連接提供者](#disconnecting-providers)
-   [相關主題](#related-topics)

如需示範如何執行伺服器端提供者的程式碼範例，請參閱 [消費者介面自動化提供者的如何主題](uiauto-howto-topics-for-uiautomation-providers.md)。

## <a name="provider-interfaces"></a>提供者介面

下列元件物件模型 (COM) 介面提供自訂控制項的功能。 若要提供基本功能，每個消費者介面自動化提供者都必須至少執行 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) 介面。 [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment)和 [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)介面是選擇性的，但應該針對複雜控制項中的元素來執行，以提供額外的功能。



| 介面                                                                         | 描述                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)             | 提供視窗中裝載之控制項的基本功能，包括控制項模式和屬性的支援。                                                         |
| [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment)         | 為複雜控制項中的專案新增功能，包括在片段中導覽、設定焦點，以及傳回元素的周框。             |
| [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) | 為複雜控制項中的根項目新增功能，包括在指定的座標尋找子項目，以及設定整個控制項的焦點狀態。 |



 

> [!Note]  
> 在 managed 程式碼的消費者介面自動化 API 中，這些介面會形成繼承階層。 這不是 c + + 中的情況，其中介面是完全分開的。

 

下列介面可提供額外的功能，但實作為選擇性。



| 介面                                                                         | 描述                                                                             |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents) | 可讓提供者追蹤事件的要求。                                      |
| [**IRawElementProviderHwndOverride**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderhwndoverride) | 可在片段的消費者介面自動化樹狀結構中，重新置放以視窗為基礎的元素。 |



 

## <a name="required-functionality-for-ui-automation-providers"></a>消費者介面自動化提供者的必要功能

若要與消費者介面自動化通訊，您的控制項必須執行下表所述的主要功能區域。



| 功能                                              | 實作                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 公開提供者以消費者介面自動化。                      | 為了回應傳送至控制項視窗的 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息，會傳回執行 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)的物件。 對於片段，這必須是片段根的提供者。                                           |
| 提供屬性值。                                   | 執行 [**IRawElementProviderSimple：： GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) 來提供或覆寫值。                                                                                                                                                             |
| 讓用戶端與控制項互動。            | 執行支援每個適當控制項模式的介面，例如 [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)。 在 [**IRawElementProviderSimple：： GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider)的實中，傳回這些控制項模式提供者。 |
| 引發事件。                                              | [**IProxyProviderWinEventSink**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iproxyproviderwineventsink)的 [**UiaRaiseAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent)方法。                                                                                                                                                |
| 啟用導覽並專注于片段。              | 針對片段中的每個元素執行 [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) 。 不是片段一部分的元素不需要。                                                                                                                         |
| 讓焦點和尋找片段中的子項目。 | 執行 [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)。 不是不是片段根項目的必要專案。                                                                                                                                                          |



 

## <a name="property-values"></a>屬性值

自訂控制項的消費者介面自動化提供者必須支援消費者介面自動化和用戶端應用程式可使用的特定屬性。 針對裝載于 windows 中的元素，消費者介面自動化可以從預設視窗提供者取得一些屬性，但必須從自訂提供者取得其他屬性。

一般來說，以視窗為基礎之控制項的提供者不需要提供 **PROPERTYID** 所識別的下列屬性：

-   [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ ProcessIdPropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ ClassNamePropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ HasKeyboardFocusPropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ IsEnabledPropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ IsPasswordPropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ RuntimeIdPropertyId**](uiauto-automation-element-propids.md)

在視窗中裝載的簡單元素或片段根的 RuntimeId 屬性是從視窗取得。 不過，根底下的片段元素（例如清單方塊中的清單專案）必須提供自己的識別碼。 如需詳細資訊，請參閱 [**IRawElementProviderFragment：： GetRuntimeId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid)。

應針對 Windows Forms 控制項中裝載的提供者傳回 IsKeyboardFocusable 屬性。 在此情況下，預設視窗提供者可能無法擷取正確值。

名稱屬性通常是由主機提供者所提供。

## <a name="events-from-providers"></a>來自提供者的事件

消費者介面自動化提供者應該引發事件，以通知用戶端應用程式在 UI 狀態中的變更。 下列函數用來引發事件。



| 函式                                                                                   | 描述                                                                                                              |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**UiaRaiseAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent)                  | 引發各種事件，包括由控制項模式觸發的事件。                                                   |
| [**UiaRaiseAutomationPropertyChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationpropertychangedevent) | 當消費者介面自動化屬性變更時引發事件。                                                               |
| [**UiaRaiseStructureChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisestructurechangedevent)      | 當消費者介面自動化樹狀結構的結構變更時引發事件，例如藉由移除或新增專案。 |



 

事件的目的是要通知用戶端在 UI 中發生的情況。 無論使用者輸入或用戶端應用程式是否使用消費者介面自動化觸發變更，提供者都應該引發事件。 例如，每當叫用控制項時，只要透過直接使用者輸入或由呼叫 [**IUIAutomationInvokePattern：： Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke)的用戶端應用程式叫用控制項，就應該引發 [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)所識別的事件。

若要最佳化效能，提供者可以選擇性地引發事件，或如果沒有註冊任何用戶端應用程式來接收事件，則完全不引發任何事件。 下列 API 元素用於優化。



| API 元素                                                                       | Description                                                                                                                                                       |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UiaClientsAreListening**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaclientsarelistening)           | 此函式會 ascertains 是否有任何用戶端應用程式已訂閱消費者介面自動化事件。                                                                 |
| [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents) | 在片段根上執行此介面可讓您在用戶端針對片段上的事件註冊和取消註冊事件處理常式時，建議提供者。 |



 

> [!Note]  
> 類似于在 COM 程式設計中執行參考計數，消費者介面自動化提供者必須將 [**IRawElementProviderAdviseEvents：： AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded)和 [**AdviseEventRemoved**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventremoved)方法（例如 [**Iunknown：： AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref)和 [**iunknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面的 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)方法）視為必要。 只要針對特定事件或屬性呼叫 **AdviseEventAdded** 的次數超過 **AdviseEventRemoved** ，提供者就應該繼續引發對應的事件，因為某些用戶端仍在接聽。 或者，消費者介面自動化提供者可以使用 [**UiaClientsAreListening**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaclientsarelistening) 函式來判斷是否至少有一個用戶端正在接聽，如果有的話，則會引發所有適當的事件。

 

## <a name="provider-navigation"></a>提供者導覽

簡單控制項的提供者（例如視窗中裝載的自訂按鈕）不需要支援消費者介面自動化樹狀結構中的導覽。 專案的導覽會由主視窗的預設提供者（在 [**IRawElementProviderSimple：： HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider)的執行中指定）來處理。 不過，當您實作複雜自訂控制項的提供者時，您必須支援片段的根節點與子系之間的導覽，以及同層級節點之間的導覽。

> [!Note]  
> 根以外的片段專案必須從 [**HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider)傳回 **Null** ，因為它們不會直接裝載在視窗中，而且沒有預設提供者可支援它們的導覽。

 

片段的結構取決於您的 [**IRawElementProviderFragment：：導覽**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate)的執行。 對於每個片段的可能方向，此方法會傳回該方向中項目的提供者物件。 如果該方向沒有任何元素，則方法會傳回 **Null**。

片段根僅支援導覽至子項目。 例如，當方向為 [ **NavigateDirection \_ FirstChild**] 時，清單方塊會傳回清單中的第一個專案，而當方向為 [ **NavigateDirection \_ LastChild**] 時，會傳回最後一個專案。 片段根目錄不支援導覽至父系或同級;這是由主機視窗提供者處理。

不是根的片段項目必須支援導覽至父代，以及導覽至任何同層級和其具有的子系。

## <a name="assigning-a-new-parent"></a>指派新的父系

快顯視窗實際上是最上層視窗，預設會顯示在消費者介面自動化樹狀結構中，做為桌面的子系。 不過，在許多情況下，快顯視窗在邏輯上是一些其他控制項的子系。 例如，下拉式方塊的下拉式清單在邏輯上是下拉式方塊的子系。 同樣地，功能表快顯視窗在邏輯上是功能表的子系。 消費者介面自動化支援將新的父系指派給快顯視窗，使其看起來像是相關聯控制項的子系。

若要將新的父系指派給快顯視窗：

1.  建立快顯視窗的提供者。 這需要事先知道快顯視窗的類別。
2.  像往常一樣，對該快顯視窗執行所有的屬性和控制項模式，就好像它本身就是控制項一樣。
3.  執行 [**IRawElementProviderSimple：： HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider) 屬性，讓它傳回從 [**UiaHostProviderFromHwnd**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahostproviderfromhwnd)取得的值，其中參數是快顯視窗的視窗控制碼。
4.  針對快顯視窗和其父代執行 [**IRawElementProviderFragment：：導覽**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) ，以便將導覽正確地處理到邏輯子系和同級子系之間。

當消費者介面自動化遇到快顯視窗時，它會辨識出從預設覆寫的導覽，並在遇到做為桌面的子系時，略過快顯視窗。 相反地，節點只能透過片段連接。

指派新的父系不適合控制項可以裝載任何類別之視窗的情況。 例如，Rebar 控制項可以在其區段中裝載任何類型的視窗。 為了處理這些情況，消費者介面自動化支援替代形式的視窗重新配置，如下一節所述。

## <a name="provider-repositioning"></a>提供者重新置放

消費者介面自動化片段可能包含兩個或多個元素，且每個專案都包含在視窗中。 由於每個視窗都有自己的預設提供者，它會將視窗視為包含視窗的子系，因此預設的消費者介面自動化樹狀結構會將視窗顯示為父視窗的子系。 在大部分情況下，這是理想的行為，但有時可能會導致混淆，因為它不符合 UI 的邏輯結構。

rebar 控制項就是這種情況的好範例。 Rebar 控制項包含群組，其中每一個都可以接著包含視窗控制項，例如工具列、編輯方塊或下拉式方塊。 Rebar 視窗的預設視窗提供者會將頻控制項視窗視為子系，而 Rebar 提供者則會將群組視為子系。 由於視窗提供者和 Rebar 提供者是以串聯方式運作，並結合其子系，因此，群組和視窗控制項都會顯示為 Rebar 控制項的子系。 不過，在邏輯上，只有波段會顯示為 Rebar 控制項的子系，而且每個波段提供者都應該與它所包含之控制項的預設視窗提供者結合。

為了達成此目的，Rebar 控制項的片段根提供者會公開一組代表群組的子系。 每個波段都有一個可公開屬性和控制項模式的單一提供者。 在 [**IRawElementProviderSimple：： HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider)的實值中，區提供者會傳回控制項視窗的預設視窗提供者，它會藉由呼叫 [**UiaHostProviderFromHwnd**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahostproviderfromhwnd)來取得它，並將控制項的視窗控制碼傳入 (**HWND**) 。 最後，Rebar 的片段根提供者會實 [**IRawElementProviderHwndOverride**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderhwndoverride) 介面，而且在其 [**IRawElementProviderHwndOverride：： GetOverrideProviderForHwnd**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderhwndoverride-getoverrideproviderforhwnd)的實中，它會針對指定之視窗中包含的控制項傳回適當的區提供者。

## <a name="disconnecting-providers"></a>中斷連接提供者

應用程式通常會在需要時建立控制項，並在之後加以終結。 終結控制項之後，應呼叫 [**UiaDisconnectProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectprovider)來釋放與控制項相關聯的消費者介面自動化提供者資源。

同樣地，應用程式應該使用 [**UiaDisconnectAllProviders**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectallproviders) 函式來釋出應用程式中所有提供者所持有的所有消費者介面自動化資源，然後再關閉。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[消費者介面自動化提供者程式設計人員指南](uiauto-providerportal.md)
</dt> </dl>

 

 