---
title: 工作集資訊
description: 進程的工作集是實際對應至其處理內容的記憶體數量。 PSAPI.DLL 可讓您取得工作集的快照集，或監視工作集。
ms.assetid: 33c42f79-cc77-4d44-84c3-8bf0a4a60019
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56e1e4dc0a68a9d4507a94ad1f5356432f8488a
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549860"
---
# <a name="working-set-information"></a>工作集資訊

進程的工作集是實際對應至其處理內容的記憶體數量。 PSAPI.DLL 可讓您取得工作集的快照集，或監視工作集。

[**QueryWorkingSet**](/windows/desktop/api/Psapi/nf-psapi-queryworkingset)或 [**QueryWorkingSetEx**](/windows/desktop/api/Psapi/nf-psapi-queryworkingsetex)函式會使用指定進程目前工作集中每個頁面的資訊快照來填滿緩衝區。 此函式只會報告實際存在於呼叫它的實際頁面。

您可以使用工作集監視來找出特定作業需要多少額外的 RAM (例如，將檔案儲存) 。 若要開始監視工作集，請呼叫 [**InitializeProcessForWsWatch**](/windows/desktop/api/Psapi/nf-psapi-initializeprocessforwswatch) 函數。 並非所有的程式都可讓您讀取其工作集資訊，因此請確定函式會傳回非零的值，然後再繼續進行。 接下來，呼叫 [**GetWsChanges**](/windows/desktop/api/Psapi/nf-psapi-getwschanges) 函數。 此函數只會報告自您開始監視工作集之後，已載入記憶體的頁面。 此函式會傳回 [**Psapi.dll \_ WS \_ WATCH \_ 資訊**](/windows/desktop/api/Psapi/ns-psapi-psapi_ws_watch_information) 結構的陣列中的資料，每個新增的頁面都會有一個結構，並新增至處理常式的工作集。 此結構會告訴您哪些頁面位於記憶體中，以及導致系統將它們分頁的原因。

[**EmptyWorkingSet**](/windows/desktop/api/Psapi/nf-psapi-emptyworkingset)函式會採用進程控制碼。 它會盡可能從進程工作集移除最多頁面。 這項作業主要適用于測試和微調。 請注意，如果您傳遞-1 的最小和最大大小， [**SetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize) 函式會執行相同的工作。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作集](/windows/desktop/Memory/working-set)
</dt> </dl>

 

 