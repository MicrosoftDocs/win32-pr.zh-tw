---
title: 提供者介面
description: 本節說明 Microsoft Win32 應用程式消費者介面自動化提供者所執行的基本介面。
ms.assetid: e76d415d-5f5e-4e17-a5e4-4746e69c5010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a18a2368624cfea533891b29ee174bf2059d2e9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842499"
---
# <a name="interfaces-for-providers"></a>提供者介面

本節說明 Microsoft Win32 應用程式消費者介面自動化提供者所執行的基本介面。

## <a name="in-this-section"></a>本節內容



| 介面                                                                                                    | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)<br/>                                                     | 公開 Microsoft 消費者介面自動化所呼叫的方法，以取得支援 Microsoft Active Accessibility 之控制項的額外資訊。<br/>                                                                                                                                                                                                                                                                                                                |
| [**IAccessibleHostingElementProviders**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders)<br/>                  | 當物件是協助工具樹狀結構的根（包含可執行消費者介面自動化的無視窗 Microsoft ActiveX 控制項）時，Microsoft Active Accessibility 物件會執行這個介面。 由於 Microsoft Active Accessibility 和消費者介面自動化使用不同的介面，因此此介面可讓用戶端探索託管的無視窗 ActiveX 控制項清單，以支援消費者介面自動化以防用戶端以不同方式處理這些控制項。<br/> |
| [**IProxyProviderWinEventHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iproxyproviderwineventhandler)<br/>                     | 公開由 proxy 提供者所執行的方法，以處理 WinEvents。<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| [**IProxyProviderWinEventSink**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iproxyproviderwineventsink)<br/>                           | 公開 proxy 提供者用來引發事件的方法。<br/>                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents)<br/>                 | 公開呼叫的方法，以在消費者介面自動化用戶端應用程式開始或結束接聽該片段上的事件時，通知片段的根項目。<br/>                                                                                                                                                                                                                                                                                                |
| [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment)<br/>                         | 公開屬於多個層級（例如清單方塊或清單專案）之結構一部分的 UI 元素的方法和屬性。 由消費者介面自動化提供者執行。<br/>                                                                                                                                                                                                                                                                                          |
| [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)<br/>                 | 公開在片段中根項目的方法與屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles)<br/> | 當提供者是存取範圍樹狀結構的根（包含支援 Microsoft Active Accessibility 的無視窗控制項）時，這個介面會由消費者介面自動化提供者來執行。 由於消費者介面自動化和 Microsoft Active Accessibility 使用不同的介面，因此此介面可讓用戶端探索裝載的 Microsoft Active Accessibility 控制項清單，以防需要以不同的方式加以處理。<br/>                                 |
| [**IRawElementProviderHwndOverride**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderhwndoverride)<br/>                 | 公開方法，這個方法可讓您在片段的消費者介面自動化樹狀結構內重新置放以視窗為基礎的元素。<br/>                                                                                                                                                                                                                                                                                                                                                        |
| [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)<br/>                             | 定義公開簡單 UI 元素的方法和屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**IRawElementProviderSimple2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple2)<br/>                           | 擴充 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) 介面，以程式設計方式叫用快顯功能表。<br/>                                                                                                                                                                                                                                                                                                                        |
| [**IRawElementProviderSimple3**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple3)<br/>                           | 擴充 [**IRawElementProviderSimple2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple2) 介面，以啟用可存取技術應該如何說出慣用內容類型的相關中繼資料。<br/>                                                                                                                                                                                                                                                                    |
| [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite)<br/>         | ActiveX 控制項網站會執行這個介面，以啟用啟用消費者介面自動化的 ActiveX 控制項來表示其存取範圍。 這個介面可讓控制項容器為無視窗 ActiveX 控制項的父代或同級提供 [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) 指標，以及提供控制網站的唯一執行時間識別碼。<br/>                                                           |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[消費者介面自動化提供者](uiauto-entry-uiautoprovidersforwin32apps.md)
</dt> </dl>

 

