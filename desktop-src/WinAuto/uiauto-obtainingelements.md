---
title: 取得 UI 自動化項目
description: 本主題說明為 UI 元素取得 IUIAutomationElement 介面的各種方式。
ms.assetid: 8675851a-4a72-4cbe-ab71-ed6fc891be17
keywords:
- 用戶端，取得消費者介面自動化元素
- 用戶端，消費者介面自動化元素
- 用戶端、根項目
- 用戶端、搜尋範圍
- 消費者介面自動化，取得元素
- 消費者介面自動化，元素
- 消費者介面自動化，根項目
- 消費者介面自動化，條件
- 消費者介面自動化，搜尋範圍
- 取得消費者介面自動化元素
- 根項目
- 搜尋範圍
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: f2ecf8a30f468e7a7ca4df60465993fa7acdc1e8eef1c8537d8c3d796132cb82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997738"
---
# <a name="obtaining-ui-automation-elements"></a>取得 UI 自動化項目

本主題說明為 UI 元素取得 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面的各種方式。

[消費者介面自動化檔內容用戶端範例應用程式](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/UIAutomationDocumentClient)中使用 **IUIAutomationElement** 。

## <a name="root-element"></a>根項目

雖然您可以使用方法（例如 [**IUIAutomation：： system.windows.input.focusmanager.getfocusedelement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)）直接抓取元素，但有些用戶端應用程式需要視圖專案的階層式結構，又稱為消費者介面自動化樹狀結構。 此階層的根項目是桌面。 您可以使用 [**IUIAutomation：： GetRootElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getrootelement) 方法或 [**IUIAutomation：： GetRootElementBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getrootelementbuildcache) 方法來取得這個元素。 這兩種方法都會捕獲 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面指標。 您可以使用方法（例如 [**IUIAutomationElement：： FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) 和 [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)）來搜尋子代元素。

> [!Note]  
> 一般來說，您應該嘗試只取得根項目的直接子系。 搜尋子代可能會逐一查看數百個或數千個元素。 如果您嘗試取得較低層級的特定項目，您應該從應用程式視窗或較低層級的容器開始搜尋。

 

## <a name="conditions"></a>條件

針對用來抓取消費者介面自動化元素的大部分技術，您必須指定條件。 條件是定義您想要取得之專案的一組準則。 條件是以 [**IUIAutomationCondition**](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition) 介面表示。

最簡單的條件是 true 條件，這是預先定義的物件，指定要傳回搜尋範圍中的所有元素。 False 條件是 true 條件的反向條件，因為它會導致找不到任何專案，所以不太實用。 您可以使用 [**IUIAutomation：： CreateTrueCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createtruecondition)來取得 true 條件的介面。

另外還有三個預先定義的條件（可做為 [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) 物件上的屬性），可以單獨使用，也可以與其他條件搭配使用： [**IUIAutomation：： ContentViewCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewcondition)、 [**ControlViewCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewcondition)和 [**RawViewCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewcondition)。 **RawViewCondition**（本身使用）相當於 true 條件，因為它不會依 [**IUIAutomationElement：： CurrentIsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) 或 [**CurrentIsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) 屬性來篩選元素。

其他條件是由條件物件所建立，每個條件物件都會指定屬性值。 例如，屬性條件可能會指定專案已啟用或支援特定的控制項模式。

您可以藉由呼叫 [**IUIAutomation：： CreateAndCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createandcondition)、 [**CreateOrCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createorcondition)、 [**CreateNotCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createnotcondition)和相關方法來結合使用布林值邏輯的條件。

## <a name="search-scope"></a>搜尋範圍

使用 [**IUIAutomationElement：： FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) 或 [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) 執行的搜尋必須具有範圍和開始位置。

> [!Note]  
> 這兩種方法的任何評論也適用于 [**IUIAutomationElement：： FindFirstBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache) 和 [**FindAllBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findallbuildcache)。

 

範圍會定義要搜尋的起始位置周圍的空間。 這可能包括元素本身、其同級、其父系、直屬子系和其子系。 請注意， **Find** 方法不支援搜尋 Microsoft 消費者介面自動化樹狀結構;也就是說，不支援搜尋上階元素。

搜尋範圍是由 [**treescope.children**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope) 列舉型別中值的位元組合所定義。

## <a name="finding-a-known-element"></a>尋找已知的項目

若要找出以名稱、自動化識別碼或其他屬性或屬性組合識別的已知專案，最簡單的方式是使用 [**IUIAutomationElement：： FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) 方法。 如果搜尋的專案是應用程式視窗，則搜尋的起始點可以是根項目。

這種尋找消費者介面自動化元素的方式最適合用於自動化測試案例。

如需示範如何尋找已知專案的程式碼範例，請參閱 [依名稱尋找元素](uiauto-howto-find-ui-elements.md)。

## <a name="finding-elements-in-a-subtree"></a>在子樹狀結構中尋找項目

若要尋找符合特定準則且與已知專案相關的所有元素，您可以在已知元素上呼叫 [**IUIAutomationElement：： FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) 。 例如，您可以使用這個方法，從清單或功能表中取出清單專案或功能表項目，或是識別對話方塊中的所有控制項。

如需示範如何在子樹中尋找專案的程式碼範例，請參閱 [尋找相關元素](uiauto-howto-find-ui-elements.md)。

## <a name="walking-a-subtree"></a>逐一查看子樹狀結構

如果您事先不知道用戶端可能使用的應用程式，您可以使用 [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)來建立所有相關專案的子樹。 例如，您的用戶端可能會這麼做，以回應焦點變更事件;也就是說，當應用程式或控制項收到輸入焦點時，消費者介面自動化用戶端會檢查子系，或許是焦點元素的所有下階。

請注意，消費者介面自動化樹狀結構的流覽需要大量資源。 只有在無法使用 [**IUIAutomationElement：： FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst)、 [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)或 [**BuildUpdatedCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-buildupdatedcache) 方法時，才會將樹狀結構引導。

您可以藉由將自訂條件傳遞至 [**IUIAutomation：： CreateTreeWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createtreewalker)來定義您自己的樹狀目錄，或者，您可以使用下列其中一個定義為基底 [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)屬性的預先定義物件。



| Object                                                              | 目的                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker) | 只尋找 [**IUIAutomationElement：： CurrentIsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) 屬性為 **TRUE** 的元素。 |
| [**ControlViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewwalker) | 只尋找 [**IUIAutomationElement：： CurrentIsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) 屬性為 **TRUE** 的元素。 |
| [**RawViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewwalker)         | 尋找所有項目。                                                                                                                                          |



 

取得 [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)之後，請呼叫 **IUIAutomationTreeWalker：： GetXxx** 方法來流覽子樹元素，並傳入要開始進行的專案。

[**IUIAutomationTreeWalker：：**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtreewalker-normalizeelement)正規化方法可以用來從另一個不是 view 一部分的專案導覽至子樹中的元素。 例如，假設您使用 [**IUIAutomation：： ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker)建立子樹的視圖。 您的應用程式會收到捲軸已收到輸入焦點的通知。 因為捲軸不是內容項目，所以不會出現在子樹狀結構檢視中。 不過，您可以將代表捲軸的 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 傳遞至 **IUIAutomationTreeWalker：：** 正規化，並取出內容視圖中最接近的上階。

如需示範如何使用 [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) 介面的程式碼範例，請參閱 [如何逐步執行消費者介面自動化樹狀結構](uiauto-howto-walk-uiautomation-tree.md)。

## <a name="other-ways-to-retrieve-an-element"></a>擷取項目的其他方式

除了搜尋和流覽之外，您還可以透過下列方式取得 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 。

### <a name="from-an-event"></a>從事件擷取

當您的應用程式收到消費者介面自動化事件時，傳遞至事件處理常式的來源物件會以 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement)表示。 例如，如果您訂閱焦點變更事件，傳遞給您 [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) 的來源就是接收焦點的元素。 如需詳細資訊，請參閱 [訂閱消費者介面自動化事件](uiauto-eventsforclients.md)。

### <a name="from-a-point"></a>從點擷取

若要從螢幕座標中取出 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) （例如，資料指標位置），請使用 [**IUIAutomation：： ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint) 方法。

### <a name="from-a-window-handle"></a>從視窗控制代碼擷取

若要從 **HWND** 取出 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) ，請使用 [**IUIAutomation：： ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle)方法。

### <a name="from-the-focused-control"></a>從取得焦點的控制項擷取

若要取出表示焦點控制項的 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) ，請使用 [**IUIAutomation：： system.windows.input.focusmanager.getfocusedelement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement) 方法。

## <a name="related-topics"></a>相關主題

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)

[消費者介面自動化檔內容用戶端範例應用程式](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/UIAutomationDocumentClient)
