---
title: Single-Threaded 和多執行緒通訊
description: Single-Threaded 和多執行緒通訊
ms.assetid: 8d3a855c-b52d-48bb-9fdf-efbf8005c374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6470ac398e6ae1c8a645fb076fbbf509d58b579
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300531"
---
# <a name="single-threaded-and-multithreaded-communication"></a>Single-Threaded 和多執行緒通訊

支援單一執行緒和多執行緒單元的用戶端或伺服器會有一個多執行緒單元，其中包含所有初始化為自由執行緒的執行緒，以及一或多個單一執行緒單元。 介面指標必須在單元之間進行封送處理，但可以在不需要封送處理的情況下使用。 對單一執行緒單元中的物件呼叫會由 COM 進行同步處理。 COM 將不會同步處理多執行緒單元中的物件呼叫。

單一執行緒單元上的所有資訊都會套用至標示為「單元模型」的執行緒，而多執行緒單元上的所有資訊則適用于所有標記為自由執行緒的執行緒。 單元執行緒規則適用于進行內部通訊，需要在具有 [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) 和 [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream)呼叫的單元之間封送處理介面指標，如 [單一執行緒單元](single-threaded-apartments.md)中所述。

> [!Note]  
> 處理同進程伺服器時，有一些特殊考慮。 如需詳細資訊，請參閱同 [進程伺服器執行緒問題](in-process-server-threading-issues.md)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[跨單元存取介面](accessing-interfaces-across-apartments.md)
</dt> <dt>

[選擇執行緒模型](choosing-the-threading-model.md)
</dt> <dt>

[多執行緒單元](multithreaded-apartments.md)
</dt> <dt>

[同進程伺服器執行緒問題](in-process-server-threading-issues.md)
</dt> <dt>

[進程、執行緒和單元](processes--threads--and-apartments.md)
</dt> <dt>

[單一執行緒單元](single-threaded-apartments.md)
</dt> </dl>

 

 




