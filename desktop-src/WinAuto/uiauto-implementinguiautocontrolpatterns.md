---
title: 執行消費者介面自動化控制項模式
description: 本節提供有關如何執行支援控制項模式的 Microsoft 消費者介面自動化提供者介面的詳細資訊。
ms.assetid: d1baa245-62a1-40b1-a671-e227dd3df60a
keywords:
- 消費者介面自動化，執行控制項模式
- 消費者介面自動化，控制項模式
- 執行消費者介面自動化控制項模式
- 控制項模式，執行消費者介面自動化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfb75b6b275fee9230eb25d9a0b02e1da26ad4d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106969915"
---
# <a name="implementing-ui-automation-control-patterns"></a><span data-ttu-id="15322-107">執行消費者介面自動化控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-107">Implementing UI Automation Control Patterns</span></span>

<span data-ttu-id="15322-108">本節提供有關如何執行支援控制項模式的 Microsoft 消費者介面自動化提供者介面的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="15322-108">This section provides detailed information about implementing the Microsoft UI Automation provider interfaces that support control patterns.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="15322-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="15322-109">In this section</span></span>

-   [<span data-ttu-id="15322-110">Annotation 控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-110">Annotation Control Pattern</span></span>](uiauto-implementingannotation.md)
-   [<span data-ttu-id="15322-111">CustomNavigation 控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-111">CustomNavigation Control Pattern</span></span>](uiauto-implementingcustomnavigation.md)
-   [<span data-ttu-id="15322-112">停駐控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-112">Dock Control Pattern</span></span>](uiauto-implementingdock.md)
-   [<span data-ttu-id="15322-113">拖曳控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-113">Drag Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingdrag)
-   [<span data-ttu-id="15322-114">DropTarget 控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-114">DropTarget Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingdroptarget)
-   [<span data-ttu-id="15322-115">ExpandCollapse 控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-115">ExpandCollapse Control Pattern</span></span>](uiauto-implementingexpandcollapse.md)
-   [<span data-ttu-id="15322-116">方格控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-116">Grid Control Pattern</span></span>](uiauto-implementinggrid.md)
-   [<span data-ttu-id="15322-117">GridItem 控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-117">GridItem Control Pattern</span></span>](uiauto-implementinggriditem.md)
-   [<span data-ttu-id="15322-118">Invoke 控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-118">Invoke Control Pattern</span></span>](uiauto-implementinginvoke.md)
-   [<span data-ttu-id="15322-119">>itemcontainer 控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-119">ItemContainer Control Pattern</span></span>](uiauto-implementingitemcontainer.md)
-   [<span data-ttu-id="15322-120">LegacyIAccessible 控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-120">LegacyIAccessible Control Pattern</span></span>](uiauto-implementinglegacyiaccessible.md)
-   [<span data-ttu-id="15322-121">MultipleView 控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-121">MultipleView Control Pattern</span></span>](uiauto-implementingmultipleview.md)
-   [<span data-ttu-id="15322-122">System.collections.objectmodel.observablecollection 控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-122">ObjectModel Control Pattern</span></span>](uiauto-implementingobjectmodel.md)
-   [<span data-ttu-id="15322-123">RangeValue 控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-123">RangeValue Control Pattern</span></span>](uiauto-implementingrangevalue.md)
-   [<span data-ttu-id="15322-124">捲軸控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-124">Scroll Control Pattern</span></span>](uiauto-implementingscroll.md)
-   [<span data-ttu-id="15322-125">ScrollItem 控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-125">ScrollItem Control Pattern</span></span>](uiauto-implementingscrollitem.md)
-   [<span data-ttu-id="15322-126">選取控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-126">Selection Control Pattern</span></span>](uiauto-implementingselection.md)
-   [<span data-ttu-id="15322-127">SelectionItem 控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-127">SelectionItem Control Pattern</span></span>](uiauto-implementingselectionitem.md)
-   [<span data-ttu-id="15322-128">試算表控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-128">Spreadsheet Control Pattern</span></span>](uiauto-implementingspreadsheet.md)
-   [<span data-ttu-id="15322-129">SpreadsheetItem 控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-129">SpreadsheetItem Control Pattern</span></span>](uiauto-implementingspreadsheetitem.md)
-   [<span data-ttu-id="15322-130">樣式控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-130">Styles Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingstyles)
-   [<span data-ttu-id="15322-131">SynchronizedInput 控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-131">SynchronizedInput Control Pattern</span></span>](uiauto-implementingsynchronizedinput.md)
-   [<span data-ttu-id="15322-132">Table 控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-132">Table Control Pattern</span></span>](uiauto-implementingtable.md)
-   [<span data-ttu-id="15322-133">TableItem 控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-133">TableItem Control Pattern</span></span>](uiauto-implementingtableitem.md)
-   [<span data-ttu-id="15322-134">Text 和 TextRange 控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-134">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
-   [<span data-ttu-id="15322-135">TextChild 控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-135">TextChild Control Pattern</span></span>](textchild-control-pattern.md)
-   [<span data-ttu-id="15322-136">Macos textedit 控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-136">TextEdit Control Pattern</span></span>](textedit-control-pattern.md)
-   [<span data-ttu-id="15322-137">切換控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-137">Toggle Control Pattern</span></span>](uiauto-implementingtoggle.md)
-   [<span data-ttu-id="15322-138">轉換控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-138">Transform Control Pattern</span></span>](uiauto-implementingtransform.md)
-   [<span data-ttu-id="15322-139">值控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-139">Value Control Pattern</span></span>](uiauto-implementingvalue.md)
-   [<span data-ttu-id="15322-140">VirtualizedItem 控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-140">VirtualizedItem Control Pattern</span></span>](uiauto-implementingvirtualizeditem.md)
-   [<span data-ttu-id="15322-141">視窗控制項模式</span><span class="sxs-lookup"><span data-stu-id="15322-141">Window Control Pattern</span></span>](uiauto-implementingwindow.md)

## <a name="related-topics"></a><span data-ttu-id="15322-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="15322-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15322-143">消費者介面自動化提供者程式設計人員指南</span><span class="sxs-lookup"><span data-stu-id="15322-143">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
</dt> <dt>

[<span data-ttu-id="15322-144">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="15322-144">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="15322-145">支援消費者介面自動化控制項類型</span><span class="sxs-lookup"><span data-stu-id="15322-145">Supporting UI Automation Control Types</span></span>](uiauto-supportinguiautocontroltypes.md)
</dt> </dl>

 

 