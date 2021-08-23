---
title: 尋找伺服器主機系統
description: 藉由使用字串系結和查詢名稱服務資料庫來尋找伺服器程式的位置，來尋找伺服器主機系統。
ms.assetid: 4aadda88-2109-481f-aa4b-b1983d81dec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 180e2e43c0350f55defb74762d6ab1b6b656dafbc1468bcc7f077ed9780a2e98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929987"
---
# <a name="finding-server-host-systems"></a>尋找伺服器主機系統

伺服器主機系統是執行分散式應用程式之伺服器程式的電腦。 網路上可能有一或多個伺服器主機系統。 用戶端程式如何尋找要連接的伺服器，取決於您的程式需求。

有兩種方法可以尋找伺服器主機系統：

-   使用儲存在用戶端原始程式碼、環境變數或應用程式特定設定檔中字串的資訊。 您的用戶端應用程式可以使用字串中的資料來撰寫用戶端與伺服器之間的系結。
-   查詢名稱服務資料庫是否有伺服器程式的位置。

本節提供下列主題中這兩種技術的相關資訊：

-   [使用字串系結](#using-string-bindings)
-   [從名稱服務資料庫匯入](#importing-from-name-service-databases)

## <a name="using-string-bindings"></a>使用字串系結

應用程式可以從儲存在字串中的資訊建立系結。 您的用戶端應用程式會將此資訊撰寫為字串，然後呼叫 [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) 函數。 用戶端必須提供下列資訊來識別伺服器：

-   介面名稱、物件的全域唯一識別碼 (GUID) 或物件的 UUID。 如需詳細資訊，請參閱 [產生介面 uuid](generating-interface-uuids.md) 和 [字串 UUID](string-uuid.md)。
-   要進行通訊的傳輸類型，例如具名管道或 TCP/IP。 如需詳細資訊，請參閱 [基本的 RPC](essential-rpc-binding-terminology.md) 系結術語和 [選取通訊協定順序](selecting-a-protocol-sequence.md)。
-   伺服器主機電腦的網路位址或名稱。
-   伺服器主機電腦上伺服器程式的端點。 如需詳細資訊，請參閱 [尋找端點](finding-endpoints.md)和 [指定端點](specifying-endpoints.md)。

 (物件 UUID 和端點資訊是選擇性的。 ) 

在下列範例中， *pszNetworkAddress* 參數和其他參數包含內嵌的反斜線。 反斜線是 C 程式設計語言中的一個 escape 字元。 需要兩個反斜線來代表每個單一常值反斜線字元。 字串系結結構必須包含四個反斜線字元，以代表伺服器名稱前面的兩個常值反斜線字元。

下列範例顯示伺服器名稱前面必須有八個反斜線，如此一來，在 **sprintf \_** 的函式處理字串之後，字串系結資料結構中就會出現四個常值反斜線字元。


```C++
/* client application */

char * pszUuid = "6B29FC40-CA47-1067-B31D-00DD010662DA";
char * pszProtocol = "ncacn_np";
char * pszNetworkAddress = "\\\\\\\\servername";
char * pszEndpoint = "\\\\pipe\\\\pipename";
char * pszString;
 
int len = 0;
 
len  = sprintf_s(pszString, strlen(pszUuid), "%s", pszUuid);
len += sprintf_s(pszString + len, strlen(pszProtocolSequence) + 2, "@%s:",
    pszProtocolSequence);
if (pszNetworkAddress != NULL)
    len += sprintf_s(pszString + len, strlen(pszNetworkAddress), "%s",
    pszNetworkAddress);
len += sprintf_s(pszString + len, strlen(pszEndpoint) + 2, "[%s]", pszEndpoint);
```



在下列範例中，字串系結會顯示為：

6B29FC40-CA47-1067-B31D-00DD010662DA@ncacn\_np： \\ \\ \\ \\ *servername* \[ \\ \\ 管道 \\ \\ *pipename*\]

然後，用戶端會呼叫 [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) 以取得系結控制碼：


```C++
RPC_BINDING_HANDLE hBinding;
 
status = RpcBindingFromStringBinding(pszString, &hBinding);
//...
```



方便的函式 [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) 會以正確的語法，將物件 UUID、通訊協定順序、網路位址和端點組合成 [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)的呼叫。 您不必擔心如何在正確的位置放置每個通訊協定順序的連字號、冒號和各種元件;您只需提供字串做為函式的參數。 執行時間程式庫甚至會配置字串系結所需的記憶體。


```C++
char * pszNetworkAddress = "\\\\server";
char * pszEndpoint = "\\pipe\\pipename";
status = RpcStringBindingCompose(
            pszUuid,
            pszProtocolSequence,
            pszNetworkAddress,
            pszEndpoint,
            pszOptions,
            &pszString);
//...
status = RpcBindingFromStringBinding(
            pszString,
            &hBinding);
//...
```



另一個方便的函式 [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)會採用系結控制碼做為輸入，並產生對應的字串系結。

## <a name="importing-from-name-service-databases"></a>從名稱服務資料庫匯入

命名服務資料庫儲存區，以及其他專案、系結控制碼和 Uuid。 您的用戶端應用程式可以在需要系結至伺服器時，搜尋其中一個或兩個。 如需名稱服務儲存的資訊以及儲存格式的討論，請參閱 [RPC 名稱服務資料庫](the-rpc-name-service-database.md)。

RPC 程式庫提供兩組功能，讓您的用戶端程式可用來搜尋名稱服務資料庫。 其中一個集合的名稱開頭為 RpcNsBindingImport。 另一個集合的名稱開頭為 RpcNsBindingLookup。 這兩個函數群組之間的差異在於 RpcNsBindingImport 函式會傳回每個呼叫的單一系結控制碼，而 RpcNsBindingLookup 函式會傳回每個呼叫的控制碼群組。

若要開始使用 RpcNsBindingImport 函數進行搜尋，請先呼叫 [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)，如下列程式碼片段所示。


```C++
RPC_STATUS status;
RPC_NS_HANDLE hNameServiceHandle;
 
status = RpcNsBindingImportBegin(
    RPC_C_NS_SYNTAX_DEFAULT,
    NULL,
    MyInterface_v1_0_c_ifspec,
    NULL,
    &hNameServiceHandle);
```



當 RPC 函數搜尋名稱服務資料庫時，他們需要一個位置來開始搜尋。 在 RPC 詞彙中，這稱為專案名稱。 用戶端程式會將專案名稱做為第二個參數傳遞至 [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)。 如果您想要搜尋整個名稱服務資料庫，這個參數可以是 **Null** 。 或者，您可以傳遞伺服器專案名稱，或藉由傳遞群組專案名稱來搜尋群組專案，以搜尋伺服器專案。 傳遞專案名稱會將搜尋限制為該專案的內容。

在上述範例中，RPC \_ C \_ NS \_ 語法預設值 \_ 會以第一個參數的形式傳遞至 [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)。 這會選取預設的專案名稱語法。 目前，這是唯一支援的專案名稱語法。

您的用戶端應用程式可以搜尋名稱服務資料庫中的介面名稱、UUID 或兩者。 如果您想要讓它依名稱搜尋介面，請傳遞 MIDL 編譯器從 IDL 檔案產生的全域介面變數，做為 [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)的第三個參數。 您會在 MIDL 編譯器產生用戶端 stub 時產生的標頭檔中，找到其宣告。 如果您想要讓用戶端程式依 UUID 搜尋，請將第三個參數設定為 **Null**。

針對 UUID 搜尋名稱服務資料庫時，請將 [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) 的第四個參數設定為您想要搜尋的 uuid。 如果您未搜尋 UUID，請將此參數設定為 **Null**。

[**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)函式會透過其第五個參數傳遞名稱服務的位址–搜尋內容控制碼。 您會將此參數傳遞給其他 RpcNsBindingImport 函數。

尤其是，您用戶端應用程式會呼叫的下一個函式是 [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)。 用戶端程式會使用此函式，從名稱服務資料庫中取出相容的系結控制碼。 下列程式碼片段會示範如何呼叫此函數：


```C++
RPC_STATUS status;
RPC_BINDING_HANDLE hBindingHandle;
// The variable hNameServiceHandle is a valid name service search 
// context handle obtained from the RpcNsBindingBegin function.
 
status = RpcNsBindingImportNext(hNameServiceHandle, &hBindingHandle);
```



一旦呼叫 [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) 函式來取得系結控制碼之後，您的用戶端應用程式就可以判斷它所收到的控制碼是否可接受。 如果沒有，您的用戶端程式可以執行迴圈，並再次呼叫 **RpcNsBindingImportNext** ，以查看名稱服務是否包含更適當的控制碼。 對於 **RpcNsBindingImportNext** 的每個呼叫，都必須有對應的 RpcNsBindingFree 呼叫。 當您的搜尋完成時，請呼叫 [**RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone) 函式來釋放查閱內容。

當您的用戶端應用程式具有可接受的系結控制碼之後，它應該檢查以確定伺服器應用程式正在執行。 用戶端可以使用兩種方法來執行此驗證。 第一個是在用戶端介面中呼叫函數。 如果伺服器程式正在執行，則會完成呼叫。 如果沒有，則呼叫會失敗。 若要確認伺服器是否正在執行，更好的方法是叫用 [**RpcEpResolveBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding)，然後呼叫 [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening)。 如需名稱服務資料庫的詳細資訊，請參閱 [RPC 名稱服務資料庫](the-rpc-name-service-database.md)。

 

 




