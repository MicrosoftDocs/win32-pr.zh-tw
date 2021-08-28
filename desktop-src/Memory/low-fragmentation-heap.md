---
description: 堆積片段是可用記憶體分成小型、非連續區塊的狀態。
ms.assetid: d10abf82-423c-4942-b05e-55de3a5c4219
title: 低片段堆積
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d4cc6f7f0e2427a20532f5e32cc1460f9b6601d1e6dddf0de603757895005e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067738"
---
# <a name="low-fragmentation-heap"></a>低片段堆積

\[本主題中的資訊適用于 Windows Server 2003 和 Windows XP。 從 Windows Vista 開始，系統會視需要使用低片段堆積 (LFH) 來服務記憶體配置要求。 應用程式不需要為其堆積啟用 LFH。\]

堆積片段是可用記憶體分成小型、非連續區塊的狀態。 當堆積已分割時，即使堆積中的總可用記憶體足以滿足要求，記憶體配置仍可能會失敗，因為沒有單一記憶體區塊夠大。 低片段堆積 (LFH) 有助於減少堆積片段。

LFH 不是個別的堆積。 相反地，它是應用程式可以為其堆積啟用的原則。 當啟用 LFH 時，系統會以某些預先決定的大小來配置記憶體。 當應用程式從已啟用 LFH 的堆積要求記憶體配置時，系統會配置夠大的記憶體區塊，以容納所要求的大小。 無論是否啟用 LFH，系統都不會將 LFH 用於大於 16 KB 的配置。

應用程式應該只針對呼叫進程的預設堆積或應用程式所建立的 [私](heap-functions.md) 用堆積，啟用 LFH。 若要啟用堆積的 LFH，請使用 [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) 函數來取得呼叫進程之預設堆積的控制碼，或使用 [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) 函數所建立之私用堆積的控制碼。 然後使用控制碼呼叫 [**HeapSetInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapsetinformation) 函式。

LFH 無法針對以 **堆積 \_ 無 \_ 序列化** 或使用固定大小建立的堆積來建立堆積。 如果您在 Windows 或[Microsoft 應用程式驗證器](https://www.microsoft.com/downloads/details.aspx?FamilyID=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18&displaylang=en)的[偵錯工具](/windows-hardware/drivers/debugger/)中使用堆積偵錯工具，也無法啟用 LFH。

針對堆積啟用 LFH 之後，就無法停用它。

從 LFH 獲益最多的應用程式是多執行緒應用程式，會經常配置記憶體，並使用 16 KB 的各種配置大小。 不過，並非所有應用程式都能受益于 LFH。 若要評估在您的應用程式中啟用 LFH 的效果，請使用效能分析資料。

 

 
