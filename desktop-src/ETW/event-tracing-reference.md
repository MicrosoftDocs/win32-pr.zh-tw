---
description: 列出與事件追蹤搭配使用的元素。
ms.assetid: 8cb5907e-9006-45d1-9d48-13a43a631664
title: 事件追蹤參考
ms.topic: article
ms.date: 01/30/2020
ms.openlocfilehash: 20aaf59de3419b4015f03b38db69839b6f258ccd561b1e918694396e875ae5a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083278"
---
# <a name="event-tracing-reference"></a>事件追蹤參考

您可以使用下列程式設計項目來撰寫應用程式，以併入事件追蹤：

-   [事件追蹤列舉](/windows/desktop/api/_etw/#enumerations)
-   [事件追蹤函數](/windows/desktop/api/_etw/#functions)
-   [事件追蹤介面](/windows/desktop/api/_etw/#interfaces)
-   [事件追蹤結構](/windows/desktop/api/_etw/#structures)
-   [事件追蹤常數](event-tracing-constants.md)

如需使用這些程式設計項目的範例詳細資訊，請參閱 [事件追蹤範例](event-tracing-samples.md)。

本節也包含下列資訊：

-   ETW 提供的[工具](event-tracing-tools.md)
-   核心事件的[MOF 類別定義](event-tracing-mof-classes.md)
-   定義事件類別時使用的[MOF 類別限定詞](event-tracing-mof-qualifiers.md)

## <a name="process-etw-traces-in-net-code"></a>在 .NET 程式碼中處理 ETW 追蹤

您也可以使用 [.Net TRACEPROCESSING API](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) 來分析應用程式和其他軟體元件的 ETW 追蹤。 Microsoft 內部使用此 API 來分析產生 Windows 工程系統的 ETW 資料，而且它也可用來在[Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer)中開啟數個數據表。 此 API 以 NuGet 套件的形式提供。

如需詳細資訊，請參閱[這篇文章](/windows/apps/trace-processing/overview)。
