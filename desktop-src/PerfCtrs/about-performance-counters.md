---
description: 計數器是用來提供與作業系統或應用程式、服務或驅動程式的執行狀況有關的資訊。
ms.assetid: d172a131-61d3-4fc1-8e0c-b07b2bd34f80
title: 關於效能計數器
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 8a80ac907ef842e4564f0e67daa173fee165bc93d8fa568920df8ffc24b8c9a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978910"
---
# <a name="about-performance-counters"></a>關於效能計數器

Windows效能計數器提供高層級的抽象層，其具有一致的介面，可收集各種類型的系統資料，例如 CPU、記憶體和磁片使用量統計資料。 系統管理員會使用效能計數器來監視效能或行為問題。 軟體發展人員會使用效能計數器來檢查其元件的資源使用量。

> [!IMPORTANT]
> Windows效能計數器最適合用於管理/診斷資料探索和收集。 它們不適合用于高頻率的資料收集或應用程式分析，因為它們的設計不是每秒收集一次以上。 若要對系統資訊進行較低的額外負荷存取，您可能會想要更多的直接 Api，例如 [**處理狀態**](../psapi/process-status-helper.md)協助程式、 [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex)、 [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes)或 [**GetProcessTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesstimes)。 針對分析，您可能會使用 [**tracelog.exe**](/windows-hardware/drivers/devtest/tracelog) 搭配、、或選項來收集 ETW 記錄檔中的系統分析資料 `-critsec` `-dpcisr` `-eflag` `-ProfileSource` ，或者您可能會使用 [**硬體計數器**](/previous-versions/windows/desktop/hcp/hcp-reference)程式碼剖析。

> [!NOTE]
> 請勿將 Windows 效能計數器與 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) API 混淆。 Windows效能計數器提供許多類型的系統資訊的高階抽象概念。 QueryPerformanceCounter 函式可針對高精確度的時間戳記提供優化的存取。

## <a name="getting-started"></a>開始使用

- 當您想要從系統收集或查看效能資料時，請使用 [效能計數器工具](performance-counters-tools.md) 。
- 當您想要撰寫腳本或從本機系統收集效能資料的程式時，請使用 [效能計數器集合 api](consuming-counter-data.md) 。
- 當您想要使用 WMI 從本機或遠端系統收集效能資料時，請使用 [Wmi 效能計數器類別](/windows/desktop/WmiSdk/monitoring-performance-data) 。
- 當您想要從軟體元件發佈效能資料時，請使用 [效能計數器提供者 api](providing-counter-data.md) 。

## <a name="concepts"></a>概念

Windows 效能計數器系統會組織成取用 **者**、**提供** 者、 **countersets**、**計數器**、**實例** 和 **計數器值**。

取用 **者** 是利用效能資料的軟體元件。 Windows 包含數個可利用效能資料的[內建工具](performance-counters-tools.md)。 這些包含工作管理員、資源監視器、效能監視器、typeperf.exe、logman.exe 和 relog.exe。 開發人員可以撰寫腳本和應用程式，透過 [效能計數器 api](consuming-counter-data.md)來存取效能計數器。

**提供者** 是 [產生和發佈效能資料](providing-counter-data.md)的軟體元件。 提供者會發行一個或多個 *countersets* 的資料。 例如，資料庫系統可能會將本身註冊為效能資料提供者。

- **V1 提供者** 是一種軟體元件，可透過在取用者進程中執行的 [效能 DLL](providing-counter-data-using-a-performance-dll.md)發佈效能資料。 V1 提供者會透過檔案安裝到系統上 `.ini` 。 V1 提供者架構已被取代。 新的提供者應該使用 V2 提供者架構。
- **V2 提供者** 是透過 [效能計數器提供者 api](providing-counter-data-using-version-2-0.md)發佈效能資料的軟體元件。 V2 提供者會透過 `.man` (的 XML 資訊清單) 檔安裝到系統上。

**Counterset** 是提供者內的效能資料群組。 Counterset 具有名稱和一或多個 *計數器*。 從 counterset 收集資料會傳回一些 *實例*。 在某些 Windows api 中，countersets 稱為 **效能物件**。 例如，資料庫系統的效能資料提供者可能會針對每個資料庫統計資料提供一個 counterset。

**計數器** 是單一效能資料片段的定義。 計數器具有名稱和類型。 例如，「每個資料庫統計資料」 counterset 可能包含名為「每秒交易數」的計數器（類型為） `PERF_COUNTER_COUNTER` 。

**實例** 是回報效能資料的實體。 實例的名稱 (字串) 和一或多個 *計數器值*。 例如，「每個資料庫統計資料」 counterset 可能會包含每個資料庫一個實例。 實例名稱會是資料庫名稱，而每個實例都會包含「每秒交易數」、「記憶體使用量」和「磁片使用量」計數器的計數器值。

**計數器值** 是效能計數器資料的單一部分值。 計數器值是不帶正負號的整數，可能是32位或64位，視相對應計數器的類型而定。 當談到 *實例* 時， *計數器值* 有時可能稱為 *計數器* 或 *值*。

> [!TIP]
> 將效能計數器詞彙與更熟悉的試算表詞彙建立關聯可能會很有説明。 **Counterset** 就像資料表一樣。 **計數器** 就像是資料行。 **實例** 就像是一個資料列。 **計數器值** 就像是資料表中的資料格。

**單一實例 countersets** 一律只包含一個實例的資料。 這對報告系統全域統計資料的 countersets 很常見。 例如，Windows 有一個名為「記憶體」的內建單一實例 counterset，可報告全域記憶體使用量。

**多重實例 countersets** 包含變數實例數目的資料。 這種情況很常見，countersets 會報告系統內的實體。 例如，Windows 有一個名為「處理器資訊」的內建多重實例 counterset，可針對每個已安裝的 CPU 報告一個實例。

取用者會定期收集並記錄來自提供者之 counterset 的資料。 例如，取用者可能會每秒收集一次資料，或每分鐘一次。 收集的資料稱為 **範例**。 範例包含時間戳記，以及 counterset 實例的資料。 每個實例的資料包括 (字串) 的實例名稱，以及一組計數器值 (整數，也就是 counterset) 中每個計數器的一個值。

實例名稱在範例中通常應該是唯一的，也就是提供者不應傳回兩個名稱與單一範例一部分相同的實例。 某些較舊的提供者不會遵循此規則，因此取用 [者必須能夠容忍非唯一的實例名稱](handling-duplicate-instance-names.md)。 實例名稱不區分大小寫，因此實例不應該有只有大小寫不同的名稱。

> [!NOTE]
> 基於回溯相容性的理由，"Process" counterset 會根據 EXE 檔案名傳回非唯一的實例名稱。 這可能會導致令人困惑的結果，特別是當具有非唯一名稱的進程啟動或關閉時，因為這通常會因為範例之間的實例名稱不正確而導致資料問題。 「進程」 counterset 的取用者必須能夠容忍這些非唯一的實例名稱和產生的資料問題。

實例名稱在範例之間必須是穩定的，也就是每次收集 counterset 時，提供者應該針對相同的實體使用相同的實例名稱。

每個計數器都有一種類型。 計數器類型指出計數器的 **原始值** 類型 (不帶正負號的32位整數或不帶正負號的64位整數) 。 計數器類型也會指出計數器的原始值代表什麼，以決定應該如何處理原始值來產生有用的統計資料。

雖然某些計數器類型很簡單，且具有直接有用的原始值，但許多計數器類型都需要 [額外的處理](calculating-counter-values.md) ，才能建立有用的 **格式化值**。 若要產生格式化的值，某些計數器類型需要來自兩個樣本的原始值、某些計數器類型需要時間戳記，而某些計數器類型需要來自多個計數器的原始值。 例如：

- `PERF_COUNTER_LARGE_RAWCOUNT` 是64位的原始值，不需要任何處理就能發揮效用。 它適用于時間點值，例如「使用中的記憶體位元組」。
- `PERF_COUNTER_RAWCOUNT_HEX` 是32位的原始值，只需要簡單的十六進位格式才能發揮效用。 它適用于時間點或識別資訊，例如「旗標」或「基底位址」。
- `PERF_COUNTER_BULK_COUNT` 這是64位的原始值，指出事件的計數，並可用來計算事件的發生率。 為了實用，此計數器類型需要兩個以時間分隔的範例。 格式化的值是事件速率，也就是在兩個範例之間的間隔中，事件每秒發生的次數。 假設有兩個範例 `s0` 和 `s1` ， (事件速率) 的格式化值會計算為 `(s1.EventCount - s0.EventCount)/(s1.TimestampInSeconds - s0.TimestampInSeconds)` 。

提供者的行為會如同無狀態，也就是從 counterset 收集資料時，應該不會明顯影響提供者的狀態。 例如，在收集 counterset 時，提供者不應將計數器值重設為0，而且不應該使用先前集合的時間戳記來調整目前集合中的值。 相反地，它應該提供簡單的原始計數器值與精確的類型，讓取用者可以根據原始值和其時間戳記來計算有用的統計資料。

## <a name="performance-api-architecture"></a>效能 API 架構

![效能計數器應用程式會叫用 Windows api 來呼叫提供者，以取得效能資料。](images/architecture.png)

效能計數器取用者包括：

- [Microsoft 提供的應用程式](performance-counters-tools.md) ，例如工作管理員、資源監視器、效能監視器和 typeperf.exe。
- Microsoft 提供的高階 API 介面可公開效能計數器資料，例如 [WMI 效能類別](/windows/desktop/WmiSdk/monitoring-performance-data)。
- 您自己的應用程式或使用 [效能計數器取用者 api](consuming-counter-data.md)的腳本。

大部分的效能計數器取用者都會使用 [PDH.dll](using-the-pdh-functions-to-consume-counter-data.md) 的 api 來收集效能資料。 PDH 管理收集效能計數器的許多複雜層面，例如剖析查詢、比對多個範例中的實例，以及計算原始計數器資料的格式化值。 從 V1 提供者取用資料時，PDH 執行會使用登錄 Api，並在取用 V2 提供者的資料時使用 V2 取用者 Api。

某些較舊的效能計數器取用者會使用登錄 [api](using-the-registry-functions-to-consume-counter-data.md) ，從特殊登錄機碼收集效能資料 `HKEY_PERFORMANCE_DATA` 。 這不建議用於新的程式碼，因為處理來自登錄的資料很複雜，而且容易出錯。 登錄 API 執行直接支援從 V1 提供者收集資料。 它間接支援透過使用 V2 取用者 Api 的轉譯層，從 V2 提供者收集資料。

某些效能計數器取用者會使用 [PerfLib v2 取用者](using-the-perflib-functions-to-consume-counter-data.md) 函式，直接存取 v2 提供者的資料。 這比使用 PDH Api 取用資料更為複雜，但如果 PDH Api 因為效能或相依性的考慮而無法使用，這種方法會很有用。 PerfLib V2 執行可直接支援從 V2 提供者收集資料。 它不支援從 V1 提供者收集資料。

> [!NOTE]
> Windows OneCore 不包含 PDH.dll，而且不包含透過登錄 api 取用效能計數器資料的支援。 在 OneCore 上執行的取用者必須使用 PerfLib V2 取用者函式。

V1 提供者會實作為載入取用者進程的提供者 DLL。 登錄 API 的執行管理載入提供者 DLL、呼叫 DLL 以收集效能資料，以及適當地卸載 DLL。 提供者 DLL 負責[收集適當的效能資料](communicating-with-your-application.md)，例如使用一般的 Windows api、RPC、具名管道、共用記憶體或其他處理序間通訊機制。

V2 提供者會實作為使用者模式程式， (通常是 Windows 服務) 或核心模式驅動程式。 效能資料提供者程式碼通常會直接整合到現有的元件中， (亦即，驅動程式或服務會報告本身) 的相關統計資料。 PerfLib V2 執行會透過 PCW.sys 核心延伸模組來管理要求和回應，因此提供者通常不需要執行任何處理序間通訊來提供效能資料。

> [!NOTE]
> Windows效能計數器 Api 和工具組含有限的支援，可透過適用于 V1 提供者的遠端登入 (（適用于 V1 提供者的遠端登入）來存取其他電腦上的效能計數器) 和)  ( 這項支援通常很難用來驗證控制項， (工具和 Api 只能根據目前的使用者) ，以及 [系統](accessing-remote-counter-data.md) 設定 (依預設) 停用所需的端點和服務來進行驗證。 在許多情況下，最好透過 [WMI](/windows/desktop/WmiSdk/monitoring-performance-data) 存取遠端系統的效能計數器，而不是透過內建的遠端存取支援。

## <a name="developer-audience"></a>開發人員對象

系統管理員通常會使用效能計數器來識別系統的效能問題或異常行為、由開發人員研究軟體元件的資源使用狀況，以及由個別使用者瞭解程式在其系統上的行為。 您可以透過 WMI 和 PowerShell 的腳本，或透過 C/c + + 和 .NET Api，使用 GUI 工具，例如工作管理員或效能監視器、命令列工具（例如 typeperf.exe 或 logman.exe）來進行使用。

效能計數器提供者通常會實作為核心模式驅動程式或使用者模式服務。 效能計數器提供者通常是以 C 或 c + + 撰寫。

## <a name="run-time-requirements"></a>執行階段需求求

如需特定程式設計專案之執行時間需求的詳細資訊，請參閱該元素之 [參考] 頁面的 [需求] 區段。

如需版本歷程記錄，請參閱 [新功能](performance-counters-what-s-new.md)。

## <a name="see-also"></a>另請參閱

[使用效能計數器](using-performance-counters.md)

[效能計數器參考](performance-counters-reference.md)
