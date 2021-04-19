---
description: 使用2.0 版時，效能計數器會變更架構，以簡化將計數器資料提供給取用者的流程。
ms.assetid: 37f75b15-3f52-4259-a6d9-5a1a14f88379
title: 使用2.0 版提供計數器資料
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 67976c8a0b6c77582ed8c50c2e5cf753c77fcf6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993135"
---
# <a name="providing-counter-data-using-version-20"></a>使用2.0 版提供計數器資料

新式效能資料提供者會使用資訊清單來定義計數器資料，並使用效能計數器提供者 Api 來管理提供者內容中的資料。 使用資訊清單和效能計數器提供者 Api 來執行的提供者通常稱為 **V2 提供者**。 Windows 支援 windows Vista 或更新版本上的使用者模式 V2 提供者，以及 Windows 7 或更新版本上的核心模式 V2 提供者。

此頁面描述使用者模式 V2 提供者。 如需核心模式 V2 提供者的詳細資訊，請參閱 [核心模式效能監視](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring)。

在執行時間，V2 提供者的運作方式如下：

- 提供者進程會藉由呼叫 PerfStartProvider 和 PerfSetCounterSetInfo，向 Windows 效能計數器系統註冊本身。 提供者會選擇性地提供回呼函式，以通知取用者要求。
- 提供者進程會使用 PerfCreateInstance 和 PerfDeleteInstance 適當地新增或移除實例。 當提供者使用 PerfSet * * _ Api 進行變更時，會更新計數器值。
- 取用者會向 counterset 提出資料的要求。 系統會確認呼叫端具有收集資料的許可權。 然後，系統會使用在提供者進程中執行的背景工作執行緒來處理要求，並在適當時叫用提供者的回呼函數。 背景工作執行緒會將收集的資料複製到系統管理的緩衝區中，然後系統會將資料傳回到取用者。

## <a name="steps-to-creating-a-provider"></a>建立提供者的步驟

1. 撰寫會定義提供者所提供之計數器資料的資訊清單。 如需寫入資訊清單的詳細資訊，請參閱 [效能計數器架構](performance-counters-schema.md)。
2. 使用 [CTRPP](ctrpp.md) 來產生您的提供者所包含的範本程式碼。 範本程式碼包含定義計數器集合、 [_ *CounterInitialize* *](counterinitialize.md)和 [**CounterCleanup**](countercleanup.md)函數以及資源字串的結構。

   您的提供者必須呼叫 [**CounterInitialize**](counterinitialize.md) 和 [**CounterCleanup**](countercleanup.md) 函數。 **CounterInitialize** 會呼叫 [**PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)函式來註冊提供者，也會呼叫 [**PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)函數來初始化計數器集合。 **CounterCleanup** 會呼叫 [**PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)函數來移除提供者的註冊。

3. 在您的專案中包含上一個步驟的範本程式碼，並完成您的提供者。

   若要完成提供者，您必須針對每個您提供的計數器集合實例呼叫 [**PerfCreateInstance**](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance) 函數。

   若要設定計數器值，請呼叫下列其中一項功能：

   - [**PerfSetULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
   - [**PerfSetULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
   - [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)

   使用 [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue) 的優點是，您不需要進行函式呼叫來設定或更新計數器值，只要更新本機計數器變數 (參考點) 的變數，而效能計數器會使用指標來存取計數器值。

   如果您不使用 [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)，您可以使用下列函數來遞增或遞減計數器值：

   - [**PerfDecrementULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulongcountervalue)
   - [**PerfDecrementULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulonglongcountervalue)
   - [**PerfIncrementULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue)
   - [**PerfIncrementULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulonglongcountervalue)

   在提供者結束之前，它必須針對它所建立的每個計數器集合實例呼叫 [**PerfDeleteInstance**](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance) 。

   如果您在資訊清單中指定 [**provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element)元素的 **回呼** 屬性，或在呼叫 [CTRPP](ctrpp.md)時使用 **-NotificationCallback** 引數，則必須執行 [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)回呼函數。 您將回呼函數傳遞給 [**CounterInitialize**](counterinitialize.md)。

   如果您在呼叫 [CTRPP](ctrpp.md)時使用 **-MemoryRoutines** ，則必須執行 [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc)和 [*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free)回呼函數。 您將回呼函數傳遞給 [**CounterInitialize**](counterinitialize.md)。

4. 安裝您的提供者時，請使用 LodCtr 工具，將包含當地語系化資源字串和資源識別碼的二進位檔案名稱寫入至登錄。 如需使用 LodCtr 的詳細資訊，請參閱 [效能計數器架構](performance-counters-schema.md)。

5. 卸載您的提供者時，請使用 UnlodCtr 工具從登錄中移除提供者的資訊。
