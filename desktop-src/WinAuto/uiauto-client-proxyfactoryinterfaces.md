---
title: 用戶端的 Proxy Factory 介面
description: 本節說明非受控消費者介面自動化用戶端應用程式的 proxy factory 介面。
ms.assetid: 46c6720a-19c2-4ddd-893c-1a46af0642fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fc1827ab36a221dcd7f27e5b2a05de91931b0ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021944"
---
# <a name="proxy-factory-interfaces-for-clients"></a>用戶端的 Proxy Factory 介面

本節說明非受控消費者介面自動化用戶端應用程式的 proxy factory 介面。

## <a name="in-this-section"></a>本節內容



| 介面                                                                                      | 描述                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory)<br/>               | 公開物件的屬性和方法，該物件會為沒有消費者介面自動化原生支援的 UI 專案建立 Microsoft 消費者介面自動化提供者。 此介面是由 proxy 所執行。<br/>                                                                          |
| [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry)<br/>     | 代表消費者介面自動化所維護之資料表中的 proxy factory，並公開可供用戶端應用程式與 [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) 物件互動的屬性和方法。<br/>                                   |
| [**IUIAutomationProxyFactoryMapping**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping)<br/> | 公開 proxy factory 資料表的屬性和方法。 每個資料表專案都以 [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) 介面表示。 專案會依照系統嘗試使用 proxy 的順序排列。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[消費者介面自動化用戶端](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





