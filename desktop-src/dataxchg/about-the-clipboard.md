---
title: 關於剪貼簿
description: 本節討論剪貼簿。
ms.assetid: 14c91730-a668-495b-9ec6-b835234821a5
keywords:
- 剪貼簿，關於
- 剪貼簿，格式
- 剪貼簿、命令
- 剪貼簿、windows
- 剪貼簿、序號
- 剪貼簿，檢視器
- 剪貼簿，檢視器視窗
- 剪貼簿、顯示格式
- 剪貼簿，擁有者顯示格式
- 顯示剪貼簿格式
- 擁有者顯示剪貼簿格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe22a16886c62824775b5f2d8174e2a8e244b9e
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549583"
---
# <a name="about-the-clipboard"></a><span data-ttu-id="5aa50-114">關於剪貼簿</span><span class="sxs-lookup"><span data-stu-id="5aa50-114">About the Clipboard</span></span>

<span data-ttu-id="5aa50-115">*剪貼* 簿是一組可讓應用程式傳輸資料的函式和訊息。</span><span class="sxs-lookup"><span data-stu-id="5aa50-115">The *clipboard* is a set of functions and messages that enable applications to transfer data.</span></span> <span data-ttu-id="5aa50-116">由於所有應用程式都有存取剪貼簿的許可權，因此可以輕鬆地在應用程式之間或應用程式內傳輸資料。</span><span class="sxs-lookup"><span data-stu-id="5aa50-116">Because all applications have access to the clipboard, data can be easily transferred between applications or within an application.</span></span>

<span data-ttu-id="5aa50-117">剪貼簿是由使用者驅動的。</span><span class="sxs-lookup"><span data-stu-id="5aa50-117">The clipboard is user-driven.</span></span> <span data-ttu-id="5aa50-118">視窗應該只是為了回應使用者的命令而傳送到剪貼簿的資料。</span><span class="sxs-lookup"><span data-stu-id="5aa50-118">A window should transfer data to or from the clipboard only in response to a command from the user.</span></span> <span data-ttu-id="5aa50-119">視窗不能使用剪貼簿來傳送資料，而不需要使用者的知識。</span><span class="sxs-lookup"><span data-stu-id="5aa50-119">A window must not use the clipboard to transfer data without the user's knowledge.</span></span>

<span data-ttu-id="5aa50-120">剪貼簿上的記憶體物件可以採用任何資料格式，稱為「剪貼簿」格式。</span><span class="sxs-lookup"><span data-stu-id="5aa50-120">A memory object on the clipboard can be in any data format, called a clipboard format.</span></span> <span data-ttu-id="5aa50-121">每種格式都是以不帶正負號的整數值來識別。</span><span class="sxs-lookup"><span data-stu-id="5aa50-121">Each format is identified by an unsigned integer value.</span></span> <span data-ttu-id="5aa50-122">針對標準 (預先定義的) 剪貼簿格式，此值是在 Winuser 中定義的常數;針對已註冊的剪貼簿格式，它是 [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) 函式的傳回值。</span><span class="sxs-lookup"><span data-stu-id="5aa50-122">For standard (predefined) clipboard formats, this value is a constant defined in Winuser.h; for registered clipboard formats, it is the return value of the [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) function.</span></span>

<span data-ttu-id="5aa50-123">除了註冊剪貼簿格式之外，個別的視窗也會執行大部分的剪貼簿作業。</span><span class="sxs-lookup"><span data-stu-id="5aa50-123">Except for registering clipboard formats, individual windows perform most clipboard operations.</span></span> <span data-ttu-id="5aa50-124">一般而言，視窗程式會將資訊傳送到剪貼簿，以回應 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息。</span><span class="sxs-lookup"><span data-stu-id="5aa50-124">Typically, a window procedure transfers information to or from the clipboard in response to the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>

<span data-ttu-id="5aa50-125">本節將討論下列各項：</span><span class="sxs-lookup"><span data-stu-id="5aa50-125">This section discusses the following:</span></span>

-   [<span data-ttu-id="5aa50-126">剪貼簿命令</span><span class="sxs-lookup"><span data-stu-id="5aa50-126">Clipboard Commands</span></span>](#clipboard-commands)
-   [<span data-ttu-id="5aa50-127">剪貼簿序號</span><span class="sxs-lookup"><span data-stu-id="5aa50-127">Clipboard Sequence Number</span></span>](#clipboard-sequence-number)
-   [<span data-ttu-id="5aa50-128">剪貼簿檢視器</span><span class="sxs-lookup"><span data-stu-id="5aa50-128">Clipboard Viewers</span></span>](#clipboard-viewers)
    -   [<span data-ttu-id="5aa50-129">剪貼簿檢視器視窗</span><span class="sxs-lookup"><span data-stu-id="5aa50-129">Clipboard Viewer Windows</span></span>](#clipboard-viewer-windows)
    -   [<span data-ttu-id="5aa50-130">顯示格式</span><span class="sxs-lookup"><span data-stu-id="5aa50-130">Display Formats</span></span>](#display-formats)
    -   [<span data-ttu-id="5aa50-131">擁有者顯示格式</span><span class="sxs-lookup"><span data-stu-id="5aa50-131">Owner Display Format</span></span>](#owner-display-format)
-   [<span data-ttu-id="5aa50-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="5aa50-132">Related topics</span></span>](#related-topics)

## <a name="clipboard-commands"></a><span data-ttu-id="5aa50-133">剪貼簿命令</span><span class="sxs-lookup"><span data-stu-id="5aa50-133">Clipboard Commands</span></span>

<span data-ttu-id="5aa50-134">使用者通常會從應用程式的 [ **編輯** ] 功能表中選擇命令，以執行剪貼簿作業。</span><span class="sxs-lookup"><span data-stu-id="5aa50-134">A user typically carries out clipboard operations by choosing commands from an application's **Edit** menu.</span></span> <span data-ttu-id="5aa50-135">以下是標準剪貼簿命令的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="5aa50-135">Following is a brief description of the standard clipboard commands.</span></span>



|  <span data-ttu-id="5aa50-136">命令</span><span class="sxs-lookup"><span data-stu-id="5aa50-136">Command</span></span>        |  <span data-ttu-id="5aa50-137">描述</span><span class="sxs-lookup"><span data-stu-id="5aa50-137">Description</span></span>                                                                                                                                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aa50-138">**剪下**</span><span class="sxs-lookup"><span data-stu-id="5aa50-138">**Cut**</span></span>    | <span data-ttu-id="5aa50-139">將目前選取範圍的複本放在剪貼簿，並從檔中刪除選取專案。</span><span class="sxs-lookup"><span data-stu-id="5aa50-139">Places a copy of the current selection on the clipboard and deletes the selection from the document.</span></span> <span data-ttu-id="5aa50-140">剪貼簿的先前內容已損毀。</span><span class="sxs-lookup"><span data-stu-id="5aa50-140">The previous content of the clipboard is destroyed.</span></span>                                                          |
| <span data-ttu-id="5aa50-141">**複製**</span><span class="sxs-lookup"><span data-stu-id="5aa50-141">**Copy**</span></span>   | <span data-ttu-id="5aa50-142">將目前選取範圍的複本放在剪貼簿上。</span><span class="sxs-lookup"><span data-stu-id="5aa50-142">Places a copy of the current selection on the clipboard.</span></span> <span data-ttu-id="5aa50-143">檔會維持不變。</span><span class="sxs-lookup"><span data-stu-id="5aa50-143">The document remains unchanged.</span></span> <span data-ttu-id="5aa50-144">剪貼簿的先前內容已損毀。</span><span class="sxs-lookup"><span data-stu-id="5aa50-144">The previous content of the clipboard is destroyed.</span></span>                                                                      |
| <span data-ttu-id="5aa50-145">**貼上**</span><span class="sxs-lookup"><span data-stu-id="5aa50-145">**Paste**</span></span>  | <span data-ttu-id="5aa50-146">以剪貼簿的內容取代目前的選取範圍。</span><span class="sxs-lookup"><span data-stu-id="5aa50-146">Replaces the current selection with the content of the clipboard.</span></span> <span data-ttu-id="5aa50-147">剪貼簿的內容不會變更。</span><span class="sxs-lookup"><span data-stu-id="5aa50-147">The content of the clipboard is not changed.</span></span>                                                                                                    |
| <span data-ttu-id="5aa50-148">**刪除**</span><span class="sxs-lookup"><span data-stu-id="5aa50-148">**Delete**</span></span> | <span data-ttu-id="5aa50-149">從檔中刪除目前的選取範圍。</span><span class="sxs-lookup"><span data-stu-id="5aa50-149">Deletes the current selection from the document.</span></span> <span data-ttu-id="5aa50-150">剪貼簿的內容不會變更。</span><span class="sxs-lookup"><span data-stu-id="5aa50-150">The content of the clipboard is not changed.</span></span> <span data-ttu-id="5aa50-151">此命令不牽涉到剪貼簿，但它應該會在 [ **編輯** ] 功能表上顯示 [剪貼簿] 命令。</span><span class="sxs-lookup"><span data-stu-id="5aa50-151">This command does not involve the clipboard, but it should appear with the clipboard commands on the **Edit** menu.</span></span> |



 

## <a name="clipboard-sequence-number"></a><span data-ttu-id="5aa50-152">剪貼簿序號</span><span class="sxs-lookup"><span data-stu-id="5aa50-152">Clipboard Sequence Number</span></span>

<span data-ttu-id="5aa50-153">每個視窗工作站的剪貼簿都有相關聯的剪貼簿序號。</span><span class="sxs-lookup"><span data-stu-id="5aa50-153">The clipboard for each window station has an associated clipboard sequence number.</span></span> <span data-ttu-id="5aa50-154">每當剪貼簿的內容變更時，這個數位就會遞增。</span><span class="sxs-lookup"><span data-stu-id="5aa50-154">This number is incremented whenever the contents of the clipboard change.</span></span> <span data-ttu-id="5aa50-155">若要取得剪貼簿序號，請呼叫 [**GetClipboardSequenceNumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) 函數。</span><span class="sxs-lookup"><span data-stu-id="5aa50-155">To obtain the clipboard sequence number, call the [**GetClipboardSequenceNumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) function.</span></span>

## <a name="clipboard-viewers"></a><span data-ttu-id="5aa50-156">剪貼簿檢視器</span><span class="sxs-lookup"><span data-stu-id="5aa50-156">Clipboard Viewers</span></span>

<span data-ttu-id="5aa50-157">剪貼簿檢視器是一種視窗，可顯示剪貼簿的目前內容。</span><span class="sxs-lookup"><span data-stu-id="5aa50-157">A clipboard viewer is a window that displays the current content of the clipboard.</span></span> <span data-ttu-id="5aa50-158">[剪貼簿檢視器] 視窗是使用者的便利性，並且不會影響剪貼簿的資料交易功能。</span><span class="sxs-lookup"><span data-stu-id="5aa50-158">The clipboard viewer window is a convenience for the user and does not affect the data-transaction functions of the clipboard.</span></span>

<span data-ttu-id="5aa50-159">剪貼簿檢視器視窗通常可以顯示至少三種最常見的格式： **cf \_ TEXT**、 **cf \_ BITMAP** 和 **cf \_ METAFILEPICT**。</span><span class="sxs-lookup"><span data-stu-id="5aa50-159">Typically, a clipboard viewer window can display at least the three most common formats: **CF\_TEXT**, **CF\_BITMAP**, and **CF\_METAFILEPICT**.</span></span> <span data-ttu-id="5aa50-160">如果視窗沒有提供這三種格式的資料，則應提供顯示格式的資料，或使用擁有者顯示格式。</span><span class="sxs-lookup"><span data-stu-id="5aa50-160">If a window does not make data available in any of these three formats, it should provide data in a display format or use the owner-display format.</span></span>

<span data-ttu-id="5aa50-161">*剪貼簿檢視器* 會將兩個或多個實體連結在一起，使其相依于另一個實體。</span><span class="sxs-lookup"><span data-stu-id="5aa50-161">A *clipboard viewer chain* is the linking together of two or more entities so that they are dependent upon one another for operation.</span></span> <span data-ttu-id="5aa50-162">這個相互相關性 (鏈) 允許所有執行中的剪貼簿檢視器應用程式接收傳送到目前剪貼簿的訊息。</span><span class="sxs-lookup"><span data-stu-id="5aa50-162">This interdependency (chain) allows all running clipboard viewer applications to receive the messages sent to the current clipboard.</span></span>

<span data-ttu-id="5aa50-163">本節將討論下列主題。</span><span class="sxs-lookup"><span data-stu-id="5aa50-163">The following topics are discussed in this section.</span></span>

-   [<span data-ttu-id="5aa50-164">剪貼簿檢視器視窗</span><span class="sxs-lookup"><span data-stu-id="5aa50-164">Clipboard Viewer Windows</span></span>](#clipboard-viewer-windows)
-   [<span data-ttu-id="5aa50-165">顯示格式</span><span class="sxs-lookup"><span data-stu-id="5aa50-165">Display Formats</span></span>](#display-formats)
-   [<span data-ttu-id="5aa50-166">擁有者顯示格式</span><span class="sxs-lookup"><span data-stu-id="5aa50-166">Owner Display Format</span></span>](#owner-display-format)

### <a name="clipboard-viewer-windows"></a><span data-ttu-id="5aa50-167">剪貼簿檢視器視窗</span><span class="sxs-lookup"><span data-stu-id="5aa50-167">Clipboard Viewer Windows</span></span>

<span data-ttu-id="5aa50-168">視窗會藉由呼叫 [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) 函式，將本身新增至剪貼簿檢視器鏈。</span><span class="sxs-lookup"><span data-stu-id="5aa50-168">A window adds itself to the clipboard viewer chain by calling the [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) function.</span></span> <span data-ttu-id="5aa50-169">傳回值是鏈中下一個視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5aa50-169">The return value is the handle to the next window in the chain.</span></span> <span data-ttu-id="5aa50-170">若要取得鏈中第一個視窗的控制碼，請呼叫 [**GetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-getclipboardviewer) 函數。</span><span class="sxs-lookup"><span data-stu-id="5aa50-170">To retrieve the handle to the first window in the chain, call the [**GetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-getclipboardviewer) function.</span></span>

<span data-ttu-id="5aa50-171">每個剪貼簿檢視器視窗都必須追蹤剪貼簿檢視器鏈中的下一個視窗。</span><span class="sxs-lookup"><span data-stu-id="5aa50-171">Each clipboard viewer window must keep track of the next window in the clipboard viewer chain.</span></span> <span data-ttu-id="5aa50-172">當剪貼簿的內容變更時，系統會將 [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) 訊息傳送至鏈中的第一個視窗。</span><span class="sxs-lookup"><span data-stu-id="5aa50-172">When the content of the clipboard changes, the system sends a [**WM\_DRAWCLIPBOARD**](wm-drawclipboard.md) message to the first window in the chain.</span></span> <span data-ttu-id="5aa50-173">更新其顯示之後，每個剪貼簿檢視器視窗都必須將此訊息傳遞至鏈中的下一個視窗。</span><span class="sxs-lookup"><span data-stu-id="5aa50-173">After updating its display, each clipboard viewer window must pass this message on to the next window in the chain.</span></span>

<span data-ttu-id="5aa50-174">在關閉之前，剪貼簿檢視器視窗必須藉由呼叫 [**ChangeClipboardChain**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) 函數，從剪貼簿檢視器鏈中移除本身。</span><span class="sxs-lookup"><span data-stu-id="5aa50-174">Before closing, a clipboard viewer window must remove itself from the clipboard viewer chain by calling the [**ChangeClipboardChain**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) function.</span></span> <span data-ttu-id="5aa50-175">然後系統會將 [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) 訊息傳送至鏈中的第一個視窗。</span><span class="sxs-lookup"><span data-stu-id="5aa50-175">The system then sends a [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) message to the first window in the chain.</span></span>

<span data-ttu-id="5aa50-176">如需處理 [**wm \_ DRAWCLIPBOARD**](wm-drawclipboard.md) 和 [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) 訊息的詳細資訊，請參閱 [建立剪貼簿檢視器視窗](using-the-clipboard.md)。</span><span class="sxs-lookup"><span data-stu-id="5aa50-176">For more information about processing the [**WM\_DRAWCLIPBOARD**](wm-drawclipboard.md) and [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) messages, see [Creating a Clipboard Viewer Window](using-the-clipboard.md).</span></span>

### <a name="display-formats"></a><span data-ttu-id="5aa50-177">顯示格式</span><span class="sxs-lookup"><span data-stu-id="5aa50-177">Display Formats</span></span>

<span data-ttu-id="5aa50-178">顯示格式是用來在 [剪貼簿檢視器] 視窗中顯示資訊的剪貼簿格式。</span><span class="sxs-lookup"><span data-stu-id="5aa50-178">A display format is a clipboard format used to display information in a clipboard viewer window.</span></span> <span data-ttu-id="5aa50-179">使用私用或已註冊剪貼簿格式的剪貼簿擁有者，以及沒有最常見的標準格式，都必須提供顯示格式的資料，以便在 [剪貼簿檢視器] 視窗中進行觀看。</span><span class="sxs-lookup"><span data-stu-id="5aa50-179">A clipboard owner that uses a private or registered clipboard format, and none of the most common standard formats, must provide data in a display format for viewing in a clipboard viewer window.</span></span> <span data-ttu-id="5aa50-180">顯示格式僅供觀賞之用，不得貼入檔中。</span><span class="sxs-lookup"><span data-stu-id="5aa50-180">The display formats are intended for viewing only and must not be pasted into a document.</span></span>

<span data-ttu-id="5aa50-181">四種顯示格式為： **cf \_ DSPBITMAP**、 **cf \_ DSPMETAFILEPICT**、 **cf \_ DSPTEXT** 和 **CF \_ DSPENHMETAFILE**。</span><span class="sxs-lookup"><span data-stu-id="5aa50-181">The four display formats are: **CF\_DSPBITMAP**, **CF\_DSPMETAFILEPICT**, **CF\_DSPTEXT**, and **CF\_DSPENHMETAFILE**.</span></span> <span data-ttu-id="5aa50-182">這些顯示格式的轉譯方式與標準格式相同，也就是： **cf \_ BITMAP**、 **cf \_ TEXT**、 **cf \_ METAFILEPICT** 和 **cf \_ ENHMETAFILE**。</span><span class="sxs-lookup"><span data-stu-id="5aa50-182">These display formats are rendered in the same way as the standard formats, which are: **CF\_BITMAP**, **CF\_TEXT**, **CF\_METAFILEPICT**, and **CF\_ENHMETAFILE**.</span></span>

### <a name="owner-display-format"></a><span data-ttu-id="5aa50-183">擁有者顯示格式</span><span class="sxs-lookup"><span data-stu-id="5aa50-183">Owner Display Format</span></span>

<span data-ttu-id="5aa50-184">針對不使用任何一般標準剪貼簿格式的剪貼簿擁有者，提供顯示格式的替代方式是使用擁有者顯示 (**CF \_ OWNERDISPLAY**) 剪貼簿格式。</span><span class="sxs-lookup"><span data-stu-id="5aa50-184">For a clipboard owner that does not use any of the common standard clipboard formats, an alternative to providing a display format is to use the owner-display (**CF\_OWNERDISPLAY**) clipboard format.</span></span>

<span data-ttu-id="5aa50-185">剪貼簿擁有者可以使用擁有者顯示格式，藉由直接控制剪貼簿檢視器視窗，來避免以其他格式轉譯資料的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="5aa50-185">By using the owner-display format, a clipboard owner can avoid the overhead of rendering data in an additional format by taking direct control over painting the clipboard viewer window.</span></span> <span data-ttu-id="5aa50-186">只要重新繪製視窗的一部分，或是滾動或調整視窗的大小，[剪貼簿檢視器] 視窗就會將訊息傳送給剪貼簿擁有者。</span><span class="sxs-lookup"><span data-stu-id="5aa50-186">The clipboard viewer window sends messages to the clipboard owner whenever a portion of the window must be repainted or when the window is scrolled or resized.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5aa50-187">相關主題</span><span class="sxs-lookup"><span data-stu-id="5aa50-187">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5aa50-188">標準剪貼簿格式</span><span class="sxs-lookup"><span data-stu-id="5aa50-188">Standard Clipboard Formats</span></span>](standard-clipboard-formats.md)
</dt> </dl>

 

 