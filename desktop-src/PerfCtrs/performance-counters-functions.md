---
description: 使用下列函數來取用和提供效能資料。
ms.assetid: a2c97b8b-b1b1-4dd8-8f23-edffaa74d028
title: 效能計數器函式
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 8ef01ac07ae8507f1005839ab838e2528e76d6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969360"
---
# <a name="performance-counters-functions"></a>效能計數器函式

使用下列函數來取用和提供效能資料。

## <a name="consumer-functions"></a>取用者函式

### <a name="performance-data-helper-pdh-functions"></a>效能資料協助程式 (PDH) 函數

使用效能資料協助程式 (PDH) 函式來取用 V1 和 V2 效能資料提供者的效能資料。

> [!Note]
> Windows OneCore 的應用程式無法使用 PDH 函數。 如果您正在撰寫 Windows OneCore 的應用程式，請使用 [PerfLib V2 取用者](using-the-perflib-functions-to-consume-counter-data.md)函式。

- [*CounterPathCallBack*](/windows/desktop/api/Pdh/nc-pdh-counterpathcallback)
- [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera)
- [**PdhAddEnglishCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddenglishcountera)
- [**PdhBindInputDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea)
- [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa)
- [**PdhBrowseCountersH**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersha)
- [**PdhCalculateCounterFromRawValue**](/windows/desktop/api/Pdh/nf-pdh-pdhcalculatecounterfromrawvalue)
- [**PdhCloseLog**](/windows/desktop/api/Pdh/nf-pdh-pdhcloselog)
- [**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
- [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)
- [**PdhCollectQueryDataEx**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydataex)
- [**PdhCollectQueryDataWithTime**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydatawithtime)
- [**PdhComputeCounterStatistics**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics)
- [**PdhConnectMachine**](/windows/desktop/api/Pdh/nf-pdh-pdhconnectmachinea)
- [**PdhEnumLogSetNames**](/windows/desktop/api/Pdh/nf-pdh-pdhenumlogsetnamesa)
- [**PdhEnumMachines**](/windows/desktop/api/Pdh/nf-pdh-pdhenummachinesa)
- [**PdhEnumMachinesH**](/windows/desktop/api/Pdh/nf-pdh-pdhenummachinesha)
- [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa)
- [**PdhEnumObjectItemsH**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsha)
- [**PdhEnumObjects**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa)
- [**PdhEnumObjectsH**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsha)
- [**PdhExpandCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandcounterpatha)
- [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha)
- [**PdhExpandWildCardPathH**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpathha)
- [**PdhFormatFromRawValue**](/windows/desktop/api/Pdh/nf-pdh-pdhformatfromrawvalue)
- [**PdhGetCounterInfo**](/windows/desktop/api/Pdh/nf-pdh-pdhgetcounterinfoa)
- [**PdhGetCounterTimeBase**](/windows/desktop/api/Pdh/nf-pdh-pdhgetcountertimebase)
- [**PdhGetDataSourceTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea)
- [**PdhGetDataSourceTimeRangeH**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangeh)
- [**PdhGetDefaultPerfCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfcountera)
- [**PdhGetDefaultPerfCounterH**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfcounterha)
- [**PdhGetDefaultPerfObject**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfobjecta)
- [**PdhGetDefaultPerfObjectH**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdefaultperfobjectha)
- [**PdhGetDllVersion**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdllversion)
- [**PdhGetFormattedCounterArray**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcounterarraya)
- [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue)
- [**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
- [**PdhGetRawCounterArray**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcounterarraya)
- [**PdhGetRawCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue)
- [**PdhIsRealTimeQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhisrealtimequery)
- [**PdhLookupPerfIndexByName**](/windows/desktop/api/Pdh/nf-pdh-pdhlookupperfindexbynamea)
- [**PdhLookupPerfNameByIndex**](/windows/desktop/api/Pdh/nf-pdh-pdhlookupperfnamebyindexa)
- [**PdhMakeCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhmakecounterpatha)
- [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)
- [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya)
- [**PdhOpenQueryH**](/windows/desktop/api/Pdh/nf-pdh-pdhopenqueryh)
- [**PdhParseCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha)
- [**PdhParseInstanceName**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea)
- [**PdhReadRawLogRecord**](/windows/desktop/api/Pdh/nf-pdh-pdhreadrawlogrecord)
- [**PdhRemoveCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)
- [**PdhSelectDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhselectdatasourcea)
- [**PdhSetCounterScaleFactor**](/windows/desktop/api/Pdh/nf-pdh-pdhsetcounterscalefactor)
- [**PdhSetDefaultRealTimeDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhsetdefaultrealtimedatasource)
- [**PdhSetQueryTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange)
- [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
- [**PdhUpdateLogFileCatalog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdatelogfilecatalog)
- [**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha)
- [**PdhValidatePathEx**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepathexa)

### <a name="perflib-v2-consumer-functions"></a>PerfLib V2 取用者函式

如果您無法使用效能資料協助程式 (PDH) 函數，請使用 PerfLib V2 取用者函式來取用 V2 效能資料提供者的效能資料。 當您撰寫 OneCore 的應用程式來收集 V2 countersets，或當您需要以基本的相依性和額外負荷收集特定 V2 countersets 時，可能會使用這些函數。

> [!TIP]
> PerfLib V2 取用者函式比效能資料協助程式更難使用 (PDH) 函式，且僅支援從 V2 提供者收集資料。 大部分的應用程式都應該偏好 PDH 函數。

- [**PerfAddCounters**](/windows/desktop/api/Perflib/nf-perflib-perfaddcounters)
- [**PerfCloseQueryHandle**](/windows/desktop/api/Perflib/nf-perflib-perfclosequeryhandle)
- [**PerfDeleteCounters**](/windows/desktop/api/Perflib/nf-perflib-perfdeletecounters)
- [**PerfEnumerateCounterSet**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecounterset)
- [**PerfEnumerateCounterSetInstances**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecountersetinstances)
- [**PerfOpenQueryHandle**](/windows/desktop/api/Perflib/nf-perflib-perfopenqueryhandle)
- [**PerfQueryCounterData**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterdata)
- [**PerfQueryCounterInfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterinfo)
- [**PerfQueryCounterSetRegistrationInfo**](/windows/desktop/api/Perflib/nf-perflib-perfquerycountersetregistrationinfo)

## <a name="provider-functions"></a>提供者函式

### <a name="perflib-v2-provider-functions"></a>PerfLib V2 提供者函式

[V2 效能資料提供者](providing-counter-data-using-version-2-0.md) 使用下列功能：

- [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc)
- [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [**CounterCleanup**](countercleanup.md)
- [**CounterInitialize**](counterinitialize.md)
- [*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free)
- [**PerfCreateInstance**](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [**PerfDecrementULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulongcountervalue)
- [**PerfDecrementULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfdecrementulonglongcountervalue)
- [**PerfDeleteInstance**](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [**PerfIncrementULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue)
- [**PerfIncrementULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfincrementulonglongcountervalue)
- [**PerfQueryInstance**](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [**PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [**PerfSetULongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [**PerfSetULongLongCounterValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [**PerfSetCounterRefValue**](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [**PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [**PerfStartProviderEx**](/windows/desktop/api/Perflib/nf-perflib-perfstartproviderex)
- [**PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

> [!Note]
> 若要安裝和卸載 V2 提供者，請使用 **lodctr** 和 **unlodctr** 工具。 **LoadPerfCounterTextStrings** 和 **UnloadPerfCounterTextStrings** 函數不能用來安裝和卸載 V2 提供者。

### <a name="performance-dll-functions"></a>效能 DLL 函數

[V1 效能資料提供者](providing-counter-data-using-a-performance-dll.md) 會執行提供下列功能的 DLL：

- [*ClosePerformanceData*](/windows/win32/api/winperf/nc-winperf-pm_close_proc)
- [*CollectPerformanceData*](/windows/win32/api/winperf/nc-winperf-pm_collect_proc)
- [*OpenPerformanceData*](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))

> [!Note]
> 由於有顯著的效能和可靠性問題，因此 V1 效能資料提供者已被取代。 雖然您仍然可以使用效能擴充 DLL 來提供計數器資料，但建議您改為 [建立 V2 提供者](providing-counter-data-using-version-2-0.md) 。 您也鼓勵您將現有的 V1 提供者取代為 V2 提供者。

您可以使用 **lodctr** 和 **unlodctr** 工具，或藉由呼叫下列函式，來安裝和卸載 V1 提供者：

- [**LoadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-loadperfcountertextstringsa)
- [**UnloadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa)
