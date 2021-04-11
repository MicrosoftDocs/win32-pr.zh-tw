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
# <a name="proxy-factory-interfaces-for-clients"></a><span data-ttu-id="9313b-103">用戶端的 Proxy Factory 介面</span><span class="sxs-lookup"><span data-stu-id="9313b-103">Proxy Factory Interfaces for Clients</span></span>

<span data-ttu-id="9313b-104">本節說明非受控消費者介面自動化用戶端應用程式的 proxy factory 介面。</span><span class="sxs-lookup"><span data-stu-id="9313b-104">This section describes the proxy factory interfaces for unmanaged UI Automation client applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9313b-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="9313b-105">In this section</span></span>



| <span data-ttu-id="9313b-106">介面</span><span class="sxs-lookup"><span data-stu-id="9313b-106">Interface</span></span>                                                                                      | <span data-ttu-id="9313b-107">描述</span><span class="sxs-lookup"><span data-stu-id="9313b-107">Description</span></span>                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9313b-108">**IUIAutomationProxyFactory**</span><span class="sxs-lookup"><span data-stu-id="9313b-108">**IUIAutomationProxyFactory**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory)<br/>               | <span data-ttu-id="9313b-109">公開物件的屬性和方法，該物件會為沒有消費者介面自動化原生支援的 UI 專案建立 Microsoft 消費者介面自動化提供者。</span><span class="sxs-lookup"><span data-stu-id="9313b-109">Exposes properties and methods of an object that creates a Microsoft UI Automation provider for UI elements that do not have native support for UI Automation.</span></span> <span data-ttu-id="9313b-110">此介面是由 proxy 所執行。</span><span class="sxs-lookup"><span data-stu-id="9313b-110">This interface is implemented by proxies.</span></span><br/>                                                                          |
| [<span data-ttu-id="9313b-111">**IUIAutomationProxyFactoryEntry**</span><span class="sxs-lookup"><span data-stu-id="9313b-111">**IUIAutomationProxyFactoryEntry**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry)<br/>     | <span data-ttu-id="9313b-112">代表消費者介面自動化所維護之資料表中的 proxy factory，並公開可供用戶端應用程式與 [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) 物件互動的屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="9313b-112">Represents a proxy factory in the table maintained by UI Automation, and exposes properties and methods that can be used by client applications to interact with [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) objects.</span></span><br/>                                   |
| [<span data-ttu-id="9313b-113">**IUIAutomationProxyFactoryMapping**</span><span class="sxs-lookup"><span data-stu-id="9313b-113">**IUIAutomationProxyFactoryMapping**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping)<br/> | <span data-ttu-id="9313b-114">公開 proxy factory 資料表的屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="9313b-114">Exposes properties and methods for a table of proxy factories.</span></span> <span data-ttu-id="9313b-115">每個資料表專案都以 [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) 介面表示。</span><span class="sxs-lookup"><span data-stu-id="9313b-115">Each table entry is represented by an [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) interface.</span></span> <span data-ttu-id="9313b-116">專案會依照系統嘗試使用 proxy 的順序排列。</span><span class="sxs-lookup"><span data-stu-id="9313b-116">The entries are in the order in which the system will attempt to use the proxies.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="9313b-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="9313b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9313b-118">消費者介面自動化用戶端</span><span class="sxs-lookup"><span data-stu-id="9313b-118">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





