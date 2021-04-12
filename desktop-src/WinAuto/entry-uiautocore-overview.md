---
title: UI 自動化基礎觀念
description: 本節說明消費者介面自動化所依據的基本概念。
ms.assetid: 109f113f-9ed0-4a57-b3af-90e831e53c42
keywords:
- 消費者介面自動化，Microsoft WIN32 API
- 消費者介面自動化，WIN32 API
- 消費者介面自動化，提供者
- 消費者介面自動化，用戶端應用程式
- 用戶端，microsoft 消費者介面自動化 for Microsoft WIN32 API
- 適用于 Microsoft WIN32 API 的用戶端、消費者介面自動化
- Win32 應用程式開發介面
- Microsoft WIN32 API
- 適用于 Microsoft WIN32 API 的消費者介面自動化
- Microsoft 消費者介面自動化 for Microsoft WIN32 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba8147a8dd7f8d03340fad43465c225a174e606
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372406"
---
# <a name="ui-automation-fundamentals"></a><span data-ttu-id="f7899-113">UI 自動化基礎觀念</span><span class="sxs-lookup"><span data-stu-id="f7899-113">UI Automation Fundamentals</span></span>

<span data-ttu-id="f7899-114">Microsoft 消費者介面自動化可讓輔助技術應用程式和自動化測試控管與其他應用程式的 UI 控制項互動。</span><span class="sxs-lookup"><span data-stu-id="f7899-114">Microsoft UI Automation enables assistive technology applications and automated testing tools to interact with the UI controls of other applications.</span></span> <span data-ttu-id="f7899-115">本節說明消費者介面自動化所依據的基本概念。</span><span class="sxs-lookup"><span data-stu-id="f7899-115">This section explains the fundamental concepts that UI Automation is based on.</span></span>

<span data-ttu-id="f7899-116">消費者介面自動化 API 分為兩個部分。</span><span class="sxs-lookup"><span data-stu-id="f7899-116">The UI Automation API is in two parts.</span></span> <span data-ttu-id="f7899-117">*消費者介面自動化提供者* 應用程式會使用一個部分，而另一個部分則由 *消費者介面自動化用戶端* 應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="f7899-117">One part is used by *UI Automation provider* applications, and the other is used by *UI Automation client* applications.</span></span> <span data-ttu-id="f7899-118">提供者 API 可讓 Microsoft Win32 自訂控制項和其他控制項架構的開發人員將這些控制項公開給消費者介面自動化，並讓用戶端應用程式看見這些控制項。</span><span class="sxs-lookup"><span data-stu-id="f7899-118">The provider API enables developers of Microsoft Win32 custom control and other control frameworks to expose those controls to UI Automation and make them visible to client applications.</span></span> <span data-ttu-id="f7899-119">用戶端 API 可讓應用程式與其他應用程式中的控制項互動，並取得其相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f7899-119">The client API enables applications to interact with controls in other applications and retrieve information about them.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f7899-120">本節內容</span><span class="sxs-lookup"><span data-stu-id="f7899-120">In this section</span></span>

-   [<span data-ttu-id="f7899-121">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="f7899-121">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
-   [<span data-ttu-id="f7899-122">消費者介面自動化和 Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="f7899-122">UI Automation and Active Accessibility</span></span>](uiauto-msaa.md)
-   [<span data-ttu-id="f7899-123">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="f7899-123">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
-   [<span data-ttu-id="f7899-124">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="f7899-124">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
-   [<span data-ttu-id="f7899-125">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="f7899-125">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
-   [<span data-ttu-id="f7899-126">UI 自動化屬性概觀</span><span class="sxs-lookup"><span data-stu-id="f7899-126">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
-   [<span data-ttu-id="f7899-127">UI 自動化事件概觀</span><span class="sxs-lookup"><span data-stu-id="f7899-127">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
-   [<span data-ttu-id="f7899-128">自訂屬性、事件和控制項模式</span><span class="sxs-lookup"><span data-stu-id="f7899-128">Custom Properties, Events, and Control Patterns</span></span>](uiauto-custompropertieseventscontrolpatterns.md)
-   [<span data-ttu-id="f7899-129">消費者介面自動化文字內容的支援</span><span class="sxs-lookup"><span data-stu-id="f7899-129">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
-   [<span data-ttu-id="f7899-130">消費者介面自動化的拖放支援</span><span class="sxs-lookup"><span data-stu-id="f7899-130">UI Automation Support for Drag-and-Drop</span></span>](ui-automation-support-for-drag-and-drop.md)
-   [<span data-ttu-id="f7899-131">輔助技術的安全性考慮</span><span class="sxs-lookup"><span data-stu-id="f7899-131">Security Considerations for Assistive Technologies</span></span>](uiauto-securityoverview.md)
-   [<span data-ttu-id="f7899-132">使用安全陣列的最佳作法</span><span class="sxs-lookup"><span data-stu-id="f7899-132">Best Practices for Using Safe Arrays</span></span>](uiauto-workingwithsafearrays.md)
-   [<span data-ttu-id="f7899-133"> 自動化規格和社群承諾</span><span class="sxs-lookup"><span data-stu-id="f7899-133">UI Automation Specification and Community Promise</span></span>](uiauto-specandcommunitypromise.md)

## <a name="related-topics"></a><span data-ttu-id="f7899-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="f7899-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7899-135">使用者介面自動化</span><span class="sxs-lookup"><span data-stu-id="f7899-135">UI Automation</span></span>](entry-uiauto-win32.md)
</dt> </dl>

 

 




