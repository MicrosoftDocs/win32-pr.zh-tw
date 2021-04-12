---
title: 使用動態資料交換
description: 本主題提供有關動態資料交換的程式碼範例。
ms.assetid: 6d94403b-64b4-4763-868a-3b94431dab79
keywords:
- 動態資料交換 (DDE) 、交談
- DDE (動態資料交換) 、交談
- '資料交換、動態資料交換 (DDE) '
- 動態資料交換 (DDE) ，範例
- DDE (動態資料交換) ，範例
- 動態資料交換 (的 DDE) ，伺服器應用程式中的命令
- 伺服器應用程式中的 DDE (動態資料交換) 命令
- 動態資料交換 (DDE) 、資料連結
- DDE (動態資料交換) 、資料連結
- 動態資料交換 (DDE) 、items
- DDE (動態資料交換) 、items
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fe20c4dedc38303fe9bcb9c4b0fae42d03ee536
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315463"
---
# <a name="using-dynamic-data-exchange"></a><span data-ttu-id="0b404-114">使用動態資料交換</span><span class="sxs-lookup"><span data-stu-id="0b404-114">Using Dynamic Data Exchange</span></span>

<span data-ttu-id="0b404-115">本節包含下列工作的程式碼範例：</span><span class="sxs-lookup"><span data-stu-id="0b404-115">This section has code samples on the following tasks:</span></span>

-   [<span data-ttu-id="0b404-116">起始對話</span><span class="sxs-lookup"><span data-stu-id="0b404-116">Initiating a Conversation</span></span>](#initiating-a-conversation)
-   [<span data-ttu-id="0b404-117">傳送單一專案</span><span class="sxs-lookup"><span data-stu-id="0b404-117">Transferring a Single Item</span></span>](#transferring-a-single-item)
    -   [<span data-ttu-id="0b404-118">從伺服器中取出專案</span><span class="sxs-lookup"><span data-stu-id="0b404-118">Retrieving an Item from the Server</span></span>](#retrieving-an-item-from-the-server)
    -   [<span data-ttu-id="0b404-119">將專案提交至伺服器</span><span class="sxs-lookup"><span data-stu-id="0b404-119">Submitting an Item to the Server</span></span>](#submitting-an-item-to-the-server)
-   [<span data-ttu-id="0b404-120">建立永久資料連結</span><span class="sxs-lookup"><span data-stu-id="0b404-120">Establishing a Permanent Data Link</span></span>](#establishing-a-permanent-data-link)
    -   [<span data-ttu-id="0b404-121">起始資料連結</span><span class="sxs-lookup"><span data-stu-id="0b404-121">Initiating a Data Link</span></span>](#initiating-a-data-link)
    -   [<span data-ttu-id="0b404-122">使用貼上連結命令起始資料連結</span><span class="sxs-lookup"><span data-stu-id="0b404-122">Initiating a Data Link with the Paste Link Command</span></span>](#initiating-a-data-link-with-the-paste-link-command)
    -   [<span data-ttu-id="0b404-123">通知用戶端資料已變更</span><span class="sxs-lookup"><span data-stu-id="0b404-123">Notifying the Client that Data Has Changed</span></span>](#notifying-the-client-that-data-has-changed)
    -   [<span data-ttu-id="0b404-124">終止資料連結</span><span class="sxs-lookup"><span data-stu-id="0b404-124">Terminating a Data Link</span></span>](#terminating-a-data-link)
-   [<span data-ttu-id="0b404-125">在伺服器應用程式中執行命令</span><span class="sxs-lookup"><span data-stu-id="0b404-125">Carrying Out Commands in a Server Application</span></span>](#carrying-out-commands-in-a-server-application)
-   [<span data-ttu-id="0b404-126">終止交談</span><span class="sxs-lookup"><span data-stu-id="0b404-126">Terminating a Conversation</span></span>](#terminating-a-conversation)

## <a name="initiating-a-conversation"></a><span data-ttu-id="0b404-127">起始對話</span><span class="sxs-lookup"><span data-stu-id="0b404-127">Initiating a Conversation</span></span>

<span data-ttu-id="0b404-128">若要起始動態資料交換 (DDE) 交談，用戶端會傳送 [**WM \_ DDE \_ 初始**](wm-dde-initiate.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="0b404-128">To initiate a Dynamic Data Exchange (DDE) conversation, the client sends a [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message.</span></span> <span data-ttu-id="0b404-129">通常，用戶端會呼叫 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)來廣播此訊息，並以-1 做為第一個參數。</span><span class="sxs-lookup"><span data-stu-id="0b404-129">Usually, the client broadcasts this message by calling [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), with –1 as the first parameter.</span></span> <span data-ttu-id="0b404-130">如果應用程式已經有伺服器應用程式的視窗控制碼，它可以將訊息直接傳送到該視窗。</span><span class="sxs-lookup"><span data-stu-id="0b404-130">If the application already has the window handle to the server application, it can send the message directly to that window.</span></span> <span data-ttu-id="0b404-131">用戶端會藉由呼叫 [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)來準備應用程式名稱和主題名稱的原子。</span><span class="sxs-lookup"><span data-stu-id="0b404-131">The client prepares atoms for the application name and topic name by calling [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma).</span></span> <span data-ttu-id="0b404-132">用戶端可以針對應用程式和主題提供 **Null** (萬用字元) 原子，要求與任何潛在的伺服器應用程式進行交談。</span><span class="sxs-lookup"><span data-stu-id="0b404-132">The client can request conversations with any potential server application and for any potential topic by supplying **NULL** (wildcard) atoms for the application and topic.</span></span>

<span data-ttu-id="0b404-133">下列範例說明用戶端如何起始交談，同時指定了應用程式和主題。</span><span class="sxs-lookup"><span data-stu-id="0b404-133">The following example illustrates how the client initiates a conversation, where both the application and topic are specified.</span></span>


```
    static BOOL fInInitiate = FALSE; 
    char *szApplication; 
    char *szTopic; 
    atomApplication = *szApplication == 0 ? 
    NULL     : GlobalAddAtom((LPSTR) szApplication); 
    atomTopic = *szTopic == 0 ? 
    NULL     : GlobalAddAtom((LPSTR) szTopic); 
 
    fInInitiate = TRUE; 
    SendMessage((HWND) HWND_BROADCAST, // broadcasts message 
        WM_DDE_INITIATE,               // initiates conversation 
        (WPARAM) hwndClientDDE,        // handle to client DDE window 
        MAKELONG(atomApplication,      // application-name atom 
            atomTopic));               // topic-name atom 
    fInInitiate = FALSE; 
    if (atomApplication != NULL) 
        GlobalDeleteAtom(atomApplication); 
    if (atomTopic != NULL) 
        GlobalDeleteAtom(atomTopic);
```



> [!Note]  
> <span data-ttu-id="0b404-134">如果您的應用程式使用 **Null** 原子，則不需要使用 [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) 和 [**GlobalDeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) 函數。</span><span class="sxs-lookup"><span data-stu-id="0b404-134">If your application uses **NULL** atoms, you need not use the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) and [**GlobalDeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) functions.</span></span> <span data-ttu-id="0b404-135">在此範例中，用戶端應用程式會建立兩個全域原子，分別包含伺服器的名稱和主題的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b404-135">In this example, the client application creates two global atoms containing the name of the server and the name of the topic, respectively.</span></span>

 

<span data-ttu-id="0b404-136">用戶端應用程式會在訊息的 *lParam* 參數中，使用這兩個原子來傳送 [**WM \_ DDE \_ 起始**](wm-dde-initiate.md)訊息。</span><span class="sxs-lookup"><span data-stu-id="0b404-136">The client application sends a [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message with these two atoms in the *lParam* parameter of the message.</span></span> <span data-ttu-id="0b404-137">在 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 函式的呼叫中，特殊的視窗控制碼（1）會指示系統將此訊息傳送給所有其他作用中的應用程式。</span><span class="sxs-lookup"><span data-stu-id="0b404-137">In the call to the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function, the special window handle –1 directs the system to send this message to all other active applications.</span></span> <span data-ttu-id="0b404-138">**SendMessage** 不會傳回用戶端應用程式，直到接收訊息的所有應用程式都將控制權傳回給系統為止。</span><span class="sxs-lookup"><span data-stu-id="0b404-138">**SendMessage** does not return to the client application until all applications that receive the message have, in turn, returned control to the system.</span></span> <span data-ttu-id="0b404-139">這表示伺服器應用程式在回復中傳送的所有 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息，在 **SendMessage** 呼叫傳回時，保證已由用戶端處理。</span><span class="sxs-lookup"><span data-stu-id="0b404-139">This means that all [**WM\_DDE\_ACK**](wm-dde-ack.md) messages sent in reply by the server applications are guaranteed to have been processed by the client by the time the **SendMessage** call has returned.</span></span>

<span data-ttu-id="0b404-140">在 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 傳回之後，用戶端應用程式會刪除全域原子。</span><span class="sxs-lookup"><span data-stu-id="0b404-140">After [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns, the client application deletes the global atoms.</span></span>

<span data-ttu-id="0b404-141">伺服器應用程式會根據下圖所示的邏輯來回應。</span><span class="sxs-lookup"><span data-stu-id="0b404-141">Server applications respond according to the logic illustrated in the following diagram.</span></span>

![伺服器應用程式回應邏輯](images/csdde-01.png)

<span data-ttu-id="0b404-143">若要認可一或多個主題，伺服器必須為每個對話建立原子 (如果有多個主題) ，並針對每個交談傳送 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息，則伺服器必須有重複的應用程式名稱原子，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="0b404-143">To acknowledge one or more topics, the server must create atoms for each conversation (requiring duplicate application-name atoms if there are multiple topics) and send a [**WM\_DDE\_ACK**](wm-dde-ack.md) message for each conversation, as illustrated in the following example.</span></span>


```
if ((atomApplication = GlobalAddAtom("Server")) != 0) 
{ 
    if ((atomTopic = GlobalAddAtom(szTopic)) != 0) 
    { 
        SendMessage(hwndClientDDE, 
            WM_DDE_ACK, 
            (WPARAM) hwndServerDDE, 
            MAKELONG(atomApplication, atomTopic)); 
        GlobalDeleteAtom(atomApplication); 
    } 
 
    GlobalDeleteAtom(atomTopic); 
} 
 
if ((atomApplication == 0) || (atomTopic == 0)) 
{ 
    // Handle errors. 
}
```



<span data-ttu-id="0b404-144">當伺服器以 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息回應時，用戶端應用程式應該將控制碼儲存至伺服器視窗。</span><span class="sxs-lookup"><span data-stu-id="0b404-144">When a server responds with a [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the client application should save a handle to the server window.</span></span> <span data-ttu-id="0b404-145">用戶端接收控制碼做為 **WM \_ DDE \_** 通知訊息的 *wParam* 參數，然後將所有後續的 DDE 訊息傳送到此控制碼識別的伺服器視窗。</span><span class="sxs-lookup"><span data-stu-id="0b404-145">The client receiving the handle as the *wParam* parameter of the **WM\_DDE\_ACK** message then sends all subsequent DDE messages to the server window this handle identifies.</span></span>

<span data-ttu-id="0b404-146">如果您的用戶端應用程式使用 **Null** atom 做為應用程式名稱或主題名稱，則預期應用程式會接收來自多個伺服器應用程式的通知。</span><span class="sxs-lookup"><span data-stu-id="0b404-146">If your client application uses a **NULL** atom for the application name or topic name, expect the application to receive acknowledgments from more than one server application.</span></span> <span data-ttu-id="0b404-147">多個通知也可以來自多個 DDE 伺服器實例，即使您的用戶端應用程式不是 **Null** ，也可以使用原子。</span><span class="sxs-lookup"><span data-stu-id="0b404-147">Multiple acknowledgements can also come from multiple instances of a DDE server, even if your client application does not **NULL** use atoms.</span></span> <span data-ttu-id="0b404-148">伺服器應該一律針對每個交談使用唯一的視窗。</span><span class="sxs-lookup"><span data-stu-id="0b404-148">A server should always use a unique window for each conversation.</span></span> <span data-ttu-id="0b404-149">用戶端應用程式中的視窗程式可以使用伺服器視窗的控制碼 (作為 [**WM \_ DDE \_ 起始**](wm-dde-initiate.md)) 的 *lParam* 參數，以追蹤多個交談。</span><span class="sxs-lookup"><span data-stu-id="0b404-149">The window procedure in the client application can use a handle to the server window (provided as the *lParam* parameter of [**WM\_DDE\_INITIATE**](wm-dde-initiate.md)) to track multiple conversations.</span></span> <span data-ttu-id="0b404-150">這可讓單一用戶端視窗處理數個交談，而不需要為每個對話終止和重新連接新的用戶端視窗。</span><span class="sxs-lookup"><span data-stu-id="0b404-150">This allows a single client window to process several conversations without needing to terminate and reconnect with a new client window for each conversation.</span></span>

## <a name="transferring-a-single-item"></a><span data-ttu-id="0b404-151">傳送單一專案</span><span class="sxs-lookup"><span data-stu-id="0b404-151">Transferring a Single Item</span></span>

<span data-ttu-id="0b404-152">一旦建立了 DDE 交談之後，用戶端就可以藉由發出 [**wm \_ dde \_ 要求**](wm-dde-request.md) 訊息來從伺服器取出資料項目的值，或是藉由發出 [**wm \_ dde \_**](wm-dde-poke.md)的郵件將資料項目目值提交至伺服器。</span><span class="sxs-lookup"><span data-stu-id="0b404-152">Once a DDE conversation has been established, the client can either retrieve the value of a data item from the server by issuing the [**WM\_DDE\_REQUEST**](wm-dde-request.md) message, or submit a data-item value to the server by issuing [**WM\_DDE\_POKE**](wm-dde-poke.md).</span></span>

-   [<span data-ttu-id="0b404-153">從伺服器中取出專案</span><span class="sxs-lookup"><span data-stu-id="0b404-153">Retrieving an Item from the Server</span></span>](#retrieving-an-item-from-the-server)
-   [<span data-ttu-id="0b404-154">將專案提交至伺服器</span><span class="sxs-lookup"><span data-stu-id="0b404-154">Submitting an Item to the Server</span></span>](#submitting-an-item-to-the-server)

### <a name="retrieving-an-item-from-the-server"></a><span data-ttu-id="0b404-155">從伺服器中取出專案</span><span class="sxs-lookup"><span data-stu-id="0b404-155">Retrieving an Item from the Server</span></span>

<span data-ttu-id="0b404-156">若要從伺服器取出專案，用戶端會傳送一個 [**WM \_ DDE \_ 要求**](wm-dde-request.md) 訊息給伺服器，以指定要抓取的專案和格式，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="0b404-156">To retrieve an item from the server, the client sends the server a [**WM\_DDE\_REQUEST**](wm-dde-request.md) message specifying the item and format to retrieve, as shown in the following example.</span></span>


```
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndServerDDE, 
            WM_DDE_REQUEST, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_REQUEST, CF_TEXT, atomItem))) 
    {
        GlobalDeleteAtom(atomItem); 
    }
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
}
```



<span data-ttu-id="0b404-157">在此範例中，用戶端會將「剪貼簿 **」格式指定為 \_ 要求** 之資料項目的慣用格式。</span><span class="sxs-lookup"><span data-stu-id="0b404-157">In this example, the client specifies the clipboard format **CF\_TEXT** as the preferred format for the requested data item.</span></span>

<span data-ttu-id="0b404-158">[**WM \_ DDE \_ 要求**](wm-dde-request.md)訊息的接收者 (server) 通常必須刪除專案 Atom，但是如果 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)呼叫失敗，用戶端就必須刪除 atom。</span><span class="sxs-lookup"><span data-stu-id="0b404-158">The receiver (server) of the [**WM\_DDE\_REQUEST**](wm-dde-request.md) message typically must delete the item atom, but if the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) call fails, the client must delete the atom.</span></span>

<span data-ttu-id="0b404-159">如果伺服器具有要求之專案的存取權，而且可以使用要求的格式來轉譯，則伺服器會將專案值複製為共用記憶體物件，並傳送 [**WM \_ DDE \_ 資料**](wm-dde-data.md) 訊息給用戶端，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="0b404-159">If the server has access to the requested item and can render it in the requested format, the server copies the item value as a shared memory object and sends the client a [**WM\_DDE\_DATA**](wm-dde-data.md) message, as illustrated in the following example.</span></span>


```
// Allocate the size of the DDE data header, plus the data: a 
// string,<CR><LF><NULL>. The byte for the string's terminating 
// null character is counted by DDEDATA.Value[1].

size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hData = GlobalAlloc(GMEM_MOVEABLE,
  (LONG) sizeof(DDEDATA) + *pcch + 2)))  
{
    return; 
}
 
if (!(lpData = (DDEDATA FAR*) GlobalLock(hData)))  
{
    GlobalFree(hData); 
    return; 
} 
 
lpData->cfFormat = CF_TEXT;
hResult = StringCchCopy((LPSTR) lpData->Value, *pcch +1, (LPCSTR) szItemValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
 
// Each line of CF_TEXT data is terminated by CR/LF. 
hResult = StringCchCat((LPSTR) lpData->Value, *pcch + 3, (LPCSTR) "\r\n");
if (FAILED(hResult)
{
// TODO: Write error handler.
 return;
} 
GlobalUnlock(hData); 
if ((atomItem = GlobalAddAtom((LPSTR) szItemName)) != 0) 
{ 
    lParam = PackDDElParam(WM_DDE_ACK, (UINT) hData, atomItem); 
    if (!PostMessage(hwndClientDDE, 
            WM_DDE_DATA, 
            (WPARAM) hwndServerDDE, 
            lParam)) 
    { 
        GlobalFree(hData); 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_ACK, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors.  
}
```



<span data-ttu-id="0b404-160">在此範例中，伺服器應用程式會配置包含資料項目的記憶體物件。</span><span class="sxs-lookup"><span data-stu-id="0b404-160">In this example, the server application allocates a memory object to contain the data item.</span></span> <span data-ttu-id="0b404-161">資料物件會初始化為 [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) 結構。</span><span class="sxs-lookup"><span data-stu-id="0b404-161">The data object is initialized as a [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure.</span></span>

<span data-ttu-id="0b404-162">然後，伺服器應用程式會將結構的 **cfFormat** 成員設定為 CF \_ text，以通知用戶端應用程式資料是文字格式。</span><span class="sxs-lookup"><span data-stu-id="0b404-162">The server application then sets the **cfFormat** member of the structure to CF\_TEXT to inform the client application that the data is in text format.</span></span> <span data-ttu-id="0b404-163">用戶端會將所要求資料的值複製到 [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata)結構的 **值** 成員，以進行回應。</span><span class="sxs-lookup"><span data-stu-id="0b404-163">The client responds by copying the value of the requested data into the **Value** member of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure.</span></span> <span data-ttu-id="0b404-164">在伺服器填妥資料物件之後，伺服器會將資料解除鎖定，並建立包含資料項目名稱的全域 atom。</span><span class="sxs-lookup"><span data-stu-id="0b404-164">After the server has filled the data object, the server unlocks the data and creates a global atom containing the name of the data item.</span></span>

<span data-ttu-id="0b404-165">最後，伺服器會呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)來發出 [**WM \_ DDE 的 \_ 資料**](wm-dde-data.md)訊息。</span><span class="sxs-lookup"><span data-stu-id="0b404-165">Finally, the server issues the [**WM\_DDE\_DATA**](wm-dde-data.md) message by calling [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea).</span></span> <span data-ttu-id="0b404-166">資料物件的控制碼和包含專案名稱的 atom 會由 [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)函數封裝至訊息的 *lParam* 參數。</span><span class="sxs-lookup"><span data-stu-id="0b404-166">The handle to the data object and the atom containing the item name are packed into the *lParam* parameter of the message by the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function.</span></span>

<span data-ttu-id="0b404-167">如果 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 失敗，伺服器必須使用 [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) 函式來釋放壓縮的 *lParam* 參數。</span><span class="sxs-lookup"><span data-stu-id="0b404-167">If [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) fails, the server must use the [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) function to free the packed *lParam* parameter.</span></span> <span data-ttu-id="0b404-168">伺服器也必須釋放所接收之 [**WM \_ DDE \_ 要求**](wm-dde-request.md)訊息的封裝 *lParam* 參數。</span><span class="sxs-lookup"><span data-stu-id="0b404-168">The server must also free the packed *lParam* parameter for the [**WM\_DDE\_REQUEST**](wm-dde-request.md) message it received.</span></span>

<span data-ttu-id="0b404-169">如果伺服器無法滿足要求，它會將負的 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息傳送至用戶端，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="0b404-169">If the server cannot satisfy the request, it sends a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message to the client, as shown in the following example.</span></span>


```
// Negative acknowledgment. 
 
PostMessage(hwndClientDDE, 
    WM_DDE_ACK, 
    (WPARAM) hwndServerDDE, 
    PackDDElParam(WM_DDE_ACK, 0, atomItem));
```



<span data-ttu-id="0b404-170">收到 [**WM \_ DDE \_ 資料**](wm-dde-data.md) 訊息時，用戶端會適當地處理資料項目目值。</span><span class="sxs-lookup"><span data-stu-id="0b404-170">Upon receiving a [**WM\_DDE\_DATA**](wm-dde-data.md) message, the client processes the data-item value as appropriate.</span></span> <span data-ttu-id="0b404-171">然後，如果在 **WM \_ dde 的 \_ 資料** 訊息中指向的 **fAckReq** 成員是1，則用戶端必須將伺服器傳送正 [**的 \_ WM \_ dde**](wm-dde-ack.md)通知訊息，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="0b404-171">Then, if the **fAckReq** member pointed to in the **WM\_DDE\_DATA** message is 1, the client must send the server a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message, as shown in the following example.</span></span>


```
UnpackDDElParam(WM_DDE_DATA, lParam, (PUINT) &hData, 
    (PUINT) &atomItem); 
if (!(lpDDEData = (DDEDATA FAR*) GlobalLock(hData)) 
        || (lpDDEData->cfFormat != CF_TEXT)) 
{ 
    PostMessage(hwndServerDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_ACK, 0, atomItem)); // Negative ACK. 
} 
 
// Copy data from lpDDEData here. 
 
if (lpDDEData->fAckReq) 
{ 
    PostMessage(hwndServerDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_ACK, 0x8000, 
            atomItem)); // Positive ACK 
} 
 
bRelease = lpDDEData->fRelease; 
GlobalUnlock(hData); 
if (bRelease) 
    GlobalFree(hData);
```



<span data-ttu-id="0b404-172">在此範例中，用戶端會檢查資料的格式。</span><span class="sxs-lookup"><span data-stu-id="0b404-172">In this example, the client examines the format of the data.</span></span> <span data-ttu-id="0b404-173">如果格式不是 **CF \_ 文字** (或用戶端無法鎖定資料) 的記憶體，用戶端會傳送負的 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息，表示它無法處理資料。</span><span class="sxs-lookup"><span data-stu-id="0b404-173">If the format is not **CF\_TEXT** (or if the client cannot lock the memory for the data), the client sends a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message to indicate that it cannot process the data.</span></span> <span data-ttu-id="0b404-174">如果用戶端因為控制碼包含 **fAckReq** 成員而無法鎖定資料控制碼，則用戶端不應該傳送負 **的 \_ WM \_ DDE** 通知訊息。</span><span class="sxs-lookup"><span data-stu-id="0b404-174">If the client cannot lock a data handle because the handle contains the **fAckReq** member, the client should not send a negative **WM\_DDE\_ACK** message.</span></span> <span data-ttu-id="0b404-175">相反地，用戶端應該終止交談。</span><span class="sxs-lookup"><span data-stu-id="0b404-175">Instead, the client should terminate the conversation.</span></span>

<span data-ttu-id="0b404-176">如果用戶端傳送負認可以回應 [**WM \_ dde 的 \_ 資料**](wm-dde-data.md) 訊息，則伺服器會負責釋出記憶體 (但不會) *lParam* 參數，而是與負認可相關聯的 **WM \_ DDE \_ 資料** 訊息所參考的資料。</span><span class="sxs-lookup"><span data-stu-id="0b404-176">If a client sends a negative acknowledgment in response to a [**WM\_DDE\_DATA**](wm-dde-data.md) message, the server is responsible for freeing the memory (but not the *lParam* parameter) referenced by the **WM\_DDE\_DATA** message associated with the negative acknowledgment.</span></span>

<span data-ttu-id="0b404-177">如果可以處理資料，用戶端會檢查 [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata)結構的 **fAckReq** 成員，判斷伺服器是否要求告知用戶端已成功接收和處理資料。</span><span class="sxs-lookup"><span data-stu-id="0b404-177">If it can process the data, the client examines the **fAckReq** member of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure to determine whether the server requested that it be informed that the client received and processed the data successfully.</span></span> <span data-ttu-id="0b404-178">如果伺服器已要求這種資訊，用戶端會傳送正面的 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息給伺服器。</span><span class="sxs-lookup"><span data-stu-id="0b404-178">If the server did request this information, the client sends the server a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="0b404-179">因為解除鎖定資料會使資料指標失效，所以用戶端會先儲存 **fRelease** 成員的值，再解除鎖定資料物件。</span><span class="sxs-lookup"><span data-stu-id="0b404-179">Because unlocking data invalidates the pointer to the data, the client saves the value of the **fRelease** member before unlocking the data object.</span></span> <span data-ttu-id="0b404-180">儲存值之後，用戶端會檢查它，判斷伺服器應用程式是否要求用戶端釋放包含資料的記憶體;用戶端會據以運作。</span><span class="sxs-lookup"><span data-stu-id="0b404-180">After saving the value, the client then examines it to determine whether the server application requested the client to free the memory containing the data; the client acts accordingly.</span></span>

<span data-ttu-id="0b404-181">在收到負的 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息時，用戶端可以再次要求相同的專案值，並指定不同的剪貼簿格式。</span><span class="sxs-lookup"><span data-stu-id="0b404-181">Upon receiving a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the client can ask for the same item value again, specifying a different clipboard format.</span></span> <span data-ttu-id="0b404-182">一般而言，用戶端會先要求其可支援的最複雜格式，然後在必要時透過逐漸簡化的格式逐步執行，直到找到伺服器可以提供的格式為止。</span><span class="sxs-lookup"><span data-stu-id="0b404-182">Typically, a client will first ask for the most complex format it can support, then step down if necessary through progressively simpler formats until it finds one the server can provide.</span></span>

<span data-ttu-id="0b404-183">如果伺服器支援系統主題的格式專案，用戶端可以判斷伺服器支援的剪貼簿格式，而不是在每次用戶端要求專案時進行判斷。</span><span class="sxs-lookup"><span data-stu-id="0b404-183">If the server supports the Formats item of the system topic, the client can determine once what clipboard formats the server supports, instead of determining them each time the client requests an item.</span></span>

### <a name="submitting-an-item-to-the-server"></a><span data-ttu-id="0b404-184">將專案提交至伺服器</span><span class="sxs-lookup"><span data-stu-id="0b404-184">Submitting an Item to the Server</span></span>

<span data-ttu-id="0b404-185">用戶端可以使用 [**WM \_ DDE \_**](wm-dde-poke.md) 請求訊息，將專案值傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="0b404-185">The client may send an item value to the server by using the [**WM\_DDE\_POKE**](wm-dde-poke.md) message.</span></span> <span data-ttu-id="0b404-186">用戶端會呈現要傳送的專案，並傳送 **WM \_ DDE \_** 傳送訊息，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="0b404-186">The client renders the item to be sent and sends the **WM\_DDE\_POKE** message, as illustrated in the following example.</span></span>


```
size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hPokeData = GlobalAlloc(GMEM_MOVEABLE,
  (LONG) sizeof(DDEPOKE) + *pcch + 2))) 
{
    return; 
}
 
if (!(lpPokeData = (DDEPOKE *) GlobalLock(hPokeData))) 
{ 
    GlobalFree(hPokeData); 
    return; 
} 
 
lpPokeData->fRelease = TRUE; 
lpPokeData->cfFormat = CF_TEXT;
hResult = StringCchCopy((LPSTR) lpPokeData->Value, *pcch +1, (LPCSTR) szValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}  
 
// Each line of CF_TEXT data is terminated by CR/LF. 
hResult = StringCchCat((LPSTR) lpPokeData->Value, *pcch + 3, (LPCSTR) "\r\n");
if (FAILED(hResult)
{
// TODO: Write error handler.
 return;
}
GlobalUnlock(hPokeData); 
if ((atomItem = GlobalAddAtom((LPSTR) szItem)) != 0) 
{ 
 
        if (!PostMessage(hwndServerDDE, 
                WM_DDE_POKE, 
                (WPARAM) hwndClientDDE, 
                PackDDElParam(WM_DDE_POKE, (UINT) hPokeData, 
                    atomItem))) 
        { 
            GlobalDeleteAtom(atomItem); 
            GlobalFree(hPokeData); 
        } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
} 
```



> [!Note]  
> <span data-ttu-id="0b404-187">使用 [**wm \_ dde \_**](wm-dde-poke.md) 訊息傳送資料時，基本上與使用 [**wm \_ dde \_ 資料**](wm-dde-data.md)傳送資料相同，不同之處在于從用戶端將 **wm \_ dde \_** 傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="0b404-187">Sending data by using a [**WM\_DDE\_POKE**](wm-dde-poke.md) message is essentially the same as sending it by using [**WM\_DDE\_DATA**](wm-dde-data.md), except that **WM\_DDE\_POKE** is sent from the client to the server.</span></span>

 

<span data-ttu-id="0b404-188">如果伺服器能夠接受用戶端所轉譯格式的資料項目目值，伺服器會適當地處理專案值，並傳送正面的 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息給用戶端。</span><span class="sxs-lookup"><span data-stu-id="0b404-188">If the server is able to accept the data-item value in the format rendered by the client, the server processes the item value as appropriate and sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span> <span data-ttu-id="0b404-189">如果它無法處理專案值（因為其格式或基於其他原因），伺服器會傳送負的 **WM \_ DDE \_** 通知訊息給用戶端。</span><span class="sxs-lookup"><span data-stu-id="0b404-189">If it is unable to process the item value, because of its format or for other reasons, the server sends the client a negative **WM\_DDE\_ACK** message.</span></span>


```
UnpackDDElParam(WM_DDE_POKE, lParam, (PUINT) &hPokeData, 
    (PUINT) &atomItem); 
GlobalGetAtomName(atomItem, szItemName, ITEM_NAME_MAX_SIZE); 
if (!(lpPokeData = (DDEPOKE *) GlobalLock(hPokeData)) 
        || lpPokeData->cfFormat != CF_TEXT 
        || !IsItemSupportedByServer(szItemName)) 
{ 
    PostMessage(hwndClientDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndServerDDE, 
        PackDDElParam(WM_DDE_ACK, 0, atomItem)); // negative ACK  
}
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
} 
hResult = StringCchCopy(szItemValue, *pcch +1, lpPokeData->Value); // copies value 
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}  
bRelease = lpPokeData->fRelease; 
GlobalUnlock(hPokeData); 
if (bRelease) 
{ 
    GlobalFree(hPokeData); 
} 
 
PostMessage(hwndClientDDE, 
    WM_DDE_ACK, 
    (WPARAM) hwndServerDDE, 
    PackDDElParam(WM_DDE_ACK, 
         0x8000, atomItem));    // positive ACK.
```



<span data-ttu-id="0b404-190">在此範例中，伺服器會呼叫 [**GlobalGetAtomName**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) ，以抓取用戶端傳送的專案名稱。</span><span class="sxs-lookup"><span data-stu-id="0b404-190">In this example, the server calls [**GlobalGetAtomName**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) to retrieve the name of the item the client sent.</span></span> <span data-ttu-id="0b404-191">伺服器接著會判斷它是否支援該專案，以及專案是否以正確的格式轉譯 (也就是 CF \_ 文字) 。</span><span class="sxs-lookup"><span data-stu-id="0b404-191">The server then determines whether it supports the item and whether the item is rendered in the correct format (that is, CF\_TEXT).</span></span> <span data-ttu-id="0b404-192">如果專案不受支援且未以正確的格式轉譯，或伺服器無法鎖定資料的記憶體，則伺服器會將負認可傳回用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="0b404-192">If the item is not supported and not rendered in the correct format, or if the server cannot lock the memory for the data, the server sends a negative acknowledgment back to the client application.</span></span> <span data-ttu-id="0b404-193">請注意，在這種情況下，傳送負認可是正確的，因為通常會假設有一組 **fAckReq** 成員設定了 [**WM \_ DDE \_**](wm-dde-poke.md)訊息。</span><span class="sxs-lookup"><span data-stu-id="0b404-193">Note that in this case, sending a negative acknowledgment is correct because [**WM\_DDE\_POKE**](wm-dde-poke.md) messages are always assumed to have the **fAckReq** member set.</span></span> <span data-ttu-id="0b404-194">伺服器應該忽略成員。</span><span class="sxs-lookup"><span data-stu-id="0b404-194">The server should ignore the member.</span></span>

<span data-ttu-id="0b404-195">如果伺服器傳送負認可以回應 [**WM \_ dde \_**](wm-dde-poke.md)傳送訊息，則用戶端會負責釋出記憶體 (，但不是由與負值通知相關聯之 **WM \_ \_ DDE** 訊息所參考的 *lParam* 參數) 。</span><span class="sxs-lookup"><span data-stu-id="0b404-195">If a server sends a negative acknowledgment in response to a [**WM\_DDE\_POKE**](wm-dde-poke.md) message, the client is responsible for freeing the memory (but not the *lParam* parameter) referenced by the **WM\_DDE\_POKE** message associated with the negative acknowledgment.</span></span>

## <a name="establishing-a-permanent-data-link"></a><span data-ttu-id="0b404-196">建立永久資料連結</span><span class="sxs-lookup"><span data-stu-id="0b404-196">Establishing a Permanent Data Link</span></span>

<span data-ttu-id="0b404-197">用戶端應用程式可以使用 DDE，在伺服器應用程式中建立專案的連結。</span><span class="sxs-lookup"><span data-stu-id="0b404-197">A client application can use DDE to establish a link to an item in a server application.</span></span> <span data-ttu-id="0b404-198">建立這類連結之後，伺服器會將連結專案的定期更新傳送至用戶端，通常是每當專案的值變更時。</span><span class="sxs-lookup"><span data-stu-id="0b404-198">After such a link is established, the server sends periodic updates of the linked item to the client, typically, whenever the value of the item changes.</span></span> <span data-ttu-id="0b404-199">因此，會在兩個應用程式之間建立永久資料流程;此資料流程會維持在原處，直到明確地中斷連接為止。</span><span class="sxs-lookup"><span data-stu-id="0b404-199">Thus, a permanent data stream is established between the two applications; this data stream remains in place until it is explicitly disconnected.</span></span>

### <a name="initiating-a-data-link"></a><span data-ttu-id="0b404-200">起始資料連結</span><span class="sxs-lookup"><span data-stu-id="0b404-200">Initiating a Data Link</span></span>

<span data-ttu-id="0b404-201">用戶端會藉由張貼 [**WM \_ DDE \_ 建議**](wm-dde-advise.md) 訊息來起始資料連結，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="0b404-201">The client initiates a data link by posting a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message, as shown in the following example.</span></span>


```
if (!(hOptions = GlobalAlloc(GMEM_MOVEABLE, 
        sizeof(DDEADVISE)))) 
    return; 
if (!(lpOptions = (DDEADVISE FAR*) GlobalLock(hOptions))) 
{ 
    GlobalFree(hOptions); 
    return; 
} 
 
lpOptions->cfFormat = CF_TEXT; 
lpOptions->fAckReq = TRUE; 
lpOptions->fDeferUpd = FALSE; 
GlobalUnlock(hOptions); 
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!(PostMessage(hwndServerDDE, 
            WM_DDE_ADVISE, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_ADVISE, (UINT) hOptions, 
                atomItem)))) 
    { 
        GlobalDeleteAtom(atomItem); 
        GlobalFree(hOptions); 
        FreeDDElParam(WM_DDE_ADVISE, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors 
 
}
```



<span data-ttu-id="0b404-202">在此範例中，用戶端應用程式會將 [**WM \_ DDE \_ 建議**](wm-dde-advise.md)訊息的 **FDeferUpd** 旗標設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="0b404-202">In this example, the client application sets the **fDeferUpd** flag of the [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message to **FALSE**.</span></span> <span data-ttu-id="0b404-203">這會指示伺服器應用程式在資料變更時，將資料傳送給用戶端。</span><span class="sxs-lookup"><span data-stu-id="0b404-203">This directs the server application to send the data to the client whenever the data changes.</span></span>

<span data-ttu-id="0b404-204">如果伺服器無法服務 [**WM \_ dde \_ 建議**](wm-dde-advise.md) 要求，它會傳送負的 [**wm \_ dde \_**](wm-dde-ack.md) 通知訊息給用戶端。</span><span class="sxs-lookup"><span data-stu-id="0b404-204">If the server is unable to service the [**WM\_DDE\_ADVISE**](wm-dde-advise.md) request, it sends the client a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span> <span data-ttu-id="0b404-205">但是，如果伺服器具有專案的存取權，而且可以使用要求的格式來轉譯，則伺服器會注意到新的連結 (重新叫用 *hOptions*) 參數中指定的旗標，並傳送給用戶端一個正的 **WM \_ DDE \_** 通知訊息。</span><span class="sxs-lookup"><span data-stu-id="0b404-205">But if the server has access to the item and can render it in the requested format, the server notes the new link (recalling the flags specified in the *hOptions* parameter) and sends the client a positive **WM\_DDE\_ACK** message.</span></span> <span data-ttu-id="0b404-206">然後，在用戶端發出相符的 [**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md) 訊息之前，伺服器會在每次伺服器中專案的值變更時，將新的資料傳送給用戶端。</span><span class="sxs-lookup"><span data-stu-id="0b404-206">From then on, until the client issues a matching [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message, the server sends the new data to the client every time the value of the item changes in the server.</span></span>

<span data-ttu-id="0b404-207">[**WM \_ DDE \_ 建議**](wm-dde-advise.md)訊息會建立連結期間要交換的資料格式。</span><span class="sxs-lookup"><span data-stu-id="0b404-207">The [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message establishes the format of the data to be exchanged during the link.</span></span> <span data-ttu-id="0b404-208">如果用戶端嘗試使用相同的專案建立另一個連結，但使用不同的資料格式，伺服器可以選擇拒絕第二個資料格式，或嘗試支援它。</span><span class="sxs-lookup"><span data-stu-id="0b404-208">If the client attempts to establish another link with the same item but is using a different data format, the server can choose to reject the second data format or attempt to support it.</span></span> <span data-ttu-id="0b404-209">如果已為任何資料項目建立暖連結，伺服器一次只能支援一種資料格式。</span><span class="sxs-lookup"><span data-stu-id="0b404-209">If a warm link has been established for any data item, the server can support only one data format at a time.</span></span> <span data-ttu-id="0b404-210">這是因為暖連結的 [**WM \_ DDE \_ 資料**](wm-dde-data.md) 訊息有 **Null** 資料控制碼，否則會包含格式資訊。</span><span class="sxs-lookup"><span data-stu-id="0b404-210">This is because the [**WM\_DDE\_DATA**](wm-dde-data.md) message for a warm link has a **NULL** data handle, which otherwise contains the format information.</span></span> <span data-ttu-id="0b404-211">因此，伺服器必須拒絕已連結專案的所有暖連結，並且必須拒絕具有暖連結之專案的所有連結。</span><span class="sxs-lookup"><span data-stu-id="0b404-211">Thus, a server must reject all warm links for an item already linked, and must reject all links for an item that has warm links.</span></span> <span data-ttu-id="0b404-212">另一項轉譯可能是當要求相同資料項目的第二個連結時，伺服器會變更連結的格式和經常性存取狀態。</span><span class="sxs-lookup"><span data-stu-id="0b404-212">Another interpretation may be that the server changes the format and the hot or warm state of a link when a second link is requested for the same data item.</span></span>

<span data-ttu-id="0b404-213">一般而言，用戶端應用程式不應該嘗試一次為數據項建立多個連結。</span><span class="sxs-lookup"><span data-stu-id="0b404-213">In general, client applications should not attempt to establish more than one link at a time for a data item.</span></span>

### <a name="initiating-a-data-link-with-the-paste-link-command"></a><span data-ttu-id="0b404-214">使用貼上連結命令起始資料連結</span><span class="sxs-lookup"><span data-stu-id="0b404-214">Initiating a Data Link with the Paste Link Command</span></span>

<span data-ttu-id="0b404-215">支援經常性存取或暖資料連結的應用程式通常支援名稱為 Link 的已註冊剪貼簿格式。</span><span class="sxs-lookup"><span data-stu-id="0b404-215">Applications that support hot or warm data links typically support a registered clipboard format named Link.</span></span> <span data-ttu-id="0b404-216">當與應用程式的複製和貼上連結命令相關聯時，此剪貼簿格式可讓使用者在應用程式之間建立 DDE 交談，只要複製伺服器應用程式中的資料項目，然後將它貼入用戶端應用程式即可。</span><span class="sxs-lookup"><span data-stu-id="0b404-216">When associated with the application's Copy and Paste Link commands, this clipboard format enables the user to establish DDE conversations between applications simply by copying a data item in the server application and pasting it into the client application.</span></span>

<span data-ttu-id="0b404-217">當使用者從 [**編輯**] 功能表中選擇 [**複製**] 命令時，伺服器應用程式會將包含應用程式、主題和專案名稱的字串放在剪貼簿中，以支援連結剪貼簿格式。</span><span class="sxs-lookup"><span data-stu-id="0b404-217">A server application supports the Link clipboard format by placing in the clipboard a string containing the application, topic, and item names when the user chooses the **Copy** command from the **Edit** menu.</span></span> <span data-ttu-id="0b404-218">以下是標準連結格式：</span><span class="sxs-lookup"><span data-stu-id="0b404-218">Following is the standard Link format:</span></span>

<span data-ttu-id="0b404-219">*應用程式 ***\\ 0*** 主題 ***\\ 0*** 專案 \* \* \\ \* \\ 0 0*\*</span><span class="sxs-lookup"><span data-stu-id="0b404-219">*application ***\\0*** topic ***\\0*** item\*\*\*\\0\\0*\*</span></span>

<span data-ttu-id="0b404-220">單一 null 字元會分隔名稱，而兩個 null 字元會結束整個字串。</span><span class="sxs-lookup"><span data-stu-id="0b404-220">A single null character separates the names, and two null characters terminate the entire string.</span></span>

<span data-ttu-id="0b404-221">用戶端和伺服器應用程式都必須註冊連結剪貼簿格式，如下所示：</span><span class="sxs-lookup"><span data-stu-id="0b404-221">Both the client and server applications must register the Link clipboard format, as shown:</span></span>


```
cfLink = RegisterClipboardFormat("Link");
```



<span data-ttu-id="0b404-222">用戶端應用程式透過 [編輯] 功能表上的 [貼上連結] 命令，支援連結剪貼簿格式。</span><span class="sxs-lookup"><span data-stu-id="0b404-222">A client application supports the Link clipboard format by means of a Paste Link command on its Edit menu.</span></span> <span data-ttu-id="0b404-223">當使用者選擇此命令時，用戶端應用程式會從連結格式的剪貼簿資料剖析應用程式、主題和專案名稱。</span><span class="sxs-lookup"><span data-stu-id="0b404-223">When the user chooses this command, the client application parses the application, topic, and item names from the Link-format clipboard data.</span></span> <span data-ttu-id="0b404-224">使用這些名稱，如果這類交談尚未存在，用戶端應用程式就會起始應用程式和主題的交談。</span><span class="sxs-lookup"><span data-stu-id="0b404-224">Using these names, the client application initiates a conversation for the application and topic, if such a conversation does not already exist.</span></span> <span data-ttu-id="0b404-225">然後，用戶端應用程式會將 [**WM \_ DDE \_ 建議**](wm-dde-advise.md) 訊息傳送至伺服器應用程式，並指定連結格式剪貼簿資料中包含的專案名稱。</span><span class="sxs-lookup"><span data-stu-id="0b404-225">The client application then sends a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message to the server application, specifying the item name contained in the Link-format clipboard data.</span></span>

<span data-ttu-id="0b404-226">以下是當使用者選擇 [貼上] 連結命令時，用戶端應用程式的回應範例。</span><span class="sxs-lookup"><span data-stu-id="0b404-226">Following is an example of a client application's response when the user chooses the Paste Link command.</span></span>


```
void DoPasteLink(hwndClientDDE) 
HWND hwndClientDDE; 
{ 
    HANDLE hData; 
    LPSTR lpData; 
    HWND hwndServerDDE; 
    CHAR szApplication[APP_MAX_SIZE + 1]; 
    CHAR szTopic[TOPIC_MAX_SIZE + 1]; 
    CHAR szItem[ITEM_MAX_SIZE + 1]; 
    size_t * nBufLen; 
 HRESULT hResult;
 
    if (OpenClipboard(hwndClientDDE)) 
    { 
        if (!(hData = GetClipboardData(cfLink)) || 
                !(lpData = GlobalLock(hData))) 
        { 
            CloseClipboard(); 
            return; 
        } 
 
        // Parse the clipboard data.
  hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
// TODO: Write error handler.
  return;
 }
 if (*nBufLen >= APP_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }
 hResult = StringCchCopy(szApplication, APP_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
// TODO: Write error handler.
  return;
 }
        lpData += (*nBufLen + 1); // skips over null
 hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
 // TODO: Write error handler.
  return;
 }
 if (*nBufLen >= TOPIC_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }
 hResult = StringCchCopy(szTopic, TOPIC_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
 // TODO: Write error handler.
  return;
 }
        lpData += (nBufLen + 1); // skips over null
 hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
 // TODO: Write error handler.
  return;
 }
 if (*nBufLen >= ITEM_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }

 hResult = StringCchCopy(szItem, ITEM_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
 // TODO: Write error handler.
  return;
 } 
        GlobalUnlock(hData); 
        CloseClipboard(); 
 
        if (hwndServerDDE = 
                FindServerGivenAppTopic(szApplication, szTopic)) 
        { 
            // App/topic conversation is already started. 
 
            if (DoesAdviseAlreadyExist(hwndServerDDE, szItem)) 
            {
                MessageBox(hwndMain, 
                    "Advisory already established", 
                    "Client", MB_ICONEXCLAMATION | MB_OK); 
            }
            else SendAdvise(hwndClientDDE, hwndServerDDE, szItem); 
        } 
        else 
        { 
            // Client must initiate a new conversation first. 
            SendInitiate(szApplication, szTopic); 
            if (hwndServerDDE = 
                    FindServerGivenAppTopic(szApplication, 
                        szTopic)) 
            {
                SendAdvise(hwndClientDDE, hwndServerDDE, szItem); 
            }
        } 
    } 
    return; 
}
```



<span data-ttu-id="0b404-227">在此範例中，用戶端應用程式會開啟剪貼簿，並判斷它是否包含連結格式的資料 (也就是先前註冊的 cfLink) 。</span><span class="sxs-lookup"><span data-stu-id="0b404-227">In this example, the client application opens the clipboard and determines whether it contains data in the Link format (that is, cfLink) it had previously registered.</span></span> <span data-ttu-id="0b404-228">如果沒有，或如果它無法鎖定剪貼簿中的資料，用戶端會傳回。</span><span class="sxs-lookup"><span data-stu-id="0b404-228">If not, or if it cannot lock the data in the clipboard, the client returns.</span></span>

<span data-ttu-id="0b404-229">在用戶端應用程式抓取剪貼簿資料的指標之後，它會剖析資料以解壓縮應用程式、主題和專案名稱。</span><span class="sxs-lookup"><span data-stu-id="0b404-229">After the client application retrieves a pointer to the clipboard data, it parses the data to extract the application, topic, and item names.</span></span>

<span data-ttu-id="0b404-230">用戶端應用程式會判斷主題的交談是否已存在於此主題與伺服器應用程式之間。</span><span class="sxs-lookup"><span data-stu-id="0b404-230">The client application determines whether a conversation on the topic already exists between it and the server application.</span></span> <span data-ttu-id="0b404-231">如果有交談存在，用戶端會檢查該資料項目是否已有連結。</span><span class="sxs-lookup"><span data-stu-id="0b404-231">If a conversation does exist, the client checks whether a link already exists for the data item.</span></span> <span data-ttu-id="0b404-232">如果有這類連結，用戶端會向使用者顯示訊息方塊。否則，它會呼叫它自己的 *SendAdvise* 函式，將 [**WM \_ DDE \_ 建議**](wm-dde-advise.md) 訊息傳送至該專案的伺服器。</span><span class="sxs-lookup"><span data-stu-id="0b404-232">If such a link exists, the client displays a message box to the user; otherwise, it calls its own *SendAdvise* function to send a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message to the server for the item.</span></span>

<span data-ttu-id="0b404-233">如果用戶端與伺服器之間尚未有主題的交談，用戶端會先呼叫它自己的 *SendInitiate* 函式來廣播 [**WM \_ DDE \_ 初始**](wm-dde-initiate.md) 訊息來要求交談，而第二個呼叫它自己的 *FindServerGivenAppTopic* 函式，以建立與代表伺服器應用程式回應之視窗的交談。</span><span class="sxs-lookup"><span data-stu-id="0b404-233">If a conversation on the topic does not already exist between the client and the server, the client first calls its own *SendInitiate* function to broadcast the [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message to request a conversation and, second, calls its own *FindServerGivenAppTopic* function to establish the conversation with the window that responds on behalf of the server application.</span></span> <span data-ttu-id="0b404-234">交談開始之後，用戶端應用程式會呼叫 *SendAdvise* 以要求連結。</span><span class="sxs-lookup"><span data-stu-id="0b404-234">After the conversation has begun, the client application calls *SendAdvise* to request the link.</span></span>

### <a name="notifying-the-client-that-data-has-changed"></a><span data-ttu-id="0b404-235">通知用戶端資料已變更</span><span class="sxs-lookup"><span data-stu-id="0b404-235">Notifying the Client that Data Has Changed</span></span>

<span data-ttu-id="0b404-236">當用戶端使用 [**WM \_ DDE \_ 建議**](wm-dde-advise.md) 訊息來建立連結時，若 **fDeferUpd** 成員未設定 (也就是在 [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) 結構中等於零) ，則用戶端會在每次專案的值變更時，要求伺服器傳送資料項目目。</span><span class="sxs-lookup"><span data-stu-id="0b404-236">When the client establishes a link by using the [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message, with the **fDeferUpd** member not set (that is, equal to zero) in the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure, the client has requested the server send the data item each time the item's value changes.</span></span> <span data-ttu-id="0b404-237">在這種情況下，伺服器會以先前指定的格式轉譯資料項目的新值，並傳送 [**WM \_ DDE \_ 資料**](wm-dde-data.md) 訊息給用戶端，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="0b404-237">In such cases, the server renders the new value of the data item in the previously specified format and sends the client a [**WM\_DDE\_DATA**](wm-dde-data.md) message, as shown in the following example.</span></span>


```
// Allocate the size of a DDE data header, plus data (a string), 
// plus a <CR><LF><NULL> 

size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hData = GlobalAlloc(GMEM_MOVEABLE,
  sizeof(DDEDATA) + *pcch + 3))) 
{
    return; 
}
if (!(lpData = (DDEDATA FAR*) GlobalLock(hData))) 
{ 
    GlobalFree(hData); 
    return; 
} 
lpData->fAckReq = bAckRequest;       // as in original WM_DDE_ADVISE 
lpData->cfFormat = CF_TEXT;
hResult = StringCchCopy(lpData->Value, *pcch +1, szItemValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
// add CR/LF for CF_TEXT format
hResult = StringCchCat(lpData->Value, *pcch + 3, "\r\n");
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
GlobalUnlock(hData); 
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndClientDDE, 
            WM_DDE_DATA, 
            (WPARAM) hwndServerDDE, 
            PackDDElParam(WM_DDE_DATA, (UINT) hData, atomItem))) 
    { 
        GlobalFree(hData); 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_DATA, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
 
}
```



<span data-ttu-id="0b404-238">在此範例中，用戶端會適當地處理專案值。</span><span class="sxs-lookup"><span data-stu-id="0b404-238">In this example, the client processes the item value as appropriate.</span></span> <span data-ttu-id="0b404-239">如果已設定專案的 **fAckReq** 旗標，用戶端會傳送正的 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息給伺服器。</span><span class="sxs-lookup"><span data-stu-id="0b404-239">If the **fAckReq** flag for the item is set, the client sends the server a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="0b404-240">當用戶端建立連結時，若 **fDeferUpd** 成員集 (也就是等於 1) ，用戶端要求每次資料變更時，都只會傳送通知，而不是資料本身。</span><span class="sxs-lookup"><span data-stu-id="0b404-240">When the client establishes the link, with the **fDeferUpd** member set (that is, equal to 1), the client has requested that only a notification, not the data itself, be sent each time the data changes.</span></span> <span data-ttu-id="0b404-241">在這種情況下，當專案值變更時，伺服器不會轉譯該值，而只會傳送具有 null 資料控制碼的 [**WM \_ DDE \_ 資料**](wm-dde-data.md) 訊息給用戶端，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="0b404-241">In such cases, when the item value changes, the server does not render the value but simply sends the client a [**WM\_DDE\_DATA**](wm-dde-data.md) message with a null data handle, as illustrated in the following example.</span></span>


```
if (bDeferUpd)      // check whether flag was set in WM_DDE_ADVISE
{
    if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
    { 
        if (!PostMessage(hwndClientDDE, 
                WM_DDE_DATA, 
                (WPARAM) hwndServerDDE, 
                PackDDElParam(WM_DDE_DATA, 0, 
                    atomItem)))                  // NULL data
        {
            GlobalDeleteAtom(atomItem); 
            FreeDDElParam(WM_DDE_DATA, lParam); 
        } 
    } 
} 
 
if (atomItem == 0) 
{ 
     // Handle errors. 
} 
```



<span data-ttu-id="0b404-242">必要時，用戶端可以藉由發出一般的 [**WM \_ DDE \_ 要求**](wm-dde-request.md) 訊息來要求資料項目的最新值，也可以直接忽略來自伺服器的資料已變更的通知。</span><span class="sxs-lookup"><span data-stu-id="0b404-242">As necessary, the client can request the latest value of the data item by issuing a normal [**WM\_DDE\_REQUEST**](wm-dde-request.md) message, or it can simply ignore the notice from the server that the data has changed.</span></span> <span data-ttu-id="0b404-243">在任何一種情況下，如果 **fAckReq** 等於1，用戶端應該會將正面的 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="0b404-243">In either case, if **fAckReq** is equal to 1, the client is expected to send a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message to the server.</span></span>

### <a name="terminating-a-data-link"></a><span data-ttu-id="0b404-244">終止資料連結</span><span class="sxs-lookup"><span data-stu-id="0b404-244">Terminating a Data Link</span></span>

<span data-ttu-id="0b404-245">如果用戶端要求終止特定的資料連結，用戶端會傳送 [**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md) 訊息給伺服器，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="0b404-245">If the client requests that a specific data link be terminated, the client sends the server a [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message, as shown in the following example.</span></span>


```
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndServerDDE, 
            WM_DDE_UNADVISE, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_UNADVISE, 0, atomItem))) 
    { 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_UNADVISE, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
}
```



<span data-ttu-id="0b404-246">伺服器會檢查用戶端目前是否有此交談中特定專案的連結。</span><span class="sxs-lookup"><span data-stu-id="0b404-246">The server checks whether the client currently has a link to the specific item in this conversation.</span></span> <span data-ttu-id="0b404-247">如果連結存在，伺服器就會傳送正面的 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息給用戶端，然後再也不需要伺服器傳送專案的相關更新。</span><span class="sxs-lookup"><span data-stu-id="0b404-247">If a link exists, the server sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message; the server is then no longer required to send updates about the item.</span></span> <span data-ttu-id="0b404-248">如果沒有連結存在，伺服器會傳送負的 **WM \_ DDE \_** 通知訊息給用戶端。</span><span class="sxs-lookup"><span data-stu-id="0b404-248">If no link exists, the server sends the client a negative **WM\_DDE\_ACK** message.</span></span>

<span data-ttu-id="0b404-249">[**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md)訊息會指定資料格式。</span><span class="sxs-lookup"><span data-stu-id="0b404-249">The [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message specifies a data format.</span></span> <span data-ttu-id="0b404-250">如果已建立數個熱連結，且每個都使用不同的格式，則零的格式會通知伺服器停止指定專案的所有連結。</span><span class="sxs-lookup"><span data-stu-id="0b404-250">A format of zero informs the server to stop all links for the specified item, even if several hot links are established and each uses a different format.</span></span>

<span data-ttu-id="0b404-251">若要終止對話的所有連結，用戶端應用程式會使用 null 專案 atom 來傳送具有一個 [**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md) 訊息的伺服器。</span><span class="sxs-lookup"><span data-stu-id="0b404-251">To terminate all links for a conversation, the client application sends the server a [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message with a null item atom.</span></span> <span data-ttu-id="0b404-252">伺服器會判斷交談是否至少有一個目前已建立的連結。</span><span class="sxs-lookup"><span data-stu-id="0b404-252">The server determines whether the conversation has at least one link currently established.</span></span> <span data-ttu-id="0b404-253">如果連結存在，伺服器就會傳送正面的 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息給用戶端，然後伺服器就不再需要傳送對話中的任何更新。</span><span class="sxs-lookup"><span data-stu-id="0b404-253">If a link exists, the server sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message; the server then no longer has to send any updates in the conversation.</span></span> <span data-ttu-id="0b404-254">如果沒有連結存在，伺服器會傳送負的 **WM \_ DDE \_** 通知訊息給用戶端。</span><span class="sxs-lookup"><span data-stu-id="0b404-254">If no link exists, the server sends the client a negative **WM\_DDE\_ACK** message.</span></span>

## <a name="carrying-out-commands-in-a-server-application"></a><span data-ttu-id="0b404-255">在伺服器應用程式中執行命令</span><span class="sxs-lookup"><span data-stu-id="0b404-255">Carrying Out Commands in a Server Application</span></span>

<span data-ttu-id="0b404-256">應用程式可以使用 [**WM \_ DDE \_ 執行**](wm-dde-execute.md) 訊息，以在另一個應用程式中執行特定命令或一系列的命令。</span><span class="sxs-lookup"><span data-stu-id="0b404-256">Applications can use the [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message to cause a certain command or series of commands to be carried out in another application.</span></span> <span data-ttu-id="0b404-257">若要這樣做，用戶端會將包含控制碼的 **WM \_ DDE \_ 執行** 訊息傳送給伺服器，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="0b404-257">To do this, the client sends the server a **WM\_DDE\_EXECUTE** message containing a handle to a command string, as shown in the following example.</span></span>


```
HRESULT hResult;
  
if (!(hCommand = GlobalAlloc(GMEM_MOVEABLE, 
        sizeof(szCommandString) + 1))) 
{
    return; 
}
if (!(lpCommand = GlobalLock(hCommand))) 
{ 
    GlobalFree(hCommand); 
    return; 
} 

hResult = StringCbCopy(lpCommand, sizeof(szCommandString), szCommandString);
if (hResult != S_OK)
{
// TODO: Write error handler.
 return;
}
 
GlobalUnlock(hCommand); 
if (!PostMessage(hwndServerDDE, 
        WM_DDE_EXECUTE, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_EXECUTE, 0, (UINT) hCommand))) 
{ 
    GlobalFree(hCommand); 
    FreeDDElParam(WM_DDE_EXECUTE, lParam); 
}
```



<span data-ttu-id="0b404-258">在此範例中，伺服器會嘗試執行指定的命令字串。</span><span class="sxs-lookup"><span data-stu-id="0b404-258">In this example, the server attempts to carry out the specified command string.</span></span> <span data-ttu-id="0b404-259">如果成功，伺服器會傳送正面的 [**wm \_ dde \_**](wm-dde-ack.md) 通知訊息給用戶端; 否則，它會傳送負的 **wm \_ dde 的 \_ ack** 訊息。</span><span class="sxs-lookup"><span data-stu-id="0b404-259">If it succeeds, the server sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message; otherwise, it sends a negative **WM\_DDE\_ACK** message.</span></span> <span data-ttu-id="0b404-260">這個 **WM \_ dde \_** 通知訊息會重複使用原始 [**WM \_ Dde \_ 執行**](wm-dde-execute.md)訊息中傳遞的 *hCommand* 控制碼。</span><span class="sxs-lookup"><span data-stu-id="0b404-260">This **WM\_DDE\_ACK** message reuses the *hCommand* handle passed in the original [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message.</span></span>

<span data-ttu-id="0b404-261">如果用戶端的命令執行字串要求伺服器終止，伺服器應該藉由傳送正的 [**wm \_ dde \_ 確認**](wm-dde-ack.md) 訊息，然後在結束之前張貼 [**WM \_ dde \_ 終止**](wm-dde-terminate.md) 訊息來回應。</span><span class="sxs-lookup"><span data-stu-id="0b404-261">If the client's command execution string requests that the server terminate, the server should respond by sending a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message and then post a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message before terminating.</span></span> <span data-ttu-id="0b404-262">所有以 [**WM \_ dde \_ 執行**](wm-dde-execute.md) 訊息傳送的其他命令都應以同步方式執行; 也就是說，只有在成功完成命令之後，伺服器才應該傳送 **WM \_ dde \_** 通知訊息。</span><span class="sxs-lookup"><span data-stu-id="0b404-262">All other commands sent with a [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message should be executed synchronously; that is, the server should send a **WM\_DDE\_ACK** message only after successfully completing the command.</span></span>

## <a name="terminating-a-conversation"></a><span data-ttu-id="0b404-263">終止交談</span><span class="sxs-lookup"><span data-stu-id="0b404-263">Terminating a Conversation</span></span>

<span data-ttu-id="0b404-264">用戶端或伺服器可以發出 [**WM \_ DDE \_ 終止**](wm-dde-terminate.md) 訊息，以隨時終止交談。</span><span class="sxs-lookup"><span data-stu-id="0b404-264">Either the client or the server can issue a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message to terminate a conversation at any time.</span></span> <span data-ttu-id="0b404-265">同樣地，用戶端和伺服器應用程式都應該隨時準備好接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="0b404-265">Similarly, both the client and server applications should be prepared to receive this message at any time.</span></span> <span data-ttu-id="0b404-266">應用程式必須先終止所有的交談，才能關閉。</span><span class="sxs-lookup"><span data-stu-id="0b404-266">An application must terminate all of its conversations before shutting down.</span></span>

<span data-ttu-id="0b404-267">在下列範例中，終止交談的應用程式會張貼一個 [**WM \_ DDE \_ 終止**](wm-dde-terminate.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="0b404-267">In the following example, the application terminating the conversation posts a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message.</span></span>


```
PostMessage(hwndServerDDE, WM_DDE_TERMINATE, 
    (WPARAM) hwndClientDDE, 0);
```



<span data-ttu-id="0b404-268">這會通知另一個應用程式，傳送應用程式不會傳送任何其他訊息，而且收件者可以關閉其視窗。</span><span class="sxs-lookup"><span data-stu-id="0b404-268">This informs the other application that the sending application will send no further messages and the recipient can close its window.</span></span> <span data-ttu-id="0b404-269">在所有情況下，收件者預期會傳送 [**WM \_ DDE \_ 終止**](wm-dde-terminate.md) 訊息來立即回應。</span><span class="sxs-lookup"><span data-stu-id="0b404-269">The recipient is expected in all cases to respond promptly by sending a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message.</span></span> <span data-ttu-id="0b404-270">收件者不能傳送負、忙碌或正面的 [**WM \_ DDE \_ ACK**](wm-dde-ack.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="0b404-270">The recipient must not send a negative, busy, or positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="0b404-271">在應用程式將 [**WM \_ dde \_ 終止**](wm-dde-terminate.md) 訊息傳送給 DDE 交談中的夥伴之後，它就不能回應來自該夥伴的訊息，因為夥伴可能已損毀傳送回應的目標視窗。</span><span class="sxs-lookup"><span data-stu-id="0b404-271">After an application has sent the [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message to the partner in a DDE conversation, it must not respond to messages from that partner, since the partner might have destroyed the window to which the response would be sent.</span></span>

<span data-ttu-id="0b404-272">如果應用程式在發佈了 **wm dde \_ dde \_ terminate** 之後，收到非 [**wm \_ dde \_**](wm-dde-terminate.md)的 dde 訊息，則應該釋出與接收訊息相關聯的所有物件，但 **不** 含 **fRelease** 成員的 wm dde [**\_ \_ 資料**](wm-dde-data.md)或 [**WM \_ dde \_**](wm-dde-poke.md)郵件的資料控制碼除外。</span><span class="sxs-lookup"><span data-stu-id="0b404-272">If an application receives a DDE message other than [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) after it has posted **WM\_DDE\_TERMINATE**, it should free all objects associated with the received messages except the data handles for [**WM\_DDE\_DATA**](wm-dde-data.md) or [**WM\_DDE\_POKE**](wm-dde-poke.md) messages that do **not** have the **fRelease** member set.</span></span>

<span data-ttu-id="0b404-273">當應用程式即將終止時，它應該會在完成 [**WM \_**](/windows/desktop/winmsg/wm-destroy) 終結訊息的處理之前結束所有作用中的 DDE 交談。</span><span class="sxs-lookup"><span data-stu-id="0b404-273">When an application is about to terminate, it should end all active DDE conversations before completing processing of the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span> <span data-ttu-id="0b404-274">但是，如果應用程式未結束其使用中的 DDE 交談，則當視窗損毀時，系統會終止與視窗相關聯的任何 DDE 交談。</span><span class="sxs-lookup"><span data-stu-id="0b404-274">However, if an application does not end its active DDE conversations, the system will terminate any DDE conversations associated with a window when the window is destroyed.</span></span> <span data-ttu-id="0b404-275">下列範例顯示伺服器應用程式如何終止所有 DDE 交談。</span><span class="sxs-lookup"><span data-stu-id="0b404-275">The following example shows how a server application terminates all DDE conversations.</span></span>


```
void TerminateConversations(hwndServerDDE) 
HWND hwndServerDDE; 
{ 
    HWND hwndClientDDE; 
 
    // Terminate each active conversation. 
 
    while (hwndClientDDE = GetNextLink(hwndClientDDE)) 
    { 
        SendTerminate(hwndServerDDE, hwndClientDDE); 
    } 
    return; 
} 
 
BOOL AtLeastOneLinkActive(VOID) 
{ 
    return TRUE; 
} 
 
HWND GetNextLink(hwndDummy) 
    HWND hwndDummy; 
{ 
    return (HWND) 1; 
} 
 
VOID SendTerminate(HWND hwndServerDDE, HWND hwndClientDDE) 
{ 
    return; 
}
```



 

 