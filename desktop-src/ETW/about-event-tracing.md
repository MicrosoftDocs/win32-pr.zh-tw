---
description: Windows 事件追蹤 (ETW) 是高效率的核心層級追蹤功能，讓您能記錄核心或應用程式定義的事件記錄檔。
ms.assetid: 0eaa7bd3-8537-483a-b0d6-db3b790a6f3d
title: 關於事件追蹤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5004ada6d0d11d9c232a6fda1553ea24de5a59fb1d03e46728084f84f0e79de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086428"
---
# <a name="about-event-tracing"></a>關於事件追蹤

Windows 事件追蹤 (ETW) 是高效率的核心層級追蹤功能，讓您能記錄核心或應用程式定義的事件記錄檔。 您可以即時或從記錄檔取用事件，並使用這些事件來對應用程式進行偵錯工具，或判斷應用程式中發生效能問題的位置。

ETW 可讓您以動態方式啟用或停用事件追蹤，讓您可以在實際執行環境中執行詳細追蹤，而不需要重新開機電腦或應用程式。

事件追蹤 API 分成三個不同的元件：

-   [控制器](#controllers)，可啟動和停止事件追蹤會話並啟用提供者
-   提供事件的[提供者](#providers)
-   取用事件的取用[者](#consumers)

下圖顯示事件追蹤模型。

![事件追蹤模型](images/etdiag2.png)

## <a name="controllers"></a>控制器

控制器是一種應用程式，可定義記錄檔的大小和位置、啟動和停止 [事件追蹤會話](event-tracing-sessions.md)、啟用提供者，讓它們可以將事件記錄到會話、管理緩衝集區的大小，以及取得會話的執行統計資料。 會話統計資料包含使用的緩衝區數目、傳遞的緩衝區數目，以及遺失的事件和緩衝區數目。 

如需詳細資訊，請參閱 [控制事件追蹤會話](controlling-event-tracing-sessions.md)。

## <a name="providers"></a>提供者

提供者是包含事件追蹤檢測的應用程式。 在提供者註冊本身之後，控制器就可以在提供者中啟用或停用事件追蹤。 提供者會定義要啟用或停用的解釋。 一般而言，啟用的提供者會產生事件，而停用的提供者則不會產生事件。 這可讓您在應用程式中新增事件追蹤，而不需要每次都產生事件。 

雖然 ETW 模型會將控制器和提供者分成不同的應用程式，但應用程式可以同時包含這兩個元件。

如需詳細資訊，請參閱 [提供事件](providing-events.md)。

### <a name="types-of-providers"></a>提供者類型

提供者有四種主要類型： MOF (傳統) 提供者、WPP 提供者、資訊清單型提供者和 TraceLogging 提供者。 如果您要撰寫 Windows Vista 或更新版本的應用程式，而不需要支援舊版系統，則應該使用以資訊清單為基礎的提供者或 TraceLogging 提供者。

#### <a name="mof-classic-providers"></a>MOF (傳統) 提供者：

-   使用 [RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) 和 [TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) 函數來註冊和寫入事件。
-   使用 MOF 類別來定義事件，讓取用者知道其使用方式。
-   一次只能由一個追蹤會話啟用。

#### <a name="wpp-providers"></a>WPP 提供者：

-   使用 [RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) 和 [TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) 函數來註冊和寫入事件。
-    (將相關聯的 TMF 檔案編譯成二進位的 .pdb) ，其中包含從預處理器掃描原始程式碼中的 WPP 檢測所推斷的解碼資訊。
-   一次只能由一個追蹤會話啟用。

#### <a name="manifest-based-providers"></a>以資訊清單為基礎的提供者：

-   使用 [EventRegister](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) 和 [EventWrite](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) 來註冊和寫入事件。
-   使用資訊清單來定義事件，讓取用者知道其使用方式。
-   最多可以同時啟用八個追蹤會話。

#### <a name="tracelogging-providers"></a>[TraceLogging](/windows/desktop/tracelogging/trace-logging-about) 提供者：

-   使用 [TraceLoggingRegister](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) 和 [TraceLoggingWrite](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) 來註冊和寫入事件。
-   使用自我描述事件，讓事件本身包含使用這些事件的所有必要資訊。
-   最多可以同時啟用八個追蹤會話。

所有事件提供者基本上都是使用 api 的事件追蹤系列 ([TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent)適用于舊版技術，而[EventWrite](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) / [EventWriteEx](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex)則適用于較新的) 。 事件提供者在其儲存于事件裝載中的欄位類型，以及它們儲存相關事件解碼資訊的位置，都是不同的。

## <a name="consumers"></a>取用者

取用者是選取一或多個事件追蹤會話作為事件來源的應用程式。 取用者可以同時從多個事件追蹤會話要求事件;系統會依時間順序傳遞事件。 取用者可以接收儲存在記錄檔中的事件，或接收即時傳遞事件的會話。 處理事件時，取用者可以指定開始和結束時間，而且只會傳遞在指定時間範圍內發生的事件。 

如需詳細資訊，請參閱 [使用事件](consuming-events.md)。

## <a name="missing-events"></a>遺失的事件

Perfmon、系統診斷和其他系統工具可能會報告事件記錄檔中遺失的事件，並指出 Windows (ETW) 的事件追蹤設定可能不是最佳的。 事件可能會因為許多原因而遺失：

-   事件大小總計大於64K。 這包括 ETW 標頭加上資料或承載。 使用者無法控制這些遺漏的事件，因為事件大小是由應用程式設定。

-   ETW 緩衝區大小小於事件大小總計。 使用者無法控制這些遺漏的事件，因為事件大小是由記錄事件的應用程式設定。

-   針對即時記錄，即時取用者不會消耗足夠的事件，也不會完全存在，然後備份檔案就會填滿。 如果事件記錄檔服務在記錄事件時停止並啟動，就會產生這種情況。 使用者無法控制這些遺漏的事件。

-   記錄到檔案時，磁片太慢，無法跟上記錄速度。

基於上述原因，請向產生事件的應用程式或服務的提供者報告這些問題。 這些問題只能由應用程式開發人員或記錄事件的服務來修正。 如果事件記錄服務中正在報告遺失的事件，這可能表示事件記錄檔服務的設定有問題。 使用者可能會有有限的功能，可增加事件記錄檔服務所要使用的最大磁碟空間，這可能會減少遺失的事件數目。

 

 
