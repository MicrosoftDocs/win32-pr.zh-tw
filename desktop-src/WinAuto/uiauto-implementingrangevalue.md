---
title: RangeValue 控制項模式
description: 描述執行 System.windows.automation.provider.irangevalueprovider> 的方針和慣例，包括屬性和方法的相關資訊。 RangeValue 控制項模式用來支援可以設定為範圍內值的控制項。
ms.assetid: e5c1104c-4b20-4fdd-bd12-dfc27cb73ac5
keywords:
- 消費者介面自動化，執行 RangeValue 控制項模式
- 消費者介面自動化，RangeValue 控制項模式
- 消費者介面自動化、System.windows.automation.provider.irangevalueprovider>
- IRangeValueProvider
- 執行消費者介面自動化 RangeValue 控制項模式
- RangeValue 控制項模式
- 控制項模式，System.windows.automation.provider.irangevalueprovider>
- 控制模式，消費者介面自動化執行 RangeValue
- 控制項模式，RangeValue
- 介面，System.windows.automation.provider.irangevalueprovider>
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf426069ad88ad272fd78c521a220ba7ccf72275
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968435"
---
# <a name="rangevalue-control-pattern"></a><span data-ttu-id="f9886-114">RangeValue 控制項模式</span><span class="sxs-lookup"><span data-stu-id="f9886-114">RangeValue Control Pattern</span></span>

<span data-ttu-id="f9886-115">描述執行 [**system.windows.automation.provider.irangevalueprovider>**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)的方針和慣例，包括屬性和方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f9886-115">Describes guidelines and conventions for implementing [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider), including information about properties and methods.</span></span> <span data-ttu-id="f9886-116">**RangeValue** 控制項模式用來支援可以設定為範圍內值的控制項。</span><span class="sxs-lookup"><span data-stu-id="f9886-116">The **RangeValue** control pattern is used to support controls that can be set to a value within a range.</span></span>

<span data-ttu-id="f9886-117">如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。</span><span class="sxs-lookup"><span data-stu-id="f9886-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="f9886-118">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="f9886-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f9886-119">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="f9886-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="f9886-120">**System.windows.automation.provider.irangevalueprovider>** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="f9886-120">Required Members for **IRangeValueProvider**</span></span>](#required-members-for-irangevalueprovider)
-   [<span data-ttu-id="f9886-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="f9886-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="f9886-122">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="f9886-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="f9886-123">在執行 **RangeValue** 控制項模式時，請注意下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="f9886-123">When implementing the **RangeValue** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="f9886-124">控制項可以根據地區設定或使用者偏好設定，重新劃分所支援屬性的刻度。</span><span class="sxs-lookup"><span data-stu-id="f9886-124">Controls allow recalibration of their supported properties based upon locale or user preference.</span></span> <span data-ttu-id="f9886-125">例如，溫度計控制項可以設為顯示華氏或攝氏溫度。</span><span class="sxs-lookup"><span data-stu-id="f9886-125">An example of this is a thermometer control that can be set to display the temperature in Fahrenheit or Celsius.</span></span>
-   <span data-ttu-id="f9886-126">範圍值不明確的控制項 (如進度列或滑桿) 應將這些值正規化。</span><span class="sxs-lookup"><span data-stu-id="f9886-126">Controls that have ambiguous range values, such as progress bars or sliders, should have those values normalized.</span></span>

## <a name="required-members-for-irangevalueprovider"></a><span data-ttu-id="f9886-127">**System.windows.automation.provider.irangevalueprovider>** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="f9886-127">Required Members for **IRangeValueProvider**</span></span>

<span data-ttu-id="f9886-128">執行 [**system.windows.automation.provider.irangevalueprovider>**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) 介面需要下列屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="f9886-128">The following properties and methods are required for implementing the [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) interface.</span></span>



| <span data-ttu-id="f9886-129">必要成員</span><span class="sxs-lookup"><span data-stu-id="f9886-129">Required members</span></span>                                              | <span data-ttu-id="f9886-130">成員類型</span><span class="sxs-lookup"><span data-stu-id="f9886-130">Member type</span></span> | <span data-ttu-id="f9886-131">備註</span><span class="sxs-lookup"><span data-stu-id="f9886-131">Notes</span></span> |
|---------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="f9886-132">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="f9886-132">**IsReadOnly**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_isreadonly)   | <span data-ttu-id="f9886-133">屬性</span><span class="sxs-lookup"><span data-stu-id="f9886-133">Property</span></span>    | <span data-ttu-id="f9886-134">無</span><span class="sxs-lookup"><span data-stu-id="f9886-134">None</span></span>  |
| [<span data-ttu-id="f9886-135">**值**</span><span class="sxs-lookup"><span data-stu-id="f9886-135">**Value**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value)             | <span data-ttu-id="f9886-136">屬性</span><span class="sxs-lookup"><span data-stu-id="f9886-136">Property</span></span>    | <span data-ttu-id="f9886-137">無</span><span class="sxs-lookup"><span data-stu-id="f9886-137">None</span></span>  |
| [<span data-ttu-id="f9886-138">**LargeChange**</span><span class="sxs-lookup"><span data-stu-id="f9886-138">**LargeChange**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | <span data-ttu-id="f9886-139">屬性</span><span class="sxs-lookup"><span data-stu-id="f9886-139">Property</span></span>    | <span data-ttu-id="f9886-140">無</span><span class="sxs-lookup"><span data-stu-id="f9886-140">None</span></span>  |
| [<span data-ttu-id="f9886-141">**SmallChange**</span><span class="sxs-lookup"><span data-stu-id="f9886-141">**SmallChange**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | <span data-ttu-id="f9886-142">屬性</span><span class="sxs-lookup"><span data-stu-id="f9886-142">Property</span></span>    | <span data-ttu-id="f9886-143">無</span><span class="sxs-lookup"><span data-stu-id="f9886-143">None</span></span>  |
| [<span data-ttu-id="f9886-144">**最大**</span><span class="sxs-lookup"><span data-stu-id="f9886-144">**Maximum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | <span data-ttu-id="f9886-145">屬性</span><span class="sxs-lookup"><span data-stu-id="f9886-145">Property</span></span>    | <span data-ttu-id="f9886-146">無</span><span class="sxs-lookup"><span data-stu-id="f9886-146">None</span></span>  |
| [<span data-ttu-id="f9886-147">**最小值**</span><span class="sxs-lookup"><span data-stu-id="f9886-147">**Minimum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | <span data-ttu-id="f9886-148">屬性</span><span class="sxs-lookup"><span data-stu-id="f9886-148">Property</span></span>    | <span data-ttu-id="f9886-149">無</span><span class="sxs-lookup"><span data-stu-id="f9886-149">None</span></span>  |
| [<span data-ttu-id="f9886-150">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="f9886-150">**SetValue**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-setvalue)       | <span data-ttu-id="f9886-151">方法</span><span class="sxs-lookup"><span data-stu-id="f9886-151">Method</span></span>      | <span data-ttu-id="f9886-152">無</span><span class="sxs-lookup"><span data-stu-id="f9886-152">None</span></span>  |



 

<span data-ttu-id="f9886-153">此控制項模式沒有任何相關聯的事件。</span><span class="sxs-lookup"><span data-stu-id="f9886-153">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9886-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="f9886-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9886-155">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="f9886-155">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="f9886-156">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="f9886-156">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="f9886-157">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="f9886-157">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




