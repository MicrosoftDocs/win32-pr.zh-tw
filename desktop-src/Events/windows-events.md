---
title: Windows 事件
description: 事件通常用來疑難排解應用程式和驅動程式軟體。在 Windows Vista 之前，您可以使用 Windows (ETW) 或事件記錄的事件追蹤來記錄事件。WindowsVista 引進了一種新的事件模型，Windows (ETW) 和 Windows 事件記錄檔 API 整合事件追蹤。Windows 10 引進了以 ETW 為基礎的 TraceLogging，並提供簡單的方式來檢測原生、.net 和 WinRT 開發人員的程式碼。
ms.assetid: c10baa8d-50b9-4fda-89d0-d00b1d9f5404
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdf0ecc85f8eed49fd32c30904c73d45bba3436d806ba408fe3ec39afb3e3af9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119388938"
---
# <a name="windows-events"></a>Windows 事件

事件通常用來疑難排解應用程式和驅動程式軟體。

-   在 Windows Vista 之前，您可以使用 Windows (ETW) 或[事件記錄](/windows/desktop/EventLog/event-logging)[的事件追蹤](/windows/desktop/ETW/event-tracing-portal)來記錄事件。
-   WindowsVista 引進了一種新的事件模型，Windows (ETW) 和[Windows 事件記錄](/windows/desktop/WES/windows-event-log)檔 API 整合[事件追蹤](/windows/desktop/ETW/event-tracing-portal)。
-   Windows 10 引進了以 ETW 為基礎的[TraceLogging](/windows/desktop/tracelogging/trace-logging-portal) ，並提供簡單的方式來檢測原生、.net 和 WinRT 開發人員的程式碼。

新的 [TraceLogging](/windows/desktop/tracelogging/trace-logging-portal) 模型可讓您包含事件的結構化資料、使事件相互關聯，而且不需要個別的檢測資訊清單 XML 檔案。

Windows Vista 模型會使用 XML 資訊清單來定義您想要發佈的事件。 事件可以發佈至通道或 ETW 會話。 您可以將事件發佈至下列類型的通道：系統管理員、操作、分析和偵錯工具。 如果您只使用 ETW 來啟用發行者，則不需要在資訊清單中指定通道。 如需撰寫資訊清單的完整詳細資訊，請參閱 [撰寫檢測資訊清單](/windows/desktop/WES/writing-an-instrumentation-manifest)，以及有關通道的詳細資訊，請參閱 [定義通道](/windows/desktop/WES/defining-channels)。

若要註冊您的事件發行者併發布事件，請使用 ETW API。 如需詳細資訊，請參閱 [提供事件](/windows/desktop/ETW/providing-events) 和 [開發提供者](/windows/desktop/WES/developing-a-provider)。 事件發行者會自動將事件寫入資訊清單中指定的通道（如果已啟用）。

如果您想要控制事件發行者以較精細的細微性層級發佈的事件，請使用 ETW API。 例如，如果資訊清單同時定義寫入和讀取事件，則您只能啟用寫入事件。 事件也可以指定層級值（例如警告或錯誤），讓您可以限制寫入至指定錯誤層級的事件。 如需詳細資訊，請參閱 [控制事件追蹤會話](/windows/desktop/ETW/controlling-event-tracing-sessions)。 事件會寫入會話的記錄檔。

取用事件牽涉到從事件通道、事件記錄檔 ( .evtx 或 .evt 檔案) 、) 的 ( 追蹤檔案，或即時 ETW 會話的事件記錄檔。 若要使用 ETW 追蹤檔或即時 ETW 會話中的事件，請在 ETW 中使用追蹤資料協助程式 (TDH) 函數來取用事件。 您也可以使用 TDH 來讀取事件中繼資料。 如需詳細資訊，請參閱 [使用事件](/windows/desktop/ETW/consuming-events)。 若要使用事件通道或事件記錄檔中的事件，請使用 Windows 事件記錄檔函數來查詢或訂閱事件。 如需詳細資訊，請參閱 [查詢事件](/windows/desktop/WES/querying-for-events) 或 [訂閱事件](/windows/desktop/WES/subscribing-to-events)。

在 Windows Vista 之前，您必須使用[事件追蹤來進行 Windows](/windows/desktop/ETW/event-tracing-portal)或[事件記錄](/windows/desktop/EventLog/event-logging)，以發佈和使用事件。

 

 