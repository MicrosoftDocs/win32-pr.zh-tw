---
description: 下列結構適用于記憶體管理：
ms.assetid: 02a2a874-9ced-4b7d-8aad-4a7768639a32
title: 記憶體管理結構
ms.topic: article
ms.date: 11/06/2018
ms.openlocfilehash: dc9f2837941c26f0ff9fed5b7d65a00f6bd254a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945418"
---
# <a name="memory-management-structures"></a>記憶體管理結構

下列結構適用于記憶體管理。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [**CFG \_ 呼叫 \_ 目標 \_ 資訊**](-cfg-call-target-info.md) | 代表控制流程防護 (CFG) 的呼叫目標相關資訊。 |
| [**堆積 \_ 將 \_ 資源 \_ 資訊優化**](/windows/desktop/api/winnt/ns-winnt-heap_optimize_resources_information) | 指定以 [**HeapSetInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapsetinformation)起始之 HeapOptimizeResources 作業的旗標。 |
| [**記憶體 \_ 位址 \_ 需求**](/windows/desktop/api/winnt/ns-winnt-mem_address_requirements) | 針對管理虛擬記憶體的函式，指定最低和最高的基底位址和對齊方式作為擴充參數的一部分。 |
| [**記憶體 \_ 擴充 \_ 參數**](/windows/desktop/api/winnt/ns-winnt-mem_extended_parameter) | 表示管理虛擬記憶體之函式的擴充參數。 |
| [**記憶體 \_ 基本 \_ 資訊**](/windows/desktop/api/winnt/ns-winnt-memory_basic_information) | 包含處理常式虛擬位址空間中某個頁面範圍的相關資訊。 |
| [**MEMORYSTATUS**](/windows/desktop/api/WinBase/ns-winbase-memorystatus) | 包含實體和虛擬記憶體目前狀態的相關資訊。 |
| [**MEMORYSTATUSEX**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-memorystatusex) | 包含實體和虛擬記憶體（包括延伸記憶體）目前狀態的相關資訊。 |
| [**進程 \_ 堆積 \_ 專案**](/windows/desktop/api/minwinbase/ns-minwinbase-process_heap_entry) | 包含堆積元素的相關資訊。 |
| [**WIN32 \_ 記憶體 \_ 範圍 \_ 專案**](/windows/desktop/api/memoryapi/ns-memoryapi-win32_memory_range_entry) | 指定記憶體的範圍。 |
| [**WIN32 \_ 記憶體 \_ 區域 \_ 資訊**](/windows/desktop/api/memoryapi/ns-memoryapi-win32_memory_region_information) | 包含記憶體區域的相關資訊。 |
| [**AtlThunkData \_ t**](/previous-versions/windows/desktop/legacy/mt805050(v=vs.85)) | 表示 ATL Thunk 的不透明資料結構。 |
