---
title: 提供者的函式
description: 本節說明適用于 Microsoft Win32 應用程式消費者介面自動化提供者的功能。
ms.assetid: 76012ec7-0114-4b6b-a35e-5cfde5b90230
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea0542c3d0b313e1bed8ec040924349e37a29fea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968499"
---
# <a name="functions-for-providers"></a>提供者的函式

本節說明適用于 Microsoft Win32 應用程式消費者介面自動化提供者的功能。

## <a name="in-this-section"></a>本節內容



| 函式                                                                                                 | 描述                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UiaClientsAreListening**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaclientsarelistening)<br/>                       | 取得值，這個值會指出是否有任何用戶端應用程式訂閱 Microsoft 消費者介面自動化事件。<br/>                                             |
| [**UiaDisconnectAllProviders**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectallproviders)<br/>                         | 釋放所有與呼叫進程相關聯的提供者所持有的消費者介面自動化資源。 <br/>                                               |
| [**UiaDisconnectProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectprovider)<br/>                                 | 釋放特定提供者在消費者介面自動化物件中所保存的所有參考。<br/>                                                                      |
| [**UiaGetReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue)<br/> | 抓取保留值，指出消費者介面自動化 text 屬性的值在文字範圍內會有所不同。<br/>                                      |
| [**UiaGetReservedNotSupportedValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservednotsupportedvalue)<br/>     | 抓取保留值，表示不支援消費者介面自動化屬性或文字屬性。<br/>                                               |
| [**UiaHostProviderFromHwnd**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahostproviderfromhwnd)<br/>                     | 取得視窗的主機提供者。<br/>                                                                                                                    |
| [**UiaIAccessibleFromProvider**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider)<br/>                   | 抓取可代表消費者介面自動化提供者提供 Microsoft Active Accessibility 資料的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 執行。<br/> |
| [**UiaProviderForNonClient**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfornonclient)<br/>                     | 取得視窗的整個非工作區或視窗之非工作區中控制項的提供者。<br/>                                      |
| [**UiaProviderFromIAccessible**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfromiaccessible)<br/>               | 根據指定的 Microsoft Active Accessibility 物件，建立消費者介面自動化提供者。<br/>                                                          |
| [**UiaRaiseAsyncContentLoadedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseasynccontentloadedevent)<br/>     | 由提供者呼叫，以通知消費者介面自動化 core 內容正在以非同步方式載入。<br/>                                                      |
| [**UiaRaiseAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent)<br/>                     | 通知事件的接聽程式。<br/>                                                                                                                         |
| [**UiaRaiseAutomationPropertyChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationpropertychangedevent)<br/>    | 由提供者呼叫，以通知消費者介面自動化核心元素屬性已變更。<br/>                                                              |
| [**UiaRaiseChangesEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisechangesevent)<br/>                           | 由提供者呼叫，以通知消費者介面自動化核心已發生變更。<br/>                                                                        |
| [**UiaRaiseNotificationEvent**](https://www.bing.com/search?q=**UiaRaiseNotificationEvent**)<br/>             | 由提供者呼叫以起始通知事件。<br/>                                                                                                   |
| [**UiaRaiseStructureChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisestructurechangedevent)<br/>         | 由提供者呼叫，以通知消費者介面自動化核心樹狀結構已變更。<br/>                                                              |
| [**UiaRaiseTextEditTextChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent)<br/>   | 由提供者呼叫，以通知消費者介面自動化核心文字控制項以程式設計方式變更文字。<br/>                                            |
| [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider)<br/>             | 取得視窗之消費者介面自動化提供者的介面。<br/>                                                                                           |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[消費者介面自動化提供者](uiauto-entry-uiautoprovidersforwin32apps.md)
</dt> </dl>

 

