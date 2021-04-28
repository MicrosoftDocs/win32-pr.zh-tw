---
title: TraceLogging
description: TraceLogging
ms.assetid: c516424a-9eba-4b56-80de-8c713fd3461a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7bd83c608d2ac98fdccce760c851496af80c217
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116716"
---
# <a name="tracelogging"></a>TraceLogging

## <a name="purpose"></a>目的

TraceLogging 是新的 Windows 10 事件追蹤架構，適用于使用者模式應用程式和核心模式驅動程式。 TraceLogging 適用于 Windows (ETW) 的事件追蹤，並提供更簡單的方式來檢測程式碼。

## <a name="in-this-section"></a>本節內容



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>主題</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="trace-logging-about.md">關於 TraceLogging</a><br/></td>
<td>TraceLogging 是使用者模式應用程式和核心模式驅動程式的新 Windows 10 事件追蹤。 TraceLogging 是適用于 Windows (ETW) 之自我描述事件追蹤的格式。 TraceLogging 適用于 Windows (ETW) 的事件追蹤，並提供更簡單的方式來檢測程式碼。<br/></td>
</tr>
<tr class="even">
<td><a href="tracelogging-using-tracelogging.md">使用 TraceLogging</a><br/></td>
<td>下列主題提供原生和 managed 程式碼的 TraceLogging 快速入門，以及範例。<br/></td>
</tr>
<tr class="odd">
<td><a href="trace-logging-reference.md">TraceLogging 參考</a><br/></td>
<td>下列主題提供有關原生 TraceLogging API 的資訊。<br/> TraceLogging 適用于 Windows (ETW) 的事件追蹤，並提供更簡單的方式來檢測程式碼。 TraceLogging 可讓您包含事件的結構化資料、使事件相互關聯，而且不需要個別的檢測資訊清單 XML 檔案。<br/> <span class="underline">適用于 WinRT 開發人員</span><br/>
<ul>
<li><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> 已在 Windows 10 中擴充，可記錄自我描述 WINDOWS (ETW) 事件的事件追蹤，而不需要資訊清單。</li>
<li><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity</strong></a> 已在 Windows 10 中擴充，以提供活動開始和停止方法，這些方法可讓您控制開始和停止事件的格式和內容。 此外，也可以嵌套活動。</li>
</ul>
<span class="underline">針對 managed 程式碼 (Microsoft .NET Framework) 開發人員</span><br/>
<ul>
<li>舊版 .NET Framework 隨附的 <a href="/dotnet/api/system.diagnostics.tracing.eventsource">EventSource</a> 類別已支援寫入 ETW 事件，而不需要資訊清單。 不過，開發人員必須使用 EventSource 作為基類，並將屬性和方法新增至已自動轉換成 ETW 資訊清單的衍生類別。 現在，開發人員不需要從 EventSource 衍生，而可以改為直接使用 EventSource 來記錄不需要資訊清單的自我描述事件。</li>
</ul>
<span class="underline">適用于 C/c + + 開發人員</span><br/>
<ul>
<li>TraceLoggingProvider 是在使用者或核心模式中，適用于 C/c + + 開發人員的建議 API。 這個 API 並不適合用於動態 (腳本) 案例（例如 JAVAscript）。 下列連結說明 C/c + + API。</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="developer-audience"></a>開發人員對象

TraceLogging 的設計目的是要讓使用者模式應用程式開發人員以及想要在程式碼中加入追蹤的核心模式驅動程式開發人員使用。

