---
title: 消費者介面自動化用戶端程式設計人員指南
description: 本節包含建立應用程式的相關資訊，這些應用程式會使用 Microsoft 消費者介面自動化與其他應用程式和桌面的 UI 互動。
ms.assetid: d3616e1f-7b38-4a3e-ac96-72ec70cc13fc
keywords:
- 建立消費者介面自動化用戶端應用程式
- 建立用戶端應用程式
- 用戶端，建立消費者介面自動化應用程式
- 用戶端，消費者介面自動化應用程式建立
- 消費者介面自動化，建立用戶端應用程式
- 消費者介面自動化，建立用戶端應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f353243c8c194e2d732efd1d68bc2894ca930285
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682462"
---
# <a name="ui-automation-client-programmers-guide"></a><span data-ttu-id="edd14-109">消費者介面自動化用戶端程式設計人員指南</span><span class="sxs-lookup"><span data-stu-id="edd14-109">UI Automation Client Programmer's Guide</span></span>

<span data-ttu-id="edd14-110">本節包含建立應用程式的相關資訊，這些應用程式會使用 Microsoft 消費者介面自動化與其他應用程式和桌面的 UI 互動。</span><span class="sxs-lookup"><span data-stu-id="edd14-110">This section contains information about creating applications that use Microsoft UI Automation to interact with the UI of other applications and the desktop.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="edd14-111">本節內容</span><span class="sxs-lookup"><span data-stu-id="edd14-111">In this section</span></span>

-   [<span data-ttu-id="edd14-112">消費者介面自動化用戶端總覽</span><span class="sxs-lookup"><span data-stu-id="edd14-112">UI Automation Clients Overview</span></span>](/windows/desktop/WinAuto/uiauto-clientsoverview)
-   [<span data-ttu-id="edd14-113">建立 CUIAutomation 物件</span><span class="sxs-lookup"><span data-stu-id="edd14-113">Creating the CUIAutomation Object</span></span>](uiauto-creatingcuiautomation.md)
-   [<span data-ttu-id="edd14-114">取得 UI 自動化項目</span><span class="sxs-lookup"><span data-stu-id="edd14-114">Obtaining UI Automation Elements</span></span>](uiauto-obtainingelements.md)
-   [<span data-ttu-id="edd14-115">從消費者介面自動化元素抓取屬性</span><span class="sxs-lookup"><span data-stu-id="edd14-115">Retrieving Properties from UI Automation Elements</span></span>](uiauto-propertiesforclients.md)
-   [<span data-ttu-id="edd14-116">快取消費者介面自動化屬性和控制項模式</span><span class="sxs-lookup"><span data-stu-id="edd14-116">Caching UI Automation Properties and Control Patterns</span></span>](uiauto-cachingforclients.md)
-   [<span data-ttu-id="edd14-117">訂閱消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="edd14-117">Subscribing to UI Automation Events</span></span>](uiauto-eventsforclients.md)
-   [<span data-ttu-id="edd14-118">使用以文字為基礎的控制項</span><span class="sxs-lookup"><span data-stu-id="edd14-118">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
-   [<span data-ttu-id="edd14-119">使用虛擬化專案</span><span class="sxs-lookup"><span data-stu-id="edd14-119">Working with Virtualized Items</span></span>](uiauto-workingwithvirtualizeditems.md)
-   [<span data-ttu-id="edd14-120">存取 Microsoft Active Accessibility 伺服器</span><span class="sxs-lookup"><span data-stu-id="edd14-120">Accessing Microsoft Active Accessibility Servers</span></span>](uiauto-accessingmsaaservers.md)
-   [<span data-ttu-id="edd14-121">使用 UI 自動化進行自動化測試</span><span class="sxs-lookup"><span data-stu-id="edd14-121">Using UI Automation for Automated Testing</span></span>](uiauto-usefortesting.md)
-   [<span data-ttu-id="edd14-122">瞭解螢幕縮放問題</span><span class="sxs-lookup"><span data-stu-id="edd14-122">Understanding Screen Scaling Issues</span></span>](uiauto-screenscaling.md)
-   [<span data-ttu-id="edd14-123">瞭解執行緒問題</span><span class="sxs-lookup"><span data-stu-id="edd14-123">Understanding Threading Issues</span></span>](uiauto-threading.md)
-   [<span data-ttu-id="edd14-124">消費者介面自動化用戶端的使用說明主題</span><span class="sxs-lookup"><span data-stu-id="edd14-124">How-To Topics for UI Automation Clients</span></span>](uiauto-howto-topics-for-uiautomation-clients.md)

## <a name="related-topics"></a><span data-ttu-id="edd14-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="edd14-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edd14-126">向輕鬆存取註冊</span><span class="sxs-lookup"><span data-stu-id="edd14-126">Registering with Ease of Access</span></span>](/windows/desktop/WinAuto/ease-of-access---assistive-technology-registration)
</dt> <dt>

[<span data-ttu-id="edd14-127">輔助技術的安全性考慮</span><span class="sxs-lookup"><span data-stu-id="edd14-127">Security Considerations for Assistive Technologies</span></span>](uiauto-securityoverview.md)
</dt> <dt>

[<span data-ttu-id="edd14-128">使用者介面自動化</span><span class="sxs-lookup"><span data-stu-id="edd14-128">UI Automation</span></span>](entry-uiauto-win32.md)
</dt> </dl>

 

 