---
description: 您可以使用 PDH 函數來收集效能資料。
ms.assetid: 2510480e-cfea-4f7c-af0b-6d229c150c91
title: 使用 PDH 函數來使用計數器資料
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 6c506e3c7a73a94a6bc3c282920e17504e28dedb42e0e3bee8a6f05a1e77ebbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033188"
---
# <a name="using-the-pdh-functions-to-consume-counter-data"></a>使用 PDH 函數來使用計數器資料

使用 PDH 函數收集效能資料。 PDH 函數比登錄 [功能](using-the-registry-functions-to-consume-counter-data.md) 更容易使用，而且可用來存取 V1 和 V2 提供者的計數器資料。 PDH 有 Api 可收集目前的效能資料、將效能資料儲存至記錄檔，以及從記錄檔讀取資料。

> [!Note]
> 如果您要撰寫 Windows OneCore 的應用程式，則無法使用效能資料協助程式抽象層函式。 相反地，請使用 [PerfLib V2 取用者](using-the-perflib-functions-to-consume-counter-data.md)函式。

PDH 是高階 API，可簡化收集效能計數器資料的工作。 它有助於查詢剖析、中繼資料快取、比對樣本之間的實例、計算原始值的格式化值、從記錄檔讀取資料，以及將資料儲存至記錄檔。 當從 **V1 提供者** 收集資料時，PDH 會自動使用登錄 [功能](using-the-registry-functions-to-consume-counter-data.md)，並在從 **v2 提供** 者收集資料時使用 [v2 取用者](using-the-perflib-functions-to-consume-counter-data.md)函式。

若要使用 PDH 函數收集效能資料，請執行下列步驟。

1. [建立查詢](creating-a-query.md)
2. [將計數器新增至查詢](creating-a-query.md)
3. [收集效能資料](collecting-performance-data.md)
4. [顯示效能資料](displaying-performance-data.md)
5. [關閉查詢](creating-a-query.md)

您可以從即時來源或記錄檔收集效能資料。 如需如何將效能資料寫入記錄檔的詳細資訊，請參閱 [使用記錄](working-with-log-files.md)檔。

## <a name="see-also"></a>另請參閱

- [收集效能資料](collecting-performance-data.md)
- [流覽計數器](browsing-counters.md)
- [檢查 PDH 介面傳回值](checking-pdh-interface-return-values.md)
- [範例](examples.md)
