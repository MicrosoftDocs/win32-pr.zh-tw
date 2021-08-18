---
title: 基本概念
description: 本主題討論有關動態資料交換的重要概念。
ms.assetid: 37826d83-4dcd-484f-b1aa-87bf309c5c09
keywords:
- 'Windows消費者介面，動態資料交換 (DDE) '
- 'Windows消費者介面，動態資料交換管理程式庫 (DDEML) '
- 動態資料交換 (DDE) 、用戶端伺服器互動
- DDE (動態資料交換) 、用戶端伺服器互動
- '資料交換、動態資料交換 (DDE) '
- '資料交換、動態資料交換管理程式庫 (DDEML) '
- 動態資料交換 (DDE) 、用戶端應用程式
- DDE (動態資料交換) ，用戶端應用程式
- 動態資料交換 (的 DDE) 、伺服器應用程式
- DDE (動態資料交換) 、伺服器應用程式
- 動態資料交換 (DDE) 、回呼函式
- DDE (動態資料交換) ，回呼函式
- 動態資料交換 (DDE) ，交易
- DDE (動態資料交換) ，交易
- 動態資料交換 (的 DDE) ，服務名稱
- DDE (動態資料交換) ，服務名稱
- 動態資料交換 (的 DDE) ，專案名稱
- DDE (動態資料交換) ，專案名稱
- 動態資料交換 (的 DDE) ，主題名稱
- DDE (動態資料交換) ，主題名稱
- 動態資料交換 (DDE) ，系統主題
- DDE (動態資料交換) ，系統主題
- 動態資料交換管理程式庫 (DDEML) 、初始化
- DDEML (動態資料交換管理程式庫) ，初始化
- 動態資料交換管理程式庫 (DDEML) 、回呼函數
- DDEML (動態資料交換管理程式庫) ，回呼函數
- 動態資料交換管理程式庫 (DDEML) 、字串管理
- DDEML (動態資料交換管理程式庫) ，字串管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fae271c359afd571cf6c51fb3387a15f1496416e5eb54b055ef518fd213f30fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128620"
---
# <a name="basic-concepts-dde"></a> (DDE) 的基本概念

這些概念是瞭解動態資料交換 (DDE) 以及動態資料交換管理程式庫 (DDEML) 的關鍵。

-   [用戶端與伺服器互動](#client-and-server-interaction)
-   [交易和 DDE 回呼函數](#transactions-and-the-dde-callback-function)
-   [服務名稱、主題名稱和專案名稱](#service-names-topic-names-and-item-names)
-   [系統主題](#system-topic)
-   [初始 化](#initialization)
-   [回呼函數](#callback-function)
-   [字串管理](#string-management)
-   [DDEML 和執行緒](#ddeml-and-threads)

## <a name="client-and-server-interaction"></a>用戶端與伺服器互動

在用戶端應用程式和伺服器應用程式之間一律會發生 DDE。 *DDE 用戶端應用程式* 會建立與伺服器的交談，以將交易傳送到伺服器，藉此起始交換。 交易是資料或服務的要求。 *DDE 伺服器應用程式* 會藉由提供資料或服務給用戶端來回應交易。 例如，圖形應用程式可能包含代表公司每季收益的橫條圖，但橫條圖的資料可能包含在試算表應用程式中。 為了取得最新的收益圖， (用戶端的圖形應用程式) 可以與 (伺服器) 的試算表應用程式建立交談。 然後，圖形應用程式可以將交易傳送到試算表應用程式，要求最新的收益圖。

伺服器可以同時有許多用戶端，而用戶端可以從多部伺服器要求資料。 應用程式也可以是用戶端和伺服器。 用戶端或伺服器隨時都可以終止交談。

## <a name="transactions-and-the-dde-callback-function"></a>交易和 DDE 回呼函數

DDEML 會將交易傳送至應用程式的 DDE 回呼函式，以通知應用程式有關的 DDE 活動。 *DDE 交易* 類似于訊息，它是名為的常數，以及其他包含交易其他資訊的參數。

DDEML 會將交易傳遞至應用程式定義的 DDE 回呼函式，此函式會執行適合交易類型的動作。 例如，當用戶端應用程式嘗試建立與伺服器應用程式的對話時，用戶端會呼叫 [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) 函數。 這個函式會讓 DDEML 將 [**XTYP \_ CONNECT**](xtyp-connect.md) 交易傳送到伺服器的 DDE 回呼函數。 回呼函式可以藉由傳回 **TRUE** 給 DDEML 來允許交談，或藉由傳回 **FALSE** 來拒絕交談。 如需交易的詳細討論，請參閱 [交易管理](transaction-management.md)。

## <a name="service-names-topic-names-and-item-names"></a>服務名稱、主題名稱和專案名稱

DDE 伺服器在先前的 DDE 檔中使用三層階層服務名稱 (稱為「應用程式名稱」) 、主題名稱和專案名稱，以唯一識別伺服器在交談期間可以交換的資料單位。

*服務名稱* 是當用戶端嘗試與伺服器建立交談時，伺服器應用程式所回應的字串。 用戶端必須指定此服務名稱，才能與伺服器建立交談。 雖然伺服器可以回應許多服務名稱，但大部分的伺服器只會回應一個名稱。

*主題名稱* 是識別邏輯資料內容的字串。 對於在以檔案為基礎的檔上操作的伺服器，主題名稱通常是檔案名;其他伺服器則是其他應用程式特定的字串。 用戶端必須在嘗試建立與伺服器的對話時，指定主題名稱以及伺服器的服務名稱。

*專案名稱* 是一個字串，可識別伺服器在交易期間可以傳遞給用戶端的資料單位。 例如，專案名稱可能會識別整數、字串、數個文欄位落或點陣圖。

服務、主題和專案名稱可讓用戶端與伺服器建立交談，以及接收來自伺服器的資料。

## <a name="system-topic"></a>系統主題

系統主題提供任何 DDE 用戶端的一般感興趣資訊的內容。 建議伺服器應用程式隨時都支援系統主題。 系統主題定義于 DDEML 中。H 標頭檔作為 SZDDESYS \_ 主題。

若要判斷有哪些伺服器存在以及它們可以提供的資訊類型，用戶端應用程式可以在啟動時要求系統主題的交談，將裝置名稱設定為 **Null**。 這類萬用字元交談在系統效能方面相當昂貴，因此應該保持最小值。 如需有關起始 DDE 交談的詳細資訊，請參閱 [對話管理](conversation-management.md)。

伺服器必須支援系統主題內的下列專案名稱，以及對用戶端有用的任何其他專案名稱。



| 項目                     | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SZDDE \_ 專案 \_ ITEMLIST    | 非系統主題下支援的專案清單。  (這份清單會隨著時間和主題的不同而有所不同。 )                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| SZDDESYS \_ 專案 \_ 格式  | 以定位字元分隔的字串清單，表示服務應用程式可能支援的所有剪貼簿格式。 代表預先定義剪貼簿格式的字串相當於 \_ 已移除 "CF" 前置詞的 C光圈值 \_ 。 例如，CF \_ 文字格式是以字串 "text" 表示。 這些字串必須是大寫，才能進一步將其識別為預先定義的格式。 格式清單必須以最豐富的內容順序出現在內容中，而不是最豐富的內容。 如需剪貼簿格式和轉譯資料的詳細資訊，請參閱 [剪貼](clipboard.md)簿。<br/> |
| SZDDESYS \_ 專案 \_ 說明     | 一般感興趣的使用者可讀取資訊。 此專案至少必須包含有關如何使用伺服器應用程式之 DDE 功能的資訊。 這項資訊可包括（但不限於）如何指定主題中的專案、伺服器可執行檔執行字串、允許的內容，以及如何在其他系統主題專案中尋找說明。                                                                                                                                                                                                                           |
| SZDDESYS \_ 專案 \_ RTNMSG   | 最近使用之 [**WM \_ DDE \_ ACK**](wm-dde-ack.md) 訊息的支援詳細資料。 當需要超過8個位的應用程式特定傳回資料時，此專案很有用。                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SZDDESYS \_ 專案 \_ 狀態   | 指出伺服器目前狀態的指示。 一般來說，這個專案僅支援 CF \_ 文字格式，並且包含就緒或忙碌的字串。                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SZDDESYS \_ 專案 \_ SYSITEMS | 此伺服器在系統主題下支援的專案清單。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SZDDESYS \_ 專案 \_ 主題   | 伺服器在目前時間所支援的主題清單。  (這份清單可能會有不同的時間。 )                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

這些專案名稱是在 DDEML 中定義的值。H 標頭檔。 若要取得這些字串的字串控制碼，應用程式必須使用 DDEML 字串管理函式，就像在 DDEML 應用程式中的任何其他字串一樣。 如需管理字串的詳細資訊，請參閱 [字串管理](#string-management)。

## <a name="initialization"></a>初始化

在呼叫任何其他 DDEML 函式之前，應用程式必須呼叫 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) 函數。 **DdeInitialize** 會取得應用程式的實例識別碼、使用 dde 來註冊應用程式的 dde 回呼函式，並指定回呼函數的交易篩選旗標。

應用程式或 DLL 的每個實例都必須將其實例識別碼作為 *idInst* 參數傳遞給任何其他需要它的 DDEML 函數。 多個 DDEML 實例的目的是要支援在應用程式使用 DDEML 時，必須同時使用該的 Dll。 應用程式不能使用一個以上的 DDEML 實例。

*交易篩選* 會防止 DDEML 將不需要的交易傳遞到應用程式的 DDE 回呼函式，以優化系統效能。 應用程式會在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) *ufCmd* 參數中設定交易篩選。 應用程式必須為每一種交易類型指定交易篩選旗標，但它不會在其回呼函數中處理。 應用程式可以使用 **DdeInitialize** 的後續呼叫來變更其交易篩選。 如需交易的詳細資訊，請參閱 [交易管理](transaction-management.md)。

下列範例示範如何初始化應用程式以使用 DDEML。


```
DWORD idInst = 0; 
HINSTANCE hinst; 
 
DdeInitialize(&idInst,         // receives instance identifier 
    (PFNCALLBACK) DdeCallback, // pointer to callback function 
    CBF_FAIL_EXECUTES |        // filter XTYPE_EXECUTE 
    CBF_SKIP_ALLNOTIFICATIONS, // filter notifications 
    0); 
```



當應用程式不再使用 DDEML 時，必須呼叫 [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) 函數。 此函式會終止應用程式目前開啟的所有交談，並釋出系統組態給應用程式的 DDEML 資源。

## <a name="callback-function"></a>回呼函式

使用 DDEML 的應用程式必須提供回呼函式，以處理影響應用程式的 DDE 事件。 DDEML 會將交易傳送至應用程式的 DDE 回呼函式，以通知應用這類事件。 回呼函數接收的交易取決於 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) 中指定的應用程式，以及應用程式是用戶端、伺服器或兩者。 如需詳細資訊，請參閱 [**DdeCallback**](/windows/win32/api/ddeml/nc-ddeml-pfncallback)。

下列範例顯示一般用戶端應用程式的回呼函式的一般結構。


```
HDDEDATA CALLBACK DdeCallback(uType, uFmt, hconv, hsz1, 
    hsz2, hdata, dwData1, dwData2) 
UINT uType;       // transaction type 
UINT uFmt;        // clipboard data format 
HCONV hconv;      // handle to conversation 
HSZ hsz1;         // handle to string 
HSZ hsz2;         // handle to string 
HDDEDATA hdata;   // handle to global memory object 
DWORD dwData1;    // transaction-specific data 
DWORD dwData2;    // transaction-specific data 
{ 
    switch (uType) 
    { 
        case XTYP_REGISTER: 
        case XTYP_UNREGISTER: 
            . 
            . 
            . 
            return (HDDEDATA) NULL; 
 
        case XTYP_ADVDATA: 
            . 
            . 
            . 
            return (HDDEDATA) DDE_FACK; 
 
        case XTYP_XACT_COMPLETE: 
            
            // 
            
            return (HDDEDATA) NULL; 
 
        case XTYP_DISCONNECT: 
            
            // 
            
            return (HDDEDATA) NULL; 
 
        default: 
            return (HDDEDATA) NULL; 
    } 
} 
```



*UType* 參數會指定 DDEML 傳送給回呼函數的交易類型。 其餘參數的值取決於交易類型。 下列主題將說明產生它們的交易類型和事件。 如需每種交易類型的詳細資訊，請參閱 [交易管理](transaction-management.md)。

## <a name="string-management"></a>字串管理

為了執行 DDE 工作，許多 DDEML 函式都需要存取字串。 例如，當用戶端呼叫 [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) 函數來要求與伺服器的對話時，用戶端必須指定服務名稱和主題名稱。 應用程式會藉由傳遞字串控制碼 (HSZ) （而不是 DDEML 函式中的指標）來指定字串。 *字串控制碼* 是系統指派的 **DWORD** 值，可識別字串。

應用程式可以藉由呼叫 [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) 函數，取得特定字串的字串控制碼。 此函式會向系統註冊字串，並將字串控制碼傳回給應用程式。 應用程式可以將控制碼傳遞給必須存取字串的 DDEML 函數。 下列範例會取得系統主題字串和服務名稱字串的字串控制碼。


```
HSZ hszServName; 
HSZ hszSysTopic; 
hszServName = DdeCreateStringHandle( 
    idInst,         // instance identifier 
    "MyServer",     // string to register 
    CP_WINANSI);    // Windows ANSI code page 
 
hszSysTopic = DdeCreateStringHandle( 
    idInst,         // instance identifier 
    SZDDESYS_TOPIC, // System topic 
    CP_WINANSI);    // Windows ANSI code page 
    
```



上述範例中的 *idInst* 參數會指定 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) 函數所取得的實例識別碼。

應用程式的 DDE 回呼函數會在大部分的 DDE 交易期間收到一或多個字串控制碼。 例如，伺服器會在 [**XTYP \_ 要求**](xtyp-request.md) 交易期間收到兩個字串控制碼：一個會識別指定主題名稱的字串，另一個則會識別指定專案名稱的字串。 應用程式可以藉由呼叫 [**DdeQueryString**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) 函式來取得對應于字串控制碼的字串長度，並將字串複製到應用程式定義的緩衝區，如下列範例所示。


```
DWORD idInst; 
DWORD cb; 
HSZ hszServ; 
PSTR pszServName; 
cb = DdeQueryString(idInst, hszServ, (LPSTR) NULL, 0, 
    CP_WINANSI) + 1; 
pszServName = (PSTR) LocalAlloc(LPTR, (UINT) cb); 
DdeQueryString(idInst, hszServ, pszServName, cb, CP_WINANSI); 
```



實例特定的字串控制碼無法從字串控制碼對應到字串，也不能對應回字串控制碼。 例如，雖然 [**DdeQueryString**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) 會從字串控制碼建立字串，然後 [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) 從該字串建立字串控制碼，但兩個控制碼並不相同，如下列範例所示。


```
DWORD idInst; 
DWORD cb; 
HSZ hszInst, hszNew; 
PSZ pszInst; 
DdeQueryString(idInst, hszInst, pszInst, cb, CP_WINANSI); 
hszNew = DdeCreateStringHandle(idInst, pszInst, CP_WINANSI); 
// hszNew != hszInst ! 
```



若要比較兩個字串控制碼的值，請使用 [**DdeCmpStringHandles**](/windows/desktop/api/Ddeml/nf-ddeml-ddecmpstringhandles) 函數。

當回呼函式傳回時，傳遞給應用程式之 DDE 回呼函數的字串控制碼會變成無效。 應用程式可以使用 [**DdeKeepStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle) 函式來儲存回呼函數傳回後使用的字串控制碼。

當應用程式呼叫 [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea)時，系統會將指定的字串輸入字串資料表中，並產生用來存取字串的控制碼。 系統也會維護字串資料表中每個字串的使用計數。

當應用程式呼叫 [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) 並指定已經存在於資料表中的字串時，系統會遞增使用量計數，而不是加入另一次出現的字串。  (應用程式也可以使用 [**DdeKeepStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle)來遞增使用量計數。 ) 當應用程式呼叫 [**DdeFreeStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreestringhandle) 函式時，系統會遞減使用計數。

當字串的使用計數等於零時，就會從資料表中移除字串。 由於有一個以上的應用程式可以取得特定字串的控制碼，因此應用程式不能將字串控制碼釋出超過其建立或保留控制碼的次數。 否則，應用程式可能會從資料表中移除字串，而拒絕其他應用程式存取字串。

DDEML 字串管理函式是以 atom 管理員為基礎，且受限於與原子相同的大小限制。

## <a name="ddeml-and-threads"></a>DDEML 和執行緒

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函式會向 DDEML 註冊應用程式，並建立 DDEML 實例。 DDEML 實例是以執行緒為基礎，與呼叫 **DdeInitialize** 的執行緒相關聯。

屬於 DDEML 實例之物件的所有 DDEML 函式呼叫，都必須從呼叫 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) 的相同執行緒建立實例。 如果您從不同的執行緒呼叫 DDEML 函式，此函式將會失敗。 您無法從配置交談以外的執行緒存取 DDEML 交談。

 

