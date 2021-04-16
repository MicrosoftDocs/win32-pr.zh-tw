---
title: 尋找和取代對話方塊
description: 顯示非強制回應對話方塊，可讓使用者指定要搜尋的字串，以及搜尋檔中的文字時要使用的選項。
ms.assetid: c8c035bf-795d-42a7-abc6-168dea43e6e9
keywords:
- Windows 消費者介面，使用者輸入
- Windows 消費者介面、通用對話方塊程式庫
- 使用者輸入、通用對話方塊程式庫
- 正在捕獲使用者輸入，通用對話方塊程式庫
- 通用對話方塊程式庫
- 通用對話方塊
- 尋找對話方塊
- 取代對話方塊
- 自訂尋找對話方塊
- 自訂取代對話方塊
- 預先定義的對話方塊
- 對話方塊、尋找
- 對話方塊、取代
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e3cf2c5217d586c0a5ada74fb7dd72aaca5f804
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104553831"
---
# <a name="find-and-replace-dialog-boxes"></a><span data-ttu-id="fae19-116">尋找和取代對話方塊</span><span class="sxs-lookup"><span data-stu-id="fae19-116">Find and Replace Dialog Boxes</span></span>

<span data-ttu-id="fae19-117">顯示非強制回應對話方塊，可讓使用者指定要搜尋的字串，以及搜尋檔中的文字時要使用的選項。</span><span class="sxs-lookup"><span data-stu-id="fae19-117">Displays a modeless dialog box that allows the user to specify a string to search for, as well as options to use when searching for text in a document.</span></span> <span data-ttu-id="fae19-118">[ **取代** ] 對話方塊可讓使用者指定要搜尋的字串和取代字串，以及控制操作的選項。</span><span class="sxs-lookup"><span data-stu-id="fae19-118">The **Replace** dialog box lets the user specify a string to search for and a replacement string, as well as options to control the operation.</span></span>

<span data-ttu-id="fae19-119">您可以藉由初始化 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)結構並將結構傳遞至 [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta)函式，來建立和顯示 [**尋找**] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="fae19-119">You create and display a **Find** dialog box by initializing a [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure and passing the structure to the [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) function.</span></span> <span data-ttu-id="fae19-120">下圖顯示一般 [ **尋找** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="fae19-120">The following illustration shows a typical **Find** dialog box.</span></span>

![尋找對話方塊](images/finddialogboxxp.png)

<span data-ttu-id="fae19-122">您可以藉由初始化 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)結構並將結構傳遞至 [**replacer.replacetext**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta)函式，來建立和顯示 [**取代**] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="fae19-122">You create and display a **Replace** dialog box by initializing a [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure and passing the structure to the [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) function.</span></span> <span data-ttu-id="fae19-123">下圖顯示典型的 [ **取代** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="fae19-123">The following illustration shows a typical **Replace** dialog box.</span></span>

![取代對話方塊](images/replacedialogboxxp.png)

<span data-ttu-id="fae19-125">不同于其他常見的對話方塊，[ **尋找** 和 **取代** ] 對話方塊是無模式。</span><span class="sxs-lookup"><span data-stu-id="fae19-125">Unlike other common dialog boxes, the **Find** and **Replace** dialog boxes are modeless.</span></span> <span data-ttu-id="fae19-126">非強制回應對話方塊可讓使用者在對話方塊和建立它的視窗之間切換。</span><span class="sxs-lookup"><span data-stu-id="fae19-126">A modeless dialog box allows the user to switch between the dialog box and the window that created it.</span></span> <span data-ttu-id="fae19-127">這適用于讓使用者搜尋字串、切換至應用程式視窗以處理字串，然後切換回對話方塊來搜尋另一個字串，而不需要重複開啟對話方塊所需的命令。</span><span class="sxs-lookup"><span data-stu-id="fae19-127">This is useful for letting the user search for a string, switch to the application window to work on the string, and switch back to the dialog box to search for another string without repeating the command needed to open the dialog box.</span></span>

<span data-ttu-id="fae19-128">如果 [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) 或 [**replacer.replacetext**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) 函式成功建立對話方塊，則會將控制碼傳回至對話方塊。</span><span class="sxs-lookup"><span data-stu-id="fae19-128">If the [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) or [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) function successfully creates the dialog box, it returns a handle to the dialog box.</span></span> <span data-ttu-id="fae19-129">您可以使用此控制碼來移動和與對話方塊進行通訊。</span><span class="sxs-lookup"><span data-stu-id="fae19-129">You can use this handle to move and communicate with the dialog box.</span></span> <span data-ttu-id="fae19-130">如果函數無法建立對話方塊，則會傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fae19-130">If the function cannot create the dialog box, it returns **NULL**.</span></span> <span data-ttu-id="fae19-131">您可以藉由呼叫 [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) 函式來取出擴充的錯誤值，以判斷錯誤的原因。</span><span class="sxs-lookup"><span data-stu-id="fae19-131">You can determine the cause of an error by calling the [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) function to retrieve the extended error value.</span></span>

<span data-ttu-id="fae19-132">本節將討論下列主題。</span><span class="sxs-lookup"><span data-stu-id="fae19-132">This section discusses the following topics.</span></span>

-   [<span data-ttu-id="fae19-133">FINDMSGSTRING 註冊的訊息</span><span class="sxs-lookup"><span data-stu-id="fae19-133">The FINDMSGSTRING Registered Message</span></span>](#the-findmsgstring-registered-message)
-   <span data-ttu-id="fae19-134">[自訂 [尋找或取代] 對話方塊](#customizing-the-find-or-replace-dialog-box)</span><span class="sxs-lookup"><span data-stu-id="fae19-134">[Customizing the Find or Replace Dialog Box](#customizing-the-find-or-replace-dialog-box)</span></span>

## <a name="the-findmsgstring-registered-message"></a><span data-ttu-id="fae19-135">FINDMSGSTRING 註冊的訊息</span><span class="sxs-lookup"><span data-stu-id="fae19-135">The FINDMSGSTRING Registered Message</span></span>

<span data-ttu-id="fae19-136">在建立 [ **尋找** 或 **取代** ] 對話方塊之前，您必須呼叫 [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) 函式來取得 [**FINDMSGSTRING**](findmsgstring.md) 註冊訊息的訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="fae19-136">Before creating a **Find** or **Replace** dialog box, you must call the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get a message identifier for the [**FINDMSGSTRING**](findmsgstring.md) registered message.</span></span> <span data-ttu-id="fae19-137">然後，您可以使用識別碼來偵測和處理從對話方塊傳送的訊息。</span><span class="sxs-lookup"><span data-stu-id="fae19-137">You can then use the identifier to detect and process messages sent from the dialog box.</span></span> <span data-ttu-id="fae19-138">當使用者按一下對話方塊中的 [ **尋找下一個**]、[ **取代**] 或 [ **取代全部** ] 按鈕時，對話方塊程式會將 **FINDMSGSTRING** 訊息傳送至主控視窗的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="fae19-138">When the user clicks the **Find Next**, **Replace**, or **Replace All** button in a dialog box, the dialog box procedure sends a **FINDMSGSTRING** message to the window procedure of the owner window.</span></span> <span data-ttu-id="fae19-139">當您建立對話方塊時， [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)結構的 **hwndOwner** 成員會識別擁有者視窗。</span><span class="sxs-lookup"><span data-stu-id="fae19-139">When you create the dialog box, the **hwndOwner** member of the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure identifies the owner window.</span></span>

<span data-ttu-id="fae19-140">[**FINDMSGSTRING**](findmsgstring.md)訊息的 *lParam* 參數是您在建立對話方塊時所指定之 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="fae19-140">The *lParam* parameter of a [**FINDMSGSTRING**](findmsgstring.md) message is a pointer to the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure that you specified when you created the dialog box.</span></span> <span data-ttu-id="fae19-141">傳送訊息之前，對話方塊會以最新的使用者輸入設定此結構的成員，包括要搜尋的字串、取代字串 (如果有任何) ，以及尋找和取代作業的選項。</span><span class="sxs-lookup"><span data-stu-id="fae19-141">Before sending the message, the dialog box sets the members of this structure with the latest user input, including the string to search for, the replacement string (if any), and options for the find-and-replace operation.</span></span>

<span data-ttu-id="fae19-142">在 [**FINDMSGSTRING**](findmsgstring.md)訊息中， [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)結構的 **flags** 成員會包含下列其中一個旗標，以指出造成訊息的事件。</span><span class="sxs-lookup"><span data-stu-id="fae19-142">In a [**FINDMSGSTRING**](findmsgstring.md) message, the **Flags** member of the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure includes one of the following flags to indicate the event that caused the message.</span></span>



| <span data-ttu-id="fae19-143">旗標</span><span class="sxs-lookup"><span data-stu-id="fae19-143">Flag</span></span>               | <span data-ttu-id="fae19-144">意義</span><span class="sxs-lookup"><span data-stu-id="fae19-144">Meaning</span></span>                                                                                                                                                                                                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fae19-145">**FR \_ DIALOGTERM**</span><span class="sxs-lookup"><span data-stu-id="fae19-145">**FR\_DIALOGTERM**</span></span> | <span data-ttu-id="fae19-146">對話方塊正在關閉。</span><span class="sxs-lookup"><span data-stu-id="fae19-146">The dialog box is closing.</span></span> <span data-ttu-id="fae19-147">擁有者視窗處理此訊息之後，對話方塊的控制碼將不再有效。</span><span class="sxs-lookup"><span data-stu-id="fae19-147">After the owner window processes this message, a handle to the dialog box is no longer valid.</span></span>                                                                                    |
| <span data-ttu-id="fae19-148">**FR \_ FINDNEXT**</span><span class="sxs-lookup"><span data-stu-id="fae19-148">**FR\_FINDNEXT**</span></span>   | <span data-ttu-id="fae19-149">使用者按一下 [**尋找** 或 **取代**] 對話方塊中的 [**尋找下一個]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="fae19-149">The user clicked the **Find Next** button in a **Find** or **Replace** dialog box.</span></span> <span data-ttu-id="fae19-150">**LpstrFindWhat** 成員會指定要搜尋的字串。</span><span class="sxs-lookup"><span data-stu-id="fae19-150">The **lpstrFindWhat** member specifies the string to search for.</span></span>                                                         |
| <span data-ttu-id="fae19-151">**FR \_ 取代**</span><span class="sxs-lookup"><span data-stu-id="fae19-151">**FR\_REPLACE**</span></span>    | <span data-ttu-id="fae19-152">使用者按一下 [**取代**] 對話方塊中的 [**取代**] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="fae19-152">The user clicked the **Replace** button in a **Replace** dialog box.</span></span> <span data-ttu-id="fae19-153">**LpstrFindWhat** 成員會指定要取代的字串，而 **lpstrReplaceWith** 成員會指定取代字串。</span><span class="sxs-lookup"><span data-stu-id="fae19-153">The **lpstrFindWhat** member specifies the string to replace and the **lpstrReplaceWith** member specifies the replacement string.</span></span>     |
| <span data-ttu-id="fae19-154">**FR \_ 型全部型**</span><span class="sxs-lookup"><span data-stu-id="fae19-154">**FR\_REPLACEALL**</span></span> | <span data-ttu-id="fae19-155">使用者按一下 [**取代**] 對話方塊中的 [**全部取代**] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="fae19-155">The user clicked the **Replace All** button in a **Replace** dialog box.</span></span> <span data-ttu-id="fae19-156">**LpstrFindWhat** 成員會指定要取代的字串，而 **lpstrReplaceWith** 成員會指定取代字串。</span><span class="sxs-lookup"><span data-stu-id="fae19-156">The **lpstrFindWhat** member specifies the string to replace and the **lpstrReplaceWith** member specifies the replacement string.</span></span> |



 

<span data-ttu-id="fae19-157">如果是 [ **尋找下一個]** 或 [ **取代全部** ] 訊息， **旗標** 成員可以包含下列旗標的任何組合，以表示搜尋選項。</span><span class="sxs-lookup"><span data-stu-id="fae19-157">For a **Find Next** or **Replace All** message, the **Flags** member can include any combination of the following flags to indicate the search options.</span></span>



| <span data-ttu-id="fae19-158">旗標</span><span class="sxs-lookup"><span data-stu-id="fae19-158">Flag</span></span>              | <span data-ttu-id="fae19-159">意義</span><span class="sxs-lookup"><span data-stu-id="fae19-159">Meaning</span></span>                                                                                                                                                                                                                                                                                          |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fae19-160">**FR-FR \_**</span><span class="sxs-lookup"><span data-stu-id="fae19-160">**FR\_DOWN**</span></span>      | <span data-ttu-id="fae19-161">如果設定，則會選取 [方向] 選項按鈕的 **向下** 按鈕，表示使用者想要從目前的位置搜尋至檔的結尾。</span><span class="sxs-lookup"><span data-stu-id="fae19-161">If set, the **Down** button of the direction radio buttons is selected, indicating that user wants to search from the current location to the end of the document.</span></span> <span data-ttu-id="fae19-162">如果未設定 **FR \_ DOWN** ，則會選取 [ **向上** ] 按鈕，讓使用者想要搜尋檔的開頭。</span><span class="sxs-lookup"><span data-stu-id="fae19-162">If **FR\_DOWN** is not set, the **Up** button is selected so the user wants to search to the beginning of the document.</span></span>       |
| <span data-ttu-id="fae19-163">**FR \_ MATCHCASE**</span><span class="sxs-lookup"><span data-stu-id="fae19-163">**FR\_MATCHCASE**</span></span> | <span data-ttu-id="fae19-164">如果設定，則會選取 [ **符合大小寫** ] 核取方塊，表示使用者想要搜尋區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="fae19-164">If set, the **Match Case** check box is selected, indicating that the user wants the search to be case sensitive.</span></span> <span data-ttu-id="fae19-165">如果未設定 **FR \_ MATCHCASE** ，則不會選取此核取方塊，讓搜尋不會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="fae19-165">If **FR\_MATCHCASE** is not set, the check box is unselected so that the search can be case insensitive.</span></span>                                                                       |
| <span data-ttu-id="fae19-166">**FR \_ WHOLEWORD**</span><span class="sxs-lookup"><span data-stu-id="fae19-166">**FR\_WHOLEWORD**</span></span> | <span data-ttu-id="fae19-167">如果設定，則會選取 [ **僅符合全字** 組] 核取方塊，表示使用者只想搜尋符合搜尋字串的全字組。</span><span class="sxs-lookup"><span data-stu-id="fae19-167">If set, the **Match Whole Word Only** check box is selected, indicating that the user wants to search only for whole words that match the search string.</span></span> <span data-ttu-id="fae19-168">如果未設定 **FR \_ WHOLEWORD** ，則不會選取此核取方塊，所以您也應該搜尋符合搜尋字串的文字片段。</span><span class="sxs-lookup"><span data-stu-id="fae19-168">If **FR\_WHOLEWORD** is not set, the check box is unselected so you should also search for word fragments that match the search string.</span></span> |



 

## <a name="customizing-the-find-or-replace-dialog-box"></a><span data-ttu-id="fae19-169">自訂 [尋找或取代] 對話方塊</span><span class="sxs-lookup"><span data-stu-id="fae19-169">Customizing the Find or Replace Dialog Box</span></span>

<span data-ttu-id="fae19-170">若要自訂 [ **尋找** 或 **取代** ] 對話方塊，您可以使用下列任何一種方法：</span><span class="sxs-lookup"><span data-stu-id="fae19-170">To customize a **Find** or **Replace** dialog box, you can use any of the following methods:</span></span>

-   <span data-ttu-id="fae19-171">當您建立對話方塊時，在 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) 結構中指定值</span><span class="sxs-lookup"><span data-stu-id="fae19-171">Specify values in the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure when you create the dialog box</span></span>
-   <span data-ttu-id="fae19-172">提供自訂範本</span><span class="sxs-lookup"><span data-stu-id="fae19-172">Provide a custom template</span></span>
-   <span data-ttu-id="fae19-173">提供勾點程式</span><span class="sxs-lookup"><span data-stu-id="fae19-173">Provide a hook procedure</span></span>

<span data-ttu-id="fae19-174">當您建立 [**尋找** 或 **取代**] 對話方塊時，可以在 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)結構的 **旗標** 成員中設定旗標，以隱藏或停用任何搜尋選項控制項。</span><span class="sxs-lookup"><span data-stu-id="fae19-174">When you create a **Find** or **Replace** dialog box, you can set flags in the **Flags** member of the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure to hide or disable any of the search option controls.</span></span> <span data-ttu-id="fae19-175">例如，您可以將 FR \_ NOMATCHCASE 旗標設定為停 **用 [符合大小寫** ] 核取方塊，或將 [fr HIDEMATCHCASE] 旗標設 \_ 為隱藏。</span><span class="sxs-lookup"><span data-stu-id="fae19-175">For example, you can set the FR\_NOMATCHCASE flag to disable the **Match Case** check box or set the FR\_HIDEMATCHCASE flag to hide it.</span></span>

<span data-ttu-id="fae19-176">您可以提供 [ **尋找** 或 **取代** ] 對話方塊的自訂範本，例如，如果您想要包含應用程式特有的其他控制項。</span><span class="sxs-lookup"><span data-stu-id="fae19-176">You can provide a custom template for a **Find** or **Replace** dialog box, for example, if you want to include additional controls that are unique to your application.</span></span> <span data-ttu-id="fae19-177">[**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta)和 [**replacer.replacetext**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta)函數會使用您的自訂範本來取代預設範本。</span><span class="sxs-lookup"><span data-stu-id="fae19-177">The [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) and [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) functions use your custom template in place of the default template.</span></span>

<span data-ttu-id="fae19-178">**若要提供尋找或取代對話方塊的自訂範本**</span><span class="sxs-lookup"><span data-stu-id="fae19-178">**To provide a custom template for a Find or Replace dialog box**</span></span>

1.  <span data-ttu-id="fae19-179">藉由修改 Findtext 檔案中指定的預設範本來建立自訂範本。</span><span class="sxs-lookup"><span data-stu-id="fae19-179">Create the custom template by modifying the default template specified in the Findtext.dlg file.</span></span> <span data-ttu-id="fae19-180">預設的 [ **尋找** ] 或 [ **取代** ] 對話方塊範本中所使用的控制項識別碼會定義在 Dlgs .h 檔案中。</span><span class="sxs-lookup"><span data-stu-id="fae19-180">The control identifiers used in the default **Find** or **Replace** dialog template are defined in the Dlgs.h file.</span></span>
2.  <span data-ttu-id="fae19-181">使用 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) 結構來啟用範本，如下所示：</span><span class="sxs-lookup"><span data-stu-id="fae19-181">Use the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure to enable the template as follows:</span></span>
    -   -   <span data-ttu-id="fae19-182">如果您的自訂範本是應用程式或動態連結程式庫中的資源，請 \_ 在 **旗標** 成員中設定 FR ENABLETEMPLATE 旗標。</span><span class="sxs-lookup"><span data-stu-id="fae19-182">If your custom template is a resource in an application or dynamic-link library, set the FR\_ENABLETEMPLATE flag in the **Flags** member.</span></span> <span data-ttu-id="fae19-183">使用結構的 **hInstance** 和 **lpTemplateName** 成員來識別模組和資源名稱。</span><span class="sxs-lookup"><span data-stu-id="fae19-183">Use the **hInstance** and **lpTemplateName** members of the structure to identify the module and resource name.</span></span>

            <span data-ttu-id="fae19-184">-或者-</span><span class="sxs-lookup"><span data-stu-id="fae19-184">-Or-</span></span>

        -   <span data-ttu-id="fae19-185">如果您的自訂範本已在記憶體中，請設定 FR \_ ENABLETEMPLATEHANDLE 旗標。</span><span class="sxs-lookup"><span data-stu-id="fae19-185">If your custom template is already in memory, set the FR\_ENABLETEMPLATEHANDLE flag.</span></span> <span data-ttu-id="fae19-186">您可以使用 **hInstance** 成員來識別包含範本的記憶體物件。</span><span class="sxs-lookup"><span data-stu-id="fae19-186">Use the **hInstance** member to identify the memory object that contains the template.</span></span>

<span data-ttu-id="fae19-187">您可以在 [**尋找** 或 **取代**] 對話方塊中提供 [**FRHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpfrhookproc)的勾點程式。</span><span class="sxs-lookup"><span data-stu-id="fae19-187">You can provide an [**FRHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpfrhookproc) hook procedure for a **Find** or **Replace** dialog box.</span></span> <span data-ttu-id="fae19-188">攔截程式可以處理傳送至對話方塊的訊息。</span><span class="sxs-lookup"><span data-stu-id="fae19-188">The hook procedure can process messages sent to the dialog box.</span></span> <span data-ttu-id="fae19-189">如果您使用自訂範本來定義其他控制項，您必須提供攔截程式來處理控制項的輸入。</span><span class="sxs-lookup"><span data-stu-id="fae19-189">If you use a custom template to define additional controls, you must provide a hook procedure to process input for your controls.</span></span>

<span data-ttu-id="fae19-190">**若要啟用尋找或取代對話方塊的勾點程式**</span><span class="sxs-lookup"><span data-stu-id="fae19-190">**To enable a hook procedure for a Find or Replace dialog box**</span></span>

1.  <span data-ttu-id="fae19-191">\_在 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)結構的 **FLAGS** 成員中設定 FR ENABLEHOOK 旗標。</span><span class="sxs-lookup"><span data-stu-id="fae19-191">Set the FR\_ENABLEHOOK flag in the **Flags** member of the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure.</span></span>
2.  <span data-ttu-id="fae19-192">在 **lpfnHook** 成員中指定攔截程式的位址。</span><span class="sxs-lookup"><span data-stu-id="fae19-192">Specify the address of the hook procedure in the **lpfnHook** member.</span></span>

<span data-ttu-id="fae19-193">處理其 [**WM \_ INITDIALOG**](wm-initdialog.md) 訊息之後，對話方塊程式會將 **wm \_ INITDIALOG** 訊息傳送到攔截程式。</span><span class="sxs-lookup"><span data-stu-id="fae19-193">After processing its [**WM\_INITDIALOG**](wm-initdialog.md) message, the dialog box procedure sends a **WM\_INITDIALOG** message to the hook procedure.</span></span> <span data-ttu-id="fae19-194">此訊息的 *lParam* 參數是用來初始化對話方塊之 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="fae19-194">The *lParam* parameter of this message is a pointer to the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure used to initialize the dialog box.</span></span>

<span data-ttu-id="fae19-195">如果攔截程式傳回 **FALSE** 以回應 [**WM \_ INITDIALOG**](wm-initdialog.md) 訊息，則不會顯示此對話方塊，除非攔截程式顯示此對話方塊。</span><span class="sxs-lookup"><span data-stu-id="fae19-195">If the hook procedure returns **FALSE** in response to the [**WM\_INITDIALOG**](wm-initdialog.md) message, the dialog box will not be shown unless the hook procedure displays it.</span></span> <span data-ttu-id="fae19-196">若要這樣做，請先執行任何其他繪製作業，然後呼叫 [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) 和 [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) 函數。</span><span class="sxs-lookup"><span data-stu-id="fae19-196">To do this, first perform any other paint operations, and then call the [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) and [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) functions.</span></span> <span data-ttu-id="fae19-197">下列程式碼提供一個範例：</span><span class="sxs-lookup"><span data-stu-id="fae19-197">The following code provides an example:</span></span>


```
// We've returned FALSE in response to WM_INITDIALOG. 
// We've performed any other paint operations. 
// Now we display the dialog box. 
ShowWindow(hDlg, SW_SHOWNORMAL); 
UpdateWindow(hDlg); 
```



 

 