---
title: 協助工具最佳作法
description: 執行本節所述的最佳作法有助於確保使用輔助技術產品的人員可以存取您的應用程式。
ms.assetid: ef694361-49b7-424c-a583-1eadc2519db7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38d9f70828610d04255b61ad3ee533d23c514867
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839811"
---
# <a name="accessibility-best-practices"></a><span data-ttu-id="eeb69-103">協助工具最佳作法</span><span class="sxs-lookup"><span data-stu-id="eeb69-103">Accessibility Best Practices</span></span>

<span data-ttu-id="eeb69-104">執行本節所述的最佳作法有助於確保使用輔助技術產品的人員可以存取您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="eeb69-104">Implementing the best practices described in this section helps ensure that your application is accessible to people who use assistive technology products.</span></span> <span data-ttu-id="eeb69-105">其中許多最佳做法著重于良好的 UI 設計。</span><span class="sxs-lookup"><span data-stu-id="eeb69-105">Many of these best practices focus on good UI design.</span></span> <span data-ttu-id="eeb69-106">每個最佳作法都包含控制項或應用程式的執行資訊。</span><span class="sxs-lookup"><span data-stu-id="eeb69-106">Each best practice includes implementation information for controls or applications.</span></span> <span data-ttu-id="eeb69-107">在許多情況下，這些最佳作法的大部分工作都已包含在控制項中。</span><span class="sxs-lookup"><span data-stu-id="eeb69-107">In many cases, much of the work to meet these best practices is already included in the controls.</span></span>

<span data-ttu-id="eeb69-108">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="eeb69-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="eeb69-109">以程式設計方式存取</span><span class="sxs-lookup"><span data-stu-id="eeb69-109">Programmatic Access</span></span>](#programmatic-access)
    -   [<span data-ttu-id="eeb69-110">啟用以程式設計方式存取所有 UI 項目和文字</span><span class="sxs-lookup"><span data-stu-id="eeb69-110">Enable Programmatic Access to all UI Elements and Text</span></span>](#enable-programmatic-access-to-all-ui-elements-and-text)
    -   [<span data-ttu-id="eeb69-111">在 UI 物件、框架和頁面上放置名稱、標題和描述</span><span class="sxs-lookup"><span data-stu-id="eeb69-111">Place Names, Titles, and Descriptions on UI Objects, Frames, and Pages</span></span>](#place-names-titles-and-descriptions-on-ui-objects-frames-and-pages)
    -   [<span data-ttu-id="eeb69-112">確定所有 UI 活動都會觸發程式設計事件</span><span class="sxs-lookup"><span data-stu-id="eeb69-112">Ensure Programmatic Events Are Triggered by All UI Activities</span></span>](#ensure-programmatic-events-are-triggered-by-all-ui-activities)
-   [<span data-ttu-id="eeb69-113">使用者設定</span><span class="sxs-lookup"><span data-stu-id="eeb69-113">User Settings</span></span>](#user-settings)
    -   [<span data-ttu-id="eeb69-114">遵循所有系統範圍設定並不會干擾協助工具功能</span><span class="sxs-lookup"><span data-stu-id="eeb69-114">Respect All System-Wide Settings and Do Not Interfere with Accessibility Functions</span></span>](#respect-all-system-wide-settings-and-do-not-interfere-with-accessibility-functions)
-   [<span data-ttu-id="eeb69-115">視覺 UI 設計</span><span class="sxs-lookup"><span data-stu-id="eeb69-115">Visual UI Design</span></span>](#visual-ui-design)
    -   [<span data-ttu-id="eeb69-116">不 Hard-Code 色彩</span><span class="sxs-lookup"><span data-stu-id="eeb69-116">Do Not Hard-Code Colors</span></span>](#do-not-hard-code-colors)
    -   [<span data-ttu-id="eeb69-117">支援高對比和所有系統的顯示屬性</span><span class="sxs-lookup"><span data-stu-id="eeb69-117">Support High Contrast and all System Display Attributes</span></span>](#support-high-contrast-and-all-system-display-attributes)
    -   [<span data-ttu-id="eeb69-118">確定所有 UI 正確地依 DPI 設定值縮放比例</span><span class="sxs-lookup"><span data-stu-id="eeb69-118">Ensure All UI Correctly Scales by Any DPI Setting</span></span>](#ensure-all-ui-correctly-scales-by-any-dpi-setting)
-   [<span data-ttu-id="eeb69-119">鍵盤流覽</span><span class="sxs-lookup"><span data-stu-id="eeb69-119">Keyboard Navigation</span></span>](#keyboard-navigation)
    -   [<span data-ttu-id="eeb69-120">提供所有 UI 項目的鍵盤介面</span><span class="sxs-lookup"><span data-stu-id="eeb69-120">Provide Keyboard Interface for All UI Elements</span></span>](#provide-keyboard-interface-for-all-ui-elements)
    -   [<span data-ttu-id="eeb69-121">顯示鍵盤焦點</span><span class="sxs-lookup"><span data-stu-id="eeb69-121">Show the Keyboard Focus</span></span>](#show-the-keyboard-focus)
    -   [<span data-ttu-id="eeb69-122">支援巡覽標準和強大的巡覽配置</span><span class="sxs-lookup"><span data-stu-id="eeb69-122">Support Navigation Standards and Powerful Navigation Schemes</span></span>](#support-navigation-standards-and-powerful-navigation-schemes)
    -   [<span data-ttu-id="eeb69-123">不要讓滑鼠位置干擾鍵盤巡覽</span><span class="sxs-lookup"><span data-stu-id="eeb69-123">Do Not Let Mouse Location Interfere with Keyboard Navigation</span></span>](#do-not-let-mouse-location-interfere-with-keyboard-navigation)
-   [<span data-ttu-id="eeb69-124">多重模式介面</span><span class="sxs-lookup"><span data-stu-id="eeb69-124">Multi-modal Interface</span></span>](#multi-modal-interface)
    -   [<span data-ttu-id="eeb69-125">對於非文字項目提供使用者可選取的對等項目</span><span class="sxs-lookup"><span data-stu-id="eeb69-125">Provide User-Selectable Equivalents for Non-Text Elements</span></span>](#provide-user-selectable-equivalents-for-non-text-elements)
    -   [<span data-ttu-id="eeb69-126">使用色彩，但是也提供色彩的替代方案</span><span class="sxs-lookup"><span data-stu-id="eeb69-126">Use Color but Also Provide Alternatives to Color</span></span>](#use-color-but-also-provide-alternatives-to-color)
    -   [<span data-ttu-id="eeb69-127">藉由與裝置無關的呼叫使用標準輸入的 API</span><span class="sxs-lookup"><span data-stu-id="eeb69-127">Use Standard Input APIs with Device-Independent Calls</span></span>](#use-standard-input-apis-with-device-independent-calls)
-   [<span data-ttu-id="eeb69-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="eeb69-128">Related topics</span></span>](#related-topics)

## <a name="programmatic-access"></a><span data-ttu-id="eeb69-129">程式設計存取</span><span class="sxs-lookup"><span data-stu-id="eeb69-129">Programmatic Access</span></span>

<span data-ttu-id="eeb69-130">本節中的最佳作法 enure 輔助技術產品具有適當的程式設計方式來存取 UI 資訊和功能。</span><span class="sxs-lookup"><span data-stu-id="eeb69-130">The best practices in this section enure that assistive technology products have adequate programmatic access to UI information and functionality.</span></span>

### <a name="enable-programmatic-access-to-all-ui-elements-and-text"></a><span data-ttu-id="eeb69-131">啟用以程式設計方式存取所有 UI 項目和文字</span><span class="sxs-lookup"><span data-stu-id="eeb69-131">Enable Programmatic Access to all UI Elements and Text</span></span>

<span data-ttu-id="eeb69-132">您應用程式的 UI 元素必須以程式設計方式存取輔助技術產品。</span><span class="sxs-lookup"><span data-stu-id="eeb69-132">The UI elements of your application must be programmatically accessible to assistive technology products.</span></span> <span data-ttu-id="eeb69-133">所有 UI 元素都必須有標籤，它們必須公開所有屬性值，而且必須引發所有適當的事件。</span><span class="sxs-lookup"><span data-stu-id="eeb69-133">All UI elements must have labels, they must expose all property values, and they must raise all appropriate events.</span></span> <span data-ttu-id="eeb69-134">針對標準的 Windows 控制項，大部分的工作都是透過 Microsoft 消費者介面自動化和 Microsoft Active Accessibility proxy 物件來完成。</span><span class="sxs-lookup"><span data-stu-id="eeb69-134">For the standard Windows controls, most of this work is already done through the Microsoft UI Automation and Microsoft Active Accessibility proxy objects.</span></span> <span data-ttu-id="eeb69-135">但是，自訂控制項需要額外的工作，以確保它們完全公開，讓輔助技術廠商可以識別和操作您應用程式 UI 的元素。</span><span class="sxs-lookup"><span data-stu-id="eeb69-135">Custom controls, however, require additional work to ensure that they are fully exposed so that assistive technology vendors can identify and manipulate elements of your application UI.</span></span>

<span data-ttu-id="eeb69-136">遵循此最佳做法可讓輔助技術廠商識別和操作您產品 UI 的元素。</span><span class="sxs-lookup"><span data-stu-id="eeb69-136">Following this best practice allows assistive technology vendors to identify and manipulate elements of your product's UI.</span></span>

### <a name="place-names-titles-and-descriptions-on-ui-objects-frames-and-pages"></a><span data-ttu-id="eeb69-137">在 UI 物件、框架和頁面上放置名稱、標題和描述</span><span class="sxs-lookup"><span data-stu-id="eeb69-137">Place Names, Titles, and Descriptions on UI Objects, Frames, and Pages</span></span>

<span data-ttu-id="eeb69-138">由於輔助技術產品（尤其是螢幕讀取器）使用標題來瞭解框架、物件或頁面在導覽配置中的位置，標題必須有很高的描述性。</span><span class="sxs-lookup"><span data-stu-id="eeb69-138">Because assistive technology products—especially screen readers—use titles to understand the location of a frame, object, or page in the navigation scheme, the titles must be very descriptive.</span></span> <span data-ttu-id="eeb69-139">好用的描述性標題可讓輔助技術產品識別和操作控制項和應用程式中的 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="eeb69-139">Good descriptive titles enable assistive technology products to identify and manipulate UI elements in controls and applications.</span></span> <span data-ttu-id="eeb69-140">例如，如果使用者已深入流覽到特定區域，則「Microsoft 網頁」的網頁標題就毫無用處。</span><span class="sxs-lookup"><span data-stu-id="eeb69-140">For example, a webpage title of "Microsoft Web Page" is useless if the user has navigated deeply into a particular area.</span></span> <span data-ttu-id="eeb69-141">描述性的標題對於失明和依賴螢幕讀取器的使用者來說很重要。</span><span class="sxs-lookup"><span data-stu-id="eeb69-141">A descriptive title is crucial for users who are blind and depend on screen readers.</span></span>

<span data-ttu-id="eeb69-142">遵循此最佳做法可讓輔助技術產品識別和操作範例控制項和應用程式中的 UI。</span><span class="sxs-lookup"><span data-stu-id="eeb69-142">Following this best practice allows assistive technology products to identify and manipulate UI in sample controls and applications.</span></span>

### <a name="ensure-programmatic-events-are-triggered-by-all-ui-activities"></a><span data-ttu-id="eeb69-143">確定所有 UI 活動都會觸發程式設計事件</span><span class="sxs-lookup"><span data-stu-id="eeb69-143">Ensure Programmatic Events Are Triggered by All UI Activities</span></span>

<span data-ttu-id="eeb69-144">每當 UI 元素的狀態或外觀發生變更時，您的應用程式應該會引發事件。</span><span class="sxs-lookup"><span data-stu-id="eeb69-144">Your application should raise events whenever changes occur in the state or appearance of a UI element.</span></span>

<span data-ttu-id="eeb69-145">遵循此最佳做法可讓輔助技術產品接聽 UI 中的變更，並通知使用者這些變更。</span><span class="sxs-lookup"><span data-stu-id="eeb69-145">Following this best practice allows assistive technology products to listen for changes in the UI and notify the user about these changes.</span></span>

## <a name="user-settings"></a><span data-ttu-id="eeb69-146">使用者設定</span><span class="sxs-lookup"><span data-stu-id="eeb69-146">User Settings</span></span>

<span data-ttu-id="eeb69-147">本節中的最佳做法可確保該控制項或應用程式不會覆寫使用者設定。</span><span class="sxs-lookup"><span data-stu-id="eeb69-147">The best practice in this section ensures that controls or applications do not override user settings.</span></span>

### <a name="respect-all-system-wide-settings-and-do-not-interfere-with-accessibility-functions"></a><span data-ttu-id="eeb69-148">遵循所有系統範圍設定並不會干擾協助工具功能</span><span class="sxs-lookup"><span data-stu-id="eeb69-148">Respect All System-Wide Settings and Do Not Interfere with Accessibility Functions</span></span>

<span data-ttu-id="eeb69-149">使用者可以使用主控台設定一些全系統旗標;您可以透過程式設計方式來設定其他旗標。</span><span class="sxs-lookup"><span data-stu-id="eeb69-149">Users can use Control Panel to set some system-wide flags; other flags can be set programmatically.</span></span> <span data-ttu-id="eeb69-150">不應該由控制項或應用程式變更這些設定。</span><span class="sxs-lookup"><span data-stu-id="eeb69-150">These settings should not be changed by controls or applications.</span></span> <span data-ttu-id="eeb69-151">此外，應用程式必須支援主機作業系統的協助工具設定。</span><span class="sxs-lookup"><span data-stu-id="eeb69-151">Also, applications must support the accessibility settings of their host operating system.</span></span>

<span data-ttu-id="eeb69-152">遵循這個最佳做法可讓使用者設定協助工具設定，並了解這些設定不會由應用程式所變更。</span><span class="sxs-lookup"><span data-stu-id="eeb69-152">Following this best practice allows users to set accessibility settings and know that those settings will not be changed by applications.</span></span>

## <a name="visual-ui-design"></a><span data-ttu-id="eeb69-153">視覺 UI 設計</span><span class="sxs-lookup"><span data-stu-id="eeb69-153">Visual UI Design</span></span>

<span data-ttu-id="eeb69-154">本節中的最佳做法可確保控制項或應用程式有效地使用色彩和影像，並可供輔助技術產品使用。</span><span class="sxs-lookup"><span data-stu-id="eeb69-154">The best practices in this section ensure that controls or applications use color and images effectively and can be used by assistive technology products.</span></span>

### <a name="do-not-hard-code-colors"></a><span data-ttu-id="eeb69-155">不 Hard-Code 色彩</span><span class="sxs-lookup"><span data-stu-id="eeb69-155">Do Not Hard-Code Colors</span></span>

<span data-ttu-id="eeb69-156">色盲、視力不佳或使用黑白螢幕的人可能無法使用色彩為硬式編碼的應用程式。</span><span class="sxs-lookup"><span data-stu-id="eeb69-156">People who are color blind, have low vision, or are using a black and white screen might not be able to use applications with hard-coded colors.</span></span>

<span data-ttu-id="eeb69-157">遵循這個最佳做法可讓使用者根據個人需求調整色彩組合。</span><span class="sxs-lookup"><span data-stu-id="eeb69-157">Following this best practice allows users to adjust color combinations based on individual needs.</span></span>

### <a name="support-high-contrast-and-all-system-display-attributes"></a><span data-ttu-id="eeb69-158">支援高對比和所有系統的顯示屬性</span><span class="sxs-lookup"><span data-stu-id="eeb69-158">Support High Contrast and all System Display Attributes</span></span>

<span data-ttu-id="eeb69-159">應用程式不應中斷或停用使用者選取的系統範圍對比設定、色彩選擇或其他系統範圍的顯示設定和屬性。</span><span class="sxs-lookup"><span data-stu-id="eeb69-159">Applications should not disrupt or disable user-selected, system-wide contrast settings, color selections, or other system-wide display settings and attributes.</span></span> <span data-ttu-id="eeb69-160">使用者採用的系統範圍設定可增強應用程式的可及性，所以應用程式不應停用或忽略它們。</span><span class="sxs-lookup"><span data-stu-id="eeb69-160">System-wide settings adopted by a user enhance the accessibility of applications, so they should not be disabled or disregarded by applications.</span></span> <span data-ttu-id="eeb69-161">應該在正確的前景背景組合中使用色彩，以提供適當的對比。</span><span class="sxs-lookup"><span data-stu-id="eeb69-161">Color should be used in their correct foreground-on-background combination to provide proper contrast.</span></span> <span data-ttu-id="eeb69-162">不應混用不相關的色彩，而且不應反轉色彩。</span><span class="sxs-lookup"><span data-stu-id="eeb69-162">Unrelated colors should not be mixed, and colors should not be reversed.</span></span>

<span data-ttu-id="eeb69-163">許多使用者需要特定的高對比組合，例如在黑色背景上的白色文字。</span><span class="sxs-lookup"><span data-stu-id="eeb69-163">Many users require specific high-contrast combinations, such as white text on a black background.</span></span> <span data-ttu-id="eeb69-164">如在白色背景上的黑色文字一樣反轉繪製，會造成背景滲出到前景，可能會使某些使用者閱讀困難。</span><span class="sxs-lookup"><span data-stu-id="eeb69-164">Drawing these reversed, as black text on a white background causes the background to bleed over the foreground and can make reading difficult for some users.</span></span>

### <a name="ensure-all-ui-correctly-scales-by-any-dpi-setting"></a><span data-ttu-id="eeb69-165">確定所有 UI 正確地依 DPI 設定值縮放比例</span><span class="sxs-lookup"><span data-stu-id="eeb69-165">Ensure All UI Correctly Scales by Any DPI Setting</span></span>

<span data-ttu-id="eeb69-166">請確定所有的 UI 元素都可以依每英寸的任何點 (DPI) 設定來適當地調整。</span><span class="sxs-lookup"><span data-stu-id="eeb69-166">Ensure that all UI elements can correctly scale by any dots per inch (dpi) setting.</span></span> <span data-ttu-id="eeb69-167">此外，請確定 UI 元素能容納在 1024 x 768 的螢幕中，每英寸都有120點 (DPI) 。</span><span class="sxs-lookup"><span data-stu-id="eeb69-167">Also, ensure that UI elements fit in a screen of 1024 x 768 with 120 dots per inch (dpi).</span></span>

## <a name="keyboard-navigation"></a><span data-ttu-id="eeb69-168">鍵盤導覽</span><span class="sxs-lookup"><span data-stu-id="eeb69-168">Keyboard Navigation</span></span>

<span data-ttu-id="eeb69-169">本節中的最佳做法可確保依賴鍵盤的使用者可以存取所有的應用程式功能。</span><span class="sxs-lookup"><span data-stu-id="eeb69-169">The best practices in this section ensure that all application functionality is accessible to users who rely on the keyboard.</span></span>

### <a name="provide-keyboard-interface-for-all-ui-elements"></a><span data-ttu-id="eeb69-170">提供所有 UI 項目的鍵盤介面</span><span class="sxs-lookup"><span data-stu-id="eeb69-170">Provide Keyboard Interface for All UI Elements</span></span>

<span data-ttu-id="eeb69-171">Tab 鍵停止，特別是在仔細規劃時，讓使用者可以用另一種方式流覽 UI。</span><span class="sxs-lookup"><span data-stu-id="eeb69-171">Tab stops, especially when carefully planned, give users another way to navigate the UI.</span></span>

<span data-ttu-id="eeb69-172">應用程式應該提供下列鍵盤介面：</span><span class="sxs-lookup"><span data-stu-id="eeb69-172">Applications should provide the following keyboard interfaces:</span></span>

-   <span data-ttu-id="eeb69-173">使用者可以與之互動的所有控制項（例如按鈕、連結或清單方塊）的 Tab 鍵停止。</span><span class="sxs-lookup"><span data-stu-id="eeb69-173">Tab stops for all controls that the user can interact with, such as buttons, links, or list boxes.</span></span>
-   <span data-ttu-id="eeb69-174">邏輯索引標籤順序。</span><span class="sxs-lookup"><span data-stu-id="eeb69-174">Logical tab order.</span></span>

### <a name="show-the-keyboard-focus"></a><span data-ttu-id="eeb69-175">顯示鍵盤焦點</span><span class="sxs-lookup"><span data-stu-id="eeb69-175">Show the Keyboard Focus</span></span>

<span data-ttu-id="eeb69-176">使用者需要知道哪個物件具有鍵盤焦點，這樣他們才可以預期按鍵的效果。</span><span class="sxs-lookup"><span data-stu-id="eeb69-176">Users need to know which object has the keyboard focus so that they can anticipate the effect of their keystrokes.</span></span> <span data-ttu-id="eeb69-177">若要醒目提示鍵盤焦點，請使用色彩、字型或圖形，例如矩形或縮放比例。</span><span class="sxs-lookup"><span data-stu-id="eeb69-177">To highlight the keyboard focus, use colors, fonts, or graphics such as rectangles or magnification.</span></span> <span data-ttu-id="eeb69-178">若要以可聽見的方式提示鍵盤焦點，請變更音量、音高或音調品質。</span><span class="sxs-lookup"><span data-stu-id="eeb69-178">To audibly highlight the keyboard focus, change the volume, pitch or tonal quality.</span></span>

<span data-ttu-id="eeb69-179">為了避免混淆，應用程式應隱藏所有視覺焦點指標，以及將位於非使用中視窗 (或窗格) 中的選取項目變暗。</span><span class="sxs-lookup"><span data-stu-id="eeb69-179">To avoid confusion, applications should hide all visual focus indicators and dim selections that are located in inactive windows (or panes).</span></span>

<span data-ttu-id="eeb69-180">應用程式應以鍵盤焦點執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="eeb69-180">Applications should do the following with keyboard focus:</span></span>

-   <span data-ttu-id="eeb69-181">一個專案應該一律具有鍵盤焦點。</span><span class="sxs-lookup"><span data-stu-id="eeb69-181">One item should always have keyboard focus.</span></span>
-   <span data-ttu-id="eeb69-182">鍵盤焦點應該是可見且顯而易見的。</span><span class="sxs-lookup"><span data-stu-id="eeb69-182">Keyboard focus should be visible and obvious.</span></span>
-   <span data-ttu-id="eeb69-183">選取專案及/或焦點專案應以視覺化方式反白顯示。</span><span class="sxs-lookup"><span data-stu-id="eeb69-183">Selections and/or focused items should be visually highlighted.</span></span>

### <a name="support-navigation-standards-and-powerful-navigation-schemes"></a><span data-ttu-id="eeb69-184">支援巡覽標準和強大的巡覽配置</span><span class="sxs-lookup"><span data-stu-id="eeb69-184">Support Navigation Standards and Powerful Navigation Schemes</span></span>

<span data-ttu-id="eeb69-185">鍵盤導覽的不同層面提供不同的方式讓使用者流覽 UI。</span><span class="sxs-lookup"><span data-stu-id="eeb69-185">Different aspects of keyboard navigation provide different ways for users to navigate the UI.</span></span>

<span data-ttu-id="eeb69-186">應用程式應該提供下列鍵盤介面：</span><span class="sxs-lookup"><span data-stu-id="eeb69-186">Applications should provide the following keyboard interfaces:</span></span>

-   <span data-ttu-id="eeb69-187">快速鍵，以及所有命令、功能表和控制項的加底線存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="eeb69-187">Shortcut keys and underlined access keys for all commands, menus, and controls.</span></span>
-   <span data-ttu-id="eeb69-188">重要連結的鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="eeb69-188">Keyboard shortcuts to important links.</span></span>
-   <span data-ttu-id="eeb69-189">所有功能表項目都有存取金鑰;所有按鈕都有快速鍵，所有命令都有快速鍵。</span><span class="sxs-lookup"><span data-stu-id="eeb69-189">All menu items have an access key; all buttons have accelerator keys, all commands have an accelerator key.</span></span>

### <a name="do-not-let-mouse-location-interfere-with-keyboard-navigation"></a><span data-ttu-id="eeb69-190">不要讓滑鼠位置干擾鍵盤巡覽</span><span class="sxs-lookup"><span data-stu-id="eeb69-190">Do Not Let Mouse Location Interfere with Keyboard Navigation</span></span>

<span data-ttu-id="eeb69-191">滑鼠位置不應干擾鍵盤巡覽。</span><span class="sxs-lookup"><span data-stu-id="eeb69-191">Mouse location should not interfere with keyboard navigation.</span></span> <span data-ttu-id="eeb69-192">例如，如果滑鼠置於某個位置，而且使用者正在以鍵盤巡覽，則不應發生滑鼠點選，除非這是由使用者啟始的。</span><span class="sxs-lookup"><span data-stu-id="eeb69-192">For example, if the mouse is positioned someplace and the user is navigating with the keyboard, a mouse click should not happen unless initiated by the user.</span></span>

## <a name="multi-modal-interface"></a><span data-ttu-id="eeb69-193">多重模式介面</span><span class="sxs-lookup"><span data-stu-id="eeb69-193">Multi-modal Interface</span></span>

<span data-ttu-id="eeb69-194">本節中的最佳做法可確保應用程式 UI 包含視覺元素的替代方案。</span><span class="sxs-lookup"><span data-stu-id="eeb69-194">The best practice in this section ensures that the application UI includes alternatives for visual elements.</span></span>

### <a name="provide-user-selectable-equivalents-for-non-text-elements"></a><span data-ttu-id="eeb69-195">對於非文字項目提供使用者可選取的對等項目</span><span class="sxs-lookup"><span data-stu-id="eeb69-195">Provide User-Selectable Equivalents for Non-Text Elements</span></span>

<span data-ttu-id="eeb69-196">對於每個非文字項目，提供文字、文字記錄或音訊描述之使用者可選取的對等項目，如替代文字、標題或視覺化回饋。</span><span class="sxs-lookup"><span data-stu-id="eeb69-196">For each non-text element, provide a user-selectable equivalent for text, transcripts, or audio descriptions, such as alt text, captions, or visual feedback.</span></span>

<span data-ttu-id="eeb69-197">非文字元素涵蓋範圍廣泛的 UI 元素，包括：影像、影像地圖區域、動畫、applet、框架、腳本、圖形按鈕、音效、獨立音訊檔案和影片。</span><span class="sxs-lookup"><span data-stu-id="eeb69-197">Non-text elements cover a wide range of UI elements including: images, image map regions, animations, applets, frames, scripts, graphical buttons, sounds, stand-alone audio files and video.</span></span> <span data-ttu-id="eeb69-198">如果非文字元素包含使用者需要存取的視覺資訊、語音或一般音訊資訊，以瞭解 UI 的內容，就很重要。</span><span class="sxs-lookup"><span data-stu-id="eeb69-198">Non-text elements are important when they contain visual information, speech, or general audio information that the user needs access to in order to understand the content of the UI.</span></span>

### <a name="use-color-but-also-provide-alternatives-to-color"></a><span data-ttu-id="eeb69-199">使用色彩，但是也提供色彩的替代方案</span><span class="sxs-lookup"><span data-stu-id="eeb69-199">Use Color but Also Provide Alternatives to Color</span></span>

<span data-ttu-id="eeb69-200">請使用色彩來增強及強調，或再次提醒以其他方式顯示的資訊，但請勿單獨使用色彩傳達資訊。</span><span class="sxs-lookup"><span data-stu-id="eeb69-200">Use color to enhance, emphasize, or reiterate information shown by other means, but do not communicate information by using color alone.</span></span> <span data-ttu-id="eeb69-201">色盲或使用單色顯示器的使用者需要色彩的替代方案。</span><span class="sxs-lookup"><span data-stu-id="eeb69-201">Users who are color blind or have a monochrome display need alternatives to color.</span></span>

### <a name="use-standard-input-apis-with-device-independent-calls"></a><span data-ttu-id="eeb69-202">藉由與裝置無關的呼叫使用標準輸入的 API</span><span class="sxs-lookup"><span data-stu-id="eeb69-202">Use Standard Input APIs with Device-Independent Calls</span></span>

<span data-ttu-id="eeb69-203">與裝置無關的呼叫可確保所有輸入裝置均視為相同，同時提供具有 UI 所需資訊的輔助技術產品。</span><span class="sxs-lookup"><span data-stu-id="eeb69-203">Device-independent calls ensure that all input devices are treated equally, while providing assistive technology products with needed information about the UI.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eeb69-204">相關主題</span><span class="sxs-lookup"><span data-stu-id="eeb69-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eeb69-205">Windows Automation API 總覽</span><span class="sxs-lookup"><span data-stu-id="eeb69-205">Windows Automation API Overview</span></span>](windows-automation-api-overview.md)
</dt> </dl>

 

 




