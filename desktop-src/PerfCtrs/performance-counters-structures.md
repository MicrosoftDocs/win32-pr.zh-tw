---
description: 使用效能資料時，您會使用下列結構。
ms.assetid: 97118b64-3a2f-49c0-92e7-324df08bdb12
title: 效能計數器結構
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 00e9a505a9fe74592f571f3db108af2247a6d44889bc3ddbc2e4dae0844600b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674748"
---
# <a name="performance-counters-structures"></a>效能計數器結構

使用效能資料時，您會使用下列結構。

如需有關使用效能計數器之函式的詳細資訊，請參閱 [效能計數器函數](performance-counters-functions.md)。

## <a name="performance-data-helper-pdh-structures"></a>效能資料協助程式 (PDH) 結構

使用 [效能資料協助程式 (PDH) ](using-the-pdh-functions-to-consume-counter-data.md) 函數的取用者會使用下列結構：

- [**PDH \_ 流覽 \_ DLG \_ 設定**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a)
- [**PDH \_ 流覽 \_ DLG \_ 設定 \_ H**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_ha)
- [**PDH \_ 計數器 \_ 資訊**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_info_a)
- [**PDH \_ 計數器 \_ 路徑 \_ 元素**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a)
- [**PDH \_ 資料項目 \_ \_ 路徑專案 \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_data_item_path_elements_a)
- [**PDH \_ BCP.FMT \_ COUNTERVALUE**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue)
- [**PDH \_ BCP.FMT \_ COUNTERVALUE \_ 專案**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue_item_a)
- [**PDH \_ 原始 \_ 計數器**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)
- [**PDH \_ 原始 \_ 計數器 \_ 專案**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter_item_a)
- [**PDH \_ 原始 \_ 記錄檔 \_ 記錄**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_log_record)
- [**PDH \_ 統計資料**](/windows/desktop/api/Pdh/ns-pdh-pdh_statistics)
- [**PDH \_ 時間 \_ 資訊**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info)

## <a name="perflib-v2-consumer-structures"></a>PerfLib V2 取用者結構

使用 [PerfLib V2 取用者](using-the-perflib-functions-to-consume-counter-data.md) 函式的取用者會使用下列結構：

- [**性能 \_ 計數器 \_ 資料**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_data)
- [**性能 \_ 計數器 \_ 標頭**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_header)
- [**性能 \_ 計數器 \_ 識別碼**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identifier)
- [**性能 \_ 計數器 \_ REG \_ INFO**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_reg_info)
- [**效能 \_ COUNTERSET \_ REG \_ 資訊**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_reg_info)
- [**效能 \_ 資料 \_ 標頭**](/windows/desktop/api/Perflib/ns-perflib-perf_data_header)
- [**效能 \_ 實例 \_ 標頭**](/windows/desktop/api/Perflib/ns-perflib-perf_instance_header)
- [**效能 \_ 多重 \_ 計數器**](/windows/desktop/api/Perflib/ns-perflib-perf_multi_counters)
- [**效能 \_ 多重 \_ 實例**](/windows/desktop/api/Perflib/ns-perflib-perf_multi_instances)
- [**效能 \_ 字串 \_ 緩衝區 \_ 標頭**](/windows/win32/api/perflib/ns-perflib-perf_string_buffer_header)
- [**效能 \_ 字串 \_ 計數器 \_ 標頭**](/windows/win32/api/perflib/ns-perflib-perf_string_counter_header)

## <a name="perflib-v2-provider-structures"></a>PerfLib V2 提供者結構

[V2 效能資料提供者](providing-counter-data-using-version-2-0.md) 會使用下列結構：

- [**性能 \_ 計數器身分 \_ 識別**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [**性能 \_ 計數器 \_ 資訊**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [**效能 \_ COUNTERSET \_ 資訊**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [**效能 \_ COUNTERSET \_ 實例**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)
- [**效能 \_ 提供者 \_ 內容**](/windows/win32/api/perflib/ns-perflib-perf_provider_context)

## <a name="performance-dll-structures"></a>效能 DLL 結構

使用登錄函式[來取用計數器資料](using-the-registry-functions-to-consume-counter-data.md)的[效能擴充 DLL 提供](providing-counter-data-using-a-performance-dll.md)者和取用者會使用下列結構：

- [**性能 \_ 計數器 \_ 區塊**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block)
- [**性能 \_ 計數器 \_ 定義**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition)
- [**效能 \_ 資料 \_ 區塊**](/windows/desktop/api/Winperf/ns-winperf-perf_data_block)
- [**效能 \_ 實例 \_ 定義**](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition)
- [**性能 \_ 物件 \_ 類型**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type)
