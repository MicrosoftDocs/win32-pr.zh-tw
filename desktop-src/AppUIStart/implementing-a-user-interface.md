---
title: 執行消費者介面
description: 本節說明一些與執行 Windows 應用程式之使用者介面相關聯的工作。
ms.assetid: 889791a7-d12c-4ec6-9b04-8fed14ecdb2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0941458e046a85dc6e27a684d8aa3a7ea609e889
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315733"
---
# <a name="implementing-a-user-interface"></a><span data-ttu-id="3bcbc-103">執行消費者介面</span><span class="sxs-lookup"><span data-stu-id="3bcbc-103">Implementing a User Interface</span></span>

<span data-ttu-id="3bcbc-104">本節說明一些與執行 Windows 應用程式之使用者介面相關聯的工作。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-104">This section describes some of the tasks associated with implementing a user interface for a Windows application.</span></span>

-   [<span data-ttu-id="3bcbc-105">原型</span><span class="sxs-lookup"><span data-stu-id="3bcbc-105">Prototype</span></span>](#prototype)
-   [<span data-ttu-id="3bcbc-106">構建</span><span class="sxs-lookup"><span data-stu-id="3bcbc-106">Construct</span></span>](#construct)
-   [<span data-ttu-id="3bcbc-107">簡化</span><span class="sxs-lookup"><span data-stu-id="3bcbc-107">Simplify</span></span>](#simplify)
    -   [<span data-ttu-id="3bcbc-108">減少、重複使用、清理</span><span class="sxs-lookup"><span data-stu-id="3bcbc-108">Reduce, Reuse, Declutter</span></span>](#reduce-reuse-declutter)
    -   [<span data-ttu-id="3bcbc-109">最佳的 UI 不是 UI</span><span class="sxs-lookup"><span data-stu-id="3bcbc-109">The Best UI Is No UI</span></span>](#the-best-ui-is-no-ui)
    -   [<span data-ttu-id="3bcbc-110">較少的 UI 是較佳的 UI</span><span class="sxs-lookup"><span data-stu-id="3bcbc-110">Less UI Is Better UI</span></span>](#less-ui-is-better-ui)
    -   [<span data-ttu-id="3bcbc-111">一致的 UI 是良好的 UI</span><span class="sxs-lookup"><span data-stu-id="3bcbc-111">Consistent UI is Good UI</span></span>](#consistent-ui-is-good-ui)

## <a name="prototype"></a><span data-ttu-id="3bcbc-112">原型</span><span class="sxs-lookup"><span data-stu-id="3bcbc-112">Prototype</span></span>

<span data-ttu-id="3bcbc-113">使用者介面 (UI) 應該從使用者案例的清單和使用者分析步驟中所識別的需求來設計。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-113">User interfaces (UI) should be designed from the list of user scenarios and requirements that were identified in the user analysis step.</span></span>

<span data-ttu-id="3bcbc-114">原型可以像鉛筆草圖一樣簡單，也可以像互動式螢幕原型一樣複雜。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-114">Prototypes can be as simple as pencil sketches or as complex as interactive screen mockups.</span></span> <span data-ttu-id="3bcbc-115">請保留所有先前的工作，因為它在顯示專案關係人的替代方案是已考慮的替代方案，並說明其捨棄原因。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-115">Keep all previous work as it can be useful when showing stakeholders the alternatives that were considered and explaining why they were discarded.</span></span>

<span data-ttu-id="3bcbc-116">請嘗試將此步驟限制為最多兩個或三個原型。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-116">Try to limit this step to two or three prototypes at most.</span></span> <span data-ttu-id="3bcbc-117">原型不需要完整的;他們只需要有效地模擬實際應用程式的使用體驗。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-117">Prototypes do not have to be exhaustive; they just have to effectively simulate the experience of using the real application.</span></span>

<span data-ttu-id="3bcbc-118">示範原型並追蹤使用者意見反應，以協助找出一般可用性趨勢。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-118">Demonstrate the prototypes and track user feedback to help identify the general usability trends.</span></span> <span data-ttu-id="3bcbc-119">如果可能的話，請捨棄最少成功的原型，並盡可能將最有用的意見反應納入一或多個其餘的原型中。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-119">If it is possible, discard the least successful prototypes and incorporate as much useful feedback as possible into one or more of the remaining prototypes.</span></span> <span data-ttu-id="3bcbc-120">在時間和資源允許的情況下重複此程式。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-120">Repeat this process as time and resources allow.</span></span>

<span data-ttu-id="3bcbc-121">有各種原型工具可供使用，包括 Microsoft Expression Studio 3 中的 [SketchFlow](/previous-versions/visualstudio/design-tools/expression-studio-3/ee341458(v=expression.30)) 、Microsoft Visual Studio 中的版面配置編輯器，甚至 Microsoft 小畫家。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-121">There are various prototyping tools available including [SketchFlow](/previous-versions/visualstudio/design-tools/expression-studio-3/ee341458(v=expression.30)) in Microsoft Expression Studio 3, the layout editor in Microsoft Visual Studio, and even Microsoft Paint.</span></span>

## <a name="construct"></a><span data-ttu-id="3bcbc-122">建構</span><span class="sxs-lookup"><span data-stu-id="3bcbc-122">Construct</span></span>

<span data-ttu-id="3bcbc-123">當您執行應用程式的使用者介面時，請考慮下列事項：</span><span class="sxs-lookup"><span data-stu-id="3bcbc-123">When you implement the user interface for an application, consider the following:</span></span>

-   <span data-ttu-id="3bcbc-124">命令結構</span><span class="sxs-lookup"><span data-stu-id="3bcbc-124">Command structure</span></span>

    <span data-ttu-id="3bcbc-125">判斷是否要根據功能表和工具列，或是以 Windows 功能區架構為基礎的替代命令結構來執行傳統的命令結構。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-125">Determine whether to implement a traditional command structure based on menus and toolbars, or an alternative command structure based on the Windows Ribbon Framework.</span></span> <span data-ttu-id="3bcbc-126">如需詳細資訊，請參閱 [功能表](../menurc/menus.md)、 [工具列](../controls/toolbar-control-reference.md)和 [Windows 功能區架構](../windowsribbon/-uiplat-windowsribbon-entry.md)。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-126">For more information, see [Menus](../menurc/menus.md), [Toolbars](../controls/toolbar-control-reference.md), and [Windows Ribbon Framework](../windowsribbon/-uiplat-windowsribbon-entry.md).</span></span>

-   <span data-ttu-id="3bcbc-127">視窗和對話方塊</span><span class="sxs-lookup"><span data-stu-id="3bcbc-127">Windows and dialog boxes</span></span>

    <span data-ttu-id="3bcbc-128">根據 UI 設計和原型工作，執行應用程式視窗，包括主視窗、子視窗、對話方塊和訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-128">Based on the UI design and prototyping work, implement the application windows, including the main window, child windows, dialog boxes, and message boxes.</span></span> <span data-ttu-id="3bcbc-129">遵循 UX 指導方針，以決定要在視窗和對話方塊中使用的樣式和控制項。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-129">Follow the UX Guidelines to determine which styles and controls to use in the windows and dialog boxes.</span></span> <span data-ttu-id="3bcbc-130">如需詳細資訊，請參閱 [視窗](../winmsg/windows.md)、 [對話方塊](../dlgbox/dialog-boxes.md)和 [windows 控制項](../controls/window-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-130">For more information, see [Windows](../winmsg/windows.md), [Dialog Boxes](../dlgbox/dialog-boxes.md), and [Windows Controls](../controls/window-controls.md).</span></span>

-   <span data-ttu-id="3bcbc-131">自訂控制項</span><span class="sxs-lookup"><span data-stu-id="3bcbc-131">Custom controls</span></span>

    <span data-ttu-id="3bcbc-132">只有當您無法從其中一個標準 Windows 控制項取得您想要的功能時，才建立新的自訂控制項。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-132">Create new custom controls only if you cannot get the functionality that you want from one of the standard Windows controls.</span></span> <span data-ttu-id="3bcbc-133">新自訂控制項的開發成本相當高，需要額外的工作才能讓它們可供存取。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-133">New custom controls are very costly to develop and require additional work to make them accessible.</span></span> <span data-ttu-id="3bcbc-134">如果您的應用程式需要自訂控制項，請確定它們已適當地公開給輔助技術。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-134">If your application requires custom controls, make sure that they are adequately exposed to assistive technologies.</span></span> <span data-ttu-id="3bcbc-135">如需詳細資訊，請參閱 [自訂控制項](../controls/user-controls-intro.md) 和 [Windows 自動化 API](../winauto/windows-automation-api-portal.md)。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-135">For more information, see [Custom Controls](../controls/user-controls-intro.md) and [Windows Automation API](../winauto/windows-automation-api-portal.md).</span></span>

-   <span data-ttu-id="3bcbc-136">標準使用者輸入裝置的支援</span><span class="sxs-lookup"><span data-stu-id="3bcbc-136">Support for standard user input devices</span></span>

    <span data-ttu-id="3bcbc-137">大部分的 Windows 應用程式都需要透過鍵盤和滑鼠支援使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-137">Most Windows applications need to support user input through the keyboard and mouse.</span></span> <span data-ttu-id="3bcbc-138">只要透過鍵盤流覽及存取所有應用程式功能，就會對視力受損或有行動性問題的使用者特別重要。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-138">The ability to navigate and access all application functionality through the keyboard alone is especially important for users who are vision-impaired or have mobility issues.</span></span> <span data-ttu-id="3bcbc-139">如需詳細資訊，請參閱 [使用者輸入](../inputdev/user-input.md) 和 [協助工具的工程軟體電子書](https://www.microsoft.com/download/details.aspx?id=19262)。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-139">For more information, see [User Input](../inputdev/user-input.md) and the [Engineering Software for Accessibility eBook](https://www.microsoft.com/download/details.aspx?id=19262).</span></span>

-   <span data-ttu-id="3bcbc-140">視覺化樣式、動畫和視覺效果</span><span class="sxs-lookup"><span data-stu-id="3bcbc-140">Visual styles, animations, and visual effects</span></span>

    <span data-ttu-id="3bcbc-141">Windows 包含數種技術，可讓您用來新增視覺效果，並將 UI 與其他應用程式分開。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-141">Windows includes several technologies that you can use to add visual interest and set the UI apart from that of other applications.</span></span> <span data-ttu-id="3bcbc-142">這些包括指定控制項的視覺化樣式、將動畫新增至 UI 元素，以及在 UI 中執行各種視覺效果。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-142">These include specifying the visual styles of controls, adding animations to UI elements, and implementing various visual effects in the UI.</span></span> <span data-ttu-id="3bcbc-143">如需詳細資訊，請參閱 [視覺化樣式](../controls/themes-overview.md)、 [Windows 動畫管理員](../uianimation/-main-portal.md)和 [桌面視窗管理員](../dwm/dwm-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-143">For more information, see [Visual Styles](../controls/themes-overview.md), [Windows Animation Manager](../uianimation/-main-portal.md), and [Desktop Window Manager](../dwm/dwm-overview.md).</span></span>

## <a name="simplify"></a><span data-ttu-id="3bcbc-144">簡化 </span><span class="sxs-lookup"><span data-stu-id="3bcbc-144">Simplify</span></span>

<span data-ttu-id="3bcbc-145">成功的使用者體驗取決於開發人員在設計過程中的方法、觀點和假設。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-145">A successful user experience depends on the approach, perspective, and assumptions of the developer during the design process.</span></span> <span data-ttu-id="3bcbc-146">對目標物件的應用程式的使用方式有基本的瞭解，需要能夠廣泛地思考，超越開發人員需求的限制。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-146">Achieving a basic understanding of how an application may be used by the target audience requires the ability to think broadly, beyond the constraints of what suits the needs of the developer.</span></span> <span data-ttu-id="3bcbc-147">在專案的開頭投資這段時間、精力和研究，將會在結束時支付紅利。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-147">Investing this time, effort, and research at the beginning of a project will pay dividends at the end.</span></span>

### <a name="reduce-reuse-declutter"></a><span data-ttu-id="3bcbc-148">減少、重複使用、清理</span><span class="sxs-lookup"><span data-stu-id="3bcbc-148">Reduce, Reuse, Declutter</span></span>

<span data-ttu-id="3bcbc-149">功能只有在實際使用時才會改善產品。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-149">Features only improve a product if they are actually used.</span></span> <span data-ttu-id="3bcbc-150">在許多情況下，增加的功能可能會造成複雜性，因為新增了更多的圖示、功能表項目、工具列，以及干擾效率和生產力的對話方塊，而不是增加價值。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-150">In many cases, the proliferation of features may introduce complexity with the addition of more icons, menu items, toolbars, and dialog boxes interfering with efficiency and productivity rather than adding value.</span></span>

### <a name="the-best-ui-is-no-ui"></a><span data-ttu-id="3bcbc-151">最佳的 UI 不是 UI</span><span class="sxs-lookup"><span data-stu-id="3bcbc-151">The Best UI Is No UI</span></span>

<span data-ttu-id="3bcbc-152">UI 表示使用者必須與應用程式互動以進行某些動作。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-152">UI implies that the user has to interact with the application to make something happen.</span></span> <span data-ttu-id="3bcbc-153">在理想的情況下，不需要任何互動。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-153">In the ideal case, no interaction is necessary.</span></span> <span data-ttu-id="3bcbc-154">從使用者的觀點來看，它只是可行的。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-154">From the user's perspective, it just works.</span></span> <span data-ttu-id="3bcbc-155">如果可以加入可安全移除使用者互動的功能，它會讓使用者體驗變得更好。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-155">If a feature can be added that safely removes a user interaction, it makes the user experience significantly better.</span></span>

### <a name="less-ui-is-better-ui"></a><span data-ttu-id="3bcbc-156">較少的 UI 是較佳的 UI</span><span class="sxs-lookup"><span data-stu-id="3bcbc-156">Less UI Is Better UI</span></span>

<span data-ttu-id="3bcbc-157">在許多情況下，不可能從使用者體驗中完全移除 UI 互動。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-157">In many cases, it is not possible to remove UI interaction completely from the user experience.</span></span> <span data-ttu-id="3bcbc-158">但是，應用程式所需的使用者互動越少越好。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-158">However, the less user interaction required by an application the better.</span></span>

<span data-ttu-id="3bcbc-159">識別使用者將使用應用程式執行的最常見和基本活動，並讓這些函式在 UI 中最為明顯。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-159">Identify the most common and essential activities that users will perform with the application and make those functions the most prominent in the UI.</span></span> <span data-ttu-id="3bcbc-160">以視覺化、階層方式或透過選擇性的應用程式設定和使用者喜好設定，將其他函式和活動 Relegate 至較小的狀態。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-160">Relegate other functions and activities to lesser status either visually, hierarchically, or through optional application settings and user preferences.</span></span>

-   <span data-ttu-id="3bcbc-161">取代新增（& a）</span><span class="sxs-lookup"><span data-stu-id="3bcbc-161">Replace Rather Than Add</span></span>

    <span data-ttu-id="3bcbc-162">保留 UI 規則會指出您只在可以離開一些東西時，才會新增一些內容。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-162">The conservation of UI rule states that you add something only when you can take something away.</span></span> <span data-ttu-id="3bcbc-163">這項規則會藉由考慮功能對整個使用者體驗的影響，來強制開發人員認真考慮新的功能。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-163">This rule forces a developer to think critically about a new feature by considering the impact that the feature has on the whole user experience.</span></span>

    <span data-ttu-id="3bcbc-164">新功能不應升級，因為它們是新功能：請勿將行銷與可用性混淆。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-164">New features should not be promoted because they are new: do not confuse marketing with usability.</span></span> <span data-ttu-id="3bcbc-165">若要協助使用者尋找您產品中的新功能，請將專案新增至 **說明功能表，** 以描述自上次應用程式版本以來發生的變更。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-165">To help users find new features in your product, add an item to the **Help** menu that describes the changes that have occurred since the last version of the application.</span></span>

-   <span data-ttu-id="3bcbc-166">使用者是受限的資源</span><span class="sxs-lookup"><span data-stu-id="3bcbc-166">The User is a Limited Resource</span></span>

    <span data-ttu-id="3bcbc-167">在任何時間公開的功能越多，使用者就越難找到所需的功能。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-167">The more functionality that is exposed at any one time, the more difficult it is for a user to find the functionality that they need.</span></span>

-   <span data-ttu-id="3bcbc-168">它會因為中斷而受到干擾</span><span class="sxs-lookup"><span data-stu-id="3bcbc-168">It's Rude to Interrupt</span></span>

    <span data-ttu-id="3bcbc-169">當應用程式顯示對話方塊時，它會強制使用者停止其正在執行的任何動作，並留意其他事項。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-169">When an application displays a dialog box, it forces the user to stop whatever it is that they are doing and pay attention to something else.</span></span> <span data-ttu-id="3bcbc-170">如果有可能，請避免錯誤案例和其他干擾性使用者體驗，完全移除對話方塊的需求。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-170">If it is possible, remove the need for a dialog box completely by avoiding error cases and other disruptive user experiences.</span></span> <span data-ttu-id="3bcbc-171">如需訊息指導方針的詳細資訊，請參閱 [訊息](https://msdn.microsoft.com/library/dd535525.aspx)。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-171">For more information about message guidelines, see [Messages](https://msdn.microsoft.com/library/dd535525.aspx).</span></span>

-   <span data-ttu-id="3bcbc-172">簡單可以強大</span><span class="sxs-lookup"><span data-stu-id="3bcbc-172">Simple Can Be Powerful</span></span>

    <span data-ttu-id="3bcbc-173">簡單的 UI 並不表示缺少功能。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-173">A simple UI does not imply a lack of functionality.</span></span> <span data-ttu-id="3bcbc-174">一般而言，較簡單的 UI 結果是縮短學習曲線、提高效率，並提升生產力。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-174">Typically, the result of a simpler UI is a shortened learning curve, increased efficiency, and improved productivity.</span></span> <span data-ttu-id="3bcbc-175">這可讓使用者透過應用程式提高他們的熟練度。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-175">This empowers a user to increase their proficiency with the application.</span></span>

### <a name="consistent-ui-is-good-ui"></a><span data-ttu-id="3bcbc-176">一致的 UI 是良好的 UI</span><span class="sxs-lookup"><span data-stu-id="3bcbc-176">Consistent UI is Good UI</span></span>

<span data-ttu-id="3bcbc-177">一般來說，建議您在整個應用程式 UI 中都能達到一致性。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-177">Generally, it is recommended to strive for consistency throughout an application UI.</span></span> <span data-ttu-id="3bcbc-178">提供一致的 UI 可讓使用者在更短的時間內更熟悉應用程式。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-178">Providing a consistent UI enables a user to become more proficient with an application in a much shorter time.</span></span> <span data-ttu-id="3bcbc-179">他們可以將應用程式的現有知識套用至不同的情況，並放心使用不熟悉的功能。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-179">They are able to apply their existing knowledge of the application to different situations and use unfamiliar functionality with confidence.</span></span>

<span data-ttu-id="3bcbc-180">在罕見的情況下，一致性對使用者不提供任何好處，甚至可能會降低使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-180">In rare cases, consistency provides no benefit to the user and can even degrade the user experience.</span></span> <span data-ttu-id="3bcbc-181">如果該一致性對完成工作的能力造成不利的影響，請勿讓 UI 保持一致。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-181">Do not make the UI consistent if that consistency impairs the ability to accomplish a task.</span></span> <span data-ttu-id="3bcbc-182">本身的一致性並不保證可用性。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-182">Consistency in itself does not guarantee usability.</span></span> <span data-ttu-id="3bcbc-183">將介面中的一致性視為良好的設計，是一項錯誤。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-183">It is a mistake to think that consistency in the interface will lead to good design.</span></span>

<span data-ttu-id="3bcbc-184">例如，影片遊戲 UI 通常非常特定于遊戲的種類。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-184">For example, video game UI is typically very specific to the kind of game.</span></span> <span data-ttu-id="3bcbc-185">如果您嘗試設計的一般 UI 適用于兩個專門的遊戲，而這兩個遊戲都需要方向盤，另一個則與搖桿和按鈕最有效果，則可能不會成功。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-185">Trying to design a generic UI that works well for two specialized games, one that requires a steering wheel and another that works best with a joystick and buttons, is likely not going to be successful for either game.</span></span> <span data-ttu-id="3bcbc-186">最好是盡可能地達成，這對兩者而言並不適用。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-186">At best a middle ground is likely to be achieved that is not good for either.</span></span>

<span data-ttu-id="3bcbc-187">有很多關於如何使用專案的資料，是進行這項決策的關鍵。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-187">Having good data about how things are used is the key to making this decision.</span></span> <span data-ttu-id="3bcbc-188">請清楚瞭解每個取捨的優缺點， (速度與可靠性、輕鬆學習與專業知識、全球一致性和本機優化) ，以及針對與整個產品相關的功能做出最佳決策。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-188">Be clear about the pros and cons of each tradeoff (speed versus reliability, ease of learning versus expert proficiency, global consistency versus local optimization) and make the best decisions for the feature in relation to the whole product.</span></span>

<span data-ttu-id="3bcbc-189">設計是選擇失敗的方法：針對某個事物進行優化，表示另一種情況是失敗的。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-189">Design is choosing how to fail: optimizing for one thing means failing at another.</span></span> <span data-ttu-id="3bcbc-190">良好的 UI 設計關鍵在於能夠決定應用程式的哪些特性是最重要的，以及可以剪下哪些特性。</span><span class="sxs-lookup"><span data-stu-id="3bcbc-190">The key to good UI design is being able to decide which characteristics of the application are the most important, and which ones can be cut.</span></span>

 

 