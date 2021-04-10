---
title: 網路管理函數緩衝區
description: RPC 執行時間程式庫會處理32位資料抓取網路管理功能所需的緩衝區，如下所示。
ms.assetid: f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385382d12aa5b5c8c7c93b9a833f684d913c5783
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183647"
---
# <a name="network-management-function-buffers"></a>網路管理函數緩衝區

RPC 執行時間程式庫會處理32位資料抓取網路管理功能所需的緩衝區，如下所示：

-   **將資料傳送至伺服器** (\[) 參數中所指定的資料 \] 。

    呼叫端必須配置和解除配置相關資訊結構 (或結構) 的緩衝區，並將指標變數傳遞給函式。 呼叫端不需要指定緩衝區長度。

    Example: [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)

-   **從伺服器抓取資料** (out 參數所指定的資料 \[ \]) 。

    系統會為傳回的資訊配置緩衝區。 呼叫端必須將指標變數傳遞給輸入上的函式。 在成功傳回時，指標會收到系統組態的緩衝區位址，其中包含傳回的資訊。 這麼做可簡化呼叫程式碼，因為呼叫端不需要估計緩衝區大小，也不需要調整緩衝區大小，然後重新發出函數。

    當呼叫端處理傳回的資訊之後，它必須藉由呼叫 [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) 函式來釋放系統組態的記憶體。 如需有關指定緩衝區大小的詳細資訊，請參閱 [網路管理函數緩衝區長度](network-management-function-buffer-lengths.md)。

    範例： [ **NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)

 

 




