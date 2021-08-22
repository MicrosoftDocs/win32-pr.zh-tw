---
title: 註冊介面
description: 註冊伺服器程式支援的介面，可讓用戶端程式從遠端程序呼叫分派至適當的伺服器常式。
ms.assetid: 953185a7-00e6-442d-b474-a983f4a91c38
keywords:
- 遠端程序呼叫 RPC、工作、註冊介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c444a82d30848f4f01643c08f17f484d027bc7b8c8efe3f10e7f3c194aac26a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926874"
---
# <a name="registering-the-interface"></a>註冊介面

註冊伺服器程式支援的介面，可讓用戶端程式從遠端程序呼叫分派至適當的伺服器常式。 伺服器程式會呼叫 [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) 來註冊其介面。 下列程式碼片段會示範其用途：


```C++
RPC_STATUS status;
status = RpcServerRegisterIf(MyInterface_v1_0_s_ifspec, NULL, NULL);
```



[**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)函式的第一個參數是 MIDL 編譯器從 IDL 檔案產生的結構，該檔案會定義伺服器) 的介面 (或介面。 第二個和第三個參數分別是 UUID 和進入點向量。 在此範例中，這些值會設定為 **Null** 。 在許多情況下，您的伺服器程式會將這些參數值設定為 **Null**。 當伺服器程式在介面中提供相同程式的多個程式時，會使用第二個和第三個參數。 如需詳細資訊，請參閱 [進入點向量](registering-interfaces.md)。

伺服器程式也可以使用 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) 來註冊介面。 使用此函式的其中一個優點是，它會提供您的應用程式設定安全性回呼函式的能力。 使用安全性回呼函數是保護介面安全的建議方法。

> [!Note]  
> MIDL 會產生兩個非常類似的結構，一個用於用戶端，另一個用於伺服器。 傳遞至 [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) 函數的結構是 MIDL 產生之結構的伺服器版本。

 

 

 




