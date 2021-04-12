---
title: 消費者介面自動化用戶端總覽
description: 本主題說明在執行 Microsoft 消費者介面自動化用戶端應用程式時所涉及的主要工作。
ms.assetid: 536ccf03-2f52-49e5-a95f-ea56cf821779
keywords:
- 消費者介面自動化，用戶端總覽
- 用戶端，關於
- 用戶端、元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d4705d75a0a80c114e2b83f9625f827c75503b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375489"
---
# <a name="ui-automation-clients-overview"></a><span data-ttu-id="576c0-106">消費者介面自動化用戶端總覽</span><span class="sxs-lookup"><span data-stu-id="576c0-106">UI Automation Clients Overview</span></span>

<span data-ttu-id="576c0-107">本主題說明在執行 Microsoft 消費者介面自動化用戶端應用程式時所涉及的主要工作。</span><span class="sxs-lookup"><span data-stu-id="576c0-107">This topic describes the main tasks involved in implementing a Microsoft UI Automation client application.</span></span>

<span data-ttu-id="576c0-108">消費者介面自動化用戶端是任何使用消費者介面自動化 API 來存取 UI 專案相關資訊的應用程式，或是透過以程式設計方式操作其 UI 元素來控制應用程式的任何應用程式。</span><span class="sxs-lookup"><span data-stu-id="576c0-108">A UI Automation client is any application that uses the UI Automation API to access information about UI elements, or to control applications through programmatic manipulation of their UI elements.</span></span> <span data-ttu-id="576c0-109">消費者介面自動化用戶端包括輔助技術應用程式，例如螢幕讀取器，它會取出 UI 元素的相關資訊，並以可供殘障人士使用的方式呈現資訊。</span><span class="sxs-lookup"><span data-stu-id="576c0-109">UI Automation clients include assistive technology applications such as screen readers, which retrieve information about UI elements and present the information in a way that is usable for people with disabilities.</span></span> <span data-ttu-id="576c0-110">它們也包含語音辨識程式和軟體測試控管之類的應用程式，這些工具使用消費者介面自動化而不是滑鼠和鍵盤來「驅動」其他應用程式。</span><span class="sxs-lookup"><span data-stu-id="576c0-110">They also include applications such as speech recognition programs and software testing tools, which use UI Automation instead of the mouse and keyboard to "drive" other applications.</span></span>

<span data-ttu-id="576c0-111">從消費者介面自動化的觀點來看，消費者介面自動化用戶端應用程式必須完成的主要工作包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="576c0-111">From a UI Automation perspective, the main tasks that a UI Automation client application must accomplish include the following:</span></span>

1.  <span data-ttu-id="576c0-112">**取得 CUIAutomation 物件的實例。**</span><span class="sxs-lookup"><span data-stu-id="576c0-112">**Obtain an instance of the CUIAutomation object.**</span></span>

    <span data-ttu-id="576c0-113">UI 元素的相關資訊，以及 UI 元素功能的存取權，會由消費者介面自動化提供者公開給用戶端。</span><span class="sxs-lookup"><span data-stu-id="576c0-113">Information about UI elements, and access to UI element functionality, is exposed to clients by UI Automation providers.</span></span> <span data-ttu-id="576c0-114">不過，用戶端應用程式無法直接與提供者搭配運作。</span><span class="sxs-lookup"><span data-stu-id="576c0-114">However, client applications do not work directly with providers.</span></span> <span data-ttu-id="576c0-115">相反地，核心服務位於用戶端和提供者之間。</span><span class="sxs-lookup"><span data-stu-id="576c0-115">Instead, a core service lies between the client and the provider.</span></span> <span data-ttu-id="576c0-116">當用戶端呼叫消費者介面自動化 API 時，它實際上會呼叫消費者介面自動化核心服務，而該服務會接著呼叫提供者所執行的介面。</span><span class="sxs-lookup"><span data-stu-id="576c0-116">When a client calls the UI Automation API, it is actually calling the UI Automation core service which, in turn, makes calls to the interfaces implemented by the provider.</span></span>

    <span data-ttu-id="576c0-117">若要取得核心消費者介面自動化服務的存取權，用戶端必須建立 [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) 物件的實例，並在物件上取出 [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="576c0-117">To gain access to the core UI Automation service, a client must create an instance of the [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) object and retrieve an [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface pointer on the object.</span></span> <span data-ttu-id="576c0-118">**IUIAutomation** 指標是用戶端用來存取用戶端可用之所有消費者介面自動化功能的金鑰。</span><span class="sxs-lookup"><span data-stu-id="576c0-118">The **IUIAutomation** pointer is the client's key to accessing all of the UI Automation functionality that is available to the client.</span></span> <span data-ttu-id="576c0-119">如需詳細資訊，請參閱 [建立 CUIAutomation 物件](uiauto-creatingcuiautomation.md)。</span><span class="sxs-lookup"><span data-stu-id="576c0-119">For more information, see [Creating the CUIAutomation Object](uiauto-creatingcuiautomation.md).</span></span>

2.  <span data-ttu-id="576c0-120">**從消費者介面自動化樹狀結構取出 UI 元素的 IUIAutomationElement 介面。**</span><span class="sxs-lookup"><span data-stu-id="576c0-120">**Retrieve IUIAutomationElement interfaces for UI elements from the UI Automation tree.**</span></span>

    <span data-ttu-id="576c0-121">消費者介面自動化會將個別的 UI 專案公開為執行 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面的物件。</span><span class="sxs-lookup"><span data-stu-id="576c0-121">UI Automation exposes individual UI elements as objects that implement the [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface.</span></span> <span data-ttu-id="576c0-122">專案的相關資訊可透過專案的 **IUIAutomationElement** 介面所公開的屬性提供給用戶端，並可存取專案的控制項模式。</span><span class="sxs-lookup"><span data-stu-id="576c0-122">Information about an element is available to clients through properties exposed by the element's **IUIAutomationElement** interface, along with access to the element's control patterns.</span></span> <span data-ttu-id="576c0-123">控制項模式介面所公開的屬性和方法，可讓您存取控制項特定的資訊和功能。</span><span class="sxs-lookup"><span data-stu-id="576c0-123">Properties and methods exposed by the control pattern interfaces provide access to control-specific information and functionality.</span></span>

    <span data-ttu-id="576c0-124">消費者介面自動化的專案物件會以階層式樹狀結構中的用戶端提供，稱為消費者介面自動化樹狀目錄。</span><span class="sxs-lookup"><span data-stu-id="576c0-124">The UI Automation element objects are provided to clients in a hierarchical tree structure called the UI Automation tree.</span></span> <span data-ttu-id="576c0-125">用戶端會使用 [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) 介面所公開的方法來取得樹狀結構中 UI 元素的 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面，以及抓取其他介面，用來搜尋樹狀結構中符合一組特定準則的元素。</span><span class="sxs-lookup"><span data-stu-id="576c0-125">Clients use methods exposed by the [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface to retrieve [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interfaces for UI elements in the tree, and to retrieve other interfaces used to search the tree for elements that match a particular set of criteria.</span></span> <span data-ttu-id="576c0-126">如需詳細資訊，請參閱 [取得消費者介面自動化元素](uiauto-obtainingelements.md)。</span><span class="sxs-lookup"><span data-stu-id="576c0-126">For more information, see [Obtaining UI Automation Elements](uiauto-obtainingelements.md).</span></span>

    <span data-ttu-id="576c0-127">在抓取 UI 元素時，用戶端可以使用消費者介面自動化的快取功能來改善系統效能。</span><span class="sxs-lookup"><span data-stu-id="576c0-127">When retrieving UI elements, clients can improve system performance by using the caching capabilities of UI Automation.</span></span> <span data-ttu-id="576c0-128">快取可讓用戶端指定一組要與元素一起抓取的屬性和控制項模式。</span><span class="sxs-lookup"><span data-stu-id="576c0-128">Caching enables a client to specify a set of properties and control patterns to retrieve along with the element.</span></span> <span data-ttu-id="576c0-129">在單一進程調用中，消費者介面自動化會抓取元素和指定的屬性和控制項模式，然後將它們儲存在快取中。</span><span class="sxs-lookup"><span data-stu-id="576c0-129">In a single interprocess call, UI Automation retrieves the element and the specified properties and control patterns, and then stores them in the cache.</span></span> <span data-ttu-id="576c0-130">如果沒有快取，則需要個別的進程調用來取得每個屬性或控制項模式。</span><span class="sxs-lookup"><span data-stu-id="576c0-130">Without caching, a separate interprocess call is required to retrieve each property or control pattern.</span></span> <span data-ttu-id="576c0-131">如需詳細資訊，請參閱快取 [消費者介面自動化屬性和控制項模式](uiauto-cachingforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="576c0-131">For more information, see [Caching UI Automation Properties and Control Patterns](uiauto-cachingforclients.md).</span></span>

3.  <span data-ttu-id="576c0-132">**取出 UI 元素屬性，並叫用 UI 專案功能。**</span><span class="sxs-lookup"><span data-stu-id="576c0-132">**Retrieve UI element properties and invoke UI element functionality.**</span></span>

    <span data-ttu-id="576c0-133">用戶端會使用 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面來取出專案的屬性和控制項模式。</span><span class="sxs-lookup"><span data-stu-id="576c0-133">Clients use the [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface to retrieve an element's properties and control patterns.</span></span> <span data-ttu-id="576c0-134">介面包含每個屬性抓取方法的兩個版本—一個版本會從快取中抓取屬性，另一個版本會從提供者抓取屬性。</span><span class="sxs-lookup"><span data-stu-id="576c0-134">The interface includes two versions of each property retrieval method—one version retrieves the property from the cache, the other retrieves the property from the provider.</span></span> <span data-ttu-id="576c0-135">如需詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="576c0-135">For more information, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>

4.  <span data-ttu-id="576c0-136">**回應消費者介面自動化事件。**</span><span class="sxs-lookup"><span data-stu-id="576c0-136">**Respond to UI Automation events.**</span></span>

    <span data-ttu-id="576c0-137">消費者介面自動化提供者會引發事件，以通知用戶端變更或重要的出現位置。</span><span class="sxs-lookup"><span data-stu-id="576c0-137">UI Automation providers notify clients of changes or important occurrences in the UI by raising events.</span></span> <span data-ttu-id="576c0-138">用戶端必須判斷所需的事件，然後執行並註冊事件處理介面，以接收和處理這些事件。</span><span class="sxs-lookup"><span data-stu-id="576c0-138">Clients must determine which events they need, and then implement and register event handling interfaces to receive and process those events.</span></span> <span data-ttu-id="576c0-139">如需詳細資訊，請參閱 [訂閱消費者介面自動化事件](uiauto-eventsforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="576c0-139">For more information, see [Subscribing to UI Automation Events](uiauto-eventsforclients.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="576c0-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="576c0-140">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="576c0-141">**概念**</span><span class="sxs-lookup"><span data-stu-id="576c0-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="576c0-142">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="576c0-142">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="576c0-143">UI 自動化屬性概觀</span><span class="sxs-lookup"><span data-stu-id="576c0-143">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
</dt> <dt>

[<span data-ttu-id="576c0-144">UI 自動化事件概觀</span><span class="sxs-lookup"><span data-stu-id="576c0-144">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> </dl>

 

 