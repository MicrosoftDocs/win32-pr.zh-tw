---
title: Client-Side 管道執行
description: 遠端程序呼叫中的用戶端管道執行 (RPC) 。
ms.assetid: d790f859-47a9-4b6c-a218-8cbe05db21b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ecae4d01e8da37c3ce65ee530643dc84abdc47da71c0e4dacbcdff21c37317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022651"
---
# <a name="client-side-pipe-implementation"></a>Client-Side 管道執行

用戶端應用程式必須執行下列程式，用戶端 stub 會在資料傳輸期間呼叫這些程式：

-   輸入管道 (的提取程式) 
-   輸出管道 (的推送程式) 
-   配置傳送資料緩衝區的配置程式

所有這些程式都必須使用由 MIDL 產生的標頭檔所指定的引數。 此外，用戶端應用程式必須有狀態變數，才能找出或放置資料的位置。

配置程式也可以像需要一樣簡單或複雜。 例如，它可以在每次存根呼叫函式時，傳回相同緩衝區的指標，或每次都可以配置不同數量的記憶體。 如果您的資料已經採用適當的格式 (管道元素的陣列，例如) 您可以協調配置程式與提取程式，以配置已經包含資料的緩衝區。 在這種情況下，您的提取程式可能是空的常式。

緩衝區配置必須以位元組為單位。 相反地，推送和提取程式會操作以位元組大小為單位的元素，取決於定義它們的方式。

本節將討論下列各節中輸入和輸出管道的用戶端執行：

-   [在用戶端上執行輸入管道](implementing-input-pipes-on-the-client.md)
-   [在用戶端上執行輸出管道](implementing-output-pipes-on-the-client.md)

 

 




