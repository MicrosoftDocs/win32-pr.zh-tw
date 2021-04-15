---
title: 選擇執行緒模型
description: 選擇執行緒模型
ms.assetid: e8a0286d-1831-454f-8549-1957fd794809
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f0fdcd327bf05c0019a03ad171d41c1f1d95a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372589"
---
# <a name="choosing-the-threading-model"></a>選擇執行緒模型

選擇物件的執行緒模型取決於物件的函數。 執行大量 i/o 的物件可能支援無限制執行緒，藉由在 i/o 延遲期間允許介面呼叫，提供最大的回應給用戶端。 另一方面，與使用者互動的物件可能會支援單元執行緒傳入的 COM 呼叫與其視窗作業。

在單一執行緒的單元中支援單元執行緒比較容易，因為 COM 會針對個別呼叫提供同步處理。 支援自由執行緒較難，因為物件必須執行同步處理;不過，對用戶端的回應可能更好，因為可以針對較小的程式碼區段來執行同步處理。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[跨單元存取介面](accessing-interfaces-across-apartments.md)
</dt> <dt>

[多執行緒單元](multithreaded-apartments.md)
</dt> <dt>

[同進程伺服器執行緒問題](in-process-server-threading-issues.md)
</dt> <dt>

[進程、執行緒和單元](processes--threads--and-apartments.md)
</dt> <dt>

[單一執行緒和多執行緒通訊](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[單一執行緒單元](single-threaded-apartments.md)
</dt> </dl>

 

 




