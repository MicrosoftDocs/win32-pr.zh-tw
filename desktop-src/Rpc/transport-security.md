---
title: 傳輸安全性
description: 雖然這不是慣用的方法，但是您可以使用具名管道傳輸提供的安全性設定，將安全性功能新增至您的分散式應用程式。
ms.assetid: faf48049-807c-4155-aa01-1947a0311a71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3d92a0c9f0b31392d265c1c60bd201d088af8e8ff0b10ac4e09e274da92d2a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011206"
---
# <a name="transport-security"></a>傳輸安全性

雖然這不是慣用的方法，但是您可以使用具名管道傳輸提供的安全性設定，將安全性功能新增至您的分散式應用程式。 這些安全性設定適用于開頭為 [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) 和 [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs)前置詞的 Microsoft RPC 函數，以及函式 [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) 和 [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself)。

> [!Note]  
> 如果您執行的是服務的應用程式，而且您使用 NTLM 進行安全性，則必須為您的應用程式新增明確的服務相依性。 Secur32.dll 會呼叫服務控制管理員 (SCM) 以開始 NTLM 安全性封裝服務。 不過，作為服務並以系統執行的 RPC 應用程式也必須與 SC 聯繫，除非它連接到同一部電腦上的另一項服務。

 

 

 




