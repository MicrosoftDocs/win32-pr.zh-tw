---
title: LegacyIAccessible 控制項模式
description: 描述使用 ILegacyIAccessibleProvider 的方針和慣例，包括屬性、方法和事件的相關資訊。
ms.assetid: 4d66b9b8-ddbe-4bbc-b475-72dad1fe9393
keywords:
- 消費者介面自動化，執行 LegacyIAccessible 控制項模式
- 消費者介面自動化，LegacyIAccessible 控制項模式
- 消費者介面自動化、ILegacyIAccessibleProvider
- ILegacyIAccessibleProvider
- 執行消費者介面自動化 LegacyIAccessible 控制項模式
- LegacyIAccessible 控制項模式
- 控制項模式，ILegacyIAccessibleProvider
- 控制模式，消費者介面自動化執行 LegacyIAccessible
- 控制項模式，LegacyIAccessible
- 介面，ILegacyIAccessibleProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cffbd205b072f6f900ea5b5eb5a9f6ddfb5ddc5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674316"
---
# <a name="legacyiaccessible-control-pattern"></a><span data-ttu-id="203c9-113">LegacyIAccessible 控制項模式</span><span class="sxs-lookup"><span data-stu-id="203c9-113">LegacyIAccessible Control Pattern</span></span>

<span data-ttu-id="203c9-114">描述使用 [**ILegacyIAccessibleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider)的方針和慣例，包括屬性、方法和事件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="203c9-114">Describes guidelines and conventions for using [**ILegacyIAccessibleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider), including information about properties, methods, and events.</span></span> <span data-ttu-id="203c9-115">Microsoft 消費者介面自動化 Proxy 的 Microsoft Active Accessibility 支援 **LegacyIAccessible** 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="203c9-115">The **LegacyIAccessible** control pattern is supported by the Microsoft Active Accessibility to Microsoft UI Automation Proxy.</span></span>

<span data-ttu-id="203c9-116">應用程式和控制項提供者絕不會執行 [**ILegacyIAccessibleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider) 介面。</span><span class="sxs-lookup"><span data-stu-id="203c9-116">Application and control providers never implement the [**ILegacyIAccessibleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider) interface.</span></span>

<span data-ttu-id="203c9-117">**LegacyIAccessible** 控制項模式會公開 [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern)介面給消費者介面自動化用戶端，讓他們能夠存取特定 UI 元素的基礎 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)實作為基礎。</span><span class="sxs-lookup"><span data-stu-id="203c9-117">The **LegacyIAccessible** control pattern exposes the [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface to UI Automation clients, enabling them to access the underlying [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation for certain UI elements.</span></span> <span data-ttu-id="203c9-118">但是， **IUIAutomationLegacyIAccessiblePattern** 不支援已過時的方法，或與消費者介面自動化功能重複的方法。</span><span class="sxs-lookup"><span data-stu-id="203c9-118">However, **IUIAutomationLegacyIAccessiblePattern** does not support methods that are obsolete or that are redundant with the UI Automation features.</span></span>

<span data-ttu-id="203c9-119">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="203c9-119">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="203c9-120">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="203c9-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="203c9-121">**LegacyIAccessible** 控制項模式的成員</span><span class="sxs-lookup"><span data-stu-id="203c9-121">Members of the **LegacyIAccessible** Control Pattern</span></span>](#members-of-the-legacyiaccessible-control-pattern)
-   [<span data-ttu-id="203c9-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="203c9-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="203c9-123">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="203c9-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="203c9-124">沒有任何應用程式或控制項會執行 [**ILegacyIAccessibleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider)。</span><span class="sxs-lookup"><span data-stu-id="203c9-124">No application or control implements [**ILegacyIAccessibleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider).</span></span> <span data-ttu-id="203c9-125">消費者介面自動化架構會自動提供原生 Microsoft Active Accessibility 伺服器的提供者執行。</span><span class="sxs-lookup"><span data-stu-id="203c9-125">The UI Automation framework automatically supplies the provider implementation for a native Microsoft Active Accessibility server.</span></span>

<span data-ttu-id="203c9-126">**LegacyIAccessible** 控制項模式不適用於以消費者介面自動化為基礎的控制項。</span><span class="sxs-lookup"><span data-stu-id="203c9-126">The **LegacyIAccessible** control pattern is not available for controls based on UI Automation.</span></span>

## <a name="members-of-the-legacyiaccessible-control-pattern"></a><span data-ttu-id="203c9-127">**LegacyIAccessible** 控制項模式的成員</span><span class="sxs-lookup"><span data-stu-id="203c9-127">Members of the **LegacyIAccessible** Control Pattern</span></span>

<span data-ttu-id="203c9-128">下列屬性、方法和事件是 **LegacyIAccessible** 控制項模式的成員。</span><span class="sxs-lookup"><span data-stu-id="203c9-128">The following properties, methods, and events are members of the **LegacyIAccessible** control pattern.</span></span> <span data-ttu-id="203c9-129">附注適用于消費者介面自動化用戶端。</span><span class="sxs-lookup"><span data-stu-id="203c9-129">The notes are for UI Automation clients.</span></span>



| <span data-ttu-id="203c9-130">成員</span><span class="sxs-lookup"><span data-stu-id="203c9-130">Members</span></span>                                                                        | <span data-ttu-id="203c9-131">成員類型</span><span class="sxs-lookup"><span data-stu-id="203c9-131">Member type</span></span> | <span data-ttu-id="203c9-132">備註</span><span class="sxs-lookup"><span data-stu-id="203c9-132">Notes</span></span>                                                                                                                                |
|--------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="203c9-133">**ChildId**</span><span class="sxs-lookup"><span data-stu-id="203c9-133">**ChildId**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_childid)                   | <span data-ttu-id="203c9-134">屬性</span><span class="sxs-lookup"><span data-stu-id="203c9-134">Property</span></span>    | <span data-ttu-id="203c9-135">傳回非子物件的 **CHILDID \_ SELF** (0) 。</span><span class="sxs-lookup"><span data-stu-id="203c9-135">Returns **CHILDID\_SELF** (0) for a non-child object.</span></span>                                                                                |
| [<span data-ttu-id="203c9-136">**DefaultAction**</span><span class="sxs-lookup"><span data-stu-id="203c9-136">**DefaultAction**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_defaultaction)       | <span data-ttu-id="203c9-137">屬性</span><span class="sxs-lookup"><span data-stu-id="203c9-137">Property</span></span>    | <span data-ttu-id="203c9-138">無</span><span class="sxs-lookup"><span data-stu-id="203c9-138">None</span></span>                                                                                                                                 |
| [<span data-ttu-id="203c9-139">**描述**</span><span class="sxs-lookup"><span data-stu-id="203c9-139">**Description**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_description)           | <span data-ttu-id="203c9-140">屬性</span><span class="sxs-lookup"><span data-stu-id="203c9-140">Property</span></span>    | <span data-ttu-id="203c9-141">無</span><span class="sxs-lookup"><span data-stu-id="203c9-141">None</span></span>                                                                                                                                 |
| [<span data-ttu-id="203c9-142">**説明**</span><span class="sxs-lookup"><span data-stu-id="203c9-142">**Help**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_help)                         | <span data-ttu-id="203c9-143">屬性</span><span class="sxs-lookup"><span data-stu-id="203c9-143">Property</span></span>    | <span data-ttu-id="203c9-144">無</span><span class="sxs-lookup"><span data-stu-id="203c9-144">None</span></span>                                                                                                                                 |
| [<span data-ttu-id="203c9-145">**KeyboardShortcut**</span><span class="sxs-lookup"><span data-stu-id="203c9-145">**KeyboardShortcut**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_keyboardshortcut) | <span data-ttu-id="203c9-146">屬性</span><span class="sxs-lookup"><span data-stu-id="203c9-146">Property</span></span>    | <span data-ttu-id="203c9-147">無</span><span class="sxs-lookup"><span data-stu-id="203c9-147">None</span></span>                                                                                                                                 |
| [<span data-ttu-id="203c9-148">**Name**</span><span class="sxs-lookup"><span data-stu-id="203c9-148">**Name**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_name)                         | <span data-ttu-id="203c9-149">屬性</span><span class="sxs-lookup"><span data-stu-id="203c9-149">Property</span></span>    | <span data-ttu-id="203c9-150">無</span><span class="sxs-lookup"><span data-stu-id="203c9-150">None</span></span>                                                                                                                                 |
| [<span data-ttu-id="203c9-151">**角色**</span><span class="sxs-lookup"><span data-stu-id="203c9-151">**Role**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_role)                         | <span data-ttu-id="203c9-152">屬性</span><span class="sxs-lookup"><span data-stu-id="203c9-152">Property</span></span>    | <span data-ttu-id="203c9-153">使用 [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) 函式來取出當地語系化的字串。</span><span class="sxs-lookup"><span data-stu-id="203c9-153">Use the [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) function to retrieve localized string.</span></span>                                                    |
| [<span data-ttu-id="203c9-154">**GetSelection**</span><span class="sxs-lookup"><span data-stu-id="203c9-154">**GetSelection**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-getselection)         | <span data-ttu-id="203c9-155">方法</span><span class="sxs-lookup"><span data-stu-id="203c9-155">Method</span></span>      | <span data-ttu-id="203c9-156">捕獲 [**IUIAutomationElementArray**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="203c9-156">Retrieves an [**IUIAutomationElementArray**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray) interface pointer.</span></span>                                |
| [<span data-ttu-id="203c9-157">**State**</span><span class="sxs-lookup"><span data-stu-id="203c9-157">**State**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_state)                       | <span data-ttu-id="203c9-158">屬性</span><span class="sxs-lookup"><span data-stu-id="203c9-158">Property</span></span>    | <span data-ttu-id="203c9-159">使用 [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) 函式來取出當地語系化的字串。</span><span class="sxs-lookup"><span data-stu-id="203c9-159">Use the [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) function to retrieve localized string.</span></span>                                                  |
| [<span data-ttu-id="203c9-160">**值**</span><span class="sxs-lookup"><span data-stu-id="203c9-160">**Value**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_value)                       | <span data-ttu-id="203c9-161">屬性</span><span class="sxs-lookup"><span data-stu-id="203c9-161">Property</span></span>    | <span data-ttu-id="203c9-162">無</span><span class="sxs-lookup"><span data-stu-id="203c9-162">None</span></span>                                                                                                                                 |
| [<span data-ttu-id="203c9-163">**DoDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="203c9-163">**DoDefaultAction**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-dodefaultaction)   | <span data-ttu-id="203c9-164">方法</span><span class="sxs-lookup"><span data-stu-id="203c9-164">Method</span></span>      | <span data-ttu-id="203c9-165">無</span><span class="sxs-lookup"><span data-stu-id="203c9-165">None</span></span>                                                                                                                                 |
| [<span data-ttu-id="203c9-166">**GetIAccessible**</span><span class="sxs-lookup"><span data-stu-id="203c9-166">**GetIAccessible**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-getiaccessible)     | <span data-ttu-id="203c9-167">方法</span><span class="sxs-lookup"><span data-stu-id="203c9-167">Method</span></span>      | <span data-ttu-id="203c9-168">無</span><span class="sxs-lookup"><span data-stu-id="203c9-168">None</span></span>                                                                                                                                 |
| [<span data-ttu-id="203c9-169">**選擇**</span><span class="sxs-lookup"><span data-stu-id="203c9-169">**Select**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-select)                     | <span data-ttu-id="203c9-170">方法</span><span class="sxs-lookup"><span data-stu-id="203c9-170">Method</span></span>      | <span data-ttu-id="203c9-171">選取旗標是 Microsoft Active Accessibility 的 **SELFLAG** 值。</span><span class="sxs-lookup"><span data-stu-id="203c9-171">The selection flag is a Microsoft Active Accessibility **SELFLAG** value.</span></span> <span data-ttu-id="203c9-172">如需詳細資訊，請參閱 [SELFLAG 常數](selflag.md)。</span><span class="sxs-lookup"><span data-stu-id="203c9-172">For more information, see [SELFLAG Constants](selflag.md).</span></span> |
| [<span data-ttu-id="203c9-173">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="203c9-173">**SetValue**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-setvalue)                 | <span data-ttu-id="203c9-174">方法</span><span class="sxs-lookup"><span data-stu-id="203c9-174">Method</span></span>      | <span data-ttu-id="203c9-175">無</span><span class="sxs-lookup"><span data-stu-id="203c9-175">None</span></span>                                                                                                                                 |



 

<span data-ttu-id="203c9-176">此控制項模式沒有任何相關聯的事件。</span><span class="sxs-lookup"><span data-stu-id="203c9-176">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="203c9-177">相關主題</span><span class="sxs-lookup"><span data-stu-id="203c9-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="203c9-178">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="203c9-178">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="203c9-179">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="203c9-179">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="203c9-180">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="203c9-180">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




