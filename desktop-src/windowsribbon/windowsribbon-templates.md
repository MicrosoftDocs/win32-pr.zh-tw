---
title: 透過大小定義和調整原則自訂功能區
description: 功能區命令列中裝載的控制項受限於 Windows 功能區架構所強制執行的版面配置規則，並根據預設行為和版面配置範本的組合 (在功能區標記中宣告的架構定義和自訂) 。 這些規則會定義功能區架構的調適型配置行為，此行為會影響命令列中的控制項在執行時間如何適應各種功能區大小。
ms.assetid: b5869394-3fa9-4817-add9-54487434fc4f
keywords:
- Windows 功能區，自訂
- 功能區，自訂
- Windows 功能區，SizeDefinition 範本
- 功能區、SizeDefinition 範本
- Windows 功能區，自訂範本
- 功能區、自訂範本
- 自訂 Windows 功能區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b12618f88576cddeff119534215e501216193c3
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/30/2020
ms.locfileid: "104558315"
---
# <a name="customizing-a-ribbon-through-size-definitions-and-scaling-policies"></a><span data-ttu-id="11f5c-111">透過大小定義和調整原則自訂功能區</span><span class="sxs-lookup"><span data-stu-id="11f5c-111">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>

<span data-ttu-id="11f5c-112">功能區命令列中裝載的控制項受限於 Windows 功能區架構所強制執行的版面配置規則，並根據預設行為和版面配置範本的組合 (在功能區標記中宣告的架構定義和自訂) 。</span><span class="sxs-lookup"><span data-stu-id="11f5c-112">Controls hosted in the ribbon Command bar are subject to layout rules that are enforced by the Windows Ribbon framework and based on a combination of default behaviors and layout templates (both framework-defined and custom) as declared in the Ribbon markup.</span></span> <span data-ttu-id="11f5c-113">這些規則會定義功能區架構的調適型配置行為，此行為會影響命令列中的控制項在執行時間如何適應各種功能區大小。</span><span class="sxs-lookup"><span data-stu-id="11f5c-113">These rules define the adaptive layout behaviors of the Ribbon framework that influence how controls in the Command bar adapt to various ribbon sizes at run time.</span></span>

-   [<span data-ttu-id="11f5c-114">簡介</span><span class="sxs-lookup"><span data-stu-id="11f5c-114">Introduction</span></span>](#introduction)
    -   [<span data-ttu-id="11f5c-115">功能區 SizeDefinition 範本</span><span class="sxs-lookup"><span data-stu-id="11f5c-115">Ribbon SizeDefinition Templates</span></span>](#customizing-a-ribbon-through-size-definitions-and-scaling-policies)
    -   [<span data-ttu-id="11f5c-116">自訂範本</span><span class="sxs-lookup"><span data-stu-id="11f5c-116">Custom Templates</span></span>](#custom-templates)
-   [<span data-ttu-id="11f5c-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="11f5c-117">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="11f5c-118">簡介</span><span class="sxs-lookup"><span data-stu-id="11f5c-118">Introduction</span></span>

<span data-ttu-id="11f5c-119">自訂版面配置是由功能區架構所定義，因此功能區 UI 中的所有控制項都能根據執行時間的功能區大小變更，動態調整其組織、大小、格式和相對比例。</span><span class="sxs-lookup"><span data-stu-id="11f5c-119">Adaptive layout, as defined by the Ribbon framework, is the ability of all controls within the ribbon UI to dynamically adjust their organization, size, format, and relative scale based on changes to the size of the ribbon at run time.</span></span>

<span data-ttu-id="11f5c-120">架構會透過一組專門用來指定和自訂各種版面配置行為的標記元素來公開自訂版面配置功能。</span><span class="sxs-lookup"><span data-stu-id="11f5c-120">The framework exposes adaptive layout functionality through a set of markup elements that are dedicated to specifying and customizing various layout behaviors.</span></span> <span data-ttu-id="11f5c-121">範本的集合（稱為 [**SizeDefinitions**](windowsribbon-element-sizedefinition.md)）是由架構所定義，每個範本都支援各種控制項和版面配置案例。</span><span class="sxs-lookup"><span data-stu-id="11f5c-121">A collection of templates, called [**SizeDefinitions**](windowsribbon-element-sizedefinition.md), is defined by the framework, each of which support various control and layout scenarios.</span></span> <span data-ttu-id="11f5c-122">但是，如果預先定義的範本不提供應用程式所需的 UI 體驗或版面配置，架構也支援自訂範本。</span><span class="sxs-lookup"><span data-stu-id="11f5c-122">However, the framework also supports custom templates should the predefined templates not provide the UI experience or layouts required by an application.</span></span>

<span data-ttu-id="11f5c-123">若要在特定功能區大小以慣用的版面配置顯示控制項，預先定義的範本和自訂範本會與 [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) 元素一起使用。</span><span class="sxs-lookup"><span data-stu-id="11f5c-123">To display controls in a preferred layout at a particular ribbon size, both predefined templates and custom templates work in conjunction with the [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) element.</span></span> <span data-ttu-id="11f5c-124">這個元素包含大小喜好設定的資訊清單，在轉譯功能區時，架構會使用這些喜好設定做為指南。</span><span class="sxs-lookup"><span data-stu-id="11f5c-124">This element contains a manifest of size preferences that the framework uses as a guide when rendering the ribbon.</span></span>

> [!Note]  
> <span data-ttu-id="11f5c-125">功能區架構會根據一組內建的啟發學習法提供預設的版面配置行為，並在執行時間呈現控制項，而不需要預先定義的 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 範本。</span><span class="sxs-lookup"><span data-stu-id="11f5c-125">The Ribbon framework provides default layout behaviors based on a set of built-in heuristics for the organization and presentation of controls at run time without the need for the predefined [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span> <span data-ttu-id="11f5c-126">不過，這項功能僅適用于原型設計用途。</span><span class="sxs-lookup"><span data-stu-id="11f5c-126">However, this capability is intended for prototyping purposes only.</span></span>

 

### <a name="ribbon-sizedefinition-templates"></a><span data-ttu-id="11f5c-127">功能區 SizeDefinition 範本</span><span class="sxs-lookup"><span data-stu-id="11f5c-127">Ribbon SizeDefinition Templates</span></span>

<span data-ttu-id="11f5c-128">功能區架構會提供一組完整的 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 範本，這些範本會指定功能區控制項 [群組](windowsribbon-controls-group.md) 的大小和版面配置行為。</span><span class="sxs-lookup"><span data-stu-id="11f5c-128">The Ribbon framework provides a comprehensive set of [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates that specify size and layout behavior for a [Group](windowsribbon-controls-group.md) of Ribbon controls.</span></span> <span data-ttu-id="11f5c-129">這些範本涵蓋了在功能區應用程式中組織控制項的最常見案例。</span><span class="sxs-lookup"><span data-stu-id="11f5c-129">These templates cover most common scenarios for organizing controls in a Ribbon application.</span></span>

<span data-ttu-id="11f5c-130">為了在功能區應用程式之間強制執行一致的使用者體驗，每個 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 範本會對其支援的控制項或控制項系列施加限制。</span><span class="sxs-lookup"><span data-stu-id="11f5c-130">To enforce a consistent user experience across Ribbon applications, each [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template imposes restrictions on the controls or the family of controls it supports.</span></span>

<span data-ttu-id="11f5c-131">例如，按鈕系列的控制項包括：</span><span class="sxs-lookup"><span data-stu-id="11f5c-131">For example, the button family of controls includes:</span></span>

-   [<span data-ttu-id="11f5c-132">按鈕</span><span class="sxs-lookup"><span data-stu-id="11f5c-132">Button</span></span>](windowsribbon-controls-button.md)
-   [<span data-ttu-id="11f5c-133">切換按鈕</span><span class="sxs-lookup"><span data-stu-id="11f5c-133">Toggle Button</span></span>](windowsribbon-controls-togglebutton.md)
-   [<span data-ttu-id="11f5c-134">下拉式按鈕</span><span class="sxs-lookup"><span data-stu-id="11f5c-134">Drop-Down Button</span></span>](windowsribbon-controls-dropdownbutton.md)
-   [<span data-ttu-id="11f5c-135">分割按鈕</span><span class="sxs-lookup"><span data-stu-id="11f5c-135">Split Button</span></span>](windowsribbon-controls-splitbutton.md)
-   [<span data-ttu-id="11f5c-136">下拉式圖庫</span><span class="sxs-lookup"><span data-stu-id="11f5c-136">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)
-   [<span data-ttu-id="11f5c-137">分割按鈕資源庫</span><span class="sxs-lookup"><span data-stu-id="11f5c-137">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)
-   [<span data-ttu-id="11f5c-138">下拉式色彩選擇器</span><span class="sxs-lookup"><span data-stu-id="11f5c-138">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md)

<span data-ttu-id="11f5c-139">控制項的輸入系列包括：</span><span class="sxs-lookup"><span data-stu-id="11f5c-139">While the input family of controls includes:</span></span>

-   [<span data-ttu-id="11f5c-140">下拉式方塊</span><span class="sxs-lookup"><span data-stu-id="11f5c-140">Combo Box</span></span>](windowsribbon-controls-combobox.md)
-   [<span data-ttu-id="11f5c-141">Spinner</span><span class="sxs-lookup"><span data-stu-id="11f5c-141">Spinner</span></span>](windowsribbon-controls-spinner.md)

<span data-ttu-id="11f5c-142">[核取方塊](windowsribbon-controls-checkbox.md) 和 [功能區圖庫](windowsribbon-controls-inribbongallery.md) 都不屬於按鈕系列或輸入系列。</span><span class="sxs-lookup"><span data-stu-id="11f5c-142">[Check Box](windowsribbon-controls-checkbox.md) and [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) do not belong to either the button family or the input family.</span></span> <span data-ttu-id="11f5c-143">這兩個控制項只能用在 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 範本中明確指出的位置。</span><span class="sxs-lookup"><span data-stu-id="11f5c-143">These two controls can be used only where explicitly indicated in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template.</span></span>

<span data-ttu-id="11f5c-144">以下是 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 範本的清單，其中包含每個範本所允許的版面配置和控制項的描述。</span><span class="sxs-lookup"><span data-stu-id="11f5c-144">The following is a list of the [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates with a description of the layout and controls allowed by each template.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="11f5c-145">如果在標記中宣告的控制項無法完全對應至關聯範本中定義的控制項類型、順序和數量，則[標記編譯器](windowsribbon-intentcl.md)會記錄[驗證錯誤](windowsribbon-compilationerrors.md)，並終止編譯。</span><span class="sxs-lookup"><span data-stu-id="11f5c-145">If the controls declared in markup do not map exactly to control type, order, and quantity defined in the associated template, a [validation error](windowsribbon-compilationerrors.md) is logged by the [markup compiler](windowsribbon-intentcl.md) and compilation is terminated.</span></span>

 



<span data-ttu-id="11f5c-146">OneButton</span><span class="sxs-lookup"><span data-stu-id="11f5c-146">OneButton</span></span>

<span data-ttu-id="11f5c-147">一個按鈕系列控制項。</span><span class="sxs-lookup"><span data-stu-id="11f5c-147">One button-family control.</span></span><br/> <span data-ttu-id="11f5c-148">僅支援大型群組大小。</span><span class="sxs-lookup"><span data-stu-id="11f5c-148">Only Large group size is supported.</span></span><br/>

![onebutton sizedefinition 範本的圖片。](images/overviews/sizedefinition-onebutton.png)

<span data-ttu-id="11f5c-150">TwoButtons</span><span class="sxs-lookup"><span data-stu-id="11f5c-150">TwoButtons</span></span>

<span data-ttu-id="11f5c-151">兩個按鈕系列控制項。</span><span class="sxs-lookup"><span data-stu-id="11f5c-151">Two button-family controls.</span></span><br/> <span data-ttu-id="11f5c-152">僅支援大型和中型群組的大小。</span><span class="sxs-lookup"><span data-stu-id="11f5c-152">Only Large and Medium group sizes are supported.</span></span><br/>

![twobuttons 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-twobuttons-large.png)

![twobuttons medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-twobuttons-medium.png)

<span data-ttu-id="11f5c-155">ThreeButtons</span><span class="sxs-lookup"><span data-stu-id="11f5c-155">ThreeButtons</span></span>

<span data-ttu-id="11f5c-156">三個按鈕系列控制項。</span><span class="sxs-lookup"><span data-stu-id="11f5c-156">Three button-family controls.</span></span><br/> <span data-ttu-id="11f5c-157">僅支援大型和中型群組的大小。</span><span class="sxs-lookup"><span data-stu-id="11f5c-157">Only Large and Medium group sizes are supported.</span></span><br/>

![threebuttons 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-threebuttons-large.png)

![threebuttons medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-threebuttons-medium.png)

<span data-ttu-id="11f5c-160">ThreeButtons-OneBigAndTwoSmall</span><span class="sxs-lookup"><span data-stu-id="11f5c-160">ThreeButtons-OneBigAndTwoSmall</span></span>

<span data-ttu-id="11f5c-161">三個按鈕系列控制項。</span><span class="sxs-lookup"><span data-stu-id="11f5c-161">Three button-family controls.</span></span><br/> <span data-ttu-id="11f5c-162">第一個按鈕會以三種大小醒目顯示。</span><span class="sxs-lookup"><span data-stu-id="11f5c-162">The first button is presented prominently in all three sizes.</span></span><br/>

![threebuttons-onebigandtwosmall 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-large.png)

![threebuttons-onebigandtwosmall medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-medium.png)

![threebuttons-onebigandtwosmall small sizedefinition 範本的圖片。](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-small.png)

<span data-ttu-id="11f5c-166">ThreeButtonsAndOneCheckBox</span><span class="sxs-lookup"><span data-stu-id="11f5c-166">ThreeButtonsAndOneCheckBox</span></span>

<span data-ttu-id="11f5c-167">三個按鈕系列控制項，伴隨著單一核取方塊控制項。</span><span class="sxs-lookup"><span data-stu-id="11f5c-167">Three button-family controls accompanied by a single CheckBox control.</span></span><br/> <span data-ttu-id="11f5c-168">僅支援大型和中型群組的大小。</span><span class="sxs-lookup"><span data-stu-id="11f5c-168">Only Large and Medium group sizes are supported.</span></span><br/>

![threebuttonsandonecheckbox 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-threebuttonsandonecheckbox-large.png)

![threebuttonsandonecheckbox medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-threebuttonsandonecheckbox-medium.png)

<span data-ttu-id="11f5c-171">FourButtons</span><span class="sxs-lookup"><span data-stu-id="11f5c-171">FourButtons</span></span>

<span data-ttu-id="11f5c-172">四個按鈕系列控制項。</span><span class="sxs-lookup"><span data-stu-id="11f5c-172">Four button-family controls.</span></span><br/>

![fourbuttons 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-fourbuttons-large.png)

![fourbuttons medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-fourbuttons-medium.png)

![fourbuttons small sizedefinition 範本的圖片。](images/overviews/sizedefinition-fourbuttons-small.png)

<span data-ttu-id="11f5c-176">FiveButtons</span><span class="sxs-lookup"><span data-stu-id="11f5c-176">FiveButtons</span></span>

<span data-ttu-id="11f5c-177">五個按鈕系列控制項。</span><span class="sxs-lookup"><span data-stu-id="11f5c-177">Five button-family controls.</span></span><br/>

![fivebuttons 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-fivebuttons-large.png)

![fivebuttons medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-fivebuttons-medium.png)

![fivebuttons small sizedefinition 範本的圖片。](images/overviews/sizedefinition-fivebuttons-small.png)

<span data-ttu-id="11f5c-181">FiveOrSixButtons</span><span class="sxs-lookup"><span data-stu-id="11f5c-181">FiveOrSixButtons</span></span>

<span data-ttu-id="11f5c-182">五個按鈕系列控制項和選擇性的第六個按鈕。</span><span class="sxs-lookup"><span data-stu-id="11f5c-182">Five button-family controls and an optional sixth button.</span></span><br/>

![fiveorsixbuttons 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-fiveorsixbuttons-large.png)

![fiveorsixbuttons medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-fiveorsixbuttons-medium.png)

![fiveorsixbuttons small sizedefinition 範本的圖片。](images/overviews/sizedefinition-fiveorsixbuttons-small.png)

<span data-ttu-id="11f5c-186">SixButtons</span><span class="sxs-lookup"><span data-stu-id="11f5c-186">SixButtons</span></span>

<span data-ttu-id="11f5c-187">六個按鈕系列控制項。</span><span class="sxs-lookup"><span data-stu-id="11f5c-187">Six button-family controls.</span></span><br/>

![sixbuttons 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-sixbuttons-large.png)

![sixbuttons medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-sixbuttons-medium.png)

![sixbuttons small sizedefinition 範本的圖片。](images/overviews/sizedefinition-sixbuttons-small.png)

<span data-ttu-id="11f5c-191">SixButtons-TwoColumns</span><span class="sxs-lookup"><span data-stu-id="11f5c-191">SixButtons-TwoColumns</span></span>

<span data-ttu-id="11f5c-192">六個按鈕系列控制項 (替代的簡報) 。</span><span class="sxs-lookup"><span data-stu-id="11f5c-192">Six button-family controls (alternate presentation).</span></span><br/>

![sixbuttons-twocolumns 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-sixbuttons-twocolumns-large.png)

![sixbuttons-twocolumns 中型 sizedefinition 範本。](images/overviews/sizedefinition-sixbuttons-twocolumns-medium.png)

![sixbuttons-twocolumns small sizedefinition 範本的圖片。](images/overviews/sizedefinition-sixbuttons-twocolumns-small.png)

<span data-ttu-id="11f5c-196">SevenButtons</span><span class="sxs-lookup"><span data-stu-id="11f5c-196">SevenButtons</span></span>

<span data-ttu-id="11f5c-197">七個按鈕系列控制項。</span><span class="sxs-lookup"><span data-stu-id="11f5c-197">Seven button-family controls.</span></span><br/>

![sevenbuttons 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-sevenbuttons-large.png)

![sevenbuttons mediumsizedefinition 範本的圖片。](images/overviews/sizedefinition-sevenbuttons-medium.png)

![sevenbuttons small sizedefinition 範本的圖片。](images/overviews/sizedefinition-sevenbuttons-small.png)

<span data-ttu-id="11f5c-201">EightButtons</span><span class="sxs-lookup"><span data-stu-id="11f5c-201">EightButtons</span></span>

<span data-ttu-id="11f5c-202">八個按鈕系列控制項。</span><span class="sxs-lookup"><span data-stu-id="11f5c-202">Eight button-family controls.</span></span><br/>

![eightbuttons-lastthreesmall 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-eightbuttons-lastthreesmall-large.png)

![eightbuttons-lastthreesmall medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-eightbuttons-lastthreesmall-medium.png)

![eightbuttons-lastthreesmall small sizedefinition 範本的圖片。](images/overviews/sizedefinition-eightbuttons-lastthreesmall-small.png)

<span data-ttu-id="11f5c-206">EightButtons-LastThreeSmall</span><span class="sxs-lookup"><span data-stu-id="11f5c-206">EightButtons-LastThreeSmall</span></span>

<span data-ttu-id="11f5c-207">八個按鈕系列控制項 (替代的簡報) 。</span><span class="sxs-lookup"><span data-stu-id="11f5c-207">Eight button-family controls (alternate presentation).</span></span><br/>

> [!Note]  
> <span data-ttu-id="11f5c-208">所有以此範本宣告的控制項元素都必須包含在兩個 [**ControlGroup**](windowsribbon-element-controlgroup.md) 元素中：一個用於前五個元素，另一個用於最後三個元素。</span><span class="sxs-lookup"><span data-stu-id="11f5c-208">All control elements declared with this template must be contained in two [**ControlGroup**](windowsribbon-element-controlgroup.md) elements: one for the first five elements and one for the last three elements.</span></span>

<br/> <span data-ttu-id="11f5c-209">下列範例示範此範本所需的標記。</span><span class="sxs-lookup"><span data-stu-id="11f5c-209">The following example demonstrates the markup required for this template.</span></span><br/>

```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="EightButtons-LastThreeSmall">
  <ControlGroup>
    <Button CommandName="cmdSDButton1" />
    <Button CommandName="cmdSDButton2" />
    <Button CommandName="cmdSDButton3" />
    <Button CommandName="cmdSDButton4" />
    <Button CommandName="cmdSDButton5" />
  </ControlGroup>
  <ControlGroup>
    <Button CommandName="cmdSDButton6" />
    <Button CommandName="cmdSDButton7" />
    <Button CommandName="cmdSDButton8" />
  </ControlGroup>
</Group>
```



![eightbuttons 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-eightbuttons-large.png)

![eightbuttons medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-eightbuttons-medium.png)

![eightbuttons small sizedefinition 範本的圖片。](images/overviews/sizedefinition-eightbuttons-small.png)

<span data-ttu-id="11f5c-213">NineButtons</span><span class="sxs-lookup"><span data-stu-id="11f5c-213">NineButtons</span></span>

<span data-ttu-id="11f5c-214">九個按鈕系列控制項。</span><span class="sxs-lookup"><span data-stu-id="11f5c-214">Nine button-family controls.</span></span>

![ninebuttons 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-ninebuttons-large.png)

![ninebuttons medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-ninebuttons-medium.png)

![ninebuttons small sizedefinition 範本的圖片。](images/overviews/sizedefinition-ninebuttons-small.png)

<span data-ttu-id="11f5c-218">TenButtons</span><span class="sxs-lookup"><span data-stu-id="11f5c-218">TenButtons</span></span>

<span data-ttu-id="11f5c-219">十個按鈕系列控制項。</span><span class="sxs-lookup"><span data-stu-id="11f5c-219">Ten button-family controls.</span></span>

![tenbuttons 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-tenbuttons-large.png)

![tenbuttons medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-tenbuttons-medium.png)

![tenbuttons small sizedefinition 範本的圖片。](images/overviews/sizedefinition-tenbuttons-small.png)

<span data-ttu-id="11f5c-223">ElevenButtons</span><span class="sxs-lookup"><span data-stu-id="11f5c-223">ElevenButtons</span></span>

<span data-ttu-id="11f5c-224">11個按鈕系列控制項。</span><span class="sxs-lookup"><span data-stu-id="11f5c-224">Eleven button-family controls.</span></span>

![elevenbuttons 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-elevenbuttons-large.png)

![elevenbuttons medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-elevenbuttons-medium.png)

![elevenbuttons small sizedefinition 範本的圖片。](images/overviews/sizedefinition-elevenbuttons-small.png)

<span data-ttu-id="11f5c-228">OneFontControl</span><span class="sxs-lookup"><span data-stu-id="11f5c-228">OneFontControl</span></span>

<span data-ttu-id="11f5c-229">其中一個 [**FontControl**](windowsribbon-element-fontcontrol.md)。</span><span class="sxs-lookup"><span data-stu-id="11f5c-229">One [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

<span data-ttu-id="11f5c-230">僅支援大型和中型群組的大小。</span><span class="sxs-lookup"><span data-stu-id="11f5c-230">Only Large and Medium group sizes are supported.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="11f5c-231">架構不支援在自訂範本定義中包含 [**FontControl**](windowsribbon-element-fontcontrol.md) 。</span><span class="sxs-lookup"><span data-stu-id="11f5c-231">Including a [**FontControl**](windowsribbon-element-fontcontrol.md) within a custom template definition is not supported by the framework.</span></span>

 

![onefontcontrol 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-onefontcontrol-large.png)

![onefontcontrol medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-onefontcontrol-medium.png)

<span data-ttu-id="11f5c-234">OneInRibbonGallery</span><span class="sxs-lookup"><span data-stu-id="11f5c-234">OneInRibbonGallery</span></span>

<span data-ttu-id="11f5c-235">一個 [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="11f5c-235">One [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) control.</span></span>

<span data-ttu-id="11f5c-236">僅支援大型和小型群組的大小。</span><span class="sxs-lookup"><span data-stu-id="11f5c-236">Only Large and Small group sizes are supported.</span></span>

![oneinribbongallery 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-oneinribbongallery-large.png)

![oneinribbongallery small sizedefinition 範本的圖片。](images/overviews/sizedefinition-oneinribbongallery-small.png)

<span data-ttu-id="11f5c-239">InRibbonGalleryAndBigButton</span><span class="sxs-lookup"><span data-stu-id="11f5c-239">InRibbonGalleryAndBigButton</span></span>

<span data-ttu-id="11f5c-240">一個 [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) 控制項和一個按鈕系列控制項。</span><span class="sxs-lookup"><span data-stu-id="11f5c-240">One [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) control and a button-family control.</span></span>

<span data-ttu-id="11f5c-241">僅支援大型和小型群組的大小。</span><span class="sxs-lookup"><span data-stu-id="11f5c-241">Only Large and Small group sizes are supported.</span></span>

![inribbongalleryandbigbutton 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-inribbongalleryandbigbutton-large.png)

![inribbongalleryandbigbutton small sizedefinition 範本的圖片。](images/overviews/sizedefinition-inribbongalleryandbigbutton-small.png)

<span data-ttu-id="11f5c-244">InRibbonGalleryAndButtons-GalleryScalesFirst</span><span class="sxs-lookup"><span data-stu-id="11f5c-244">InRibbonGalleryAndButtons-GalleryScalesFirst</span></span>

<span data-ttu-id="11f5c-245">一個 [功能區圖庫](windowsribbon-controls-inribbongallery.md) 控制項，以及兩個或三個按鈕系列控制項。</span><span class="sxs-lookup"><span data-stu-id="11f5c-245">One [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control and two or three button-family controls.</span></span>

<span data-ttu-id="11f5c-246">資源庫會折迭為中等和小型群組大小的快顯視窗表示。</span><span class="sxs-lookup"><span data-stu-id="11f5c-246">The gallery collapses to Popup representation in Medium and Small group sizes.</span></span>

![inribbongalleryandbuttons-galleryscalesfirst 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-large.png)

![inribbongalleryandbuttons-galleryscalesfirst medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-medium.png)

![inribbongalleryandbuttons-galleryscalesfirst small sizedefinition 範本的圖片。](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-small.png)

<span data-ttu-id="11f5c-250">ButtonGroups</span><span class="sxs-lookup"><span data-stu-id="11f5c-250">ButtonGroups</span></span>

<span data-ttu-id="11f5c-251">32按鈕系列控制項的複雜排列 (大多數都是選擇性) 。</span><span class="sxs-lookup"><span data-stu-id="11f5c-251">A complex arrangement of 32 button-family controls (most of which are optional).</span></span>

> [!Note]  
> <span data-ttu-id="11f5c-252">除了大型 ButtonGroups 範本的選擇性完整大小按鈕之外，以此範本宣告的所有控制項元素都必須包含在 [**ControlGroup**](windowsribbon-element-controlgroup.md) 元素中。</span><span class="sxs-lookup"><span data-stu-id="11f5c-252">Aside from the optional full-sized button of the large ButtonGroups template, all control elements declared with this template must be contained in [**ControlGroup**](windowsribbon-element-controlgroup.md) elements.</span></span>

 

<span data-ttu-id="11f5c-253">下列範例示範使用這個範本 (必要和選擇性) 顯示所有32控制項元素所需的標記。</span><span class="sxs-lookup"><span data-stu-id="11f5c-253">The following example demonstrates the markup required to display all 32 control elements (required and optional) with this template.</span></span>


```
<Group CommandName="cmdSizeDefinitionsGroup"
       SizeDefinition="ButtonGroups">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton16" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton30" />
      <Button CommandName="cmdSDButton31" />
    </ControlGroup>
  </ControlGroup>
  <Button CommandName="cmdSDButton32" />            
</Group>
```



![buttongroups 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-buttongroups-large.png)

![buttongroups medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-buttongroups-medium.png)

![buttongroups small sizedefinition 範本的圖片。](images/overviews/sizedefinition-buttongroups-small.png)

<span data-ttu-id="11f5c-257">ButtonGroupsAndInputs</span><span class="sxs-lookup"><span data-stu-id="11f5c-257">ButtonGroupsAndInputs</span></span>

<span data-ttu-id="11f5c-258">第二個輸入系列控制項 (第二個是選擇性的) 接著是29個按鈕系列控制項的複雜相片順序 (大部分都是選擇性的) 。</span><span class="sxs-lookup"><span data-stu-id="11f5c-258">Two input-family controls (the second is optional) followed by a complex arrangement of 29 button-family controls (most of which are optional).</span></span>

<span data-ttu-id="11f5c-259">僅支援大型和中型群組的大小。</span><span class="sxs-lookup"><span data-stu-id="11f5c-259">Only Large and Medium group sizes are supported.</span></span>

> [!Note]  
> <span data-ttu-id="11f5c-260">所有以此範本宣告的控制項元素都必須包含在 [**ControlGroup**](windowsribbon-element-controlgroup.md) 元素中。</span><span class="sxs-lookup"><span data-stu-id="11f5c-260">All control elements declared with this template must be contained in [**ControlGroup**](windowsribbon-element-controlgroup.md) elements.</span></span>

 

<span data-ttu-id="11f5c-261">下列範例示範使用這個範本 (必要和選擇性) 顯示所有控制項元素所需的標記。</span><span class="sxs-lookup"><span data-stu-id="11f5c-261">The following example demonstrates the markup required to display all control elements (required and optional) with this template.</span></span>


```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="ButtonGroupsAndInputs">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <ComboBox CommandName="cmdSDComboBox" />
      <Spinner CommandName="cmdSDSpinner" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->  
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
      <Button CommandName="cmdSDButton16" />
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
  </ControlGroup>
</Group>
```



![buttongroupsandinputs 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-buttongroupsandinputs-large.png)

![buttongroupsandinputs medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-buttongroupsandinputs-medium.png)

<span data-ttu-id="11f5c-264">BigButtonsAndSmallButtonsOrInputs</span><span class="sxs-lookup"><span data-stu-id="11f5c-264">BigButtonsAndSmallButtonsOrInputs</span></span>

<span data-ttu-id="11f5c-265">兩個按鈕系列控制項 (選用) 後面接著二或三個按鈕或輸入系列控制項。</span><span class="sxs-lookup"><span data-stu-id="11f5c-265">Two button-family controls (both optional) followed by two or three button or input-family controls.</span></span>

<span data-ttu-id="11f5c-266">僅支援大型和中型群組的大小。</span><span class="sxs-lookup"><span data-stu-id="11f5c-266">Only Large and Medium group sizes are supported.</span></span>

![bigbuttonsandsmallbuttonsorinputs 大型 sizedefinition 範本的圖片。](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-large.png)

![bigbuttonsandsmallbuttonsorinputs medium sizedefinition 範本的圖片。](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-medium.png)



 

### <a name="basic-sizedefinition-example"></a><span data-ttu-id="11f5c-269">基本 SizeDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="11f5c-269">Basic SizeDefinition Example</span></span>

<span data-ttu-id="11f5c-270">下列程式碼範例提供如何在功能區標記中宣告 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 範本的基本示範。</span><span class="sxs-lookup"><span data-stu-id="11f5c-270">The following code example provides a basic demonstration of how to declare a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template in Ribbon markup.</span></span>

<span data-ttu-id="11f5c-271">*OneInRibbonGallery* [**SizeDefinition**](windowsribbon-element-sizedefinition.md)用於此特定範例，但所有架構範本都是以類似的方式指定。</span><span class="sxs-lookup"><span data-stu-id="11f5c-271">The *OneInRibbonGallery* [**SizeDefinition**](windowsribbon-element-sizedefinition.md) is used for this particular example, but all framework templates are specified in a similar fashion.</span></span>


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



### <a name="complex-sizedefinition-example-with-scaling-policies"></a><span data-ttu-id="11f5c-272">具有調整原則的複雜 SizeDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="11f5c-272">Complex SizeDefinition Example with Scaling Policies</span></span>

<span data-ttu-id="11f5c-273">您可以使用功能區標記中的調整原則來控制 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 範本的折迭行為。</span><span class="sxs-lookup"><span data-stu-id="11f5c-273">The collapsing behavior of [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates can be controlled through the use of scaling policies in the Ribbon markup.</span></span>

<span data-ttu-id="11f5c-274">[**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)元素包含 [**ScalingPolicy**](windowsribbon-element-scalingpolicy-idealsizes.md)的資訊清單，並在調整大小功能區 [**時，指定**](windowsribbon-element-scale.md)一或多個 [**群組**](windowsribbon-element-group.md)元素的自我調整版面配置喜好設定。</span><span class="sxs-lookup"><span data-stu-id="11f5c-274">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) element contains a manifest of [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) and [**Scale**](windowsribbon-element-scale.md) declarations that specify adaptive layout preferences for one or more [**Group**](windowsribbon-element-group.md) elements when the Ribbon is resized.</span></span>

> [!Note]  
> <span data-ttu-id="11f5c-275">強烈建議您指定適當的調整原則詳細資料，如此一來，大部分的 [**群組**](windowsribbon-element-group.md)元素都會與 *大小* 屬性等於的 [**縮放**](windowsribbon-element-scale.md)元素相關聯 `Popup` 。</span><span class="sxs-lookup"><span data-stu-id="11f5c-275">It is highly recommended that adequate scaling policy detail be specified such that most, if not all, [**Group**](windowsribbon-element-group.md) elements are associated with a [**Scale**](windowsribbon-element-scale.md) element where the *Size* attribute is equal to `Popup`.</span></span> <span data-ttu-id="11f5c-276">這麼做可讓架構盡可能以最小的大小轉譯功能區，並支援最大範圍的顯示裝置，再自動導入滾動機制。</span><span class="sxs-lookup"><span data-stu-id="11f5c-276">Doing so allows the framework to render the ribbon at the smallest size possible, and support the broadest range of display devices, before automatically introducing a scrolling mechanism.</span></span>

 

<span data-ttu-id="11f5c-277">下列程式碼範例會示範 [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)資訊清單，該資訊清單會針對 [**主** 資料夾] 索引標籤上的四個控制項群組，指定 [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md)喜好設定。此外，也會指定 [**小**](windowsribbon-element-scale.md)數位數元素，以影響每個群組的折迭行為（依遞減大小排序）。</span><span class="sxs-lookup"><span data-stu-id="11f5c-277">The following code example demonstrates a [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest that specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


```C++
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupFont" Size="Popup"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Popup"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
```



### <a name="custom-templates"></a><span data-ttu-id="11f5c-278">自訂範本</span><span class="sxs-lookup"><span data-stu-id="11f5c-278">Custom Templates</span></span>

<span data-ttu-id="11f5c-279">如果預設的版面配置行為和預先定義的 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 範本未提供特定版面配置案例的彈性或支援，功能區架構會透過 [**SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) 元素來支援自訂範本。</span><span class="sxs-lookup"><span data-stu-id="11f5c-279">If the default layout behaviors and the predefined [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates do not offer the flexibility or support for a particular layout scenario, custom templates are supported by the Ribbon framework through the [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element.</span></span>

<span data-ttu-id="11f5c-280">您可以使用下列兩種方式宣告自訂範本：使用 [**SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) 專案的獨立方法，宣告可重複使用的、命名範本或 [**群組**](windowsribbon-element-group.md)特定的內嵌方法。</span><span class="sxs-lookup"><span data-stu-id="11f5c-280">Custom templates can be declared in two ways: a standalone method using the [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element for declaring reusable, named templates or an inline method that is [**Group**](windowsribbon-element-group.md)-specific.</span></span>

### <a name="standalone-template"></a><span data-ttu-id="11f5c-281">獨立範本</span><span class="sxs-lookup"><span data-stu-id="11f5c-281">Standalone Template</span></span>

<span data-ttu-id="11f5c-282">下列程式碼範例說明基本、可重複使用的自訂範本。</span><span class="sxs-lookup"><span data-stu-id="11f5c-282">The following code example illustrates a basic, reusable custom template.</span></span>


```
<Ribbon.SizeDefinitions>
  <SizeDefinition Name="CustomTemplate">
    <GroupSizeDefinition Size="Large">
      <ControlSizeDefinition ImageSize="Large" IsLabelVisible="true" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
  </SizeDefinition>
</Ribbon.SizeDefinitions>
```



### <a name="inline-template"></a><span data-ttu-id="11f5c-283">內嵌範本</span><span class="sxs-lookup"><span data-stu-id="11f5c-283">Inline Template</span></span>

<span data-ttu-id="11f5c-284">下列程式碼範例說明四個按鈕群組的基本內嵌自訂範本。</span><span class="sxs-lookup"><span data-stu-id="11f5c-284">The following code examples illustrate a basic inline custom template for a group of four buttons.</span></span>

<span data-ttu-id="11f5c-285">這段程式碼會顯示一組按鈕的命令宣告。</span><span class="sxs-lookup"><span data-stu-id="11f5c-285">This section of code shows the Command declarations for a group of buttons.</span></span> <span data-ttu-id="11f5c-286">您也可以在這裡指定大型和小型影像資源。</span><span class="sxs-lookup"><span data-stu-id="11f5c-286">Large and small image resources are also specified here.</span></span>


```XML
<!-- Button -->
<Command Name="cmdButtonGroup"
         Symbol="cmdButtonGroup"
         Comment="Button Group"
         LabelTitle="ButtonGroup"/>
<Command Name="cmdButton1"
         Symbol="cmdButton1"
         Comment="Button1"
         LabelTitle="Button1"/>
<Command Name="cmdButton2"
         Symbol="cmdButton2"
         Comment="Button2"
         LabelTitle="Button2"/>
<Command Name="cmdButton3"
         Symbol="cmdButton3"
         Comment="Button3"
         LabelTitle="Button3"/>
<Command Name="cmdButtonGroup2"
         Symbol="cmdButtonGroup2"
         Comment="Button Group2"
         LabelTitle="ButtonGroup2"/>
<Command Name="cmdButtonG21"
         Symbol="cmdButtonG21"
         Comment="ButtonG21"
         LabelTitle="ButtonG21">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG22"
         Symbol="cmdButtonG22"
         Comment="ButtonG22"
         LabelTitle="ButtonG22">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG23"
         Symbol="cmdButtonG23"
         Comment="ButtonG23"
         LabelTitle="ButtonG23">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG24"
         Symbol="cmdButtonG24"
         Comment="ButtonG24"
         LabelTitle="ButtonG24">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
```



<span data-ttu-id="11f5c-287">這一節的程式碼示範如何定義大型、中型和 small [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) 範本，以顯示各種不同大小和版面配置的四個按鈕。</span><span class="sxs-lookup"><span data-stu-id="11f5c-287">This section of code demonstrates how to define large, medium, and small [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) templates to display the four buttons at various sizes and layouts.</span></span> <span data-ttu-id="11f5c-288">索引標籤的 [ [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) ] 宣告會根據 [使用中] 索引標籤所需的功能區大小和空間，定義要用於控制項群組的範本。</span><span class="sxs-lookup"><span data-stu-id="11f5c-288">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) declaration for the tab defines which template is used for a group of controls based on the ribbon size and space required by the active tab.</span></span>


```XML
        <Tab CommandName="cmdTab6">
          <Tab.ScalingPolicy>
            <ScalingPolicy>
              <ScalingPolicy.IdealSizes>
                <Scale Group="cmdButtonGroup"
                       Size="Large"/>
                <Scale Group="cmdButtonGroup2"
                       Size="Large"/>
                <Scale Group="cmdToggleButtonGroup"
                       Size="Large"/>
              </ScalingPolicy.IdealSizes>
              <Scale Group="cmdButtonGroup"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Small"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Popup"/>
            </ScalingPolicy>
          </Tab.ScalingPolicy>

          <Group CommandName="cmdButtonGroup2">
            <SizeDefinition>
              <ControlNameMap>
                <ControlNameDefinition Name="button1"/>
                <ControlNameDefinition Name="button2"/>
                <ControlNameDefinition Name="button3"/>
                <ControlNameDefinition Name="button4"/>
              </ControlNameMap>
              <GroupSizeDefinition Size="Large">
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                </ControlGroup>
                <ColumnBreak ShowSeparator="true"/>
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Large"
                                        IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                        ImageSize="Large"
                                        IsLabelVisible="true" />
                </ControlGroup>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Medium">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Small">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
              </GroupSizeDefinition>
            </SizeDefinition>
            <Button CommandName="cmdButtonG21"></Button>
            <Button CommandName="cmdButtonG22"></Button>
            <Button CommandName="cmdButtonG23"></Button>
            <Button CommandName="cmdButtonG24"></Button>
          </Group>
          <Group CommandName="cmdCheckBoxGroup">
            <CheckBox CommandName="cmdCheckBox"></CheckBox>
          </Group>
          <Group CommandName="cmdToggleButtonGroup"
                 SizeDefinition="OneButton">
            <ToggleButton CommandName="cmdToggleButton"></ToggleButton>
          </Group>
          <Group CommandName="cmdButtonGroup"
                 SizeDefinition="ThreeButtons">
            <Button CommandName="cmdButton1"></Button>
            <Button CommandName="cmdButton2"></Button>
            <Button CommandName="cmdButton3"></Button>
          </Group>
        </Tab>
```



<span data-ttu-id="11f5c-289">下圖顯示上一個範例中的範本如何套用至功能區 UI，以配合功能區大小的減少。</span><span class="sxs-lookup"><span data-stu-id="11f5c-289">The following images show how the templates from the previous example are applied to the ribbon UI to accommodate a decrease in ribbon size.</span></span>



|        |                                                                                                    |
|--------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11f5c-290">大</span><span class="sxs-lookup"><span data-stu-id="11f5c-290">Large</span></span>  | ![內嵌大型自訂範本的圖片。](images/overviews/sizedefinition-custom-large.png)   |
| <span data-ttu-id="11f5c-292">中</span><span class="sxs-lookup"><span data-stu-id="11f5c-292">Medium</span></span> | ![內嵌中型自訂範本的圖片。](images/overviews/sizedefinition-custom-medium.png) |
| <span data-ttu-id="11f5c-294">小</span><span class="sxs-lookup"><span data-stu-id="11f5c-294">Small</span></span>  | ![內嵌小型自訂範本的圖片。](images/overviews/sizedefinition-custom-small.png)   |
| <span data-ttu-id="11f5c-296">快顯</span><span class="sxs-lookup"><span data-stu-id="11f5c-296">Popup</span></span>  | ![內嵌快顯視窗自訂範本的圖片。](images/overviews/sizedefinition-custom-popup.png)   |



 

## <a name="related-topics"></a><span data-ttu-id="11f5c-298">相關主題</span><span class="sxs-lookup"><span data-stu-id="11f5c-298">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11f5c-299">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="11f5c-299">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)
</dt> <dt>

[<span data-ttu-id="11f5c-300">**調整**</span><span class="sxs-lookup"><span data-stu-id="11f5c-300">**Scale**</span></span>](windowsribbon-element-scale.md)
</dt> <dt>

[<span data-ttu-id="11f5c-301">**Group**</span><span class="sxs-lookup"><span data-stu-id="11f5c-301">**Group**</span></span>](windowsribbon-element-group.md)
</dt> </dl>

 

 





