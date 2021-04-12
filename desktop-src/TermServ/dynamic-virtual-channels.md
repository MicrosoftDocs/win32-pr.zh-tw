---
title: 動態虛擬通道
description: 動態虛擬通道 (DVC) Api 擴充現有的虛擬通道 Api，以供遠端桌面服務（稱為靜態虛擬通道 (SVC) Api）。
ms.assetid: bddf0048-482d-40f3-a973-9d7bc15be8fa
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3181c0960b50289846018c3ace773a8351cb20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372145"
---
# <a name="dynamic-virtual-channels"></a>動態虛擬通道

動態虛擬通道 (DVC) Api 擴充現有的虛擬通道 Api，以供遠端桌面服務（稱為靜態虛擬通道 (SVC) Api）。 DVC Api 可解決用戶端與伺服器之間的 SVC Api 中存在的數個限制，例如：

-   頻道數量有限
-   封包重建

DVC Api 將協助您在伺服器和用戶端上，在與彼此通訊的遠端桌面服務連接上執行模組。

就像許多其他用戶端/伺服器架構一樣，系統會根據常同意的資料片段（稱為端點）來建立連接。 類似的範例是 TCP/IP，也就是透過伺服器 IP 位址和埠名稱的組合來建立端點。 另一個範例是具名管道，其中端點是伺服器名稱和管道名稱的組合。 在遠端桌面服務連接中，只涉及兩個邊。 因此，端點是由可唯一識別連接的簡單任一字元串所組成。 就像 TCP/IP 和具名管道一樣，可以從相同的端點名稱起始多個連接。 在這種情況下，連接沒有名稱;只有接聽程式會等候端點上的傳入要求。

DVC Api 包含下列各項：

-   用戶端 API

    這些 Api 可在遠端桌面連線 (RDC) 用戶端以外掛程式的形式提供。 用戶端處於被動模式，它會接聽連入連線，但不會主動建立連線。

-   伺服器 Api

    這些 Api 會主動起始連接。

如需如何將動態虛擬通道寫入 (DVC) 模組的相關資訊，請參閱 [DVC 的實作為詳細資料](dvc-implementation-details.md)。

 

 




