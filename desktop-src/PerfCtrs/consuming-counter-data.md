---
description: 您可以使用下列其中一個介面來取用效能資料：效能資料協助程式 (PDH) 介面，此介面可提供第1版和第2版效能計數器提供者之資料的高階存取權。登錄介面，可為效能計數器提供者的資料提供低層級的存取權。效能程式庫介面，可直接存取第2版效能計數器提供者的資料。PDH 介面比登錄介面更容易使用，建議用於大部分的效能資料收集工作。 PDH 介面基本上是登錄介面所提供功能的較高層級抽象概念。 只有當您無法使用 PDH 抽象層函式時，才能使用 [效能程式庫] 介面。
ms.assetid: a42f6cdd-47e9-4f43-aeaf-37a5abb0fa36
title: 使用計數器資料
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: f3abcc6dd5a385ebffdc887516613efb76b53359e5f8995bc28ba7f6239187b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119775678"
---
# <a name="consuming-counter-data"></a>使用計數器資料

想要讀取和使用 Windows 效能計數器資料的程式，可以使用適用于此案例的數個介面之一。

- 腳本可以使用 [WMI 效能計數器類別](/windows/desktop/WmiSdk/monitoring-performance-data) 或 [TypePerf](/windows-server/administration/windows-commands/typeperf) 工具。
- .NET 程式可以使用 [PerformanceCounter 類別](/dotnet/api/system.diagnostics.performancecounter)。
- [效能資料協助程式 (PDH) 程式庫](using-the-pdh-functions-to-consume-counter-data.md)可透過 Win32 (C/c + +) API，提供 V1 和 V2 效能計數器提供者的資料高階存取權。
- 登錄 [介面](using-the-registry-functions-to-consume-counter-data.md) 可讓您透過特殊登錄機碼來存取 V1 和 V2 效能計數器提供者的資料 `HKEY_PERFORMANCE_DATA` 。
- [PerfLib v2 取用者](using-the-perflib-functions-to-consume-counter-data.md)函式可透過 Win32 (C/c + +) API，從 V2 效能計數器提供者提供低層級的資料存取。

建議使用 PDH 介面進行大部分的 C/c + + 效能資料收集工作，因為它比登錄和 PerfLib 介面更容易使用。
