---
title: 讓伺服器可在網路上使用
description: 在伺服器應用程式接受遠端程序呼叫之前，必須先在網路上提供。
ms.assetid: 1fad55e2-7221-4153-b530-b36ea42e03e1
keywords:
- 遠端程序呼叫 RPC、工作、使伺服器可供使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55385a1ba10f7f8ca28622af0b145ce25ef1bbbd0ab8df327687ce7fd7db6f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020052"
---
# <a name="making-the-server-available-on-the-network"></a>讓伺服器可在網路上使用

在伺服器應用程式接受遠端程序呼叫之前，必須先在網路上提供。 若要這樣做，伺服器會向 RPC 執行時間指出它願意接受一或多個通訊協定序列的呼叫。 選擇伺服器應用程式所支援的通訊協定順序是一個重要的決策;不同的通訊協定順序具有非常不同的功能。 預期在本機接收呼叫的伺服器應該使用 **ncalrpc**。 接受遠端呼叫的伺服器應該使用 **ncacn 的 \_ ip \_ tcp**。 伺服器不應確認接收呼叫的通訊協定順序，是它們預期接收呼叫的通訊協定順序。 如需詳細資訊，請參閱最佳 RPC 程式設計實務中，在相同進程中執行的其他 RPC 端點的小心謹慎。

下列範例會使用 **ncacn 的 \_ ip \_ tcp**。

大部分的伺服器程式會使用網路上所有可用的通訊協定順序。 若要這樣做，他們會叫用 [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) 函式，如下列程式碼片段所示：


```C++
RPC_STATUS status;
status = RpcServerUseAllProtseq(
    L"ncacn_ip_tcp",
    RPC_C_PROTSEQ_MAX_REQS_DEFAULT,    // Protseq dependent parameter
    NULL);                             // Always specify NULL here.
```



[**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq)函數的第一個參數是通訊協定順序。 第二個參數相依于通訊協定順序。 如程式碼片段所示，大部分的伺服器程式都會將此參數設定為 **RPC \_ C \_ PROTSEQ \_ MAX \_ 先決條件 \_ DEFAULT**。 此值會將 RPC 程式庫設定為使用預設值。 第三個參數是安全描述項，不應在應用程式中使用。 如需詳細資訊，請參閱 [**安全性**](security.md)。

您也可以使用 [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs)、 [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)、 [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep)或 [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) 函數。

當伺服器應用程式至少選取一個通訊協定序列之後，使用動態端點的伺服器必須為它所使用的每個通訊協定順序建立系結資訊。 伺服器會在系結向量中儲存系結資訊，然後將其匯出至端點對應程式服務。

您可以使用 [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) 函數取得伺服器應用程式的系結向量，如下列範例所示：


```C++
RPC_STATUS status;
RPC_BINDING_VECTOR *rpcBindingVector;
 
status = RpcServerInqBindings(&rpcBindingVector);
```



傳遞至 [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) 函式的唯一參數是指向 RPC 系結 [**\_ \_ 向量**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector) 結構指標的指標。 RPC 執行時間程式庫會動態配置系結向量的陣列，並將陣列的位址儲存在參數變數 (在此案例中為 **rpcBindingVector**) 。 每個伺服器應用程式在使用 RpcBindingVectorFree 函式完成使用之後，會負責使用[](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree)函式釋放這個系結向量 (例如，將它傳遞給適當的函式) 。

 

 




