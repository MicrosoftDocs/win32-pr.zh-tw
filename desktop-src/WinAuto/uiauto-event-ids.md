---
title: '事件識別碼 (Uiautomationclient.dll .h) '
description: 本主題說明用來識別 Microsoft 消費者介面自動化事件的已命名常數。
ms.assetid: 4baf5cb9-c965-4977-ae2b-420e84dc2e94
topic_type:
- apiref
api_name:
- UIA_AsyncContentLoadedEventId
- UIA_AutomationFocusChangedEventId
- UIA_AutomationPropertyChangedEventId
- UIA_ActiveTextPositionChangedEventId
- UIA_ChangesEventId
- UIA_Drag_DragCancelEventId
- UIA_Drag_DragCompleteEventId
- UIA_Drag_DragStartEventId
- UIA_DropTarget_DragEnterEventId
- UIA_DropTarget_DragLeaveEventId
- UIA_DropTarget_DroppedEventId
- UIA_HostedFragmentRootsInvalidatedEventId
- UIA_InputDiscardedEventId
- UIA_InputReachedOtherElementEventId
- UIA_InputReachedTargetEventId
- UIA_Invoke_InvokedEventId
- UIA_LayoutInvalidatedEventId
- UIA_LiveRegionChangedEventId
- UIA_MenuClosedEventId
- UIA_MenuModeEndEventId
- UIA_MenuModeStartEventId
- UIA_MenuOpenedEventId
- UIA_NotificationEventId
- UIA_Selection_InvalidatedEventId
- UIA_SelectionItem_ElementAddedToSelectionEventId
- UIA_SelectionItem_ElementRemovedFromSelectionEventId
- UIA_SelectionItem_ElementSelectedEventId
- UIA_StructureChangedEventId
- UIA_SystemAlertEventId
- UIA_Text_TextChangedEventId
- UIA_Text_TextSelectionChangedEventId
- UIA_TextEdit_ConversionTargetChangedEventId
- UIA_TextEdit_TextChangedEventId
- UIA_ToolTipClosedEventId
- UIA_ToolTipOpenedEventId
- UIA_Window_WindowClosedEventId
- UIA_Window_WindowOpenedEventId
api_location:
- UIAutomationClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5789483cf7fb8e604d1aeed16e848d2cf5d89a34eb1256ed81054e1863e8f4f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133341"
---
# <a name="event-identifiers-uiautomationclienth"></a>事件識別碼 (Uiautomationclient.dll .h) 

本主題說明用來識別 Microsoft 消費者介面自動化事件的已命名常數。



| 常數/值                                                                                                                                                                                                                                                                                                                                                                                                        | 描述                                                                                                                                                                                                                                                                                                                           |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIA_ActiveTextPositionChangedEventId"></span><span id="uia_activetextpositionchangedeventid"></span><span id="UIA_ACTIVETEXTPOSITIONCHANGEDEVENTID"></span><dl> <dt>**UIA \_ActiveTextPositionChangedEventId**</dt> <dt>20036</dt> </dl>                                                                                              | 識別活動文字位置變更時所引發的事件，此事件是在唯讀文字專案 (（例如網頁瀏覽器、PDF 檔或 EPUB) 檔）中使用書簽 (片段識別碼（參考資源) 內的位置）所表示。<br/>                                                                                                                                  |
| <span id="UIA_AsyncContentLoadedEventId"></span><span id="uia_asynccontentloadedeventid"></span><span id="UIA_ASYNCCONTENTLOADEDEVENTID"></span><dl> <dt>**UIA \_AsyncContentLoadedEventId**</dt> <dt>20006</dt> </dl>                                                                                              | 識別載入非同步內容時引發的事件。 此事件主要是由提供者用來表示已發生非同步內容載入事件。<br/>                                                                                                                                  |
| <span id="UIA_AutomationFocusChangedEventId"></span><span id="uia_automationfocuschangedeventid"></span><span id="UIA_AUTOMATIONFOCUSCHANGEDEVENTID"></span><dl> <dt>**UIA \_AutomationFocusChangedEventId**</dt> <dt>20005</dt> </dl>                                                                              | 識別焦點已從某個元素變更為另一個專案時所引發的事件。<br/>                                                                                                                                                                                                                                |
| <span id="UIA_AutomationPropertyChangedEventId"></span><span id="uia_automationpropertychangedeventid"></span><span id="UIA_AUTOMATIONPROPERTYCHANGEDEVENTID"></span><dl> <dt>**UIA \_AutomationPropertyChangedEventId**</dt> <dt>20004</dt> </dl>                                                                  | 識別屬性值變更時引發的事件。<br/>                                                                                                                                                                                                                                              |
| <span id="UIA_ChangesEventId"></span><span id="uia_changeseventid"></span><span id="UIA_CHANGESEVENTID"></span><dl> <dt>**UIA \_ChangesEventId**</dt> <dt>20034</dt> </dl>                                                                                                                                          | 識別當提供者呼叫 [**UiaRaiseChangesEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisechangesevent) 函數時引發的事件。<br/>                                                                                                                                                                                |
| <span id="UIA_Drag_DragCancelEventId"></span><span id="uia_drag_dragcanceleventid"></span><span id="UIA_DRAG_DRAGCANCELEVENTID"></span><dl> <dt>**UIA \_拖曳 \_ DragCancelEventId**</dt> <dt>20027</dt> </dl>                                                                                                         | 識別當使用者結束拖曳作業之前，在卸載目標上放置專案之前所引發的事件。 這個事件是由正在拖曳的元素所引發。 從 Windows 8 開始支援。<br/>                                                                                                                 |
| <span id="UIA_Drag_DragCompleteEventId"></span><span id="uia_drag_dragcompleteeventid"></span><span id="UIA_DRAG_DRAGCOMPLETEEVENTID"></span><dl> <dt>**UIA \_拖曳 \_ DragCompleteEventId**</dt> <dt>20028</dt> </dl>                                                                                                 | 識別當使用者卸載放置目標上的專案時所引發的事件。 這個事件是由正在拖曳的元素所引發。 從 Windows 8 開始支援。<br/>                                                                                                                                                 |
| <span id="UIA_Drag_DragStartEventId"></span><span id="uia_drag_dragstarteventid"></span><span id="UIA_DRAG_DRAGSTARTEVENTID"></span><dl> <dt>**UIA \_拖曳 \_ DragStartEventId**</dt> <dt>20026</dt> </dl>                                                                                                             | 識別當使用者開始拖曳專案時所引發的事件。 這個事件是由正在拖曳的元素所引發。 從 Windows 8 開始支援。<br/>                                                                                                                                                         |
| <span id="UIA_DropTarget_DragEnterEventId"></span><span id="uia_droptarget_dragentereventid"></span><span id="UIA_DROPTARGET_DRAGENTEREVENTID"></span><dl> <dt>**UIA \_DropTarget \_ DragEnterEventId**</dt> <dt>20029</dt> </dl>                                                                                     | 識別當使用者將專案拖曳至放置目標的界限時引發的事件。 這個事件是由 drop target 元素所引發。 從 Windows 8 開始支援。<br/>                                                                                                                                      |
| <span id="UIA_DropTarget_DragLeaveEventId"></span><span id="uia_droptarget_dragleaveeventid"></span><span id="UIA_DROPTARGET_DRAGLEAVEEVENTID"></span><dl> <dt>**UIA \_DropTarget \_ DragLeaveEventId**</dt> <dt>20030</dt> </dl>                                                                                     | 識別當使用者將專案拖曳出放置目標的界限時引發的事件。 這個事件是由 drop target 元素所引發。 從 Windows 8 開始支援。<br/>                                                                                                                                    |
| <span id="UIA_DropTarget_DroppedEventId"></span><span id="uia_droptarget_droppedeventid"></span><span id="UIA_DROPTARGET_DROPPEDEVENTID"></span><dl> <dt>**UIA \_DropTarget \_ DroppedEventId**</dt> <dt>20031</dt> </dl>                                                                                             | 識別當使用者卸載放置目標上的專案時所引發的事件。 這個事件是由 drop target 元素所引發。 從 Windows 8 開始支援。<br/>                                                                                                                                                   |
| <span id="UIA_HostedFragmentRootsInvalidatedEventId"></span><span id="uia_hostedfragmentrootsinvalidatedeventid"></span><span id="UIA_HOSTEDFRAGMENTROOTSINVALIDATEDEVENTID"></span><dl> <dt>**UIA \_HostedFragmentRootsInvalidatedEventId**</dt> <dt>20025</dt> </dl>                                              | 識別當對另一個專案中所裝載消費者介面自動化片段的根節點進行變更時，所引發的事件。 從 Windows 8 開始支援。<br/>                                                                                                                                               |
| <span id="UIA_InputDiscardedEventId"></span><span id="uia_inputdiscardedeventid"></span><span id="UIA_INPUTDISCARDEDEVENTID"></span><dl> <dt>**UIA \_InputDiscardedEventId**</dt> <dt>20022</dt> </dl>                                                                                                              | 識別當指定的輸入被捨棄或無法連線到任何專案時所引發的事件。<br/>                                                                                                                                                                                                       |
| <span id="UIA_InputReachedOtherElementEventId"></span><span id="uia_inputreachedotherelementeventid"></span><span id="UIA_INPUTREACHEDOTHERELEMENTEVENTID"></span><dl> <dt>**UIA \_InputReachedOtherElementEventId**</dt> <dt>20021</dt> </dl>                                                                      | 識別當指定的輸入到達 [**StartListening**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationsynchronizedinputpattern-startlistening) 方法所呼叫專案以外的專案時所引發的事件。<br/>                                                                                              |
| <span id="UIA_InputReachedTargetEventId"></span><span id="uia_inputreachedtargeteventid"></span><span id="UIA_INPUTREACHEDTARGETEVENTID"></span><dl> <dt>**UIA \_InputReachedTargetEventId**</dt> <dt>20020</dt> </dl>                                                                                              | 識別當指定的滑鼠或鍵盤輸入到達呼叫 [**StartListening**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationsynchronizedinputpattern-startlistening) 方法的專案時所引發的事件。<br/>                                                                                                  |
| <span id="UIA_Invoke_InvokedEventId"></span><span id="uia_invoke_invokedeventid"></span><span id="UIA_INVOKE_INVOKEDEVENTID"></span><dl> <dt>**UIA \_Invoke \_ InvokedEventId**</dt> <dt>20009</dt> </dl>                                                                                                             | 識別叫用或啟動控制項時引發的事件。<br/>                                                                                                                                                                                                                                                |
| <span id="UIA_LayoutInvalidatedEventId"></span><span id="uia_layoutinvalidatedeventid"></span><span id="UIA_LAYOUTINVALIDATEDEVENTID"></span><dl> <dt>**UIA \_LayoutInvalidatedEventId**</dt> <dt>20008</dt> </dl>                                                                                                  | 識別控制項中子專案的版面配置變更時引發的事件。 此事件也會用於 [自動建議的協助工具](/windows/uwp/design/accessibility/accessible-text-requirements)。<br/>                                                                |
| <span id="UIA_LiveRegionChangedEventId"></span><span id="uia_liveregionchangedeventid"></span><span id="UIA_LIVEREGIONCHANGEDEVENTID"></span><dl> <dt>**UIA \_LiveRegionChangedEventId**</dt> <dt>20024</dt> </dl>                                                                                                  | 識別即時區域的內容變更時引發的事件。 從 Windows 8 開始支援。<br/>                                                                                                                                                                                                      |
| <span id="UIA_MenuClosedEventId"></span><span id="uia_menuclosedeventid"></span><span id="UIA_MENUCLOSEDEVENTID"></span><dl> <dt>**UIA \_MenuClosedEventId**</dt> <dt>20007</dt> </dl>                                                                                                                              | 識別功能表關閉時引發的事件。<br/>                                                                                                                                                                                                                                                                 |
| <span id="UIA_MenuModeEndEventId"></span><span id="uia_menumodeendeventid"></span><span id="UIA_MENUMODEENDEVENTID"></span><dl> <dt>**UIA \_MenuModeEndEventId**</dt> <dt>20019</dt> </dl>                                                                                                                          | 識別在功能表模式結束時引發的事件。<br/>                                                                                                                                                                                                                                                             |
| <span id="UIA_MenuModeStartEventId"></span><span id="uia_menumodestarteventid"></span><span id="UIA_MENUMODESTARTEVENTID"></span><dl> <dt>**UIA \_MenuModeStartEventId**</dt> <dt>20018</dt> </dl>                                                                                                                  | 識別啟動功能表模式時引發的事件。<br/>                                                                                                                                                                                                                                                           |
| <span id="UIA_MenuOpenedEventId"></span><span id="uia_menuopenedeventid"></span><span id="UIA_MENUOPENEDEVENTID"></span><dl> <dt>**UIA \_MenuOpenedEventId**</dt> <dt>20003</dt> </dl>                                                                                                                              | 識別功能表開啟時引發的事件。<br/>                                                                                                                                                                                                                                                                 |
| <span id="UIA_NotificationEventId"></span><span id="uia_notificationeventid"></span><span id="UIA_NOTIFICATIONEVENTID"></span><dl> <dt>**UIA \_NotificationEventId**</dt> <dt>20035</dt> </dl>                                                                                                                      | 識別當提供者呼叫 [**UiaRaiseNotificationEvent**](https://www.bing.com/search?q=**UiaRaiseNotificationEvent**) 方法時引發的事件。<br/>                                                                                                                                                                    |
| <span id="UIA_Selection_InvalidatedEventId"></span><span id="uia_selection_invalidatedeventid"></span><span id="UIA_SELECTION_INVALIDATEDEVENTID"></span><dl> <dt>**UIA \_選取 \_ InvalidatedEventId**</dt> <dt>20013</dt> </dl>                                                                                 | 識別當容器中的選取範圍大幅變更時引發的事件。<br/>                                                                                                                                                                                                                             |
| <span id="UIA_SelectionItem_ElementAddedToSelectionEventId"></span><span id="uia_selectionitem_elementaddedtoselectioneventid"></span><span id="UIA_SELECTIONITEM_ELEMENTADDEDTOSELECTIONEVENTID"></span><dl> <dt>**UIA \_SelectionItem \_ ElementAddedToSelectionEventId**</dt> <dt>20010</dt> </dl>                 | 識別當項目加入選取的項目集合中時所引發的事件。<br/>                                                                                                                                                                                                                                       |
| <span id="UIA_SelectionItem_ElementRemovedFromSelectionEventId"></span><span id="uia_selectionitem_elementremovedfromselectioneventid"></span><span id="UIA_SELECTIONITEM_ELEMENTREMOVEDFROMSELECTIONEVENTID"></span><dl> <dt>**UIA \_SelectionItem \_ ElementRemovedFromSelectionEventId**</dt> <dt>20011</dt> </dl> | 識別從選取的項目集合中移除項目時所引發的事件。<br/>                                                                                                                                                                                                                                   |
| <span id="UIA_SelectionItem_ElementSelectedEventId"></span><span id="uia_selectionitem_elementselectedeventid"></span><span id="UIA_SELECTIONITEM_ELEMENTSELECTEDEVENTID"></span><dl> <dt>**UIA \_SelectionItem \_ ElementSelectedEventId**</dt> <dt>20012</dt> </dl>                                                 | 識別當 [**Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select)、 [**AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-addtoselection)或 [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-removefromselection) 方法的呼叫導致選取單一專案時所引發的事件。<br/> |
| <span id="UIA_StructureChangedEventId"></span><span id="uia_structurechangedeventid"></span><span id="UIA_STRUCTURECHANGEDEVENTID"></span><dl> <dt>**UIA \_StructureChangedEventId**</dt> <dt>20002</dt> </dl>                                                                                                      | 識別消費者介面自動化樹狀結構變更時引發的事件。<br/>                                                                                                                                                                                                                                      |
| <span id="UIA_SystemAlertEventId"></span><span id="uia_systemalerteventid"></span><span id="UIA_SYSTEMALERTEVENTID"></span><dl> <dt>**UIA \_SystemAlertEventId**</dt> <dt>20023</dt> </dl>                                                                                                                          | 識別提供者發出系統警示時引發的事件。 從 Windows 8 開始支援。<br/>                                                                                                                                                                                                              |
| <span id="UIA_Text_TextChangedEventId"></span><span id="uia_text_textchangedeventid"></span><span id="UIA_TEXT_TEXTCHANGEDEVENTID"></span><dl> <dt>**UIA \_文字 \_ TextChangedEventId**</dt> <dt>20015</dt> </dl>                                                                                                     | 識別修改文字內容時所引發的事件。<br/>                                                                                                                                                                                                                                                  |
| <span id="UIA_Text_TextSelectionChangedEventId"></span><span id="uia_text_textselectionchangedeventid"></span><span id="UIA_TEXT_TEXTSELECTIONCHANGEDEVENTID"></span><dl> <dt>**UIA \_文字 \_ TextSelectionChangedEventId**</dt> <dt>20014</dt> </dl>                                                                 | 識別修改文字選取範圍時所引發的事件。<br/>                                                                                                                                                                                                                                                   |
| <span id="UIA_TextEdit_ConversionTargetChangedEventId"></span><span id="uia_textedit_conversiontargetchangedeventid"></span><span id="UIA_TEXTEDIT_CONVERSIONTARGETCHANGEDEVENTID"></span><dl> <dt>**UIA \_Macos textedit \_ ConversionTargetChangedEventId**</dt> <dt>20033</dt> </dl>                                     | 識別每當控制項執行組合取代時引發的事件。 從 Windows 8.1 開始支援。<br/>                                                                                                                                                                                     |
| <span id="UIA_TextEdit_TextChangedEventId"></span><span id="uia_textedit_textchangedeventid"></span><span id="UIA_TEXTEDIT_TEXTCHANGEDEVENTID"></span><dl> <dt>**UIA \_Macos textedit \_ TextChangedEventId**</dt> <dt>20032</dt> </dl>                                                                                     | 識別每當控制項執行文字自動校正時所引發的事件。 從 Windows 8.1 開始支援。<br/>                                                                                                                                                                                          |
| <span id="UIA_ToolTipClosedEventId"></span><span id="uia_tooltipclosedeventid"></span><span id="UIA_TOOLTIPCLOSEDEVENTID"></span><dl> <dt>**UIA \_ToolTipClosedEventId**</dt> <dt>20001</dt> </dl>                                                                                                                  | 識別工具提示關閉時引發的事件。<br/>                                                                                                                                                                                                                                                              |
| <span id="UIA_ToolTipOpenedEventId"></span><span id="uia_tooltipopenedeventid"></span><span id="UIA_TOOLTIPOPENEDEVENTID"></span><dl> <dt>**UIA \_ToolTipOpenedEventId**</dt> <dt>20000</dt> </dl>                                                                                                                  | 識別工具提示開啟時引發的事件。<br/>                                                                                                                                                                                                                                                              |
| <span id="UIA_Window_WindowClosedEventId"></span><span id="uia_window_windowclosedeventid"></span><span id="UIA_WINDOW_WINDOWCLOSEDEVENTID"></span><dl> <dt>**UIA \_視窗 \_ WindowClosedEventId**</dt> <dt>20017</dt> </dl>                                                                                         | 識別視窗關閉時引發的事件。<br/>                                                                                                                                                                                                                                                               |
| <span id="UIA_Window_WindowOpenedEventId"></span><span id="uia_window_windowopenedeventid"></span><span id="UIA_WINDOW_WINDOWOPENEDEVENTID"></span><dl> <dt>**UIA \_視窗 \_ WindowOpenedEventId**</dt> <dt>20016</dt> </dl>                                                                                         | 識別視窗開啟時引發的事件。<br/>                                                                                                                                                                                                                                                               |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsXP \[ desktop apps \| UWP 應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | WindowsServer 2003 \[ desktop app \| UWP 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Uiautomationclient.dll。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[UI 自動化事件概觀](uiauto-eventsoverview.md)
</dt> </dl>

 

 





