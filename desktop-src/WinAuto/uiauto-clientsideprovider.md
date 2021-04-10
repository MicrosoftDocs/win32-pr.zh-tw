---
title: '消費者介面自動化提供者執行 Client-Side (Proxy) '
description: 本主題說明如何撰寫不受支援控制項的 proxy 提供者，並將它新增至用戶端應用程式所使用的 proxy 清單。
ms.assetid: c66f4a7b-0a12-4c65-a3e9-1c826d54ac6b
keywords:
- 消費者介面自動化，用戶端提供者的執行
- 消費者介面自動化，提供者執行
- 消費者介面自動化，執行用戶端提供者
- 消費者介面自動化，執行提供者
- 消費者介面自動化，proxy
- Proxy
- 用戶端提供者
- 提供者，實施
- 執行用戶端提供者
- 實作提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e2bdb4a94ba6e693792508de5c573317299b0d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023564"
---
# <a name="implementing-a-client-side-proxy-ui-automation-provider"></a>消費者介面自動化提供者執行 Client-Side (Proxy) 

Microsoft 消費者介面自動化提供一組適用于大部分標準控制項的 proxy，例如 Microsoft Win32、Windows Forms 和 Windows Presentation Foundation (WPF) 應用程式中使用的控制項。 不過，許多自訂控制項和協力廠商控制項都不會執行原生消費者介面自動化提供者。 若要消費者介面自動化用戶端應用程式存取，這些控制項必須提供用戶端提供者（也稱為 *proxy 提供者或 proxy*） **。

本主題說明如何撰寫不受支援控制項的 proxy 提供者，並將它新增至用戶端應用程式所使用的 proxy 清單。 它包含下列主題︰

-   [什麼是 Proxy？](#what-is-a-proxy)
-   [什麼是 Proxy Factory？](#what-is-a-proxy-factory)
-   [Proxy Factory 對應](#proxy-factory-mapping)
-   [管理預設 proxy](#managing-default-proxies)
-   [相關主題](#related-topics)

如需示範如何執行 proxy 提供者的程式碼範例，請參閱 [消費者介面自動化提供者的如何主題](uiauto-howto-topics-for-uiautomation-providers.md)。

## <a name="what-is-a-proxy"></a>什麼是 Proxy？

用戶端提供者（或 proxy）是代表沒有本身之 **IRawElementProviderSimple** 執行的控制項來實 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)介面的物件。 如果沒有 proxy，則這類控制項在消費者介面自動化中大多是不透明的，它只能提供視窗控制碼 (**HWND**) 所提供的基本資訊，例如控制項位置。

## <a name="what-is-a-proxy-factory"></a>什麼是 Proxy Factory？

每個 proxy 都需要對應的 *proxy factory*，也就是公開 [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) 介面的物件。 消費者介面自動化會維護 proxy 處理站 *專案* 的內部資料表，其中每個專案都包含每個 proxy 的 proxy factory 參考，以及一組條件。 當消費者介面自動化遇到沒有原生 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) 執行的控制項時，它會搜尋其條件指出支援控制項的 proxy factory 專案。 消費者介面自動化從一開始就搜尋資料表，當它找到相符的專案時，消費者介面自動化會呼叫 factory 的 [**IUIAutomationProxyFactory：： CreateProvider**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider) 方法。 如果已成功建立相符的 proxy，消費者介面自動化會停止搜尋並使用新建立的 proxy 物件;否則，消費者介面自動化會繼續搜尋。

用戶端應用程式會使用 [**IUIAutomation：： CreateProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createproxyfactoryentry) 方法建立 proxy factory 專案的實例，此方法會傳回 [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) 介面指標。 用戶端會使用 **IUIAutomationProxyFactoryEntry** 所公開的方法來指定 proxy factory 用來建立 proxy 的一組條件。

當它呼叫 [**IUIAutomationProxyFactory：： CreateProvider**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider)時，消費者介面自動化會傳遞 proxy factory 物件可使用的參數，以判斷 proxy 是否已充分支援自訂控制項。 若是如此，proxy factory 會建立 proxy 的實例，並傳回 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) 介面指標;否則，它會傳回 **Null** 指標。

## <a name="proxy-factory-mapping"></a>Proxy Factory 對應

依預設，消費者介面自動化會依下列順序搜尋 proxy factory 資料表。



| 單 | Proxy                        | 描述                                                                      |
|-------|------------------------------|----------------------------------------------------------------------------------|
| 1     | Microsoft：非控制 Proxy | 適用于具有完整類別名稱或基類名稱 "ComboBoxEx32" 的視窗。         |
| 2     | Microsoft：非控制 Proxy | 適用于具有完整類別名稱或基類名稱 "WorkerW" 的視窗。              |
| 3     | Microsoft：非控制 Proxy | 適用于具有完整類別名稱或基類名稱 "SHELLDLL \_ DefView" 的視窗。    |
| 4     | Microsoft：容器 Proxy   | 適用于具有完整類別名稱或基類名稱 " \# 32770" 的視窗。              |
| 5     | Microsoft：容器 Proxy   | 適用于具有類別名稱的 windows 或包含 "AfxControlBar" 的基類名稱。     |
| 6     | Microsoft： TreeView Proxy    | 適用于具有類別名稱的 windows 或包含 "SysTreeView32" 的基類名稱。     |
| 7     | Microsoft： ListView Proxy    | 若為具有類別名稱的 windows 或包含 "SysListView32" 的基類名稱 (1) 。 |
| 8     | Microsoft： ListView Proxy    | 若為具有類別名稱的 windows 或包含 "SysListView32" 的基類名稱 (2) 。 |
| 9     | Microsoft： MSAA Proxy        | 適用于任何視窗。                                                                  |



 

Proxy 7 和8是 SysListView32 控制項的重複專案。 如果沒有修改，則會一律使用 proxy 7 作為 SysListView32 控制項，而且永遠不會使用 proxy 8。 Proxy 8 僅適用于可見的清單專案，而且通常僅供使用 visible 元素或具有嚴格效能需求的用戶端應用程式使用。 這些用戶端可以移除 proxy 7。

Proxy 9 是消費者介面自動化 proxy 的 Microsoft Active Accessibility 應該一律是資料表中的最後一個專案。 這可為執行 Microsoft Active Accessibility 但不消費者介面自動化的控制項啟用 Microsoft Active Accessibility 的回溯功能。

修改 proxy factory 資料表中的專案時，您應該仔細評估專案的新位置。 建議您將自訂 proxy 的專案放置在非控制項和容器 proxy 之後，但在 Microsoft Active Accessibility 至消費者介面自動化 proxy 之前。 此外，雖然 [**CreateProvider**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider) 呼叫中的程式碼可以判斷它是否應該支援給定的視窗控制碼 (**HWND**) ，但更有效率的方法是讓消費者介面自動化根據類別名稱選取 Proxy，然後將 **CreateProvider** 方法中的條件碼保持為最小值。

消費者介面自動化為每個用戶端維護不同的 proxy factory 資料表。 當用戶端變更其 proxy 資料表時，變更只會影響用戶端本身;其他用戶端則不受影響。

## <a name="managing-default-proxies"></a>管理預設 proxy

當用戶端應用程式建立 [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) 物件時，proxy factory 資料表最初隻會包含標準控制項之預設 proxy 提供者的專案。 藉由使用 [**IUIAutomationProxyFactoryMapping**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping) 介面，用戶端可以新增專案、移除不必要的專案、變更專案的順序等等。 用戶端可以藉由呼叫 [**IUIAutomation：:P roxyfactorymapping**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_proxyfactorymapping)方法來取出 **IUIAutomationProxyFactoryMapping** 介面指標。

可用 proxy 的表格包含每個 proxy 的 [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) 介面。 每個 **IUIAutomationProxyFactoryEntry** 都會指定 proxy 所服務的 [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) 和控制項類別，並定義事件的處理方式。

Proxy 的資料表會以 [**IUIAutomationProxyFactoryMapping**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping) 介面表示，而此介面可以從 [**IUIAutomation：:P roxyfactorymapping**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_proxyfactorymapping) 屬性取得。 應用程式可以使用 **IUIAutomationProxyFactoryMapping** 方法來新增和刪除 proxy。 若要建立要加入此資料表的新專案，請使用 [**IUIAutomation：： CreateProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createproxyfactoryentry) 取得介面，然後使用 [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) 方法來定義適用的控制項類別和 proxy 的行為。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何) 消費者介面自動化提供者建立 Client-Side (Proxy](uiauto-howto-create-clientside-provider.md)
</dt> <dt>

[消費者介面自動化提供者程式設計人員指南](uiauto-providerportal.md)
</dt> </dl>

 

 