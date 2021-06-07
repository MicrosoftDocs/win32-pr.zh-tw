---
description: 程式的工作集是其虛擬位址空間中最近參考的頁面集合。
ms.assetid: 6017ef59-d2e9-4245-a406-8965024dbb35
title: 處理工作集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaded3d0b5f8c6ad552cc728c68ad0407391c343
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549900"
---
# <a name="process-working-set"></a>處理工作集

程式的 *工作集* 是其虛擬位址空間中最近參考的頁面集合。 它包含共用和私用資料。 共用資料包含包含應用程式執行之所有指令的頁面，包括您的 Dll 和系統 Dll 中的所有指示。 當工作集大小增加時，記憶體需求也會增加。

進程有相關聯的工作集大小下限和工作集大小上限。 每次呼叫 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)時，它會保留進程的工作集大小下限。 當程式為使用中狀態時，虛擬記憶體管理員會嘗試保留足夠的記憶體供最小的工作集常駐，但不會超過大小上限。

若要取得應用程式的工作集所要求的最小和最大大小，請呼叫 [**GetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-getprocessworkingsetsize) 函數。

系統會設定預設的工作集大小。 您也可以使用 [**SetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize) 函數來修改工作集大小。 設定這些值並不保證會保留或駐留記憶體。 請小心要求太大或最大的工作集大小，因為這樣做可能會降低系統效能。

若要取得處理常式之工作集目前或最大的大小，請使用 [**GetProcessMemoryInfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) 函數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[記憶體效能資訊](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))
</dt> <dt>

[工作集](../memory/working-set.md)
</dt> </dl>

 

 
