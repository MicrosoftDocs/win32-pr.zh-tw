---
title: 請小心在相同進程中執行其他 RPC 端點
description: 當應用程式與其他 RPC 伺服器位於同一個進程時，所有應用程式都會接聽所有的通訊協定。
ms.assetid: edb20108-e0c3-4b9b-b57d-45a96d9472ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00828ddf95fd024069a8a535c95673eb014d84b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673915"
---
# <a name="be-wary-of-other-rpc-endpoints-running-in-the-same-process"></a>請小心在相同進程中執行其他 RPC 端點

當應用程式與其他 RPC 伺服器位於同一個進程時，所有應用程式都會接聽所有的通訊協定。 如此一來，如果元件[](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) \* 只針對 LRPC 呼叫 RpcServerUseProtseq，就不一定能透過 LRPC 來存取它。 它可能可以透過其他通訊協定來存取，因為進程中的其他 RPC 伺服器可能會在管道或通訊端上接聽 (例如) 。

類似于嚴格的內容控制碼，不會將另一個端點放在進程中，也不表示另一個端點不存在。 無論您註冊伺服器的方式為何，您的介面和端點之間都沒有特殊的關聯;所有介面都可在該進程的所有端點上呼叫。 這是端點安全性模型失效的另一個原因;如果安全描述項放在端點上，攻擊者可以在另一個端點上呼叫介面。

若要確保只會在特定的通訊協定順序呼叫進程，請註冊安全性回呼函式，並在該函式中檢查發出呼叫的通訊協定順序。

 

 




