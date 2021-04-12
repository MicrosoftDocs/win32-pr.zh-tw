---
title: 視覺化樣式總覽
description: 本主題說明視覺化樣式，並識別支援這些樣式的 Windows 元件。 此外，也會說明在應用程式中使用視覺化樣式所必須採取的步驟。
ms.assetid: 5B5D7BB6-684F-478D-BF5F-B8D18BBCFF2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5663730c752fbf16c4f229a031eafa0c65bb9dbb
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104463941"
---
# <a name="visual-styles-overview"></a><span data-ttu-id="53e27-104">視覺化樣式總覽</span><span class="sxs-lookup"><span data-stu-id="53e27-104">Visual Styles Overview</span></span>

<span data-ttu-id="53e27-105">本主題說明視覺化樣式，並識別支援這些樣式的 Windows 元件。</span><span class="sxs-lookup"><span data-stu-id="53e27-105">This topic describes visual styles and identifies the Windows components that support them.</span></span> <span data-ttu-id="53e27-106">此外，也會說明在應用程式中使用視覺化樣式所必須採取的步驟。</span><span class="sxs-lookup"><span data-stu-id="53e27-106">It also explains the steps you must take to use visual styles in your applications.</span></span> <span data-ttu-id="53e27-107">本主題包含下列章節：</span><span class="sxs-lookup"><span data-stu-id="53e27-107">This topic includes the following sections:</span></span>

-   [<span data-ttu-id="53e27-108">Themes and Visual Styles</span><span class="sxs-lookup"><span data-stu-id="53e27-108">Themes and Visual Styles</span></span>](#themes-and-visual-styles)
-   [<span data-ttu-id="53e27-109">視覺化樣式元件</span><span class="sxs-lookup"><span data-stu-id="53e27-109">Visual Styles Components</span></span>](#visual-styles-components)
-   [<span data-ttu-id="53e27-110">支援視覺效果樣式的應用程式需求</span><span class="sxs-lookup"><span data-stu-id="53e27-110">Application Requirements for Supporting Visual Styles</span></span>](#application-requirements-for-supporting-visual-styles)
-   [<span data-ttu-id="53e27-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="53e27-111">Related topics</span></span>](#related-topics)

## <a name="themes-and-visual-styles"></a><span data-ttu-id="53e27-112">Themes and Visual Styles</span><span class="sxs-lookup"><span data-stu-id="53e27-112">Themes and Visual Styles</span></span>

<span data-ttu-id="53e27-113">Windows 包含數個功能，可讓使用者量身打造 UI 來滿足其個別的需求和喜好設定。</span><span class="sxs-lookup"><span data-stu-id="53e27-113">Windows includes several features that enable users to tailor the UI to accommodate their individual needs and preferences.</span></span> <span data-ttu-id="53e27-114">這些功能包括在 Microsoft Plus 中引進的主題</span><span class="sxs-lookup"><span data-stu-id="53e27-114">These features include themes, which were introduced in Microsoft Plus!</span></span> <span data-ttu-id="53e27-115">適用于 Windows 95。</span><span class="sxs-lookup"><span data-stu-id="53e27-115">for Windows 95.</span></span> <span data-ttu-id="53e27-116">主題是使用者可選取的設定集合，其中包含背景圖樣、游標、字型、音效和圖示。</span><span class="sxs-lookup"><span data-stu-id="53e27-116">A theme is a user-selectable collection of settings that includes wallpaper, cursors, fonts, sounds, and icons.</span></span> <span data-ttu-id="53e27-117">以下是主題的一些特性。</span><span class="sxs-lookup"><span data-stu-id="53e27-117">The following are some characteristics of themes.</span></span>

-   <span data-ttu-id="53e27-118">主題設定是在具有類似 win.ini 檔案格式的主題檔案中指定。</span><span class="sxs-lookup"><span data-stu-id="53e27-118">Theme settings are specified in .theme files that have a format similar to win.ini files.</span></span>
-   <span data-ttu-id="53e27-119">獨立軟體廠商 (ISV) 可以使用產品來建立並散發主題檔案。</span><span class="sxs-lookup"><span data-stu-id="53e27-119">An independent software vendor (ISV) can create and distribute a .theme file with a product.</span></span>
-   <span data-ttu-id="53e27-120">在 Windows Vista 之前的版本中，主題檔案會顯示在 [顯示] 控制台的 [主題] 索引標籤上。</span><span class="sxs-lookup"><span data-stu-id="53e27-120">In versions earlier than Windows Vista, theme files are displayed on the Theme tab of the Display control panel.</span></span> <span data-ttu-id="53e27-121">在 Windows Vista 和更新版本中，主題會顯示在 [個人化] 控制台中。</span><span class="sxs-lookup"><span data-stu-id="53e27-121">In Windows Vista and later, themes are displayed in the Personalization control panel.</span></span>

<span data-ttu-id="53e27-122">如需主題檔案的詳細資訊，請參閱 [主題檔案格式](themesfileformat-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="53e27-122">For more information about .theme files, see [Theme File Format](themesfileformat-overview.md).</span></span>

<span data-ttu-id="53e27-123">視覺化樣式是定義 Windows 通用控制面板的規格。</span><span class="sxs-lookup"><span data-stu-id="53e27-123">A visual style is a specification that defines the appearance of the Windows common controls.</span></span> <span data-ttu-id="53e27-124">視覺化樣式與主題相關聯;亦即，主題檔案包含一個區段，可指定當特定主題為使用中時要套用的視覺化樣式。</span><span class="sxs-lookup"><span data-stu-id="53e27-124">Visual styles are associated with themes; that is, a .theme file contains a section that specifies the visual style to apply when the particular theme is active.</span></span> <span data-ttu-id="53e27-125">以下是視覺化樣式的部分特性。</span><span class="sxs-lookup"><span data-stu-id="53e27-125">The following are some characteristics of visual styles.</span></span>

-   <span data-ttu-id="53e27-126">使用者可以選取不同的主題，隨時變更視覺效果樣式。</span><span class="sxs-lookup"><span data-stu-id="53e27-126">Users can change the visual style at any time by selecting a different theme.</span></span>
-   <span data-ttu-id="53e27-127">您必須使用視覺化樣式 API，將目前使用中的視覺效果樣式套用至應用程式的自訂或主控描繪控制項（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="53e27-127">You must use the visual styles API to apply the currently active visual style to your application's custom or owner-drawn controls, if any.</span></span>
-   <span data-ttu-id="53e27-128">定義視覺效果樣式的資訊會儲存在 msstyles 檔案中。</span><span class="sxs-lookup"><span data-stu-id="53e27-128">The information that defines a visual style is stored in a .msstyles file.</span></span> <span data-ttu-id="53e27-129">Microsoft 不支援 msstyles 檔案的撰寫。</span><span class="sxs-lookup"><span data-stu-id="53e27-129">Microsoft does not support the authoring of .msstyles files.</span></span>


<span data-ttu-id="53e27-130">下圖顯示一個簡單的對話方塊，其中包含工作列，在使用 Windows Aero 主題但沒有透明度的 Windows 7 桌面上。</span><span class="sxs-lookup"><span data-stu-id="53e27-130">The following illustration shows a simple dialog box with a taskbar, on a Windows 7 desktop that uses the Windows Aero theme without transparency.</span></span> <span data-ttu-id="53e27-131">因為應用程式未設定為使用視覺化樣式，所以不論主題設定為何，按鈕都會顯示相同。</span><span class="sxs-lookup"><span data-stu-id="53e27-131">Because the application is not configured to use visual styles, the buttons appear the same regardless of the theme settings.</span></span>

![對話方塊的螢幕擷取畫面，其中包含不使用透明度的按鈕](images/tb-wostyles.png)

<span data-ttu-id="53e27-133">相反地，下圖顯示相同桌面上的相同對話方塊，但這次應用程式已設定為使用視覺化樣式。</span><span class="sxs-lookup"><span data-stu-id="53e27-133">In contrast, the following illustration shows the same dialog box on the same desktop, but this time the application has been configured to work with visual styles.</span></span> <span data-ttu-id="53e27-134">請注意工作區中按鈕的不同外觀。</span><span class="sxs-lookup"><span data-stu-id="53e27-134">Note the different appearance of the buttons in the client area.</span></span> <span data-ttu-id="53e27-135">按鈕看起來會不同，因為系統已套用 Aero 主題中定義的視覺效果樣式。</span><span class="sxs-lookup"><span data-stu-id="53e27-135">The buttons look different because the system has applied the visual styles that are defined in the Aero theme.</span></span>

![對話方塊的螢幕擷取畫面，其中包含使用透明度的按鈕](images/tb-withstyles.png)

<span data-ttu-id="53e27-137">下列範例顯示 Windows 8 桌面上的類似對話方塊。</span><span class="sxs-lookup"><span data-stu-id="53e27-137">The following example shows a similar dialog box on a Windows 8 desktop.</span></span> <span data-ttu-id="53e27-138">在 Windows 8 中，視覺效果樣式一律會開啟，因此 Windows 8 應用程式會取得「免費」的主題。</span><span class="sxs-lookup"><span data-stu-id="53e27-138">In Windows 8, visual styles are always on, so Windows 8 apps get theming "for free".</span></span>

![windows 8 桌面上簡單對話方塊的螢幕擷取畫面](images/tb-win8.png)

## <a name="visual-styles-components"></a><span data-ttu-id="53e27-140">視覺化樣式元件</span><span class="sxs-lookup"><span data-stu-id="53e27-140">Visual Styles Components</span></span>

<span data-ttu-id="53e27-141">下列元件支援視覺化樣式：</span><span class="sxs-lookup"><span data-stu-id="53e27-141">Visual styles are supported by the following components:</span></span>

-   <span data-ttu-id="53e27-142">第6版或更新版本的通用控制項程式庫 (ComCtl32.dll) </span><span class="sxs-lookup"><span data-stu-id="53e27-142">Version 6 or later of the common control library (ComCtl32.dll)</span></span>
-   <span data-ttu-id="53e27-143">在 UxTheme.dll 中實作為視覺化樣式 API</span><span class="sxs-lookup"><span data-stu-id="53e27-143">The visual styles API implemented in UxTheme.dll</span></span>
-   <span data-ttu-id="53e27-144">主題服務</span><span class="sxs-lookup"><span data-stu-id="53e27-144">Themes service</span></span>
-   <span data-ttu-id="53e27-145">一或多個視覺化樣式定義檔案 (. msstyles) </span><span class="sxs-lookup"><span data-stu-id="53e27-145">One or more visual style definition files (.msstyles)</span></span>

<span data-ttu-id="53e27-146">視覺化樣式 API 相依于稱為主題的系統服務。</span><span class="sxs-lookup"><span data-stu-id="53e27-146">The visual styles API depends on a system service called Themes.</span></span> <span data-ttu-id="53e27-147">通用控制項程式庫會查詢主題服務來取得樣式相關資訊，而在 Windows 7 中，則會使用服務，以目前的視覺化樣式呈現控制項。</span><span class="sxs-lookup"><span data-stu-id="53e27-147">The common control library queries the Themes service to get style-related information and, up through Windows 7, uses the service to render controls in the current visual style.</span></span>

<span data-ttu-id="53e27-148">在 Windows 8 和更新版本中，如果主題服務已關閉，視覺效果樣式 API 仍可運作。</span><span class="sxs-lookup"><span data-stu-id="53e27-148">In Windows 8 and later, the visual styles API still works if the Themes service is off.</span></span> <span data-ttu-id="53e27-149">這表示當主題服務關閉時，通用控制項和非工作區的視窗仍會有視覺化樣式。</span><span class="sxs-lookup"><span data-stu-id="53e27-149">This means that the common controls and the non-client area of windows will still have visual styles when the Themes service is off.</span></span> <span data-ttu-id="53e27-150">仍需要主題服務的 Windows 8 功能包括：</span><span class="sxs-lookup"><span data-stu-id="53e27-150">The Windows 8 features that still require the Themes service include:</span></span>

-   <span data-ttu-id="53e27-151">變更視覺效果樣式， **通常是透過 [** **電腦設定**] 的 [個人化] 頁面。</span><span class="sxs-lookup"><span data-stu-id="53e27-151">Changing the visual style, typically through the **Personalization** page of **PC Settings**.</span></span>
-   <span data-ttu-id="53e27-152">在使用者會話之間切換使用者、登出、關機和共用所涉及的效能優化。</span><span class="sxs-lookup"><span data-stu-id="53e27-152">Performance optimizations involved in switching users, logging off, shutting down, and sharing across user sessions.</span></span>

<span data-ttu-id="53e27-153">視覺化樣式 API 會從與目前選取之主題相關聯的 msstyles 檔案取得樣式資訊。</span><span class="sxs-lookup"><span data-stu-id="53e27-153">The visual styles API gets style information from the .msstyles file associated with the currently selected theme.</span></span> <span data-ttu-id="53e27-154">Msstyles 檔案包含一組定義視覺效果樣式的度量、字型、色彩和點陣圖。</span><span class="sxs-lookup"><span data-stu-id="53e27-154">The .msstyles file contains a set of metrics, fonts, colors, and bitmaps that define a visual style</span></span>

## <a name="application-requirements-for-supporting-visual-styles"></a><span data-ttu-id="53e27-155">支援視覺效果樣式的應用程式需求</span><span class="sxs-lookup"><span data-stu-id="53e27-155">Application Requirements for Supporting Visual Styles</span></span>

<span data-ttu-id="53e27-156">若要使用視覺化樣式，您的應用程式必須在包含 ComCtl32.dll 6 版或更新版本的作業系統上執行。</span><span class="sxs-lookup"><span data-stu-id="53e27-156">To use visual styles, your application must be running on an operating system that contains ComCtl32.dll version 6 or later.</span></span> <span data-ttu-id="53e27-157">如果您想要讓應用程式使用 ComCtl32.dll 第6版，則必須新增應用程式資訊清單或編譯器指示詞，以指定應該使用第6版（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="53e27-157">If you want your application to use ComCtl32.dll version 6, you must add an application manifest or compiler directive to specify that version 6 should be used if it is available.</span></span> <span data-ttu-id="53e27-158">如需如何建立應用程式資訊清單以便讓應用程式使用視覺化樣式的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="53e27-158">For information on how to create an application manifest that enables your application to use visual styles, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

<span data-ttu-id="53e27-159">針對通用控制項，不需要採取進一步的動作，以確保控制項顯示在使用者的慣用視覺效果樣式中。</span><span class="sxs-lookup"><span data-stu-id="53e27-159">For common controls, no further action is necessary to ensure that the controls are displayed in the user's preferred visual style.</span></span>

<span data-ttu-id="53e27-160">如果您的應用程式包含自訂或主控描繪的控制項，您必須使用視覺化樣式 API 來取得目前使用中視覺效果樣式的相關資訊，並使用該樣式來繪製控制項。</span><span class="sxs-lookup"><span data-stu-id="53e27-160">If your application contains custom or owner-drawn controls, you need to use the visual styles API to retrieve information about the currently active visual style, and to draw the controls in that style.</span></span>

<span data-ttu-id="53e27-161">在 Windows 8 之前的 Windows 版本中，應用程式通常需要提供兩個不同的程式碼路徑，以繪製自訂和主控描繪的控制項。</span><span class="sxs-lookup"><span data-stu-id="53e27-161">For Windows versions prior to Windows 8, applications typically need to provide two separate code paths for drawing custom and owner-drawn controls.</span></span> <span data-ttu-id="53e27-162">當使用視覺化樣式的主題為作用中時，其中一個程式碼路徑會繪製控制項，而當 Windows 傳統主題或高對比主題為作用中時，另一個程式碼路徑會繪製控制項。</span><span class="sxs-lookup"><span data-stu-id="53e27-162">One code path draws the controls when a theme that uses visual styles is active, and another code path draws the controls when the Windows Classic theme or a high contrast theme is active.</span></span> <span data-ttu-id="53e27-163">不過，在 Windows 8 中，視覺效果樣式一律是開啟的，因此不需要個別的主題程式碼路徑。</span><span class="sxs-lookup"><span data-stu-id="53e27-163">In Windows 8, however, visual styles are always on, so separate theming code paths are not needed.</span></span> <span data-ttu-id="53e27-164">針對 Windows 8 的應用程式取得高對比主題「免費」。</span><span class="sxs-lookup"><span data-stu-id="53e27-164">Applications that are manifested for Windows 8 get high contrast theming "for free."</span></span> <span data-ttu-id="53e27-165">如需詳細資訊，請參閱 [支援高對比主題](supporting-high-contrast-themes.md)。</span><span class="sxs-lookup"><span data-stu-id="53e27-165">For more information, see [Supporting High Contrast Themes](supporting-high-contrast-themes.md).</span></span>

<span data-ttu-id="53e27-166">如需的詳細資訊，請參閱 [使用視覺化樣式搭配自訂和 Owner-Drawn 控制項](using-visual-styles.md) 和 [視覺化樣式參考](uxctl-ref.md)。</span><span class="sxs-lookup"><span data-stu-id="53e27-166">For more information about, see [Using Visual Styles with Custom and Owner-Drawn Controls](using-visual-styles.md) and [Visual Styles Reference](uxctl-ref.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="53e27-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="53e27-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53e27-168">視覺化樣式</span><span class="sxs-lookup"><span data-stu-id="53e27-168">Visual Styles</span></span>](themes-overview.md)
</dt> </dl>

 

 




