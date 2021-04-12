---
title: 字型控制項
description: 為了在需要文字處理和文字編輯功能的應用程式中簡化字型支援的整合和設定，Windows 功能區架構會提供特製化的字型控制項，以公開字型名稱、樣式、點大小和效果等範圍的字型屬性。
ms.assetid: 6052f2e3-2c9e-432e-9ed6-c1e3a50843d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e179296ae03163bf03e08d2fbf7287264792e6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375832"
---
# <a name="font-control"></a><span data-ttu-id="d9b96-103">字型控制項</span><span class="sxs-lookup"><span data-stu-id="d9b96-103">Font Control</span></span>

<span data-ttu-id="d9b96-104">為了在需要文字處理和文字編輯功能的應用程式中簡化字型支援的整合和設定，Windows 功能區架構會提供特製化的字型控制項，以公開字型名稱、樣式、點大小和效果等範圍的字型屬性。</span><span class="sxs-lookup"><span data-stu-id="d9b96-104">To simplify the integration and configuration of font support in applications that require word processing and text editing capabilities, the Windows Ribbon framework provides a specialized Font Control that exposes a wide range of font properties such as typeface name, style, point size, and effects.</span></span>

-   [<span data-ttu-id="d9b96-105">簡介</span><span class="sxs-lookup"><span data-stu-id="d9b96-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="d9b96-106">一致的體驗</span><span class="sxs-lookup"><span data-stu-id="d9b96-106">A Consistent Experience</span></span>](#a-consistent-experience)
-   [<span data-ttu-id="d9b96-107">輕鬆整合和設定</span><span class="sxs-lookup"><span data-stu-id="d9b96-107">Easy Integration and Configuration</span></span>](#easy-integration-and-configuration)
-   [<span data-ttu-id="d9b96-108">與常用 GDI 文字結構對齊</span><span class="sxs-lookup"><span data-stu-id="d9b96-108">Alignment with Common GDI Text Structures</span></span>](#alignment-with-common-gdi-text-structures)
-   [<span data-ttu-id="d9b96-109">新增 FontControl</span><span class="sxs-lookup"><span data-stu-id="d9b96-109">Add a FontControl</span></span>](#add-a-fontcontrol)
    -   [<span data-ttu-id="d9b96-110">在標記中宣告 FontControl</span><span class="sxs-lookup"><span data-stu-id="d9b96-110">Declaring a FontControl in Markup</span></span>](#declaring-a-fontcontrol-in-markup)
    -   [<span data-ttu-id="d9b96-111">字型控制項屬性</span><span class="sxs-lookup"><span data-stu-id="d9b96-111">Font Control Properties</span></span>](#font-control-properties)
-   [<span data-ttu-id="d9b96-112">定義 FontControl 命令處理常式</span><span class="sxs-lookup"><span data-stu-id="d9b96-112">Define a FontControl Command Handler</span></span>](#define-a-fontcontrol-command-handler)
-   [<span data-ttu-id="d9b96-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="d9b96-113">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="d9b96-114">簡介</span><span class="sxs-lookup"><span data-stu-id="d9b96-114">Introduction</span></span>

<span data-ttu-id="d9b96-115">字型控制項是由按鈕、切換按鈕、下拉式清單方塊和下拉式方塊組成的複合控制項，它們全都是用來指定特定的字型屬性或格式選項。</span><span class="sxs-lookup"><span data-stu-id="d9b96-115">The Font Control is a composite control that consists of buttons, toggle buttons, drop-down list boxes, and combo boxes, all of which are used to specify a particular font property or formatting option.</span></span>

<span data-ttu-id="d9b96-116">下列螢幕擷取畫面顯示 Windows 7 的 WordPad 中的功能區字型控制項。</span><span class="sxs-lookup"><span data-stu-id="d9b96-116">The following screen shot shows the Ribbon Font Control in WordPad for Windows 7.</span></span>

![fontcontrol 專案的螢幕擷取畫面，其中 richfont 屬性設定為 true。](images/controls/fontcontrol.png)

## <a name="a-consistent-experience"></a><span data-ttu-id="d9b96-118">一致的體驗</span><span class="sxs-lookup"><span data-stu-id="d9b96-118">A Consistent Experience</span></span>

<span data-ttu-id="d9b96-119">字型控制項是內建的功能區控制項，可改善整體字型管理、選取和格式化功能，並在所有功能區應用程式中提供豐富且一致的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="d9b96-119">As a built-in Ribbon control, the Font Control improves overall font management, selection and formatting functionality, and provides a rich, consistent user experience across all Ribbon applications.</span></span>

<span data-ttu-id="d9b96-120">這種一致的體驗包括</span><span class="sxs-lookup"><span data-stu-id="d9b96-120">This consistent experience includes</span></span>

-   <span data-ttu-id="d9b96-121">跨功能區應用程式標準化格式化和選取字型。</span><span class="sxs-lookup"><span data-stu-id="d9b96-121">Standardized formatting and selection of fonts across Ribbon applications.</span></span>
-   <span data-ttu-id="d9b96-122">跨功能區應用程式的標準化字型標記法。</span><span class="sxs-lookup"><span data-stu-id="d9b96-122">Standardized font representation across Ribbon applications.</span></span>
-   <span data-ttu-id="d9b96-123">自動，在 Windows 7 中，以字型 **[控制台]** 中每個字型的 [**顯示**] 或 [**隱藏**] 設定為基礎的字型啟用。</span><span class="sxs-lookup"><span data-stu-id="d9b96-123">Automatic, in Windows 7, font activation that is based on the **Show** or **Hide** setting for each font in the **Fonts** control panel.</span></span> <span data-ttu-id="d9b96-124">字型控制項只會顯示已設定為 **顯示** 的字型。</span><span class="sxs-lookup"><span data-stu-id="d9b96-124">The Font Control only displays those fonts that are set to **Show**.</span></span>
    > [!Note]  
    > <span data-ttu-id="d9b96-125">在 Windows Vista 中， **[字型** ] 控制台不提供 **顯示** 或 **隱藏** 功能，因此所有字型都會啟用。</span><span class="sxs-lookup"><span data-stu-id="d9b96-125">In Windows Vista, the **Fonts** control panel does not offer the **Show** or **Hide** functionality, so all fonts are activated.</span></span>

     

-   <span data-ttu-id="d9b96-126">可直接從控制項取得的字型管理。</span><span class="sxs-lookup"><span data-stu-id="d9b96-126">Font management that is available directly from the control.</span></span>

    <span data-ttu-id="d9b96-127">下列螢幕擷取畫面顯示可直接從 **字型控制項存取 [字型** ] 控制台。</span><span class="sxs-lookup"><span data-stu-id="d9b96-127">The following screen shot shows that the **Fonts** control panel can be accessed directly from the Font Control.</span></span>

    ![適用于 windows 7 之 wordpad 中的字型系列清單螢幕擷取畫面。](images/controls/fontcontrol-fontcpl.png)

-   <span data-ttu-id="d9b96-129">支援自動預覽。</span><span class="sxs-lookup"><span data-stu-id="d9b96-129">Support for auto-preview.</span></span>
-   <span data-ttu-id="d9b96-130">公開與使用者最相關的字型，例如</span><span class="sxs-lookup"><span data-stu-id="d9b96-130">Exposure of fonts that are most relevant to a user, such as</span></span>
    -   <span data-ttu-id="d9b96-131">國際使用者的當地語系化字型清單。</span><span class="sxs-lookup"><span data-stu-id="d9b96-131">Localized font lists for international users.</span></span>
    -   <span data-ttu-id="d9b96-132">以輸入裝置為基礎的字型清單。</span><span class="sxs-lookup"><span data-stu-id="d9b96-132">Font lists based on input device.</span></span>

    > [!Note]  
    > <span data-ttu-id="d9b96-133">在 Windows 7 之前的任何平臺上，都無法使用此功能的支援。</span><span class="sxs-lookup"><span data-stu-id="d9b96-133">Support for this functionality is not available on any platform older than Windows 7.</span></span>

     

## <a name="easy-integration-and-configuration"></a><span data-ttu-id="d9b96-134">輕鬆整合和設定</span><span class="sxs-lookup"><span data-stu-id="d9b96-134">Easy Integration and Configuration</span></span>

<span data-ttu-id="d9b96-135">藉由提供標準、可重複使用且容易使用的功能，功能區字型控制項可減輕將字型支援整合至應用程式的負擔。</span><span class="sxs-lookup"><span data-stu-id="d9b96-135">By providing standard, reusable, and easily consumed functionality, the Ribbon Font Control eases the burden of integrating font support into an application.</span></span>

<span data-ttu-id="d9b96-136">字型選取和格式的詳細資料會包裝在一個獨立的邏輯元素中，</span><span class="sxs-lookup"><span data-stu-id="d9b96-136">The details of font selection and formatting are wrapped in one, self-contained logical element that</span></span>

-   <span data-ttu-id="d9b96-137">消除了字型控制項執行的複雜控制項相依性管理。</span><span class="sxs-lookup"><span data-stu-id="d9b96-137">Eliminates the complex management of control interdependencies typical of font control implementations.</span></span>
-   <span data-ttu-id="d9b96-138">所有由字型控制項子控制項公開的功能，都需要單一的命令處理常式。</span><span class="sxs-lookup"><span data-stu-id="d9b96-138">Requires a single Command handler for all functionality exposed by the Font Control sub-controls.</span></span>

<span data-ttu-id="d9b96-139">這個單一命令處理常式允許字型控制項在內部管理各種子控制項的功能;子控制項絕不會直接與應用程式互動，而不論其功能為何。</span><span class="sxs-lookup"><span data-stu-id="d9b96-139">This single Command handler allows the Font Control to manage the functionality of various sub-controls internally; a sub-control never interacts directly with the application, regardless of its function.</span></span>

<span data-ttu-id="d9b96-140">字型控制項的其他功能包括</span><span class="sxs-lookup"><span data-stu-id="d9b96-140">Other features of the Font Control include</span></span>

-   <span data-ttu-id="d9b96-141">自動、DPI 感知的 WYSIWYG 世代 (您所看到的內容，就是您在 [ **字型系列** ] 功能表中為每個字型取得) 點陣圖表示的結果。</span><span class="sxs-lookup"><span data-stu-id="d9b96-141">Automatic, DPI-aware generation of a WYSIWYG (what you see is what you get) bitmap representation for each font in the **Font family** menu.</span></span>
-   <span data-ttu-id="d9b96-142">[Windows 圖形裝置介面 (GDI) ](../gdi/windows-gdi.md) 整合。</span><span class="sxs-lookup"><span data-stu-id="d9b96-142">[Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) integration.</span></span>
-   <span data-ttu-id="d9b96-143">當地語系化的字型系列點陣圖和工具提示。</span><span class="sxs-lookup"><span data-stu-id="d9b96-143">Localized font family bitmaps and tooltips.</span></span>
-   <span data-ttu-id="d9b96-144">用來管理和呈現字型的字型列舉、群組和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="d9b96-144">Font enumeration, grouping, and metadata for managing and presenting fonts.</span></span>
    > [!Note]  
    > <span data-ttu-id="d9b96-145">在 Windows 7 之前的任何平臺上，都無法使用此功能的支援。</span><span class="sxs-lookup"><span data-stu-id="d9b96-145">Support for this functionality is not available on any platform older than Windows 7 .</span></span>

     

-   <span data-ttu-id="d9b96-146">反映功能區 [下拉式色彩選擇器](windowsribbon-controls-dropdowncolorpicker.md)行為的 **文字色彩** 和 **文字反白顯示** 色彩下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="d9b96-146">The **Text color** and **Text highlight color** drop-down color pickers that mirror the Ribbon [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md) behavior.</span></span>
-   <span data-ttu-id="d9b96-147">支援以所有字型控制項庫為基礎的子控制項進行自動預覽： **字型家族**、 **字型大小**、 **文字色彩** 和 **文字反白顯示色彩**。</span><span class="sxs-lookup"><span data-stu-id="d9b96-147">Support of auto-previewing by all Font Control gallery-based sub-controls: **Font family**, **Font size**, **Text color**, and **Text highlight color**.</span></span>

## <a name="alignment-with-common-gdi-text-structures"></a><span data-ttu-id="d9b96-148">與常用 GDI 文字結構對齊</span><span class="sxs-lookup"><span data-stu-id="d9b96-148">Alignment with Common GDI Text Structures</span></span>

<span data-ttu-id="d9b96-149">[Windows 圖形裝置介面 (GDI) ](../gdi/windows-gdi.md) 文字堆疊元件可用來透過功能區字型控制項來公開字型選取和格式化功能。</span><span class="sxs-lookup"><span data-stu-id="d9b96-149">[Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) text stack components are used to expose font selection and formatting functionality through the Ribbon Font Control.</span></span> <span data-ttu-id="d9b96-150">[LOGFONT 結構](/windows/win32/api/wingdi/ns-wingdi-logfonta)、 [CHOOSEFONT 結構](/windows/win32/api/commdlg/ns-commdlg-choosefonta)和[CHARFORMAT2 結構](/windows/win32/api/richedit/ns-richedit-charformat2a)所支援的各種字型功能都是透過字型控制項中所包含的子控制項來公開。</span><span class="sxs-lookup"><span data-stu-id="d9b96-150">The various font features supported by the [LOGFONT Structure](/windows/win32/api/wingdi/ns-wingdi-logfonta), [CHOOSEFONT Structure](/windows/win32/api/commdlg/ns-commdlg-choosefonta), and [CHARFORMAT2 Structure](/windows/win32/api/richedit/ns-richedit-charformat2a) are exposed through the sub-controls that are included in the Font Control.</span></span>

<span data-ttu-id="d9b96-151">字型控制項中顯示的子控制項，取決於在功能區標記中宣告的 *FontType* 範本。</span><span class="sxs-lookup"><span data-stu-id="d9b96-151">The sub-controls that are displayed in the Font Control depend on the *FontType* template declared in the Ribbon markup.</span></span> <span data-ttu-id="d9b96-152">下節 (詳細討論的 *FontType* 範本，) 是設計來配合一般 [WINDOWS 圖形裝置介面 (GDI)](../gdi/windows-gdi.md) 文字結構。</span><span class="sxs-lookup"><span data-stu-id="d9b96-152">The *FontType* templates (discussed in further detail in the following section) are designed to align with the common [Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) text structures.</span></span>

## <a name="add-a-fontcontrol"></a><span data-ttu-id="d9b96-153">新增 FontControl</span><span class="sxs-lookup"><span data-stu-id="d9b96-153">Add a FontControl</span></span>

<span data-ttu-id="d9b96-154">本節概述將字型控制項新增至功能區應用程式的基本步驟。</span><span class="sxs-lookup"><span data-stu-id="d9b96-154">This section outlines the basic steps for adding a Font Control to a Ribbon application.</span></span>

### <a name="declaring-a-fontcontrol-in-markup"></a><span data-ttu-id="d9b96-155">在標記中宣告 FontControl</span><span class="sxs-lookup"><span data-stu-id="d9b96-155">Declaring a FontControl in Markup</span></span>

<span data-ttu-id="d9b96-156">如同其他功能區控制項，字型控制項是在具有 [**FontControl**](windowsribbon-element-fontcontrol.md) 專案的標記中宣告，並且透過命令識別碼與命令宣告相關聯。</span><span class="sxs-lookup"><span data-stu-id="d9b96-156">Like other Ribbon controls, the Font Control is declared in markup with a [**FontControl**](windowsribbon-element-fontcontrol.md) element and associated with a Command declaration through a Command ID.</span></span> <span data-ttu-id="d9b96-157">當編譯應用程式時，會使用命令識別碼將命令系結至主應用程式中的命令處理常式。</span><span class="sxs-lookup"><span data-stu-id="d9b96-157">When the application is compiled, the Command ID is used to bind the Command to a Command handler in the host application.</span></span>

> [!Note]  
> <span data-ttu-id="d9b96-158">如果未在標記中使用 [**FontControl**](windowsribbon-element-fontcontrol.md) 宣告任何命令 ID，則架構會產生一個識別碼。</span><span class="sxs-lookup"><span data-stu-id="d9b96-158">If no Command ID is declared with the [**FontControl**](windowsribbon-element-fontcontrol.md) in markup, then one is generated by the framework.</span></span>

 

<span data-ttu-id="d9b96-159">由於不會直接公開字型控制項的子控制項，因此自訂字型控制項僅限於架構所定義的三個 *FontType* 版面配置範本。</span><span class="sxs-lookup"><span data-stu-id="d9b96-159">Because the sub-controls of the Font Control are not exposed directly, customization of the Font Control is limited to three *FontType* layout templates defined by the framework.</span></span>

<span data-ttu-id="d9b96-160">將版面配置範本與 [**FontControl**](windowsribbon-element-fontcontrol.md) 屬性（例如 *IsHighlightButtonVisible*、 *IsStrikethroughButtonVisible* 和 *IsUnderlineButtonVisible*）結合，即可完成字型控制項的自訂。</span><span class="sxs-lookup"><span data-stu-id="d9b96-160">Further customization of the Font Control can be accomplished by combining the layout template with [**FontControl**](windowsribbon-element-fontcontrol.md) attributes such as *IsHighlightButtonVisible*, *IsStrikethroughButtonVisible*, and *IsUnderlineButtonVisible*.</span></span>

> [!Note]  
> <span data-ttu-id="d9b96-161">除了標準字型控制項範本和屬性所公開的字型功能之外，還需要在本文討論範圍之外的自訂字型控制項執行。</span><span class="sxs-lookup"><span data-stu-id="d9b96-161">Font functionality beyond that exposed by the standard Font Control templates and attributes requires a custom font control implementation that is outside the scope of this article.</span></span>

 

<span data-ttu-id="d9b96-162">下表列出字型控制項範本，以及每個範本對齊的編輯控制項類型。</span><span class="sxs-lookup"><span data-stu-id="d9b96-162">The following table lists the Font Control templates and the edit control type that each template is aligned with.</span></span>



| <span data-ttu-id="d9b96-163">範本</span><span class="sxs-lookup"><span data-stu-id="d9b96-163">Template</span></span>      | <span data-ttu-id="d9b96-164">支援</span><span class="sxs-lookup"><span data-stu-id="d9b96-164">Supports</span></span>                                                                 |
|---------------|--------------------------------------------------------------------------|
| <span data-ttu-id="d9b96-165">FontOnly</span><span class="sxs-lookup"><span data-stu-id="d9b96-165">FontOnly</span></span>      | [<span data-ttu-id="d9b96-166">LOGFONT 結構</span><span class="sxs-lookup"><span data-stu-id="d9b96-166">LOGFONT Structure</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)     |
| <span data-ttu-id="d9b96-167">FontWithColor</span><span class="sxs-lookup"><span data-stu-id="d9b96-167">FontWithColor</span></span> | [<span data-ttu-id="d9b96-168">CHOOSEFONT 結構</span><span class="sxs-lookup"><span data-stu-id="d9b96-168">CHOOSEFONT Structure</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)  |
| <span data-ttu-id="d9b96-169">RichFont</span><span class="sxs-lookup"><span data-stu-id="d9b96-169">RichFont</span></span>      | [<span data-ttu-id="d9b96-170">CHARFORMAT2 結構</span><span class="sxs-lookup"><span data-stu-id="d9b96-170">CHARFORMAT2 Structure</span></span>](/windows/win32/api/richedit/ns-richedit-charformat2a) |



 

<span data-ttu-id="d9b96-171">下表列出與每個範本相關聯的控制項，並識別相關聯範本的選擇性控制項。</span><span class="sxs-lookup"><span data-stu-id="d9b96-171">The following table lists the controls that are associated with each template and identifies the controls that are optional for an associated template.</span></span>



<span data-ttu-id="d9b96-172">控制項</span><span class="sxs-lookup"><span data-stu-id="d9b96-172">Controls</span></span>

<span data-ttu-id="d9b96-173">範本</span><span class="sxs-lookup"><span data-stu-id="d9b96-173">Templates</span></span>

<span data-ttu-id="d9b96-174">**RichFont**</span><span class="sxs-lookup"><span data-stu-id="d9b96-174">**RichFont**</span></span>

<span data-ttu-id="d9b96-175">**FontWithColor**</span><span class="sxs-lookup"><span data-stu-id="d9b96-175">**FontWithColor**</span></span>

<span data-ttu-id="d9b96-176">**FontOnly**</span><span class="sxs-lookup"><span data-stu-id="d9b96-176">**FontOnly**</span></span>

<span data-ttu-id="d9b96-177">預設</span><span class="sxs-lookup"><span data-stu-id="d9b96-177">Default</span></span>

<span data-ttu-id="d9b96-178">選擇性</span><span class="sxs-lookup"><span data-stu-id="d9b96-178">Optional</span></span>

<span data-ttu-id="d9b96-179">預設</span><span class="sxs-lookup"><span data-stu-id="d9b96-179">Default</span></span>

<span data-ttu-id="d9b96-180">選擇性</span><span class="sxs-lookup"><span data-stu-id="d9b96-180">Optional</span></span>

<span data-ttu-id="d9b96-181">預設</span><span class="sxs-lookup"><span data-stu-id="d9b96-181">Default</span></span>

<span data-ttu-id="d9b96-182">選擇性</span><span class="sxs-lookup"><span data-stu-id="d9b96-182">Optional</span></span>

<span data-ttu-id="d9b96-183">**字型大小** 下拉式方塊</span><span class="sxs-lookup"><span data-stu-id="d9b96-183">**Font size** combo box</span></span>

<span data-ttu-id="d9b96-184">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-184">Yes</span></span>

<span data-ttu-id="d9b96-185">否</span><span class="sxs-lookup"><span data-stu-id="d9b96-185">No</span></span>

<span data-ttu-id="d9b96-186">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-186">Yes</span></span>

<span data-ttu-id="d9b96-187">否</span><span class="sxs-lookup"><span data-stu-id="d9b96-187">No</span></span>

<span data-ttu-id="d9b96-188">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-188">Yes</span></span>

<span data-ttu-id="d9b96-189">否</span><span class="sxs-lookup"><span data-stu-id="d9b96-189">No</span></span>

<span data-ttu-id="d9b96-190">**字型家族** 下拉式方塊</span><span class="sxs-lookup"><span data-stu-id="d9b96-190">**Font family** combo box</span></span>

<span data-ttu-id="d9b96-191">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-191">Yes</span></span>

<span data-ttu-id="d9b96-192">否</span><span class="sxs-lookup"><span data-stu-id="d9b96-192">No</span></span>

<span data-ttu-id="d9b96-193">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-193">Yes</span></span>

<span data-ttu-id="d9b96-194">否</span><span class="sxs-lookup"><span data-stu-id="d9b96-194">No</span></span>

<span data-ttu-id="d9b96-195">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-195">Yes</span></span>

<span data-ttu-id="d9b96-196">否</span><span class="sxs-lookup"><span data-stu-id="d9b96-196">No</span></span>

<span data-ttu-id="d9b96-197">**放大字型** 按鈕</span><span class="sxs-lookup"><span data-stu-id="d9b96-197">**Grow font** button</span></span>

<span data-ttu-id="d9b96-198">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-198">Yes</span></span>

<span data-ttu-id="d9b96-199">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-199">Yes</span></span>

<span data-ttu-id="d9b96-200">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-200">Yes</span></span>

<span data-ttu-id="d9b96-201">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-201">Yes</span></span>

\-

\-

<span data-ttu-id="d9b96-202">**壓縮字型** 按鈕</span><span class="sxs-lookup"><span data-stu-id="d9b96-202">**Shrink font** button</span></span>

<span data-ttu-id="d9b96-203">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-203">Yes</span></span>

<span data-ttu-id="d9b96-204">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-204">Yes</span></span>

<span data-ttu-id="d9b96-205">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-205">Yes</span></span>

<span data-ttu-id="d9b96-206">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-206">Yes</span></span>

\-

\-

<span data-ttu-id="d9b96-207">**粗體** 按鈕</span><span class="sxs-lookup"><span data-stu-id="d9b96-207">**Bold** button</span></span>

<span data-ttu-id="d9b96-208">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-208">Yes</span></span>

<span data-ttu-id="d9b96-209">否</span><span class="sxs-lookup"><span data-stu-id="d9b96-209">No</span></span>

<span data-ttu-id="d9b96-210">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-210">Yes</span></span>

<span data-ttu-id="d9b96-211">否</span><span class="sxs-lookup"><span data-stu-id="d9b96-211">No</span></span>

<span data-ttu-id="d9b96-212">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-212">Yes</span></span>

<span data-ttu-id="d9b96-213">否</span><span class="sxs-lookup"><span data-stu-id="d9b96-213">No</span></span>

<span data-ttu-id="d9b96-214">**斜體** 按鈕</span><span class="sxs-lookup"><span data-stu-id="d9b96-214">**Italic** button</span></span>

<span data-ttu-id="d9b96-215">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-215">Yes</span></span>

<span data-ttu-id="d9b96-216">否</span><span class="sxs-lookup"><span data-stu-id="d9b96-216">No</span></span>

<span data-ttu-id="d9b96-217">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-217">Yes</span></span>

<span data-ttu-id="d9b96-218">否</span><span class="sxs-lookup"><span data-stu-id="d9b96-218">No</span></span>

<span data-ttu-id="d9b96-219">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-219">Yes</span></span>

<span data-ttu-id="d9b96-220">否</span><span class="sxs-lookup"><span data-stu-id="d9b96-220">No</span></span>

<span data-ttu-id="d9b96-221">底線按鈕</span><span class="sxs-lookup"><span data-stu-id="d9b96-221">**Underline** button</span></span>

<span data-ttu-id="d9b96-222">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-222">Yes</span></span>

<span data-ttu-id="d9b96-223">否</span><span class="sxs-lookup"><span data-stu-id="d9b96-223">No</span></span>

<span data-ttu-id="d9b96-224">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-224">Yes</span></span>

<span data-ttu-id="d9b96-225">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-225">Yes</span></span>

<span data-ttu-id="d9b96-226">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-226">Yes</span></span>

<span data-ttu-id="d9b96-227">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-227">Yes</span></span>

<span data-ttu-id="d9b96-228">**刪除線** 按鈕</span><span class="sxs-lookup"><span data-stu-id="d9b96-228">**Strikethrough** button</span></span>

<span data-ttu-id="d9b96-229">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-229">Yes</span></span>

<span data-ttu-id="d9b96-230">否</span><span class="sxs-lookup"><span data-stu-id="d9b96-230">No</span></span>

<span data-ttu-id="d9b96-231">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-231">Yes</span></span>

<span data-ttu-id="d9b96-232">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-232">Yes</span></span>

<span data-ttu-id="d9b96-233">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-233">Yes</span></span>

<span data-ttu-id="d9b96-234">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-234">Yes</span></span>

<span data-ttu-id="d9b96-235">注 **標** 按鈕</span><span class="sxs-lookup"><span data-stu-id="d9b96-235">**Subscript** button</span></span>

<span data-ttu-id="d9b96-236">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-236">Yes</span></span>

<span data-ttu-id="d9b96-237">否</span><span class="sxs-lookup"><span data-stu-id="d9b96-237">No</span></span>

\-

\-

\-

\-

<span data-ttu-id="d9b96-238">**上標** 按鈕</span><span class="sxs-lookup"><span data-stu-id="d9b96-238">**Superscript** button</span></span>

<span data-ttu-id="d9b96-239">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-239">Yes</span></span>

<span data-ttu-id="d9b96-240">否</span><span class="sxs-lookup"><span data-stu-id="d9b96-240">No</span></span>

\-

\-

\-

\-

<span data-ttu-id="d9b96-241">**文字反白顯示色彩** 按鈕</span><span class="sxs-lookup"><span data-stu-id="d9b96-241">**Text highlight color** button</span></span>

<span data-ttu-id="d9b96-242">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-242">Yes</span></span>

<span data-ttu-id="d9b96-243">否</span><span class="sxs-lookup"><span data-stu-id="d9b96-243">No</span></span>

<span data-ttu-id="d9b96-244">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-244">Yes</span></span>

<span data-ttu-id="d9b96-245">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-245">Yes</span></span>

\-

\-

<span data-ttu-id="d9b96-246">**文字色彩** 按鈕</span><span class="sxs-lookup"><span data-stu-id="d9b96-246">**Text color** button</span></span>

<span data-ttu-id="d9b96-247">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-247">Yes</span></span>

<span data-ttu-id="d9b96-248">否</span><span class="sxs-lookup"><span data-stu-id="d9b96-248">No</span></span>

<span data-ttu-id="d9b96-249">是</span><span class="sxs-lookup"><span data-stu-id="d9b96-249">Yes</span></span>

<span data-ttu-id="d9b96-250">否</span><span class="sxs-lookup"><span data-stu-id="d9b96-250">No</span></span>

\-

\-



 

<span data-ttu-id="d9b96-251">當您宣告字型控制項的版面配置行為時，功能區架構會提供選擇性的 *SizeDefinition* 版面配置範本， `OneFontControl` 它會根據功能區大小和字型控制項可用的空間，定義兩個子控制項設定。</span><span class="sxs-lookup"><span data-stu-id="d9b96-251">When the layout behavior of a Font Control is declared, the Ribbon framework provides an optional *SizeDefinition* layout template, `OneFontControl`, that defines two sub-control configurations based on the size of the Ribbon and the space available for the Font Control.</span></span> <span data-ttu-id="d9b96-252">如需詳細資訊，請參閱 [透過大小定義自訂功能區和調整原則](windowsribbon-templates.md)。</span><span class="sxs-lookup"><span data-stu-id="d9b96-252">For more information, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

### <a name="adding-a-fontcontrol-to-a-ribbon"></a><span data-ttu-id="d9b96-253">將 FontControl 新增至功能區</span><span class="sxs-lookup"><span data-stu-id="d9b96-253">Adding a FontControl to a Ribbon</span></span>

<span data-ttu-id="d9b96-254">下列程式碼範例示範將字型控制項新增至功能區的基本標記需求：</span><span class="sxs-lookup"><span data-stu-id="d9b96-254">The following code examples demonstrate the basic markup requirements for adding a Font Control to a Ribbon:</span></span>

<span data-ttu-id="d9b96-255">這段程式碼會顯示 [**FontControl**](windowsribbon-element-fontcontrol.md)命令宣告標記，包括在 [**功能區**](windowsribbon-element-ribbon.md)中顯示控制項所需的 [**Tab**](windowsribbon-element-tab.md)和 [**Group**](windowsribbon-element-group.md)命令。</span><span class="sxs-lookup"><span data-stu-id="d9b96-255">This section of code shows the [**FontControl**](windowsribbon-element-fontcontrol.md) Command declaration markup, including the [**Tab**](windowsribbon-element-tab.md) and [**Group**](windowsribbon-element-group.md) Commands that are required for displaying a control in the [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>


```C++
<Command Name="cmdTab1"
  Comment="These comments are optional and are inserted into the header file."
  Symbol="cmdTab1" Id="10000" >
  <Command.LabelTitle>Tab 1</Command.LabelTitle>
</Command>
<Command Name="cmdGroup1" Comment="Group #1" Symbol="cmdGroup1" Id="20000">
  <!-- This image is used when the group scales to a pop-up. -->
  <Command.SmallImages>
    <Image>res/Button_Image.bmp</Image>
  </Command.SmallImages>
</Command>
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



<span data-ttu-id="d9b96-256">這一節的程式碼顯示使用命令識別碼來宣告 [**FontControl**](windowsribbon-element-fontcontrol.md) 與 [**命令**](windowsribbon-element-command.md) 的必要標記。</span><span class="sxs-lookup"><span data-stu-id="d9b96-256">This section of code shows the markup required to declare and associate a [**FontControl**](windowsribbon-element-fontcontrol.md) with a [**Command**](windowsribbon-element-command.md) through a Command ID.</span></span> <span data-ttu-id="d9b96-257">此特定範例包括索引標籤和 [**群組**](windowsribbon-element-group.md)宣告 [**，以及縮放**](windowsribbon-element-tab.md)喜好設定。</span><span class="sxs-lookup"><span data-stu-id="d9b96-257">This particular example includes the [**Tab**](windowsribbon-element-tab.md) and [**Group**](windowsribbon-element-group.md) declarations, with scaling preferences.</span></span>


```C++
<Ribbon.Tabs>
  <Tab CommandName="cmdTab1">
    <Tab.ScalingPolicy>
      <ScalingPolicy>
        <ScalingPolicy.IdealSizes>
          <Scale Group="cmdGroup1" Size="Large" />
        </ScalingPolicy.IdealSizes>
        <!-- Describe how the FontControl group scales. -->
        <Scale Group="cmdGroup1" Size="Medium" />
        <Scale Group="cmdGroup1" Size="Popup" />
      </ScalingPolicy>
    <Group CommandName="cmdGroup1" SizeDefinition="OneFontControl">
      <FontControl CommandName="cmdFontControl" FontType="RichFont" />
    </Group>
  </Tab>
</Ribbon.Tabs>
```



### <a name="adding-a-fontcontrol-to-a-contextpopup"></a><span data-ttu-id="d9b96-258">將 FontControl 新增至 CoNtextPopup</span><span class="sxs-lookup"><span data-stu-id="d9b96-258">Adding a FontControl to a ContextPopup</span></span>

<span data-ttu-id="d9b96-259">將字型控制項新增至 [內容快顯視窗](windowsribbon-controls-contextpopup.md) ，需要的程式類似于將字型控制項加入功能區。</span><span class="sxs-lookup"><span data-stu-id="d9b96-259">Adding a Font Control to a [Context Popup](windowsribbon-controls-contextpopup.md) requires a procedure similar to that of adding a Font Control to the Ribbon.</span></span> <span data-ttu-id="d9b96-260">不過， [**浮動工具列**](windowsribbon-element-minitoolbar.md) 中的字型控制項受限於所有字型控制項範本通用的預設子控制項集： **字型家族**、 **字型大小**、 **粗體** 和 **斜體**。</span><span class="sxs-lookup"><span data-stu-id="d9b96-260">However, a Font Control in a [**MiniToolbar**](windowsribbon-element-minitoolbar.md) is restricted to the set of default sub-controls that are common to all Font Control templates: **Font family**, **Font size**, **Bold**, and **Italic**.</span></span>

<span data-ttu-id="d9b96-261">下列程式碼範例示範將字型控制項新增至 [內容快顯視窗](windowsribbon-controls-contextpopup.md)的基本標記需求：</span><span class="sxs-lookup"><span data-stu-id="d9b96-261">The following code examples demonstrate the basic markup requirements for adding a Font Control to a [Context Popup](windowsribbon-controls-contextpopup.md):</span></span>

<span data-ttu-id="d9b96-262">這段程式碼會顯示在 [**CoNtextPopup**](windowsribbon-element-contextpopup.md)中顯示 **FontControl** 所需的 [**FontControl**](windowsribbon-element-fontcontrol.md)命令宣告標記。</span><span class="sxs-lookup"><span data-stu-id="d9b96-262">This section of code shows the [**FontControl**](windowsribbon-element-fontcontrol.md) Command declaration markup that is required for displaying a **FontControl** in the [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" />
```



<span data-ttu-id="d9b96-263">這一節的程式碼顯示使用命令識別碼來宣告 [**FontControl**](windowsribbon-element-fontcontrol.md) 與命令的必要標記。</span><span class="sxs-lookup"><span data-stu-id="d9b96-263">This section of code shows the markup required to declare and associate a [**FontControl**](windowsribbon-element-fontcontrol.md) with a Command through a Command ID.</span></span>


```C++
<ContextPopup.MiniToolbars>
  <MiniToolBar Name="MiniToolbar1">
    <MenuCategory Class="StandardItems">
      <FontControl CommandName="cmdFontControl" />
    </MenuCategory>
  </MiniToolBar>
</ContextPopup.MiniToolbars>
```



### <a name="keytips"></a><span data-ttu-id="d9b96-264">按鍵提示</span><span class="sxs-lookup"><span data-stu-id="d9b96-264">Keytips</span></span>

<span data-ttu-id="d9b96-265">功能區字型控制項中的每個子控制項都可以透過鍵盤快速鍵或 keytip 來存取。</span><span class="sxs-lookup"><span data-stu-id="d9b96-265">Each sub-control in the Ribbon Font Control is accessible through a keyboard shortcut, or keytip.</span></span> <span data-ttu-id="d9b96-266">此快捷方式已預先定義，並由架構指派給每個子控制項。</span><span class="sxs-lookup"><span data-stu-id="d9b96-266">This keytip is predefined and assigned to each sub-control by the framework.</span></span>

<span data-ttu-id="d9b96-267">如果在標記中將 [ *快速鍵* ] 屬性值指派給 [**FontControl**](windowsribbon-element-fontcontrol.md) 元素，則會將此值新增為架構定義之 Keytip 的前置詞。</span><span class="sxs-lookup"><span data-stu-id="d9b96-267">If a *Keytip* attribute value is assigned to the [**FontControl**](windowsribbon-element-fontcontrol.md) element in markup, this value is added as a prefix to the framework-defined keytip.</span></span>

> [!Note]  
> <span data-ttu-id="d9b96-268">應用程式應該為此前置詞強制採用單一字元的規則。</span><span class="sxs-lookup"><span data-stu-id="d9b96-268">The application should enforce a single-character rule for this prefix.</span></span>

 

<span data-ttu-id="d9b96-269">下表列出由架構所定義的按鍵提示。</span><span class="sxs-lookup"><span data-stu-id="d9b96-269">The following table lists the keytips defined by the framework.</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d9b96-270">子控制項</span><span class="sxs-lookup"><span data-stu-id="d9b96-270">Sub-control</span></span></th>
<th><span data-ttu-id="d9b96-271">Keytip</span><span class="sxs-lookup"><span data-stu-id="d9b96-271">Keytip</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d9b96-272">字型家族</span><span class="sxs-lookup"><span data-stu-id="d9b96-272">Font family</span></span></td>
<td><span data-ttu-id="d9b96-273">F</span><span class="sxs-lookup"><span data-stu-id="d9b96-273">F</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9b96-274">字型樣式</span><span class="sxs-lookup"><span data-stu-id="d9b96-274">Font style</span></span></td>
<td><span data-ttu-id="d9b96-275">T</span><span class="sxs-lookup"><span data-stu-id="d9b96-275">T</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9b96-276">字型大小</span><span class="sxs-lookup"><span data-stu-id="d9b96-276">Font size</span></span></td>
<td><span data-ttu-id="d9b96-277">S</span><span class="sxs-lookup"><span data-stu-id="d9b96-277">S</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9b96-278">成長字型</span><span class="sxs-lookup"><span data-stu-id="d9b96-278">Grow font</span></span></td>
<td><span data-ttu-id="d9b96-279">G</span><span class="sxs-lookup"><span data-stu-id="d9b96-279">G</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9b96-280">壓縮字型</span><span class="sxs-lookup"><span data-stu-id="d9b96-280">Shrink font</span></span></td>
<td><span data-ttu-id="d9b96-281">K</span><span class="sxs-lookup"><span data-stu-id="d9b96-281">K</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9b96-282">粗體</span><span class="sxs-lookup"><span data-stu-id="d9b96-282">Bold</span></span></td>
<td><span data-ttu-id="d9b96-283">B</span><span class="sxs-lookup"><span data-stu-id="d9b96-283">B</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9b96-284">斜體</span><span class="sxs-lookup"><span data-stu-id="d9b96-284">Italic</span></span></td>
<td><span data-ttu-id="d9b96-285">I</span><span class="sxs-lookup"><span data-stu-id="d9b96-285">I</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9b96-286">Underline</span><span class="sxs-lookup"><span data-stu-id="d9b96-286">Underline</span></span></td>
<td><span data-ttu-id="d9b96-287">U</span><span class="sxs-lookup"><span data-stu-id="d9b96-287">U</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9b96-288">刪除線</span><span class="sxs-lookup"><span data-stu-id="d9b96-288">Strikethrough</span></span></td>
<td><span data-ttu-id="d9b96-289">X</span><span class="sxs-lookup"><span data-stu-id="d9b96-289">X</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9b96-290">標</span><span class="sxs-lookup"><span data-stu-id="d9b96-290">Superscript</span></span></td>
<td><span data-ttu-id="d9b96-291">Y 或 Z</span><span class="sxs-lookup"><span data-stu-id="d9b96-291">Y or Z</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="d9b96-292">如果 [ <em>快速鍵</em> ] 屬性未在標記中宣告，則預設的快速鍵提示為 Y;否則，預設的快速鍵提示會是 <em>keytip</em> + Z。</span><span class="sxs-lookup"><span data-stu-id="d9b96-292">If the <em>Keytip</em> attribute is not declared in markup, the default keytip is Y; otherwise, the default keytip is <em>Keytip</em> + Z.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9b96-293">標</span><span class="sxs-lookup"><span data-stu-id="d9b96-293">Subscript</span></span></td>
<td><span data-ttu-id="d9b96-294">A</span><span class="sxs-lookup"><span data-stu-id="d9b96-294">A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9b96-295">字型色彩</span><span class="sxs-lookup"><span data-stu-id="d9b96-295">Font color</span></span></td>
<td><span data-ttu-id="d9b96-296">C</span><span class="sxs-lookup"><span data-stu-id="d9b96-296">C</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9b96-297">字型醒目提示</span><span class="sxs-lookup"><span data-stu-id="d9b96-297">Font highlight</span></span></td>
<td><span data-ttu-id="d9b96-298">H</span><span class="sxs-lookup"><span data-stu-id="d9b96-298">H</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d9b96-299">多語系消費者介面 (MUI 的建議首碼) EN-US 功能區是 ' F '，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="d9b96-299">The recommended prefix for a Multilingual User Interface (MUI) EN-US Ribbon is 'F', as shown in the following example.</span></span>


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



<span data-ttu-id="d9b96-300">下列螢幕擷取畫面說明字型控制項按鍵提示，因為它們是在上一個範例中定義的。</span><span class="sxs-lookup"><span data-stu-id="d9b96-300">The following screen shot illustrates the Font Control keytips as they are defined in the previous example.</span></span>

![適用于 windows 7 之 wordpad 中的 fontcontrol 按鍵提示螢幕擷取畫面。](images/controls/fontcontrol-keytips.png)

### <a name="the-ribbon-resource-file"></a><span data-ttu-id="d9b96-302">功能區資源檔</span><span class="sxs-lookup"><span data-stu-id="d9b96-302">The Ribbon Resource File</span></span>

<span data-ttu-id="d9b96-303">編譯標記檔案時，會產生包含功能區應用程式之所有資源參考的資源檔。</span><span class="sxs-lookup"><span data-stu-id="d9b96-303">When the markup file is compiled, a resource file that contains all resource references for the Ribbon application is generated.</span></span>

<span data-ttu-id="d9b96-304">簡單資源檔的範例：</span><span class="sxs-lookup"><span data-stu-id="d9b96-304">Example of a simple resource file:</span></span>


```C++
// ******************************************************************************
// * This is an automatically generated file containing the ribbon resource for *
// * your application.                                                          *
// ******************************************************************************

#include ".\ids.h"

STRINGTABLE 
BEGIN
  cmdTab1_LabelTitle_RESID L"Tab 1" 
    /* LabelTitle cmdTab1_LabelTitle_RESID: These comments are optional and are 
       inserted into the header file. */
END

cmdGroup1_SmallImages_RESID    BITMAP    "res\\Button_Image.bmp" 
  /* SmallImages cmdGroup1_SmallImages_RESID: Group #1 */
STRINGTABLE 
BEGIN
  cmdFontControl_Keytip_RESID L"F" /* Keytip cmdFontControl_Keytip_RESID: FontControl */
END

FCSAMPLE_RIBBON    UIFILE    "Debug\\FCSample.bml"

```



### <a name="font-control-properties"></a><span data-ttu-id="d9b96-305">字型控制項屬性</span><span class="sxs-lookup"><span data-stu-id="d9b96-305">Font Control Properties</span></span>

<span data-ttu-id="d9b96-306">功能區架構會為字型控制項和其組成子控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。</span><span class="sxs-lookup"><span data-stu-id="d9b96-306">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Font Control and its constituent sub-controls.</span></span>

<span data-ttu-id="d9b96-307">一般而言，字型控制項屬性會在功能區 UI 中更新，方法是透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效。</span><span class="sxs-lookup"><span data-stu-id="d9b96-307">Typically, a Font Control property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="d9b96-308">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。</span><span class="sxs-lookup"><span data-stu-id="d9b96-308">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="d9b96-309">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。</span><span class="sxs-lookup"><span data-stu-id="d9b96-309">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="d9b96-310">例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。</span><span class="sxs-lookup"><span data-stu-id="d9b96-310">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="d9b96-311">在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。</span><span class="sxs-lookup"><span data-stu-id="d9b96-311">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="d9b96-312">下表列出與字型控制項相關聯的屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="d9b96-312">The following table lists the property keys that are associated with the Font Control.</span></span>



| <span data-ttu-id="d9b96-313">屬性索引鍵</span><span class="sxs-lookup"><span data-stu-id="d9b96-313">Property Key</span></span>                                                                                                                  | <span data-ttu-id="d9b96-314">備註</span><span class="sxs-lookup"><span data-stu-id="d9b96-314">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d9b96-315">UI \_ PKEY \_ FontProperties</span><span class="sxs-lookup"><span data-stu-id="d9b96-315">UI\_PKEY\_FontProperties</span></span>](windowsribbon-reference-properties-uipkey-fontproperties.md)                                      | <span data-ttu-id="d9b96-316">將匯總中的 [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) 物件公開為所有字型控制項子控制項屬性。</span><span class="sxs-lookup"><span data-stu-id="d9b96-316">Exposes, in aggregate as an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) object, all Font Control sub-control properties.</span></span><br/> <span data-ttu-id="d9b96-317">當 `UI_INVALIDATIONS_VALUE` 做為 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand)呼叫中的 *旗標* 值傳遞時，架構會查詢這個屬性。</span><span class="sxs-lookup"><span data-stu-id="d9b96-317">The framework queries this property when `UI_INVALIDATIONS_VALUE` is passed as the value of *flags* in the call to [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span></span><br/> |
| [<span data-ttu-id="d9b96-318">UI \_ PKEY \_ FontProperties \_ ChangedProperties</span><span class="sxs-lookup"><span data-stu-id="d9b96-318">UI\_PKEY\_FontProperties\_ChangedProperties</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md) | <span data-ttu-id="d9b96-319">在匯總中公開為 [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) 物件，只有已變更的字型控制項子控制項屬性。</span><span class="sxs-lookup"><span data-stu-id="d9b96-319">Exposes, in aggregate as an [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object, only Font Control sub-control properties that have changed.</span></span><br/>                                                                                                                                                                                                        |
| [<span data-ttu-id="d9b96-320">UI \_ PKEY \_ 按鍵提示</span><span class="sxs-lookup"><span data-stu-id="d9b96-320">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                                                      | <span data-ttu-id="d9b96-321">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="d9b96-321">Can only be updated through invalidation.</span></span>                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="d9b96-322">UI \_ PKEY \_ 已啟用</span><span class="sxs-lookup"><span data-stu-id="d9b96-322">UI\_PKEY\_Enabled</span></span>](windowsribbon-reference-properties-uipkey-enabled.md)                                                    | <span data-ttu-id="d9b96-323">支援 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 和 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)。</span><span class="sxs-lookup"><span data-stu-id="d9b96-323">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span>                                                                                                                                                                  |



 

<span data-ttu-id="d9b96-324">除了字型控制項本身所支援的屬性之外，功能區架構也會定義每個字型控制項子控制項的 [屬性索引鍵](windowsribbon-reference-properties.md) 。</span><span class="sxs-lookup"><span data-stu-id="d9b96-324">In addition to the properties supported by the Font Control itself, the Ribbon framework also defines a [property key](windowsribbon-reference-properties.md) for each Font Control sub-control.</span></span> <span data-ttu-id="d9b96-325">架構會透過 [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面執行來公開這些屬性索引鍵及其值，此介面會定義用來管理集合的方法，也稱為屬性包（名稱和值組）。</span><span class="sxs-lookup"><span data-stu-id="d9b96-325">These property keys and their values are exposed by the framework through an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface implementation that defines the methods for managing a collection, also called a property bag, of name and value pairs.</span></span>

<span data-ttu-id="d9b96-326">應用程式會將字型結構轉譯成可透過 [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面方法存取的屬性。</span><span class="sxs-lookup"><span data-stu-id="d9b96-326">The application translates the font structures to properties that are accessible through the [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface methods.</span></span> <span data-ttu-id="d9b96-327">此模型強調字型控制項和 Windows 圖形裝置介面 (GDI) 文字堆疊元件之間的差異， ([LOGFONT 結構](/windows/win32/api/wingdi/ns-wingdi-logfonta)、 [CHOOSEFONT 結構](/windows/win32/api/commdlg/ns-commdlg-choosefonta)，以及 Framework 所支援的 [CHARFORMAT2 結構](/windows/win32/api/richedit/ns-richedit-charformat2a)) 。</span><span class="sxs-lookup"><span data-stu-id="d9b96-327">This model emphasizes the distinction between the Font Control and the Windows Graphics Device Interface (GDI) text stack components ([LOGFONT Structure](/windows/win32/api/wingdi/ns-wingdi-logfonta), [CHOOSEFONT Structure](/windows/win32/api/commdlg/ns-commdlg-choosefonta), and [CHARFORMAT2 Structure](/windows/win32/api/richedit/ns-richedit-charformat2a)) that are supported by the framework.</span></span>

<span data-ttu-id="d9b96-328">下表列出個別控制項與其相關聯的屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="d9b96-328">The following table lists the individual controls and their associated property keys.</span></span>



| <span data-ttu-id="d9b96-329">控制項</span><span class="sxs-lookup"><span data-stu-id="d9b96-329">Controls</span></span>                 | <span data-ttu-id="d9b96-330">屬性索引鍵</span><span class="sxs-lookup"><span data-stu-id="d9b96-330">Property Key</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="d9b96-331">備註</span><span class="sxs-lookup"><span data-stu-id="d9b96-331">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9b96-332">**字型大小**</span><span class="sxs-lookup"><span data-stu-id="d9b96-332">**Font size**</span></span>            | [<span data-ttu-id="d9b96-333">UI \_ PKEY \_ FontProperties \_ 大小</span><span class="sxs-lookup"><span data-stu-id="d9b96-333">UI\_PKEY\_FontProperties\_Size</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | <span data-ttu-id="d9b96-334">反白顯示執行 heterogeneously 大小的文字時，功能區架構會將 **字型大小** 控制項設定為空白，並將 [UI \_ PKEY \_ FontProperties \_ 大小](windowsribbon-reference-properties-uipkey-fontproperties-size.md) 的值設定為0。</span><span class="sxs-lookup"><span data-stu-id="d9b96-334">When a run of heterogeneously sized text is highlighted, the Ribbon framework sets the **Font size** control to blank and the value of [UI\_PKEY\_FontProperties\_Size](windowsribbon-reference-properties-uipkey-fontproperties-size.md) to 0.</span></span> <span data-ttu-id="d9b96-335">按一下 [ **成長字型** ] 或 [ **縮小字型** ] 按鈕時，會重設所有反白顯示的文字大小，但會保留文字大小的相對差異。</span><span class="sxs-lookup"><span data-stu-id="d9b96-335">When the **Grow font** or **Shrink font** button is clicked, all highlighted text is resized but the relative difference in text sizes is preserved.</span></span>                                                                                                                                                    |
| <span data-ttu-id="d9b96-336">**字型家族**</span><span class="sxs-lookup"><span data-stu-id="d9b96-336">**Font family**</span></span>          | [<span data-ttu-id="d9b96-337">UI \_ PKEY \_ FontProperties \_ 系列</span><span class="sxs-lookup"><span data-stu-id="d9b96-337">UI\_PKEY\_FontProperties\_Family</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-family.md)                                                                                                                                                                | <span data-ttu-id="d9b96-338">GDI 字型系列名稱會隨著系統地區設定而有所不同。</span><span class="sxs-lookup"><span data-stu-id="d9b96-338">GDI font family names vary with system locale.</span></span> <span data-ttu-id="d9b96-339">因此，如果在應用程式會話之間保留 [UI \_ PKEY \_ FontProperties \_ 系列](windowsribbon-reference-properties-uipkey-fontproperties-family.md) 的值，則應該在每個新的會話上取出該值。</span><span class="sxs-lookup"><span data-stu-id="d9b96-339">As such, if the value of [UI\_PKEY\_FontProperties\_Family](windowsribbon-reference-properties-uipkey-fontproperties-family.md) is preserved across application sessions, that value should be retrieved on each new session.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="d9b96-340">**成長字型**</span><span class="sxs-lookup"><span data-stu-id="d9b96-340">**Grow font**</span></span>            | [<span data-ttu-id="d9b96-341">UI \_ PKEY \_ FontProperties \_ 大小</span><span class="sxs-lookup"><span data-stu-id="d9b96-341">UI\_PKEY\_FontProperties\_Size</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | <span data-ttu-id="d9b96-342">請參閱 **字型大小**。</span><span class="sxs-lookup"><span data-stu-id="d9b96-342">See **Font size**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="d9b96-343">**壓縮字型**</span><span class="sxs-lookup"><span data-stu-id="d9b96-343">**Shrink font**</span></span>          | [<span data-ttu-id="d9b96-344">UI \_ PKEY \_ FontProperties \_ 大小</span><span class="sxs-lookup"><span data-stu-id="d9b96-344">UI\_PKEY\_FontProperties\_Size</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | <span data-ttu-id="d9b96-345">請參閱 **字型大小**。</span><span class="sxs-lookup"><span data-stu-id="d9b96-345">See **Font size**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="d9b96-346">**粗體字**</span><span class="sxs-lookup"><span data-stu-id="d9b96-346">**Bold**</span></span>                 | [<span data-ttu-id="d9b96-347">UI \_ PKEY \_ FontProperties \_ Bold</span><span class="sxs-lookup"><span data-stu-id="d9b96-347">UI\_PKEY\_FontProperties\_Bold</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-bold.md)                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d9b96-348">**斜體**</span><span class="sxs-lookup"><span data-stu-id="d9b96-348">**Italic**</span></span>               | [<span data-ttu-id="d9b96-349">UI \_ PKEY \_ FontProperties \_ 斜體</span><span class="sxs-lookup"><span data-stu-id="d9b96-349">UI\_PKEY\_FontProperties\_Italic</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-italic.md)                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d9b96-350">**Underline**</span><span class="sxs-lookup"><span data-stu-id="d9b96-350">**Underline**</span></span>            | [<span data-ttu-id="d9b96-351">UI \_ PKEY \_ FontProperties \_ 波浪線</span><span class="sxs-lookup"><span data-stu-id="d9b96-351">UI\_PKEY\_FontProperties\_Underline</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-underline.md)                                                                                                                                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d9b96-352">**刪除線**</span><span class="sxs-lookup"><span data-stu-id="d9b96-352">**Strikethrough**</span></span>        | [<span data-ttu-id="d9b96-353">UI \_ PKEY \_ FontProperties \_ 刪除線</span><span class="sxs-lookup"><span data-stu-id="d9b96-353">UI\_PKEY\_FontProperties\_Strikethrough</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-strikethrough.md)                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d9b96-354">**標**</span><span class="sxs-lookup"><span data-stu-id="d9b96-354">**Subscript**</span></span>            | [<span data-ttu-id="d9b96-355">UI \_ PKEY \_ FontProperties \_ VerticalPositioning</span><span class="sxs-lookup"><span data-stu-id="d9b96-355">UI\_PKEY\_FontProperties\_VerticalPositioning</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | <span data-ttu-id="d9b96-356">如果設定了 [注 **標** ] 按鈕，則也無法設定 **上標** 。</span><span class="sxs-lookup"><span data-stu-id="d9b96-356">If the **Subscript** button is set, then the **Superscript** cannot also be set.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="d9b96-357">**標**</span><span class="sxs-lookup"><span data-stu-id="d9b96-357">**Superscript**</span></span>          | [<span data-ttu-id="d9b96-358">UI \_ PKEY \_ FontProperties \_ VerticalPositioning</span><span class="sxs-lookup"><span data-stu-id="d9b96-358">UI\_PKEY\_FontProperties\_VerticalPositioning</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | <span data-ttu-id="d9b96-359">如果設定了 **上標** 按鈕，則也不能設定注 **標** 。</span><span class="sxs-lookup"><span data-stu-id="d9b96-359">If the **Superscript** button is set, then the **Subscript** cannot also be set.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="d9b96-360">**文字反白顯示色彩**</span><span class="sxs-lookup"><span data-stu-id="d9b96-360">**Text highlight color**</span></span> | <span data-ttu-id="d9b96-361">[UI \_PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor)、 [UI \_ PKEY \_ FontProperties \_ BackgroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolortype.md)</span><span class="sxs-lookup"><span data-stu-id="d9b96-361">[UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), [UI\_PKEY\_FontProperties\_BackgroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolortype.md)</span></span> | <span data-ttu-id="d9b96-362">提供與 `HighlightColors` [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) 元素之範本相同的功能。</span><span class="sxs-lookup"><span data-stu-id="d9b96-362">Provides the same functionality as the `HighlightColors` template of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) element.</span></span><br/> <span data-ttu-id="d9b96-363">強烈建議您只設定應用程式所需的初始 **文字醒目提示色彩** 值。</span><span class="sxs-lookup"><span data-stu-id="d9b96-363">We highly recommend that only an initial **Text highlight color** value be set by the application.</span></span> <span data-ttu-id="d9b96-364">當游標在檔內重新置放時，應該保留最後一個選取的值，而且不會設定。</span><span class="sxs-lookup"><span data-stu-id="d9b96-364">The last selected value should be preserved and not set when the cursor is repositioned within a document.</span></span> <span data-ttu-id="d9b96-365">這可讓使用者快速存取最後選取的專案，而不需要重新開啟色彩選擇器。</span><span class="sxs-lookup"><span data-stu-id="d9b96-365">This allows quick access to the user's last selection, and the color picker does not have to be reopened.</span></span><br/> <span data-ttu-id="d9b96-366">無法自訂色彩色板。</span><span class="sxs-lookup"><span data-stu-id="d9b96-366">Color swatches cannot be customized.</span></span><br/> |
| <span data-ttu-id="d9b96-367">**文字色彩**</span><span class="sxs-lookup"><span data-stu-id="d9b96-367">**Text color**</span></span>           | <span data-ttu-id="d9b96-368">[UI \_PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md)、 [UI \_ PKEY \_ FontProperties \_ ForegroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolortype.md)</span><span class="sxs-lookup"><span data-stu-id="d9b96-368">[UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), [UI\_PKEY\_FontProperties\_ForegroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolortype.md)</span></span>           | <span data-ttu-id="d9b96-369">提供與 `StandardColors` [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) 元素之範本相同的功能。</span><span class="sxs-lookup"><span data-stu-id="d9b96-369">Provides the same functionality as the `StandardColors` template of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) element.</span></span><br/> <span data-ttu-id="d9b96-370">強烈建議您只設定應用程式所需的初始 **文字色彩** 值。</span><span class="sxs-lookup"><span data-stu-id="d9b96-370">We highly recommend that only an initial **Text color** value be set by the application.</span></span> <span data-ttu-id="d9b96-371">當游標在檔內重新置放時，應該保留最後一個選取的值，而且不會設定。</span><span class="sxs-lookup"><span data-stu-id="d9b96-371">The last selected value should be preserved and not set when the cursor is repositioned within a document.</span></span> <span data-ttu-id="d9b96-372">這可讓使用者快速存取最後選取的專案，而不需要重新開啟色彩選擇器。</span><span class="sxs-lookup"><span data-stu-id="d9b96-372">This allows quick access to the user's last selection, and the color picker does not have to be reopened.</span></span><br/> <span data-ttu-id="d9b96-373">無法自訂色彩色板。</span><span class="sxs-lookup"><span data-stu-id="d9b96-373">Color swatches cannot be customized.</span></span><br/>            |



 

## <a name="define-a-fontcontrol-command-handler"></a><span data-ttu-id="d9b96-374">定義 FontControl 命令處理常式</span><span class="sxs-lookup"><span data-stu-id="d9b96-374">Define a FontControl Command Handler</span></span>

<span data-ttu-id="d9b96-375">本節說明將字型控制項系結至命令處理常式所需的步驟。</span><span class="sxs-lookup"><span data-stu-id="d9b96-375">This section describes the steps required to bind a Font Control to a Command handler.</span></span>

> [!WARNING]
> <span data-ttu-id="d9b96-376">如果沒有與控制項相關聯的命令處理常式，嘗試從字型控制項的色彩選擇器選取色彩樣本，可能會造成存取違規。</span><span class="sxs-lookup"><span data-stu-id="d9b96-376">Any attempt to select a color swatch from the color picker of a Font Control may result in an access violation if no Command handler is associated with the control.</span></span>

 

<span data-ttu-id="d9b96-377">下列程式碼範例示範如何將標記中宣告的命令系結至命令處理常式。</span><span class="sxs-lookup"><span data-stu-id="d9b96-377">The following code example demonstrates how to bind Commands that are declared in markup to a Command handler.</span></span>


```C++
//
//  FUNCTION: OnCreateUICommand(UINT, UI_COMMANDTYPE, IUICommandHandler)
//
//  PURPOSE: Called by the Ribbon framework for each command specified in markup, to allow
//           the host application to bind a command handler to that command.
//
STDMETHODIMP CApplication::OnCreateUICommand(
  UINT nCmdID,
  __in UI_COMMANDTYPE typeID,
  __deref_out IUICommandHandler** ppCommandHandler)
{
  UNREFERENCED_PARAMETER(typeID);
  UNREFERENCED_PARAMETER(nCmdID);

  if (NULL == m_pCommandHandler)
  {
    HRESULT hr = CCommandHandler::CreateInstance(&m_pCommandHandler);
    if (FAILED(hr))
    {
      return hr;
    }
  }

  return m_pCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
}
```



<span data-ttu-id="d9b96-378">下列程式碼範例說明如何針對字型控制項來執行 [**IUICommandHandler：： Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) 方法。</span><span class="sxs-lookup"><span data-stu-id="d9b96-378">The following code example illustrates how to implement the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) method for a Font Control.</span></span>


```C++
//
//  FUNCTION: Execute()
//
//  PURPOSE: Called by the Ribbon framework when a command is executed 
//           by the user. For example, when a button is pressed.
//
STDMETHODIMP CCommandHandler::Execute(
  UINT nCmdID,
  UI_EXECUTIONVERB verb,
  __in_opt const PROPERTYKEY* key,
  __in_opt const PROPVARIANT* ppropvarValue,
  __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if ((key) && (*key == UI_PKEY_FontProperties))
  {
    // Font properties have changed.
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Using the changed properties, set the new font on the selection on RichEdit control.
              g_pFCSampleAppManager->SetValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_PREVIEW:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties for the preview event.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Set the previewed values on the RichEdit control.
              g_pFCSampleAppManager->SetPreviewValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_CANCELPREVIEW:
      {
        hr = E_POINTER;
        if (ppropvarValue != NULL)
        {
          // Cancel the preview.
          IPropertyStore *pValues;
          hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarValue, &pValues);
          if (SUCCEEDED(hr))
          {   
            g_pFCSampleAppManager->CancelPreview(pValues);
            pValues->Release();
          }
        }
        break;
      }
    }
  }

  return hr;
}
```



<span data-ttu-id="d9b96-379">下列程式碼範例說明如何針對字型控制項來執行 [**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) 方法。</span><span class="sxs-lookup"><span data-stu-id="d9b96-379">The following code example illustrates how to implement the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) method for a Font Control.</span></span>


```C++
//
//  FUNCTION: UpdateProperty()
//
//  PURPOSE: Called by the Ribbon framework when a command property (PKEY) needs to be updated.
//
//  COMMENTS:
//
//    This function is used to provide new command property values, such as labels, icons, or
//    tooltip information, when requested by the Ribbon framework.  
//    
//
STDMETHODIMP CCommandHandler::UpdateProperty(
  UINT nCmdID,
  __in REFPROPERTYKEY key,
  __in_opt const PROPVARIANT* ppropvarCurrentValue,
  __out PROPVARIANT* ppropvarNewValue)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if (key == UI_PKEY_FontProperties)
  {
    hr = E_POINTER;
    if (ppropvarCurrentValue != NULL)
    {
      // Get the font values for the selected text in the font control.
      IPropertyStore *pValues;
      hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarCurrentValue, &pValues);
      if (SUCCEEDED(hr))
      {
        g_pFCSampleAppManager->GetValues(pValues);

        // Provide the new values to the font control.
        hr = UIInitPropertyFromInterface(UI_PKEY_FontProperties, pValues, ppropvarNewValue);
        pValues->Release();
      }
    }
  }

  return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="d9b96-380">相關主題</span><span class="sxs-lookup"><span data-stu-id="d9b96-380">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9b96-381">Windows 功能區架構控制項程式庫</span><span class="sxs-lookup"><span data-stu-id="d9b96-381">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="d9b96-382">**FontControl 元素**</span><span class="sxs-lookup"><span data-stu-id="d9b96-382">**FontControl element**</span></span>](windowsribbon-element-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="d9b96-383">字型控制項屬性</span><span class="sxs-lookup"><span data-stu-id="d9b96-383">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="d9b96-384">FontControl 範例</span><span class="sxs-lookup"><span data-stu-id="d9b96-384">FontControl Sample</span></span>](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

