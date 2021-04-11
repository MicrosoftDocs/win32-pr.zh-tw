---
title: 選取控制項模式
description: 描述執行 ISelectionProvider 的方針和慣例，包括屬性、方法和事件的相關資訊。
ms.assetid: 9371e656-6f93-4a43-bd0c-c6977348b16a
keywords:
- 消費者介面自動化，執行選取控制項模式
- 消費者介面自動化，選取控制項模式
- 消費者介面自動化、ISelectionProvider
- ISelectionProvider
- 執行消費者介面自動化選取控制項模式
- 選取控制項模式
- 控制項模式，ISelectionProvider
- 控制項模式，執行消費者介面自動化選取專案
- 控制項模式，選取
- 介面，ISelectionProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad6950302373494f307c91c0aadaeab1db0132a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021507"
---
# <a name="selection-control-pattern"></a><span data-ttu-id="be690-113">選取控制項模式</span><span class="sxs-lookup"><span data-stu-id="be690-113">Selection Control Pattern</span></span>

<span data-ttu-id="be690-114">描述執行 [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)的方針和慣例，包括屬性、方法和事件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="be690-114">Describes guidelines and conventions for implementing [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider), including information about properties, methods, and events.</span></span> <span data-ttu-id="be690-115">**選取** 控制項模式用來支援控制項，這些控制項可作為可選取之子專案集合的容器。</span><span class="sxs-lookup"><span data-stu-id="be690-115">The **Selection** control pattern is used to support controls that act as containers for a collection of selectable child items.</span></span> <span data-ttu-id="be690-116">這個元素的子系必須執行 [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)。</span><span class="sxs-lookup"><span data-stu-id="be690-116">The children of this element must implement [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span></span>

<span data-ttu-id="be690-117">如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。</span><span class="sxs-lookup"><span data-stu-id="be690-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="be690-118">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="be690-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="be690-119">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="be690-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="be690-120">**ISelectionProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="be690-120">Required Members for **ISelectionProvider**</span></span>](#required-members-for-iselectionprovider)
-   [<span data-ttu-id="be690-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="be690-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="be690-122">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="be690-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="be690-123">在執行 **選取** 控制項模式時，請注意下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="be690-123">When implementing the **Selection** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="be690-124">執行 [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) 的控制項允許選取單一或多個子專案。</span><span class="sxs-lookup"><span data-stu-id="be690-124">Controls that implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) allow either single or multiple child items to be selected.</span></span> <span data-ttu-id="be690-125">例如，清單方塊、清單視圖和樹狀檢視支援多重選取，而下拉式方塊、滑杆和選項按鈕群組則支援單一選取。</span><span class="sxs-lookup"><span data-stu-id="be690-125">For example, list boxes, list views, and tree views support multiple selections, whereas combo boxes, sliders, and radio button groups support single selection.</span></span>
-   <span data-ttu-id="be690-126">具有最小值、最大值和連續範圍的控制項（例如媒體播放機的 **音量** 滑杆控制項）應該執行 [**system.windows.automation.provider.irangevalueprovider>**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) ，而不是 [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)。</span><span class="sxs-lookup"><span data-stu-id="be690-126">Controls that have a minimum, maximum, and continuous range, such as the **Volume** slider control of a media player, should implement [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) instead of [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span></span>
-   <span data-ttu-id="be690-127">單一選取控制項，可管理執行 [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)的子控制項，例如 Windows 的 [**顯示內容**] 對話方塊中的 [**螢幕解析度**] 滑杆，或 Microsoft Word (的 **色彩選擇器** 選取控制項，請參閱下列影像) ，應執行 [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider);其子系應同時執行 [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment)和 [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)。</span><span class="sxs-lookup"><span data-stu-id="be690-127">Single-selection controls that manage child controls that implement [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), such as the **Screen Resolution** slider in the **Display Properties** dialog for Windows, or the **Color Picker** selection control from Microsoft Word (see the following image), should implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); their children should implement both [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) and [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span></span>

    ![顯示色樣字串對應範例的影像](images/uia-valuepattern-colorpicker.jpg)

-   <span data-ttu-id="be690-129">功能表不支援 **選取** 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="be690-129">Menus do not support the **Selection** control pattern.</span></span> <span data-ttu-id="be690-130">如果您使用的功能表項目包括圖形和文字 (例如 Microsoft Outlook 的 [ **View** ] 功能表中的 [**預覽] 窗格** 專案) 而且需要傳達狀態，則您應該執行 [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)。</span><span class="sxs-lookup"><span data-stu-id="be690-130">If you are working with menu items that include both graphics and text (such as the **Preview Pane** items in the **View** menu in Microsoft Outlook) and need to convey state, you should implement [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).</span></span>

## <a name="required-members-for-iselectionprovider"></a><span data-ttu-id="be690-131">**ISelectionProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="be690-131">Required Members for **ISelectionProvider**</span></span>

<span data-ttu-id="be690-132">執行 [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) 介面需要下列屬性、方法和事件。</span><span class="sxs-lookup"><span data-stu-id="be690-132">The following properties, methods, and events are required for implementing the [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) interface.</span></span>



| <span data-ttu-id="be690-133">必要成員</span><span class="sxs-lookup"><span data-stu-id="be690-133">Required members</span></span>                                                                                | <span data-ttu-id="be690-134">成員類型</span><span class="sxs-lookup"><span data-stu-id="be690-134">Member type</span></span> | <span data-ttu-id="be690-135">備註</span><span class="sxs-lookup"><span data-stu-id="be690-135">Notes</span></span>                                                                       |
|-------------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="be690-136">**CanSelectMultiple**</span><span class="sxs-lookup"><span data-stu-id="be690-136">**CanSelectMultiple**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)                        | <span data-ttu-id="be690-137">屬性</span><span class="sxs-lookup"><span data-stu-id="be690-137">Property</span></span>    | <span data-ttu-id="be690-138">無</span><span class="sxs-lookup"><span data-stu-id="be690-138">None</span></span>                                                                        |
| [<span data-ttu-id="be690-139">**IsSelectionRequired**</span><span class="sxs-lookup"><span data-stu-id="be690-139">**IsSelectionRequired**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired)                    | <span data-ttu-id="be690-140">屬性</span><span class="sxs-lookup"><span data-stu-id="be690-140">Property</span></span>    | <span data-ttu-id="be690-141">無</span><span class="sxs-lookup"><span data-stu-id="be690-141">None</span></span>                                                                        |
| [<span data-ttu-id="be690-142">**GetSelection**</span><span class="sxs-lookup"><span data-stu-id="be690-142">**GetSelection**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection)                                  | <span data-ttu-id="be690-143">方法</span><span class="sxs-lookup"><span data-stu-id="be690-143">Method</span></span>      | <span data-ttu-id="be690-144">無</span><span class="sxs-lookup"><span data-stu-id="be690-144">None</span></span>                                                                        |
| [<span data-ttu-id="be690-145">**UIA \_ 選取專案 \_ InvalidatedEventId**</span><span class="sxs-lookup"><span data-stu-id="be690-145">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="be690-146">事件</span><span class="sxs-lookup"><span data-stu-id="be690-146">Event</span></span>       | <span data-ttu-id="be690-147">當容器中的選取範圍大幅變更時，引發此事件。</span><span class="sxs-lookup"><span data-stu-id="be690-147">Raise this event when a selection in a container has changed significantly.</span></span> |



 

<span data-ttu-id="be690-148">[**ISelectionProvider：： IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired)和 [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)屬性可以是動態的。</span><span class="sxs-lookup"><span data-stu-id="be690-148">The [**ISelectionProvider::IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) and [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) properties can be dynamic.</span></span> <span data-ttu-id="be690-149">例如，控制項的初始狀態可能沒有任何預設選取的專案，表示 **IsSelectionRequired** 為 false。</span><span class="sxs-lookup"><span data-stu-id="be690-149">For example, the initial state of a control might not have any items selected by default, indicating that **IsSelectionRequired** is false.</span></span> <span data-ttu-id="be690-150">不過，在選取項目之後，控制項就必須至少有一個項目一律保持為選取。</span><span class="sxs-lookup"><span data-stu-id="be690-150">However, after an item is selected, the control must always have at least one item selected.</span></span> <span data-ttu-id="be690-151">同樣地，在極少數的情況下，控制項可能會允許最初選取多個項目，但之後就只允許單一選取。</span><span class="sxs-lookup"><span data-stu-id="be690-151">Similarly, in rare cases, a control might allow multiple items to be selected on initialization, but subsequently allow only single selections to be made.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be690-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="be690-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be690-153">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="be690-153">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="be690-154">SelectionItem 控制項模式</span><span class="sxs-lookup"><span data-stu-id="be690-154">SelectionItem Control Pattern</span></span>](uiauto-implementingselectionitem.md)
</dt> <dt>

[<span data-ttu-id="be690-155">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="be690-155">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="be690-156">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="be690-156">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




