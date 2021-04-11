---
title: 關於圖示
description: 本主題討論圖示。
ms.assetid: 67867460-07f6-460f-9263-05bbf3474744
keywords:
- 資源，圖示
- 圖示、作用點
- 圖示，標準
- 標準圖示
- 圖示，自訂
- 自訂圖示
- 圖示，大小
- 建立圖示
- 圖示，顯示
- 圖示，終結
- 圖示，複製
- 圖示，建立
- 顯示圖示
- 終結圖示
- 複製圖示
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bda00540d613b6d0efd4a080251ebd6407560ed
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315004"
---
# <a name="about-icons"></a><span data-ttu-id="ab948-118">關於圖示</span><span class="sxs-lookup"><span data-stu-id="ab948-118">About Icons</span></span>

<span data-ttu-id="ab948-119">系統會在使用者介面中使用圖示來代表物件，例如檔案、資料夾、快捷方式、應用程式和檔。</span><span class="sxs-lookup"><span data-stu-id="ab948-119">The system uses icons throughout the user interface to represent objects such as files, folders, shortcuts, applications, and documents.</span></span> <span data-ttu-id="ab948-120">圖示函式可讓應用程式建立、載入、顯示、排列、建立動畫，以及終結圖示。</span><span class="sxs-lookup"><span data-stu-id="ab948-120">The icon functions enable applications to create, load, display, arrange, animate, and destroy icons.</span></span> <span data-ttu-id="ab948-121">如需指定檔案類型圖示的詳細資訊，請參閱 [**ExtractIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extracticona)。</span><span class="sxs-lookup"><span data-stu-id="ab948-121">For information on specifying icons for file types, see [**ExtractIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extracticona).</span></span>

<span data-ttu-id="ab948-122">本總覽提供下列主題的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="ab948-122">This overview provides information on the following topics:</span></span>

-   [<span data-ttu-id="ab948-123">圖示作用點</span><span class="sxs-lookup"><span data-stu-id="ab948-123">Icon Hot Spot</span></span>](#icon-hot-spot)
-   [<span data-ttu-id="ab948-124">圖示類型</span><span class="sxs-lookup"><span data-stu-id="ab948-124">Icon Types</span></span>](#icon-types)
-   [<span data-ttu-id="ab948-125">圖示大小</span><span class="sxs-lookup"><span data-stu-id="ab948-125">Icon Sizes</span></span>](#icon-sizes)
    -   [<span data-ttu-id="ab948-126">變更系統小圖示的大小</span><span class="sxs-lookup"><span data-stu-id="ab948-126">To change the size of the system small icon</span></span>](#to-change-the-size-of-the-system-small-icon)
    -   [<span data-ttu-id="ab948-127">取出系統小圖示的大小</span><span class="sxs-lookup"><span data-stu-id="ab948-127">To retrieve the size of the system small icon</span></span>](#to-retrieve-the-size-of-the-system-small-icon)
    -   [<span data-ttu-id="ab948-128">取出系統大型圖示的大小</span><span class="sxs-lookup"><span data-stu-id="ab948-128">To retrieve the size of the system large icon</span></span>](#to-retrieve-the-size-of-the-system-large-icon)
    -   [<span data-ttu-id="ab948-129">取得 shell 小圖示的大小</span><span class="sxs-lookup"><span data-stu-id="ab948-129">To retrieve the size of the shell small icon</span></span>](#to-retrieve-the-size-of-the-shell-small-icon)
    -   [<span data-ttu-id="ab948-130">變更大型圖示的大小</span><span class="sxs-lookup"><span data-stu-id="ab948-130">To change the size of the large icon</span></span>](#to-change-the-size-of-the-large-icon)
    -   [<span data-ttu-id="ab948-131">取得 shell 大型圖示的大小</span><span class="sxs-lookup"><span data-stu-id="ab948-131">To retrieve the size of the shell large icon</span></span>](#to-retrieve-the-size-of-the-shell-large-icon)
-   [<span data-ttu-id="ab948-132">圖示建立</span><span class="sxs-lookup"><span data-stu-id="ab948-132">Icon Creation</span></span>](#icon-creation)
-   [<span data-ttu-id="ab948-133">圖示顯示</span><span class="sxs-lookup"><span data-stu-id="ab948-133">Icon Display</span></span>](#icon-display)
-   [<span data-ttu-id="ab948-134">圖示損毀</span><span class="sxs-lookup"><span data-stu-id="ab948-134">Icon Destruction</span></span>](#icon-destruction)
-   [<span data-ttu-id="ab948-135">圖示重複</span><span class="sxs-lookup"><span data-stu-id="ab948-135">Icon Duplication</span></span>](#icon-duplication)

## <a name="icon-hot-spot"></a><span data-ttu-id="ab948-136">圖示作用點</span><span class="sxs-lookup"><span data-stu-id="ab948-136">Icon Hot Spot</span></span>

<span data-ttu-id="ab948-137">圖示中的其中一個圖元會指定為 [作用](#icon-hot-spot)點，也就是系統追蹤和辨識為圖示位置的位置。</span><span class="sxs-lookup"><span data-stu-id="ab948-137">One of the pixels in an icon is designated as the [hot spot](#icon-hot-spot), which is the point the system tracks and recognizes as the position of the icon.</span></span> <span data-ttu-id="ab948-138">圖示的作用點通常是位於圖示中間的圖元。</span><span class="sxs-lookup"><span data-stu-id="ab948-138">An icon's hot spot is typically the pixel located at the center of the icon.</span></span> <span data-ttu-id="ab948-139">如果您使用 [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) 函式來建立圖示，則可以指定任何圖元作為作用點。</span><span class="sxs-lookup"><span data-stu-id="ab948-139">If you use the [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) function to create an icon, you can specify any pixel to be the hot spot.</span></span>

## <a name="icon-types"></a><span data-ttu-id="ab948-140">圖示類型</span><span class="sxs-lookup"><span data-stu-id="ab948-140">Icon Types</span></span>

<span data-ttu-id="ab948-141">作業系統提供一組 *標準圖示* ，可供任何應用程式隨時使用。</span><span class="sxs-lookup"><span data-stu-id="ab948-141">The operating system provides a set of *standard icons* that are available for any application to use at any time.</span></span> <span data-ttu-id="ab948-142">軟體發展工具組 (SDK) 標頭檔包含標準圖示的識別碼-識別碼開頭為 **IDI \_** 前置詞。</span><span class="sxs-lookup"><span data-stu-id="ab948-142">The software development kit (SDK) header files contain identifiers for the standard icons—the identifiers begin with the **IDI\_** prefix.</span></span>

<span data-ttu-id="ab948-143">每個標準圖示都有與其相關聯的對應預設影像。</span><span class="sxs-lookup"><span data-stu-id="ab948-143">Each standard icon has a corresponding default image associated with it.</span></span> <span data-ttu-id="ab948-144">使用者可以隨時取代與任何標準資料指標相關聯的預設影像。</span><span class="sxs-lookup"><span data-stu-id="ab948-144">The user can replace the default image associated with any standard cursor at any time.</span></span>

<span data-ttu-id="ab948-145">*自訂圖示* 的設計目的是要在特定應用程式中使用，而且可以是任何設計。</span><span class="sxs-lookup"><span data-stu-id="ab948-145">*Custom icons* are designed for use in a particular application and can be any design.</span></span> <span data-ttu-id="ab948-146">以下是數個自訂圖示。</span><span class="sxs-lookup"><span data-stu-id="ab948-146">Following are several custom icons.</span></span>

![數個自訂圖示](images/csicn-02.png)

## <a name="icon-sizes"></a><span data-ttu-id="ab948-148">圖示大小</span><span class="sxs-lookup"><span data-stu-id="ab948-148">Icon Sizes</span></span>

<span data-ttu-id="ab948-149">系統使用四個圖示大小：</span><span class="sxs-lookup"><span data-stu-id="ab948-149">The system uses four icon sizes:</span></span>

-   <span data-ttu-id="ab948-150">系統小</span><span class="sxs-lookup"><span data-stu-id="ab948-150">System small</span></span>
-   <span data-ttu-id="ab948-151">系統大型</span><span class="sxs-lookup"><span data-stu-id="ab948-151">System large</span></span>
-   <span data-ttu-id="ab948-152">Shell small</span><span class="sxs-lookup"><span data-stu-id="ab948-152">Shell small</span></span>
-   <span data-ttu-id="ab948-153">Shell 大型</span><span class="sxs-lookup"><span data-stu-id="ab948-153">Shell large</span></span>

<span data-ttu-id="ab948-154">*系統小圖示* 會顯示在視窗標題中。</span><span class="sxs-lookup"><span data-stu-id="ab948-154">The *system small icon* is displayed in the window caption.</span></span>

### <a name="to-change-the-size-of-the-system-small-icon"></a><span data-ttu-id="ab948-155">變更系統小圖示的大小</span><span class="sxs-lookup"><span data-stu-id="ab948-155">To change the size of the system small icon</span></span>

1.  <span data-ttu-id="ab948-156">在主控台中，按一下 [ **顯示**]，然後按一下 [ **外觀** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="ab948-156">From Control Panel, click **Display**, then click the **Appearance** tab.</span></span>
2.  <span data-ttu-id="ab948-157">從 [**專案**] 清單中選取 [**標題] 按鈕**，然後設定 [**大小**] 欄位。</span><span class="sxs-lookup"><span data-stu-id="ab948-157">Select **Caption Buttons** from the **Item** list, then set the **Size** field.</span></span>

### <a name="to-retrieve-the-size-of-the-system-small-icon"></a><span data-ttu-id="ab948-158">取出系統小圖示的大小</span><span class="sxs-lookup"><span data-stu-id="ab948-158">To retrieve the size of the system small icon</span></span>

-   <span data-ttu-id="ab948-159">使用 **sm \_ CXSMICON** 和 **Sm \_ CYSMICON** 來呼叫 [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)函數。</span><span class="sxs-lookup"><span data-stu-id="ab948-159">Call the [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function with **SM\_CXSMICON** and **SM\_CYSMICON**.</span></span>

<span data-ttu-id="ab948-160">*系統大型圖示* 主要是由應用程式使用，但它也會顯示在 Alt + Tab 對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="ab948-160">The *system large icon* is mainly used by applications, but it is also displayed in the Alt+Tab dialog.</span></span> <span data-ttu-id="ab948-161">[**CreateIconFromResource**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresource)、 [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon)、 [**ExtractAssociatedIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extractassociatedicona)、 [**ExtractIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extracticona)、 [**ExtractIconEx**](/windows/desktop/api/Shellapi/nf-shellapi-extracticonexa)和 [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona)函數全都使用系統大型圖示。</span><span class="sxs-lookup"><span data-stu-id="ab948-161">The [**CreateIconFromResource**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresource), [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon), [**ExtractAssociatedIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extractassociatedicona), [**ExtractIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extracticona), [**ExtractIconEx**](/windows/desktop/api/Shellapi/nf-shellapi-extracticonexa), and [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) functions all use system large icons.</span></span> <span data-ttu-id="ab948-162">系統大型圖示的大小是由 video 驅動程式所定義，因此無法變更。</span><span class="sxs-lookup"><span data-stu-id="ab948-162">The size of the system large icon is defined by the video driver, therefore it cannot be changed.</span></span>

### <a name="to-retrieve-the-size-of-the-system-large-icon"></a><span data-ttu-id="ab948-163">取出系統大型圖示的大小</span><span class="sxs-lookup"><span data-stu-id="ab948-163">To retrieve the size of the system large icon</span></span>

-   <span data-ttu-id="ab948-164">使用 **sm \_ CXICON** 和 **Sm \_ CYICON** 來呼叫 [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) 。</span><span class="sxs-lookup"><span data-stu-id="ab948-164">Call [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) with **SM\_CXICON** and **SM\_CYICON**.</span></span>

<span data-ttu-id="ab948-165">您可以使用 [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon)、 [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex)、 [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect)和 [**SHGetFileInfo**](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) 函式來處理系統大型以外大小的圖示。</span><span class="sxs-lookup"><span data-stu-id="ab948-165">The [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon), [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex), [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect), and [**SHGetFileInfo**](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) functions can be used to work with icons in sizes other than system large.</span></span>

<span data-ttu-id="ab948-166">[ *Shell small] 圖示* 用於 Windows 檔案總管和一般對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="ab948-166">The *shell small icon* is used in the Windows Explorer and the common dialogs.</span></span> <span data-ttu-id="ab948-167">目前，這預設為系統小的大小。</span><span class="sxs-lookup"><span data-stu-id="ab948-167">Currently, this defaults to the system small size.</span></span>

### <a name="to-retrieve-the-size-of-the-shell-small-icon"></a><span data-ttu-id="ab948-168">取得 shell 小圖示的大小</span><span class="sxs-lookup"><span data-stu-id="ab948-168">To retrieve the size of the shell small icon</span></span>

1.  <span data-ttu-id="ab948-169">使用 [SHGetFileInfo](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) 函式搭配 `SHGFI_SHELLICONSIZE | SHGFI_SMALLICON` 來取得系統映射清單的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ab948-169">Use the [SHGetFileInfo](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) function with `SHGFI_SHELLICONSIZE | SHGFI_SMALLICON` to retrieve a handle to the system image list.</span></span>
2.  <span data-ttu-id="ab948-170">然後呼叫 [**ImageList \_ GetIconSize**](/windows/win32/api/commctrl/nf-commctrl-imagelist_geticonsize) 函式以取得圖示大小。</span><span class="sxs-lookup"><span data-stu-id="ab948-170">Then call the [**ImageList\_GetIconSize**](/windows/win32/api/commctrl/nf-commctrl-imagelist_geticonsize) function to get the icon size.</span></span>

<span data-ttu-id="ab948-171">桌面上會使用 shell 大型圖示。</span><span class="sxs-lookup"><span data-stu-id="ab948-171">The shell large icon is used on the desktop.</span></span>

### <a name="to-change-the-size-of-the-large-icon"></a><span data-ttu-id="ab948-172">變更大型圖示的大小</span><span class="sxs-lookup"><span data-stu-id="ab948-172">To change the size of the large icon</span></span>

1.  <span data-ttu-id="ab948-173">在主控台中，按一下 [ **顯示**]，然後按一下 [ **外觀** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="ab948-173">From Control Panel , click **Display**, then click the **Appearance** tab,</span></span>
2.  <span data-ttu-id="ab948-174">從 [**專案**] 清單中選取 [**圖示**]，然後設定 [**大小**] 欄位 (此大小儲存在登錄中，在 [ **HKEY \_ 目前 \_ 使用者主控台] 下，[ \\ 桌面 \\ WindowMetrics \\ Shell 圖示大小**]) 。</span><span class="sxs-lookup"><span data-stu-id="ab948-174">Select **Icon** from the **Item** list, then set the **Size** field (this size is stored in the registry, under **HKEY\_CURRENT\_USER\\Control Panel, Desktop\\WindowMetrics\\Shell Icon Size**).</span></span>
3.  <span data-ttu-id="ab948-175">按一下 [ **plus** ]</span><span class="sxs-lookup"><span data-stu-id="ab948-175">Click the **Plus!**</span></span> <span data-ttu-id="ab948-176">索引標籤，然後選取 [ **使用大圖示** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="ab948-176">tab and then select the **Use Large Icons** check box.</span></span>

### <a name="to-retrieve-the-size-of-the-shell-large-icon"></a><span data-ttu-id="ab948-177">取得 shell 大型圖示的大小</span><span class="sxs-lookup"><span data-stu-id="ab948-177">To retrieve the size of the shell large icon</span></span>

1.  <span data-ttu-id="ab948-178">使用 [**SHGetFileInfo**](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) 函式搭配 **SHGFI \_ SHELLICONSIZE** ，以取得系統映射清單的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ab948-178">Use the [**SHGetFileInfo**](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) function with **SHGFI\_SHELLICONSIZE** to retrieve a handle to the system image list.</span></span>
2.  <span data-ttu-id="ab948-179">然後呼叫 [**ImageList \_ GetIconSize**](/windows/win32/api/commctrl/nf-commctrl-imagelist_geticonsize) 函式以取得圖示大小。</span><span class="sxs-lookup"><span data-stu-id="ab948-179">Then call the [**ImageList\_GetIconSize**](/windows/win32/api/commctrl/nf-commctrl-imagelist_geticonsize) function to get the icon size.</span></span>

<span data-ttu-id="ab948-180">根據是否選取 [ **使用大圖示** ] 核取方塊，[開始] 功能表會使用 shell 小型圖示或 shell 大型圖示。</span><span class="sxs-lookup"><span data-stu-id="ab948-180">The Start menu uses either shell small icons or shell large icons, depending on whether the **Use Large Icons** check box is selected.</span></span>

<span data-ttu-id="ab948-181">您的應用程式應該提供下列大小的圖示影像群組：</span><span class="sxs-lookup"><span data-stu-id="ab948-181">Your application should supply groups of icon images in the following sizes:</span></span>

-   <span data-ttu-id="ab948-182">48x48，256色彩</span><span class="sxs-lookup"><span data-stu-id="ab948-182">48x48, 256 color</span></span>
-   <span data-ttu-id="ab948-183">32x32、16色</span><span class="sxs-lookup"><span data-stu-id="ab948-183">32x32, 16 color</span></span>
-   <span data-ttu-id="ab948-184">16x16 圖元、16色</span><span class="sxs-lookup"><span data-stu-id="ab948-184">16x16 pixels, 16 color</span></span>

<span data-ttu-id="ab948-185">填入要用於註冊視窗類別的 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) 結構時，請將 **hIcon** 成員設定為32x32 圖示，並將 **hIconSm** 成員設定為16x16 圖示。</span><span class="sxs-lookup"><span data-stu-id="ab948-185">When filling in the [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) structure to be used in registering your window class, set the **hIcon** member to the 32x32 icon and the **hIconSm** member to the 16x16 icon.</span></span> <span data-ttu-id="ab948-186">如需類別圖示的詳細資訊，請參閱 [類別圖示](/windows/desktop/winmsg/about-window-classes)。</span><span class="sxs-lookup"><span data-stu-id="ab948-186">For more information about class icons, see [Class Icons](/windows/desktop/winmsg/about-window-classes).</span></span>

## <a name="icon-creation"></a><span data-ttu-id="ab948-187">圖示建立</span><span class="sxs-lookup"><span data-stu-id="ab948-187">Icon Creation</span></span>

<span data-ttu-id="ab948-188">標準圖示是預先定義的，因此不需要建立它們。</span><span class="sxs-lookup"><span data-stu-id="ab948-188">Standard icons are predefined, so it is not necessary to create them.</span></span> <span data-ttu-id="ab948-189">若要使用標準圖示，應用程式可以使用 [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) 函式來取得其控制碼。</span><span class="sxs-lookup"><span data-stu-id="ab948-189">To use a standard icon, an application can obtain its handle by using the [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) function.</span></span> <span data-ttu-id="ab948-190">*圖示控制碼* 是 **HICON** 類型的唯一值，可識別標準或自訂圖示。</span><span class="sxs-lookup"><span data-stu-id="ab948-190">An *icon handle* is a unique value of the **HICON** type that identifies a standard or custom icon.</span></span>

<span data-ttu-id="ab948-191">若要建立應用程式的自訂圖示，您通常會使用圖形應用程式，並在應用程式的資源定義檔中包含 [圖示資源](./icon-resource.md) 。</span><span class="sxs-lookup"><span data-stu-id="ab948-191">To create a custom icon for an application, you would typically use a graphics application and include the [ICON Resource](./icon-resource.md) in the application's resource-definition file.</span></span> <span data-ttu-id="ab948-192">在執行時間，您可以呼叫 [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) 或 [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) 來取得圖示的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ab948-192">At run-time, you can call [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) or [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) to retrieve a handle to the icon.</span></span> <span data-ttu-id="ab948-193">圖示資源可以包含數個不同顯示裝置的一組影像。</span><span class="sxs-lookup"><span data-stu-id="ab948-193">An icon resource can contain a group of images for several different display devices.</span></span> <span data-ttu-id="ab948-194">**LoadIcon** 和 **LoadImage** 會自動從目前顯示裝置的群組中選取最適當的圖示。</span><span class="sxs-lookup"><span data-stu-id="ab948-194">**LoadIcon** and **LoadImage** automatically select the most appropriate icon from the group for the current display device.</span></span>

<span data-ttu-id="ab948-195">應用程式也可以使用 [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) 函式在執行時間建立自訂圖示，該函式會根據 [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) 結構的內容建立圖示。</span><span class="sxs-lookup"><span data-stu-id="ab948-195">An application can also create a custom icon at run-time by using the [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) function, which creates an icon based on the contents of an [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) structure.</span></span> <span data-ttu-id="ab948-196">[**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo)函式會以作用點座標和圖示的位元遮罩點陣圖和色彩點陣圖的相關資訊填入結構。</span><span class="sxs-lookup"><span data-stu-id="ab948-196">The [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) function fills the structure with the hot-spot coordinates and information about the bitmask bitmap and color bitmap for the icon.</span></span>

<span data-ttu-id="ab948-197">應用程式應該將自訂圖示實作為資源，而且應該使用 [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) 或 [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea)，而不是在執行時間建立圖示。</span><span class="sxs-lookup"><span data-stu-id="ab948-197">Applications should implement custom icons as resources and should use [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) or [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea), rather than create the icon at run-time.</span></span> <span data-ttu-id="ab948-198">使用圖示資源可避免裝置的相依性、簡化當地語系化，以及讓應用程式共用圖示圖形。</span><span class="sxs-lookup"><span data-stu-id="ab948-198">Using icon resources avoids device dependence, simplifies localization, and enables applications to share icon shapes.</span></span>

<span data-ttu-id="ab948-199">[**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex)函式可讓應用程式流覽系統的資源，並根據資源資料建立圖示和資料指標。</span><span class="sxs-lookup"><span data-stu-id="ab948-199">The [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex) function enables an application to browse through the system's resources and create icons and cursors based on resource data.</span></span> <span data-ttu-id="ab948-200">**CreateIconFromResourceEx** 會根據其他可執行檔或 dll 中的二進位資源資料建立圖示。</span><span class="sxs-lookup"><span data-stu-id="ab948-200">**CreateIconFromResourceEx** creates an icon based on binary resource data from other executable files or DLLs.</span></span> <span data-ttu-id="ab948-201">應用程式必須在此函式之前，呼叫 [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex) 函式和數個資源函數。</span><span class="sxs-lookup"><span data-stu-id="ab948-201">An application must precede this function with calls to the [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex) function and several of the resource functions.</span></span> <span data-ttu-id="ab948-202">**LookupIconIdFromDirectoryEx** 會傳回目前顯示裝置最適當的圖示資料識別碼。</span><span class="sxs-lookup"><span data-stu-id="ab948-202">**LookupIconIdFromDirectoryEx** returns the identifier of the most appropriate icon data for the current display device.</span></span>

## <a name="icon-display"></a><span data-ttu-id="ab948-203">圖示顯示</span><span class="sxs-lookup"><span data-stu-id="ab948-203">Icon Display</span></span>

<span data-ttu-id="ab948-204">您可以使用 [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) 函式來抓取圖示的影像，也可以使用 [**DrawIconEx**](/windows/desktop/api/Winuser/nf-winuser-drawiconex) 函數來繪製它。</span><span class="sxs-lookup"><span data-stu-id="ab948-204">You can retrieve the image for an icon by using the [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) function, and can draw it by using the [**DrawIconEx**](/windows/desktop/api/Winuser/nf-winuser-drawiconex) function.</span></span> <span data-ttu-id="ab948-205">若要繪製圖示的預設影像，請在 **DrawIconEx** 的呼叫中指定 **DI \_ 相容** 性旗標。</span><span class="sxs-lookup"><span data-stu-id="ab948-205">To draw the default image for a icon, specify the **DI\_COMPAT** flag in the call to **DrawIconEx**.</span></span> <span data-ttu-id="ab948-206">如果您未指定 **DI \_ 相容** 性旗標， **DrawIconEx** 會使用使用者指定的影像繪製圖示。</span><span class="sxs-lookup"><span data-stu-id="ab948-206">If you do not specify the **DI\_COMPAT** flag, **DrawIconEx** draws the icon using the image that the user specified.</span></span>

<span data-ttu-id="ab948-207">當系統顯示圖示時，必須從 .exe 或 .dll 檔案解壓縮適當的圖示影像。</span><span class="sxs-lookup"><span data-stu-id="ab948-207">When the system displays an icon, it must extract the appropriate icon image from the .exe or .dll file.</span></span> <span data-ttu-id="ab948-208">系統會使用下列步驟來選取圖示影像：</span><span class="sxs-lookup"><span data-stu-id="ab948-208">The system uses the following steps to select the icon image:</span></span>

1.  <span data-ttu-id="ab948-209">選取 **RT \_ 群組 \_ 圖示** 資源。</span><span class="sxs-lookup"><span data-stu-id="ab948-209">Select the **RT\_GROUP\_ICON** resource.</span></span> <span data-ttu-id="ab948-210">如果有一個以上的這類資源存在，系統會使用資源腳本中所列的第一個資源。</span><span class="sxs-lookup"><span data-stu-id="ab948-210">If more than one such resource exists, the system uses the first resource listed in the resource scrip.</span></span>
2.  <span data-ttu-id="ab948-211">從 **RT \_ 群組 \_ 圖示** 資源選取適當的 **rt \_ 圖示** 影像。</span><span class="sxs-lookup"><span data-stu-id="ab948-211">Select the appropriate **RT\_ICON** image from the **RT\_GROUP\_ICON** resource.</span></span> <span data-ttu-id="ab948-212">如果有一個以上的映射存在，系統會使用下列準則來選擇映射：</span><span class="sxs-lookup"><span data-stu-id="ab948-212">If more than one image exists, the system uses the following criteria to choose an image:</span></span>
    -   -   <span data-ttu-id="ab948-213">選擇最接近所要求大小的影像。</span><span class="sxs-lookup"><span data-stu-id="ab948-213">The image closest in size to the requested size is chosen.</span></span>
        -   <span data-ttu-id="ab948-214">如果有兩個或多個大小的影像，則會選擇符合顯示器色彩深度的影像。</span><span class="sxs-lookup"><span data-stu-id="ab948-214">If two or more images of that size are present, the one that matches the color depth of the display is chosen.</span></span>
        -   <span data-ttu-id="ab948-215">如果沒有任何影像與顯示器的色彩深度完全相符，則會選擇具有最大色彩深度（不超過顯示器的色彩深度）的影像。</span><span class="sxs-lookup"><span data-stu-id="ab948-215">If no images exactly match the color depth of the display, the image with the greatest color depth that does not exceed the color depth of the display is chosen.</span></span> <span data-ttu-id="ab948-216">如果全部超過色彩深度，則會選擇具有最低色彩深度的色彩深度。</span><span class="sxs-lookup"><span data-stu-id="ab948-216">If all exceed the color depth, the one with the lowest color depth is chosen.</span></span>

> [!Note]  
> <span data-ttu-id="ab948-217">系統會將8或更多 bpp 的所有色彩深度視為相等。</span><span class="sxs-lookup"><span data-stu-id="ab948-217">The system treats all color depths of 8 or more bpp as equal.</span></span> <span data-ttu-id="ab948-218">因此，在相同的資源中，不會有包含 16x16 256 色影像和 16x16 16 色影像的優點，系統只會選擇它所遇到的第一個。</span><span class="sxs-lookup"><span data-stu-id="ab948-218">Therefore, there is no advantage of including a 16x16 256-color image and a 16x16 16-color image in the same resource—the system will simply choose the first one it encounters.</span></span> <span data-ttu-id="ab948-219">當顯示器處於 8 bpp 模式時，系統會在256色彩的圖示上選擇16色圖示，並使用系統預設調色板來顯示所有圖示。</span><span class="sxs-lookup"><span data-stu-id="ab948-219">When the display is in 8-bpp mode, the system will choose a 16-color icon over a 256-color icon, and will display all icons using the system default palette.</span></span>

 

<span data-ttu-id="ab948-220">若要顯示動畫圖標，請使用靜態控制項，如下列程式碼片段所示。</span><span class="sxs-lookup"><span data-stu-id="ab948-220">To display an animated icon, use a static control as shown in the following code fragment.</span></span>


```
hIcon = LoadImage(NULL, "ico.ani", IMAGE_ICON, 0, 0, LR_LOADFROMFILE);
SendMessage( hStatic, STM_SETIMAGE, IMAGE_ICON, (LPARAM)(UINT)hIcon);
```



## <a name="icon-destruction"></a><span data-ttu-id="ab948-221">圖示損毀</span><span class="sxs-lookup"><span data-stu-id="ab948-221">Icon Destruction</span></span>

<span data-ttu-id="ab948-222">當應用程式不再需要使用 [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) 函式所建立的圖示時，它應該會摧毀圖示。</span><span class="sxs-lookup"><span data-stu-id="ab948-222">When an application no longer needs an icon it created by using the [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) function, it should destroy the icon.</span></span> <span data-ttu-id="ab948-223">[**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon)函式會終結圖示控制碼，並釋出圖示所使用的任何記憶體。</span><span class="sxs-lookup"><span data-stu-id="ab948-223">The [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) function destroys the icon handle and frees any memory used by the icon.</span></span> <span data-ttu-id="ab948-224">應用程式應該只將此函式用於以 **CreateIconIndirect** 建立的圖示;不需要終結其他圖示。</span><span class="sxs-lookup"><span data-stu-id="ab948-224">Applications should use this function only for icons created with **CreateIconIndirect**; it is not necessary to destroy other icons.</span></span>

## <a name="icon-duplication"></a><span data-ttu-id="ab948-225">圖示重複</span><span class="sxs-lookup"><span data-stu-id="ab948-225">Icon Duplication</span></span>

<span data-ttu-id="ab948-226">[**CopyIcon**](/windows/desktop/api/Winuser/nf-winuser-copyicon)函式會複製圖示控制碼。</span><span class="sxs-lookup"><span data-stu-id="ab948-226">The [**CopyIcon**](/windows/desktop/api/Winuser/nf-winuser-copyicon) function copies an icon handle.</span></span> <span data-ttu-id="ab948-227">這可讓應用程式或 DLL 取得其他模組所擁有之圖示的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ab948-227">This enables an application or DLL to get its own handle to an icon owned by another module.</span></span> <span data-ttu-id="ab948-228">然後，如果已釋出其他模組，複製圖示的應用程式仍然可以使用此圖示。</span><span class="sxs-lookup"><span data-stu-id="ab948-228">Then, if the other module is freed, the application that copied the icon will still be able to use the icon.</span></span>

<span data-ttu-id="ab948-229">[**CopyImage**](/windows/desktop/api/Winuser/nf-winuser-copyimage)函式會根據指定的來源圖示來建立新的圖示。</span><span class="sxs-lookup"><span data-stu-id="ab948-229">The [**CopyImage**](/windows/desktop/api/Winuser/nf-winuser-copyimage) function creates a new icon based on the specified source icon.</span></span> <span data-ttu-id="ab948-230">新圖示可以大於或小於來源圖示。</span><span class="sxs-lookup"><span data-stu-id="ab948-230">The new icon can be larger or smaller than the source icon.</span></span>

<span data-ttu-id="ab948-231">如需有關在可執行檔 ( .exe) 檔中新增、移除或取代圖示資源的詳細資訊，請參閱 [資源](resources.md)。</span><span class="sxs-lookup"><span data-stu-id="ab948-231">For information about adding, removing, or replacing icon resources in executable (.exe) files, see [Resources](resources.md).</span></span>

<span data-ttu-id="ab948-232">[**DuplicateIcon**](/windows/desktop/api/Shellapi/nf-shellapi-duplicateicon)函式會建立圖示的實際複本。</span><span class="sxs-lookup"><span data-stu-id="ab948-232">The [**DuplicateIcon**](/windows/desktop/api/Shellapi/nf-shellapi-duplicateicon) function makes an actual copy of the icon.</span></span>

 

 