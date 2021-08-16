---
description: 本檔適用于想要使用 ETW 的使用者模式應用程式。 如需檢測以核心模式執行之設備磁碟機的相關資訊，請參閱 [WPP 軟體追蹤]，並將事件追蹤新增至 Windows 驅動程式套件 (WDK) 中 Kernel-Mode 的驅動程式。
ms.assetid: 3de69436-671b-46a2-8d92-4eb3af2a4233
title: 事件追蹤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 908e935d48749d80e5b2cfe237efeed5413c839157e53b489f4857c0349b4a1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070218"
---
# <a name="event-tracing"></a>事件追蹤

## <a name="purpose"></a>目的

Windows (ETW) 的事件追蹤可讓應用程式設計人員能夠啟動和停止事件追蹤會話、檢測應用程式以提供追蹤事件，以及使用追蹤事件。 追蹤事件包含事件標頭和提供者定義的資料，可描述應用程式或作業的目前狀態。 您可以使用這些事件來對應用程式進行偵錯工具並執行容量和效能分析。

本檔適用于想要使用 ETW 的使用者模式應用程式。 如需檢測以核心模式執行之設備磁碟機的相關資訊，請參閱 [ [WPP 軟體追蹤](/windows-hardware/drivers/devtest/wpp-software-tracing)]，並[將事件追蹤新增至](/windows-hardware/drivers/devtest/event-tracing-for-windows--etw-)Windows 驅動程式套件 (WDK) 中 Kernel-Mode 的驅動程式。

## <a name="where-applicable"></a>適用時

當您想要檢測應用程式、將使用者或核心事件記錄至記錄檔，並使用記錄檔中的事件時，請使用 ETW。

## <a name="developer-audience"></a>開發人員對象

ETW 是針對撰寫使用者模式應用程式的 C 和 c + + 開發人員所設計。

## <a name="run-time-requirements"></a>執行階段需求求

ETW 包含在 Microsoft Windows 2000 和更新版本中。 如需哪些作業系統需要哪些作業系統才能使用特定功能的相關資訊，請參閱函式檔集的需求一節。

## <a name="process-etw-traces-in-net-code"></a>在 .NET 程式碼中處理 ETW 追蹤

您可以使用 [.Net TRACEPROCESSING API](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) 來分析應用程式和其他軟體元件的 ETW 追蹤。 Microsoft 內部使用此 API 來分析產生 Windows 工程系統的 ETW 資料，而且它也可用來在[Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer)中開啟數個數據表。 此 API 以 NuGet 套件的形式提供。

如需詳細資訊，請參閱[這篇文章](/windows/apps/trace-processing/overview)。

## <a name="in-this-section"></a>本節內容



| 主題                                                                     | 描述                                                                        |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [事件追蹤的新功能](what-s-new-in-event-tracing.md)<br/> | 在每個版本中新增至事件追蹤的新功能。<br/>          |
| [關於事件追蹤](about-event-tracing.md)<br/>                 | 事件追蹤的一般資訊。<br/>                                |
| [使用事件追蹤](using-event-tracing.md)<br/>                 | 說明如何使用 ETW API 的工作相關主題。<br/>               |
| [事件追蹤參考](event-tracing-reference.md)<br/>         | ETW 函數和其他程式設計專案的詳細描述。 <br/> |



 

 

 
