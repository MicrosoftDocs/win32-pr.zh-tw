---
title: Memory-Management 模型
description: Memory-Management 模型
ms.assetid: 1690901b-2a1e-455b-a440-2674f5e5dfa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a985158f54bf09d149e04c7eebc5853417e39191ca0bb854cb7d1ba5de1e5d86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019978"
---
# <a name="memory-management-models"></a>Memory-Management 模型

如果您是開發人員，則有數個選項可供您選擇如何配置和釋放記憶體。 請考慮包含與指標連接之節點（例如連結清單或樹狀結構）所組成的複雜資料結構。 您可以套用屬性，選取下列其中一個模型：

-   [依節點的配置和解除](node-by-node-allocation-and-deallocation.md)分配。
-   [存根配置給整個樹狀結構的單一線性緩衝區](stub-allocated-buffers.md)。
-   [伺服器 stub 記憶體管理](server-stub-memory-management.md)
-   [用戶端應用程式配置給整個樹狀結構的單一線性緩衝區](application-allocated-buffer.md)。
-   [伺服器上的持續性儲存體](persistent-storage-on-the-server.md)。

 

 




