---
description: 在 Windows 環境中封鎖的概念，一直以來都是非常重要的。
ms.assetid: bd2ede96-34a4-4912-b9d2-ef11d37d2292
title: 封鎖作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8040865b4c6ededab925279e15d67cb89f7bc6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973063"
---
# <a name="blocking-operations"></a>封鎖作業

在 Windows 環境中封鎖的概念，一直以來都是非常重要的。 在 Windows 通訊端1.1 環境中，不建議使用封鎖呼叫，因為它們比起停用與系統的持續互動。 此外，它們也採用 pseudoblocking 技術，基於各種原因，不一定會如預期運作。 不過，在事先排程的 Windows 環境中，封鎖呼叫會更有意義，可由原生作業系統服務來執行，事實上通常是慣用的機制。 Winsock 2 API 已不再支援 psuedoblocking，但因為 Windows 通訊端1.1 相容性填充碼必須繼續模擬這項行為，所以服務提供者必須支援這項功能，如下所述。

 

 



