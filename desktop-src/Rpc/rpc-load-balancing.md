---
title: RPC 負載平衡
description: RPC 負載平衡
ms.assetid: c646f748-d5f2-422d-8305-1f86c0dc61b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7fbace237f6d86ebadf3fadc5f3b376d94799b137153b114bc07fead3d64b09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101648"
---
# <a name="rpc-load-balancing"></a>RPC 負載平衡

Microsoft RPC 負載平衡旨在提供可調整的解決方案，適用于需要高負載 [RPC OVER HTTP](remote-procedure-calls-using-rpc-over-http.md) 流量的案例。 RPC Load Balancer 的主要用途是確保伺服器陣列可以服務 RPC/HTTP 流量，以改善擴充性。 為了達成此目的，RPC 必須確保用戶端進程的所有連接都是由伺服器陣列中的相同伺服器端點所服務。 RPC Load Balancer 會實作為服務，以與 RPC over HTTP Proxy 服務一起執行。

若要啟用負載平衡，在每部伺服器上執行的 RPC 負載平衡服務會彼此通訊，以判斷初始用戶端連接的慣用伺服器。 此程式稱為仲裁，它會在初始用戶端連線時進行。 為了減少跨伺服器流量，如果用戶端尚未與伺服器相關聯，則 RPC 負載平衡服務會選擇本機端點來服務連接。 針對指定的用戶端連接，仲裁的結果有兩種：

-   如果用戶端已建立連接，則第一次接收連接的伺服器將會處理後續的連線。
-   如果這是用戶端的第一個連接，仲裁將會導致本機伺服器處理連線，因此會產生來自用戶端的所有連接。 這項資訊一旦決定後，就會認可到伺服器陣列中的其他 RPC Load Balancer 服務，因此會通知伺服器處理所有用戶端的要求。

本節提供下列主題中的 RPC 負載平衡總覽：

-   [部署負載平衡](deploying-load-balancing.md)
-   [設定負載平衡](configuring-load-balancing.md)
-   [負載平衡的最佳作法](load-balancing-best-practices.md)

## <a name="requirements"></a>規格需求

執行 Windows Server 2008 R2 或更新版本的伺服器，以及執行 Windows 7 或更新版本 Windows 的用戶端，都支援 RPC 負載平衡服務。

RPC Proxy 服務、RPC 負載平衡服務和伺服器端點都必須在同一部電腦上執行。 此外，伺服器陣列中的所有伺服器都必須能夠服務所要求的端點。 如需設定 RPC Proxy 服務與 RPC 負載平衡服務的相關資訊，請參閱分別設定 [rpc OVER HTTP 的電腦](configuring-computers-for-rpc-over-http.md) 和設定 [負載平衡](configuring-load-balancing.md)。

## <a name="limitations"></a>限制

目前，RPC 負載平衡只支援每個資源一個伺服器陣列。 所有伺服器陣列中的所有伺服器也必須能夠服務所有資源。

 

 




