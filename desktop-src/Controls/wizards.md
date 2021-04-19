---
title: 如何建立嚮導
description: Wizard 是一種屬性工作表，可提供簡單且強大的方式來引導使用者完成程式。
ms.assetid: f8def159-0a68-4d7f-9840-c7b6b906ed08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fedd35bd0454e0d78ddbe74d832543e58d0a8fc7
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2021
ms.locfileid: "106986137"
---
# <a name="how-to-create-wizards"></a><span data-ttu-id="9f211-103">如何建立嚮導</span><span class="sxs-lookup"><span data-stu-id="9f211-103">How to Create Wizards</span></span>

<span data-ttu-id="9f211-104">Wizard 是一種屬性工作表，可提供簡單且強大的方式來引導使用者完成程式。</span><span class="sxs-lookup"><span data-stu-id="9f211-104">A wizard is a type of property sheet that provides a simple and powerful way to guide users through a procedure.</span></span>

<span data-ttu-id="9f211-105">嚮導是簡化使用者體驗的其中一個關鍵。</span><span class="sxs-lookup"><span data-stu-id="9f211-105">Wizards are one of the keys to simplifying the user experience.</span></span> <span data-ttu-id="9f211-106">它們可讓您執行複雜的作業，例如應用程式的設定，並將其分成一系列簡單的步驟。</span><span class="sxs-lookup"><span data-stu-id="9f211-106">They allow you to take a complex operation, such as configuration of an application, and break it into a series of simple steps.</span></span> <span data-ttu-id="9f211-107">在程式的每個階段，您可以提供所需專案的說明，並顯示可讓使用者進行選取並輸入文字的控制項。</span><span class="sxs-lookup"><span data-stu-id="9f211-107">At each point in the process, you can provide an explanation of what is needed, and display controls that allow the user to make selections and enter text.</span></span>

<span data-ttu-id="9f211-108">Wizard 其實是一種屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="9f211-108">A wizard is actually a type of property sheet.</span></span> <span data-ttu-id="9f211-109">屬性工作表基本上是 *頁面* 集合的容器，每個頁面都是個別的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="9f211-109">A property sheet is essentially a container for a collection of *pages*, where each page is a separate dialog box.</span></span> <span data-ttu-id="9f211-110">雖然一般屬性工作表可讓使用者隨時存取任何頁面，但嚮導會依序顯示頁面。</span><span class="sxs-lookup"><span data-stu-id="9f211-110">Whereas regular property sheets allow the user to access any page at any time, wizards present pages in sequence.</span></span> <span data-ttu-id="9f211-111">按鈕是用來向前及向後導覽，而不是索引標籤。</span><span class="sxs-lookup"><span data-stu-id="9f211-111">Instead of tabs, buttons are used to navigate forward and backward.</span></span> <span data-ttu-id="9f211-112">頁面的顯示順序是由應用程式所控制，並且可以根據使用者輸入加以修改。</span><span class="sxs-lookup"><span data-stu-id="9f211-112">The order in which pages are displayed is controlled by the application and can be modified based on user input.</span></span>

<span data-ttu-id="9f211-113">Wizard 有兩種主要的樣式：舊版 Wizard97 樣式，以及 Windows Vista 中引進的 Aero 樣式。</span><span class="sxs-lookup"><span data-stu-id="9f211-113">There are two main styles of wizard: the older Wizard97 style, and the Aero style introduced in Windows Vista.</span></span> <span data-ttu-id="9f211-114">如需圖例，請參閱 [關於屬性工作表](property-sheets.md)。</span><span class="sxs-lookup"><span data-stu-id="9f211-114">For illustrations, see [About Property Sheets](property-sheets.md).</span></span> <span data-ttu-id="9f211-115"> (第三種樣式，只使用 PSH \_ WIZARD 或 PSH \_ wizard \_ LITE 旗標，提供簡單的屬性工作表順序，不含標頭或浮水印。 ) </span><span class="sxs-lookup"><span data-stu-id="9f211-115">(A third style, using just the PSH\_WIZARD or PSH\_WIZARD\_LITE flag, presents a simple sequence of property sheets with no headers or watermarks.)</span></span>

> [!Note]  
> <span data-ttu-id="9f211-116">在嚮導的內容中，「浮水印」是顯示在部分頁面左邊界的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="9f211-116">A "watermark" in the context of wizards is a bitmap that appears in the left margin of some pages.</span></span>

 

<span data-ttu-id="9f211-117">本檔中的討論內容假設您正在為具有 [5.80 版](common-control-versions.md) 或更新版本之通用控制項的系統，執行嚮導。</span><span class="sxs-lookup"><span data-stu-id="9f211-117">The discussion in most of this document assumes that you are implementing a wizard for a system with [version 5.80](common-control-versions.md) or later of the common controls.</span></span> <span data-ttu-id="9f211-118">如果您嘗試使用 Wizard97 樣式搭配舊版的通用控制項，則您的應用程式可能會進行編譯，但不會正確顯示。</span><span class="sxs-lookup"><span data-stu-id="9f211-118">If you attempt to use the Wizard97 style with earlier versions of the common controls, your application may compile but it will not display properly.</span></span> <span data-ttu-id="9f211-119">如需有關如何在舊版系統上建立與 Wizard97 相容的 wizard 的討論，請參閱本主題稍後的回溯相容的 wizard。</span><span class="sxs-lookup"><span data-stu-id="9f211-119">For a discussion about how to create a Wizard97-compatible wizard on earlier systems, see Backward Compatible Wizards later in this topic.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="9f211-120">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="9f211-120">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="9f211-121">技術</span><span class="sxs-lookup"><span data-stu-id="9f211-121">Technologies</span></span>

-   [<span data-ttu-id="9f211-122">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="9f211-122">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="9f211-123">必要條件</span><span class="sxs-lookup"><span data-stu-id="9f211-123">Prerequisites</span></span>

-   <span data-ttu-id="9f211-124">C/C++</span><span class="sxs-lookup"><span data-stu-id="9f211-124">C/C++</span></span>
-   <span data-ttu-id="9f211-125">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="9f211-125">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="9f211-126">指示</span><span class="sxs-lookup"><span data-stu-id="9f211-126">Instructions</span></span>

### <a name="wizard-implementation"></a><span data-ttu-id="9f211-127">Wizard 執行</span><span class="sxs-lookup"><span data-stu-id="9f211-127">Wizard Implementation</span></span>

<span data-ttu-id="9f211-128">執行嚮導與執行一般的屬性工作表類似。</span><span class="sxs-lookup"><span data-stu-id="9f211-128">Implementing a wizard is similar to implementing a regular property sheet.</span></span> <span data-ttu-id="9f211-129">在最基本的層級中，您可以在定義屬性工作表的 [**PROPSHEETHEADER**](pss-propsheetheader.md) 結構中，設定下列其中一個旗標或旗標組合。</span><span class="sxs-lookup"><span data-stu-id="9f211-129">At the most basic level, it is a matter of setting one of the following flags or combinations of flags in the [**PROPSHEETHEADER**](pss-propsheetheader.md) structure that defines the property sheet.</span></span>



| <span data-ttu-id="9f211-130">旗標</span><span class="sxs-lookup"><span data-stu-id="9f211-130">Flag</span></span>                           | <span data-ttu-id="9f211-131">樣式</span><span class="sxs-lookup"><span data-stu-id="9f211-131">Style</span></span>                                                                                                                                                 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f211-132">PSH \_ WIZARD</span><span class="sxs-lookup"><span data-stu-id="9f211-132">PSH\_WIZARD</span></span>                    | <span data-ttu-id="9f211-133">沒有標頭或點陣圖的簡易 wizard。</span><span class="sxs-lookup"><span data-stu-id="9f211-133">A simple wizard with no headers or bitmaps.</span></span>                                                                                                           |
| <span data-ttu-id="9f211-134">PSH \_ WIZARD \_ LITE</span><span class="sxs-lookup"><span data-stu-id="9f211-134">PSH\_WIZARD\_LITE</span></span>              | <span data-ttu-id="9f211-135">類似于 PSH \_ WIZARD，外觀上有些微差異; 例如，按鈕上方的分隔線會設定為視窗的全形。</span><span class="sxs-lookup"><span data-stu-id="9f211-135">Similar to PSH\_WIZARD, with some minor differences in appearance; for example, the divider above the buttons is set to the full width of the window.</span></span> |
| <span data-ttu-id="9f211-136">PSH \_ WIZARD97</span><span class="sxs-lookup"><span data-stu-id="9f211-136">PSH\_WIZARD97</span></span>                  | <span data-ttu-id="9f211-137">Wizard97 wizard (選擇性的) 標頭、標頭點陣圖和浮水印。</span><span class="sxs-lookup"><span data-stu-id="9f211-137">A Wizard97 wizard with (optional) headers, header bitmaps, and watermarks.</span></span>                                                                            |
| <span data-ttu-id="9f211-138">PSH \_ WIZARD \| PSH \_ AEROWIZARD</span><span class="sxs-lookup"><span data-stu-id="9f211-138">PSH\_WIZARD \| PSH\_AEROWIZARD</span></span> | <span data-ttu-id="9f211-139">Aero Wizard。</span><span class="sxs-lookup"><span data-stu-id="9f211-139">An Aero Wizard.</span></span> <span data-ttu-id="9f211-140">Aero 的嚮導不會使用浮水印或標頭點陣圖。</span><span class="sxs-lookup"><span data-stu-id="9f211-140">Aero Wizards do not use watermarks or header bitmaps.</span></span> <span data-ttu-id="9f211-141">它們需要單一執行緒的單元 (STA) 模型。</span><span class="sxs-lookup"><span data-stu-id="9f211-141">They require the single-threaded apartment (STA) model.</span></span>                         |



 

<span data-ttu-id="9f211-142">執行嚮導的基本程式如下所示：</span><span class="sxs-lookup"><span data-stu-id="9f211-142">The basic procedure for implementing a wizard is as follows:</span></span>

1.  <span data-ttu-id="9f211-143">為每個頁面建立對話方塊範本。</span><span class="sxs-lookup"><span data-stu-id="9f211-143">Create a dialog box template for each page.</span></span>
2.  <span data-ttu-id="9f211-144">藉由建立每個頁面的 [**PROPSHEETPAGE**](pss-propsheetpage.md) 結構來定義頁面。</span><span class="sxs-lookup"><span data-stu-id="9f211-144">Define the pages by creating a [**PROPSHEETPAGE**](pss-propsheetpage.md) structure for each page.</span></span> <span data-ttu-id="9f211-145">此結構會定義頁面，並包含對話方塊範本和任何點陣圖或其他資源的指標。</span><span class="sxs-lookup"><span data-stu-id="9f211-145">This structure defines the page, and contains pointers to the dialog box template and any bitmaps or other resources.</span></span>
3.  <span data-ttu-id="9f211-146">將在上一個步驟中建立的 [**PROPSHEETPAGE**](pss-propsheetpage.md) 結構傳遞至 [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) 函數，以建立頁面的 HPROPSHEETPAGE 控制碼。</span><span class="sxs-lookup"><span data-stu-id="9f211-146">Pass the [**PROPSHEETPAGE**](pss-propsheetpage.md) structure that was created in the previous step to the [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) function to create the page's HPROPSHEETPAGE handle.</span></span>
4.  <span data-ttu-id="9f211-147">藉由建立 [**PROPSHEETHEADER**](pss-propsheetheader.md) 結構來定義嚮導。</span><span class="sxs-lookup"><span data-stu-id="9f211-147">Define the wizard by creating a [**PROPSHEETHEADER**](pss-propsheetheader.md) structure for it.</span></span>
5.  <span data-ttu-id="9f211-148">將 [**PROPSHEETHEADER**](pss-propsheetheader.md) 結構傳遞至 [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) 函式，以顯示嚮導。</span><span class="sxs-lookup"><span data-stu-id="9f211-148">Pass the [**PROPSHEETHEADER**](pss-propsheetheader.md) structure to the [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) function to display the wizard.</span></span>
6.  <span data-ttu-id="9f211-149">針對每個頁面執行對話方塊程式，以處理來自頁面控制項的通知訊息，以及 wizard 的按鈕和處理其他 Windows 訊息。</span><span class="sxs-lookup"><span data-stu-id="9f211-149">Implement dialog box procedures for each page to handle notification messages from the page's controls and the wizard's buttons and to process other Windows messaging.</span></span>

### <a name="create-the-dialog-box-templates"></a><span data-ttu-id="9f211-150">建立對話方塊範本</span><span class="sxs-lookup"><span data-stu-id="9f211-150">Create the Dialog Box Templates</span></span>

<span data-ttu-id="9f211-151">有兩種基本類型的 wizard 頁面：外部和內部。</span><span class="sxs-lookup"><span data-stu-id="9f211-151">There are two basic types of wizard page: exterior and interior.</span></span> <span data-ttu-id="9f211-152">外部頁面是 (歡迎使用) 和完成頁面的簡介。</span><span class="sxs-lookup"><span data-stu-id="9f211-152">Exterior pages are the introduction (welcome) and completion pages.</span></span> <span data-ttu-id="9f211-153">所有其他都是內部頁面。</span><span class="sxs-lookup"><span data-stu-id="9f211-153">All others are interior pages.</span></span>

<span data-ttu-id="9f211-154">**外部頁面對話方塊範本**</span><span class="sxs-lookup"><span data-stu-id="9f211-154">**Exterior Page Dialog Box Templates**</span></span>

<span data-ttu-id="9f211-155">簡介和完成頁面的基本版面配置相同。</span><span class="sxs-lookup"><span data-stu-id="9f211-155">The basic layout of the introduction and completion pages is identical.</span></span> <span data-ttu-id="9f211-156">下圖顯示範例 Wizard97 簡介頁面，以及預留位置浮水印。</span><span class="sxs-lookup"><span data-stu-id="9f211-156">The following illustration shows a sample Wizard97 introduction page, with a placeholder watermark.</span></span>

![顯示 wizard 頁面的螢幕擷取畫面，右邊有一個圖形、右邊的標題和內文文字，以及底部的 [上一頁] 和 [取消] 按鈕](images/wiz97exterior.png)

<span data-ttu-id="9f211-158">針對 Wizard97 的外部頁面，對話方塊範本為317x193 對話方塊單位。</span><span class="sxs-lookup"><span data-stu-id="9f211-158">For Wizard97 exterior pages, the dialog box template is 317x193 dialog units.</span></span> <span data-ttu-id="9f211-159">它會填滿所有的 wizard，除了包含 [ **上一頁** **]、[下一頁]** 和 [ **取消** ] 按鈕的標題和頻外。</span><span class="sxs-lookup"><span data-stu-id="9f211-159">It fills all of the wizard, except for the caption and the band at the bottom that contains the **Back**, **Next**, and **Cancel** buttons.</span></span> <span data-ttu-id="9f211-160">範本的左邊是保留給「浮水印」點陣圖，不應包含任何控制項。</span><span class="sxs-lookup"><span data-stu-id="9f211-160">The left side of the template, which is reserved for a "watermark" bitmap, should not contain any controls.</span></span> <span data-ttu-id="9f211-161">浮水印是在 wizard 的 [**PROPSHEETHEADER**](pss-propsheetheader.md) 結構中指定，並且會自動加入至頁面。</span><span class="sxs-lookup"><span data-stu-id="9f211-161">The watermark is specified in the wizard's [**PROPSHEETHEADER**](pss-propsheetheader.md) structure and is added to the page automatically.</span></span> <span data-ttu-id="9f211-162">設計資源範本時，您必須允許其空間。</span><span class="sxs-lookup"><span data-stu-id="9f211-162">You must allow space for it when designing the resource template.</span></span>

<span data-ttu-id="9f211-163">當您建立浮水印點陣圖時，請記住，如果使用者選擇大型系統字型，對話方塊的大小可能會增加。</span><span class="sxs-lookup"><span data-stu-id="9f211-163">When you create the watermark bitmap, keep in mind that the dialog box may increase in size if, for example, the user chooses a large system font.</span></span> <span data-ttu-id="9f211-164">不同的語言也傾向于使用不同的字型計量。</span><span class="sxs-lookup"><span data-stu-id="9f211-164">Different languages also tend to have different font metrics.</span></span> <span data-ttu-id="9f211-165">當頁面成長時，為浮水印保留的區域會以比例放大。</span><span class="sxs-lookup"><span data-stu-id="9f211-165">When the page grows, the area reserved for the watermark gets proportionately larger.</span></span> <span data-ttu-id="9f211-166">不過，您無法變更浮水印點陣圖，也不能延展點陣圖以填滿較大的區域。</span><span class="sxs-lookup"><span data-stu-id="9f211-166">However, you cannot change the watermark bitmap, nor is the bitmap stretched to fill the larger area.</span></span> <span data-ttu-id="9f211-167">相反地，點陣圖會保留在保留區域左上角部分的原始大小。</span><span class="sxs-lookup"><span data-stu-id="9f211-167">Instead, the bitmap is left in its original size in the upper-left portion of the reserved area.</span></span> <span data-ttu-id="9f211-168">浮水印未涵蓋的較大保留區域部分，會自動填入點陣圖左上角圖元的色彩。</span><span class="sxs-lookup"><span data-stu-id="9f211-168">The part of the larger reserved area that is not covered by the watermark is automatically filled with the color of the bitmap's upper-left pixel.</span></span>

<span data-ttu-id="9f211-169">如果您需要針對不同的字型計量使用不同大小的浮水印點陣圖，有兩個可能的解決方案：</span><span class="sxs-lookup"><span data-stu-id="9f211-169">If you need to have different-sized watermark bitmaps for different font metrics, two possible solutions are:</span></span>

-   <span data-ttu-id="9f211-170">建立嚮導之前取得字型計量，並指定適當大小的浮水印點陣圖。</span><span class="sxs-lookup"><span data-stu-id="9f211-170">Get the font metrics before creating the wizard, and specify an appropriately sized watermark bitmap.</span></span>
-   <span data-ttu-id="9f211-171">建立嚮導時，請勿指定浮水印點陣圖。</span><span class="sxs-lookup"><span data-stu-id="9f211-171">Do not specify a watermark bitmap when you create the wizard.</span></span> <span data-ttu-id="9f211-172">Wizard97 會將浮水印區域保留空白。</span><span class="sxs-lookup"><span data-stu-id="9f211-172">Wizard97 will leave the watermark area blank.</span></span> <span data-ttu-id="9f211-173">然後，在為浮水印保留的區域上繪製適當大小的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="9f211-173">Then draw an appropriately sized bitmap on the area reserved for the watermark.</span></span>

<span data-ttu-id="9f211-174">您可以依照一般對話方塊的方式，將控制項放在浮水印右邊的區域中。</span><span class="sxs-lookup"><span data-stu-id="9f211-174">You can place controls in the area to the right of the watermark as you would for a regular dialog box.</span></span> <span data-ttu-id="9f211-175">此區域的背景色彩是由系統決定，而不需要您採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="9f211-175">The background color of this area is determined by the system, and requires no action on your part.</span></span> <span data-ttu-id="9f211-176">您通常會在此區域中放置兩個靜態控制項。</span><span class="sxs-lookup"><span data-stu-id="9f211-176">You typically put two static controls in this area.</span></span> <span data-ttu-id="9f211-177">上半部會保存標題，並使用大型粗體字型 (Wizard97) 的12點 Verdana 粗體。</span><span class="sxs-lookup"><span data-stu-id="9f211-177">The upper one holds the title and uses a large bold font (12 point Verdana Bold for Wizard97).</span></span> <span data-ttu-id="9f211-178">另一種是解說文字，則使用標準對話方塊字型。</span><span class="sxs-lookup"><span data-stu-id="9f211-178">The other one, which is for explanatory text, uses the standard dialog box font.</span></span>

<span data-ttu-id="9f211-179">[簡介] 和 [完成] 頁面之間的主要差異是 [wizard] 按鈕和靜態控制項中的文字。</span><span class="sxs-lookup"><span data-stu-id="9f211-179">The main difference between the introduction and completion pages is the wizard buttons and the text in the static controls.</span></span> <span data-ttu-id="9f211-180">簡介頁面通常會有 **下** 一個按鈕和 [ **上一頁** ] 按鈕，而且只會啟用 [ **下一步]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="9f211-180">Introduction pages normally have a **Next** and a **Back** button, with only the **Next** button enabled.</span></span> <span data-ttu-id="9f211-181">完成頁面會啟用 [ **上一頁** ] 按鈕，而 [ **下一步** ] 按鈕會由 **[完成]** 按鈕取代。</span><span class="sxs-lookup"><span data-stu-id="9f211-181">Completion pages have the **Back** button enabled, and the **Next** button is replaced by a **Finish** button.</span></span>

> [!Note]  
> <span data-ttu-id="9f211-182">在 Aero 精靈中，[ **上一頁** ] 按鈕會由標題列中的箭號按鈕取代。</span><span class="sxs-lookup"><span data-stu-id="9f211-182">In Aero Wizards, the **Back** button is replaced by an arrow button in the caption bar.</span></span>

 

<span data-ttu-id="9f211-183">您可以將 [**PSM \_ SETFINISHTEXT**](psm-setfinishtext.md)訊息傳送給 wizard，以修改 [**完成]** 按鈕上的文字。</span><span class="sxs-lookup"><span data-stu-id="9f211-183">You can modify the text on the **Finish** button by sending the wizard a [**PSM\_SETFINISHTEXT**](psm-setfinishtext.md) message.</span></span> <span data-ttu-id="9f211-184">依預設，[ **完成]** 按鈕不包含鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="9f211-184">By default, the **Finish** button does not include a keyboard accelerator.</span></span> <span data-ttu-id="9f211-185">若要定義鍵盤快速鍵，請在您傳遞至 PSM SETFINISHTEXT 的文字字串中包含連字號 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9f211-185">To define a keyboard accelerator, include an ampersand in the text string that you pass to PSM\_SETFINISHTEXT.</span></span> <span data-ttu-id="9f211-186">例如，「&完成」會將 ' F ' 定義為鍵盤對應鍵。</span><span class="sxs-lookup"><span data-stu-id="9f211-186">For instance, "&Finish" defines 'F' as the keyboard accelerator.</span></span>

<span data-ttu-id="9f211-187">**內部頁面對話方塊範本**</span><span class="sxs-lookup"><span data-stu-id="9f211-187">**Interior Page Dialog Box Templates**</span></span>

<span data-ttu-id="9f211-188">內部頁面的外觀與外部頁面稍有不同。</span><span class="sxs-lookup"><span data-stu-id="9f211-188">Interior pages have a somewhat different appearance than exterior pages.</span></span> <span data-ttu-id="9f211-189">下圖顯示範例 Wizard97 內部頁面，其中包含預留位置標頭點陣圖。</span><span class="sxs-lookup"><span data-stu-id="9f211-189">The following illustration shows a sample Wizard97 interior page, with a placeholder header bitmap.</span></span>

![頁面的螢幕擷取畫面，其中包含標題和子標題文字，以及頂端的文字、中間的文字，以及底部的按鈕](images/wiz97interior.png)

<span data-ttu-id="9f211-191">頁面頂端的標頭區域是由屬性工作表處理，因此不會包含在範本中。</span><span class="sxs-lookup"><span data-stu-id="9f211-191">The header area at the top of the page is handled by the property sheet, so it is not included in the template.</span></span> <span data-ttu-id="9f211-192">標頭的內容會指定在頁面的 [**PROPSHEETPAGE**](pss-propsheetpage.md) 結構和 Wizard 的 [**PROPSHEETHEADER**](pss-propsheetheader.md) 結構中。</span><span class="sxs-lookup"><span data-stu-id="9f211-192">The contents of the header are specified in the page's [**PROPSHEETPAGE**](pss-propsheetpage.md) structure and the wizard's [**PROPSHEETHEADER**](pss-propsheetheader.md) structure.</span></span> <span data-ttu-id="9f211-193">因為內部頁面必須符合標題和按鈕，所以 Wizard97 對話方塊範本是317x143 對話單位，稍微小於外部頁面的範本。</span><span class="sxs-lookup"><span data-stu-id="9f211-193">Because the interior page needs to fit between the header and the buttons, the Wizard97 dialog box template is 317x143 dialog units, somewhat smaller than the template for exterior pages.</span></span>

<span data-ttu-id="9f211-194">下圖顯示從相同範本建立的 Aero Wizard。</span><span class="sxs-lookup"><span data-stu-id="9f211-194">The following illustration shows an Aero Wizard that was created from the same template.</span></span>

![螢幕擷取畫面，其頂端有標題區域，且底部只有 [下一步] 和 [取消] 按鈕，與上一個專案不同](images/wizardaerointerior.png)

### <a name="define-the-wizard-pages"></a><span data-ttu-id="9f211-196">定義嚮導頁面</span><span class="sxs-lookup"><span data-stu-id="9f211-196">Define the Wizard Pages</span></span>

<span data-ttu-id="9f211-197">建立對話方塊範本和相關資源（例如點陣圖和字串資料表）之後，您可以建立屬性工作表頁面。</span><span class="sxs-lookup"><span data-stu-id="9f211-197">After you have created the dialog box templates and related resources such as bitmaps and string tables, you can create the property sheet pages.</span></span> <span data-ttu-id="9f211-198">此程式類似于標準屬性工作表的程式。</span><span class="sxs-lookup"><span data-stu-id="9f211-198">The procedure is similar to that for standard property sheets.</span></span> <span data-ttu-id="9f211-199">首先，填入 [**PROPSHEETPAGE**](pss-propsheetpage.md) 結構的適當成員。</span><span class="sxs-lookup"><span data-stu-id="9f211-199">First, fill in the appropriate members of a [**PROPSHEETPAGE**](pss-propsheetpage.md) structure.</span></span> <span data-ttu-id="9f211-200"> (部分成員是由嚮導所特有。 ) 接著呼叫 [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) 函式來建立頁面的 HPROPSHEETPAGE 控制碼。</span><span class="sxs-lookup"><span data-stu-id="9f211-200">(Some members are specific to wizards.) Then call the [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) function to create the page's HPROPSHEETPAGE handle.</span></span>

<span data-ttu-id="9f211-201">下列與 wizard 相關的旗標可以在 [**PROPSHEETPAGE**](pss-propsheetpage.md)結構的 **dwFlags** 成員中設定。</span><span class="sxs-lookup"><span data-stu-id="9f211-201">The following wizard-related flags can be set in the **dwFlags** member of the [**PROPSHEETPAGE**](pss-propsheetpage.md) structure.</span></span>



| <span data-ttu-id="9f211-202">旗標</span><span class="sxs-lookup"><span data-stu-id="9f211-202">Flag</span></span>                   | <span data-ttu-id="9f211-203">描述</span><span class="sxs-lookup"><span data-stu-id="9f211-203">Description</span></span>                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f211-204">PSP \_ HIDEHEADER</span><span class="sxs-lookup"><span data-stu-id="9f211-204">PSP\_HIDEHEADER</span></span>        | <span data-ttu-id="9f211-205">針對 Wizard97 中的外部頁面設定此旗標。</span><span class="sxs-lookup"><span data-stu-id="9f211-205">Set this flag for exterior pages in Wizard97.</span></span> <span data-ttu-id="9f211-206">標頭不會顯示，而且可以顯示浮水印。</span><span class="sxs-lookup"><span data-stu-id="9f211-206">The header is not shown, and a watermark can be shown.</span></span>                                |
| <span data-ttu-id="9f211-207">PSP \_ USEHEADERTITLE</span><span class="sxs-lookup"><span data-stu-id="9f211-207">PSP\_USEHEADERTITLE</span></span>    | <span data-ttu-id="9f211-208">為內部頁面設定此旗標，將標題放在 Wizard97 的標頭區域中，或在 Aero Wizard 中的工作區頂端。</span><span class="sxs-lookup"><span data-stu-id="9f211-208">Set this flag for interior pages to put a title in the header area in Wizard97, or at the top of the client area in an Aero Wizard.</span></span> |
| <span data-ttu-id="9f211-209">PSP \_ USEHEADERSUBTITLE</span><span class="sxs-lookup"><span data-stu-id="9f211-209">PSP\_USEHEADERSUBTITLE</span></span> | <span data-ttu-id="9f211-210">為內部頁面設定此旗標，以在 Wizard97 的標頭區域中放入子標題。</span><span class="sxs-lookup"><span data-stu-id="9f211-210">Set this flag for interior pages to put a subtitle in the header area in Wizard97.</span></span>                                                  |



 

<span data-ttu-id="9f211-211">如果您已設定 PSP \_ USEHEADERTITLE 或 psp \_ USEHEADERSUBTITLE，請分別將標題和子標題文字指派給 **pszHeaderTitle** 和 **pszHeaderSubtitle** 成員。</span><span class="sxs-lookup"><span data-stu-id="9f211-211">If you have set PSP\_USEHEADERTITLE or PSP\_USEHEADERSUBTITLE, assign the title and subtitle text to the **pszHeaderTitle** and **pszHeaderSubtitle** members, respectively.</span></span> <span data-ttu-id="9f211-212">當您將文字字串指派給 [**PROPSHEETPAGE**](pss-propsheetpage.md) 和 [**PROPSHEETHEADER**](pss-propsheetheader.md) 結構的成員時，您可以指派字串指標，或使用 **MAKEINTRESOURCE** 宏來指派字串資源的值。</span><span class="sxs-lookup"><span data-stu-id="9f211-212">When you assign text strings to members of the [**PROPSHEETPAGE**](pss-propsheetpage.md) and [**PROPSHEETHEADER**](pss-propsheetheader.md) structures, you can either assign a string pointer or use the **MAKEINTRESOURCE** macro to assign a value from a string resource.</span></span> <span data-ttu-id="9f211-213">字串資源是從 wizard **PROPSHEETHEADER** 結構的 **hInstance** 成員所指定的模組載入。</span><span class="sxs-lookup"><span data-stu-id="9f211-213">The string resource is loaded from the module specified in the **hInstance** member of the wizard's **PROPSHEETHEADER** structure.</span></span>

<span data-ttu-id="9f211-214">當您呼叫 [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) 來建立頁面時，請將結果指派給 HPROPSHEETPAGE 控制碼陣列的元素。</span><span class="sxs-lookup"><span data-stu-id="9f211-214">When you call [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) to create a page, assign the result to an element of an array of HPROPSHEETPAGE handles.</span></span> <span data-ttu-id="9f211-215">建立屬性工作表時，會使用這個陣列。</span><span class="sxs-lookup"><span data-stu-id="9f211-215">This array is used when creating the property sheet.</span></span> <span data-ttu-id="9f211-216">頁面控制碼的陣列索引會決定其顯示的預設順序。</span><span class="sxs-lookup"><span data-stu-id="9f211-216">The array index of a page's handle determines the default order in which it is displayed.</span></span> <span data-ttu-id="9f211-217">建立頁面的 HPROPSHEETPAGE 控制碼之後，您可以重複使用相同的 [**PROPSHEETPAGE**](pss-propsheetpage.md) 結構，藉由指派新值給相關成員來建立下一頁。</span><span class="sxs-lookup"><span data-stu-id="9f211-217">After you have created a page's HPROPSHEETPAGE handle, you can reuse the same [**PROPSHEETPAGE**](pss-propsheetpage.md) structure to create the next page by assigning new values to the relevant members.</span></span>

<span data-ttu-id="9f211-218">建立頁面的另一種方式是為每個頁面使用不同的 [**PROPSHEETPAGE**](pss-propsheetpage.md) 結構，並建立結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="9f211-218">An alternative way to create pages is to use separate [**PROPSHEETPAGE**](pss-propsheetpage.md) structures for each page, and create an array of structures.</span></span> <span data-ttu-id="9f211-219">建立屬性工作表時，會使用這個陣列，而不是 HPROPSHEETPAGE 控制碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="9f211-219">This array is used instead of an array of HPROPSHEETPAGE handles when creating the property sheet.</span></span> <span data-ttu-id="9f211-220">使用個別的 **PROPSHEETPAGE** 結構，不需要呼叫 [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) ，但會使用更多的記憶體。</span><span class="sxs-lookup"><span data-stu-id="9f211-220">Using separate **PROPSHEETPAGE** structures eliminates the need to call [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) but uses more memory.</span></span> <span data-ttu-id="9f211-221">否則，這兩種方法之間並沒有顯著的差異。</span><span class="sxs-lookup"><span data-stu-id="9f211-221">Otherwise, there is no significant difference between the two approaches.</span></span>

<span data-ttu-id="9f211-222">下列範例會將值指派給 [**PROPSHEETPAGE**](pss-propsheetpage.md) 結構，以定義內部 Wizard97 頁面。</span><span class="sxs-lookup"><span data-stu-id="9f211-222">The following example defines an interior Wizard97 page by assigning values to a [**PROPSHEETPAGE**](pss-propsheetpage.md) structure.</span></span> <span data-ttu-id="9f211-223">在此範例中，頁面的標題、子標題和對話方塊範本都是由其資源識別碼所識別。</span><span class="sxs-lookup"><span data-stu-id="9f211-223">In this example, the page's title, subtitle, and dialog box template are all identified by their resource IDs.</span></span> <span data-ttu-id="9f211-224">然後呼叫 [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) 函式來建立頁面的 HPROPSHEETPAGE 控制碼。</span><span class="sxs-lookup"><span data-stu-id="9f211-224">The [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) function is then called to create the page's HPROPSHEETPAGE handle.</span></span> <span data-ttu-id="9f211-225">因為它將會是第二頁，所以會將控制碼指派給控制碼 *ahpsp* 的陣列，索引為1。</span><span class="sxs-lookup"><span data-stu-id="9f211-225">Because it will be the second page to appear, the handle is assigned to the array of handles, *ahpsp*, with an index of 1.</span></span>


```C++
// g_hInstance is the global HINSTANCE of the application.
// IntPage1DlgProc is the dialog procedure for this page.
// ahpsp is an array of HPROPSHEETPAGE handles.

PROPSHEETPAGE psp = { sizeof(psp) };

psp.hInstance         = g_hInstance;
psp.dwFlags           = PSP_USEHEADERTITLE | PSP_USEHEADERSUBTITLE;
psp.lParam            = (LPARAM) &wizdata;
psp.pszHeaderTitle    = MAKEINTRESOURCE(IDS_TITLE1);
psp.pszHeaderSubTitle = MAKEINTRESOURCE(IDS_SUBTITLE1);
psp.pszTemplate       = MAKEINTRESOURCE(IDD_INTERIOR1);
psp.pfnDlgProc        = IntPage1DlgProc;

ahpsp[1] = CreatePropertySheetPage(&psp);
```



### <a name="custom-page-data"></a><span data-ttu-id="9f211-226">自訂頁面資料</span><span class="sxs-lookup"><span data-stu-id="9f211-226">Custom Page Data</span></span>

<span data-ttu-id="9f211-227">當您建立網頁時，您可以使用 [**PROPSHEETPAGE**](pss-propsheetpage.md)結構的 **lParam** 成員將自訂資料指派給它，通常是藉由將指標指派給使用者定義的結構。</span><span class="sxs-lookup"><span data-stu-id="9f211-227">When you create a page, you can assign custom data to it by using the **lParam** member of the [**PROPSHEETPAGE**](pss-propsheetpage.md) structure, typically by assigning it a pointer to a user-defined structure.</span></span>

<span data-ttu-id="9f211-228">第一次選取頁面時，其對話方塊程式會收到 [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) 訊息。</span><span class="sxs-lookup"><span data-stu-id="9f211-228">When the page is first selected, its dialog box procedure receives a [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) message.</span></span> <span data-ttu-id="9f211-229">訊息的 *lParam* 值指向頁面 [**PROPSHEETPAGE**](pss-propsheetpage.md) 結構的複本，您可以從中取得自訂資料。</span><span class="sxs-lookup"><span data-stu-id="9f211-229">The message's *lParam* value points to a copy of of the page's [**PROPSHEETPAGE**](pss-propsheetpage.md) structure, from which you can retrieve the custom data.</span></span> <span data-ttu-id="9f211-230">然後，您可以使用 [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) 搭配 GWL \_ USERDATA 作為索引參數，來儲存這項資料以用於後續訊息。</span><span class="sxs-lookup"><span data-stu-id="9f211-230">You can then store this data for use in subsequent messages by using [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) with GWL\_USERDATA as the index parameter.</span></span> <span data-ttu-id="9f211-231">多個頁面可以有相同資料的指標，而任何頁面所做的資料變更都可供其對話方塊程式中的其他頁面使用。</span><span class="sxs-lookup"><span data-stu-id="9f211-231">Multiple pages can have a pointer to the same data, and any change to the data made by one page is available to the other pages in their dialog procedures.</span></span>

### <a name="define-the-wizard-property-sheet"></a><span data-ttu-id="9f211-232">定義 Wizard 屬性工作表</span><span class="sxs-lookup"><span data-stu-id="9f211-232">Define the Wizard Property Sheet</span></span>

<span data-ttu-id="9f211-233">如同一般的屬性工作表，您可以藉由填入 [**PROPSHEETHEADER**](pss-propsheetheader.md) 結構的成員來定義 wizard 的屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="9f211-233">As with ordinary property sheets, you define the wizard's property sheet by filling in members of a [**PROPSHEETHEADER**](pss-propsheetheader.md) structure.</span></span> <span data-ttu-id="9f211-234">此結構可讓您指定組成 wizard 的頁面，以及顯示的預設順序，以及數個相關的參數。</span><span class="sxs-lookup"><span data-stu-id="9f211-234">This structure allows you to specify the pages that make up the wizard and the default order in which they are displayed, along with several related parameters.</span></span> <span data-ttu-id="9f211-235">接著，您可以藉由呼叫 [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) 函式來啟動精靈。</span><span class="sxs-lookup"><span data-stu-id="9f211-235">You then launch the wizard by calling the [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) function.</span></span>

<span data-ttu-id="9f211-236">在 Wizard97 樣式中，會忽略 [**PROPSHEETHEADER**](pss-propsheetheader.md)結構的 **pszCaption** 成員。</span><span class="sxs-lookup"><span data-stu-id="9f211-236">In the Wizard97 style, the **pszCaption** member of the [**PROPSHEETHEADER**](pss-propsheetheader.md) structure is ignored.</span></span> <span data-ttu-id="9f211-237">相反地，嚮導會顯示目前頁面的對話方塊範本中指定的標題。</span><span class="sxs-lookup"><span data-stu-id="9f211-237">Instead, the wizard displays the caption that is specified in the current page's dialog box template.</span></span> <span data-ttu-id="9f211-238">如果範本缺少標題，則會顯示前一頁的標題。</span><span class="sxs-lookup"><span data-stu-id="9f211-238">If the template lacks a caption, the caption from the previous page is displayed.</span></span> <span data-ttu-id="9f211-239">因此，若要在所有頁面上顯示相同的標題，請在 [簡介] 頁面的範本中指定標題。</span><span class="sxs-lookup"><span data-stu-id="9f211-239">Thus, to display the same caption on all pages, specify the caption in the template for the introductory page.</span></span>

<span data-ttu-id="9f211-240">在 Aero Wizard 樣式中，對話方塊標題是取自 **pszCaption**。</span><span class="sxs-lookup"><span data-stu-id="9f211-240">In the Aero Wizard style, the dialog box caption is taken from **pszCaption**.</span></span>

<span data-ttu-id="9f211-241">如果您已建立頁面的 HPROPSHEETPAGE 控制碼陣列，請將陣列指派給 **phpage** 成員。</span><span class="sxs-lookup"><span data-stu-id="9f211-241">If you have created an array of HPROPSHEETPAGE handles for your pages, assign the array to the **phpage** member.</span></span> <span data-ttu-id="9f211-242">如果您改為建立 [**PROPSHEETPAGE**](pss-propsheetpage.md) 結構的陣列，請將陣列指派給 **ppsp** 成員，然後 \_ 在 **dwFlags** 成員中設定 PSH PROPSHEETPAGE 旗標。</span><span class="sxs-lookup"><span data-stu-id="9f211-242">If you have instead created an array of [**PROPSHEETPAGE**](pss-propsheetpage.md) structures, assign the array to the **ppsp** member and set the PSH\_PROPSHEETPAGE flag in the **dwFlags** member.</span></span>

<span data-ttu-id="9f211-243">下列範例會將值指派給 *psh*、 [**PROPSHEETHEADER**](pss-propsheetheader.md) 結構，然後呼叫 [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) 函式來啟動 wizard。</span><span class="sxs-lookup"><span data-stu-id="9f211-243">The following example assigns values to *psh*, a [**PROPSHEETHEADER**](pss-propsheetheader.md) structure, and calls the [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) function to launch the wizard.</span></span> <span data-ttu-id="9f211-244">Wizard97 樣式的 wizard 具有浮水印和標頭圖形，由其資源識別碼指定。</span><span class="sxs-lookup"><span data-stu-id="9f211-244">The Wizard97-style wizard has both watermark and header graphics, specified by their resource IDs.</span></span> <span data-ttu-id="9f211-245">*Ahpsp* 陣列包含所有 HPROPSHEETPAGE 控制碼，並定義其顯示的預設順序。</span><span class="sxs-lookup"><span data-stu-id="9f211-245">The *ahpsp* array contains all the HPROPSHEETPAGE handles and defines the default order in which they are displayed.</span></span>


```C++
// g_hInstance is the global HINSTANCE of the application.
// ahpsp is an array of HPROPSHEETPAGE handles.

PROPSHEETHEADER psh = { sizeof(psh) };

psh.hInstance      = g_hInstance;
psh.hwndParent     = NULL;
psh.phpage         = ahpsp;
psh.dwFlags        = PSH_WIZARD97 | PSH_WATERMARK | PSH_HEADER;
psh.pszbmWatermark = MAKEINTRESOURCE(IDB_WATERMARK);
psh.pszbmHeader    = MAKEINTRESOURCE(IDB_BANNER);
psh.nStartPage     = 0;
psh.nPages         = 4;

PropertySheet(&psh);
```



### <a name="the-dialog-box-procedure"></a><span data-ttu-id="9f211-246">對話方塊程式</span><span class="sxs-lookup"><span data-stu-id="9f211-246">The Dialog Box Procedure</span></span>

<span data-ttu-id="9f211-247">Wizard 的每一頁都需要一個對話方塊程式來處理 Windows 訊息，特別是來自其控制項和 wizard 的通知。</span><span class="sxs-lookup"><span data-stu-id="9f211-247">Each page of the wizard needs a dialog box procedure to process Windows messages, particularly notifications from its controls and the wizard.</span></span> <span data-ttu-id="9f211-248">幾乎所有嚮導都必須能夠處理的三個訊息為 [**wm \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog)、 [**wm \_ 摧毀**](/windows/desktop/winmsg/wm-destroy)和 [**wm \_ 通知**](wm-notify.md)。</span><span class="sxs-lookup"><span data-stu-id="9f211-248">The three messages that almost all wizards must be able to handle are [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog), [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy), and [**WM\_NOTIFY**](wm-notify.md).</span></span>

<span data-ttu-id="9f211-249">在顯示頁面之前，以及按一下任何 wizard 按鈕時，會收到 [**WM \_ 通知**](wm-notify.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="9f211-249">The [**WM\_NOTIFY**](wm-notify.md) message is received before the page is displayed and when any of the wizard's buttons are clicked.</span></span> <span data-ttu-id="9f211-250">訊息的 *lParam* 參數是指向 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) 標頭結構的指標。</span><span class="sxs-lookup"><span data-stu-id="9f211-250">The *lParam* parameter of the message is a pointer to a [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) header structure.</span></span> <span data-ttu-id="9f211-251">通知的識別碼包含在結構的程式 **代碼** 成員中。</span><span class="sxs-lookup"><span data-stu-id="9f211-251">The notification's ID is contained in the structure's **code** member.</span></span> <span data-ttu-id="9f211-252">大部分的嚮導需要處理的這四個通知如下。</span><span class="sxs-lookup"><span data-stu-id="9f211-252">The four notifications that most wizards need to handle are the following.</span></span>



| <span data-ttu-id="9f211-253">程式碼</span><span class="sxs-lookup"><span data-stu-id="9f211-253">Code</span></span>                                | <span data-ttu-id="9f211-254">描述</span><span class="sxs-lookup"><span data-stu-id="9f211-254">Description</span></span>                                 |
|-------------------------------------|---------------------------------------------|
| [<span data-ttu-id="9f211-255">PSN \_ ADVANCED.FIELD.SETACTIVE</span><span class="sxs-lookup"><span data-stu-id="9f211-255">PSN\_SETACTIVE</span></span>](psn-setactive.md) | <span data-ttu-id="9f211-256">在頁面顯示前傳送。</span><span class="sxs-lookup"><span data-stu-id="9f211-256">Sent before the page is displayed.</span></span>          |
| [<span data-ttu-id="9f211-257">PSN \_ WIZBACK</span><span class="sxs-lookup"><span data-stu-id="9f211-257">PSN\_WIZBACK</span></span>](psn-wizback.md)     | <span data-ttu-id="9f211-258">按一下 [ **上一頁** ] 按鈕時傳送。</span><span class="sxs-lookup"><span data-stu-id="9f211-258">Sent when the **Back** button is clicked.</span></span>   |
| [<span data-ttu-id="9f211-259">PSN \_ WIZNEXT</span><span class="sxs-lookup"><span data-stu-id="9f211-259">PSN\_WIZNEXT</span></span>](psn-wiznext.md)     | <span data-ttu-id="9f211-260">按一下 [ **下一步]** 按鈕時傳送。</span><span class="sxs-lookup"><span data-stu-id="9f211-260">Sent when the **Next** button is clicked.</span></span>   |
| [<span data-ttu-id="9f211-261">PSN \_ WIZFINISH</span><span class="sxs-lookup"><span data-stu-id="9f211-261">PSN\_WIZFINISH</span></span>](psn-wizfinish.md) | <span data-ttu-id="9f211-262">按一下 [ **完成]** 按鈕時傳送。</span><span class="sxs-lookup"><span data-stu-id="9f211-262">Sent when the **Finish** button is clicked.</span></span> |



 

### <a name="handle-wm_initdialog-and-wm_destroy"></a><span data-ttu-id="9f211-263">處理 WM \_ INITDIALOG 和 wm 損 \_ 毀</span><span class="sxs-lookup"><span data-stu-id="9f211-263">Handle WM\_INITDIALOG and WM\_DESTROY</span></span>

<span data-ttu-id="9f211-264">第一次顯示頁面時，其對話方塊程式會收到 [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) 訊息。</span><span class="sxs-lookup"><span data-stu-id="9f211-264">When a page is about to be displayed for the first time, its dialog box procedure receives a [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) message.</span></span> <span data-ttu-id="9f211-265">處理此訊息可讓 wizard 進行任何必要的初始化工作，例如儲存自訂資料或設定字型。</span><span class="sxs-lookup"><span data-stu-id="9f211-265">Handling this message allows the wizard to do any needed initialization tasks, such as storing custom data or setting fonts.</span></span>

<span data-ttu-id="9f211-266">當屬性工作表已損毀時，您會收到 [**WM 損 \_ 毀**](/windows/desktop/winmsg/wm-destroy) 訊息。</span><span class="sxs-lookup"><span data-stu-id="9f211-266">When the property sheet is destroyed, you receive a [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span> <span data-ttu-id="9f211-267">系統會自動終結嚮導，但處理此訊息可讓您進行任何必要的清除。</span><span class="sxs-lookup"><span data-stu-id="9f211-267">The wizard is automatically destroyed by the system, but handling this message allows you to do any needed cleanup.</span></span>

### <a name="handle-psn_setactive"></a><span data-ttu-id="9f211-268">處理 PSN \_ advanced.field.setactive</span><span class="sxs-lookup"><span data-stu-id="9f211-268">Handle PSN\_SETACTIVE</span></span>

<span data-ttu-id="9f211-269">每次顯示頁面時，都會傳送 [PSN \_ advanced.field.setactive](psn-setactive.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="9f211-269">The [PSN\_SETACTIVE](psn-setactive.md) notification code is sent each time a page is about to be made visible.</span></span> <span data-ttu-id="9f211-270">第一次造訪網頁時，PSN \_ advanced.field.setactive 會遵循 [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) 訊息。</span><span class="sxs-lookup"><span data-stu-id="9f211-270">The first time a page is visited, PSN\_SETACTIVE follows the [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) message.</span></span> <span data-ttu-id="9f211-271">如果後續正在使用頁面，它只會收到 PSN \_ advanced.field.setactive 通知。</span><span class="sxs-lookup"><span data-stu-id="9f211-271">If the page is subsequently revisited, it receives only a PSN\_SETACTIVE notification.</span></span> <span data-ttu-id="9f211-272">這項通知通常是用來初始化頁面的資料，並啟用適當的按鈕。</span><span class="sxs-lookup"><span data-stu-id="9f211-272">This notification is usually handled to initialize data for the page and enable the appropriate buttons.</span></span>

<span data-ttu-id="9f211-273">根據預設，嚮導會顯示[上一頁 **]、[下一頁] 和 [\*\*\*\*取消**] 按鈕，並啟用所有按鈕。</span><span class="sxs-lookup"><span data-stu-id="9f211-273">By default, the wizard displays **Back**, **Next**, and **Cancel** buttons, with all buttons enabled.</span></span> <span data-ttu-id="9f211-274">若要停用按鈕或顯示 **[完成** ] 而不是 **[下一步**]，您必須傳送 [**PSM \_ SETWIZBUTTONS**](psm-setwizbuttons.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="9f211-274">To disable a button or display **Finish** instead of **Next**, you must send a [**PSM\_SETWIZBUTTONS**](psm-setwizbuttons.md) message.</span></span> <span data-ttu-id="9f211-275">傳送此訊息之後，按鈕的狀態會一直保留到另一個 **PSM \_ SETWIZBUTTONS** 訊息修改後，即使已選取新的頁面。</span><span class="sxs-lookup"><span data-stu-id="9f211-275">After this message has been sent, the state of the buttons is preserved until it is modified by another **PSM\_SETWIZBUTTONS** message, even if a new page is selected.</span></span> <span data-ttu-id="9f211-276">一般而言，所有 [PSN \_ advanced.field.setactive](psn-setactive.md) 處理常式都會傳送此訊息，以確保每個頁面都有正確的按鈕狀態。</span><span class="sxs-lookup"><span data-stu-id="9f211-276">Typically, all [PSN\_SETACTIVE](psn-setactive.md) handlers send this message to ensure that each page has the correct button state.</span></span>

<span data-ttu-id="9f211-277">您可以隨時變更此訊息的按鈕狀態。</span><span class="sxs-lookup"><span data-stu-id="9f211-277">You can change the button state with this message at any time.</span></span> <span data-ttu-id="9f211-278">例如，您可能想要一開始停用 [ **下一步]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="9f211-278">For example, you may want the **Next** button to be initially disabled.</span></span> <span data-ttu-id="9f211-279">在使用者輸入所有必要的資訊之後，您可以傳送其他的 [**PSM \_ SETWIZBUTTONS**](psm-setwizbuttons.md) 訊息來啟用 [ **下一步]** 按鈕，並讓使用者繼續前往下一個頁面。</span><span class="sxs-lookup"><span data-stu-id="9f211-279">After a user has entered all the necessary information, you can send another [**PSM\_SETWIZBUTTONS**](psm-setwizbuttons.md) message to enable the **Next** button and let the user proceed to the next page.</span></span>

<span data-ttu-id="9f211-280">下列程式碼片段會使用 [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) 宏來啟用內部頁面上的 [ **上一頁** **] 和 [下一頁]** 按鈕，然後再顯示它。</span><span class="sxs-lookup"><span data-stu-id="9f211-280">The following code fragment uses the [**PropSheet\_SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) macro to enable the **Back** and **Next** buttons on an interior page before it is displayed.</span></span>


```C++
case WM_NOTIFY :
    {
        LPNMHDR pnmh = (LPNMHDR)lParam;
        
        switch(pnmh->code)
        {
        
        ...
        
        case PSN_SETACTIVE :
        
            ...
            
            // This is an interior page.
            PropSheet_SetWizButtons(hwnd, PSWIZB_NEXT | PSWIZB_BACK);
            
            ...
        }
    ...
    
    }
```



### <a name="handle-psn_wiznext-psnwizback-and-psn_wizfinish"></a><span data-ttu-id="9f211-281">處理 PSN \_ WIZNEXT、PSNWIZBACK 和 PSN \_ WIZFINISH</span><span class="sxs-lookup"><span data-stu-id="9f211-281">Handle PSN\_WIZNEXT, PSNWIZBACK, and PSN\_WIZFINISH</span></span>

<span data-ttu-id="9f211-282">按一下 **[下一步] 或 [** **上一頁** ] 按鈕時，您會收到 [PSN \_ WIZNEXT](psn-wiznext.md) 或 [PSN \_ WIZBACK](psn-wizback.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="9f211-282">When a **Next** or **Back** button is clicked, you receive a [PSN\_WIZNEXT](psn-wiznext.md) or [PSN\_WIZBACK](psn-wizback.md) notification code.</span></span> <span data-ttu-id="9f211-283">根據預設，嚮導會依照建立屬性工作表時所定義的順序，自動移至下一個或前一個頁面。</span><span class="sxs-lookup"><span data-stu-id="9f211-283">By default, the wizard automatically goes to either the next or previous page in the order that is defined when the property sheet is created.</span></span> <span data-ttu-id="9f211-284">處理這些通知的常見原因是防止使用者切換頁面，或覆寫預設的頁面順序。</span><span class="sxs-lookup"><span data-stu-id="9f211-284">A common reason to handle these notifications is to prevent the user from switching pages, or to override the default page order.</span></span>

<span data-ttu-id="9f211-285">若要防止使用者切換頁面，請處理按鈕通知、呼叫 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函式，並將 DWL \_ MSGRESULT 值設定為–1，並傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="9f211-285">To prevent the user from switching pages, handle the button notification, call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value set to –1, and return **TRUE**.</span></span> <span data-ttu-id="9f211-286">例如：</span><span class="sxs-lookup"><span data-stu-id="9f211-286">For example:</span></span>


```C++
case PSN_WIZNEXT :

        ...
        
        // Do not go to the next page yet.
        SetWindowLong(hwnd, DWL_MSGRESULT, -1);
        
        return TRUE;
        
        ...
```



<span data-ttu-id="9f211-287">若要覆寫標準順序並移至特定頁面，請呼叫 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) ，並將 DWL \_ MSGRESULT 值設定為頁面的對話方塊資源識別碼，並傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="9f211-287">To override the standard order and go to a particular page, call [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) with the DWL\_MSGRESULT value set to the page's dialog box resource ID, and return **TRUE**.</span></span> <span data-ttu-id="9f211-288">例如：</span><span class="sxs-lookup"><span data-stu-id="9f211-288">For example:</span></span>


```C++
case PSN_WIZNEXT :

        ...
        
        // Go straight to the completion page.
        SetWindowLong(hwnd, DWL_MSGRESULT, IDD_FINISH);
        
        return TRUE;
        
        ...
```



<span data-ttu-id="9f211-289">按一下 [ **完成]** 或 [ **取消** ] 按鈕時，您會分別收到 [PSN \_ WIZFINISH](psn-wizfinish.md) 或 [PSN \_ 重設](psn-reset.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="9f211-289">When the **Finish** or **Cancel** button is clicked, you receive a [PSN\_WIZFINISH](psn-wizfinish.md) or [PSN\_RESET](psn-reset.md) notification code, respectively.</span></span> <span data-ttu-id="9f211-290">當您按一下其中一個按鈕時，系統就會自動終結 wizard。</span><span class="sxs-lookup"><span data-stu-id="9f211-290">When either of these buttons is clicked, the wizard is automatically destroyed by the system.</span></span> <span data-ttu-id="9f211-291">但是，如果您需要在嚮導終結之前執行清除工作，則可以處理這些通知。</span><span class="sxs-lookup"><span data-stu-id="9f211-291">However, you can handle these notifications if you need to perform cleanup tasks before the wizard is destroyed.</span></span> <span data-ttu-id="9f211-292">若要防止在您收到 PSN WIZFINISH 通知時無法終結嚮導 \_ ，請呼叫 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) ，並將 DWL \_ MSGRESULT 值設定為 **true**，並傳回 **true**。</span><span class="sxs-lookup"><span data-stu-id="9f211-292">To prevent the wizard from being destroyed when you receive a PSN\_WIZFINISH notification, call [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) with the DWL\_MSGRESULT value set to **TRUE**, and return **TRUE**.</span></span> <span data-ttu-id="9f211-293">例如：</span><span class="sxs-lookup"><span data-stu-id="9f211-293">For example:</span></span>


```C++
case PSN_WIZFINISH :

        ...
        
        // Not finished yet.
        SetWindowLong(hwnd, DWL_MSGRESULT, TRUE);
        
        return TRUE;
        
        ...
```



### <a name="backward-compatible-wizards"></a><span data-ttu-id="9f211-294">回溯相容的嚮導</span><span class="sxs-lookup"><span data-stu-id="9f211-294">Backward Compatible Wizards</span></span>

<span data-ttu-id="9f211-295">上一節假設您正在為具有 [第5版](common-control-versions.md) 或更新版本之通用控制項的系統，執行嚮導。</span><span class="sxs-lookup"><span data-stu-id="9f211-295">The preceding section assumes that you are implementing a wizard for a system with [version 5](common-control-versions.md) or later of the common controls.</span></span>

<span data-ttu-id="9f211-296">如果您要為具有舊版通用控制項的系統撰寫嚮導，將無法使用上一節所討論的許多功能。</span><span class="sxs-lookup"><span data-stu-id="9f211-296">If you are writing a wizard for systems with earlier versions of the common controls, many of the features discussed in the preceding section will not be available.</span></span> <span data-ttu-id="9f211-297">只有通用控制項第5版和更新版本才支援 Wizard97 樣式所使用的 [**PROPSHEETHEADER**](pss-propsheetheader.md) 和 [**PROPSHEETPAGE**](pss-propsheetpage.md) 結構的一些成員。</span><span class="sxs-lookup"><span data-stu-id="9f211-297">A number of the members of the [**PROPSHEETHEADER**](pss-propsheetheader.md) and [**PROPSHEETPAGE**](pss-propsheetpage.md) structures that are used by the Wizard97 style are supported only by common controls version 5 and later.</span></span> <span data-ttu-id="9f211-298">不過，您仍然可以使用類似 Wizard97 樣式的外觀來執行回溯 *相容* 的 wizard。</span><span class="sxs-lookup"><span data-stu-id="9f211-298">However, it is still possible to implement a *backward compatible* wizard with an appearance similar to that of the Wizard97 style.</span></span> <span data-ttu-id="9f211-299">若要這樣做，您必須明確地執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="9f211-299">To do so, you must explicitly implement the following:</span></span>

-   <span data-ttu-id="9f211-300">將浮水印圖形新增至 [簡介] 和 [完成] 頁面的對話方塊範本。</span><span class="sxs-lookup"><span data-stu-id="9f211-300">Add the watermark graphic to the dialog box template for your introduction and completion pages.</span></span>
-   <span data-ttu-id="9f211-301">讓所有範本的大小都相同。</span><span class="sxs-lookup"><span data-stu-id="9f211-301">Make all your templates the same size.</span></span> <span data-ttu-id="9f211-302">內部頁面沒有個別的系統定義標頭區域。</span><span class="sxs-lookup"><span data-stu-id="9f211-302">There is no separate system-defined header area for interior pages.</span></span>
-   <span data-ttu-id="9f211-303">在您的範本上明確建立內部頁面的標頭區域。</span><span class="sxs-lookup"><span data-stu-id="9f211-303">Create the interior page's header area explicitly on your templates.</span></span>
-   <span data-ttu-id="9f211-304">請勿使用標頭圖形，因為如果 wizard 變更大小，它可能會與標題或子標題發生衝突。</span><span class="sxs-lookup"><span data-stu-id="9f211-304">Do not use a header graphic because it may conflict with the title or subtitle if the wizard changes size.</span></span>

<span data-ttu-id="9f211-305">如需回溯相容性檢查的進一步討論，請參閱回溯 [相容的 Wizard 97](/previous-versions//ms737910(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="9f211-305">For further discussion of backward-compatible wizards, see [Backward Compatible Wizard 97](/previous-versions//ms737910(v=vs.85)).</span></span>

## <a name="remarks"></a><span data-ttu-id="9f211-306">備註</span><span class="sxs-lookup"><span data-stu-id="9f211-306">Remarks</span></span>

<span data-ttu-id="9f211-307">如需 Wizard97 設計問題的完整討論，請參閱 Windows SDK 中其他位置的 [Wizard97 規格](/previous-versions//ms738248(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="9f211-307">For a complete discussion of design issues for Wizard97, see the [Wizard97 Specification](/previous-versions//ms738248(v=vs.85)), elsewhere in the Windows SDK.</span></span> <span data-ttu-id="9f211-308">本檔包含對話方塊的維度、點陣圖維度和色彩，以及控制項位置等專案的指導方針。</span><span class="sxs-lookup"><span data-stu-id="9f211-308">This document has guidelines for such things as the dimensions for the dialog boxes, bitmap dimensions and colors, and the placement of controls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f211-309">相關主題</span><span class="sxs-lookup"><span data-stu-id="9f211-309">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f211-310">使用屬性工作表</span><span class="sxs-lookup"><span data-stu-id="9f211-310">Using Property Sheets</span></span>](using-property-sheets.md)
</dt> <dt>

<span data-ttu-id="9f211-311">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="9f211-311">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 