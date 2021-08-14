---
title: " (RPC) 的管道"
description: 管道型別函式是一種非常有效率的機制，可傳遞大量資料，或一次無法在記憶體中使用的任何資料數量。
ms.assetid: 913d5e2a-00ad-4060-9274-a6db23fb2817
keywords:
- 遠端程序呼叫 RPC、描述、管道
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c477dc249e400022efda21fef4055840c5095e74500f4ae0bea375310b1903f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927520"
---
# <a name="pipes-rpc"></a> (RPC) 的管道

管道型別函式是一種非常有效率的機制，可傳遞大量資料，或一次無法在記憶體中使用的任何資料數量。 藉由使用管道，RPC 執行時間會處理實際的資料傳輸，消除與重複遠端程序呼叫相關聯的額外負荷。

用戶端叫用具有管道參數的遠端程式之後，用戶端和伺服器會進入迴圈來傳送資料。 資料可以在用戶端或伺服器上產生。 無論何種方式， (位元組的資料量（以位元組為) 單位）都不需要事先知道。 您可以用累加方式產生或取用資料。 在資料傳輸迴圈中，伺服器會呼叫載入或卸載資料緩衝區的存根常式。 用戶端會呼叫程式設計人員定義的程式，以配置緩衝區、將資料載入至緩衝區以及從中卸載資料。

本節提供使用管道進行遠端程序呼叫的總覽。 本主題提供下列主題的總覽：

-   [基本管道術語](essential-pipe-terminology.md)
-   [管道狀態](the-pipe-state.md)
-   [在 IDL 檔案中定義管道](defining-pipes-in-idl-files.md)
-   [用戶端管道執行](client-side-pipe-implementation.md)
-   [伺服器端管道執行](server-side-pipe-implementation.md)
-   [多個管道的規則](rules-for-multiple-pipes.md)
-   [結合管道和 Nonpipe 參數](combining-pipe-and-nonpipe-parameters.md)

如需管道語法和限制的詳細資訊，請參閱 MIDL 語言參考中的 [管道](/windows/desktop/Midl/pipe) 。 平臺軟體發展工具組中的管道範例程式 (SDK) 範例 \\ rpc 目錄示範如何在用戶端與伺服器之間傳輸資料 **\[ ，以在中使用 in、out \]** 管道。

 

 
