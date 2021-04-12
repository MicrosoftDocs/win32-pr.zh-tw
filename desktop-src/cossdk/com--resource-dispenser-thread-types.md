---
description: COM + 資源配置器執行緒類型
ms.assetid: 3ab67adb-311f-404c-a3ca-d274af53f91c
title: COM + 資源配置器執行緒類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 761d85edc3105785ded904fd2dc6083a9aea30cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385899"
---
# <a name="com-resource-dispenser-thread-types"></a>COM + 資源配置器執行緒類型

COM + 資源配置器的呼叫可能源自下列其中一種執行緒類型：

-    (STA) 的單元執行緒
-    (MTA) 的自由執行緒
-   非 COM 執行緒 (應用程式或分配 [器管理員](com--dispenser-manager.md) 垃圾收集器執行緒) 

如果資源配置器不是 COM 物件，它就必須能夠隨時處理來自任何執行緒的呼叫。 如果資源配置器是 COM 物件，則應該使用 **兩者** 的執行緒模型來註冊 com 物件。 這可讓 STA 或 MTA 執行緒在沒有線程切換的情況下，建立及使用資源配置器。

如果資源配置器建立並使用另一個 COM 物件 (例如，跨進程的 resource manager) ，資源配置器可能需要維護此其他 COM 物件的多個 proxy，並確保對呼叫執行緒使用適當的 proxy 來呼叫物件。 當資源配置器建立這個物件時，它會封送處理並儲存參考。 再次呼叫物件之前，必須先 unmarshal 來建立呼叫執行緒的 proxy。

快取這些每個執行緒的 proxy 可能更有效率，方法是將對應從執行緒識別碼保留至 proxy 指標。 此對應會在進程中使用新的執行緒時展開。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 資源配置器概念](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



