---
title: 使用內容控制碼的用戶端開發
description: 唯一使用用戶端程式的內容控制碼，就是在每次用戶端進行遠端程序呼叫時，將它傳遞至伺服器。
ms.assetid: fcbdfb1e-4f1e-4d22-9a3e-cf5a29d300d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ff599bebdf042bc2021d53538cff1c0203d2de875bdc52c50a72675b73a47f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931839"
---
# <a name="client-development-using-context-handles"></a>使用內容控制碼的用戶端開發

唯一使用用戶端程式的內容控制碼，就是在每次用戶端進行遠端程序呼叫時，將它傳遞至伺服器。 用戶端應用程式不需要存取控制碼的內容。 它不應該嘗試以任何方式變更內容處理資料。 用戶端叫用的遠端程式會對伺服器內容執行所有必要的作業。

從伺服器要求內容控制碼之前，用戶端必須先建立與伺服器的系結。 用戶端可以使用自動、隱含或明確的系結控制碼。 透過有效的系結控制碼，用戶端可以呼叫伺服器上的遠端程式，以傳回開啟的 (非 **Null**) 內容控制碼，或透過遠端程式的參數清單中的 **\[ out \]** 參數傳遞一個。

用戶端可能會以任何需要的方式使用開啟的內容控制碼。 不過，它們應該會在不再需要時使控制碼失效。 有兩種方式可以執行此作業：

-   若要叫用伺服器程式所提供的遠端程式以釋出內容，並關閉內容控制碼 (將它設定為 **Null**) 。
-   無法連線到伺服器時，請呼叫 [**RpcSsDestroyClientCoNtext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) 函式。

第二種方法只會清除用戶端狀態，而且不會清除伺服器端狀態，因此只有在懷疑網路磁碟分割時，才應該使用它，而用戶端和伺服器則會執行獨立的清除作業。 伺服器會透過運行時常式執行獨立的清除，用戶端會使用 [**RpcSsDestroyClientCoNtext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) 函式來執行此動作。

下列程式碼片段會顯示用戶端如何使用內容控制碼的範例。 若要查看此範例所使用介面的定義，請參閱 [使用內容控制碼進行介面開發](interface-development-using-context-handles.md)。 如需伺服器的執行，請參閱 [使用內容控制碼的伺服器開發](server-development-using-context-handles.md)。

在此範例中，用戶端會呼叫 RemoteOpen 來取得包含有效資料的內容控制碼。 然後，用戶端就可以使用遠端程序呼叫中的內容控制碼。 由於它不再需要系結控制碼，因此用戶端可以釋放用來建立內容控制碼的明確控制碼：


```C++
// cxhndlc.c  (fragment of client side application)
printf("Calling the remote procedure RemoteOpen\n");
if (RemoteOpen(&phContext, pszFileName) < 0) 
{
    printf("Unable to open %s\n", pszFileName);
    Shutdown();
    exit(2);
}
 
// Now the context handle also manages the binding.
// The variable hBindingHandle is a valid binding handle.
status = RpcBindingFree(&hBindingHandle);
printf("RpcBindingFree returned 0x%x\n", status);
if (status) 
    exit(status);
```



此範例中的用戶端應用程式會使用名為 RemoteRead 的程式來讀取伺服器上的資料檔案，直到遇到檔案結尾為止。 然後藉由呼叫 RemoteClose 來關閉檔案。 內容控制碼會顯示為 RemoteRead 和 RemoteClose 函式中的參數，如下所示：


```C++
printf("Calling the remote procedure RemoteRead\n");
do 
{
    cbRead = 1024; // Using a 1K buffer
    RemoteRead(phContext, pbBuf, &cbRead);
    // cbRead contains the number of bytes actually read.
    for (int i = 0; i < cbRead; i++)
        putchar(*(pbBuf+i));
} while(cbRead);
 
printf("Calling the remote procedure RemoteClose\n");
if (RemoteClose(&phContext) < 0 ) 
{
    printf("Close failed on %s\n", pszFileName);
    exit(2);
}
```



 

 




