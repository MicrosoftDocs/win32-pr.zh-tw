---
title: 對話管理
description: 本主題討論用戶端與伺服器之間的交談。
ms.assetid: 4e5ff1a1-d46a-4e2a-a37c-8df951f2a1ee
keywords:
- 'Windows消費者介面，動態資料交換 (DDE) '
- 動態資料交換 (DDE) 、交談
- DDE (動態資料交換) 、交談
- '資料交換、動態資料交換 (DDE) '
- 'Windows消費者介面，動態資料交換管理程式庫 (DDEML) '
- 動態資料交換管理程式庫 (DDEML) 、交談
- DDEML (動態資料交換管理程式庫) ，交談
- '資料交換、動態資料交換管理程式庫 (DDEML) '
- 動態資料交換 (DDE) 、多重對話
- DDE (動態資料交換) 、多重對話
- 動態資料交換管理程式庫 (DDEML) 、多重對話
- DDEML (動態資料交換管理程式庫) 、多重對話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3531cc396a3b4d0eca5d7c11e3677aec9ea2ee35dcdac110455daee252f798
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991328"
---
# <a name="conversation-management"></a>對話管理

用戶端與伺服器之間的對話一律會在用戶端要求時建立。 當交談建立時，每個夥伴都會收到識別交談的控制碼。 合作夥伴會在其他動態資料交換管理程式庫中使用此控制碼 (DDEML) 函式來傳送交易及管理交談。 用戶端可以要求與單一伺服器的對話，也可以要求與一或多部伺服器的多個交談。

下列主題描述應用程式如何建立新的交談，並取得現有交談的相關資訊。

-   [單一對話](#single-conversations)
-   [多個交談](#multiple-conversations)

## <a name="single-conversations"></a>單一對話

用戶端應用程式會藉由呼叫 [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) 函式並指定字串控制碼來識別包含伺服器應用程式服務名稱的字串，以及交談的主題名稱，要求與伺服器的單一交談。 DDEML 會將 [**XTYP \_ CONNECT**](xtyp-connect.md)交易傳送至每個伺服器應用程式的動態資料交換 (DDE) 回呼函式，該函式已註冊符合 **DdeConnect** 中指定的服務名稱，或藉由呼叫 [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)來關閉服務名稱篩選功能。 伺服器也可以藉由 **在 \_** \_ \_ [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) 函數中指定 CBF FAIL CONNECTIONS 篩選旗標，來篩選 XTYP CONNECT 交易。 在 **XTYP \_ CONNECT** 交易期間，DDEML 會將服務名稱和主題名稱傳遞至伺服器。 伺服器必須檢查名稱，如果它支援服務名稱和主題名稱組，則傳回 **TRUE** ，否則傳回 **FALSE** 。

如果沒有伺服器回應用戶端的連線要求，用戶端會從 [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)接收 **Null** ，且不會建立任何交談。 如果伺服器傳回 **TRUE**，就會建立交談，且用戶端會收到交談控制碼，此為識別交談的 **DWORD** 值。 用戶端會使用後續 DDEML 呼叫中的控制碼，從伺服器取得資料。 伺服器會接收 [**XTYP \_ CONNECT \_ CONFIRM**](xtyp-connect-confirm.md) 交易 (除非伺服器指定 CBF \_ SKIP \_ connect \_ 確認篩選旗標) 。 此交易會將交談控制碼傳遞至伺服器。

下列範例會要求系統主題上的交談，以及可辨識服務名稱 MyServer 的伺服器。 *HszServName* 和 *hszSysTopic* 參數是先前建立的字串控制碼。


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



在上述範例中， [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) 會讓 MyServer 應用程式的 DDE 回呼函式收到 [**XTYP \_ CONNECT**](xtyp-connect.md) 交易。

在下列範例中，伺服器會使用伺服器支援的主題名稱字串控制碼陣列中的每個專案，來對 [**XTYP \_ CONNECT**](xtyp-connect.md) 交易進行比較，方法是將傳遞給伺服器的 DDEML，與伺服器所支援的主題名稱字串的陣列中的每個元素 如果伺服器找到相符的，則會建立交談。


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



如果伺服器在回應 [**XTYP \_ connect**](xtyp-connect.md)交易時傳回 **TRUE** ，則 DDEML 會將 [**XTYP \_ CONNECT \_ CONFIRM**](xtyp-connect-confirm.md)交易傳送到伺服器的 DDE 回呼函數。 伺服器可以藉由處理此交易來取得交談的控制碼。

用戶端可以藉由在呼叫 [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)時指定 **Null** 做為服務名稱字串控制碼、主題名稱字串控制碼或兩者來建立萬用字元交談。 如果至少有一個字串控制碼為 **Null**，則 DDEML 會將 [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) 交易傳送至所有 DDE 應用程式的回呼函式 (但篩選 **XTYP \_ WILDCONNECT** 交易) 的交易除外。 每個伺服器應用程式都應該藉由傳回資料控制碼來回應，該控制碼會識別以 null 結束的 [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) 結構陣列。 如果伺服器應用程式未呼叫 [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) 來註冊其服務名稱，而且篩選是開啟的，則伺服器不會接收 **XTYP \_ WILDCONNECT** 交易。 如需資料處理程式的詳細資訊，請參閱 [資料管理](data-management.md)。

陣列必須針對符合用戶端所指定之配對的每個服務名稱和主題名稱組，各包含一個結構。 DDEML 會選取其中一個配對來建立交談，並將識別交談的控制碼傳回給用戶端。 DDEML 會將 [**XTYP \_ CONNECT \_ 確認**](xtyp-connect-confirm.md) 交易傳送到伺服器 (除非伺服器將此交易篩選) 。 下列範例顯示 [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) 交易的一般伺服器回應。


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



用戶端或伺服器可以藉由呼叫 [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) 函數，隨時終止交談。 此函式會導致交談中夥伴的回呼函數接收 [**XTYP \_ 中斷連接**](xtyp-disconnect.md) 交易 (除非指定 CBF 的夥伴 \_ 略過 \_ 中斷連接篩選旗標) 。 一般而言，應用程式會使用 [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo)函式來取得已終止之交談的相關資訊，以回應 **XTYP \_ 中斷連接** 交易。 在回呼函數從處理 **XTYP \_ 中斷連接** 交易傳回後，交談控制碼已不再有效。

在其 DDE 回呼函式中接收 [**XTYP \_ 中斷連接**](xtyp-disconnect.md) 交易的用戶端應用程式，可以藉由呼叫 [**DdeReconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddereconnect) 函數來嘗試重新建立交談。 用戶端必須從其 DDE 回呼函式內呼叫 **DdeReconnect** 。

## <a name="multiple-conversations"></a>多個交談

用戶端應用程式可以使用 [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) 函數來判斷是否有任何感興趣的伺服器可在系統中使用。 用戶端會在呼叫 **DdeConnectList** 時指定服務名稱和主題名稱，使 DDEML 將 [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) 交易廣播到所有符合服務名稱 (的伺服器的 DDE 回呼函式，但是篩選交易) 的伺服器除外。 伺服器的回呼函式應傳回資料控制碼，該控制碼可識別以 null 結束的 [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) 結構陣列。 陣列應針對符合用戶端所指定之配對的每個服務名稱和主題名稱組，各包含一個結構。 DDEML 會為伺服器所填滿的每個 **HSZPAIR** 結構建立交談，並將交談清單控制碼傳回給用戶端。 伺服器會透過 [**XTYP \_ CONNECT**](xtyp-connect.md) 交易 (接收對話控制碼，除非伺服器將此交易篩選) 。

用戶端可以在呼叫 [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)時，為服務名稱、主題名稱或兩者指定 **Null** 。 如果服務名稱是 **Null**，則系統中支援指定之主題名稱的所有伺服器會回應。 交談會與每個回應的伺服器建立，包括相同伺服器的多個實例。 如果主題名稱是 **Null**，則會在每個符合服務名稱的伺服器所辨識的每個主題上建立交談。

用戶端可以使用 [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) 和 [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) 函數來識別回應 [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)的伺服器。 **DdeQueryNextServer** 會傳回交談清單中的下一個對話控制碼，而 **DdeQueryConvInfo** 會以對話的相關資訊填滿 [**CONVINFO**](/windows/win32/api/ddeml/ns-ddeml-convinfo) 結構。 用戶端可以保留所需的對話控制碼，並捨棄對話清單中的其餘部分。

下列範例會使用 [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) 來建立與所有支援系統主題之伺服器的交談，然後使用 [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) 和 [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) 函數來取得伺服器的服務名稱字串控制碼，並將其儲存在緩衝區中。


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



應用程式可以藉由呼叫 [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) 函式來終止交談清單中的個別交談。 應用程式可以藉由呼叫 [**DdeDisconnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnectlist) 函數，來終止交談清單中的所有交談。 這兩個函式都會使 DDEML 將 [**XTYP \_ 中斷連接**](xtyp-disconnect.md) 交易傳送至每個夥伴的 DDE 回呼函數。 **DdeDisconnectList** 會針對清單中的每個對話控制碼，傳送 **XTYP \_ 中斷連接** 交易。

用戶端可以藉由將現有的交談清單控制碼傳遞給 [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)，來取得交談清單中的交談控制碼清單。 列舉進程會從清單中移除已終止交談的控制碼，並新增符合指定服務名稱和主題名稱的 nonduplicate 交談。

如果 [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) 指定現有的交談清單控制碼，此函式會建立新的交談清單，其中包含任何新交談的控制碼，以及現有清單中的控制碼。

如果有重複的交談存在， [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) 會嘗試避免交談清單中重複的對話控制碼。 重複的對話是與相同服務名稱和主題名稱上相同伺服器的第二個交談。 這兩種交談會有不同的控制碼，但它們會識別相同的交談。

 

 




