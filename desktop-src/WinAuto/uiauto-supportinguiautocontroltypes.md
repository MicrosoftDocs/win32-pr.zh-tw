---
title: 支援消費者介面自動化控制項類型
description: 本節包含每個 Microsoft 消費者介面自動化控制項類型都必須支援的樹狀結構、屬性、控制項模式和事件的詳細資訊。
ms.assetid: 35232907-6c54-47cd-b82a-0daee279ef17
keywords:
- 消費者介面自動化，關於控制項類型
- 消費者介面自動化，控制項類型總覽
- 控制項類型的支援
- 控制項類型，支援
- 控制項類型，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ac6f857da87691428c747cfe5dbff5102218f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382478"
---
# <a name="supporting-ui-automation-control-types"></a><span data-ttu-id="54ecc-108">支援消費者介面自動化控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-108">Supporting UI Automation Control Types</span></span>

<span data-ttu-id="54ecc-109">本節包含每個 Microsoft 消費者介面自動化控制項類型都必須支援的樹狀結構、屬性、控制項模式和事件的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="54ecc-109">This section contains detailed information about the tree structure, properties, control patterns, and events that each Microsoft UI Automation control type is required to support.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="54ecc-110">本節內容</span><span class="sxs-lookup"><span data-stu-id="54ecc-110">In this section</span></span>

-   [<span data-ttu-id="54ecc-111">AppBar 控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-111">AppBar Control Type</span></span>](uiauto-supportappbarcontroltype.md)
-   [<span data-ttu-id="54ecc-112">Button 控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-112">Button Control Type</span></span>](uiauto-supportbuttoncontroltype.md)
-   [<span data-ttu-id="54ecc-113">行事曆控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-113">Calendar Control Type</span></span>](uiauto-supportcalendarcontroltype.md)
-   [<span data-ttu-id="54ecc-114">CheckBox 控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-114">CheckBox Control Type</span></span>](uiauto-supportcheckboxcontroltype.md)
-   [<span data-ttu-id="54ecc-115">ComboBox 控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-115">ComboBox Control Type</span></span>](uiauto-supportcomboboxcontroltype.md)
-   [<span data-ttu-id="54ecc-116">DataGrid 控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-116">DataGrid Control Type</span></span>](uiauto-supportdatagridcontroltype.md)
-   [<span data-ttu-id="54ecc-117">DataItem 控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-117">DataItem Control Type</span></span>](uiauto-supportdataitemcontroltype.md)
-   [<span data-ttu-id="54ecc-118">檔控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-118">Document Control Type</span></span>](uiauto-supportdocumentcontroltype.md)
-   [<span data-ttu-id="54ecc-119">編輯控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-119">Edit Control Type</span></span>](uiauto-supporteditcontroltype.md)
-   [<span data-ttu-id="54ecc-120">群組控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-120">Group Control Type</span></span>](uiauto-supportgroupcontroltype.md)
-   [<span data-ttu-id="54ecc-121">標題控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-121">Header Control Type</span></span>](uiauto-supportheadercontroltype.md)
-   [<span data-ttu-id="54ecc-122">HeaderItem 控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-122">HeaderItem Control Type</span></span>](uiauto-supportheaderitemcontroltype.md)
-   [<span data-ttu-id="54ecc-123">Hyperlink 控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-123">Hyperlink Control Type</span></span>](uiauto-supporthyperlinkcontroltype.md)
-   [<span data-ttu-id="54ecc-124">影像控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-124">Image Control Type</span></span>](uiauto-supportimagecontroltype.md)
-   [<span data-ttu-id="54ecc-125">清單控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-125">List Control Type</span></span>](uiauto-supportlistcontroltype.md)
-   <span data-ttu-id="54ecc-126">[[類型] 控制項類型](uiauto-supportlistitemcontroltype.md)</span><span class="sxs-lookup"><span data-stu-id="54ecc-126">[ListItem Control Type](uiauto-supportlistitemcontroltype.md)</span></span>
-   [<span data-ttu-id="54ecc-127">Menu 控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-127">Menu Control Type</span></span>](uiauto-supportmenucontroltype.md)
-   [<span data-ttu-id="54ecc-128">功能表列控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-128">MenuBar Control Type</span></span>](uiauto-supportmenubarcontroltype.md)
-   [<span data-ttu-id="54ecc-129">MenuItem 控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-129">MenuItem Control Type</span></span>](uiauto-supportmenuitemcontroltype.md)
-   [<span data-ttu-id="54ecc-130">窗格控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-130">Pane Control Type</span></span>](uiauto-supportpanecontroltype.md)
-   [<span data-ttu-id="54ecc-131">ProgressBar 控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-131">ProgressBar Control Type</span></span>](uiauto-supportprogressbarcontroltype.md)
-   [<span data-ttu-id="54ecc-132">選項按鈕控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-132">RadioButton Control Type</span></span>](uiauto-supportradiobuttoncontroltype.md)
-   [<span data-ttu-id="54ecc-133">捲軸控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-133">ScrollBar Control Type</span></span>](uiauto-supportscrollbarcontroltype.md)
-   [<span data-ttu-id="54ecc-134">SemanticZoom 控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-134">SemanticZoom Control Type</span></span>](/windows/desktop/WinAuto/uiauto-supportsemanticzoomcontroltype)
-   [<span data-ttu-id="54ecc-135">分隔符號控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-135">Separator Control Type</span></span>](uiauto-supportseparatorcontroltype.md)
-   [<span data-ttu-id="54ecc-136">滑杆控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-136">Slider Control Type</span></span>](uiauto-supportslidercontroltype.md)
-   [<span data-ttu-id="54ecc-137">微調控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-137">Spinner Control Type</span></span>](uiauto-supportspinnercontroltype.md)
-   [<span data-ttu-id="54ecc-138">SplitButton 控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-138">SplitButton Control Type</span></span>](uiauto-supportsplitbuttoncontroltype.md)
-   [<span data-ttu-id="54ecc-139">狀態列控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-139">StatusBar Control Type</span></span>](uiauto-supportstatusbarcontroltype.md)
-   [<span data-ttu-id="54ecc-140">索引標籤控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-140">Tab Control Type</span></span>](uiauto-supporttabcontroltype.md)
-   [<span data-ttu-id="54ecc-141">TabItem 控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-141">TabItem Control Type</span></span>](uiauto-supporttabitemcontroltype.md)
-   [<span data-ttu-id="54ecc-142">Table 控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-142">Table Control Type</span></span>](uiauto-supporttablecontroltype.md)
-   [<span data-ttu-id="54ecc-143">Text 控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-143">Text Control Type</span></span>](uiauto-supporttextcontroltype.md)
-   [<span data-ttu-id="54ecc-144">Thumb 控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-144">Thumb Control Type</span></span>](uiauto-supportthumbcontroltype.md)
-   [<span data-ttu-id="54ecc-145">標題列控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-145">TitleBar Control Type</span></span>](uiauto-supporttitlebarcontroltype.md)
-   [<span data-ttu-id="54ecc-146">ToolBar 控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-146">ToolBar Control Type</span></span>](uiauto-supporttoolbarcontroltype.md)
-   [<span data-ttu-id="54ecc-147">ToolTip 控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-147">ToolTip Control Type</span></span>](uiauto-supporttooltipcontroltype.md)
-   [<span data-ttu-id="54ecc-148">樹狀目錄控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-148">Tree Control Type</span></span>](uiauto-supporttreecontroltype.md)
-   [<span data-ttu-id="54ecc-149">TreeItem 控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-149">TreeItem Control Type</span></span>](uiauto-supporttreeitemcontroltype.md)
-   [<span data-ttu-id="54ecc-150">Window 控制項類型</span><span class="sxs-lookup"><span data-stu-id="54ecc-150">Window Control Type</span></span>](uiauto-supportwindowcontroltype.md)

## <a name="related-topics"></a><span data-ttu-id="54ecc-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="54ecc-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54ecc-152">消費者介面自動化提供者程式設計人員指南</span><span class="sxs-lookup"><span data-stu-id="54ecc-152">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
</dt> </dl>

 

 