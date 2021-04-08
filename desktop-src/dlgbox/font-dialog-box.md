---
title: 字型對話方塊
description: '[字型] 對話方塊可讓使用者選擇邏輯字型的屬性，例如字型系列和相關聯的字型樣式、點大小、效果 (底線、刪除線和文字色彩) ，以及腳本 (或字元集) 。'
ms.assetid: e8a996aa-4e34-45d0-a325-9c20b1a6ce07
keywords:
- Windows 消費者介面，使用者輸入
- Windows 消費者介面、通用對話方塊程式庫
- 使用者輸入、通用對話方塊程式庫
- 正在捕獲使用者輸入，通用對話方塊程式庫
- 通用對話方塊程式庫
- 通用對話方塊
- 字型對話方塊
- 自訂字型對話方塊
- 旗標、字型對話方塊
- 初始化旗標
- 預先定義的對話方塊
- 對話方塊、字型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a752ce53ecf496c58efb0c346a8c3d67c4f1b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024029"
---
# <a name="font-dialog-box"></a><span data-ttu-id="cd902-115">字型對話方塊</span><span class="sxs-lookup"><span data-stu-id="cd902-115">Font Dialog Box</span></span>

<span data-ttu-id="cd902-116">[ **字型** ] 對話方塊可讓使用者選擇邏輯字型的屬性，例如字型系列和相關聯的字型樣式、點大小、效果 (底線、刪除線和文字色彩) ，以及腳本 (或字元集) 。</span><span class="sxs-lookup"><span data-stu-id="cd902-116">The **Font** dialog box lets the user choose attributes for a logical font, such as font family and associated font style, point size, effects (underline, strikeout, and text color), and a script (or character set).</span></span>

<span data-ttu-id="cd902-117">您可以藉由初始化 [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)結構並將結構傳遞至 [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)函式，來建立和顯示 **字型** 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="cd902-117">You create and display a **Font** dialog box by initializing a [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure and passing the structure to the [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function.</span></span>

<span data-ttu-id="cd902-118">下列螢幕擷取畫面顯示一般的 [ **字型** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="cd902-118">The following screen shot shows a typical **Font** dialog box.</span></span>

![顯示 [字型] 對話方塊的螢幕擷取畫面](images/fontdialogboxxp.png)

<span data-ttu-id="cd902-120">如果使用者按一下 [ **確定]** 按鈕， [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) 函式會傳回 **TRUE** ，並在 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) 結構中設定使用者選取範圍的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cd902-120">If the user clicks the **OK** button, the [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function returns **TRUE** and sets the information about the user's selection in the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure.</span></span>

<span data-ttu-id="cd902-121">如果使用者取消 [ **字型** ] 對話方塊或發生錯誤， [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) 會傳回 **FALSE** ，且不會定義 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) 結構的內容。</span><span class="sxs-lookup"><span data-stu-id="cd902-121">If the user cancels the **Font** dialog box or an error occurs, [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) returns **FALSE** and the contents of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure are not defined.</span></span> <span data-ttu-id="cd902-122">您可以使用 [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) 函式來取出擴充的錯誤值，以判斷錯誤的原因。</span><span class="sxs-lookup"><span data-stu-id="cd902-122">You can determine the cause of an error by using the [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) function to retrieve the extended error value.</span></span>

<span data-ttu-id="cd902-123">本節將討論下列主題。</span><span class="sxs-lookup"><span data-stu-id="cd902-123">The following topics are discussed in this section.</span></span>

-   [<span data-ttu-id="cd902-124">字型對話方塊初始化旗標</span><span class="sxs-lookup"><span data-stu-id="cd902-124">Font Dialog Box Initialization Flags</span></span>](#font-dialog-box-initialization-flags)
-   [<span data-ttu-id="cd902-125">在舊版 Windows 上自訂字型對話方塊</span><span class="sxs-lookup"><span data-stu-id="cd902-125">Customizing the Font Dialog Box on earlier versions of Windows</span></span>](#customizing-the-font-dialog-box-on-earlier-versions-of-windows)
-   [<span data-ttu-id="cd902-126">在 Windows 7 上自訂字型對話方塊</span><span class="sxs-lookup"><span data-stu-id="cd902-126">Customizing the Font Dialog Box on Windows 7</span></span>](#customizing-the-font-dialog-box-on-windows-7)

## <a name="font-dialog-box-initialization-flags"></a><span data-ttu-id="cd902-127">字型對話方塊初始化旗標</span><span class="sxs-lookup"><span data-stu-id="cd902-127">Font Dialog Box Initialization Flags</span></span>

<span data-ttu-id="cd902-128">在呼叫 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)之前， [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)結構的 **旗標** 成員必須指定 **cf \_ SCREENFONTS**、 **cf \_ PRINTERFONTS** 或 **cf \_ 兩者**，以指出對話方塊是否應列出螢幕字型、印表機字型或兩者。</span><span class="sxs-lookup"><span data-stu-id="cd902-128">Before calling [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta), the **Flags** member of the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure must specify **CF\_SCREENFONTS**, **CF\_PRINTERFONTS**, or **CF\_BOTH**, to indicate whether the dialog box should list screen fonts, printer fonts, or both.</span></span> <span data-ttu-id="cd902-129">如果您指定 **cf \_ PRINTERFONTS** 或 **cf \_**， **CHOOSEFONT** 結構的 **hDC** 成員就必須指定印表機的裝置內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="cd902-129">If you specify **CF\_PRINTERFONTS** or **CF\_BOTH**, the **hDC** member of the **CHOOSEFONT** structure must specify a handle to a device context for the printer.</span></span>

<span data-ttu-id="cd902-130">如果已設定 **cf \_ PRINTERFONTS** 或 **cf \_ 兩個** 旗標，字型類型描述標籤會出現在 [ **字型** ] 對話方塊的底部。</span><span class="sxs-lookup"><span data-stu-id="cd902-130">If the **CF\_PRINTERFONTS** or **CF\_BOTH** flag is set, the font type description label appears at the bottom of the **Font** dialog box.</span></span>

<span data-ttu-id="cd902-131">從 Windows 7 開始，適用于字型列舉的 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)函式不再使用 **cf \_ PRINTERFONTS**、 **cf \_ SCREENFONTS**、 **cf \_** 和 **cf \_ WYSIWYG** 旗標。</span><span class="sxs-lookup"><span data-stu-id="cd902-131">Starting with Windows 7, the **CF\_PRINTERFONTS**, **CF\_SCREENFONTS**, **CF\_BOTH**, and **CF\_WYSIWYG** flags are no longer used by the [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function for font enumeration.</span></span> <span data-ttu-id="cd902-132">它們在 Windows 7 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="cd902-132">They are obsolete in Windows 7.</span></span> <span data-ttu-id="cd902-133">不過， **CF \_ PRINTERFONTS** 旗標會保留一個函式：在 [ **字型** ] 對話方塊底部顯示 [字型類型描述] 標籤。</span><span class="sxs-lookup"><span data-stu-id="cd902-133">However, the **CF\_PRINTERFONTS** flag retains one function: to display the font type description label at the bottom of the **Font** dialog box.</span></span>

<span data-ttu-id="cd902-134">您可以使用 **旗標** 成員來啟用或停用某些 **字型** 對話方塊控制項，而且您可以搭配其他 [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)成員使用 **旗標** 成員來控制某些控制項的初始值。</span><span class="sxs-lookup"><span data-stu-id="cd902-134">You can use the **Flags** member to enable or disable some of the **Font** dialog box controls, and you can use the **Flags** member in conjunction with other [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) members to control the initial values of some controls.</span></span>

<span data-ttu-id="cd902-135">**若要顯示允許使用者選取 [刪除]、[底線] 和 [色彩] 選項的控制項：**</span><span class="sxs-lookup"><span data-stu-id="cd902-135">**To display the controls that allow the user to select strikeout, underline, and color options:**</span></span>

-   <span data-ttu-id="cd902-136">設定 **CF \_ 效果** 旗標。</span><span class="sxs-lookup"><span data-stu-id="cd902-136">Set the **CF\_EFFECTS** flag.</span></span> <span data-ttu-id="cd902-137">您可以使用 [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)結構的 **rgbColors** 成員來指定初始字型色彩。</span><span class="sxs-lookup"><span data-stu-id="cd902-137">You can use the **rgbColors** member of the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure to specify an initial font color.</span></span>

<span data-ttu-id="cd902-138">**指定字型、字型樣式、大小、刪除線和底線對話方塊控制項的初始值：**</span><span class="sxs-lookup"><span data-stu-id="cd902-138">**To specify the initial values for the Font, Font Style, Size, Strikeout, and Underline dialog box controls:**</span></span>

1.  <span data-ttu-id="cd902-139">指定字型、字型樣式、大小、刪除線和底線對話方塊控制項的初始值：</span><span class="sxs-lookup"><span data-stu-id="cd902-139">To specify the initial values for the Font, Font Style, Size, Strikeout, and Underline dialog box controls:</span></span>
2.  <span data-ttu-id="cd902-140">在 **旗標** 成員中設定 **CF \_ INITTOLOGFONTSTRUCT** 旗標，以及 **lpLogFont** 所指向之 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的成員，以指定字型屬性的初始值。</span><span class="sxs-lookup"><span data-stu-id="cd902-140">Set the **CF\_INITTOLOGFONTSTRUCT** flag in the **Flags** member, along with members of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that is pointed to by the **lpLogFont**, to specify the initial values for the font attributes.</span></span>
3.  <span data-ttu-id="cd902-141">您也可以使用 **cf \_ NOFACESEL**、 **cf \_ NOSTYLESEL** 和 **cf \_ NOSIZESEL** 旗標，以防止 [ **字型** ] 對話方塊顯示對應控制項的初始值。</span><span class="sxs-lookup"><span data-stu-id="cd902-141">You can also use the **CF\_NOFACESEL**, **CF\_NOSTYLESEL**, and **CF\_NOSIZESEL** flags to prevent the **Font** dialog box from displaying initial values for the corresponding controls.</span></span> <span data-ttu-id="cd902-142">當您使用具有多個字型、樣式或點大小的文字選取專案時，這會很有用。</span><span class="sxs-lookup"><span data-stu-id="cd902-142">This is useful when you are working with a selection of text that has more than one typeface, style, or point size.</span></span> <span data-ttu-id="cd902-143">如果使用者未選取對應的值，則 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)傳回時，這些值也會設定在 **旗標** 中。</span><span class="sxs-lookup"><span data-stu-id="cd902-143">These values will also be set in **Flags** when [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) returns, if the user did not select a corresponding value.</span></span>

<span data-ttu-id="cd902-144">**將字型樣式控制項初始化為指定的樣式名稱**</span><span class="sxs-lookup"><span data-stu-id="cd902-144">**To initialize the Font Style control to a specified style name**</span></span>

-   <span data-ttu-id="cd902-145">設定 **CF \_ USESTYLE** 旗標，並使用 **lpszStyle** 成員指定樣式名稱。</span><span class="sxs-lookup"><span data-stu-id="cd902-145">Set the **CF\_USESTYLE** flag and use the **lpszStyle** member to specify the style name.</span></span>

> [!Note]  
> <span data-ttu-id="cd902-146">若要全球化您的應用程式，請使用 **lpLogFont** 所指向之 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的 **lfWeight** 和 **lfItalic** 成員來指定樣式。</span><span class="sxs-lookup"><span data-stu-id="cd902-146">To globalize your application, specify the style by using the **lfWeight** and **lfItalic** members of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that is pointed to by **lpLogFont**.</span></span> <span data-ttu-id="cd902-147">樣式名稱可能會隨著系統使用者介面語言而變更。</span><span class="sxs-lookup"><span data-stu-id="cd902-147">The style name may change depending on the system user interface language.</span></span>

 

<span data-ttu-id="cd902-148">**若要顯示 [套用] 按鈕**</span><span class="sxs-lookup"><span data-stu-id="cd902-148">**To display the Apply button**</span></span>

-   <span data-ttu-id="cd902-149">設定 **CF 套用 \_** 旗標，並提供攔截程式來處理 **適用于**[套用] 按鈕的 [**WM \_ 命令**](/windows/desktop/menurc/wm-command)訊息。</span><span class="sxs-lookup"><span data-stu-id="cd902-149">Set the **CF\_APPLY** flag and provide a hook procedure to process [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages for the **Apply** button.</span></span> <span data-ttu-id="cd902-150">攔截程式可以將 [**WM \_ CHOOSEFONT \_ GETLOGFONT**](wm-choosefont-getlogfont.md) 訊息傳送至對話方塊，以取得包含字型目前選取範圍的 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) 結構位址。</span><span class="sxs-lookup"><span data-stu-id="cd902-150">The hook procedure can send the [**WM\_CHOOSEFONT\_GETLOGFONT**](wm-choosefont-getlogfont.md) message to the dialog box to retrieve the address of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure that contains the current selections for the font.</span></span>

<span data-ttu-id="cd902-151">**若要顯示 [說明] 按鈕**</span><span class="sxs-lookup"><span data-stu-id="cd902-151">**To display the Help button**</span></span>

-   <span data-ttu-id="cd902-152">設定 **CF \_ SHOWHELP** 旗標。</span><span class="sxs-lookup"><span data-stu-id="cd902-152">Set the **CF\_SHOWHELP** flag.</span></span> <span data-ttu-id="cd902-153">當使用者按一下 [說明 **] 按鈕時**， **hwndOwner** 成員必須識別要接收 [**HELPMSGSTRING**](helpmsgstring.md)註冊訊息的視窗。</span><span class="sxs-lookup"><span data-stu-id="cd902-153">The **hwndOwner** member must identify the window to receive the [**HELPMSGSTRING**](helpmsgstring.md) registered message when the user clicks the **Help** button.</span></span>

<span data-ttu-id="cd902-154">**限制顯示在對話方塊中的字型**</span><span class="sxs-lookup"><span data-stu-id="cd902-154">**To restrict the fonts displayed in the dialog box**</span></span>

-   <span data-ttu-id="cd902-155">設定 **cf \_ TTONLY**、 **cf \_ FIXEDPITCHONLY**、 **cf \_ NOVECTORFONTS**、 **cf \_ NOVERTFONTS**、 **cf \_ SCALABLEONLY** 和 **CF \_ WYSIWYG** 旗標的任何組合。</span><span class="sxs-lookup"><span data-stu-id="cd902-155">Set any combination of the **CF\_TTONLY**, **CF\_FIXEDPITCHONLY**, **CF\_NOVECTORFONTS**, **CF\_NOVERTFONTS**, **CF\_SCALABLEONLY**, and **CF\_WYSIWYG** flags.</span></span> <span data-ttu-id="cd902-156">您也可以使用 **CF \_ NOSIMULATIONS** 值，限制對話方塊針對某些字型顯示的可用樣式。</span><span class="sxs-lookup"><span data-stu-id="cd902-156">You can also restrict the available styles that the dialog box displays for some fonts by using the **CF\_NOSIMULATIONS** value.</span></span>

<span data-ttu-id="cd902-157">從 Windows 7 開始，對話方塊中顯示的字型清單會根據使用者的顯示字型而受到限制。</span><span class="sxs-lookup"><span data-stu-id="cd902-157">Starting with Windows 7, the list of fonts displayed in the dialog box is restricted based on the user's shown fonts.</span></span> <span data-ttu-id="cd902-158">若要移除限制，請設定 **CF \_ INACTIVEFONTS** 旗標。</span><span class="sxs-lookup"><span data-stu-id="cd902-158">To remove the restriction, set the **CF\_INACTIVEFONTS** flag.</span></span>

<span data-ttu-id="cd902-159">**限制使用者可指定的字型名稱、樣式和點大小**</span><span class="sxs-lookup"><span data-stu-id="cd902-159">**To restrict the typeface names, styles, and point sizes that the user can specify**</span></span>

1.  <span data-ttu-id="cd902-160">設定 **CF \_ FORCEFONTEXIST** 旗標，以限制使用者只指定有效的字型名稱、樣式，以及對話方塊中所列的點大小。</span><span class="sxs-lookup"><span data-stu-id="cd902-160">Set the **CF\_FORCEFONTEXIST** flag to restrict the user to specifying only valid typeface names, styles, and point sizes listed in the dialog box.</span></span>
2.  <span data-ttu-id="cd902-161">設定 **CF \_ LIMITSIZE** 旗標，以限制使用者在 **nSizeMin** 和 **nSizeMax** 成員所指定的範圍中指定點大小。</span><span class="sxs-lookup"><span data-stu-id="cd902-161">Set the **CF\_LIMITSIZE** flag to restrict the user to specifying point sizes in the range specified by the **nSizeMin** and **nSizeMax** members.</span></span>

<span data-ttu-id="cd902-162">**限制或停用腳本下拉式方塊**</span><span class="sxs-lookup"><span data-stu-id="cd902-162">**To restrict or disable the Scripts combo box**</span></span>

-   <span data-ttu-id="cd902-163">將 **cf \_ NOSCRIPTSEL** 旗標設定為停用 [ **腳本** ] 下拉式方塊，或設定 **cf \_ SELECTSCRIPT** 旗標，將 [ **腳本** ] 下拉式方塊中的選取範圍限制為指定的字元集。</span><span class="sxs-lookup"><span data-stu-id="cd902-163">Set the **CF\_NOSCRIPTSEL** flag to disable the **Scripts** combo box, or set the **CF\_SELECTSCRIPT** flag to restrict selections in the **Scripts** combo box to a specified character set.</span></span>

## <a name="customizing-the-font-dialog-box-on-earlier-versions-of-windows"></a><span data-ttu-id="cd902-164">在舊版 Windows 上自訂字型對話方塊</span><span class="sxs-lookup"><span data-stu-id="cd902-164">Customizing the Font Dialog Box on earlier versions of Windows</span></span>

<span data-ttu-id="cd902-165">您可以提供 [ **字型** ] 對話方塊的自訂範本，例如，如果您想要包含應用程式特有的其他控制項。</span><span class="sxs-lookup"><span data-stu-id="cd902-165">You can provide a custom template for the **Font** dialog box, for example, if you want to include additional controls that are unique to your application.</span></span> <span data-ttu-id="cd902-166">[**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)函式會使用您的自訂範本來取代預設範本。</span><span class="sxs-lookup"><span data-stu-id="cd902-166">The [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function uses your custom template in place of the default template.</span></span>

<span data-ttu-id="cd902-167">**提供 [字型] 對話方塊的自訂範本**</span><span class="sxs-lookup"><span data-stu-id="cd902-167">**To provide a custom template for the Font dialog box**</span></span>

1.  <span data-ttu-id="cd902-168">藉由修改 Font-family 檔案中指定的預設範本來建立自訂範本。</span><span class="sxs-lookup"><span data-stu-id="cd902-168">Create the custom template by modifying the default template specified in the Font.dlg file.</span></span> <span data-ttu-id="cd902-169">在 [預設字型] 對話方塊範本中使用的控制項識別碼是在 Dlgs 檔中定義。</span><span class="sxs-lookup"><span data-stu-id="cd902-169">The control identifiers used in the default Font dialog template are defined in the Dlgs.h file.</span></span>
2.  <span data-ttu-id="cd902-170">使用 [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) 結構來啟用範本，如下所示：</span><span class="sxs-lookup"><span data-stu-id="cd902-170">Use the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure to enable the template as follows:</span></span>
    -   <span data-ttu-id="cd902-171">如果您的自訂範本是應用程式或動態連結程式庫中的資源，請在 **旗標** 成員中設定 **CF \_ ENABLETEMPLATE** 旗標。</span><span class="sxs-lookup"><span data-stu-id="cd902-171">If your custom template is a resource in an application or dynamic link library, set the **CF\_ENABLETEMPLATE** flag in the **Flags** member.</span></span> <span data-ttu-id="cd902-172">使用結構的 **hInstance** 和 **lpTemplateName** 成員來識別模組和資源名稱。</span><span class="sxs-lookup"><span data-stu-id="cd902-172">Use the **hInstance** and **lpTemplateName** members of the structure to identify the module and resource name.</span></span>
    -   <span data-ttu-id="cd902-173">如果您的自訂範本已在記憶體中，請設定 **CF \_ ENABLETEMPLATEHANDLE** 旗標。</span><span class="sxs-lookup"><span data-stu-id="cd902-173">If your custom template is already in memory, set the **CF\_ENABLETEMPLATEHANDLE** flag.</span></span> <span data-ttu-id="cd902-174">您可以使用 **hInstance** 成員來識別包含範本的記憶體物件。</span><span class="sxs-lookup"><span data-stu-id="cd902-174">Use the **hInstance** member to identify the memory object that contains the template.</span></span>

<span data-ttu-id="cd902-175">您可以針對 [**字型**] 對話方塊提供 [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)攔截程式。</span><span class="sxs-lookup"><span data-stu-id="cd902-175">You can provide a [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) hook procedure for the **Font** dialog box.</span></span> <span data-ttu-id="cd902-176">攔截程式可以處理傳送至對話方塊的訊息，並將訊息傳送至對話方塊。</span><span class="sxs-lookup"><span data-stu-id="cd902-176">The hook procedure can process messages sent to the dialog box and send messages to the dialog box.</span></span> <span data-ttu-id="cd902-177">如果您使用自訂範本來定義其他控制項，您必須提供攔截程式來處理控制項的輸入。</span><span class="sxs-lookup"><span data-stu-id="cd902-177">If you use a custom template to define additional controls, you must provide a hook procedure to process input for your controls.</span></span>

<span data-ttu-id="cd902-178">**若要啟用 [字型] 對話方塊的勾點程式**</span><span class="sxs-lookup"><span data-stu-id="cd902-178">**To enable a hook procedure for the Font dialog box**</span></span>

1.  <span data-ttu-id="cd902-179">在 [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)結構的 **旗標** 成員中設定 **CF \_ ENABLEHOOK** 旗標。</span><span class="sxs-lookup"><span data-stu-id="cd902-179">Set the **CF\_ENABLEHOOK** flag in the **Flags** member of the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure.</span></span>
2.  <span data-ttu-id="cd902-180">在 **lpfnHook** 成員中指定攔截程式的位址。</span><span class="sxs-lookup"><span data-stu-id="cd902-180">Specify the address of the hook procedure in the **lpfnHook** member.</span></span>

<span data-ttu-id="cd902-181">處理 [**wm \_ INITDIALOG**](wm-initdialog.md) 訊息之後，對話方塊程式會將 **wm \_ INITDIALOG** 訊息傳送到攔截程式。</span><span class="sxs-lookup"><span data-stu-id="cd902-181">After processing the [**WM\_INITDIALOG**](wm-initdialog.md) message, the dialog box procedure sends a **WM\_INITDIALOG** message to the hook procedure.</span></span> <span data-ttu-id="cd902-182">此訊息的 *lParam* 參數是用來初始化對話方塊之 [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="cd902-182">The *lParam* parameter of this message is a pointer to the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure that is used to initialize the dialog box.</span></span>

<span data-ttu-id="cd902-183">攔截程式可以將 [**wm \_ CHOOSEFONT \_ GETLOGFONT**](wm-choosefont-getlogfont.md)、 [**wm \_ CHOOSEFONT \_ SETLOGFONT**](wm-choosefont-setlogfont.md)和 [**wm \_ CHOOSEFONT \_ SETFLAGS**](wm-choosefont-setflags.md) 訊息傳送至對話方塊，以取得和設定對話方塊的目前值和旗標。</span><span class="sxs-lookup"><span data-stu-id="cd902-183">The hook procedure can send the [**WM\_CHOOSEFONT\_GETLOGFONT**](wm-choosefont-getlogfont.md), [**WM\_CHOOSEFONT\_SETLOGFONT**](wm-choosefont-setlogfont.md), and [**WM\_CHOOSEFONT\_SETFLAGS**](wm-choosefont-setflags.md) messages to the dialog box to get and set the current values and flags of the dialog box.</span></span>

## <a name="customizing-the-font-dialog-box-on-windows-7"></a><span data-ttu-id="cd902-184">在 Windows 7 上自訂字型對話方塊</span><span class="sxs-lookup"><span data-stu-id="cd902-184">Customizing the Font Dialog Box on Windows 7</span></span>

<span data-ttu-id="cd902-185">下列螢幕擷取畫面顯示 Windows 7 中的一般 **字型** 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="cd902-185">The following screen shot shows a typical **Font** dialog box in Windows 7.</span></span>

![顯示 [字型 dialob] 方塊的螢幕擷取畫面](images/fontdialogboxwin7.png)

<span data-ttu-id="cd902-187">在舊版的 Windows 中，font-family 範本檔案包含一個預設 ChooseFont 範本。</span><span class="sxs-lookup"><span data-stu-id="cd902-187">In earlier Windows versions, the font.dlg template file contains one default ChooseFont template.</span></span> <span data-ttu-id="cd902-188">Windows 7 上的 font-size 範本檔包含兩個預設範本：舊版 Windows 的預設範本和新的 Windows 7 ChooseFont 範本。</span><span class="sxs-lookup"><span data-stu-id="cd902-188">The font.dlg template file on Windows 7 contains two default templates: the default template from earlier Windows versions and the new Windows 7 ChooseFont template.</span></span> <span data-ttu-id="cd902-189">因此，當您在 Windows 7 上自訂 [ **字型** ] 對話方塊時，您必須考慮下列問題。</span><span class="sxs-lookup"><span data-stu-id="cd902-189">Therefore, when you customize the **Font** dialog box on Windows 7, you must consider the following issues.</span></span>

1.  <span data-ttu-id="cd902-190">當您針對在 Windows 7 上執行的應用程式建立自訂範本時，請使用新的範本。</span><span class="sxs-lookup"><span data-stu-id="cd902-190">Use the new template when you create custom templates for applications that run on Windows 7.</span></span> <span data-ttu-id="cd902-191">這個新範本包含連結控制項，可讓使用者按一下以啟動字型 **主控台** 視窗，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="cd902-191">This new template contains a link control that the user can click to launch the **Fonts Control Panel** window, as shown in the following screen shot.</span></span>

    ![顯示 windows 7 中字型 [控制台] 的螢幕擷取畫面](images/fontcontrolpanelforwin7.png)

2.  <span data-ttu-id="cd902-193">若要使用此連結控制項，呼叫的應用程式必須使用 COMCTL32.DLL 6 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="cd902-193">To use this link control, your calling application must use the COMCTL32.DLL version 6 or later.</span></span> <span data-ttu-id="cd902-194">否則，當 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) 函式嘗試在您的自訂範本中建立連結控制項時，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="cd902-194">Otherwise, the [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function returns an error when it tries to create the link control in your custom template.</span></span> <span data-ttu-id="cd902-195">若要判斷是否已啟用此控制項，請針對 COMCTL32.DLL 版本6.0 編譯您的呼叫應用程式。</span><span class="sxs-lookup"><span data-stu-id="cd902-195">To determine if this control is enabled, compile your calling application against COMCTL32.DLL version 6.0.</span></span> <span data-ttu-id="cd902-196">如需詳細資訊，請參閱 [使用通用控制項啟用視覺化樣式](/previous-versions//ms649781(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="cd902-196">For more information, see [Enabling Visual Styles with Common Controls](/previous-versions//ms649781(v=vs.85)).</span></span>
3.  <span data-ttu-id="cd902-197">如果您的應用程式使用 COMCTL32.DLL 5.0 版或更早版本，當您建立自訂範本時，必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="cd902-197">If your application uses COMCTL32.DLL version 5.0 or earlier, you must do the following when you create a custom template:</span></span>

    -   <span data-ttu-id="cd902-198">將控制項指定為 **按鈕**。</span><span class="sxs-lookup"><span data-stu-id="cd902-198">Specify the control as a **PUSHBUTTON**.</span></span> <span data-ttu-id="cd902-199">用來啟動字型 **主控台** 的控制項將會顯示為按鈕，而不是連結。</span><span class="sxs-lookup"><span data-stu-id="cd902-199">The control used to launch the **Fonts Control Panel** will appear as a button rather than as a link.</span></span>
    -   <span data-ttu-id="cd902-200">取代下列字型中的文字： d：</span><span class="sxs-lookup"><span data-stu-id="cd902-200">Replace the following text in the font.dlg:</span></span>

        `CONTROL         "<A>Show more fonts</A>", IDC_MANAGE_LINK, "SysLink", WS_TABSTOP, 7, 199, 227, 9`

        <span data-ttu-id="cd902-201">使用下列文字：</span><span class="sxs-lookup"><span data-stu-id="cd902-201">with the following text:</span></span>

        `PUSHBUTTON      "S&how more fonts", IDC_MANAGE_LINK, 7, 199, 74, 14 , WS_TABSTOP`

    -   <span data-ttu-id="cd902-202">為確保您的應用程式使用自訂範本，您必須使用 **CF \_ ENABLETEMPLATE** 旗標來指定自訂範本、根據 Windows 7 ChooseFont 範本建立自訂範本，然後選擇性地啟用攔截程式。</span><span class="sxs-lookup"><span data-stu-id="cd902-202">To ensure that your application uses a custom template, you must specify a custom template with the **CF\_ENABLETEMPLATE** flag, create a custom template based on the Windows 7 ChooseFont template, and then optionally enable a hook procedure.</span></span>

        <span data-ttu-id="cd902-203">如果您在未建立自訂範本的情況下啟用攔截程式，將會載入舊版 Windows 的預設 ChooseFont 範本。</span><span class="sxs-lookup"><span data-stu-id="cd902-203">If you enable a hook procedure without creating a custom template, the default ChooseFont template for earlier Windows versions will be loaded.</span></span>

> [!Note]  
> <span data-ttu-id="cd902-204">您必須根據應用程式所編譯的 COMMCTL.DLL 版本，在新的範本中指定 **控制項** 或 **按鈕** 控制項類型。</span><span class="sxs-lookup"><span data-stu-id="cd902-204">You must specify the **CONTROL** or **PUSHBUTTON** control type in your new template, depending on the version of COMMCTL.DLL that your application compiles against.</span></span> <span data-ttu-id="cd902-205">另請注意，當您的應用程式在舊版 Windows 作業系統上執行時，就無法使用 Windows 7 特有的功能，例如，字型清單和延伸系列的 WYSIWYG 顯示。</span><span class="sxs-lookup"><span data-stu-id="cd902-205">Also note that Windows 7 specific features, such as WYSIWYG display of font lists and extended families, are not available when your applications run on earlier versions of the Windows operating system.</span></span>

 

 

 