---
title: 使用 PerfLib 函式來取用計數器資料
description: 當無法使用 PDH 時，PerfLib API 函式可用來直接使用 V2 效能計數器資料。
ms.date: 08/17/2020
ms.topic: article
ms.openlocfilehash: 9fec3bb97ec32ff98e2b317b737023da81147bdd
ms.sourcegitcommit: f7cf41ffc79d1ffead9de2fc61677201f94b423a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2020
ms.locfileid: "106969733"
---
# <a name="using-the-perflib-functions-to-consume-counter-data"></a>使用 PerfLib 函式來取用計數器資料

當您無法使用 [效能資料協助程式 (PDH) ](using-the-pdh-functions-to-consume-counter-data.md)函式時，請使用 PerfLib 取用者函數來取用 V2 效能資料提供者的效能資料。 當您撰寫 OneCore 的應用程式來收集 V2 countersets，或當您需要以基本的相依性和額外負荷收集 V2 countersets 時，可能會使用這些函數。

> [!TIP]
> PerfLib V2 取用者函式比效能資料協助程式更難使用 (PDH) 函式，且僅支援從 V2 提供者收集資料。 大部分的應用程式都應該偏好 PDH 函數。

PerfLib V2 取用者函式是用來從 **V2 提供者** 收集資料的低層級 API。 PerfLib V2 取用者函式不支援從 **V1 提供** 者收集資料。

> [!WARNING]
> PerfLib V2 取用者函式可能會從不受信任的來源（例如，從有限許可權的本機服務或從遠端電腦）收集資料。 PerfLib V2 取用者函式不會驗證資料的完整性或一致性。 您可以利用取用者應用程式來確認傳回的資料是否一致，例如傳回的資料區塊中的大小值不會超過所傳回資料區塊的實際大小。 當取用者應用程式以較高的許可權執行時，這一點特別重要。

## <a name="perflib-usage"></a>PerfLib 使用方式

`perflib.h`標頭包含 V2 使用者模式提供者所使用的宣告 (亦即，PerfLib PROVIDER api) 和 v2 取用者 (亦即 PerfLib 取用者 api) 。 它會宣告下列用來取用 V2 效能資料的功能：

- 使用 [**PerfEnumerateCounterSet**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecounterset) 取得系統上 V2 提供者所註冊之 Countersets 的 guid。
- 使用 [**PerfQueryCounterSetRegistrationInfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycountersetregistrationinfo) 來取得特定 counterset 的相關資訊，例如 counterset 的名稱、描述、類型 (單一實例或多重實例) 、計數器類型、計數器名稱和計數器描述。
- 使用 [**PerfEnumerateCounterSetInstances**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecountersetinstances) 取得多重實例 counterset 目前作用中實例的名稱。
- 使用 [**PerfOpenQueryHandle**](/windows/desktop/api/Perflib/nf-perflib-perfopenqueryhandle) 建立新的查詢控制碼，以用於從一個或多個 countersets 收集資料。
- 使用 [**PerfCloseQueryHandle**](/windows/desktop/api/Perflib/nf-perflib-perfclosequeryhandle) 來關閉查詢控制碼。
- 使用 [**PerfAddCounters**](/windows/desktop/api/Perflib/nf-perflib-perfaddcounters) 將查詢加入至查詢控制碼。
- 使用 [**PerfDeleteCounters**](/windows/desktop/api/Perflib/nf-perflib-perfdeletecounters) 從查詢控制碼移除查詢。
- 使用 [**PerfQueryCounterInfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterinfo) 來取得查詢控制碼上目前查詢的相關資訊。
- 使用 [**PerfQueryCounterData**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterdata) 從查詢控制碼收集效能資料。

如果您的取用者只會從 GUID 和計數器索引穩定的特定提供者取用資料，而且您可以從 CTRPP 參數) 存取 [CTRPP](ctrpp.md)產生的符號檔 (`-ch` ，您可以將 counterset GUID 和計數器索引值硬式編碼到您的取用者。

否則，您將需要載入 counterset 中繼資料，以判斷要在查詢中使用的 counterset GUID (s) 和計數器索引，如下所示：

- 使用 **PerfEnumerateCounterSet** 取得支援的 counterset guid 清單。
- 針對每個 GUID，使用 **PerfQueryCounterSetRegistrationInfo** 載入 counterset 名稱。 當您找到您要尋找的名稱時，請停止。
- 使用 **PerfQueryCounterSetRegistrationInfo** 載入其餘的中繼資料 (counterset 設定、計數器名稱、計數器索引、該 counterset) 的計數器類型。

如果您只需要知道 counterset 目前作用中實例的名稱 (亦即，如果您不需要實際的效能資料值) ，您可以使用 **PerfEnumerateCounterSetInstances**。 這會將 counterset GUID 做為輸入，並 `PERF_INSTANCE_HEADER` 傳回具有指定之 counterset 目前作用中實例之名稱和識別碼的區塊。

### <a name="queries"></a>查詢

若要收集效能資料，您必須建立查詢控制碼、將查詢加入至查詢控制碼，然後從查詢收集資料。

查詢控制碼可以有許多相關聯的查詢。 當您針對查詢控制碼呼叫 **PerfQueryCounterData** 時，PerfLib 將會執行所有控制碼的查詢並收集所有的結果。

每個查詢都會指定 counterset GUID、實例名稱篩選、選擇性的實例識別碼篩選，以及選擇性的計數器識別碼篩選。

- 需要 counterset GUID。 指出查詢將從中收集資料之 counterset 的 GUID。 這類似于 `FROM` SQL 查詢的子句。
- 需要實例名稱篩選。 它會指出實例名稱必須符合的萬用字元模式，才能讓實例包含在查詢中， `*` 並指出「任何字元」並指出「 `?` 單一字元」。 若為單一實例 countersets，此值 **必須** 設定為長度為零的字串 `""` 。 若為多重實例 countersets， **必須** 將此設定為非空白字串， (用 `"*"` 來接受) 的所有實例名稱。 這類似于 `WHERE InstanceName LIKE NameFilter` SQL 查詢的子句。
- 實例識別碼篩選是選擇性的。 如果有 (亦即，如果設定為) 以外的值 `0xFFFFFFFF` ，則表示查詢只應收集實例識別碼符合指定識別碼的實例。 如果不存在 (亦即，如果設定為 `0xFFFFFFFF`) ，則表示查詢應接受所有的實例識別碼。 這類似于 `WHERE InstanceId == IdFilter` SQL 查詢的子句。
- 計數器 ID 篩選是選擇性的。 如果有 (亦即，如果設定為) 以外的值 `PERF_WILDCARD_COUNTER` ，則表示查詢應該收集單一計數器，類似于 `SELECT CounterName` SQL 查詢的子句。 如果不存在 (亦即，如果設定為 `PERF_WILDCARD_COUNTER`) ，則表示查詢應該收集所有可用的計數器，類似于 `SELECT *` SQL 查詢的子句。

使用 **PerfAddCounters** 將查詢加入至查詢控制碼。 使用 **PerfDeleteCounters** 從查詢控制碼移除查詢。

變更查詢控制碼中的查詢之後，請使用 **PerfQueryCounterInfo** 來取得查詢索引。 索引會指出 **PerfQueryCounterData** 傳回查詢結果的順序 (結果不會一律符合) 中加入查詢的順序。

查詢控制碼就緒後，請使用 **PerfQueryCounterData** 來收集資料。 您通常會定期收集資料 (一次或一分鐘一次，) 然後視需要處理資料。

> [!NOTE]
> 效能計數器的設計並非每秒收集一次以上。

**PerfQueryCounterData** 會傳回 `PERF_DATA_HEADER` 區塊，其中包含具有時間戳記的資料標頭，後面接著一連串的 `PERF_COUNTER_HEADER` 區塊，每個區塊都包含一個查詢的結果。

`PERF_COUNTER_HEADER`可能包含各種不同的資料類型，如欄位的值所示 `dwType` ：

- `PERF_ERROR_RETURN` -PerfLib 無法從提供者取得有效的計數器資料。
- `PERF_SINGLE_COUNTER` -查詢是單一實例 counterset 中的單一計數器。 結果只會包含要求的計數器值。
- `PERF_MULTIPLE_COUNTERS` -查詢適用于單一實例 counterset 中的多個計數器。 結果包含計數器值，以及用來比對每個值與相對應計數器 (也就是資料行標題) 的資訊。
- `PERF_MULTIPLE_INSTANCES` -查詢來自多重實例 counterset 的單一計數器。 結果會包含實例資訊 (亦即，資料列標題) 和每個實例一個計數器值。
- `PERF_COUNTERSET` -查詢來自多重實例 counterset 的多個計數器。 結果會包含實例資訊 (亦即，資料列標題) 、每個實例的計數器值，以及用來比對每個值與對應計數器的資訊 (例如，資料行標題) 。

**PerfQueryCounterData** 傳回的值為 `UINT32` 或 `UINT64` 原始值。 這些通常需要一些處理來產生所需的格式化值。 必要的處理取決於計數器的型別。 許多計數器類型都需要其他資訊才能完成處理，例如時間戳記或相同樣本中 "base" 計數器的值。

某些計數器類型是「差異」計數器，只有在與上一個範例中的資料相較之下，才有意義。 例如，型別的計數器 `PERF_SAMPLE_COUNTER` 具有格式化的值，此值應該會顯示一個速率， (取樣間隔) 的特定事物每秒發生的次數，但實際的原始值只是 (總計) 中發生特定情況的次數。 若要產生格式化的「速率」值，您必須套用對應至計數器類型的公式。 的公式 `PERF_SAMPLE_COUNTER` 是 `(N1 - N0) / ((T1 - T0) / F)` ：從上一個範例的值減去目前的樣本值， (提供在取樣間隔期間發生事件的次數) 然後將結果除以取樣間隔中的秒數， (從上一個樣本的時間戳記減去目前樣本的時間戳記，並除以 frequency 以將時間範圍轉換成秒) 。

如需有關從原始值計算格式化值的詳細資訊，請參閱 [計算計數器值](calculating-counter-values.md) 。

## <a name="sample"></a>範例

下列程式碼會執行使用 PerfLib V2 取用者函式的取用者，以讀取「處理器資訊」 counterset 的 CPU 效能資訊。

取用者的組織方式如下：

- 類別會實作為 `CpuPerfCounters` 耗用效能資料的邏輯。 它會封裝查詢控制碼，以及記錄查詢結果的資料緩衝區。
- `CpuPerfTimestamp`結構會儲存範例的時間戳記資訊。 每次收集資料時，呼叫端都會收到單一 `CpuPerfTimestamp` 。
- `CpuPerfData`結構會將效能資訊儲存 (實例名稱和原始效能值，) 為一個 CPU。 每次收集資料時，呼叫端會收到 `CpuPerfData` 每個 CPU)  (一個陣列。

此範例會使用硬式編碼的 counterset GUID 和計數器識別碼值，因為它已針對特定 counterset (處理器資訊進行優化，) 不會變更 GUID 或識別碼值。 從任意 countersets 讀取效能資料的更泛型類別，需要使用 **PerfQueryCounterSetRegistrationInfo** 來查閱計數器識別碼和計數器值在執行時間之間的對應。

簡單的 `CpuPerfCountersConsumer.cpp` 程式會顯示如何使用類別中的值 `CpuPerfCounters` 。

### <a name="cpuperfcountersh"></a>CpuPerfCounters。h

```cpp
#pragma once
#include <sal.h>

// Contains timestamp data for a Processor Information data collection.
struct CpuPerfTimestamp
{
    __int64 PerfTimeStamp;   // Timestamp from the high-resolution clock.
    __int64 PerfTime100NSec; // The number of 100 nanosecond intervals since January 1, 1601, in Coordinated Universal Time (UTC).
    __int64 PerfFreq;        // The frequency of the high-resolution clock.
};

// Contains the raw data from a Processor Information sample.
// Note that the values returned are raw data. Converting from raw data to a
// friendly value may require computation, and the computation may require
// two samples of data. The computation depends on the Type, and the formula
// to use for each type can be found on MSDN.
// For example, ProcessorTime contains raw data of type PERF_100NSEC_TIMER_INV.
// Given two samples of data, s0 at time t0 and s1 at time t1, the friendly
// "% Processor Time" value is computed as:
// 100*(1-(s1.ProcessorTime-s0.ProcessorTime)/(t1.PerfTime100NSec-t0.PerfTime100NSec))
struct CpuPerfData
{
    wchar_t Name[16]; // Format: "NumaNode,NumaIndex", "NumaNode,_Total", or "_Total".
    __int64 unsigned ProcessorTime; // % Processor Time (#0, Type=PERF_100NSEC_TIMER_INV)
    __int64 unsigned UserTime; // % User Time (#1, Type=PERF_100NSEC_TIMER)
    __int64 unsigned PrivilegedTime; // % Privileged Time (#2, Type=PERF_100NSEC_TIMER)
    __int32 unsigned Interrupts; // Interrupts / sec (#3, Type=PERF_COUNTER_COUNTER)
    __int64 unsigned DpcTime; // % DPC Time (#4, Type=PERF_100NSEC_TIMER)
    __int64 unsigned InterruptTime; // % Interrupt Time (#5, Type=PERF_100NSEC_TIMER)
    __int32 unsigned DpcsQueued; // DPCs Queued / sec (#6, Type=PERF_COUNTER_COUNTER)
    __int32 unsigned Dpcs; // DPC Rate (#7, Type=PERF_COUNTER_RAWCOUNT)
    __int64 unsigned IdleTime; // % Idle Time (#8, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C1Time; // % C1 Time (#9, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C2Time; // % C2 Time (#10, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C3Time; // % C3 Time (#11, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C1Transitions; // C1 Transitions / sec (#12, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned C2Transitions; // C2 Transitions / sec (#13, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned C3Transitions; // C3 Transitions / sec (#14, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned PriorityTime; // % Priority Time (#15, Type=PERF_100NSEC_TIMER_INV)
    __int32 unsigned ParkingStatus; // Parking Status (#16, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned ProcessorFrequency; // Processor Frequency (#17, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned PercentMaximumFrequency; // % of Maximum Frequency (#18, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned ProcessorStateFlags; // Processor State Flags (#19, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned ClockInterrupts; // Clock Interrupts / sec (#20, Type=PERF_COUNTER_COUNTER)
    __int64 unsigned AverageIdleTime; // Average Idle Time (#21, Type=PERF_PRECISION_100NS_TIMER)
    __int64 unsigned AverageIdleTimeBase; // Average Idle Time Base (#22, Type=PERF_PRECISION_TIMESTAMP)
    __int64 unsigned IdleBreakEvents; // Idle Break Events / sec (#23, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned ProcessorPerformance; // % Processor Performance (#24, Type=PERF_AVERAGE_BULK)
    __int32 unsigned ProcessorPerformanceBase; // % Processor Performance Base (#25, Type=PERF_AVERAGE_BASE)
    __int64 unsigned ProcessorUtility; // % Processor Utility (#26, Type=PERF_AVERAGE_BULK)
    __int64 unsigned PrivilegedUtility; // % Privileged Utility (#28, Type=PERF_AVERAGE_BULK)
    __int32 unsigned UtilityBase; // % Utility Base (#27, Type=PERF_AVERAGE_BASE)
    __int32 unsigned PercentPerformanceLimit; // % Performance Limit (#30, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned PerformanceLimitFlags; // Performance Limit Flags (#31, Type=PERF_COUNTER_RAWCOUNT)
};

// Performs data collection from the Processor Information performance counter.
class CpuPerfCounters
{
public:

    CpuPerfCounters(CpuPerfCounters const&) = delete;
    void operator=(CpuPerfCounters const&) = delete;

    ~CpuPerfCounters();
    CpuPerfCounters() noexcept;

    // Reads CPU performance counter data.
    // Returns ERROR_SUCCESS (0) on success, ERROR_MORE_DATA if bufferCount is
    // too small, or another Win32 error code on failure.
    _Success_(return == 0)
    unsigned
    ReadData(
        _Out_opt_ CpuPerfTimestamp* timestamp,
        _Out_cap_post_count_(bufferCount, *bufferUsed) CpuPerfData* buffer,
        unsigned bufferCount,
        _Out_ unsigned* bufferUsed) noexcept;

private:

    void* m_hQuery;
    void* m_pData;
    unsigned m_cbData;
};
```

### <a name="cpuperfcounterscpp"></a>CpuPerfCounters .cpp

```cpp
#include "CpuPerfCounters.h"
#include <windows.h>
#include <perflib.h>
#include <winperf.h>
#include <stdlib.h>

_Check_return_ _Ret_maybenull_ _Post_writable_byte_size_(cb)
static void*
AllocateBytes(unsigned cb) noexcept
{
    return malloc(cb);
}

static void
FreeBytes(_Pre_maybenull_ _Post_invalid_ void* p) noexcept
{
    if (p)
    {
        free(p);
    }
    return;
}

static void
AssignCounterValue(
    _Inout_ __int32 unsigned* pVar,
    _In_ PERF_COUNTER_DATA const* pData) noexcept
{
    if (pData->dwDataSize == 4 ||
        pData->dwDataSize == 8)
    {
        *pVar = *reinterpret_cast<__int32 unsigned const*>(pData + 1);
    }
}

static void
AssignCounterValue(
    _Inout_ __int64 unsigned* pVar,
    _In_ PERF_COUNTER_DATA const* pData) noexcept
{
    if (pData->dwDataSize == 8)
    {
        *pVar = *reinterpret_cast<__int64 unsigned const*>(pData + 1);
    }
    else if (pData->dwDataSize == 4)
    {
        *pVar = *reinterpret_cast<__int32 unsigned const*>(pData + 1);
    }
}

CpuPerfCounters::~CpuPerfCounters()
{
    if (m_hQuery)
    {
        PerfCloseQueryHandle(m_hQuery);
    }

    FreeBytes(m_pData);
}

CpuPerfCounters::CpuPerfCounters() noexcept
    : m_hQuery()
    , m_pData()
    , m_cbData()
{
    return;
}

_Success_(return == 0)
unsigned
CpuPerfCounters::ReadData(
    _Out_opt_ CpuPerfTimestamp* timestamp,
    _Out_cap_post_count_(bufferCount, *bufferUsed) CpuPerfData* buffer,
    unsigned bufferCount,
    _Out_ unsigned* bufferUsed) noexcept
{
    unsigned status;
    DWORD cbData;
    PERF_DATA_HEADER* pDataHeader;
    PERF_COUNTER_HEADER const* pCounterHeader;
    PERF_MULTI_COUNTERS const* pMultiCounters;
    PERF_MULTI_INSTANCES const* pMultiInstances;
    PERF_INSTANCE_HEADER const* pInstanceHeader;
    unsigned cInstances = 0;

    if (m_hQuery == nullptr)
    {
        HANDLE hQuery = 0;
        status = PerfOpenQueryHandle(nullptr, &hQuery);
        if (ERROR_SUCCESS != status)
        {
            goto Done;
        }

        struct
        {
            PERF_COUNTER_IDENTIFIER Identifier;
            WCHAR Name[4];
        } querySpec = {
            {
                // ProcessorCounterSetGuid
                { 0xb4fc721a, 0x378, 0x476f, 0x89, 0xba, 0xa5, 0xa7, 0x9f, 0x81, 0xb, 0x36 },
                0,
                sizeof(querySpec),
                PERF_WILDCARD_COUNTER, // Get all data for each CPU.
                0xFFFFFFFF // Get data for all instance IDs.
            },
            L"*" // Get data for all instance names.
        };

        status = PerfAddCounters(hQuery, &querySpec.Identifier, sizeof(querySpec));
        if (ERROR_SUCCESS == status)
        {
            status = querySpec.Identifier.Status;
        }

        if (ERROR_SUCCESS != status)
        {
            PerfCloseQueryHandle(hQuery);
            goto Done;
        }

        // NOTE: A program that adds more than one query to the handle would need to call
        // PerfQueryCounterInfo to determine the order of the query results.

        m_hQuery = hQuery;
    }

    for (;;)
    {
        cbData = 0;
        pDataHeader = static_cast<PERF_DATA_HEADER*>(m_pData);
        status = PerfQueryCounterData(m_hQuery, pDataHeader, m_cbData, &cbData);
        if (ERROR_SUCCESS == status)
        {
            break;
        }
        else if (ERROR_NOT_ENOUGH_MEMORY != status)
        {
            goto Done;
        }

        FreeBytes(m_pData);
        m_cbData = 0;

        m_pData = AllocateBytes(cbData);
        if (nullptr == m_pData)
        {
            status = ERROR_OUTOFMEMORY;
            goto Done;
        }

        m_cbData = cbData;
    }

    // PERF_DATA_HEADER block = PERF_DATA_HEADER + dwNumCounters PERF_COUNTER_HEADER blocks
    if (cbData < sizeof(PERF_DATA_HEADER) ||
        cbData < pDataHeader->dwTotalSize ||
        pDataHeader->dwTotalSize < sizeof(PERF_DATA_HEADER) ||
        pDataHeader->dwNumCounters != 1)
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    // PERF_COUNTERSET block = PERF_COUNTER_HEADER + PERF_MULTI_COUNTERS block + PERF_MULTI_INSTANCES block
    cbData = pDataHeader->dwTotalSize - sizeof(PERF_DATA_HEADER);
    pCounterHeader = reinterpret_cast<PERF_COUNTER_HEADER*>(pDataHeader + 1);
    if (cbData < sizeof(PERF_COUNTER_HEADER) ||
        cbData < pCounterHeader->dwSize ||
        pCounterHeader->dwSize < sizeof(PERF_COUNTER_HEADER) ||
        PERF_COUNTERSET != pCounterHeader->dwType)
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    // PERF_MULTI_COUNTERS block = PERF_MULTI_COUNTERS + dwCounters DWORDs
    cbData = pCounterHeader->dwSize - sizeof(PERF_COUNTER_HEADER);
    pMultiCounters = reinterpret_cast<PERF_MULTI_COUNTERS const*>(pCounterHeader + 1);
    if (cbData < sizeof(PERF_MULTI_COUNTERS) ||
        cbData < pMultiCounters->dwSize ||
        pMultiCounters->dwSize < sizeof(PERF_MULTI_COUNTERS) ||
        (pMultiCounters->dwSize - sizeof(PERF_MULTI_COUNTERS)) / sizeof(DWORD) < pMultiCounters->dwCounters)
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    // PERF_MULTI_INSTANCES block = PERF_MULTI_INSTANCES + dwInstances instance data blocks
    cbData -= pMultiCounters->dwSize;
    pMultiInstances = reinterpret_cast<PERF_MULTI_INSTANCES const*>((LPCBYTE)pMultiCounters + pMultiCounters->dwSize);
    if (cbData < sizeof(PERF_MULTI_INSTANCES) ||
        cbData < pMultiInstances->dwTotalSize ||
        pMultiInstances->dwTotalSize < sizeof(PERF_MULTI_INSTANCES))
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    cInstances = pMultiInstances->dwInstances;
    if (bufferCount < cInstances)
    {
        status = ERROR_MORE_DATA;
        goto Done;
    }

    memset(buffer, 0, sizeof(buffer[0]) * cInstances);

    cbData = pMultiInstances->dwTotalSize - sizeof(PERF_MULTI_INSTANCES);
    pInstanceHeader = reinterpret_cast<PERF_INSTANCE_HEADER const*>(pMultiInstances + 1);
    for (unsigned iInstance = 0; iInstance != pMultiInstances->dwInstances; iInstance += 1)
    {
        CpuPerfData& d = buffer[iInstance];

        // instance data block = PERF_INSTANCE_HEADER block + dwCounters PERF_COUNTER_DATA blocks
        if (cbData < sizeof(PERF_INSTANCE_HEADER) ||
            cbData < pInstanceHeader->Size ||
            pInstanceHeader->Size < sizeof(PERF_INSTANCE_HEADER))
        {
            status = ERROR_INVALID_DATA;
            goto Done;
        }

        unsigned const instanceNameMax = (pInstanceHeader->Size - sizeof(PERF_INSTANCE_HEADER)) / sizeof(WCHAR);
        WCHAR const* const instanceName = reinterpret_cast<WCHAR const*>(pInstanceHeader + 1);
        if (instanceNameMax == wcsnlen(instanceName, instanceNameMax))
        {
            status = ERROR_INVALID_DATA;
            goto Done;
        }

        wcsncpy_s(d.Name, instanceName, _TRUNCATE);

        cbData -= pInstanceHeader->Size;
        PERF_COUNTER_DATA const* pCounterData = reinterpret_cast<PERF_COUNTER_DATA const*>((LPCBYTE)pInstanceHeader + pInstanceHeader->Size);
        for (unsigned iCounter = 0; iCounter != pMultiCounters->dwCounters; iCounter += 1)
        {
            if (cbData < sizeof(PERF_COUNTER_DATA) ||
                cbData < pCounterData->dwSize ||
                pCounterData->dwSize < sizeof(PERF_COUNTER_DATA) + 8 ||
                pCounterData->dwSize - sizeof(PERF_COUNTER_DATA) < pCounterData->dwDataSize)
            {
                status = ERROR_INVALID_DATA;
                goto Done;
            }

            DWORD const* pCounterIds = reinterpret_cast<DWORD const*>(pMultiCounters + 1);
            switch (pCounterIds[iCounter])
            {
            case 0: // PERF_100NSEC_TIMER_INV
                AssignCounterValue(&d.ProcessorTime, pCounterData);
                break;
            case 1: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.UserTime, pCounterData);
                break;
            case 2: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.PrivilegedTime, pCounterData);
                break;
            case 3: // PERF_COUNTER_COUNTER
                AssignCounterValue(&d.Interrupts, pCounterData);
                break;
            case 4: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.DpcTime, pCounterData);
                break;
            case 5: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.InterruptTime, pCounterData);
                break;
            case 6: // PERF_COUNTER_COUNTER
                AssignCounterValue(&d.DpcsQueued, pCounterData);
                break;
            case 7: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.Dpcs, pCounterData);
                break;
            case 8: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.IdleTime, pCounterData);
                break;
            case 9: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.C1Time, pCounterData);
                break;
            case 10: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.C2Time, pCounterData);
                break;
            case 11: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.C3Time, pCounterData);
                break;
            case 12: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.C1Transitions, pCounterData);
                break;
            case 13: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.C2Transitions, pCounterData);
                break;
            case 14: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.C3Transitions, pCounterData);
                break;
            case 15: // PERF_100NSEC_TIMER_INV
                AssignCounterValue(&d.PriorityTime, pCounterData);
                break;
            case 16: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.ParkingStatus, pCounterData);
                break;
            case 17: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.ProcessorFrequency, pCounterData);
                break;
            case 18: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.PercentMaximumFrequency, pCounterData);
                break;
            case 19: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.ProcessorStateFlags, pCounterData);
                break;
            case 20: // PERF_COUNTER_COUNTER
                AssignCounterValue(&d.ClockInterrupts, pCounterData);
                break;
            case 21: // PERF_PRECISION_100NS_TIMER
                AssignCounterValue(&d.AverageIdleTime, pCounterData);
                break;
            case 22: // PERF_PRECISION_TIMESTAMP
                AssignCounterValue(&d.AverageIdleTimeBase, pCounterData);
                break;
            case 23: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.IdleBreakEvents, pCounterData);
                break;
            case 24: // PERF_AVERAGE_BULK
                AssignCounterValue(&d.ProcessorPerformance, pCounterData);
                break;
            case 25: // PERF_AVERAGE_BASE
                AssignCounterValue(&d.ProcessorPerformanceBase, pCounterData);
                break;
            case 26: // PERF_AVERAGE_BULK
                AssignCounterValue(&d.ProcessorUtility, pCounterData);
                break;
            case 28: // PERF_AVERAGE_BULK
                AssignCounterValue(&d.PrivilegedUtility, pCounterData);
                break;
            case 27: // PERF_AVERAGE_BASE
                AssignCounterValue(&d.UtilityBase, pCounterData);
                break;
            case 30: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.PercentPerformanceLimit, pCounterData);
                break;
            case 31: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.PerformanceLimitFlags, pCounterData);
                break;
            }

            cbData -= pCounterData->dwSize;
            pCounterData = reinterpret_cast<PERF_COUNTER_DATA const*>((LPCBYTE)pCounterData + pCounterData->dwSize);
        }

        pInstanceHeader = reinterpret_cast<PERF_INSTANCE_HEADER const*>(pCounterData);
    }

    if (nullptr != timestamp)
    {
        timestamp->PerfTimeStamp = pDataHeader->PerfTimeStamp;
        timestamp->PerfTime100NSec = pDataHeader->PerfTime100NSec;
        timestamp->PerfFreq = pDataHeader->PerfFreq;
    }

    status = ERROR_SUCCESS;

Done:

    *bufferUsed = cInstances;
    return status;
}
```

### <a name="cpuperfcountersconsumercpp"></a>CpuPerfCountersConsumer .cpp

```cpp
#include <windows.h>
#include <stdio.h>
#include "CpuPerfCounters.h"
#include <utility>

int wmain()
{
    unsigned status;
    unsigned const dataMax = 30; // Support up to 30 instances
    CpuPerfCounters cpc;
    CpuPerfTimestamp timestamp[2];
    CpuPerfTimestamp* t0 = timestamp + 0;
    CpuPerfTimestamp* t1 = timestamp + 1;
    CpuPerfData data[dataMax * 2];
    CpuPerfData* d0 = data + 0;
    CpuPerfData* d1 = data + dataMax;
    unsigned used;

    status = cpc.ReadData(t0, d0, dataMax, &used);
    printf("ReadData0 used=%u, status=%u\n", used, status);

    for (unsigned iSample = 1; iSample != 10; iSample += 1)
    {
        Sleep(1000);
        status = cpc.ReadData(t1, d1, dataMax, &used);
        printf("ReadData%u used=%u, status=%u\n", iSample, used, status);

        if (status == ERROR_SUCCESS && used != 0)
        {
            // Show the ProcessorTime value from instance #0 (usually the "_Total" instance):
            auto& s0 = d0[0];
            auto& s1 = d1[0];
            printf("  %ls/%ls = %f\n", s0.Name, s1.Name,
                100.0 * (1.0 - static_cast<double>(s1.ProcessorTime - s0.ProcessorTime) / static_cast<double>(t1->PerfTime100NSec - t0->PerfTime100NSec)));

            std::swap(t0, t1); // Swap "current" and "previous" timestamp pointers.
            std::swap(d0, d1); // Swap "current" and "previous" sample pointers.
        }
    }

    return status;
}
```
