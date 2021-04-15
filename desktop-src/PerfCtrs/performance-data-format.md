---
description: RegQueryValueEx 函式所抓取資料的格式是以固定長度的標頭結構（效能 \_ 資料區塊）開始 \_ 。
ms.assetid: a68fa617-834c-4ad9-b922-fac3a648ad75
title: 效能資料格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88029634594843a50fd6010993eb6517dce831f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570643"
---
# <a name="performance-data-format"></a>效能資料格式

[**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa)函式所抓取資料的格式是以固定長度的標頭結構（效能 [**\_ 資料 \_ 區塊**](/windows/desktop/api/Winperf/ns-winperf-perf_data_block)）開始。 效能 **\_ 資料 \_ 區塊** 結構描述系統和效能資料。 效能 **\_ 資料 \_ 區塊** 結構後面會加上可變長度的可變長度物件資料項目。 每個物件專案的標頭包含清單中下一個物件專案的位移。 下圖顯示基本效能資料結構。

![效能資料結構](images/perfdata.png)

物件資料項目有兩種格式：一個支援多個實例，另一個則不支援多個實例。

每個物件資料項目區塊都包含一個效能 [**\_ 物件 \_ 類型**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type) 結構，描述物件的效能資料。 **性能 \_ 物件 \_ 類型** 結構後面接著 [**性能 \_ 計數器 \_ 定義**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition)結構的清單，為物件定義的每個計數器各一個。 對於只有一個實例的物件， **性能 \_ 計數器 \_ 定義** 結構的清單後面會接著一個 [**性能 \_ 計數器 \_ 區塊**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block) 結構，後面接著計數器資料。 每個 **性能 \_ 計數器 \_ 定義** 結構都包含從 **性能 \_ 計數器 \_ 區塊** 結構開始到對應計數器資料的位移。 下圖顯示不支援多個實例的效能物件結構。

![不支援多個實例的效能物件結構](images/perfnoinst.png)

針對支援多個實例的物件類型， [**性能 \_ 計數器 \_ 定義**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) 結構的清單後面會接著實例資訊區塊的清單， (每個實例) 一個。 每個實例資訊區塊都包含一個效能 [**\_ 實例 \_ 定義**](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition) 結構、實例的名稱，以及一個 [**性能 \_ 計數器 \_ 區塊**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block) 結構。 下圖顯示支援兩個實例的效能物件結構。

![支援兩個實例的效能物件結構](images/perfinst.png)

如需使用位移的範例，請參閱 [顯示物件、實例和計數器名稱](displaying-object-instance-and-counter-names.md)。

 

 
