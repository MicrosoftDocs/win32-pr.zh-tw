---
title: RPC 和網路
description: 本節討論如何在使用 RPC 時處理網路程度，並說明 RPC 層級 Api 如何轉譯成網路活動。 區段只會參考 ncacn 的 \_ ip \_ tcp 和 ncacn \_ HTTP 通訊協定序列。
ms.assetid: af7c67ea-32af-40b0-b74b-0a339e5088c4
keywords:
- 遠端程序呼叫 RPC、最佳作法、RPC 和網路
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 212e1f3b6f281709a3344367a59d858b7f96b77a6adbdc44fc8556769f2edcaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926650"
---
# <a name="rpc-and-the-network"></a>RPC 和網路

本節討論如何在使用 RPC 時處理網路程度，並說明 RPC 層級 Api 如何轉譯成網路活動。 區段只會參考 ncacn 的 [**\_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp) 和 [**ncacn \_ HTTP**](/windows/desktop/Midl/ncacn-http) 通訊協定序列。

本節分為下列主題：

-   [在網路中開發與部署](development-versus-deployment-in-the-network.md)
-   [防止 Client-Side 停止回應](preventing-client-side-hangs.md)
-   [管理 (關聯) 的網路連接集 ](managing-network-connection-sets-associations-.md)
-   [閒置連接清除](idle-connection-cleanup.md)
-   [處理連接中斷](dealing-with-loss-of-connectivity.md)
-   [伺服器端清除](server-side-cleanup.md)

 

 