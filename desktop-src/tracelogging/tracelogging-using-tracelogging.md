---
title: 使用 TraceLogging
description: 下列主題提供原生和 managed 程式碼的 TraceLogging 快速入門，以及範例。
ms.assetid: CEC57517-7A0E-45AA-85F7-F358AE51EF4A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e331f5ebec3d7eb8ce9c50d3e9d92f747bf76414
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382705"
---
# <a name="using-tracelogging"></a>使用 TraceLogging

下列主題提供原生和 managed 程式碼的 TraceLogging 快速入門，以及範例。

## <a name="prerequisites"></a>必要條件

-   需要 Windows 10 軟體發展工具組 (SDK) 才能撰寫使用者模式提供者
-   需要 Windows 驅動程式套件 (WDK) 才能撰寫核心模式提供者

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                        | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [TraceLogging C/c + + 快速入門](tracelogging-native-quick-start.md)<br/>                             | 下一節說明將 TraceLogging 新增至原生使用者模式程式碼所需的基本步驟。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [TraceLogging 受控快速入門](tracelogging-managed-quick-start.md)<br/>                          | 下一節說明將 TraceLogging 新增至 managed 程式碼所需的基本步驟。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [記錄和顯示 TraceLogging 事件](tracelogging-record-and-display-tracelogging-events.md)<br/> | 使用 Windows Performance Recorder (WPR 來記錄 TraceLogging 事件) 並使用 Windows Performance Analyzer (WPA) 加以查看。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [C/c + + Tracelogging 範例](tracelogging-c-cpp-tracelogging-examples.md)<br/>                       | 本主題包含 C/c + + Tracelogging 範例。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [.NET Tracelogging 範例](tracelogging-net-examples.md)<br/>                                       | 本主題包含 managed 程式碼 Tracelogging 範例，說明如何只在會話詳細資訊層級為詳細資訊時記錄事件，以及如何記錄結構化的事件資料。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [通用 Windows 平臺記錄範例](universal-windows-platform-logging-examples.md)<br/>     | 這個範例示範如何使用 LoggingChannel、LoggingActivity、LoggingSession 和 FileLoggingSession 等 Windows Foundation. Diagnostics 命名空間中的記錄 Api。 這些類別是針對 Windows 應用程式內的診斷記錄所設計。 這些 Api 已新增至 Windows 8.1。 <br/> LoggingChannel 和 LoggingActivity Api 已在 Windows 10 中擴充，以支援使用 TraceLogging 事件編碼來撰寫複雜的事件。<br/> 您可以從 [GitHub](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/Logging)下載通用 Windows 平臺記錄範例。<br/> |



 

TraceLogging 範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[核心模式驅動程式和元件的 TraceLogging](/windows-hardware/drivers/devtest/tracelogging-for-kernel-mode-drivers-and-components)
</dt> </dl>

 

