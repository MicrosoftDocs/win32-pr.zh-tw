---
title: 使用內容控制碼進行介面開發
description: 一般而言，您會在 \_ IDL 檔案中的類型定義上指定 \ 內容控制碼 \ 屬性，以建立內容控制碼。
ms.assetid: e4caf91f-f92d-4aef-a20f-0a3073230640
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77e65e36384bda3d81526d5891eca92a77a67402e7cd3aa7af8b61e061a9d3b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020468"
---
# <a name="interface-development-using-context-handles"></a>使用內容控制碼進行介面開發

一般而言，您會在 \[ IDL 檔案中的類型定義上指定 [**內容 \_ 控制碼**](/windows/desktop/Midl/context-handle)屬性，藉以建立內容控制碼 \] 。 型別定義也會隱含地指定必須提供的內容執行常式。 如果用戶端與伺服器之間的通訊中斷，伺服器執行時間會叫用此常式來執行任何所需的清除。 如需內容執行程式的詳細資訊，請參閱 [伺服器內容運行時常式](server-context-run-down-routine.md)。

使用內容控制碼的介面必須具有初始系結的系結控制碼，而此控制碼必須在伺服器可以傳回內容控制碼之前發生。 您可以使用自動、隱含或明確的系結控制碼，建立系結並建立內容。

內容控制碼必須是 [ * *void \** _](/windows/desktop/Midl/void)類型或解析為 [_ *\* void* *](/windows/desktop/Midl/void)的型別。 伺服器程式會將它轉換成所需的型別。

> [!Note]  
> \[除非關閉內容控制碼的常式，否則不建議使用 [**in**](/windows/desktop/Midl/in)、 [**out**](/windows/desktop/Midl/out-idl) \] for coNtext handles 參數。 如果內容處理標記 \[ [**在中**](/windows/desktop/Midl/in)的 [](/windows/desktop/Midl/out-idl)參數， \] 則會使用 out，請勿將 **Null** 或未初始化的內容控制碼從用戶端傳遞至伺服器。 應改為傳遞內容控制碼的 **Null** 指標。 請注意，在中標示的內容控制碼參數 \[ [](/windows/desktop/Midl/in) \] 不接受 **Null** 指標。

 

下列範例介面定義的片段會顯示分散式應用程式如何使用內容控制碼來開啟伺服器，並更新每個用戶端的資料檔案。

介面必須包含用來初始化控制碼的遠端程序呼叫，並將它設定為非 **null** 值。 在此範例中，RemoteOpen 函數會執行這項作業。 它會以 \[ [**out**](/windows/desktop/Midl/out-idl)方向屬性指定內容控制碼 \] 。 或者，您可以將內容控制碼傳回為程式的傳回值。 不過，在此範例中，我們會透過參數清單傳遞內容控制碼。

在此範例中，內容資訊為檔案控制代碼。 它會持續追蹤檔案中的目前位置。 介面會將檔案控制代碼封裝為內容處理常式，並將它當作參數傳遞給遠端程序呼叫。 結構包含檔案名和檔案控制代碼。

``` syntax
/* file: cxhndl.idl (fragment of interface definition file) */
typedef [context_handle] void * PCONTEXT_HANDLE_TYPE;
typedef [ref] PCONTEXT_HANDLE_TYPE * PPCONTEXT_HANDLE_TYPE;
 
short RemoteOpen([out] PPCONTEXT_HANDLE_TYPE pphContext,
    [in, string] unsigned char * pszFile);
 
void RemoteRead(
    [in] PCONTEXT_HANDLE_TYPE phContext,
    [out, size_is(cbBuf)] unsigned char achBuf[],
    [in, out] short *pcbBuf);
 
short RemoteClose([in, out] PPCONTEXT_HANDLE_TYPE pphContext);
```

RemoteOpen 函式會建立有效的非 **null** 內容控制碼。 它會將內容控制碼傳遞給用戶端。 後續的遠端程序呼叫（例如 RemoteRead）會使用內容控制碼做為 in 指標。

除了初始化內容控制碼的遠端程式之外，介面還必須包含釋放伺服器內容的程式，並將內容控制碼設為 **Null**。 在上述範例中，RemoteClose 函數會執行這項作業。

 

 