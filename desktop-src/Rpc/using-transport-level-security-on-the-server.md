---
title: 在伺服器上使用傳輸層級安全性
description: 在具有遠端程序呼叫的伺服器上使用傳輸層級安全性， (RPC) 。
ms.assetid: 8ad86d46-cdc8-44f0-bb56-4d5069f33e64
keywords:
- 在伺服器上使用傳輸層級安全性的遠端程序呼叫 RPC、工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6abd1f072f249336f4804aed56fb1122556596c43286383b763839d988a2406b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010586"
---
# <a name="using-transport-level-security-on-the-server"></a>在伺服器上使用傳輸層級安全性

本節提供傳輸層級安全性的討論，分為下列主題：

-   [在用戶端上使用 Transport-Level 安全性](using-transport-level-security-on-the-client.md)

當您使用 [ncacn \_ np](/windows/desktop/Midl/ncacn-np) 或 [ncalrpc](/windows/desktop/Midl/ncalrpc) 做為通訊協定順序時，伺服器會在選取通訊協定順序時，指定端點的安全描述項。 如需通訊協定順序的詳細資訊，請參閱 [指定通訊協定順序](specifying-protocol-sequences.md)。 您的應用程式會將安全描述項提供為額外的參數， (標準憑證-DCE 參數的擴充功能，) 所有開頭為首碼 [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) 和 [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs)的函式。 安全描述項可控制用戶端是否可以連接到端點。

每個進程和執行緒都與安全性權杖相關聯。 此權杖包含預設安全描述項，可用於處理常式所建立的任何物件，例如端點。 如果您的應用程式在呼叫 [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) 和 [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs)首碼的函式時未指定安全描述項，則 RPC 執行時間程式庫會將預設安全描述項從進程安全性權杖套用至端點。

為了保證所有用戶端都可以存取伺服器應用程式，系統管理員應該在具有所有用戶端可使用之預設安全描述項的進程上啟動伺服器應用程式。 一般來說，只有系統進程會有預設的安全描述項。

如需這些函式和函數的詳細資訊， [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) 和 [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself)。

 

 