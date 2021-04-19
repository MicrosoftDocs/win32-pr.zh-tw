---
title: 對話管理
description: 本主題討論用戶端與伺服器之間的交談。
ms.assetid: 4e5ff1a1-d46a-4e2a-a37c-8df951f2a1ee
keywords:
- 'Windows 消費者介面，動態資料交換 (DDE) '
- 動態資料交換 (DDE) 、交談
- DDE (動態資料交換) 、交談
- '資料交換、動態資料交換 (DDE) '
- 'Windows 消費者介面、動態資料交換管理程式庫 (DDEML) '
- 動態資料交換管理程式庫 (DDEML) 、交談
- DDEML (動態資料交換管理程式庫) ，交談
- '資料交換、動態資料交換管理程式庫 (DDEML) '
- 動態資料交換 (DDE) 、多重對話
- DDE (動態資料交換) 、多重對話
- 動態資料交換管理程式庫 (DDEML) 、多重對話
- DDEML (動態資料交換管理程式庫) 、多重對話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ca1a0a8e02bceb6b2f69051d89df289871fdd42
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967224"
---
# <a name="conversation-management"></a><span data-ttu-id="783c4-115">對話管理</span><span class="sxs-lookup"><span data-stu-id="783c4-115">Conversation Management</span></span>

<span data-ttu-id="783c4-116">用戶端與伺服器之間的對話一律會在用戶端要求時建立。</span><span class="sxs-lookup"><span data-stu-id="783c4-116">A conversation between a client and a server is always established at the request of the client.</span></span> <span data-ttu-id="783c4-117">當交談建立時，每個夥伴都會收到識別交談的控制碼。</span><span class="sxs-lookup"><span data-stu-id="783c4-117">When a conversation is established, each partner receives a handle that identifies the conversation.</span></span> <span data-ttu-id="783c4-118">合作夥伴會在其他動態資料交換管理程式庫中使用此控制碼 (DDEML) 函式來傳送交易及管理交談。</span><span class="sxs-lookup"><span data-stu-id="783c4-118">The partners use this handle in other Dynamic Data Exchange Management Library (DDEML) functions to send transactions and manage the conversation.</span></span> <span data-ttu-id="783c4-119">用戶端可以要求與單一伺服器的對話，也可以要求與一或多部伺服器的多個交談。</span><span class="sxs-lookup"><span data-stu-id="783c4-119">A client can request a conversation with a single server, or it can request multiple conversations with one or more servers.</span></span>

<span data-ttu-id="783c4-120">下列主題描述應用程式如何建立新的交談，並取得現有交談的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="783c4-120">The following topics describe how an application establishes new conversations and gets information about existing conversations.</span></span>

-   [<span data-ttu-id="783c4-121">單一對話</span><span class="sxs-lookup"><span data-stu-id="783c4-121">Single Conversations</span></span>](#single-conversations)
-   [<span data-ttu-id="783c4-122">多個交談</span><span class="sxs-lookup"><span data-stu-id="783c4-122">Multiple Conversations</span></span>](#multiple-conversations)

## <a name="single-conversations"></a><span data-ttu-id="783c4-123">單一對話</span><span class="sxs-lookup"><span data-stu-id="783c4-123">Single Conversations</span></span>

<span data-ttu-id="783c4-124">用戶端應用程式會藉由呼叫 [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) 函式並指定字串控制碼來識別包含伺服器應用程式服務名稱的字串，以及交談的主題名稱，要求與伺服器的單一交談。</span><span class="sxs-lookup"><span data-stu-id="783c4-124">A client application requests a single conversation with a server by calling the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) function and specifying string handles that identify the strings containing the service name of the server application and the topic name for the conversation.</span></span> <span data-ttu-id="783c4-125">DDEML 會將 [**XTYP \_ CONNECT**](xtyp-connect.md) 交易傳送至每個伺服器應用程式的動態資料交換 (DDE) 回呼函式，該函式已註冊符合 **DdeConnect** 中指定的服務名稱，或藉由呼叫 [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)來關閉服務名稱篩選功能。</span><span class="sxs-lookup"><span data-stu-id="783c4-125">The DDEML responds by sending the [**XTYP\_CONNECT**](xtyp-connect.md) transaction to the Dynamic Data Exchange (DDE) callback function of each server application that either has registered a service name that matches the one specified in **DdeConnect** or has turned service name filtering off by calling [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice).</span></span> <span data-ttu-id="783c4-126">伺服器也可以藉由 **在 \_** \_ \_ [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) 函數中指定 CBF FAIL CONNECTIONS 篩選旗標，來篩選 XTYP CONNECT 交易。</span><span class="sxs-lookup"><span data-stu-id="783c4-126">A server can also filter **XTYP\_CONNECT** transactions by specifying the CBF\_FAIL\_CONNECTIONS filter flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span> <span data-ttu-id="783c4-127">在 **XTYP \_ CONNECT** 交易期間，DDEML 會將服務名稱和主題名稱傳遞至伺服器。</span><span class="sxs-lookup"><span data-stu-id="783c4-127">During the **XTYP\_CONNECT** transaction, the DDEML passes the service name and the topic name to the server.</span></span> <span data-ttu-id="783c4-128">伺服器必須檢查名稱，如果它支援服務名稱和主題名稱組，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="783c4-128">The server must examine the names and return **TRUE** if it supports the service name and topic name pair or **FALSE** if it does not.</span></span>

<span data-ttu-id="783c4-129">如果沒有伺服器回應用戶端的連線要求，用戶端會從 [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)接收 **Null** ，且不會建立任何交談。</span><span class="sxs-lookup"><span data-stu-id="783c4-129">If no server responds positively to the client's request to connect, the client receives **NULL** from [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) and no conversation is established.</span></span> <span data-ttu-id="783c4-130">如果伺服器傳回 **TRUE**，就會建立交談，且用戶端會收到交談控制碼，此為識別交談的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="783c4-130">If a server returns **TRUE**, a conversation is established and the client receives a conversation handle — a **DWORD** value that identifies the conversation.</span></span> <span data-ttu-id="783c4-131">用戶端會使用後續 DDEML 呼叫中的控制碼，從伺服器取得資料。</span><span class="sxs-lookup"><span data-stu-id="783c4-131">The client uses the handle in subsequent DDEML calls to obtain data from the server.</span></span> <span data-ttu-id="783c4-132">伺服器會接收 [**XTYP \_ CONNECT \_ CONFIRM**](xtyp-connect-confirm.md) 交易 (除非伺服器指定 CBF \_ SKIP \_ connect \_ 確認篩選旗標) 。</span><span class="sxs-lookup"><span data-stu-id="783c4-132">The server receives the [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction (unless the server specified the CBF\_SKIP\_CONNECT\_CONFIRMS filter flag).</span></span> <span data-ttu-id="783c4-133">此交易會將交談控制碼傳遞至伺服器。</span><span class="sxs-lookup"><span data-stu-id="783c4-133">This transaction passes the conversation handle to the server.</span></span>

<span data-ttu-id="783c4-134">下列範例會要求系統主題上的交談，以及可辨識服務名稱 MyServer 的伺服器。</span><span class="sxs-lookup"><span data-stu-id="783c4-134">The following example requests a conversation on the System topic with a server that recognizes the service name MyServer.</span></span> <span data-ttu-id="783c4-135">*HszServName* 和 *hszSysTopic* 參數是先前建立的字串控制碼。</span><span class="sxs-lookup"><span data-stu-id="783c4-135">The *hszServName* and *hszSysTopic* parameters are previously created string handles.</span></span>


```
HCONV hConv;         // conversation handle 
HWND hwndParent;     // parent window handle 
HSZ hszServName;     // service name string handle 
HSZ hszSysTopic;     // System topic string handle 
 
hConv = DdeConnect( 
    idInst,               // instance identifier 
    hszServName,          // service name string handle 
    hszSysTopic,          // System topic string handle 
    (PCONVCONTEXT) NULL); // use default context 
 
if (hConv == NULL) 
{ 
    MessageBox(hwndParent, "MyServer is unavailable.", 
        (LPSTR) NULL, MB_OK); 
    return FALSE; 
} 
```



<span data-ttu-id="783c4-136">在上述範例中， [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) 會讓 MyServer 應用程式的 DDE 回呼函式收到 [**XTYP \_ CONNECT**](xtyp-connect.md) 交易。</span><span class="sxs-lookup"><span data-stu-id="783c4-136">In the preceding example, [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) causes the DDE callback function of the MyServer application to receive an [**XTYP\_CONNECT**](xtyp-connect.md) transaction.</span></span>

<span data-ttu-id="783c4-137">在下列範例中，伺服器會使用伺服器支援的主題名稱字串控制碼陣列中的每個專案，來對 [**XTYP \_ CONNECT**](xtyp-connect.md) 交易進行比較，方法是將傳遞給伺服器的 DDEML，與伺服器所支援的主題名稱字串的陣列中的每個元素</span><span class="sxs-lookup"><span data-stu-id="783c4-137">In the following example, the server responds to the [**XTYP\_CONNECT**](xtyp-connect.md) transaction by comparing the topic name string handle the DDEML passed to the server with each element in the array of topic name string handles the server supports.</span></span> <span data-ttu-id="783c4-138">如果伺服器找到相符的，則會建立交談。</span><span class="sxs-lookup"><span data-stu-id="783c4-138">If the server finds a match, it establishes the conversation.</span></span>


```
#define CTOPICS 5 
 
HSZ hsz1;                  // string handle passed by DDEML 
HSZ ahszTopics[CTOPICS];   // array of supported topics 
int i;                     // loop counter 
 
// Use a switch statement to examine transaction types. 
// Here is the connect case.
 
    case XTYP_CONNECT: 
        for (i = 0; i < CTOPICS; i++) 
        { 
            if (hsz1 == ahszTopics[i]) 
                return TRUE;   // establish a conversation 
        } 
 
        return FALSE; // Topic not supported; deny conversation.  
 
// Process other transaction types. 
```



<span data-ttu-id="783c4-139">如果伺服器在回應 [**XTYP \_ connect**](xtyp-connect.md)交易時傳回 **TRUE** ，則 DDEML 會將 [**XTYP \_ CONNECT \_ CONFIRM**](xtyp-connect-confirm.md)交易傳送到伺服器的 DDE 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="783c4-139">If the server returns **TRUE** in response to the [**XTYP\_CONNECT**](xtyp-connect.md) transaction, the DDEML sends an [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server's DDE callback function.</span></span> <span data-ttu-id="783c4-140">伺服器可以藉由處理此交易來取得交談的控制碼。</span><span class="sxs-lookup"><span data-stu-id="783c4-140">The server can obtain the handle to the conversation by processing this transaction.</span></span>

<span data-ttu-id="783c4-141">用戶端可以藉由在呼叫 [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)時指定 **Null** 做為服務名稱字串控制碼、主題名稱字串控制碼或兩者來建立萬用字元交談。</span><span class="sxs-lookup"><span data-stu-id="783c4-141">A client can establish a wildcard conversation by specifying **NULL** for the service name string handle, the topic name string handle, or both in a call to [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect).</span></span> <span data-ttu-id="783c4-142">如果至少有一個字串控制碼為 **Null**，則 DDEML 會將 [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) 交易傳送至所有 DDE 應用程式的回呼函式 (但篩選 **XTYP \_ WILDCONNECT** 交易) 的交易除外。</span><span class="sxs-lookup"><span data-stu-id="783c4-142">If at least one of the string handles is **NULL**, the DDEML sends the [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction to the callback functions of all DDE applications (except those that filter the **XTYP\_WILDCONNECT** transaction).</span></span> <span data-ttu-id="783c4-143">每個伺服器應用程式都應該藉由傳回資料控制碼來回應，該控制碼會識別以 null 結束的 [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) 結構陣列。</span><span class="sxs-lookup"><span data-stu-id="783c4-143">Each server application should respond by returning a data handle that identifies a null-terminated array of [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) structures.</span></span> <span data-ttu-id="783c4-144">如果伺服器應用程式未呼叫 [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) 來註冊其服務名稱，而且篩選是開啟的，則伺服器不會接收 **XTYP \_ WILDCONNECT** 交易。</span><span class="sxs-lookup"><span data-stu-id="783c4-144">If the server application has not called [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) to register its service names and if filtering is on, the server does not receive **XTYP\_WILDCONNECT** transactions.</span></span> <span data-ttu-id="783c4-145">如需資料處理程式的詳細資訊，請參閱 [資料管理](data-management.md)。</span><span class="sxs-lookup"><span data-stu-id="783c4-145">For more information about data handles, see [Data Management](data-management.md).</span></span>

<span data-ttu-id="783c4-146">陣列必須針對符合用戶端所指定之配對的每個服務名稱和主題名稱組，各包含一個結構。</span><span class="sxs-lookup"><span data-stu-id="783c4-146">The array must contain one structure for each service name and topic name pair that matches the pair specified by the client.</span></span> <span data-ttu-id="783c4-147">DDEML 會選取其中一個配對來建立交談，並將識別交談的控制碼傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="783c4-147">The DDEML selects one of the pairs to establish a conversation and returns to the client a handle that identifies the conversation.</span></span> <span data-ttu-id="783c4-148">DDEML 會將 [**XTYP \_ CONNECT \_ 確認**](xtyp-connect-confirm.md) 交易傳送到伺服器 (除非伺服器將此交易篩選) 。</span><span class="sxs-lookup"><span data-stu-id="783c4-148">The DDEML sends the [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server (unless the server filters this transaction).</span></span> <span data-ttu-id="783c4-149">下列範例顯示 [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) 交易的一般伺服器回應。</span><span class="sxs-lookup"><span data-stu-id="783c4-149">The following example shows a typical server response to the [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction.</span></span>


```
#define CTOPICS 2 
 
UINT uType; 
HSZPAIR ahszp[(CTOPICS + 1)]; 
HSZ ahszTopicList[CTOPICS]; 
HSZ hszServ, hszTopic; 
WORD i, j; 
 
if (uType == XTYP_WILDCONNECT) 
{ 
    // Scan the topic list and create an array of HSZPAIR structures. 
 
    j = 0; 
    for (i = 0; i < CTOPICS; i++) 
    { 
        if (hszTopic == (HSZ) NULL || 
                hszTopic == ahszTopicList[i]) 
        { 
            ahszp[j].hszSvc = hszServ; 
            ahszp[j++].hszTopic = ahszTopicList[i]; 
        } 
    } 
 
    // End the list with an HSZPAIR structure that contains NULL 
    // string handles as its members. 
 
    ahszp[j].hszSvc = NULL; 
    ahszp[j++].hszTopic = NULL; 
 
    // Return a handle to a global memory object containing the 
    // HSZPAIR structures. 
 
    return DdeCreateDataHandle( 
        idInst,          // instance identifier 
        (LPBYTE) &ahszp, // pointer to HSZPAIR array 
        sizeof(HSZ) * j, // length of the array 
        0,               // start at the beginning 
        (HSZ) NULL,      // no item name string 
        0,               // return the same format 
        0);              // let the system own it 
} 
```



<span data-ttu-id="783c4-150">用戶端或伺服器可以藉由呼叫 [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) 函數，隨時終止交談。</span><span class="sxs-lookup"><span data-stu-id="783c4-150">Either the client or the server can terminate a conversation at any time by calling the [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) function.</span></span> <span data-ttu-id="783c4-151">此函式會導致交談中夥伴的回呼函數接收 [**XTYP \_ 中斷連接**](xtyp-disconnect.md) 交易 (除非指定 CBF 的夥伴 \_ 略過 \_ 中斷連接篩選旗標) 。</span><span class="sxs-lookup"><span data-stu-id="783c4-151">This function causes the callback function of the partner in the conversation to receive the [**XTYP\_DISCONNECT**](xtyp-disconnect.md) transaction (unless the partner specified the CBF\_SKIP\_DISCONNECTS filter flag).</span></span> <span data-ttu-id="783c4-152">一般而言，應用程式會使用 [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo)函式來取得已終止之交談的相關資訊，以回應 **XTYP \_ 中斷連接** 交易。</span><span class="sxs-lookup"><span data-stu-id="783c4-152">Typically, an application responds to the **XTYP\_DISCONNECT** transaction by using the [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) function to obtain information about the conversation that terminated.</span></span> <span data-ttu-id="783c4-153">在回呼函數從處理 **XTYP \_ 中斷連接** 交易傳回後，交談控制碼已不再有效。</span><span class="sxs-lookup"><span data-stu-id="783c4-153">After the callback function returns from processing the **XTYP\_DISCONNECT** transaction, the conversation handle is no longer valid.</span></span>

<span data-ttu-id="783c4-154">在其 DDE 回呼函式中接收 [**XTYP \_ 中斷連接**](xtyp-disconnect.md) 交易的用戶端應用程式，可以藉由呼叫 [**DdeReconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddereconnect) 函數來嘗試重新建立交談。</span><span class="sxs-lookup"><span data-stu-id="783c4-154">A client application that receives an [**XTYP\_DISCONNECT**](xtyp-disconnect.md) transaction in its DDE callback function can attempt to reestablish the conversation by calling the [**DdeReconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddereconnect) function.</span></span> <span data-ttu-id="783c4-155">用戶端必須從其 DDE 回呼函式內呼叫 **DdeReconnect** 。</span><span class="sxs-lookup"><span data-stu-id="783c4-155">The client must call **DdeReconnect** from within its DDE callback function.</span></span>

## <a name="multiple-conversations"></a><span data-ttu-id="783c4-156">多個交談</span><span class="sxs-lookup"><span data-stu-id="783c4-156">Multiple Conversations</span></span>

<span data-ttu-id="783c4-157">用戶端應用程式可以使用 [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) 函數來判斷是否有任何感興趣的伺服器可在系統中使用。</span><span class="sxs-lookup"><span data-stu-id="783c4-157">A client application can use the [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) function to determine whether any servers of interest are available in the system.</span></span> <span data-ttu-id="783c4-158">用戶端會在呼叫 **DdeConnectList** 時指定服務名稱和主題名稱，使 DDEML 將 [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) 交易廣播到所有符合服務名稱 (的伺服器的 DDE 回呼函式，但是篩選交易) 的伺服器除外。</span><span class="sxs-lookup"><span data-stu-id="783c4-158">A client specifies a service name and topic name when it calls **DdeConnectList**, causing the DDEML to broadcast the [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction to the DDE callback functions of all servers that match the service name (except those that filter the transaction).</span></span> <span data-ttu-id="783c4-159">伺服器的回呼函式應傳回資料控制碼，該控制碼可識別以 null 結束的 [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) 結構陣列。</span><span class="sxs-lookup"><span data-stu-id="783c4-159">A server's callback function should return a data handle that identifies a null-terminated array of [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) structures.</span></span> <span data-ttu-id="783c4-160">陣列應針對符合用戶端所指定之配對的每個服務名稱和主題名稱組，各包含一個結構。</span><span class="sxs-lookup"><span data-stu-id="783c4-160">The array should contain one structure for each service name and topic name pair that matches the pair specified by the client.</span></span> <span data-ttu-id="783c4-161">DDEML 會為伺服器所填滿的每個 **HSZPAIR** 結構建立交談，並將交談清單控制碼傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="783c4-161">The DDEML establishes a conversation for each **HSZPAIR** structure filled by the server and returns a conversation list handle to the client.</span></span> <span data-ttu-id="783c4-162">伺服器會透過 [**XTYP \_ CONNECT**](xtyp-connect.md) 交易 (接收對話控制碼，除非伺服器將此交易篩選) 。</span><span class="sxs-lookup"><span data-stu-id="783c4-162">The server receives the conversation handle by way of the [**XTYP\_CONNECT**](xtyp-connect.md) transaction (unless the server filters this transaction).</span></span>

<span data-ttu-id="783c4-163">用戶端可以在呼叫 [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)時，為服務名稱、主題名稱或兩者指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="783c4-163">A client can specify **NULL** for the service name, topic name, or both when it calls [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span></span> <span data-ttu-id="783c4-164">如果服務名稱是 **Null**，則系統中支援指定之主題名稱的所有伺服器會回應。</span><span class="sxs-lookup"><span data-stu-id="783c4-164">If the service name is **NULL**, all servers in the system that support the specified topic name respond.</span></span> <span data-ttu-id="783c4-165">交談會與每個回應的伺服器建立，包括相同伺服器的多個實例。</span><span class="sxs-lookup"><span data-stu-id="783c4-165">A conversation is established with each responding server, including multiple instances of the same server.</span></span> <span data-ttu-id="783c4-166">如果主題名稱是 **Null**，則會在每個符合服務名稱的伺服器所辨識的每個主題上建立交談。</span><span class="sxs-lookup"><span data-stu-id="783c4-166">If the topic name is **NULL**, a conversation is established on each topic recognized by each server that matches the service name.</span></span>

<span data-ttu-id="783c4-167">用戶端可以使用 [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) 和 [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) 函數來識別回應 [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)的伺服器。</span><span class="sxs-lookup"><span data-stu-id="783c4-167">A client can use the [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) and [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) functions to identify the servers that respond to [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span></span> <span data-ttu-id="783c4-168">**DdeQueryNextServer** 會傳回交談清單中的下一個對話控制碼，而 **DdeQueryConvInfo** 會以對話的相關資訊填滿 [**CONVINFO**](/windows/win32/api/ddeml/ns-ddeml-convinfo) 結構。</span><span class="sxs-lookup"><span data-stu-id="783c4-168">**DdeQueryNextServer** returns the next conversation handle in a conversation list, and **DdeQueryConvInfo** fills a [**CONVINFO**](/windows/win32/api/ddeml/ns-ddeml-convinfo) structure with information about the conversation.</span></span> <span data-ttu-id="783c4-169">用戶端可以保留所需的對話控制碼，並捨棄對話清單中的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="783c4-169">The client can keep the conversation handles that it needs and discard the rest from the conversation list.</span></span>

<span data-ttu-id="783c4-170">下列範例會使用 [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) 來建立與所有支援系統主題之伺服器的交談，然後使用 [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) 和 [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) 函數來取得伺服器的服務名稱字串控制碼，並將其儲存在緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="783c4-170">The following example uses [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) to establish conversations with all servers that support the System topic and then uses the [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) and [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) functions to obtain the servers' service name string handles and store them in a buffer.</span></span>


```
HCONVLIST hconvList; // conversation list 
DWORD idInst;        // instance identifier 
HSZ hszSystem;       // System topic 
HCONV hconv = NULL;  // conversation handle 
CONVINFO ci;         // holds conversation data 
UINT cConv = 0;      // count of conv. handles 
HSZ *pHsz, *aHsz;    // point to string handles 
 
// Connect to all servers that support the System topic. 
 
hconvList = DdeConnectList(idInst, NULL, hszSystem, NULL, NULL); 
 
// Count the number of handles in the conversation list. 
 
while ((hconv = DdeQueryNextServer(hconvList, hconv)) != NULL) 
    cConv++; 
 
// Allocate a buffer for the string handles. 
 
hconv = NULL; 
aHsz = (HSZ *) LocalAlloc(LMEM_FIXED, cConv * sizeof(HSZ)); 
 
// Copy the string handles to the buffer. 
 
pHsz = aHsz; 
while ((hconv = DdeQueryNextServer(hconvList, hconv)) != NULL) 
{ 
    DdeQueryConvInfo(hconv, QID_SYNC, (PCONVINFO) &ci); 
    DdeKeepStringHandle(idInst, ci.hszSvcPartner); 
    *pHsz++ = ci.hszSvcPartner; 
} 
 
// Use the handles; converse with the servers. 
 
// Free the memory and terminate the conversations. 
 
LocalFree((HANDLE) aHsz); 
DdeDisconnectList(hconvList); 
```



<span data-ttu-id="783c4-171">應用程式可以藉由呼叫 [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) 函式來終止交談清單中的個別交談。</span><span class="sxs-lookup"><span data-stu-id="783c4-171">An application can terminate an individual conversation in a conversation list by calling the [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) function.</span></span> <span data-ttu-id="783c4-172">應用程式可以藉由呼叫 [**DdeDisconnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnectlist) 函數，來終止交談清單中的所有交談。</span><span class="sxs-lookup"><span data-stu-id="783c4-172">An application can terminate all conversations in a conversation list by calling the [**DdeDisconnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnectlist) function.</span></span> <span data-ttu-id="783c4-173">這兩個函式都會使 DDEML 將 [**XTYP \_ 中斷連接**](xtyp-disconnect.md) 交易傳送至每個夥伴的 DDE 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="783c4-173">Both functions cause the DDEML to send [**XTYP\_DISCONNECT**](xtyp-disconnect.md) transactions to each partner's DDE callback function.</span></span> <span data-ttu-id="783c4-174">**DdeDisconnectList** 會針對清單中的每個對話控制碼，傳送 **XTYP \_ 中斷連接** 交易。</span><span class="sxs-lookup"><span data-stu-id="783c4-174">**DdeDisconnectList** sends an **XTYP\_DISCONNECT** transaction for each conversation handle in the list.</span></span>

<span data-ttu-id="783c4-175">用戶端可以藉由將現有的交談清單控制碼傳遞給 [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)，來取得交談清單中的交談控制碼清單。</span><span class="sxs-lookup"><span data-stu-id="783c4-175">A client can retrieve a list of the conversation handles in a conversation list by passing an existing conversation list handle to [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span></span> <span data-ttu-id="783c4-176">列舉進程會從清單中移除已終止交談的控制碼，並新增符合指定服務名稱和主題名稱的 nonduplicate 交談。</span><span class="sxs-lookup"><span data-stu-id="783c4-176">The enumeration process removes the handles of terminated conversations from the list, and nonduplicate conversations that fit the specified service name and topic name are added.</span></span>

<span data-ttu-id="783c4-177">如果 [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) 指定現有的交談清單控制碼，此函式會建立新的交談清單，其中包含任何新交談的控制碼，以及現有清單中的控制碼。</span><span class="sxs-lookup"><span data-stu-id="783c4-177">If [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) specifies an existing conversation list handle, the function creates a new conversation list that contains the handles of any new conversations and the handles from the existing list.</span></span>

<span data-ttu-id="783c4-178">如果有重複的交談存在， [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) 會嘗試避免交談清單中重複的對話控制碼。</span><span class="sxs-lookup"><span data-stu-id="783c4-178">If duplicate conversations exist, [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) attempts to prevent duplicate conversation handles in the conversation list.</span></span> <span data-ttu-id="783c4-179">重複的對話是與相同服務名稱和主題名稱上相同伺服器的第二個交談。</span><span class="sxs-lookup"><span data-stu-id="783c4-179">A duplicate conversation is a second conversation with the same server on the same service name and topic name.</span></span> <span data-ttu-id="783c4-180">這兩種交談會有不同的控制碼，但它們會識別相同的交談。</span><span class="sxs-lookup"><span data-stu-id="783c4-180">Two such conversations would have different handles, yet they would identify the same conversation.</span></span>

 

 




