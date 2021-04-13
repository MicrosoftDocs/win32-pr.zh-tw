---
title: 一般對話
description: Microsoft Windows 通用對話方塊包含 [開啟檔案]、[儲存檔案]、[開啟資料夾]、[尋找和取代]、[列印]、[版面設定]、[字型] 和 [色彩] 對話方塊。
ms.assetid: 3f9fb0c9-bc1a-48c4-b021-99f155f8ea9e
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 336cb368fa25bf68313e2bf336de68845a87e663
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104386315"
---
# <a name="common-dialogs"></a><span data-ttu-id="a79ae-103">一般對話</span><span class="sxs-lookup"><span data-stu-id="a79ae-103">Common Dialogs</span></span>

> [!NOTE]
> <span data-ttu-id="a79ae-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="a79ae-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="a79ae-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="a79ae-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="a79ae-106">Microsoft Windows 通用對話方塊包含 [開啟檔案]、[儲存檔案]、[開啟資料夾]、[尋找和取代]、[列印]、[版面設定]、[字型] 和 [色彩] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a79ae-106">The Microsoft Windows common dialogs consist of the Open File, Save File, Open Folder, Find and Replace, Print, Page Setup, Font, and Color dialog boxes.</span></span>

## <a name="open-file"></a><span data-ttu-id="a79ae-107">開啟檔案</span><span class="sxs-lookup"><span data-stu-id="a79ae-107">Open File</span></span>

![<span data-ttu-id="a79ae-108">[開啟] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a79ae-108">screen shot of open dialog box</span></span> ](images/win-common-dlg-image1.png)

<span data-ttu-id="a79ae-109">開啟檔案已優化，可快速尋找要與程式搭配使用的專案。</span><span class="sxs-lookup"><span data-stu-id="a79ae-109">Open File is optimized for quickly finding items to use with a program.</span></span>

## <a name="save-file"></a><span data-ttu-id="a79ae-110">儲存檔案</span><span class="sxs-lookup"><span data-stu-id="a79ae-110">Save File</span></span>

![<span data-ttu-id="a79ae-111">[另存新檔] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a79ae-111">screen shot of save as dialog box</span></span> ](images/win-common-dlg-image2.png)

<span data-ttu-id="a79ae-112">儲存檔案會以其中繼資料儲存檔案來關閉迴圈。</span><span class="sxs-lookup"><span data-stu-id="a79ae-112">Save File closes the loop by saving a file with its metadata.</span></span>

## <a name="open-folder"></a><span data-ttu-id="a79ae-113">開啟資料夾</span><span class="sxs-lookup"><span data-stu-id="a79ae-113">Open Folder</span></span>

![<span data-ttu-id="a79ae-114">[流覽檔案/資料夾] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a79ae-114">screen shot of browse for files/folders dialog box</span></span> ](images/win-common-dlg-image3.png)

<span data-ttu-id="a79ae-115">[開啟資料夾] 專門用來選擇資料夾。</span><span class="sxs-lookup"><span data-stu-id="a79ae-115">Open Folder is specifically for choosing folders.</span></span>

## <a name="find-and-replace"></a><span data-ttu-id="a79ae-116">尋找和取代</span><span class="sxs-lookup"><span data-stu-id="a79ae-116">Find and replace</span></span>

![<span data-ttu-id="a79ae-117">[尋找和取代] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a79ae-117">screen shot of find and replace dialog boxes</span></span> ](images/win-common-dlg-image4.png)

<span data-ttu-id="a79ae-118">[尋找] 可讓使用者搜尋文字字串，而取代版本則可選擇性地讓使用者以另一個字串取代相符專案。</span><span class="sxs-lookup"><span data-stu-id="a79ae-118">Find allows users to search for text strings, whereas the Replace version optionally allows users to replace matches with another string.</span></span>

## <a name="print"></a><span data-ttu-id="a79ae-119">列印</span><span class="sxs-lookup"><span data-stu-id="a79ae-119">Print</span></span>

![<span data-ttu-id="a79ae-120">[列印] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a79ae-120">screen shot of print dialog box</span></span> ](images/win-common-dlg-image5.png)

<span data-ttu-id="a79ae-121">[列印] 可讓使用者選取要列印的內容、要列印的份數和定序順序，以及選擇和設定印表機的能力。</span><span class="sxs-lookup"><span data-stu-id="a79ae-121">Print allows users to select what to print, the number of copies to print, and the collation sequence, along with the ability to choose and configure printers.</span></span>

## <a name="page-setup"></a><span data-ttu-id="a79ae-122">版面設定</span><span class="sxs-lookup"><span data-stu-id="a79ae-122">Page setup</span></span>

![<span data-ttu-id="a79ae-123">[版面設定] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a79ae-123">screen shot of page setup dialog box</span></span> ](images/win-common-dlg-image6.png)

<span data-ttu-id="a79ae-124">頁面設定可讓使用者選取紙張大小和來源、頁面方向和邊界。</span><span class="sxs-lookup"><span data-stu-id="a79ae-124">Page setup allows users to select the paper size and source, page orientation, and margins.</span></span>

## <a name="font"></a><span data-ttu-id="a79ae-125">字型</span><span class="sxs-lookup"><span data-stu-id="a79ae-125">Font</span></span>

![<span data-ttu-id="a79ae-126">[字型] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a79ae-126">screen shot of font dialog box</span></span> ](images/win-common-dlg-image7.png)

<span data-ttu-id="a79ae-127">字型：顯示可用已安裝字型的字型和點大小。</span><span class="sxs-lookup"><span data-stu-id="a79ae-127">Font displays the fonts and point sizes of the available installed fonts.</span></span>

## <a name="color"></a><span data-ttu-id="a79ae-128">Color</span><span class="sxs-lookup"><span data-stu-id="a79ae-128">Color</span></span>

![<span data-ttu-id="a79ae-129">[編輯色彩] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a79ae-129">screen shot of edit colors dialog box</span></span> ](images/win-common-dlg-image8.png)

<span data-ttu-id="a79ae-130">色彩可讓使用者選取色彩，方法是透過一組預先定義的色彩，或選擇「自訂」的色彩。</span><span class="sxs-lookup"><span data-stu-id="a79ae-130">Color allows users to select a color, either through a predefined set of colors or by choosing a "custom" color.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="a79ae-131">設計概念</span><span class="sxs-lookup"><span data-stu-id="a79ae-131">Design concepts</span></span>

<span data-ttu-id="a79ae-132">藉由使用通用對話方塊，可讓使用者在不同的程式之間獲得一致的體驗。</span><span class="sxs-lookup"><span data-stu-id="a79ae-132">By using the common dialogs, you help give users a consistent experience across different programs.</span></span> <span data-ttu-id="a79ae-133">而且，藉由使用通用對話方塊，您也可以為使用者提供有效率、愉快的體驗。</span><span class="sxs-lookup"><span data-stu-id="a79ae-133">And by using the common dialogs well, you also help give users an efficient, enjoyable experience.</span></span>

<span data-ttu-id="a79ae-134">您可以選擇最適當的預設值，以大幅改善使用者對這些對話的體驗：</span><span class="sxs-lookup"><span data-stu-id="a79ae-134">You can significantly improve users' experience with these dialogs by choosing the most appropriate defaults for:</span></span>

-   <span data-ttu-id="a79ae-135">輸入值 (範例：預設資料夾、預設檔案名) 。</span><span class="sxs-lookup"><span data-stu-id="a79ae-135">Input values (examples: default folders, default file names).</span></span>
-   <span data-ttu-id="a79ae-136">選取的選項 (範例：選取的印表機、列印選項) 。</span><span class="sxs-lookup"><span data-stu-id="a79ae-136">Selected options (examples: selected printer, printing options).</span></span>
-   <span data-ttu-id="a79ae-137">Views (範例：在縮圖中顯示圖片、顯示沒有檔案名的圖片、依日期排序、資料行寬度) 。</span><span class="sxs-lookup"><span data-stu-id="a79ae-137">Views (examples: showing pictures in thumbnail view, showing pictures without file names, sorting by date, column widths).</span></span>
-   <span data-ttu-id="a79ae-138">展示 (範例： [視窗大小]、[位置] 和 [內容]) 。</span><span class="sxs-lookup"><span data-stu-id="a79ae-138">Presentation (examples: window size, location, and contents).</span></span>

<span data-ttu-id="a79ae-139">您必須決定初始預設值和後續的預設值。</span><span class="sxs-lookup"><span data-stu-id="a79ae-139">You must determine both the initial defaults and subsequent defaults.</span></span> <span data-ttu-id="a79ae-140">初始預設值取決於您的程式，以及根據目標使用者的預期使用方式，而後續預設值則是以實際的使用量為基礎。</span><span class="sxs-lookup"><span data-stu-id="a79ae-140">Initial default values are determined by your program and based on the target user's expected usage, whereas subsequent defaults are based on the actual usage.</span></span> <span data-ttu-id="a79ae-141">過去的使用量是未來使用的最佳指標。</span><span class="sxs-lookup"><span data-stu-id="a79ae-141">Past usage is the best indicator of future usage.</span></span>

<span data-ttu-id="a79ae-142">您的程式預設值是否有效？</span><span class="sxs-lookup"><span data-stu-id="a79ae-142">Are your program's defaults efficient?</span></span> <span data-ttu-id="a79ae-143">監視使用者執行最常見工作所需執行的步驟數目。</span><span class="sxs-lookup"><span data-stu-id="a79ae-143">Monitor the number of steps users have to take to perform the most common tasks.</span></span> <span data-ttu-id="a79ae-144">如果使用者在每次執行工作時都必須重複相同的可能不必要步驟，則可以改善您的預設值。</span><span class="sxs-lookup"><span data-stu-id="a79ae-144">If users have to repeat the same, potentially unnecessary steps every time they perform a task, your default values can be improved.</span></span>

<span data-ttu-id="a79ae-145">**如果您只做一件事 .。。**</span><span class="sxs-lookup"><span data-stu-id="a79ae-145">**If you do only one thing...**</span></span>

<span data-ttu-id="a79ae-146">選取適當的初始和後續預設值，為使用者提供有效率、愉快的體驗。</span><span class="sxs-lookup"><span data-stu-id="a79ae-146">Give users an efficient, enjoyable experience by selecting appropriate initial and subsequent defaults.</span></span>

## <a name="is-this-the-right-user-interface"></a><span data-ttu-id="a79ae-147">這是正確的使用者介面嗎？</span><span class="sxs-lookup"><span data-stu-id="a79ae-147">Is this the right user interface?</span></span>

<span data-ttu-id="a79ae-148">**是的！使用通用對話方塊可獲得一致的使用者體驗。請勿建立您自己的。**</span><span class="sxs-lookup"><span data-stu-id="a79ae-148">**Yes! Use the common dialogs for a consistent user experience. Don't create your own.**</span></span> <span data-ttu-id="a79ae-149">建立可正確且安全地流覽命名空間的自訂 Ui，會更加困難。</span><span class="sxs-lookup"><span data-stu-id="a79ae-149">It is especially difficult to create custom UIs that navigate the namespace correctly and securely.</span></span> <span data-ttu-id="a79ae-150">請注意，您可以視需要自訂通用對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a79ae-150">Note that you can customize the common dialogs if necessary.</span></span>

<span data-ttu-id="a79ae-151">在 Windows Vista 中，開啟的檔案和儲存檔案具有新的可擴充架構，可讓您更輕鬆地公開其他功能。</span><span class="sxs-lookup"><span data-stu-id="a79ae-151">For Windows Vista, the Open File and Save File have a new extensible architecture to make it easier to expose additional functionality.</span></span> <span data-ttu-id="a79ae-152">這項機制有足夠的彈性，可符合主要獨立軟體廠商 (Isv) 的最低需求，但不會被未來的 Windows 版本所打破。</span><span class="sxs-lookup"><span data-stu-id="a79ae-152">This mechanism is flexible enough to meet the minimum requirements of major independent software vendors (ISVs), but not be broken by future releases of Windows.</span></span>

## <a name="guidelines"></a><span data-ttu-id="a79ae-153">指導方針</span><span class="sxs-lookup"><span data-stu-id="a79ae-153">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="a79ae-154">一般</span><span class="sxs-lookup"><span data-stu-id="a79ae-154">General</span></span>

-   <span data-ttu-id="a79ae-155">適當時，請提供更多 [直接或非強制回應的替代](glossary.md) 方案。</span><span class="sxs-lookup"><span data-stu-id="a79ae-155">When appropriate, provide more direct or [modeless](glossary.md) alternatives.</span></span> <span data-ttu-id="a79ae-156">允許使用者：</span><span class="sxs-lookup"><span data-stu-id="a79ae-156">Allow users to:</span></span>
    -   <span data-ttu-id="a79ae-157">將檔案放在您的程式上以開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="a79ae-157">Open files by dropping them on your program.</span></span>
    -   <span data-ttu-id="a79ae-158">使用 [儲存] 命令，以目前的名稱和位置儲存檔案。</span><span class="sxs-lookup"><span data-stu-id="a79ae-158">Save files using their current name and location with a Save command.</span></span>
    -   <span data-ttu-id="a79ae-159">使用 F3 鍵找出下一個出現的字串。</span><span class="sxs-lookup"><span data-stu-id="a79ae-159">Find the next occurrence of a string using the F3 key.</span></span>
    -   <span data-ttu-id="a79ae-160">使用列印命令，將整份檔的一份複本列印到預設印表機。</span><span class="sxs-lookup"><span data-stu-id="a79ae-160">Print one copy of an entire document to the default printer with a Print command.</span></span>
    -   <span data-ttu-id="a79ae-161">使用工具列或調色盤視窗變更字型和字型屬性。</span><span class="sxs-lookup"><span data-stu-id="a79ae-161">Change fonts and font attributes using a toolbar or palette window.</span></span>
    -   <span data-ttu-id="a79ae-162">使用工具列或調色盤視窗變更色彩。</span><span class="sxs-lookup"><span data-stu-id="a79ae-162">Change colors using a toolbar or palette window.</span></span>
-   <span data-ttu-id="a79ae-163">使用下列命令來顯示 (指定的通用對話方塊，以及其慣用的 [存取金鑰](glossary.md)) ：</span><span class="sxs-lookup"><span data-stu-id="a79ae-163">Use the following commands to display common dialogs (given along with their preferred [access keys](glossary.md)):</span></span>



|                              |                                               |
|------------------------------|-----------------------------------------------|
| <span data-ttu-id="a79ae-164">**通用對話方塊**</span><span class="sxs-lookup"><span data-stu-id="a79ae-164">**Common dialog**</span></span><br/> | <span data-ttu-id="a79ae-165">**命令**</span><span class="sxs-lookup"><span data-stu-id="a79ae-165">**Command**</span></span><br/>                        |
| <span data-ttu-id="a79ae-166">開啟檔案</span><span class="sxs-lookup"><span data-stu-id="a79ae-166">Open File</span></span><br/>         | <span data-ttu-id="a79ae-167">開啟...</span><span class="sxs-lookup"><span data-stu-id="a79ae-167">Open...</span></span><br/>                            |
| <span data-ttu-id="a79ae-168">儲存檔案</span><span class="sxs-lookup"><span data-stu-id="a79ae-168">Save File</span></span><br/>         | <span data-ttu-id="a79ae-169">另存新檔 .。。</span><span class="sxs-lookup"><span data-stu-id="a79ae-169">Save as...</span></span><br/>                         |
| <span data-ttu-id="a79ae-170">開啟資料夾</span><span class="sxs-lookup"><span data-stu-id="a79ae-170">Open Folder</span></span><br/>       | <span data-ttu-id="a79ae-171">開啟資料夾 .。。或選擇資料夾 .。。</span><span class="sxs-lookup"><span data-stu-id="a79ae-171">Open folder... or Choose folder...</span></span><br/> |
| <span data-ttu-id="a79ae-172">尋找和取代</span><span class="sxs-lookup"><span data-stu-id="a79ae-172">Find and Replace</span></span><br/>  | <span data-ttu-id="a79ae-173">找到。。。或取代 .。。</span><span class="sxs-lookup"><span data-stu-id="a79ae-173">Find... or Replace...</span></span><br/>              |
| <span data-ttu-id="a79ae-174">列印</span><span class="sxs-lookup"><span data-stu-id="a79ae-174">Print</span></span><br/>             | <span data-ttu-id="a79ae-175">列印...</span><span class="sxs-lookup"><span data-stu-id="a79ae-175">Print...</span></span><br/>                           |
| <span data-ttu-id="a79ae-176">設定列印格式</span><span class="sxs-lookup"><span data-stu-id="a79ae-176">Page Setup</span></span><br/>        | <span data-ttu-id="a79ae-177">頁面設定 .。。</span><span class="sxs-lookup"><span data-stu-id="a79ae-177">Page setup...</span></span><br/>                      |
| <span data-ttu-id="a79ae-178">字型</span><span class="sxs-lookup"><span data-stu-id="a79ae-178">Font</span></span><br/>              | <span data-ttu-id="a79ae-179">字體。。。或選擇字型 .。。</span><span class="sxs-lookup"><span data-stu-id="a79ae-179">Font... or Choose font...</span></span><br/>          |
| <span data-ttu-id="a79ae-180">Color</span><span class="sxs-lookup"><span data-stu-id="a79ae-180">Color</span></span><br/>             | <span data-ttu-id="a79ae-181">顏色。。。或選擇色彩 .。。</span><span class="sxs-lookup"><span data-stu-id="a79ae-181">Color... or Choose color...</span></span><br/>        |



 

-   <span data-ttu-id="a79ae-182">您可以視需要使用更明確的命令。</span><span class="sxs-lookup"><span data-stu-id="a79ae-182">You can use more specific commands, as appropriate.</span></span> <span data-ttu-id="a79ae-183">範例：若要匯出檔案，請使用命令匯出檔案，而不是 [另存新檔]。</span><span class="sxs-lookup"><span data-stu-id="a79ae-183">Example: for exporting a file, use the command Export file instead of Save as.</span></span>
-   <span data-ttu-id="a79ae-184">設定對話方塊標題，以反映啟動它的命令。</span><span class="sxs-lookup"><span data-stu-id="a79ae-184">Set the dialog box title to reflect the command that launched it.</span></span> <span data-ttu-id="a79ae-185">範例：如果 [儲存檔案] 是從 [匯出檔案] 命令啟動，請將對話方塊重新命名為匯出檔案。</span><span class="sxs-lookup"><span data-stu-id="a79ae-185">Example: If Save File is launched from an Export file command, rename the dialog box to Export File.</span></span>

### <a name="open-file"></a><span data-ttu-id="a79ae-186">開啟檔案</span><span class="sxs-lookup"><span data-stu-id="a79ae-186">Open File</span></span>

-   <span data-ttu-id="a79ae-187">針對初始預設資料夾，請視需要使用特殊資料夾 (圖片、音樂、影片) ，否則請使用檔。</span><span class="sxs-lookup"><span data-stu-id="a79ae-187">For the initial default folder, use a specialized folder (Pictures, Music, Videos) as appropriate, otherwise use Documents.</span></span>
-   <span data-ttu-id="a79ae-188">針對後續的預設資料夾，請使用使用者使用程式開啟的最後一個資料夾。</span><span class="sxs-lookup"><span data-stu-id="a79ae-188">For subsequent default folders, use the last folder opened by the user using the program.</span></span>
-   <span data-ttu-id="a79ae-189">開啟相片檔案時，預設會隱藏檔案名。</span><span class="sxs-lookup"><span data-stu-id="a79ae-189">When opening photo files, suppress file names by default.</span></span> <span data-ttu-id="a79ae-190">相片通常是根據其縮圖來識別，而其名稱通常沒有意義。</span><span class="sxs-lookup"><span data-stu-id="a79ae-190">Photos are usually identified by their thumbnails and their names typically aren't meaningful.</span></span>

### <a name="save-file"></a><span data-ttu-id="a79ae-191">儲存檔案</span><span class="sxs-lookup"><span data-stu-id="a79ae-191">Save File</span></span>

-   <span data-ttu-id="a79ae-192">若為初始預設資料夾 (第一次) 儲存新檔案時，請視需要使用特製化資料夾 (圖片、音樂、影片) ，否則請使用檔。</span><span class="sxs-lookup"><span data-stu-id="a79ae-192">For the initial default folder (if a new file is being saved for the first time), use the specialized folder (Pictures, Music, Videos) as appropriate, otherwise use Documents.</span></span>
-   <span data-ttu-id="a79ae-193">若為暫存檔案，請使用目前使用者的暫存資料夾。</span><span class="sxs-lookup"><span data-stu-id="a79ae-193">For temporary files, use the current user's temporary folder.</span></span> <span data-ttu-id="a79ae-194">選擇一般但唯一的檔案名。</span><span class="sxs-lookup"><span data-stu-id="a79ae-194">Choose plain, but unique file names.</span></span> <span data-ttu-id="a79ae-195">範例：使用 File0001，而不是 ~ DF1A92. .tmp。</span><span class="sxs-lookup"><span data-stu-id="a79ae-195">Example: Use File0001.tmp instead of ~DF1A92.tmp.</span></span>
    -   <span data-ttu-id="a79ae-196">**開發人員：** 您可以使用 GetTempPath API 函數來取得目前使用者的暫存資料夾。</span><span class="sxs-lookup"><span data-stu-id="a79ae-196">**Developers:** You can get the current user's temporary folder using the GetTempPath API function.</span></span>
-   <span data-ttu-id="a79ae-197">針對初始預設檔案名，根據下列內容使用唯一的預設名稱：</span><span class="sxs-lookup"><span data-stu-id="a79ae-197">For the initial default file name, use a unique default name based on:</span></span>
    -   <span data-ttu-id="a79ae-198">檔案的內容（如果已知的話）。</span><span class="sxs-lookup"><span data-stu-id="a79ae-198">The file's contents, if known.</span></span> <span data-ttu-id="a79ae-199">範例：檔中的第一個字組。</span><span class="sxs-lookup"><span data-stu-id="a79ae-199">Example: The first words in a document.</span></span>
    -   <span data-ttu-id="a79ae-200">使用者選擇的模式。</span><span class="sxs-lookup"><span data-stu-id="a79ae-200">A pattern chosen by the user.</span></span> <span data-ttu-id="a79ae-201">範例：如果先前的檔案命名為 "夏威夷 1.jpg"，請選擇 [夏威夷 2.jpg] 作為下一個檔案。</span><span class="sxs-lookup"><span data-stu-id="a79ae-201">Example: If the previous file was named "Hawaii 1.jpg", choose "Hawaii 2.jpg" as the next file.</span></span>
    -   <span data-ttu-id="a79ae-202">以檔案類型為基礎的泛型模式。</span><span class="sxs-lookup"><span data-stu-id="a79ae-202">A generic pattern based on the file type.</span></span> <span data-ttu-id="a79ae-203">範例：「Photo1.jpg」。</span><span class="sxs-lookup"><span data-stu-id="a79ae-203">Example: "Photo1.jpg".</span></span>
-   <span data-ttu-id="a79ae-204">針對後續預設 (如果檔案已存在) ，請使用檔案的目前資料夾和名稱。</span><span class="sxs-lookup"><span data-stu-id="a79ae-204">For subsequent defaults (if the file already exists), use the file's current folder and name.</span></span>
-   <span data-ttu-id="a79ae-205">儲存檔案時，請保留其建立日期。</span><span class="sxs-lookup"><span data-stu-id="a79ae-205">When saving a file, preserve its creation date.</span></span> <span data-ttu-id="a79ae-206">如果您的程式會藉由建立暫存檔案來儲存檔案、刪除原始檔案，然後將暫存檔重新命名為原始檔案，請務必從源檔案複製建立日期。</span><span class="sxs-lookup"><span data-stu-id="a79ae-206">If your program saves files by creating a temporary file, deletes the original, and renames the temporary file to the original file name, be sure to copy the creation date from the original file.</span></span>
-   <span data-ttu-id="a79ae-207">如果使用者選取 [儲存] 命令而不指定檔案名，請使用 [儲存檔案]。</span><span class="sxs-lookup"><span data-stu-id="a79ae-207">Use Save File if the user selects the Save command without specifying a file name.</span></span>

### <a name="file-types-lists"></a><span data-ttu-id="a79ae-208">檔案類型清單</span><span class="sxs-lookup"><span data-stu-id="a79ae-208">File types lists</span></span>

<span data-ttu-id="a79ae-209">**注意：** [檔案類型] 清單是由 [開啟檔案] 和 [儲存檔案] 用來判斷所顯示的檔案類型和預設副檔名。</span><span class="sxs-lookup"><span data-stu-id="a79ae-209">**Note:** File types lists are used by Open File and Save File to determine the types of files displayed and the default file extension.</span></span>

-   <span data-ttu-id="a79ae-210">如果 [檔案類型] 清單很短 (五個或更少的) ，請依使用量的可能性來排序清單。</span><span class="sxs-lookup"><span data-stu-id="a79ae-210">If the file types list is short (five or fewer), order the list by likelihood of usage.</span></span> <span data-ttu-id="a79ae-211">如果清單的長度很長 (六個以上的) ，請使用字母順序，讓型別更容易尋找。</span><span class="sxs-lookup"><span data-stu-id="a79ae-211">If the list is long (six or more), use an alphabetical order to make the types easy to find.</span></span>
-   <span data-ttu-id="a79ae-212">針對 [儲存檔案]，包含支援之副檔名的所有變化（即使不常見），並先放置最常見的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="a79ae-212">For Save File, include all variations of the supported file extensions, even if uncommon, and put the most common extension first.</span></span> <span data-ttu-id="a79ae-213">檔案處理邏輯會查看此清單，以判斷使用者是否提供支援的副檔名。</span><span class="sxs-lookup"><span data-stu-id="a79ae-213">The file handling logic looks at this list to determine if the user supplied a supported file extension.</span></span> <span data-ttu-id="a79ae-214">範例：如果 JPEG 檔案類型清單僅包含 .jpg 和 JPEG，jpe 檔案可能會儲存為 test.jpe.jpg。</span><span class="sxs-lookup"><span data-stu-id="a79ae-214">Example: If a JPEG file types list includes only .jpg and .jpeg, the file test.jpe might be saved as test.jpe.jpg.</span></span>
-   <span data-ttu-id="a79ae-215">針對儲存檔案，初始預設檔案類型是目標使用者最可能選擇的類型。</span><span class="sxs-lookup"><span data-stu-id="a79ae-215">For Save File, the initial default file type is the most likely chosen by the target user.</span></span> <span data-ttu-id="a79ae-216">後續的預設值是檔案的目前類型。</span><span class="sxs-lookup"><span data-stu-id="a79ae-216">The subsequent default is the file's current type.</span></span>
-   <span data-ttu-id="a79ae-217">針對開啟的檔案，初始預設檔案類型是目標使用者最可能選擇的類型。</span><span class="sxs-lookup"><span data-stu-id="a79ae-217">For Open File, the initial default file type is the most likely chosen by the target user.</span></span> <span data-ttu-id="a79ae-218">後續的預設值應該是最後使用的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="a79ae-218">The subsequent default should be the last file type used.</span></span>
-   <span data-ttu-id="a79ae-219">針對 [開啟檔案]，如果使用者可以開啟任何檔案類型，請將 [所有檔案] 專案包含為第一個專案，或可能需要同時查看資料夾中的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="a79ae-219">For Open File, include an "All files" entry as the first item if users can open any file type, or may need to see all files in a folder at the same time.</span></span> <span data-ttu-id="a79ae-220">請考慮提供其他中繼篩選，例如「所有圖片」、「所有音樂」和「所有影片」。</span><span class="sxs-lookup"><span data-stu-id="a79ae-220">Consider providing other meta filters, such as "All pictures," "All music," and "All videos."</span></span> <span data-ttu-id="a79ae-221">立即將這些檔案放在 [所有檔案] 之後。</span><span class="sxs-lookup"><span data-stu-id="a79ae-221">Place these immediately after "All files."</span></span>
-   <span data-ttu-id="a79ae-222">使用 "File type name (\* . ext1;" 格式 \* 。ext2) 」。</span><span class="sxs-lookup"><span data-stu-id="a79ae-222">Use the format "File type name (\*.ext1; \*.ext2)."</span></span> <span data-ttu-id="a79ae-223">檔案類型名稱應該是註冊的檔案類型名稱，您可以在 [資料夾選項] 控制台專案中加以查看。</span><span class="sxs-lookup"><span data-stu-id="a79ae-223">The file type name should be the registered file type name, which you can view in the Folder Options control panel item.</span></span> <span data-ttu-id="a79ae-224">範例：「HTML 檔案 (\* .htm; \* 。html) 」。</span><span class="sxs-lookup"><span data-stu-id="a79ae-224">Example: "HTML document (\*.htm; \*.html)."</span></span>
    -   <span data-ttu-id="a79ae-225">**例外狀況：** 若為中繼篩選，請移除副檔名清單來消除雜亂的情形。</span><span class="sxs-lookup"><span data-stu-id="a79ae-225">**Exception:** For meta-filters, remove the file extension list to eliminate clutter.</span></span> <span data-ttu-id="a79ae-226">範例：「所有檔案」、「所有圖片」、「所有音樂」和「所有影片」。</span><span class="sxs-lookup"><span data-stu-id="a79ae-226">Examples: "All files," "All pictures," "All music," and "All videos."</span></span>
-   <span data-ttu-id="a79ae-227">針對檔案類型名稱使用 [句子樣式的大小寫](glossary.md) ，並針對檔案類型副檔名使用小寫。</span><span class="sxs-lookup"><span data-stu-id="a79ae-227">Use [sentence-style capitalization](glossary.md) for the file type names, and lowercase for the file type extensions.</span></span>

### <a name="open-folder"></a><span data-ttu-id="a79ae-228">開啟資料夾</span><span class="sxs-lookup"><span data-stu-id="a79ae-228">Open Folder</span></span>

-   <span data-ttu-id="a79ae-229">**針對新程式，請使用 [挑選資料夾] 模式中的 [開啟檔案] 對話方塊。**</span><span class="sxs-lookup"><span data-stu-id="a79ae-229">**For new programs, use the Open Files dialog in the "pick folders" mode.**</span></span> <span data-ttu-id="a79ae-230">這麼做需要 Windows Vista 或更新版本，因此請針對在舊版 Windows 中執行的程式使用 [開啟資料夾] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a79ae-230">Doing so requires Windows Vista or later, so use the Open Folder dialog for programs that run in earlier versions of Windows.</span></span>
    -   <span data-ttu-id="a79ae-231">**開發人員：** 您可以使用 [選擇資料夾] 模式中的 [開啟檔案] 對話方塊，方法是使用 FOS \_ PICKFOLDERS 旗標。</span><span class="sxs-lookup"><span data-stu-id="a79ae-231">**Developers:** You can use the Open Files dialog in the "pick folders" mode by using the FOS\_PICKFOLDERS flag.</span></span>

### <a name="font"></a><span data-ttu-id="a79ae-232">字型</span><span class="sxs-lookup"><span data-stu-id="a79ae-232">Font</span></span>

-   <span data-ttu-id="a79ae-233">如有必要，您可以篩選 [字型] 清單，只顯示您的程式可用的字型。</span><span class="sxs-lookup"><span data-stu-id="a79ae-233">If necessary, you can filter the font list to show only the fonts available to your program.</span></span>

### <a name="persistence"></a><span data-ttu-id="a79ae-234">持續性</span><span class="sxs-lookup"><span data-stu-id="a79ae-234">Persistence</span></span>

-   <span data-ttu-id="a79ae-235">請考慮讓下列值持續使用，作為後續的預設值：</span><span class="sxs-lookup"><span data-stu-id="a79ae-235">Consider making the following values persistent to use as subsequent defaults:</span></span>
    -   <span data-ttu-id="a79ae-236">輸入值 (範例：預設資料夾、預設檔案名) 。</span><span class="sxs-lookup"><span data-stu-id="a79ae-236">Input values (examples: default folders, default file names).</span></span>
    -   <span data-ttu-id="a79ae-237">選取的選項 (範例：選取的印表機、列印選項) 。</span><span class="sxs-lookup"><span data-stu-id="a79ae-237">Selected options (examples: selected printer, printing options).</span></span>
    -   <span data-ttu-id="a79ae-238">Views (範例：在縮圖中顯示圖片、顯示沒有檔案名的圖片、依日期排序、資料行寬度) 。</span><span class="sxs-lookup"><span data-stu-id="a79ae-238">Views (examples: showing pictures in thumbnail view, showing pictures without file names, sorting by date, column widths).</span></span>
    -   <span data-ttu-id="a79ae-239">展示 (範例： [視窗大小]、[位置] 和 [內容]) 。</span><span class="sxs-lookup"><span data-stu-id="a79ae-239">Presentation (examples: window size, location, and contents).</span></span>

<span data-ttu-id="a79ae-240">**例外狀況：** 當這些值的使用方式是讓使用者更有可能想要從頭開始時，請不要讓這些值保存在常見的對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="a79ae-240">**Exception:** Don't make these values persist for common dialogs when their usage is such that users are far more likely to want to start completely over.</span></span>

-   <span data-ttu-id="a79ae-241">決定預設值時，請根據重要的案例考慮使用者最可能想要的目標。</span><span class="sxs-lookup"><span data-stu-id="a79ae-241">When determining default values, consider what target users are most likely to want based on the important scenarios.</span></span> <span data-ttu-id="a79ae-242">此外，請考慮程式實例內的案例、跨多個實例， (連續或並行) ，以及跨多份檔。</span><span class="sxs-lookup"><span data-stu-id="a79ae-242">Also, consider scenarios within a program instance, across multiple instances (both consecutive or concurrent), and across multiple documents.</span></span> <span data-ttu-id="a79ae-243">請勿在不太可能有説明的情況下，將值保存。</span><span class="sxs-lookup"><span data-stu-id="a79ae-243">Don't make values persist in circumstances that aren't likely to be helpful.</span></span>
    -   <span data-ttu-id="a79ae-244">**範例：** 若為一般檔架構應用程式，使用持續性開啟檔案並在程式實例和連續實例之間儲存檔案設定，會很有説明，但讓並行實例保持獨立。</span><span class="sxs-lookup"><span data-stu-id="a79ae-244">**Example:** For a typical document-based application, it's helpful to use persistent Open File and Save File settings within a program instance and across consecutive instances, but keep concurrent instances independent.</span></span> <span data-ttu-id="a79ae-245">如此一來，使用者一次可以使用數份檔有效率地工作。</span><span class="sxs-lookup"><span data-stu-id="a79ae-245">That way, users can work efficiently with several documents at a time.</span></span>
-   <span data-ttu-id="a79ae-246">讓設定以個別程式、每個使用者為基礎來保存。</span><span class="sxs-lookup"><span data-stu-id="a79ae-246">Make the settings persist on a per-program, per-user basis.</span></span>

 

