---
title: 架構和互通性
description: 本主題簡要說明 Microsoft Active Accessibility 和 Microsoft 消費者介面自動化的架構，以及允許應用程式之間的互通性的元件（以兩種不同的技術為基礎）。
ms.assetid: 7309819c-7c72-4bb3-ab9c-608a27c56d42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f318e46a6a0ad833b7aedb114974240fc4e52c08
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "104092505"
---
# <a name="architecture-and-interoperability"></a><span data-ttu-id="8d379-103">架構和互通性</span><span class="sxs-lookup"><span data-stu-id="8d379-103">Architecture and Interoperability</span></span>

<span data-ttu-id="8d379-104">本主題簡要說明 Microsoft Active Accessibility 和 Microsoft 消費者介面自動化的架構，以及允許應用程式之間的互通性的元件（以兩種不同的技術為基礎）。</span><span class="sxs-lookup"><span data-stu-id="8d379-104">This topic briefly describes the architecture of Microsoft Active Accessibility and Microsoft UI Automation, and the components that allow interoperability between applications based on the two different technologies.</span></span>

<span data-ttu-id="8d379-105">如需 Microsoft Active Accessibility 和消費者介面自動化互通性的詳細資訊，請參閱 [通用基礎結構](common-infrastructure.md)。</span><span class="sxs-lookup"><span data-stu-id="8d379-105">For more information about Microsoft Active Accessibility and UI Automation interoperability, see [Common Infrastructure](common-infrastructure.md).</span></span>

<span data-ttu-id="8d379-106">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="8d379-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="8d379-107">Microsoft Active Accessibility 架構</span><span class="sxs-lookup"><span data-stu-id="8d379-107">Microsoft Active Accessibility Architecture</span></span>](#microsoft-active-accessibility-architecture)
-   [<span data-ttu-id="8d379-108">消費者介面自動化架構</span><span class="sxs-lookup"><span data-stu-id="8d379-108">UI Automation Architecture</span></span>](#ui-automation-architecture)
-   [<span data-ttu-id="8d379-109">Microsoft Active Accessibility 和消費者介面自動化互通性</span><span class="sxs-lookup"><span data-stu-id="8d379-109">Microsoft Active Accessibility and UI Automation Interoperability</span></span>](#microsoft-active-accessibility-and-ui-automation-interoperability)
-   [<span data-ttu-id="8d379-110">IAccessibleEx 介面</span><span class="sxs-lookup"><span data-stu-id="8d379-110">The IAccessibleEx Interface</span></span>](#the-iaccessibleex-interface)
-   [<span data-ttu-id="8d379-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="8d379-111">Related topics</span></span>](#related-topics)

## <a name="microsoft-active-accessibility-architecture"></a><span data-ttu-id="8d379-112">Microsoft Active Accessibility 架構</span><span class="sxs-lookup"><span data-stu-id="8d379-112">Microsoft Active Accessibility Architecture</span></span>

<span data-ttu-id="8d379-113">Microsoft Active Accessibility 會公開有關控制項的基本資訊，例如控制項名稱、畫面上的位置和控制項類型，以及狀態資訊，例如可見度和啟用/停用狀態。</span><span class="sxs-lookup"><span data-stu-id="8d379-113">Microsoft Active Accessibility exposes basic information about controls such as control name, location on screen, and type of control, as well as state information such as visibility and enabled/disabled status.</span></span> <span data-ttu-id="8d379-114">UI 會以可存取物件的階層表示;變更和動作會以 WinEvents 表示。</span><span class="sxs-lookup"><span data-stu-id="8d379-114">The UI is represented as a hierarchy of accessible objects; changes and actions are represented as WinEvents.</span></span>

<span data-ttu-id="8d379-115">Microsoft Active Accessibility 是由下列元件所組成：</span><span class="sxs-lookup"><span data-stu-id="8d379-115">Microsoft Active Accessibility consists of the following components:</span></span>

-   <span data-ttu-id="8d379-116">可存取的物件-邏輯 UI 元素 (例如按鈕) ，此專案是由 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 元件物件模型所表示 (COM) 介面和整數子識別碼 (ChildID) 。</span><span class="sxs-lookup"><span data-stu-id="8d379-116">Accessible object—A logical UI element (such as a button) that is represented by an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Component Object Model (COM) interface and an integer child identifier (ChildID).</span></span>
-   <span data-ttu-id="8d379-117">WinEvents：一種事件系統，可讓伺服器在可存取的物件變更時通知用戶端。</span><span class="sxs-lookup"><span data-stu-id="8d379-117">WinEvents—An event system that enables servers to notify clients when an accessible object changes.</span></span> <span data-ttu-id="8d379-118">如需詳細資訊，請參閱 [WinEvents](winevents-infrastructure.md)。</span><span class="sxs-lookup"><span data-stu-id="8d379-118">For more information, see [WinEvents](winevents-infrastructure.md).</span></span>
-   <span data-ttu-id="8d379-119">OLEACC.dll：提供 Microsoft Active Accessibility API 和協助工具系統架構的執行時間動態連結程式庫。</span><span class="sxs-lookup"><span data-stu-id="8d379-119">OLEACC.dll—The run-time, dynamic-link library that provides the Microsoft Active Accessibility API and the accessibility system framework.</span></span> <span data-ttu-id="8d379-120">OLEACC 會執行可提供標準 UI 元素之預設協助工具資訊的 proxy 物件，包括使用者控制項、使用者功能表和通用控制項。</span><span class="sxs-lookup"><span data-stu-id="8d379-120">OLEACC implements proxy objects that provide default accessibility information for standard UI elements, including USER controls, USER menus, and common controls.</span></span>

<span data-ttu-id="8d379-121">針對 Microsoft Active Accessibility，協助工具架構 (OLEACC) 的系統元件，可協助輔助技術 (協助工具工具) 和應用程式之間的通訊，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="8d379-121">For Microsoft Active Accessibility, the system component of the accessibility framework (OLEACC) helps the communication between assistive technologies (accessibility tools) and applications, as the following illustration shows.</span></span>

![圖例顯示協助工具工具如何與應用程式互動](images/msaaarch.gif)

<span data-ttu-id="8d379-123">應用程式 (Microsoft Active Accessibility 伺服器) 提供 UI 協助工具資訊給 (Microsoft Active Accessibility 用戶端) 的工具，這會代表使用者與 UI 互動。</span><span class="sxs-lookup"><span data-stu-id="8d379-123">The applications (Microsoft Active Accessibility servers) provide UI accessibility information to tools (Microsoft Active Accessibility clients), which interact with the UI on behalf of users.</span></span> <span data-ttu-id="8d379-124">程式碼界限是以程式設計方式和進程界限。</span><span class="sxs-lookup"><span data-stu-id="8d379-124">The code boundary is both a programmatic and a process boundary.</span></span>

## <a name="ui-automation-architecture"></a><span data-ttu-id="8d379-125">消費者介面自動化架構</span><span class="sxs-lookup"><span data-stu-id="8d379-125">UI Automation Architecture</span></span>

<span data-ttu-id="8d379-126">使用消費者介面自動化，消費者介面自動化核心元件 (UIAutomationCore.dll) 會載入至協助工具工具和應用程式的進程。</span><span class="sxs-lookup"><span data-stu-id="8d379-126">With UI Automation, the UI Automation core component (UIAutomationCore.dll) is loaded into both the accessibility tools' and applications' processes.</span></span> <span data-ttu-id="8d379-127">核心元件可管理跨進程通訊、提供較高層級的服務，例如依屬性值搜尋元素，以及啟用大量提取或快取屬性，以提供比 Microsoft Active Accessibility 的執行更好的效能。</span><span class="sxs-lookup"><span data-stu-id="8d379-127">The core component manages cross-process communication, provides higher level services such as searching for elements by property values, and enables bulk fetching or caching of properties, which provides better performance than the Microsoft Active Accessibility implementation.</span></span>

<span data-ttu-id="8d379-128">消費者介面自動化包含的 proxy 物件可提供有關標準 UI 元素的 UI 資訊，例如使用者控制項、使用者功能表和通用控制項。</span><span class="sxs-lookup"><span data-stu-id="8d379-128">UI Automation includes proxy objects that provide UI information about standard UI elements such as USER controls, USER menus, and common controls.</span></span> <span data-ttu-id="8d379-129">它也包含可讓消費者介面自動化用戶端從 Microsoft Active Accessibility 伺服器取得 UI 資訊的 proxy。</span><span class="sxs-lookup"><span data-stu-id="8d379-129">It also includes proxies that enable UI Automation clients to get UI information from Microsoft Active Accessibility servers.</span></span>

<span data-ttu-id="8d379-130">下圖顯示協助工具工具 (用戶端) 和應用程式 (提供者) 中所使用的各種消費者介面自動化元件之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="8d379-130">The following illustration shows the relationships among the various UI Automation compontents used in accessibility tools (clients) and in applications (providers).</span></span>

![圖例顯示協助工具工具的元件如何與應用程式中的元件互動](images/uiaarch.gif)

## <a name="microsoft-active-accessibility-and-ui-automation-interoperability"></a><span data-ttu-id="8d379-132">Microsoft Active Accessibility 和消費者介面自動化互通性</span><span class="sxs-lookup"><span data-stu-id="8d379-132">Microsoft Active Accessibility and UI Automation Interoperability</span></span>

<span data-ttu-id="8d379-133">Microsoft Active Accessibility 橋接器的消費者介面自動化可讓 Microsoft Active Accessibility 用戶端藉由將消費者介面自動化物件模型轉換成 Microsoft Active Accessibility 物件模型，來存取消費者介面自動化提供者。</span><span class="sxs-lookup"><span data-stu-id="8d379-133">The UI Automation to Microsoft Active Accessibility Bridge enables Microsoft Active Accessibility clients to access UI Automation providers by converting the UI Automation object model to a Microsoft Active Accessibility object model.</span></span> <span data-ttu-id="8d379-134">下圖顯示消費者介面自動化對 Microsoft Active Accessibility 橋接器的角色。</span><span class="sxs-lookup"><span data-stu-id="8d379-134">The following illustration shows the role of the UI Automation-to-Microsoft Active Accessibility Bridge.</span></span>

![圖例顯示 ui 自動化如何與協助工具工具和應用程式搭配運作](images/uiatomsaabridge.gif)

<span data-ttu-id="8d379-136">同樣地，Microsoft Active Accessibility 對消費者介面自動化 Proxy 會為消費者介面自動化用戶端轉譯以 Microsoft Active Accessibility 為基礎的伺服器物件模型。</span><span class="sxs-lookup"><span data-stu-id="8d379-136">Similarly, the Microsoft Active Accessibility-to-UI Automation Proxy translates Microsoft Active Accessibility-based server object models for UI Automation clients.</span></span> <span data-ttu-id="8d379-137">下圖顯示 Microsoft Active Accessibility 對消費者介面自動化 Proxy 的角色。</span><span class="sxs-lookup"><span data-stu-id="8d379-137">The following illustration shows the role of the Microsoft Active Accessibility-to-UI Automation Proxy.</span></span>

![圖例顯示 ui automation proxy 如何搭配協助工具工具和應用程式運作](images/msaatouiaproxy.gif)

## <a name="the-iaccessibleex-interface"></a><span data-ttu-id="8d379-139">IAccessibleEx 介面</span><span class="sxs-lookup"><span data-stu-id="8d379-139">The IAccessibleEx Interface</span></span>

<span data-ttu-id="8d379-140">[**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)介面可讓現有的應用程式或 UI 程式庫擴充其 Microsoft Active Accessibility 物件模型，以支援消費者介面自動化，而不需要從頭重寫執行。</span><span class="sxs-lookup"><span data-stu-id="8d379-140">The [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface enables existing applications or UI libraries to extend their Microsoft Active Accessibility object model to support UI Automation without rewriting the implementation from scratch.</span></span> <span data-ttu-id="8d379-141">使用 **IAccessibleEx**，您可以只執行完整描述 UI 和其功能所需的其他消費者介面自動化屬性和控制項模式。</span><span class="sxs-lookup"><span data-stu-id="8d379-141">With **IAccessibleEx**, you can implement only the additional UI Automation properties and control patterns needed to fully describe the UI and its functionality.</span></span>

<span data-ttu-id="8d379-142">由於 Microsoft Active Accessibility 對消費者介面自動化 Proxy 會將已啟用 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)之 Microsoft Active Accessibility 伺服器的物件模型轉譯成消費者介面自動化物件模型，因此消費者介面自動化用戶端不需要執行任何額外的工作。</span><span class="sxs-lookup"><span data-stu-id="8d379-142">Because the Microsoft Active Accessibility-to-UI Automation Proxy translates the object models of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)-enabled Microsoft Active Accessibility servers as UI Automation object models, UI Automation clients do not need to do any extra work.</span></span> <span data-ttu-id="8d379-143">**IAccessibleEx** 介面也可以啟用同進程 Microsoft Active Accessibility 用戶端直接與消費者介面自動化提供者互動。</span><span class="sxs-lookup"><span data-stu-id="8d379-143">The **IAccessibleEx** interface can also enable in-process Microsoft Active Accessibility clients to interact directly with UI Automation providers.</span></span>

<span data-ttu-id="8d379-144">如需詳細資訊，請參閱 [IAccessibleEx 介面](iaccessibleex.md)。</span><span class="sxs-lookup"><span data-stu-id="8d379-144">For more information, see [The IAccessibleEx Interface](iaccessibleex.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d379-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="8d379-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d379-146">Windows Automation API 總覽</span><span class="sxs-lookup"><span data-stu-id="8d379-146">Windows Automation API Overview</span></span>](windows-automation-api-overview.md)
</dt> <dt>

[<span data-ttu-id="8d379-147">IAccessibleEx 介面</span><span class="sxs-lookup"><span data-stu-id="8d379-147">The IAccessibleEx Interface</span></span>](iaccessibleex.md)
</dt> <dt>

[<span data-ttu-id="8d379-148">輔助技術的安全性考慮</span><span class="sxs-lookup"><span data-stu-id="8d379-148">Security Considerations for Assistive Technologies</span></span>](uiauto-securityoverview.md)
</dt> </dl>

 

 




