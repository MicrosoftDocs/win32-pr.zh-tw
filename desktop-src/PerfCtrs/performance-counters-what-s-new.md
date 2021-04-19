---
description: 本節說明每個版本的效能計數器已新增的新功能。
ms.assetid: 14bdae6c-9dcd-401e-8c43-5391e00cf7e3
title: " (效能計數器的新) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0c1189a185351eabae438a01c6f111952f164e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983493"
---
# <a name="whats-new-with-performance-counters"></a>效能計數器的新功能

本節說明每個版本的效能計數器已新增的新功能。

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 與 Windows Server 2008 R2

[CTRPP](ctrpp.md)工具已變更，可改善和簡化程式碼產生。 此工具現在只會產生標頭和資源檔。 如果您想要使用舊的程式碼產生行為 (不建議) ，您可以使用新的 `-legacy` 引數。

- 您現在必須指定新的 `-o` 和 `-rc` 引數，分別指定標頭和資源檔的名稱和位置。
- 您可以使用選擇性的 new `-prefix` 引數，指定要加入至在產生的標頭檔中定義的全域變數和函數開頭的字串。
- 如果您必須更新您的計數器資訊清單，使用新的程式碼產生時，就不需要將先前的回呼實作為新產生的程式碼，因為這些回呼不再包含在產生的程式碼中。

`symbol`下列資訊清單元素可使用新的屬性：

- [供應商](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element)
- [counterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)
- [計數器](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element)

`symbol`[提供者](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element)和[counterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)需要屬性，而且對[counter](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element)而言是選擇性的。 屬性可讓您提供符號名稱，讓您在呼叫提供者函式時，用來參考每個元素 (例如，您可以在呼叫 [PerfCreateInstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)) 時使用計數器集合符號名稱。

## <a name="windows-vista"></a>Windows Vista

在此版本中，提供計數器資料的效能計數器架構已完全變更。

先前，您已使用 INI 檔案定義您的計數器資料，並已執行可在取用者的進程中執行的效能 DLL，以在取用者要求時提供資料。 此架構已被取代，不建議用於新的程式碼，因為會有顯著的效能和可靠性問題。

新的架構會使用資訊清單來定義計數器資料，並在提供者的進程中執行程式碼，以在取用者要求時提供資料。 如需其他詳細資訊，請參閱 [使用2.0 版提供計數器資料](providing-counter-data-using-version-2-0.md)。

此版本已新增下列函式：

- [ControlCallback](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [PerfCreateInstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [PerfDeleteInstance](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [PerfQueryInstance](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [PerfSetCounterSetInfo](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [PerfSetULongCounterValue](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [PerfSetULongLongCounterValue](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [PerfSetCounterRefValue](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [PerfStartProvider](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [PerfStopProvider](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

此版本已新增下列結構：

- [性能 \_ 計數器身分 \_ 識別](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [性能 \_ 計數器 \_ 資訊](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [效能 \_ COUNTERSET \_ 資訊](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [效能 \_ COUNTERSET \_ 實例](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)

如需您在資訊清單中用來定義計數器的 XML 元素清單，請參閱 [效能計數器架構](performance-counters-schema.md)。

如需有關剖析資訊清單並產生您作為提供者起點之程式碼的 CTRPP 前置處理器工具的詳細資訊，請參閱 [CTRPP](ctrpp.md)。
