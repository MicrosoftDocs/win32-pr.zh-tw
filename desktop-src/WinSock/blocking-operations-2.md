---
description: 在 Windows 環境中封鎖的概念，一直以來都是非常重要的。
ms.assetid: bd2ede96-34a4-4912-b9d2-ef11d37d2292
title: 封鎖作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d130de2322e10de15bc73e9901b7d55764b34cfbb609e2e25942fb55a3cf445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322433"
---
# <a name="blocking-operations"></a>封鎖作業

在 Windows 環境中封鎖的概念，一直以來都是非常重要的。 在 Windows 通訊端1.1 環境中，不建議使用封鎖呼叫，因為它們比起停用與系統的持續互動。 此外，它們也採用 pseudoblocking 技術，基於各種原因，不一定會如預期運作。 不過，在事先排程 Windows 環境中，封鎖的呼叫會更有意義，可由原生作業系統服務執行，而且實際上是慣用的機制。 Winsock 2 API 已不再支援 psuedoblocking，但因為 Windows 通訊端1.1 相容性填充碼必須繼續模擬此行為，所以服務提供者必須支援這項功能，如下所述。

 

 



