---
description: 您可以針對檔案類型或專案註冊唯一的內容視圖屬性清單和版面配置模式。
ms.assetid: EA5A3ADA-4DFD-4F85-A176-93577D822815
title: 為檔案類型或專案註冊內容視圖集的屬性和版面配置模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e84861a0761f2f5ebb9737f62409c8f72e00bd
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/28/2021
ms.locfileid: "104321296"
---
# <a name="how-to-register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item"></a><span data-ttu-id="8b74d-103">如何註冊檔案類型或專案的唯一內容視圖集屬性和配置模式</span><span class="sxs-lookup"><span data-stu-id="8b74d-103">How to Register a Unique Content View Set of Properties and Layout Pattern for the File Type or Item</span></span>

<span data-ttu-id="8b74d-104">您可以針對檔案類型或專案註冊唯一的內容視圖屬性清單和版面配置模式。</span><span class="sxs-lookup"><span data-stu-id="8b74d-104">You can register a unique Content view property list and layout pattern for the file type or item.</span></span> <span data-ttu-id="8b74d-105">如果您的檔案類型或專案也與某個種類相關聯，則檔案類型或專案的特定內容視圖註冊將會覆寫種類註冊。</span><span class="sxs-lookup"><span data-stu-id="8b74d-105">If your file type or item is also associated with a Kind, the specific Content view registration of the file type or item will override the Kind registration.</span></span> <span data-ttu-id="8b74d-106">如果這個專案的最重要屬性與相同類型的其他專案不同，這可能會很有用。</span><span class="sxs-lookup"><span data-stu-id="8b74d-106">This might be useful if the most important properties for this item are different from other items of the same Kind.</span></span> <span data-ttu-id="8b74d-107">如果您沒有將檔案類型或專案與專案種類建立關聯，或直接註冊內容視圖，系統會使用預設的內容查看資訊 (儲存在所有專案的關聯陣列中最後一個元素所參考的登錄機碼中，HKEY \_ 類別 \_ 根目錄 \\ \*) </span><span class="sxs-lookup"><span data-stu-id="8b74d-107">If you do not associate your file type or item with an item Kind or directly register the Content view, the system uses the default Content view information (stored in a registry key referenced by the last element in all items' association array, HKEY\_CLASSES\_ROOT\\\*)</span></span>

<span data-ttu-id="8b74d-108">註冊檔案類型的自訂屬性清單之前，您應該瞭解搜尋結果模式和瀏覽模式，以及您可以使用的版面配置模式。</span><span class="sxs-lookup"><span data-stu-id="8b74d-108">Before registering a custom property list for your file type, you should understand the Search Result mode and Browse mode, and the layout patterns that are available to you.</span></span>

## <a name="instructions"></a><span data-ttu-id="8b74d-109">指示</span><span class="sxs-lookup"><span data-stu-id="8b74d-109">Instructions</span></span>

### <a name="step-1-understanding-the-search-result-mode-and-browse-mode"></a><span data-ttu-id="8b74d-110">步驟1：瞭解搜尋結果模式和瀏覽模式</span><span class="sxs-lookup"><span data-stu-id="8b74d-110">Step 1: Understanding the Search Result Mode and Browse Mode</span></span>

<span data-ttu-id="8b74d-111">內容視圖需要為一組搜尋結果中的專案定義配置模式和屬性清單的屬性清單 (搜尋結果模式) ，以及流覽至 Shell 位置 (瀏覽模式) 。</span><span class="sxs-lookup"><span data-stu-id="8b74d-111">Content view requires defining a layout pattern and set of property lists for an item in a set of search results (Search result mode), and when browsing to a Shell location (Browse mode).</span></span> <span data-ttu-id="8b74d-112">您可以使用相同的值來搜尋結果和流覽 `Kind.Music` 。</span><span class="sxs-lookup"><span data-stu-id="8b74d-112">You can use the same values for Search result and Browse, as `Kind.Music` does.</span></span> <span data-ttu-id="8b74d-113">或者，您也可以定義不同的屬性清單和/或版面配置模式 `Kind.Document` 。</span><span class="sxs-lookup"><span data-stu-id="8b74d-113">Alternatively, you can define a different property list and/or layout pattern as `Kind.Document` does.</span></span>

<span data-ttu-id="8b74d-114">在的案例中 `Kind.Document` ，使用者通常會在檔的文字中搜尋文字。</span><span class="sxs-lookup"><span data-stu-id="8b74d-114">In the case of `Kind.Document`, users often search for words in the text of the document.</span></span> <span data-ttu-id="8b74d-115">因此，在搜尋結果中包含更多範例文字，可能是最好的選擇。</span><span class="sxs-lookup"><span data-stu-id="8b74d-115">Therefore, including more sample text in the search result might be the best choice.</span></span> <span data-ttu-id="8b74d-116">下列範例說明的流覽內容視圖 `Kind.Document` 。</span><span class="sxs-lookup"><span data-stu-id="8b74d-116">The following example illustrates the Browse Content view of `Kind.Document`.</span></span>

![流覽 kind.doc>ument 的內容視圖](images/content-view/browsecontentviewkinddocument.png)

<span data-ttu-id="8b74d-118">由於使用者很少會在流覽檔時搜尋特定文字，因此優化您所選擇的屬性和版面配置以在螢幕上容納更多搜尋結果，可能是最佳選擇。</span><span class="sxs-lookup"><span data-stu-id="8b74d-118">Because users are rarely looking for particular text when browsing for documents, optimizing your choice of properties and layout to fit more search results on the screen might be the best choice.</span></span> <span data-ttu-id="8b74d-119">下列螢幕擷取畫面說明的搜尋內容視圖 `Kind.Document` 。</span><span class="sxs-lookup"><span data-stu-id="8b74d-119">The following screen shot illustrates the Search Content view of `Kind.Document`.</span></span>

### <a name="step-2-understanding-layout-patterns"></a><span data-ttu-id="8b74d-120">步驟2：瞭解版面配置模式</span><span class="sxs-lookup"><span data-stu-id="8b74d-120">Step 2: Understanding Layout Patterns</span></span>

<span data-ttu-id="8b74d-121">有四種配置模式： Alpha、Beta、Gamma 和 Delta。</span><span class="sxs-lookup"><span data-stu-id="8b74d-121">There are four layout patterns: Alpha, Beta, Gamma, and Delta.</span></span>

<span data-ttu-id="8b74d-122">**Alpha 版面配置**</span><span class="sxs-lookup"><span data-stu-id="8b74d-122">**Alpha layout**</span></span>

<span data-ttu-id="8b74d-123">Alpha 配置模式最適合用於包含摘錄的檔搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="8b74d-123">The Alpha layout pattern is optimized for document search results that contain excerpts.</span></span> <span data-ttu-id="8b74d-124">它具有下列規格：</span><span class="sxs-lookup"><span data-stu-id="8b74d-124">It has the following specifications:</span></span>

-   <span data-ttu-id="8b74d-125">資料列：4</span><span class="sxs-lookup"><span data-stu-id="8b74d-125">Rows: 4</span></span>
-   <span data-ttu-id="8b74d-126">屬性：7</span><span class="sxs-lookup"><span data-stu-id="8b74d-126">Properties: 7</span></span>
-   <span data-ttu-id="8b74d-127">當專案具有350圖元或更多水準空間時的 Alpha 配置，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="8b74d-127">Alpha layout when the item has 350 pixels or more of horizontal space, as shown in the following illustration.</span></span>

    ![Alpha 版面配置模式](images/content-view/layout1.png)

-   <span data-ttu-id="8b74d-129">下圖顯示當專案具有350圖元或更多水準空間時的 Alpha 版面配置。</span><span class="sxs-lookup"><span data-stu-id="8b74d-129">The following illustration shows the Alpha layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![顯示 Alpha 版面配置範例的圖表](images/content-view/alphaviewmore.png)

-   <span data-ttu-id="8b74d-131">下圖顯示當專案的水準空間小於350圖元時的 Alpha 版面配置。</span><span class="sxs-lookup"><span data-stu-id="8b74d-131">The following illustration shows the Alpha layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![顯示 Microsoft Word 中 Alpha 版面配置範例的螢幕擷取畫面。](images/content-view/layout2.png)

-   <span data-ttu-id="8b74d-133">下圖顯示當專案的水準空間小於350圖元時的 Alpha 版面配置。</span><span class="sxs-lookup"><span data-stu-id="8b74d-133">The following illustration shows the Alpha layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![Alpha 版面配置範例](images/content-view/alphaviewless.png)

<span data-ttu-id="8b74d-135">**Beta 版面配置**</span><span class="sxs-lookup"><span data-stu-id="8b74d-135">**Beta Layout**</span></span>

<span data-ttu-id="8b74d-136">Beta 版面配置模式已針對包含摘錄的電子郵件檔搜尋結果進行優化。</span><span class="sxs-lookup"><span data-stu-id="8b74d-136">The Beta layout pattern is optimized for email document search results that contain excerpts.</span></span> <span data-ttu-id="8b74d-137">它具有下列規格：</span><span class="sxs-lookup"><span data-stu-id="8b74d-137">It has the following specifications:</span></span>

-   <span data-ttu-id="8b74d-138">資料列：4</span><span class="sxs-lookup"><span data-stu-id="8b74d-138">Rows: 4</span></span>
-   <span data-ttu-id="8b74d-139">屬性：5</span><span class="sxs-lookup"><span data-stu-id="8b74d-139">Properties: 5</span></span>
-   <span data-ttu-id="8b74d-140">當專案具有350圖元或更多水準空間時的 Beta 版面配置，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="8b74d-140">Beta layout when the item has 350 pixels or more of horizontal space, as shown in the following illustration.</span></span>

    ![顯示 Beta 版面配置範例的圖表。](images/content-view/layout3.png)

-   <span data-ttu-id="8b74d-142">下圖顯示當專案具有350圖元或更多水準空間時的 Beta 版面配置。</span><span class="sxs-lookup"><span data-stu-id="8b74d-142">The following illustration shows the beta layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![顯示電子郵件 Beta 版面配置範例的螢幕擷取畫面。](images/content-view/betaviewmore.png)

-   <span data-ttu-id="8b74d-144">下圖顯示當專案的水準空間小於350圖元時的 Beta 版面配置。</span><span class="sxs-lookup"><span data-stu-id="8b74d-144">The following illustration shows the Beta layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![顯示 Beta 版面配置範例的圖表，其水準空間小於350圖元。](images/content-view/layout4.png)

-   <span data-ttu-id="8b74d-146">下圖顯示當專案的水準空間小於350圖元時的 Beta 版面配置：</span><span class="sxs-lookup"><span data-stu-id="8b74d-146">The following illustration shows the beta layout when the item has less than 350 pixels of horizontal space:</span></span>

    ![Beta 版面配置範例](images/content-view/betaviewless.png)

<span data-ttu-id="8b74d-148">**Gamma 版面配置**</span><span class="sxs-lookup"><span data-stu-id="8b74d-148">**Gamma Layout**</span></span>

<span data-ttu-id="8b74d-149">Gamma 配置模式類似于 Alpha，但會使用兩行配置，而不是四個線條的版面配置。</span><span class="sxs-lookup"><span data-stu-id="8b74d-149">The Gamma layout pattern is similar to Alpha but uses a two-line layout instead of four.</span></span> <span data-ttu-id="8b74d-150">如果您想要查看程式碼片段，但想要在螢幕上容納更多專案，或針對需要較少空間來顯示最重要資訊的檔案類型，則這種版面配置很適合。</span><span class="sxs-lookup"><span data-stu-id="8b74d-150">This layout is ideal for scenarios in which you want to see a snippet but want to fit more items on the screen, or for file types that require less space to show the most critical information.</span></span> <span data-ttu-id="8b74d-151">Gamma 版面配置具有下列規格：</span><span class="sxs-lookup"><span data-stu-id="8b74d-151">The Gamma layout has the following specifications:</span></span>

-   <span data-ttu-id="8b74d-152">資料列：2</span><span class="sxs-lookup"><span data-stu-id="8b74d-152">Rows: 2</span></span>
-   <span data-ttu-id="8b74d-153">屬性：4</span><span class="sxs-lookup"><span data-stu-id="8b74d-153">Properties: 4</span></span>
-   <span data-ttu-id="8b74d-154">下圖顯示當專案具有350圖元或更多水準空間時的 gamma 版面配置。</span><span class="sxs-lookup"><span data-stu-id="8b74d-154">The following illustration shows the gamma layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![顯示 gamma 版面配置範例的圖表。](images/content-view/layout5.png)

-   <span data-ttu-id="8b74d-156">下圖顯示當專案具有350圖元或更多水準空間時的 gamma 版面配置。</span><span class="sxs-lookup"><span data-stu-id="8b74d-156">The following illustration shows the gamma layout when the item has 350 pixels or more of horizontal space.</span></span>

    ![顯示檢查清單專案之 gamma 版面配置範例的螢幕擷取畫面。](images/content-view/gammaviewmore.png)

-   <span data-ttu-id="8b74d-158">下圖顯示當專案的水準空間小於350圖元時的 gamma 版面配置。</span><span class="sxs-lookup"><span data-stu-id="8b74d-158">The following illustration shows the gamma layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![顯示 gamma 版面配置範例的圖表，其水準空間小於350圖元。](images/content-view/layout6.png)

-   <span data-ttu-id="8b74d-160">當專案的水準空間小於350圖元時，gamma 配置的範例。</span><span class="sxs-lookup"><span data-stu-id="8b74d-160">Example of the gamma layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![gamma 版面配置範例](images/content-view/gammaviewless.png)

<span data-ttu-id="8b74d-162">**差異版面配置**</span><span class="sxs-lookup"><span data-stu-id="8b74d-162">**Delta Layout**</span></span>

<span data-ttu-id="8b74d-163">差異配置模式最適合用來顯示許多較短的屬性，例如音樂和圖片。</span><span class="sxs-lookup"><span data-stu-id="8b74d-163">The Delta layout pattern is optimized for displaying many shorter properties such as for music and pictures.</span></span> <span data-ttu-id="8b74d-164">它具有下列規格：</span><span class="sxs-lookup"><span data-stu-id="8b74d-164">It has the following specifications:</span></span>

-   <span data-ttu-id="8b74d-165">資料列：2</span><span class="sxs-lookup"><span data-stu-id="8b74d-165">Rows: 2</span></span>
-   <span data-ttu-id="8b74d-166">屬性：6</span><span class="sxs-lookup"><span data-stu-id="8b74d-166">Properties: 6</span></span>
-   <span data-ttu-id="8b74d-167">當專案具有700圖元或更多水準空間時的差異版面配置，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="8b74d-167">Delta layout when the item has 700 pixels or more of horizontal space, as shown in the following illustration.</span></span>

    ![顯示差異版面配置範例的圖表。](images/content-view/layout7.png)

-   <span data-ttu-id="8b74d-169">當專案具有700圖元或更多水準空間時的差異版面配置範例。</span><span class="sxs-lookup"><span data-stu-id="8b74d-169">Example of the delta layout when the item has 700 pixels or more of horizontal space.</span></span>

    ![顯示音樂檔案差異版面配置範例的螢幕擷取畫面。](images/content-view/deltalayoutmore.png)

-   <span data-ttu-id="8b74d-171">當專案在水準空間的350到700圖元之間時，差異版面配置。</span><span class="sxs-lookup"><span data-stu-id="8b74d-171">Delta layout when the item has between 350 and 700 pixels of horizontal space.</span></span>

    ![顯示差異版面配置範例的圖表，其水準空間的350和700圖元之間。](images/content-view/layout8.png)

-   <span data-ttu-id="8b74d-173">當專案在水準空間的350和700圖元之間時，差異版面配置的範例。</span><span class="sxs-lookup"><span data-stu-id="8b74d-173">Example of the delta layout when the item has between 350 and 700 pixels of horizontal space.</span></span>

    ![差異版面配置範例](images/content-view/deltaviewbetween.png)

-   <span data-ttu-id="8b74d-175">當專案的水準空間小於350圖元時，則為差異版面配置。</span><span class="sxs-lookup"><span data-stu-id="8b74d-175">Delta layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![版面配置範例](images/content-view/layout9.png)

-   <span data-ttu-id="8b74d-177">當專案的水準空間小於350圖元時，差異版面配置的範例。</span><span class="sxs-lookup"><span data-stu-id="8b74d-177">Example of the delta layout when the item has less than 350 pixels of horizontal space.</span></span>

    ![螢幕擷取畫面，顯示在水準空間小於350圖元之音樂檔案的差異版面配置範例。](images/content-view/deltaviewless.png)

### <a name="step-3-registering-custom-properties-and-layout-for-your-file-type"></a><span data-ttu-id="8b74d-179">步驟3：註冊您的檔案類型的自訂屬性和版面配置</span><span class="sxs-lookup"><span data-stu-id="8b74d-179">Step 3: Registering Custom Properties and Layout for Your File Type</span></span>

<span data-ttu-id="8b74d-180">當您瞭解搜尋結果模式、瀏覽模式和版面配置模式之後，就可以為您的檔案類型註冊自訂屬性清單。</span><span class="sxs-lookup"><span data-stu-id="8b74d-180">After you understand the Search Result mode, the Browse mode, and the layout patterns, you can register a custom property list for your file type.</span></span>

<span data-ttu-id="8b74d-181">**註冊檔案類型的自訂屬性清單和配置模式。**</span><span class="sxs-lookup"><span data-stu-id="8b74d-181">**To register a custom property list and layout pattern for your file type.**</span></span>

1.  <span data-ttu-id="8b74d-182">從四種版面配置模式中選擇： Alpha、Beta、Gamma 或 Delta。</span><span class="sxs-lookup"><span data-stu-id="8b74d-182">Choose from the four layout patterns: Alpha, Beta, Gamma, or Delta.</span></span>
2.  <span data-ttu-id="8b74d-183">請考慮下列格式化規則，這同樣適用于全部四種版面配置模式：</span><span class="sxs-lookup"><span data-stu-id="8b74d-183">Consider the following formatting rules, which apply equally to all four layout patterns:</span></span>
    -   <span data-ttu-id="8b74d-184">屬性1一律會以較大的字型大小顯示。</span><span class="sxs-lookup"><span data-stu-id="8b74d-184">Property 1 is always displayed in a larger font size.</span></span> <span data-ttu-id="8b74d-185">大型字型大小通常用於專案名稱，但也可以用於錨點或其他專案屬性。</span><span class="sxs-lookup"><span data-stu-id="8b74d-185">The large font size usually used for the item name, but can also be used for the anchor or other item property.</span></span>
    -   <span data-ttu-id="8b74d-186">屬性4適用于 Alpha、Beta 和 Gamma 版面配置模式中的摘錄。</span><span class="sxs-lookup"><span data-stu-id="8b74d-186">Property 4 is intended for excerpts in the Alpha, Beta, and Gamma layout patterns.</span></span> <span data-ttu-id="8b74d-187">這個屬性會在這些模式中配置更多空間，並以灰色字型色彩顯示，而不像其他屬性一樣黑色，以協助它脫穎而出。</span><span class="sxs-lookup"><span data-stu-id="8b74d-187">This property is allotted more space in those patterns and is displayed in a gray font color, as opposed to black like the other properties, to help it stand out.</span></span>
    -   <span data-ttu-id="8b74d-188">下方的圖元測量是以相對圖元為單位，而大小則包含屬性左邊的圖示/縮圖，以及圖示/縮圖和選取矩形之間的間距。</span><span class="sxs-lookup"><span data-stu-id="8b74d-188">The pixel measurements below are in relative pixels, and the size includes the icon/thumbnail to the left of the properties and the space between the icon/thumbnail and the selection rectangle.</span></span>
    -   <span data-ttu-id="8b74d-189">大部分屬性都有最小的顯示大小。</span><span class="sxs-lookup"><span data-stu-id="8b74d-189">Most properties have a minimum display size.</span></span> <span data-ttu-id="8b74d-190">因此，如果沒有足夠的空間可供特定的視圖大小使用，它們就不會出現。</span><span class="sxs-lookup"><span data-stu-id="8b74d-190">Therefore, they will not appear if there is not enough space for them at a particular view size.</span></span> <span data-ttu-id="8b74d-191">大小下限通常是100圖元寬。</span><span class="sxs-lookup"><span data-stu-id="8b74d-191">The minimum size is usually 100 pixels wide.</span></span>
    -   <span data-ttu-id="8b74d-192">每個配置模式都會定義每個資料列中的資料列數目和屬性數目。</span><span class="sxs-lookup"><span data-stu-id="8b74d-192">Each layout pattern defines the number of rows and the number of properties in each row.</span></span>
3.  <span data-ttu-id="8b74d-193">決定您想要在版面配置中顯示哪些屬性，以及要在每個位置顯示哪個屬性。</span><span class="sxs-lookup"><span data-stu-id="8b74d-193">Decide which properties you want to display in the layout, and which property you want to display in each location.</span></span> <span data-ttu-id="8b74d-194">當您決定要在版面配置中的每個位置顯示哪一個屬性時，請考慮屬性的一般長度、對使用者的重要性，以及當視窗大小太小而無法包含所有屬性時是否應該卸載。</span><span class="sxs-lookup"><span data-stu-id="8b74d-194">When deciding which property to display in each position in the layout, consider the typical length of the property, its importance to the user, and whether it should be dropped when the window size is too small to contain all properties.</span></span>
4.  <span data-ttu-id="8b74d-195">為您的檔案類型或專案類型，在此範例中的檔案類型或專案 (的 ProgID 登錄機碼底下加入下列索引鍵，以註冊配置模式和屬性清單，) 的 [xyz] 檔案類型。</span><span class="sxs-lookup"><span data-stu-id="8b74d-195">Register a layout pattern and a property list for your file type or item type by adding the following keys under the ProgID registry key for the file type or item (in this example, for the .xyz file type).</span></span>

    ```
    HKEY_CLASSES_ROOT\*
       Contoso.xyzfile
          (ContentViewModeForBrowse) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeForSearch) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeLayoutPatternForBrowse) = <PropertyList>
          (ContentViewModeLayoutPatternForSearch) = <PropertyList>
    ```

5.  <span data-ttu-id="8b74d-196">請觀察下列用於註冊屬性的格式化指導方針：</span><span class="sxs-lookup"><span data-stu-id="8b74d-196">Observe the following formatting guidelines for registering properties:</span></span>

    -   <span data-ttu-id="8b74d-197">每個註冊的開頭為 `prop:`</span><span class="sxs-lookup"><span data-stu-id="8b74d-197">Each registration starts with `prop:`</span></span>
    -   <span data-ttu-id="8b74d-198">每個屬性都需要完整的屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="8b74d-198">Each property requires the full property name.</span></span>
    -   <span data-ttu-id="8b74d-199">屬性以分號分隔，而且沒有空格。</span><span class="sxs-lookup"><span data-stu-id="8b74d-199">Properties are separated by a semicolon with no space.</span></span>
    -   <span data-ttu-id="8b74d-200">屬性會依所選版面配置模式所定義的順序顯示。</span><span class="sxs-lookup"><span data-stu-id="8b74d-200">Properties are displayed in the order defined by the selected layout pattern.</span></span>
    -   <span data-ttu-id="8b74d-201">`~` 指出不應該顯示內容標籤。</span><span class="sxs-lookup"><span data-stu-id="8b74d-201">`~` indicates that the property label should not be displayed.</span></span>
    -   <span data-ttu-id="8b74d-202">`~System.LayoutPattern.PlaceHolder` 如果您想要將配置模式所指定的屬性保留空白，則應該使用。</span><span class="sxs-lookup"><span data-stu-id="8b74d-202">`~System.LayoutPattern.PlaceHolder` should be used if you want to leave blank a property that is specified in the layout pattern.</span></span>

    <span data-ttu-id="8b74d-203">下列範例登錄機碼說明這些格式設定指導方針。</span><span class="sxs-lookup"><span data-stu-id="8b74d-203">The following sample registry key illustrates these formatting guidelines.</span></span>

    ```
    HKEY_CLASSES_ROOT\
       Kind.Document
          (ContentViewModeForBrowse) = <PropertyList>
    ```

    <span data-ttu-id="8b74d-204"> (ContentViewModeForBrowse) 的可能值包括下列各項：： ~ System. ItemNameDisplay;System. Author;LayoutPattern。預留位置;System.string;System. DateModified;~ System. Size</span><span class="sxs-lookup"><span data-stu-id="8b74d-204">Possible values for (ContentViewModeForBrowse) include the following: prop:~System.ItemNameDisplay;System.Author;System.LayoutPattern.Placeholder;System.Keywords;System.DateModified; ~System.Size</span></span>

## <a name="remarks"></a><span data-ttu-id="8b74d-205">備註</span><span class="sxs-lookup"><span data-stu-id="8b74d-205">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b74d-206">相關主題</span><span class="sxs-lookup"><span data-stu-id="8b74d-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b74d-207">檔案類型</span><span class="sxs-lookup"><span data-stu-id="8b74d-207">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="8b74d-208">種類名稱</span><span class="sxs-lookup"><span data-stu-id="8b74d-208">Kind Names</span></span>](../properties/building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="8b74d-209">PropList. ContentViewModeForBrowse</span><span class="sxs-lookup"><span data-stu-id="8b74d-209">System.PropList.ContentViewModeForBrowse</span></span>](../properties/props-system-proplist-contentviewmodeforbrowse.md)
</dt> <dt>

[<span data-ttu-id="8b74d-210">PropList. ContentViewModeForSearch</span><span class="sxs-lookup"><span data-stu-id="8b74d-210">System.PropList.ContentViewModeForSearch</span></span>](../properties/props-system-proplist-contentviewmodeforsearch.md)
</dt> </dl>

 

 
