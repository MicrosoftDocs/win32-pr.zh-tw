---
title: 屬性視窗
description: '[屬性視窗] 是下列使用者介面類別型的集體名稱 (Ui) 屬性工作表，用於在對話方塊中，用來查看和變更物件或物件集合的屬性。屬性偵測器，用來在窗格中用來查看和變更物件或物件集合的屬性。用來查看和變更應用程式選項的 [選項] 對話方塊。'
ms.assetid: 18fc04da-9f84-4a44-9f3d-a9e29b121e7c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c255d638f236b4bc4a4f1a6c923eac24421cfe9d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "103696100"
---
# <a name="property-windows"></a><span data-ttu-id="60d41-103">屬性視窗</span><span class="sxs-lookup"><span data-stu-id="60d41-103">Property Windows</span></span>

> [!NOTE]
> <span data-ttu-id="60d41-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="60d41-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="60d41-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="60d41-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="60d41-106">[屬性視窗] 是下列使用者介面類別型的集體名稱 (Ui) ：</span><span class="sxs-lookup"><span data-stu-id="60d41-106">Property window is the collective name for the following types of user interfaces (UIs):</span></span>

-   <span data-ttu-id="60d41-107">屬性工作表：用於 **在對話方塊中，用來查看和變更物件或物件集合的屬性**。</span><span class="sxs-lookup"><span data-stu-id="60d41-107">Property sheet: used to **view and change properties for an object or collection of objects in a dialog box**.</span></span>
-   <span data-ttu-id="60d41-108">屬性偵測器： **在窗格中用來查看和變更物件或物件集合的屬性**。</span><span class="sxs-lookup"><span data-stu-id="60d41-108">Property inspector: used to **view and change properties for an object or collection of objects in a pane**.</span></span>
-   <span data-ttu-id="60d41-109">[選項] 對話方塊：用來 **查看和變更應用程式的選項**。</span><span class="sxs-lookup"><span data-stu-id="60d41-109">Options dialog box: used to **view and change options for an application**.</span></span>

<span data-ttu-id="60d41-110">物件的屬性是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="60d41-110">A property for an object is either of the following:</span></span>

-   <span data-ttu-id="60d41-111">使用者可變更的設定 (例如檔案的名稱和唯讀屬性) 。</span><span class="sxs-lookup"><span data-stu-id="60d41-111">A setting that users can change (such as a file's name and read-only attribute).</span></span>
-   <span data-ttu-id="60d41-112">物件的屬性，使用者無法直接變更 (例如檔案的大小和建立日期) 。</span><span class="sxs-lookup"><span data-stu-id="60d41-112">An attribute of an object that users cannot directly change (such as a file's size and creation date).</span></span>

<span data-ttu-id="60d41-113">不同于對話方塊 ([選項] 對話方塊以外) 和嚮導，屬性視窗通常支援數個工作，而不是單一工作。</span><span class="sxs-lookup"><span data-stu-id="60d41-113">Unlike dialog boxes (other than options dialogs) and wizards, property windows typically support several tasks instead of a single task.</span></span>

<span data-ttu-id="60d41-114">屬性視窗通常會組織成可透過索引標籤存取的頁面。</span><span class="sxs-lookup"><span data-stu-id="60d41-114">Property windows are usually organized into pages, which are accessed through tabs.</span></span> <span data-ttu-id="60d41-115">屬性視窗通常會與索引標籤 (相關聯，反之亦然) ，但索引標籤 **不是屬性視窗的必要選項**。</span><span class="sxs-lookup"><span data-stu-id="60d41-115">Property windows are often associated with tabs (and vice versa), but **tabs are not essential to property windows**.</span></span>

![<span data-ttu-id="60d41-116">[檔案屬性] 屬性工作表的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="60d41-116">screen shot of document properties property sheet</span></span> ](images/win-property-win-image1.png)

<span data-ttu-id="60d41-117">一般的屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="60d41-117">A typical property sheet.</span></span>

<span data-ttu-id="60d41-118">**注意：** 與 [版面](vis-layout.md) 配置和索引標籤 [相關的指導方針會顯示](ctrl-tabs.md) 在不同的文章中。</span><span class="sxs-lookup"><span data-stu-id="60d41-118">**Note:** Guidelines related to [layout](vis-layout.md) and [tabs](ctrl-tabs.md) are presented in separate articles.</span></span>

## <a name="is-this-the-right-user-interface"></a><span data-ttu-id="60d41-119">這是正確的使用者介面嗎？</span><span class="sxs-lookup"><span data-stu-id="60d41-119">Is this the right user interface?</span></span>

<span data-ttu-id="60d41-120">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="60d41-120">To decide, consider these questions:</span></span>

-   <span data-ttu-id="60d41-121">**設定屬性是否需要使用者執行固定、非簡單的步驟順序？**</span><span class="sxs-lookup"><span data-stu-id="60d41-121">**Does setting the properties require users to perform a fixed, non-trivial sequence of steps?**</span></span> <span data-ttu-id="60d41-122">若是如此，請改用 [wizard](win-wizards.md) 或工作 [流程](glossary.md) 。</span><span class="sxs-lookup"><span data-stu-id="60d41-122">If so, use a [wizard](win-wizards.md) or [task flow](glossary.md) instead.</span></span>
-   <span data-ttu-id="60d41-123">**內容僅限應用程式的選項嗎？**</span><span class="sxs-lookup"><span data-stu-id="60d41-123">**Is the content solely an application's options?**</span></span> <span data-ttu-id="60d41-124">如果是，請使用 [選項] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="60d41-124">If so, use an options dialog box.</span></span>
-   <span data-ttu-id="60d41-125">**內容只是應用程式的屬性嗎？**</span><span class="sxs-lookup"><span data-stu-id="60d41-125">**Is the content solely an application's attributes?**</span></span> <span data-ttu-id="60d41-126">如果是，請使用 [ [關於](glossary.md)] 方塊。</span><span class="sxs-lookup"><span data-stu-id="60d41-126">If so, use an [About box](glossary.md).</span></span>
-   <span data-ttu-id="60d41-127">**內容大多是物件的屬性 (其設定或屬性) ？**</span><span class="sxs-lookup"><span data-stu-id="60d41-127">**Is the content mostly an object's properties (its settings or attributes)?**</span></span> <span data-ttu-id="60d41-128">如果沒有，請使用標準 [對話方塊對話方塊](win-dialog-box.md) 或索引標籤 [式對話方塊](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="60d41-128">If not, use a standard [dialog boxe](win-dialog-box.md) or [tabbed dialog box](glossary.md).</span></span>
-   <span data-ttu-id="60d41-129">使用者是否 **可能經常或超過一段長時間來查看或變更屬性？**</span><span class="sxs-lookup"><span data-stu-id="60d41-129">Are users **likely to view or change properties frequently or over an extended period of time?**</span></span> <span data-ttu-id="60d41-130">如果是，請使用屬性偵測器;否則，請使用屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="60d41-130">If so, use a property inspector; otherwise, use a property sheet.</span></span>
-   <span data-ttu-id="60d41-131">使用者是否 **可能一次看到或變更數個不同物件的屬性？**</span><span class="sxs-lookup"><span data-stu-id="60d41-131">Are users **likely to view or change properties for several different objects at a time?**</span></span> <span data-ttu-id="60d41-132">如果是，請使用屬性偵測器;否則，請使用屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="60d41-132">If so, use a property inspector; otherwise, use a property sheet.</span></span>

<span data-ttu-id="60d41-133">**屬性工作表和屬性偵測器不是獨佔的。**</span><span class="sxs-lookup"><span data-stu-id="60d41-133">**Property sheets and property inspectors aren't exclusive.**</span></span> <span data-ttu-id="60d41-134">您可以在屬性偵測器中顯示最常存取的屬性，以及在屬性工作表中顯示完整的設定。</span><span class="sxs-lookup"><span data-stu-id="60d41-134">You can display the most frequently accessed properties in a property inspector, and the complete set in the property sheet.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="60d41-135">設計概念</span><span class="sxs-lookup"><span data-stu-id="60d41-135">Design concepts</span></span>

<span data-ttu-id="60d41-136">**屬性視窗通常會成為奇數分類的低層級、以技術為基礎之設定的傾印。**</span><span class="sxs-lookup"><span data-stu-id="60d41-136">**Property windows often become a dumping ground for an odd assortment of low-level, technology-based settings.**</span></span> <span data-ttu-id="60d41-137">這些屬性通常會組織成索引標籤，但不是針對任何特定工作或使用者所設計。</span><span class="sxs-lookup"><span data-stu-id="60d41-137">Too often, these properties are organized into tabs, but beyond that not designed for any particular tasks or users.</span></span> <span data-ttu-id="60d41-138">如此一來，當使用者在屬性視窗中遇到工作時，通常不會知道該怎麼做。</span><span class="sxs-lookup"><span data-stu-id="60d41-138">As a result, when users are faced with a task in a property window, they often don't know what to do.</span></span>

<span data-ttu-id="60d41-139">若要確保您的屬性視窗有用且可用，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="60d41-139">To ensure that your property windows are useful and usable, follow these steps:</span></span>

-   <span data-ttu-id="60d41-140">請確定屬性是必要的。</span><span class="sxs-lookup"><span data-stu-id="60d41-140">Make sure the properties are necessary.</span></span>
-   <span data-ttu-id="60d41-141">以使用者目標為依據，而不是以技術呈現屬性。</span><span class="sxs-lookup"><span data-stu-id="60d41-141">Present properties in terms of user goals, not technology.</span></span>
-   <span data-ttu-id="60d41-142">將屬性顯示在正確層級。</span><span class="sxs-lookup"><span data-stu-id="60d41-142">Present properties at the right level.</span></span>
-   <span data-ttu-id="60d41-143">特定工作的設計頁面。</span><span class="sxs-lookup"><span data-stu-id="60d41-143">Design pages for specific tasks.</span></span>
-   <span data-ttu-id="60d41-144">特定使用者的設計頁面， (非系統管理員) ，尤其是限制使用者。</span><span class="sxs-lookup"><span data-stu-id="60d41-144">Design pages for specific users, especially limited users (non-administrators).</span></span>
-   <span data-ttu-id="60d41-145">有效率地組織屬性頁。</span><span class="sxs-lookup"><span data-stu-id="60d41-145">Organize the property pages efficiently.</span></span>

<span data-ttu-id="60d41-146">**如果您只做一件事 .。。**</span><span class="sxs-lookup"><span data-stu-id="60d41-146">**If you do only one thing...**</span></span>

<span data-ttu-id="60d41-147">以使用者目標為依據，而不是以技術呈現屬性。</span><span class="sxs-lookup"><span data-stu-id="60d41-147">Present properties in terms of user goals, not technology.</span></span> <span data-ttu-id="60d41-148">假設您正在說明屬性，以及它對 friend 而言很有用的原因。</span><span class="sxs-lookup"><span data-stu-id="60d41-148">Pretend that you are explaining the property and why it is useful to a friend.</span></span> <span data-ttu-id="60d41-149">您要如何加以解釋？</span><span class="sxs-lookup"><span data-stu-id="60d41-149">How would you explain it?</span></span> <span data-ttu-id="60d41-150">您使用何種語言？</span><span class="sxs-lookup"><span data-stu-id="60d41-150">What language would you use?</span></span> <span data-ttu-id="60d41-151">這就是您在屬性頁中使用的語言。</span><span class="sxs-lookup"><span data-stu-id="60d41-151">That's the language to use in your property pages.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="60d41-152">使用模式</span><span class="sxs-lookup"><span data-stu-id="60d41-152">Usage patterns</span></span>

<span data-ttu-id="60d41-153">屬性視窗有數種使用模式。</span><span class="sxs-lookup"><span data-stu-id="60d41-153">Property windows have several usage patterns.</span></span>

-   <span data-ttu-id="60d41-154">屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="60d41-154">Property sheets.</span></span> <span data-ttu-id="60d41-155">單一物件的屬性會顯示在非強制回應對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="60d41-155">Properties for a single object are displayed in a modeless dialog box.</span></span>
-   <span data-ttu-id="60d41-156">多物件屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="60d41-156">Multiple-object property sheets.</span></span> <span data-ttu-id="60d41-157">多個物件的屬性會顯示在非強制回應對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="60d41-157">Properties for multiple objects are displayed in a modeless dialog box.</span></span>
-   <span data-ttu-id="60d41-158">有效的設定屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="60d41-158">Effective settings property sheets.</span></span> <span data-ttu-id="60d41-159">單一物件的有效屬性會顯示在非強制回應對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="60d41-159">The effective properties for a single object are displayed in a modeless dialog box.</span></span>
-   <span data-ttu-id="60d41-160">選項對話方塊。</span><span class="sxs-lookup"><span data-stu-id="60d41-160">Options dialog boxes.</span></span> <span data-ttu-id="60d41-161">應用程式的屬性會顯示在強制回應對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="60d41-161">Properties for an application are displayed in a modal dialog box.</span></span>
-   <span data-ttu-id="60d41-162">屬性偵測器。</span><span class="sxs-lookup"><span data-stu-id="60d41-162">Property inspectors.</span></span> <span data-ttu-id="60d41-163">目前選取範圍的屬性 (單一物件或物件群組) 顯示在非強制回應視窗窗格或未移除視窗中。</span><span class="sxs-lookup"><span data-stu-id="60d41-163">Properties for the current selection (a single object or group of objects) are displayed in a modeless window pane or undocked window.</span></span>

<span data-ttu-id="60d41-164">屬性偵測器以外的所有屬性視窗模式都使用延遲認可，這表示只有當使用者按一下 [確定] 或 [套用] 時，變更才會生效。</span><span class="sxs-lookup"><span data-stu-id="60d41-164">All property window patterns except property inspectors use a delayed commit, meaning that changes take effect only when users click OK or Apply.</span></span> <span data-ttu-id="60d41-165">屬性偵測器會使用立即認可 (當使用者變更) 時，就會變更屬性，因此不需要 [確定]、[取消] 和 [套用] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="60d41-165">Property inspectors use an immediate commit (properties are changed as soon as users make changes), so there is no need for OK, Cancel, and Apply buttons.</span></span>

## <a name="guidelines"></a><span data-ttu-id="60d41-166">指導方針</span><span class="sxs-lookup"><span data-stu-id="60d41-166">Guidelines</span></span>

### <a name="property-sheets"></a><span data-ttu-id="60d41-167">屬性工作表</span><span class="sxs-lookup"><span data-stu-id="60d41-167">Property sheets</span></span>

-   <span data-ttu-id="60d41-168">**當使用者時顯示內容表：**</span><span class="sxs-lookup"><span data-stu-id="60d41-168">**Display a property sheet when users:**</span></span>
    -   <span data-ttu-id="60d41-169">選取物件的 [屬性] 命令。</span><span class="sxs-lookup"><span data-stu-id="60d41-169">Select the Properties command for an object.</span></span>
    -   <span data-ttu-id="60d41-170">設定物件的輸入焦點，然後按 Alt + Enter。</span><span class="sxs-lookup"><span data-stu-id="60d41-170">Set input focus on an object and press Alt+Enter.</span></span>

<span data-ttu-id="60d41-171">**多物件屬性工作表**</span><span class="sxs-lookup"><span data-stu-id="60d41-171">**Multiple-object property sheets**</span></span>

-   <span data-ttu-id="60d41-172">**顯示所有選取物件的通用屬性。**</span><span class="sxs-lookup"><span data-stu-id="60d41-172">**Display the common properties of all the selected objects.**</span></span> <span data-ttu-id="60d41-173">如果屬性值不同，則會使用混合狀態顯示與這些值相關聯的控制項。</span><span class="sxs-lookup"><span data-stu-id="60d41-173">Where the property values differ, display the controls associated with those values using a mixed state.</span></span> <span data-ttu-id="60d41-174"> (參閱使用混合狀態值的個別控制指導方針。 ) </span><span class="sxs-lookup"><span data-stu-id="60d41-174">(See the respective control guidelines for using mixed-state values.)</span></span>
-   <span data-ttu-id="60d41-175">如果選取的物件是多個離散物件的集合 (例如檔案資料夾) ，則會 **顯示單一群組物件的屬性，而不是個別物件的多物件屬性工作表。**</span><span class="sxs-lookup"><span data-stu-id="60d41-175">If the selected object is a collection of multiple discrete objects (such as a file folder), **display the properties of the single grouped object instead of a multiple-object property sheet for the discrete objects.**</span></span>

### <a name="options-dialog-boxes"></a><span data-ttu-id="60d41-176">選項對話方塊</span><span class="sxs-lookup"><span data-stu-id="60d41-176">Options dialog boxes</span></span>

-   <span data-ttu-id="60d41-177">**請勿將選項與自訂區隔開。**</span><span class="sxs-lookup"><span data-stu-id="60d41-177">**Don't separate options from customization.**</span></span> <span data-ttu-id="60d41-178">也就是說，沒有選項命令和自訂命令。</span><span class="sxs-lookup"><span data-stu-id="60d41-178">That is, don't have both an Options command and a Customize command.</span></span> <span data-ttu-id="60d41-179">使用者通常會因為這種分隔而混淆。</span><span class="sxs-lookup"><span data-stu-id="60d41-179">Users are often confused by this separation.</span></span> <span data-ttu-id="60d41-180">相反地，透過選項來存取自訂。</span><span class="sxs-lookup"><span data-stu-id="60d41-180">Instead, access customization through options.</span></span>

### <a name="property-pages"></a><span data-ttu-id="60d41-181">「屬性頁」</span><span class="sxs-lookup"><span data-stu-id="60d41-181">Property pages</span></span>

-   <span data-ttu-id="60d41-182">**請針對頁面順序遵循下列指導方針：**</span><span class="sxs-lookup"><span data-stu-id="60d41-182">**Follow these guidelines for page order:**</span></span>
    -   <span data-ttu-id="60d41-183">將 [一般] 頁面或其對等專案設為第一頁。</span><span class="sxs-lookup"><span data-stu-id="60d41-183">Make the General page or its equivalent the first page.</span></span>
    -   <span data-ttu-id="60d41-184">使 [Advanced] 頁面或其對等的最後一頁。</span><span class="sxs-lookup"><span data-stu-id="60d41-184">Make the Advanced page or its equivalent the last page.</span></span>
    -   <span data-ttu-id="60d41-185">針對其餘的頁面：</span><span class="sxs-lookup"><span data-stu-id="60d41-185">For the remaining pages:</span></span>
        -   <span data-ttu-id="60d41-186">將它們組織成相關頁面的群組。</span><span class="sxs-lookup"><span data-stu-id="60d41-186">Organize them into groups of related pages.</span></span>
        -   <span data-ttu-id="60d41-187">依使用量的可能性來排序群組。</span><span class="sxs-lookup"><span data-stu-id="60d41-187">Order the groups by the likelihood of their usage.</span></span>
        -   <span data-ttu-id="60d41-188">在每個群組內，依其關聯性或其使用可能性來排列頁面的順序。</span><span class="sxs-lookup"><span data-stu-id="60d41-188">Within each group, order the pages either by their relationships or by the likelihood of their use.</span></span>
        -   <span data-ttu-id="60d41-189">您不應該有這麼多頁面需要依字母順序顯示。</span><span class="sxs-lookup"><span data-stu-id="60d41-189">You shouldn't have so many pages that there is a need to display them in alphabetical order.</span></span>
-   <span data-ttu-id="60d41-190">**藉由將每個頁面上的所有屬性關聯至單一、特定、以工作為基礎的目的，使頁面一致。**</span><span class="sxs-lookup"><span data-stu-id="60d41-190">**Make pages coherent by relating all properties on each page to a single, specific, task-based purpose.**</span></span>
-   <span data-ttu-id="60d41-191">**如果空間允許，請在頁面頂端說明 [屬性] 視窗的用途（如果您的目標使用者並不明顯的話）。**</span><span class="sxs-lookup"><span data-stu-id="60d41-191">**If space allows, explain the purpose of the property window at the top of the page if it isn't obvious to your target users.**</span></span> <span data-ttu-id="60d41-192">如果頁面只是用來執行單一工作，請 **將文字視為有關如何執行該工作的清楚指示**。</span><span class="sxs-lookup"><span data-stu-id="60d41-192">If the page is used to perform only a single task, **phrase the text as a clear instruction about how to perform that task**.</span></span> <span data-ttu-id="60d41-193">使用完整句子，以句號結尾。</span><span class="sxs-lookup"><span data-stu-id="60d41-193">Use complete sentences, ending with a period.</span></span>

    ![<span data-ttu-id="60d41-194">[防火牆內容] 屬性工作表的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="60d41-194">screen shot of firewall properties property sheet</span></span> ](images/win-property-win-image2.png)

    <span data-ttu-id="60d41-195">在此範例中，會在 [一般] 頁面頂端說明 Microsoft Windows 防火牆的用途。</span><span class="sxs-lookup"><span data-stu-id="60d41-195">In this example, the purpose of Microsoft Windows Firewall is explained at the top of the General page.</span></span>

-   <span data-ttu-id="60d41-196">**使用一致的控制項名稱和位置，在頁面之間保持類似的內容。**</span><span class="sxs-lookup"><span data-stu-id="60d41-196">**Make similar content consistent across pages by using consistent control names and locations.**</span></span> <span data-ttu-id="60d41-197">例如，如果有數個頁面有名稱方塊，請試著將它們放在頁面上的相同位置，並使用一致的標籤。</span><span class="sxs-lookup"><span data-stu-id="60d41-197">For example, if several pages have Name boxes, try to place them in the same location on the page and use consistent labels.</span></span> <span data-ttu-id="60d41-198">類似內容不應從頁面彈跳到頁面。</span><span class="sxs-lookup"><span data-stu-id="60d41-198">Similar content shouldn't bounce around from page to page.</span></span>
-   <span data-ttu-id="60d41-199">**將相同的屬性放在整個應用程式的相同頁面上。**</span><span class="sxs-lookup"><span data-stu-id="60d41-199">**Place the same property on the same page throughout your application.**</span></span> <span data-ttu-id="60d41-200">例如，不要在某個物件類型的 [一般] 索引標籤上，以及另一種類型的 [Advanced] 索引標籤上放置到期屬性。</span><span class="sxs-lookup"><span data-stu-id="60d41-200">For example, don't put an Expiration property on the General tab for one object type, and on the Advanced tab for another type.</span></span>
-   <span data-ttu-id="60d41-201">**如果使用者可能會在最後一個顯示的頁面上開始，請將頁面索引標籤保存，並依預設選取它。**</span><span class="sxs-lookup"><span data-stu-id="60d41-201">**If users are likely to start with the last page displayed, make the page tab persist, and select it by default.**</span></span> <span data-ttu-id="60d41-202">將設定保留在每個屬性的視窗上，以每個使用者為基礎。</span><span class="sxs-lookup"><span data-stu-id="60d41-202">Make the settings persist on a per-property window, per-user basis.</span></span> <span data-ttu-id="60d41-203">否則，預設會選取第一個頁面。</span><span class="sxs-lookup"><span data-stu-id="60d41-203">Otherwise, select the first page by default.</span></span>
-   <span data-ttu-id="60d41-204">**請勿讓頁面上的設定相依于其他頁面上的設定。**</span><span class="sxs-lookup"><span data-stu-id="60d41-204">**Don't make the settings on a page dependent upon settings on other pages.**</span></span> <span data-ttu-id="60d41-205">請改為將相依設定放在單一頁面上。</span><span class="sxs-lookup"><span data-stu-id="60d41-205">Put the dependent settings on a single page instead.</span></span> <span data-ttu-id="60d41-206">變更單一頁面上的設定時，不應該自動變更其他頁面上的設定。</span><span class="sxs-lookup"><span data-stu-id="60d41-206">Changing a setting on one page should never automatically change settings on other pages.</span></span>
    -   <span data-ttu-id="60d41-207">**例外狀況：** 如果相依設定在兩個不同的屬性視窗中，請使用靜態文字標籤來說明這兩個位置中的這項關聯性。</span><span class="sxs-lookup"><span data-stu-id="60d41-207">**Exception:** If the dependent settings are in two different property windows, use static text labels to explain this relationship in both locations.</span></span>
-   <span data-ttu-id="60d41-208">**不要滾動屬性頁。**</span><span class="sxs-lookup"><span data-stu-id="60d41-208">**Don't scroll property pages.**</span></span> <span data-ttu-id="60d41-209">索引標籤和捲軸可用來增加視窗的有效區域，但其中一種機制應該就已足夠。</span><span class="sxs-lookup"><span data-stu-id="60d41-209">Both tabs and scrollbars are used to increase the effective area of a window, but one mechanism should be sufficient.</span></span> <span data-ttu-id="60d41-210">不使用捲軸，讓屬性頁面變得更大，並有效率地配置頁面。</span><span class="sxs-lookup"><span data-stu-id="60d41-210">Instead of using scrollbars, make the property pages larger and lay out the pages efficiently.</span></span>

<span data-ttu-id="60d41-211">**第一頁**</span><span class="sxs-lookup"><span data-stu-id="60d41-211">**First pages**</span></span>

-   <span data-ttu-id="60d41-212">針對物件屬性， **將物件的名稱放在第一頁。**</span><span class="sxs-lookup"><span data-stu-id="60d41-212">For object properties, **put the object's name on the first page.**</span></span>
-   <span data-ttu-id="60d41-213">如果您要將 (選擇性) [圖示](vis-icons.md) 與物件產生關聯，請在第一頁的 **左上角顯示適當的圖示** 。</span><span class="sxs-lookup"><span data-stu-id="60d41-213">If you are associating (optional) [icons](vis-icons.md) with your objects, **display the appropriate icon in the upper-left corner** of the first page.</span></span>

<span data-ttu-id="60d41-214">**一般頁面**</span><span class="sxs-lookup"><span data-stu-id="60d41-214">**General pages**</span></span>

-   <span data-ttu-id="60d41-215">**避免一般頁面。**</span><span class="sxs-lookup"><span data-stu-id="60d41-215">**Avoid General pages.**</span></span> <span data-ttu-id="60d41-216">您不需要有 [一般] 頁面。</span><span class="sxs-lookup"><span data-stu-id="60d41-216">You aren't required to have a General page.</span></span> <span data-ttu-id="60d41-217">只有在下列情況時，才使用一般頁面：</span><span class="sxs-lookup"><span data-stu-id="60d41-217">Use a General page only if:</span></span>
    -   <span data-ttu-id="60d41-218">這些屬性適用于數個工作，對大部分的使用者而言都有意義。</span><span class="sxs-lookup"><span data-stu-id="60d41-218">The properties apply to several tasks and are meaningful to most users.</span></span> <span data-ttu-id="60d41-219">請勿在 [一般] 頁面上放置特製化或 advanced 屬性，但您可以透過 [一般] 頁面上的 [命令] 按鈕來存取它們。</span><span class="sxs-lookup"><span data-stu-id="60d41-219">Don't put specialized or advanced properties on a General page, but you can make them accessible through a command button on the General page.</span></span>
    -   <span data-ttu-id="60d41-220">屬性不符合更明確的類別。</span><span class="sxs-lookup"><span data-stu-id="60d41-220">The properties don't fit a more specific category.</span></span> <span data-ttu-id="60d41-221">如果有的話，請改為使用該頁面的名稱。</span><span class="sxs-lookup"><span data-stu-id="60d41-221">If they do, use that name for the page instead.</span></span>

<span data-ttu-id="60d41-222">**Advanced 頁面**</span><span class="sxs-lookup"><span data-stu-id="60d41-222">**Advanced pages**</span></span>

-   <span data-ttu-id="60d41-223">**避免 [Advanced] 頁面。**</span><span class="sxs-lookup"><span data-stu-id="60d41-223">**Avoid Advanced pages.**</span></span> <span data-ttu-id="60d41-224">只有在下列情況時，才使用 Advanced 頁面：</span><span class="sxs-lookup"><span data-stu-id="60d41-224">Use an Advanced page only if:</span></span>
    -   <span data-ttu-id="60d41-225">這些屬性會套用至不常見的工作，而且主要是對 advanced 使用者有意義的。</span><span class="sxs-lookup"><span data-stu-id="60d41-225">The properties apply to uncommon tasks and are meaningful primarily to advanced users.</span></span>
    -   <span data-ttu-id="60d41-226">屬性不符合更明確的類別。</span><span class="sxs-lookup"><span data-stu-id="60d41-226">The properties don't fit a more specific category.</span></span> <span data-ttu-id="60d41-227">如果有的話，請改為使用該頁面的名稱。</span><span class="sxs-lookup"><span data-stu-id="60d41-227">If they do, use that name for the page instead.</span></span>
-   <span data-ttu-id="60d41-228">**請勿只以技術量值為基礎來呼叫 advanced 屬性。**</span><span class="sxs-lookup"><span data-stu-id="60d41-228">**Don't call properties advanced based solely on technological measures.**</span></span> <span data-ttu-id="60d41-229">例如，印表機裝訂選項可能是先進的印表機功能，但對所有使用者而言都有意義，因此不應該在 [Advanced] 頁面上。</span><span class="sxs-lookup"><span data-stu-id="60d41-229">For example, a printer stapling option may be an advanced printer feature, but it is meaningful to all users, so it shouldn't be on an Advanced page.</span></span>

### <a name="owned-property-windows"></a><span data-ttu-id="60d41-230">擁有的屬性視窗</span><span class="sxs-lookup"><span data-stu-id="60d41-230">Owned property windows</span></span>

-   <span data-ttu-id="60d41-231">**不要在屬性視窗中顯示一個以上擁有的屬性視窗。**</span><span class="sxs-lookup"><span data-stu-id="60d41-231">**Don't display more than one owned property window from a property window.**</span></span> <span data-ttu-id="60d41-232">顯示一個以上的表示 [確定] 和 [取消] 按鈕的意義很難理解。</span><span class="sxs-lookup"><span data-stu-id="60d41-232">Displaying more than one makes the meaning of the OK and Cancel buttons difficult to understand.</span></span> <span data-ttu-id="60d41-233">您可以視需要顯示其他類型的輔助對話方塊 (例如物件選擇器) 。</span><span class="sxs-lookup"><span data-stu-id="60d41-233">You can display other types of auxiliary dialog boxes (such as object pickers) as needed.</span></span>

    <span data-ttu-id="60d41-234">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="60d41-234">**Incorrect:**</span></span>

    ![<span data-ttu-id="60d41-235">三個擁有屬性視窗的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="60d41-235">screen shot of three owned property windows</span></span> ](images/win-property-win-image3.png)

    <span data-ttu-id="60d41-236">在此範例中，[擁有者選項] 對話方塊有三個層級的 [屬性] 視窗。</span><span class="sxs-lookup"><span data-stu-id="60d41-236">In this example, the owner options dialog box has three levels of owned property windows.</span></span> <span data-ttu-id="60d41-237">因此，「確定」和「取消」的意義會造成混淆。</span><span class="sxs-lookup"><span data-stu-id="60d41-237">As a result, the meanings of OK and Cancel are confusing.</span></span>

-   <span data-ttu-id="60d41-238">若為使用延遲認可模型的屬性視窗，請 **在擁有者視窗上按一下 [取消]，確定使用者可以取消在擁有的屬性視窗中所做的變更。**</span><span class="sxs-lookup"><span data-stu-id="60d41-238">For property windows that use a delayed commit model, **make sure users can cancel changes made in an owned property window by clicking Cancel on the owner window.**</span></span>
-   <span data-ttu-id="60d41-239">如果擁有的屬性視窗需要立即認可，請將主控 **視窗上的 [取消] 按鈕重新命名為 [關閉]，以表示已認可變更。**</span><span class="sxs-lookup"><span data-stu-id="60d41-239">If an owned property window requires an immediate commit, **indicate that changes were committed by renaming the Cancel button on the owner window to Close.**</span></span> <span data-ttu-id="60d41-240">如果使用者按一下 [套用]，則將按鈕還原回 [取消]。</span><span class="sxs-lookup"><span data-stu-id="60d41-240">Revert the button back to Cancel if the user clicks Apply.</span></span>

    ![<span data-ttu-id="60d41-241">具有 [確定] 和 [關閉] 之屬性視窗的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="60d41-241">screen shot of property window with ok and close</span></span> ](images/win-property-win-image4.png)

    <span data-ttu-id="60d41-242">在此範例中，無法取消自訂字典和文法設定的變更。</span><span class="sxs-lookup"><span data-stu-id="60d41-242">In this example, changes to custom dictionaries and grammar settings can't be cancelled.</span></span> <span data-ttu-id="60d41-243">您可以將 [取消] 變更為 [關閉]，為使用者提供這項意見反應。</span><span class="sxs-lookup"><span data-stu-id="60d41-243">You can give users this feedback by changing Cancel to Close.</span></span>

<span data-ttu-id="60d41-244">**其他擁有的視窗**</span><span class="sxs-lookup"><span data-stu-id="60d41-244">**Other owned windows**</span></span>

-   <span data-ttu-id="60d41-245">如果使用擁有的視窗來執行輔助工作， **請勿重新命名 [取消] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="60d41-245">If an owned window is used to perform an auxiliary task, **don't rename the Cancel button.**</span></span> <span data-ttu-id="60d41-246">上述指導方針只適用于擁有的屬性視窗，而不是用來執行輔助工作的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="60d41-246">The preceding guidelines apply only to owned property windows, not dialog boxes used to perform auxiliary tasks.</span></span>

    ![<span data-ttu-id="60d41-247">擁有者視窗和磁片清理的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="60d41-247">screen shot of owner window and disk cleanup</span></span> ](images/win-property-win-image5.png)

    <span data-ttu-id="60d41-248">在此範例中，[磁片清理] 是一項輔助工作，因此不適用先前的指導方針。</span><span class="sxs-lookup"><span data-stu-id="60d41-248">In this example, Disk Cleanup is an auxiliary task, so the previous guidelines don't apply.</span></span> <span data-ttu-id="60d41-249">例如，[擁有者] 視窗上的 [取消] 按鈕不應變更為 [關閉]。</span><span class="sxs-lookup"><span data-stu-id="60d41-249">For example, the Cancel button on the owner window shouldn't be changed to Close.</span></span>

-   <span data-ttu-id="60d41-250">如果所擁有的視窗是用來執行輔助工作，請 **不要在按下命令按鈕時關閉 [擁有者] 屬性視窗。**</span><span class="sxs-lookup"><span data-stu-id="60d41-250">If the owned window is used to perform an auxiliary task, **don't close the owner property window when the command button is clicked.**</span></span> <span data-ttu-id="60d41-251">這麼做是 disorienting，並假設使用者顯示內容視窗的唯一原因是要執行該命令。</span><span class="sxs-lookup"><span data-stu-id="60d41-251">Doing so is disorienting and assumes that the only reason the user displayed the property window was to perform that command.</span></span>

    <span data-ttu-id="60d41-252">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="60d41-252">**Incorrect:**</span></span>

    ![<span data-ttu-id="60d41-253">[選項] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="60d41-253">screen shot of options dialog box</span></span> ](images/win-property-win-image6.png)

    <span data-ttu-id="60d41-254">在此範例中，按一下 [ **保護檔** ] 會不正確地關閉 [選項] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="60d41-254">In this example, clicking **Protect document** incorrectly closes the Options dialog box.</span></span>

### <a name="tabs"></a><span data-ttu-id="60d41-255">定位點</span><span class="sxs-lookup"><span data-stu-id="60d41-255">Tabs</span></span>

-   <span data-ttu-id="60d41-256">**使用簡潔的索引標籤標籤。**</span><span class="sxs-lookup"><span data-stu-id="60d41-256">**Use concise tab labels.**</span></span> <span data-ttu-id="60d41-257">使用可清楚描述頁面內容的一或兩個字組。</span><span class="sxs-lookup"><span data-stu-id="60d41-257">Use one or two words that clearly describe the content of the page.</span></span> <span data-ttu-id="60d41-258">較長的標籤會導致螢幕空間的使用效率不佳，尤其是當標籤已當地語系化時。</span><span class="sxs-lookup"><span data-stu-id="60d41-258">Longer labels result in an inefficient use of screen space, especially when the labels are localized.</span></span>
-   <span data-ttu-id="60d41-259">**使用有意義的特定索引標籤標籤。**</span><span class="sxs-lookup"><span data-stu-id="60d41-259">**Use specific, meaningful tab labels.**</span></span> <span data-ttu-id="60d41-260">避免可套用至任何索引標籤的一般索引標籤標籤，例如 [一般]、[Advanced] 或 [設定]。</span><span class="sxs-lookup"><span data-stu-id="60d41-260">Avoid generic tab labels that could apply to any tab, such as General, Advanced, or Settings.</span></span>
-   <span data-ttu-id="60d41-261">**使用水準索引標籤的情況：**</span><span class="sxs-lookup"><span data-stu-id="60d41-261">**Use horizontal tabs if:**</span></span>
    -   <span data-ttu-id="60d41-262">屬性視窗有七個或更少的索引標籤 (包括) 的任何協力廠商延伸模組。</span><span class="sxs-lookup"><span data-stu-id="60d41-262">The property window has seven or fewer tabs (including any third-party extensions).</span></span>
    -   <span data-ttu-id="60d41-263">**所有索引標籤都能容納在一個資料列上，即使 UI 已當地語系化也一樣。**</span><span class="sxs-lookup"><span data-stu-id="60d41-263">**All the tabs fit on one row, even when the UI is localized.**</span></span>
    -   <span data-ttu-id="60d41-264">您可以在應用程式中的其他屬性視窗上使用水準索引標籤。</span><span class="sxs-lookup"><span data-stu-id="60d41-264">You use horizontal tabs on the other property windows in your application.</span></span>
-   <span data-ttu-id="60d41-265">**使用垂直索引標籤的情況：**</span><span class="sxs-lookup"><span data-stu-id="60d41-265">**Use vertical tabs if:**</span></span>

    -   <span data-ttu-id="60d41-266">屬性視窗有八個以上的索引標籤 (包括) 的任何協力廠商延伸模組。</span><span class="sxs-lookup"><span data-stu-id="60d41-266">The property window has eight or more tabs (including any third-party extensions).</span></span>
    -   <span data-ttu-id="60d41-267">**使用水準索引標籤需要一個以上的資料列。**</span><span class="sxs-lookup"><span data-stu-id="60d41-267">**Using horizontal tabs would require more than one row.**</span></span>
    -   <span data-ttu-id="60d41-268">您可以在應用程式中的其他屬性視窗上使用垂直索引標籤。</span><span class="sxs-lookup"><span data-stu-id="60d41-268">You use vertical tabs on the other property windows in your application.</span></span>

    ![<span data-ttu-id="60d41-269">具有垂直索引標籤之屬性視窗的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="60d41-269">screen shot of property window with vertical tabs</span></span> ](images/win-property-win-image7.png)

    <span data-ttu-id="60d41-270">在此範例中，垂直索引標籤可用來容納八個以上的索引標籤。</span><span class="sxs-lookup"><span data-stu-id="60d41-270">In this example, vertical tabs are used to accommodate eight or more tabs.</span></span>

-   <span data-ttu-id="60d41-271">**針對屬性偵測器，若要節省空間，請考慮使用下拉式清單（而非** 索引標籤），特別是當使用者很少變更目前的索引標籤時。</span><span class="sxs-lookup"><span data-stu-id="60d41-271">**For property inspectors, to conserve space, consider using a drop-down list instead of tabs**, especially if the current tab is rarely changed by the user.</span></span>
-   <span data-ttu-id="60d41-272">如果索引標籤 **不會套用至目前的內容，而且使用者不會預期它，請移除該** 索引標籤。這麼做可簡化 UI，使用者也不會錯過。</span><span class="sxs-lookup"><span data-stu-id="60d41-272">**If a tab doesn't apply to the current context and users don't expect it to, remove the tab.** Doing so simplifies the UI, and users won't miss it.</span></span>

    <span data-ttu-id="60d41-273">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="60d41-273">**Incorrect:**</span></span>

    ![<span data-ttu-id="60d41-274">灰色的 [檔案位置] 索引標籤的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="60d41-274">screen shot of dimmed file locations tab</span></span> ](images/win-property-win-image8.png)

    <span data-ttu-id="60d41-275">在此範例中，當 Microsoft Word 2003 當做電子郵件編輯器使用時，會不正確地停用 [檔案位置] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="60d41-275">In this example, the File Locations tab is incorrectly disabled when Microsoft Word 2003 is used as an e-mail editor.</span></span> <span data-ttu-id="60d41-276">應該移除頁面，因為使用者不會預期會在此內容中查看或變更檔案位置。</span><span class="sxs-lookup"><span data-stu-id="60d41-276">The page should be removed because users wouldn't expect to view or change file locations in this context.</span></span>

-   <span data-ttu-id="60d41-277">**如果索引標籤不適用於目前的內容，使用者可能會預期：**</span><span class="sxs-lookup"><span data-stu-id="60d41-277">**If a tab doesn't apply to the current context and users might expect it to:**</span></span>

    -   <span data-ttu-id="60d41-278">**顯示索引標籤。**</span><span class="sxs-lookup"><span data-stu-id="60d41-278">**Display the tab.**</span></span>
    -   <span data-ttu-id="60d41-279">**停用頁面上的控制項。**</span><span class="sxs-lookup"><span data-stu-id="60d41-279">**Disable the controls on the page.**</span></span>
    -   <span data-ttu-id="60d41-280">**包含說明控制項停用原因的文字。**</span><span class="sxs-lookup"><span data-stu-id="60d41-280">**Include text explaining why the controls are disabled.**</span></span>

    <span data-ttu-id="60d41-281">請勿停用此索引標籤，因為這樣做並不容易理解，且禁止探索。</span><span class="sxs-lookup"><span data-stu-id="60d41-281">Don't disable the tab because doing so isn't self-explanatory and prohibits exploration.</span></span> <span data-ttu-id="60d41-282">此外，需要特定內容的使用者才能查看所有其他索引標籤。</span><span class="sxs-lookup"><span data-stu-id="60d41-282">Furthermore, users looking for a specific property would be forced to look on all other tabs.</span></span>

    ![<span data-ttu-id="60d41-283">灰色視圖控制項的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="60d41-283">screen shot of dimmed view controls</span></span> ](images/win-property-win-image9.png)

    <span data-ttu-id="60d41-284">在此範例中，從 Word 2003 開始，任何 View 選項都不會套用在閱讀配置中。</span><span class="sxs-lookup"><span data-stu-id="60d41-284">In this example from Word 2003, none of the View options apply in Reading Layout.</span></span> <span data-ttu-id="60d41-285">不過，使用者可能會預期他們會根據索引標籤標籤來套用，因此會顯示頁面，但選項會停用。</span><span class="sxs-lookup"><span data-stu-id="60d41-285">However, users might expect them to apply based on the tab label, so the page is displayed but the options are disabled.</span></span>

-   <span data-ttu-id="60d41-286">**請勿指派變更索引標籤的效果。**</span><span class="sxs-lookup"><span data-stu-id="60d41-286">**Don't assign effects to changing tabs.**</span></span> <span data-ttu-id="60d41-287">變更目前的索引標籤絕不會有副作用、套用設定或產生錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="60d41-287">Changing the current tab should never have side effects, apply settings, or result in an error message.</span></span>
-   <span data-ttu-id="60d41-288">**請勿使用垂直索引標籤來嵌套索引標籤或合併水準索引標籤。**</span><span class="sxs-lookup"><span data-stu-id="60d41-288">**Don't nest tabs or combine horizontal tabs with vertical tabs.**</span></span> <span data-ttu-id="60d41-289">相反地，請減少索引標籤數目、僅使用垂直索引標籤，或使用另一個控制項（例如下拉式清單）。</span><span class="sxs-lookup"><span data-stu-id="60d41-289">Instead, reduce the number of tabs, use only vertical tabs, or use another control such as a drop-down list.</span></span>
-   <span data-ttu-id="60d41-290">**如果屬性視窗只有一個索引標籤，而且無法擴充，請不要使用索引標籤。**</span><span class="sxs-lookup"><span data-stu-id="60d41-290">**Don't use tabs if a property window has only a single tab and isn't extensible.**</span></span> <span data-ttu-id="60d41-291">請改用 [確定]、[取消] 和 [選擇性套用] 按鈕的一般對話方塊。</span><span class="sxs-lookup"><span data-stu-id="60d41-291">Use a regular dialog box with OK, Cancel, and an optional Apply button instead.</span></span> <span data-ttu-id="60d41-292">可由協力廠商擴充的可延伸屬性 windows () 一律需要使用索引標籤。</span><span class="sxs-lookup"><span data-stu-id="60d41-292">Extensible property windows (which can be extended by third parties) always need to use tabs.</span></span>
-   <span data-ttu-id="60d41-293">**請勿將圖示放在索引標籤上。**</span><span class="sxs-lookup"><span data-stu-id="60d41-293">**Don't put icons on tabs.**</span></span> <span data-ttu-id="60d41-294">圖示通常會加入不必要的視覺效果雜亂、取用螢幕空間，而且通常不會改善使用者理解。</span><span class="sxs-lookup"><span data-stu-id="60d41-294">Icons usually add unnecessary visual clutter, consume screen space, and often don't improve user comprehension.</span></span> <span data-ttu-id="60d41-295">只新增可協助理解的圖示，例如標準符號。</span><span class="sxs-lookup"><span data-stu-id="60d41-295">Only add icons that aid in comprehension, such as standard symbols.</span></span>

    <span data-ttu-id="60d41-296">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="60d41-296">**Incorrect:**</span></span>

    ![<span data-ttu-id="60d41-297">具有圖示之索引標籤標籤的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="60d41-297">screen shot of tab labels with icons</span></span> ](images/win-property-win-image10.png)

    <span data-ttu-id="60d41-298">在此範例中，圖形加入了不必要的視覺效果，並不太能改善使用者理解。</span><span class="sxs-lookup"><span data-stu-id="60d41-298">In this example, the graphics add unnecessary visual clutter and do little to improve user comprehension.</span></span>

-   <span data-ttu-id="60d41-299">**請勿使用標籤圖形的產品標誌。**</span><span class="sxs-lookup"><span data-stu-id="60d41-299">**Don't use product logos for tab graphics.**</span></span> <span data-ttu-id="60d41-300">索引標籤不適用於商標。</span><span class="sxs-lookup"><span data-stu-id="60d41-300">Tabs aren't for branding.</span></span>
-   <span data-ttu-id="60d41-301">**不要滾動水準索引標籤。**</span><span class="sxs-lookup"><span data-stu-id="60d41-301">**Don't scroll horizontal tabs.**</span></span> <span data-ttu-id="60d41-302">無法立即探索水準滾動。</span><span class="sxs-lookup"><span data-stu-id="60d41-302">Horizontal scrolling isn't readily discoverable.</span></span> <span data-ttu-id="60d41-303">不過，您可以滾動垂直索引標籤。</span><span class="sxs-lookup"><span data-stu-id="60d41-303">You may scroll vertical tabs, however.</span></span>

    <span data-ttu-id="60d41-304">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="60d41-304">**Incorrect:**</span></span>

    ![<span data-ttu-id="60d41-305">截斷的水準索引標籤標籤的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="60d41-305">screen shot of truncated horizontal tab label</span></span> ](images/win-property-win-image11.png)

    <span data-ttu-id="60d41-306">在此範例中，會滾動水準索引標籤。</span><span class="sxs-lookup"><span data-stu-id="60d41-306">In this example, the horizontal tabs are scrolled.</span></span>

### <a name="command-buttons"></a><span data-ttu-id="60d41-307">命令按鈕</span><span class="sxs-lookup"><span data-stu-id="60d41-307">Command buttons</span></span>

-   <span data-ttu-id="60d41-308">**放置套用至屬性視窗底部所有屬性頁的命令按鈕。**</span><span class="sxs-lookup"><span data-stu-id="60d41-308">**Place command buttons that apply to all property pages at the bottom of the property window.**</span></span> <span data-ttu-id="60d41-309">將按鈕靠右對齊，並使用此順序 (從左至右) ： [確定]、[取消] 和 [套用]。</span><span class="sxs-lookup"><span data-stu-id="60d41-309">Right-align the buttons and use this order (from left to right): OK, Cancel, and Apply.</span></span>
-   <span data-ttu-id="60d41-310">**只將命令按鈕放在屬性頁上，直接套用至個別的屬性頁。**</span><span class="sxs-lookup"><span data-stu-id="60d41-310">**Place command buttons that apply only to individual property pages directly on the property page.**</span></span>

### <a name="commit-buttons"></a><span data-ttu-id="60d41-311">認可按鈕</span><span class="sxs-lookup"><span data-stu-id="60d41-311">Commit buttons</span></span>

<span data-ttu-id="60d41-312">**確定按鈕**</span><span class="sxs-lookup"><span data-stu-id="60d41-312">**OK buttons**</span></span>

-   <span data-ttu-id="60d41-313">**若為 [擁有者] 屬性視窗，[確定] 按鈕表示套用自視窗開啟或上次套用) 之後 (的暫止變更，然後關閉視窗。**</span><span class="sxs-lookup"><span data-stu-id="60d41-313">**For owner property windows, the OK button means apply the pending changes (made since the window was opened or the last Apply), and close the window.**</span></span>
-   <span data-ttu-id="60d41-314">**針對擁有的屬性視窗，[確定] 按鈕表示保留變更、關閉視窗，並在套用主控視窗的變更時套用變更。**</span><span class="sxs-lookup"><span data-stu-id="60d41-314">**For owned property windows, the OK button means keep the changes, close the window, and apply the changes when the owner window's changes are applied.**</span></span>
-   <span data-ttu-id="60d41-315">**請勿重新命名 [確定] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="60d41-315">**Don't rename the OK button.**</span></span> <span data-ttu-id="60d41-316">不同于其他對話方塊，屬性視窗不會用來執行任何一項特定工作。</span><span class="sxs-lookup"><span data-stu-id="60d41-316">Unlike other dialog boxes, property windows aren't used to perform any one specific task.</span></span> <span data-ttu-id="60d41-317">如果重新命名 [確定] (按鈕（例如) ）是合理的，則視窗不是屬性視窗。</span><span class="sxs-lookup"><span data-stu-id="60d41-317">If it makes sense to rename the OK button (to Print, for example), the window isn't a property window.</span></span>
-   <span data-ttu-id="60d41-318">**請勿指派存取金鑰。**</span><span class="sxs-lookup"><span data-stu-id="60d41-318">**Don't assign an access key.**</span></span>

<span data-ttu-id="60d41-319">**取消按鈕**</span><span class="sxs-lookup"><span data-stu-id="60d41-319">**Cancel buttons**</span></span>

-   <span data-ttu-id="60d41-320">**[取消] 按鈕表示捨棄自從開啟視窗或上次套用) 之後 (所做的所有暫止變更，然後關閉視窗。**</span><span class="sxs-lookup"><span data-stu-id="60d41-320">**The Cancel button means discard all pending changes (made since the window was opened or the last Apply), and close the window.**</span></span>
-   <span data-ttu-id="60d41-321">**如果無法放棄所有暫止的變更，請重新命名 [取消] 按鈕以關閉。**</span><span class="sxs-lookup"><span data-stu-id="60d41-321">**If all pending changes can't be abandoned, rename the Cancel button to Close.**</span></span> <span data-ttu-id="60d41-322">按一下 [取消] 必須放棄所有暫止的變更。</span><span class="sxs-lookup"><span data-stu-id="60d41-322">Clicking Cancel must abandon all pending changes.</span></span>
-   <span data-ttu-id="60d41-323">**如果 [擁有的屬性] 視窗需要立即認可，請將擁有者視窗上的 [取消] 按鈕重新命名為關閉，以顯示已認可的變更。**</span><span class="sxs-lookup"><span data-stu-id="60d41-323">**If the owned property window requires an immediate commit, rename the Cancel button on the owner window to Close to show that changes were committed.**</span></span>
-   <span data-ttu-id="60d41-324">**請勿指派存取金鑰。**</span><span class="sxs-lookup"><span data-stu-id="60d41-324">**Don't assign an access key.**</span></span>

<span data-ttu-id="60d41-325">**套用按鈕**</span><span class="sxs-lookup"><span data-stu-id="60d41-325">**Apply buttons**</span></span>

-   <span data-ttu-id="60d41-326">**在 [擁有者] 屬性工作表中，[套用] 按鈕表示套用自視窗開啟後 (所做的暫止變更，或上次套用) ，但讓視窗保持開啟狀態。**</span><span class="sxs-lookup"><span data-stu-id="60d41-326">**For owner property sheets, the Apply button means apply the pending changes (made since the window was opened or the last Apply), but leave the window open.**</span></span> <span data-ttu-id="60d41-327">這麼做可讓使用者在關閉屬性工作表之前評估變更。</span><span class="sxs-lookup"><span data-stu-id="60d41-327">Doing so allows users to evaluate the changes before closing the property sheet.</span></span>
-   <span data-ttu-id="60d41-328">**若為擁有的屬性工作表，請不要使用。**</span><span class="sxs-lookup"><span data-stu-id="60d41-328">**For owned property sheets, don't use.**</span></span> <span data-ttu-id="60d41-329">使用所擁有屬性工作表上的 [套用] 按鈕，可讓 [擁有者] 屬性工作表上的 [認可] 按鈕的意義難以理解。</span><span class="sxs-lookup"><span data-stu-id="60d41-329">Using an Apply button on an owned property sheet makes the meaning of the commit buttons on the owner property sheet difficult to understand.</span></span>
-   <span data-ttu-id="60d41-330">**只有當屬性工作表的設定 (至少一個) 具有使用者可透過有意義的方式評估的效果時，才提供 [套用] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="60d41-330">**Provide an Apply button only if the property sheet has settings (at least one) with effects that users can evaluate in a meaningful way.**</span></span> <span data-ttu-id="60d41-331">一般情況下，[套用] 按鈕會在設定進行可見變更時使用。</span><span class="sxs-lookup"><span data-stu-id="60d41-331">Typically, Apply buttons are used when settings make visible changes.</span></span> <span data-ttu-id="60d41-332">使用者應該能夠套用變更、評估變更，然後根據該評估進行進一步的變更。</span><span class="sxs-lookup"><span data-stu-id="60d41-332">Users should be able to apply a change, evaluate the change, and make further changes based on that evaluation.</span></span> <span data-ttu-id="60d41-333">如果沒有，請移除 [套用] 按鈕，而不要停用它。</span><span class="sxs-lookup"><span data-stu-id="60d41-333">If not, remove the Apply button instead of disabling it.</span></span>

    <span data-ttu-id="60d41-334">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="60d41-334">**Incorrect:**</span></span>

    ![<span data-ttu-id="60d41-335">具有 [套用] 按鈕之系統屬性的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="60d41-335">screen shot of system properties with apply button</span></span> ](images/win-property-win-image12.png)

    <span data-ttu-id="60d41-336">在此範例中，沒有任何系統屬性具有視覺效果，因此 [套用] 按鈕沒有任何值，而且應該移除。</span><span class="sxs-lookup"><span data-stu-id="60d41-336">In this example, none of the system properties have a visual effect, so the Apply button has no value and should be removed.</span></span>

-   <span data-ttu-id="60d41-337">**放置使用者可能想要在擁有者頁面上套用的所有設定。**</span><span class="sxs-lookup"><span data-stu-id="60d41-337">**Place all settings that users may want to apply on owner pages.**</span></span> <span data-ttu-id="60d41-338">不要在擁有的屬性工作表上使用 [套用] 按鈕，因為這樣做會造成混淆。</span><span class="sxs-lookup"><span data-stu-id="60d41-338">Don't use Apply buttons on owned property sheets, because doing so is confusing.</span></span>
-   <span data-ttu-id="60d41-339">**只使用 [套用] 按鈕與 [屬性工作表]，而非 [選項] 對話方塊。**</span><span class="sxs-lookup"><span data-stu-id="60d41-339">**Use Apply buttons only with property sheets, not with options dialog boxes.**</span></span>
-   <span data-ttu-id="60d41-340">**只有在有暫止的變更時，才啟用 [** 套用] 按鈕;否則，請將它停用。</span><span class="sxs-lookup"><span data-stu-id="60d41-340">**Enable the Apply button only when there are pending changes**; otherwise, disable it.</span></span>
-   <span data-ttu-id="60d41-341">**指派 "A" 作為存取金鑰。**</span><span class="sxs-lookup"><span data-stu-id="60d41-341">**Assign "A" as the access key.**</span></span>

<span data-ttu-id="60d41-342">**關閉按鈕**</span><span class="sxs-lookup"><span data-stu-id="60d41-342">**Close buttons**</span></span>

-   <span data-ttu-id="60d41-343">**如果無法放棄所有暫止的變更，請重新命名 [取消] 按鈕以關閉。**</span><span class="sxs-lookup"><span data-stu-id="60d41-343">**If all pending changes can't be abandoned, rename the Cancel button to Close.**</span></span> <span data-ttu-id="60d41-344">按一下 [取消] 必須放棄所有暫止的變更。</span><span class="sxs-lookup"><span data-stu-id="60d41-344">Clicking Cancel must abandon all pending changes.</span></span>
-   <span data-ttu-id="60d41-345">**請勿確認使用者是否捨棄其變更。**</span><span class="sxs-lookup"><span data-stu-id="60d41-345">**Don't confirm if users discard their changes.**</span></span>
    -   <span data-ttu-id="60d41-346">**例外狀況：** 如果 [屬性] 視窗有需要大量設定的設定，而且使用者已進行變更，您可能會在使用者按一下標題列上的 [關閉] 按鈕時顯示 [確認](mess-confirm.md) 。</span><span class="sxs-lookup"><span data-stu-id="60d41-346">**Exception:** If the property window has settings that require significant effort to set and the user has made changes, you may display a [confirmation](mess-confirm.md) if the user clicks the Close button on the title bar.</span></span> <span data-ttu-id="60d41-347">原因是某些使用者誤以為標題列上的 [關閉] 按鈕與 [確定] 按鈕的效果相同。</span><span class="sxs-lookup"><span data-stu-id="60d41-347">The reason is that some users mistakenly assume that the Close button on the title bar has the same effect as the OK button.</span></span>
-   <span data-ttu-id="60d41-348">**除了確認訊息以外，請確定標題列上的 [關閉] 按鈕與 [取消] 或 [關閉] 具有相同的效果。**</span><span class="sxs-lookup"><span data-stu-id="60d41-348">**With the exception of the confirmation message, make sure the Close button on the title bar has the same effect as Cancel or Close.**</span></span>

### <a name="page-contents"></a><span data-ttu-id="60d41-349">頁面內容</span><span class="sxs-lookup"><span data-stu-id="60d41-349">Page contents</span></span>

-   <span data-ttu-id="60d41-350">**請確定屬性是必要的。**</span><span class="sxs-lookup"><span data-stu-id="60d41-350">**Make sure the properties are necessary.**</span></span> <span data-ttu-id="60d41-351">不要讓您的頁面具有不必要的屬性，就可以避免進行硬性的設計決策。</span><span class="sxs-lookup"><span data-stu-id="60d41-351">Don't clutter your pages with unnecessary properties just to avoid making hard design decisions.</span></span>
-   <span data-ttu-id="60d41-352">**以使用者目標為依據，而不是以技術呈現屬性。**</span><span class="sxs-lookup"><span data-stu-id="60d41-352">**Present properties in terms of user goals, not technology.**</span></span> <span data-ttu-id="60d41-353">因為屬性會設定特定的技術，並不表示您必須根據該技術來呈現該屬性。</span><span class="sxs-lookup"><span data-stu-id="60d41-353">Just because a property configures a specific technology doesn't mean that you must present the property in terms of that technology.</span></span>
    -   <span data-ttu-id="60d41-354">如果您必須以技術來呈現設定 (可能是因為您的使用者辨識技術的名稱) ，請提供使用者如何從該設定獲益的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="60d41-354">If you must present settings in terms of technology (perhaps because your users recognize the technology's name), include a brief description of how the user benefits from that setting.</span></span>
-   <span data-ttu-id="60d41-355">**將屬性顯示在正確層級。**</span><span class="sxs-lookup"><span data-stu-id="60d41-355">**Present properties at the right level.**</span></span> <span data-ttu-id="60d41-356">您不需要在屬性頁上顯示個別的低層級設定，因此可讓您的使用者有意義的層級上提供屬性。</span><span class="sxs-lookup"><span data-stu-id="60d41-356">You don't need to present individual, low-level settings on a property page, so present the properties at a level that makes sense to your users.</span></span>
-   <span data-ttu-id="60d41-357">**針對特定工作設計屬性頁。**</span><span class="sxs-lookup"><span data-stu-id="60d41-357">**Design property pages for specific tasks.**</span></span> <span data-ttu-id="60d41-358">判斷使用者將執行的工作，並確定有明確的路徑可以執行這些工作。</span><span class="sxs-lookup"><span data-stu-id="60d41-358">Determine the tasks that users will perform, and make sure there is a clear path to perform those tasks.</span></span>
-   <span data-ttu-id="60d41-359">藉由減少索引標籤數目、決定根據邏輯分組和連貫性的頁面，以及簡化頁面的簡報，來 **有效率地整理屬性頁**。</span><span class="sxs-lookup"><span data-stu-id="60d41-359">**Organize property pages efficiently** by reducing the number of tabs, deciding what goes on a page based on logical grouping and coherence, and simplifying the page's presentation.</span></span>

<!-- -->

-   <span data-ttu-id="60d41-360">**如果強烈建議選項，請考慮將「 (建議的) 」新增至標籤。**</span><span class="sxs-lookup"><span data-stu-id="60d41-360">**If an option is strongly recommended, consider adding "(recommended)" to the label.**</span></span>
-   <span data-ttu-id="60d41-361">**當下列情況時，提供屬性頁或整個屬性視窗的 [還原預設值] 命令按鈕：**</span><span class="sxs-lookup"><span data-stu-id="60d41-361">**Provide a Restore Defaults command button for a property page or the entire property window when:**</span></span>

    -   <span data-ttu-id="60d41-362">您的使用者可能會考慮複雜且難以理解的設定。</span><span class="sxs-lookup"><span data-stu-id="60d41-362">Your users are likely to consider the settings complex and difficult to understand.</span></span>
    -   <span data-ttu-id="60d41-363">如果設定不正確，可能會造成中斷的功能，但預設值可能會還原功能。</span><span class="sxs-lookup"><span data-stu-id="60d41-363">Having incorrect settings may result in breaking functionality, but the defaults might restore functionality.</span></span>
    -   <span data-ttu-id="60d41-364">當物件設定錯誤時，使用者可以更輕鬆地開始。</span><span class="sxs-lookup"><span data-stu-id="60d41-364">It's easier for users to start over when the object is misconfigured.</span></span>

    ![<span data-ttu-id="60d41-365">[還原預設值] 按鈕索引標籤的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="60d41-365">screen shot of tab with restore defaults button</span></span> ](images/win-property-win-image13.png)

    <span data-ttu-id="60d41-366">在此範例中，Windows 防火牆設定很複雜，而且可能會導致功能中斷。</span><span class="sxs-lookup"><span data-stu-id="60d41-366">In this example, the Windows Firewall settings are complex and may result in broken functionality.</span></span> <span data-ttu-id="60d41-367">如果發生問題，使用者通常可以藉由按一下 [還原預設值] 來重新開始。</span><span class="sxs-lookup"><span data-stu-id="60d41-367">If there's a problem, it is often easier for users to start over by clicking Restore Defaults.</span></span>

-   <span data-ttu-id="60d41-368">如果其效果不明顯或設定很複雜，請確認 [還原預設值] 命令。</span><span class="sxs-lookup"><span data-stu-id="60d41-368">Confirm the Restore Defaults command if its effect isn't obvious or the settings are complex.</span></span> <span data-ttu-id="60d41-369">使用 [省略號](ctrl-command-buttons.md)表示確認。</span><span class="sxs-lookup"><span data-stu-id="60d41-369">Indicate the confirmation by using [ellipses](ctrl-command-buttons.md).</span></span>
-   <span data-ttu-id="60d41-370">**適當時，顯示設定結果的預覽。**</span><span class="sxs-lookup"><span data-stu-id="60d41-370">**When appropriate, display a preview of the results of a setting.**</span></span>

    ![<span data-ttu-id="60d41-371">滑鼠屬性指標範例的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="60d41-371">screen shot of mouse properties pointer examples</span></span> ](images/win-property-win-image14.png)

    <span data-ttu-id="60d41-372">在此範例中，頁面會顯示指標配置的預覽。</span><span class="sxs-lookup"><span data-stu-id="60d41-372">In this example, the page displays a preview of the pointer schemes.</span></span> <span data-ttu-id="60d41-373">按一下 [套用] 也會顯示預覽，在頁面上有預覽功能對使用者而言更有效率。</span><span class="sxs-lookup"><span data-stu-id="60d41-373">While clicking Apply also shows a preview, having a preview on the page is more efficient for users.</span></span>

    ![<span data-ttu-id="60d41-374">字型設定結果預覽的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="60d41-374">screen shot of preview of results of font settings</span></span> ](images/win-property-win-image15.png)

    <span data-ttu-id="60d41-375">在此範例中，[預覽] 方塊會顯示字型設定的結果。</span><span class="sxs-lookup"><span data-stu-id="60d41-375">In this example, the Preview box shows the results of the font settings.</span></span> <span data-ttu-id="60d41-376">此範例顯示您可以預覽非圖形化的設定。</span><span class="sxs-lookup"><span data-stu-id="60d41-376">This example shows that you can preview settings that aren't graphical.</span></span>

### <a name="help"></a><span data-ttu-id="60d41-377">Help</span><span class="sxs-lookup"><span data-stu-id="60d41-377">Help</span></span>

-   <span data-ttu-id="60d41-378">提供使用者協助時， **請考慮使用下列選項** (依照其喜好設定) 順序列出：</span><span class="sxs-lookup"><span data-stu-id="60d41-378">When providing user assistance, **consider using the following options** (listed in their order of preference):</span></span>
    -   <span data-ttu-id="60d41-379">提供互動式控制項自理解標籤。</span><span class="sxs-lookup"><span data-stu-id="60d41-379">Give interactive controls self-explanatory labels.</span></span> <span data-ttu-id="60d41-380">使用者比較有可能讀取互動式控制項上的標籤，而不是任何其他文字。</span><span class="sxs-lookup"><span data-stu-id="60d41-380">Users are more likely to read the labels on interactive controls than any other text.</span></span>
    -   <span data-ttu-id="60d41-381">使用靜態文字標籤提供內容中的說明。</span><span class="sxs-lookup"><span data-stu-id="60d41-381">Provide in-context explanations using static text labels.</span></span>
    -   <span data-ttu-id="60d41-382">提供相關說明主題的特定 [連結](ctrl-links.md) 。</span><span class="sxs-lookup"><span data-stu-id="60d41-382">Provide a specific [link](ctrl-links.md) to a relevant Help topic.</span></span>
-   <span data-ttu-id="60d41-383">**找出每個頁面底部的 [說明] 連結。**</span><span class="sxs-lookup"><span data-stu-id="60d41-383">**Locate Help links at the bottom of each page.**</span></span> <span data-ttu-id="60d41-384">如果某個頁面有幾個不同的設定群組，其中有說明主題 (可能在群組方塊) 內，請找出群組底部的 [說明] 連結。</span><span class="sxs-lookup"><span data-stu-id="60d41-384">If a page has several distinct groups of settings that have a Help topic (perhaps within group boxes), locate the Help link at the bottom of the group.</span></span>
-   <span data-ttu-id="60d41-385">**請勿使用一般或模糊的說明主題連結或一般説明按鈕。**</span><span class="sxs-lookup"><span data-stu-id="60d41-385">**Don't use general or vague Help topic links or generic Help buttons.**</span></span> <span data-ttu-id="60d41-386">使用者通常會忽略一般說明。</span><span class="sxs-lookup"><span data-stu-id="60d41-386">Users often ignore generic Help.</span></span>

<span data-ttu-id="60d41-387">如需詳細資訊和範例， [請參閱說明](winenv-help.md)。</span><span class="sxs-lookup"><span data-stu-id="60d41-387">For more information and examples, see [Help](winenv-help.md).</span></span>

### <a name="standard-users-and-protected-administrators"></a><span data-ttu-id="60d41-388">標準使用者和受保護的系統管理員</span><span class="sxs-lookup"><span data-stu-id="60d41-388">Standard users and Protected administrators</span></span>

<span data-ttu-id="60d41-389">**許多設定都需要系統管理員許可權才能變更。**</span><span class="sxs-lookup"><span data-stu-id="60d41-389">**Many settings require administrator privileges to change.**</span></span> <span data-ttu-id="60d41-390">如果進程需要系統管理員許可權，Windows 和更新版本需要 [標準使用者](glossary.md) 和 [受保護](glossary.md) 的系統管理員明確地提升其許可權。</span><span class="sxs-lookup"><span data-stu-id="60d41-390">If a process requires administrator privileges, Windows and later requires [Standard users](glossary.md) and [Protected administrators](glossary.md) to elevate their privileges explicitly.</span></span> <span data-ttu-id="60d41-391">這樣做有助於防止惡意程式碼以系統管理員許可權執行。</span><span class="sxs-lookup"><span data-stu-id="60d41-391">Doing so helps prevent malicious code from running with administrator privileges.</span></span>

<span data-ttu-id="60d41-392">如需詳細資訊和範例，請參閱 [使用者帳戶控制](winenv-uac.md)。</span><span class="sxs-lookup"><span data-stu-id="60d41-392">For more information and examples, see [User Account Control](winenv-uac.md).</span></span>

### <a name="default-values"></a><span data-ttu-id="60d41-393">預設值</span><span class="sxs-lookup"><span data-stu-id="60d41-393">Default values</span></span>

-   <span data-ttu-id="60d41-394">**屬性視窗內的設定必須反映應用程式、物件或物件集合的目前狀態。**</span><span class="sxs-lookup"><span data-stu-id="60d41-394">**The settings within a property window must reflect the current state of the application, object, or collection of objects.**</span></span> <span data-ttu-id="60d41-395">否則會產生誤導，可能會導致不想要的結果。</span><span class="sxs-lookup"><span data-stu-id="60d41-395">Doing otherwise would be misleading and possibly lead to undesired results.</span></span> <span data-ttu-id="60d41-396">例如，如果設定反映出建議，而不是目前的狀態，則使用者可能會按一下 [取消]，而不是進行變更，以為不需要任何變更。</span><span class="sxs-lookup"><span data-stu-id="60d41-396">For example, if the settings reflect the recommendations but not the current state, users might click Cancel instead of making changes, thinking that no changes are needed.</span></span>
-   <span data-ttu-id="60d41-397">**選擇最安全的 (，以防止資料遺失或系統存取) 和最安全的初始狀態。**</span><span class="sxs-lookup"><span data-stu-id="60d41-397">**Choose the safest (to prevent loss of data or system access) and most secure initial state.**</span></span> <span data-ttu-id="60d41-398">假設大部分的使用者不會變更設定。</span><span class="sxs-lookup"><span data-stu-id="60d41-398">Assume that most users won't change the settings.</span></span>
-   <span data-ttu-id="60d41-399">**如果安全性和安全性不是因素，請選擇最有可能或方便的初始狀態。**</span><span class="sxs-lookup"><span data-stu-id="60d41-399">**If safety and security aren't factors, choose the initial state that is most likely or convenient.**</span></span>

## <a name="text"></a><span data-ttu-id="60d41-400">Text</span><span class="sxs-lookup"><span data-stu-id="60d41-400">Text</span></span>

### <a name="commands"></a><span data-ttu-id="60d41-401">命令</span><span class="sxs-lookup"><span data-stu-id="60d41-401">Commands</span></span>

-   <span data-ttu-id="60d41-402">若要顯示程式選項，請使用 [選項]。</span><span class="sxs-lookup"><span data-stu-id="60d41-402">To display program options, use "Options."</span></span>
-   <span data-ttu-id="60d41-403">若要顯示物件的屬性視窗，請使用「屬性」。</span><span class="sxs-lookup"><span data-stu-id="60d41-403">To display an object's property window, use "Properties."</span></span>
-   <span data-ttu-id="60d41-404">若要顯示常用程式自訂設定的摘要，請使用「[個人](glossary.md)化」。</span><span class="sxs-lookup"><span data-stu-id="60d41-404">To display a summary of the commonly used program customization settings, use "[Personalize](glossary.md)."</span></span>
-   <span data-ttu-id="60d41-405">請勿使用「設定」或「喜好設定」。</span><span class="sxs-lookup"><span data-stu-id="60d41-405">Don't use "Settings" or "Preferences."</span></span>
-   <span data-ttu-id="60d41-406">請勿將 [省略號](ctrl-command-buttons.md) 用於這些命令。</span><span class="sxs-lookup"><span data-stu-id="60d41-406">Don't use [ellipses](ctrl-command-buttons.md) for these commands.</span></span>

### <a name="property-sheet-titles"></a><span data-ttu-id="60d41-407">屬性工作表標題</span><span class="sxs-lookup"><span data-stu-id="60d41-407">Property sheet titles</span></span>

-   <span data-ttu-id="60d41-408">若為單一物件，請使用「 \[ 物件名稱 \] 屬性」。</span><span class="sxs-lookup"><span data-stu-id="60d41-408">For a single object, use "\[object name\] Properties."</span></span>
    -   <span data-ttu-id="60d41-409">如果物件沒有名稱，請使用物件的類型名稱。</span><span class="sxs-lookup"><span data-stu-id="60d41-409">If the object has no name, use the object's type name.</span></span> <span data-ttu-id="60d41-410"> (例如使用者帳戶屬性。 ) </span><span class="sxs-lookup"><span data-stu-id="60d41-410">(For example, User Account Properties.)</span></span>
-   <span data-ttu-id="60d41-411">針對多個物件，請使用「 \[ 第一個物件名稱 \] ，.。。屬性。」</span><span class="sxs-lookup"><span data-stu-id="60d41-411">For multiple objects, use "\[first object name\], ... Properties."</span></span>
    -   <span data-ttu-id="60d41-412">如果物件沒有名稱，請使用物件的類型名稱。</span><span class="sxs-lookup"><span data-stu-id="60d41-412">If the objects have no names, use the objects' type name.</span></span> <span data-ttu-id="60d41-413">例如， (使用者帳戶屬性。 ) </span><span class="sxs-lookup"><span data-stu-id="60d41-413">(For example, User Accounts Properties.)</span></span>
    -   <span data-ttu-id="60d41-414">如果物件有不同的類型，請使用「選取屬性」。</span><span class="sxs-lookup"><span data-stu-id="60d41-414">If the objects have different types, use "Selection Properties."</span></span>
-   <span data-ttu-id="60d41-415">使用 [標題樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="60d41-415">Use [title-style capitalization](glossary.md).</span></span>
-   <span data-ttu-id="60d41-416">請勿使用結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="60d41-416">Don't use ending punctuation.</span></span>
-   <span data-ttu-id="60d41-417">請勿使用連字號，例如「 \[ 物件名稱 \] -屬性」。</span><span class="sxs-lookup"><span data-stu-id="60d41-417">Don't use hyphens, such as "\[object name\] - Properties."</span></span>

### <a name="property-inspector-titles"></a><span data-ttu-id="60d41-418">屬性偵測器標題</span><span class="sxs-lookup"><span data-stu-id="60d41-418">Property inspector titles</span></span>

-   <span data-ttu-id="60d41-419">使用「屬性」。</span><span class="sxs-lookup"><span data-stu-id="60d41-419">Use "Properties."</span></span>
-   <span data-ttu-id="60d41-420">使用標題樣式的大小寫。</span><span class="sxs-lookup"><span data-stu-id="60d41-420">Use title-style capitalization.</span></span>
-   <span data-ttu-id="60d41-421">請勿使用結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="60d41-421">Don't use ending punctuation.</span></span>

### <a name="options-dialog-box-titles"></a><span data-ttu-id="60d41-422">選項對話方塊標題</span><span class="sxs-lookup"><span data-stu-id="60d41-422">Options dialog box titles</span></span>

-   <span data-ttu-id="60d41-423">使用 [選項]。</span><span class="sxs-lookup"><span data-stu-id="60d41-423">Use "Options."</span></span>
-   <span data-ttu-id="60d41-424">使用標題樣式的大小寫。</span><span class="sxs-lookup"><span data-stu-id="60d41-424">Use title-style capitalization.</span></span>
-   <span data-ttu-id="60d41-425">請勿使用結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="60d41-425">Don't use ending punctuation.</span></span>

### <a name="property-page-tab-names"></a><span data-ttu-id="60d41-426">屬性頁索引標籤名稱</span><span class="sxs-lookup"><span data-stu-id="60d41-426">Property page tab names</span></span>

-   <span data-ttu-id="60d41-427">**使用簡潔的索引標籤標籤。**</span><span class="sxs-lookup"><span data-stu-id="60d41-427">**Use concise tab labels.**</span></span> <span data-ttu-id="60d41-428">使用可清楚描述頁面內容的一或兩個字組。</span><span class="sxs-lookup"><span data-stu-id="60d41-428">Use one or two words that clearly describe the content of the page.</span></span> <span data-ttu-id="60d41-429">使用較長的索引標籤名稱會導致螢幕空間的使用效率不佳，尤其是在已當地語系化索引標籤名稱的情況下。</span><span class="sxs-lookup"><span data-stu-id="60d41-429">Using longer tab names results in an inefficient use of screen space, especially when the tab names are localized.</span></span>
-   <span data-ttu-id="60d41-430">**使用有意義的特定索引標籤標籤。**</span><span class="sxs-lookup"><span data-stu-id="60d41-430">**Use specific, meaningful tab labels.**</span></span> <span data-ttu-id="60d41-431">避免可套用至任何索引標籤的一般索引標籤標籤，例如 [一般]、[Advanced] 或 [設定]。</span><span class="sxs-lookup"><span data-stu-id="60d41-431">Avoid generic tab labels that could apply to any tab, such as General, Advanced, or Settings.</span></span>
-   <span data-ttu-id="60d41-432">將標籤寫入為一或兩個單字的片語，且不使用結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="60d41-432">Write the label as a one- or two-word phrase and use no ending punctuation.</span></span>
-   <span data-ttu-id="60d41-433">使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="60d41-433">Use [sentence-style capitalization](glossary.md).</span></span>
-   <span data-ttu-id="60d41-434">請勿指派唯一的 [存取金鑰](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="60d41-434">Don't assign a unique [access key](glossary.md).</span></span>

### <a name="property-page-text"></a><span data-ttu-id="60d41-435">屬性頁文字</span><span class="sxs-lookup"><span data-stu-id="60d41-435">Property page text</span></span>

-   <span data-ttu-id="60d41-436">避免大型文字區塊。</span><span class="sxs-lookup"><span data-stu-id="60d41-436">Avoid large blocks of text.</span></span>
-   <span data-ttu-id="60d41-437">為文字提供足夠的空間，以在其當地語系化時將其擴充30%。</span><span class="sxs-lookup"><span data-stu-id="60d41-437">Provide enough room for the text to expand 30 percent if it will be localized.</span></span>
-   <span data-ttu-id="60d41-438">請勿使用文字片語作為屬性視窗上的命令。</span><span class="sxs-lookup"><span data-stu-id="60d41-438">Don't use text phrased as a command on property windows.</span></span> <span data-ttu-id="60d41-439">由於使用者可能只想要查看設定，因此您不會想要提示他們變更設定。</span><span class="sxs-lookup"><span data-stu-id="60d41-439">Because users might want to simply view settings, you don't want to prompt them to change settings.</span></span>
-   <span data-ttu-id="60d41-440">使用句子樣式的大小寫和結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="60d41-440">Use sentence-style capitalization and ending punctuation.</span></span>

## <a name="documentation"></a><span data-ttu-id="60d41-441">文件</span><span class="sxs-lookup"><span data-stu-id="60d41-441">Documentation</span></span>

<span data-ttu-id="60d41-442">參考屬性視窗時：</span><span class="sxs-lookup"><span data-stu-id="60d41-442">When referring to property windows:</span></span>

-   <span data-ttu-id="60d41-443">在程式設計和其他技術檔中，請將 [屬性工作表] 和 [選項] 對話方塊稱為屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="60d41-443">In programming and other technical documentation, refer to property sheets and options dialog boxes as property sheets.</span></span> <span data-ttu-id="60d41-444">在其他地方使用對話方塊，尤其是在使用者檔中。</span><span class="sxs-lookup"><span data-stu-id="60d41-444">Everywhere else, use dialog box, especially in user documentation.</span></span>
-   <span data-ttu-id="60d41-445">使用確切的標題文字，包括其大小寫。</span><span class="sxs-lookup"><span data-stu-id="60d41-445">Use the exact title text, including its capitalization.</span></span>
-   <span data-ttu-id="60d41-446">若要描述使用者互動，請使用 [開啟] 和 [關閉]。</span><span class="sxs-lookup"><span data-stu-id="60d41-446">To describe user interaction, use open and close.</span></span>
-   <span data-ttu-id="60d41-447">可能的話，請使用粗體文字來格式化標題。</span><span class="sxs-lookup"><span data-stu-id="60d41-447">When possible, format the title using bold text.</span></span> <span data-ttu-id="60d41-448">否則，請只在必要時才將標題放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="60d41-448">Otherwise, put the title in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="60d41-449">參考屬性頁時：</span><span class="sxs-lookup"><span data-stu-id="60d41-449">When referring to property pages:</span></span>

-   <span data-ttu-id="60d41-450">在程式設計和其他技術檔中，請將屬性頁稱為屬性頁。</span><span class="sxs-lookup"><span data-stu-id="60d41-450">In programming and other technical documentation, refer to property pages as property pages.</span></span> <span data-ttu-id="60d41-451">在其他地方，使用 tab 鍵，尤其是在使用者檔中。</span><span class="sxs-lookup"><span data-stu-id="60d41-451">Everywhere else, use tab, especially in user documentation.</span></span>
-   <span data-ttu-id="60d41-452">使用確切的標題文字，包括其大小寫。</span><span class="sxs-lookup"><span data-stu-id="60d41-452">Use the exact title text, including its capitalization.</span></span>
-   <span data-ttu-id="60d41-453">若要描述使用者互動，請使用按一下滑鼠右鍵，以參考按一下索引標籤。</span><span class="sxs-lookup"><span data-stu-id="60d41-453">To describe user interaction, use click to refer to clicking a tab.</span></span>
-   <span data-ttu-id="60d41-454">可能的話，請使用粗體文字來格式化名稱。</span><span class="sxs-lookup"><span data-stu-id="60d41-454">When possible, format the name using bold text.</span></span> <span data-ttu-id="60d41-455">否則，請只在必要時才將名稱放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="60d41-455">Otherwise, put the name in quotation marks only if required to prevent confusion.</span></span>

 

 