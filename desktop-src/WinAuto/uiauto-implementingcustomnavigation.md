---
title: CustomNavigation 控制項模式
description: 描述執行 ICustomNavigationProvider 介面的方針和慣例，包括屬性和方法的相關資訊。
ms.assetid: 428540BB-5CC0-4F49-8384-0FFC130FBB38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cc6524585f3ddd7ec764a791141fce9daa3c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183452"
---
# <a name="customnavigation-control-pattern"></a><span data-ttu-id="94885-103">CustomNavigation 控制項模式</span><span class="sxs-lookup"><span data-stu-id="94885-103">CustomNavigation Control Pattern</span></span>

<span data-ttu-id="94885-104">描述執行 **ICustomNavigationProvider** 介面的方針和慣例，包括屬性和方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="94885-104">Describes guidelines and conventions for implementing the **ICustomNavigationProvider** interface, including information about properties and methods.</span></span> <span data-ttu-id="94885-105">**CustomNavigation** 控制項模式是用來在階層式結構中的控制項（例如清單專案、項目符號清單、編號清單和標題）之間啟用自訂導覽。</span><span class="sxs-lookup"><span data-stu-id="94885-105">The **CustomNavigation** control pattern is used to enable custom navigation between controls in hierarchy-like structures such as list items, bulleted lists, numbered lists and headings.</span></span> <span data-ttu-id="94885-106">這可讓提供者描述結構，或單獨使用元素來定義可導覽的關聯性，而不只是包含控制項。</span><span class="sxs-lookup"><span data-stu-id="94885-106">This enables providers to describe structures or define the navigable relationships using the element alone and not just the containing control.</span></span>

<span data-ttu-id="94885-107">如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。</span><span class="sxs-lookup"><span data-stu-id="94885-107">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="94885-108">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="94885-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="94885-109">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="94885-109">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="94885-110">**ICustomNavigationProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="94885-110">Required Members for **ICustomNavigationProvider**</span></span>](#required-members-for-icustomnavigationprovider)
-   [<span data-ttu-id="94885-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="94885-111">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="94885-112">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="94885-112">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="94885-113">在實施 **CustomNavigation** 提供者時，請注意下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="94885-113">When implementing the **CustomNavigation** provider, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="94885-114">**>positioninset**、 **SizeOfSet** 和 **Level** 的屬性值是以一為基礎的整數值。</span><span class="sxs-lookup"><span data-stu-id="94885-114">Property values for **PositionInSet**, **SizeOfSet**, and **Level** are one-based integer values.</span></span>
-   <span data-ttu-id="94885-115">**ICustomNavigationProvider** 不提供控制項的主動式操作，例如移動位置、新增和移除專案，或升級和降級層級。</span><span class="sxs-lookup"><span data-stu-id="94885-115">**ICustomNavigationProvider** does not provide for active manipulation of the control such as moving positions, adding and removing items, or promoting and demoting levels.</span></span>
-   <span data-ttu-id="94885-116">執行 **ICustomNavigationProvider** 的控制項通常會有階層式結構，但是可以使用 **導覽** 方法略過層級。</span><span class="sxs-lookup"><span data-stu-id="94885-116">Controls that implement **ICustomNavigationProvider** typically have a hierarchical structure, but can skip levels by using the **Navigate** method.</span></span> <span data-ttu-id="94885-117">屬性 **>positioninset**、 **SizeOfSet** 和 **Level** 需要在模式上。</span><span class="sxs-lookup"><span data-stu-id="94885-117">The properties **PositionInSet**, **SizeOfSet**, and **Level** are required on the pattern.</span></span>

## <a name="required-members-for-icustomnavigationprovider"></a><span data-ttu-id="94885-118">**ICustomNavigationProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="94885-118">Required Members for **ICustomNavigationProvider**</span></span>

<span data-ttu-id="94885-119">執行 **ICustomNavigationProvider** 介面需要下列屬性。</span><span class="sxs-lookup"><span data-stu-id="94885-119">The following properties are required for implementing the **ICustomNavigationProvider** interface.</span></span>



| <span data-ttu-id="94885-120">必要成員</span><span class="sxs-lookup"><span data-stu-id="94885-120">Required members</span></span>                                                                  | <span data-ttu-id="94885-121">成員類型</span><span class="sxs-lookup"><span data-stu-id="94885-121">Member type</span></span> | <span data-ttu-id="94885-122">備註</span><span class="sxs-lookup"><span data-stu-id="94885-122">Notes</span></span>                                                                               |
|-----------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="94885-123">**CachedLevel**</span><span class="sxs-lookup"><span data-stu-id="94885-123">**CachedLevel**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedlevel)                   | <span data-ttu-id="94885-124">屬性</span><span class="sxs-lookup"><span data-stu-id="94885-124">Property</span></span>    | <span data-ttu-id="94885-125">位於 [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) 介面上。</span><span class="sxs-lookup"><span data-stu-id="94885-125">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="94885-126">**CachedPositionInSet**</span><span class="sxs-lookup"><span data-stu-id="94885-126">**CachedPositionInSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedpositioninset)   | <span data-ttu-id="94885-127">屬性</span><span class="sxs-lookup"><span data-stu-id="94885-127">Property</span></span>    | <span data-ttu-id="94885-128">位於 [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) 介面上。</span><span class="sxs-lookup"><span data-stu-id="94885-128">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="94885-129">**CachedSizeOfSet**</span><span class="sxs-lookup"><span data-stu-id="94885-129">**CachedSizeOfSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedsizeofset)           | <span data-ttu-id="94885-130">屬性</span><span class="sxs-lookup"><span data-stu-id="94885-130">Property</span></span>    | <span data-ttu-id="94885-131">位於 [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) 介面上。</span><span class="sxs-lookup"><span data-stu-id="94885-131">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="94885-132">**CurrentLevel**</span><span class="sxs-lookup"><span data-stu-id="94885-132">**CurrentLevel**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentlevel)                 | <span data-ttu-id="94885-133">屬性</span><span class="sxs-lookup"><span data-stu-id="94885-133">Property</span></span>    | <span data-ttu-id="94885-134">位於 [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) 介面上。</span><span class="sxs-lookup"><span data-stu-id="94885-134">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="94885-135">**CurrentPositionInSet**</span><span class="sxs-lookup"><span data-stu-id="94885-135">**CurrentPositionInSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentpositioninset) | <span data-ttu-id="94885-136">屬性</span><span class="sxs-lookup"><span data-stu-id="94885-136">Property</span></span>    | <span data-ttu-id="94885-137">位於 [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) 介面上。</span><span class="sxs-lookup"><span data-stu-id="94885-137">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="94885-138">**CurrentSizeOfSet**</span><span class="sxs-lookup"><span data-stu-id="94885-138">**CurrentSizeOfSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentsizeofset)         | <span data-ttu-id="94885-139">屬性</span><span class="sxs-lookup"><span data-stu-id="94885-139">Property</span></span>    | <span data-ttu-id="94885-140">位於 [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) 介面上。</span><span class="sxs-lookup"><span data-stu-id="94885-140">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="94885-141">**導航**</span><span class="sxs-lookup"><span data-stu-id="94885-141">**Navigate**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate)                   | <span data-ttu-id="94885-142">方法</span><span class="sxs-lookup"><span data-stu-id="94885-142">Method</span></span>      | <span data-ttu-id="94885-143">無</span><span class="sxs-lookup"><span data-stu-id="94885-143">None</span></span>                                                                                |



 

<span data-ttu-id="94885-144">此控制項模式沒有任何相關聯的方法或事件。</span><span class="sxs-lookup"><span data-stu-id="94885-144">This control pattern has no associated methods or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94885-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="94885-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94885-146">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="94885-146">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

<span data-ttu-id="94885-147">[[中] 控制項](uiauto-supportlistitemcontroltype.md)</span><span class="sxs-lookup"><span data-stu-id="94885-147">[ListItem Control](uiauto-supportlistitemcontroltype.md)</span></span>
</dt> <dt>

[<span data-ttu-id="94885-148">HeaderItem 控制項</span><span class="sxs-lookup"><span data-stu-id="94885-148">HeaderItem Control</span></span>](uiauto-supportheaderitemcontroltype.md)
</dt> <dt>

[<span data-ttu-id="94885-149">DataItem 控制項</span><span class="sxs-lookup"><span data-stu-id="94885-149">DataItem Control</span></span>](uiauto-supportdataitemcontroltype.md)
</dt> <dt>

[<span data-ttu-id="94885-150">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="94885-150">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




