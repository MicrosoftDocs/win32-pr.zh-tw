---
description: 「自動記錄器」事件追蹤會話會記錄在作業系統開機程式初期發生的事件。
ms.assetid: df5a79f4-abbf-4b83-afc3-cbd14b166067
title: 設定和啟動自動記錄器會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b17e7e818193aa4fa316d17a0e4392e41b55dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973849"
---
# <a name="configuring-and-starting-an-autologger-session"></a>設定和啟動自動記錄器會話

「自動記錄器」事件追蹤會話會記錄在作業系統開機程式初期發生的事件。 應用程式和設備磁碟機可以在使用者登入之前，使用「自動記錄器」會話來捕捉追蹤。 請注意，某些設備磁碟機（例如磁片設備磁碟機）在自動記錄器會話開始時不會載入。

自動記錄器與全域記錄器有下列不同之處：

-   您可以指定一或多個自動記錄器會話， (全域記錄器是每個人記錄事件) 的單一會話。
-   當會話啟動時，自動記錄器會將啟用通知傳送給提供者， (全域記錄器不會將啟用通知傳送給提供者，因此提供者必須依賴其他方法來知道是否啟動全域記錄器會話，才能開始) 記錄事件。
-   自動記錄器不支援記錄 NT 核心記錄器事件 (請參閱 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)的 **EnableFlags** 成員) 。 若要記錄 NT 核心記錄器事件，您必須使用 [全域記錄器](configuring-and-starting-the-global-logger-session.md)。

如需全域記錄器 seesion 的詳細資訊，請參閱設定 [和啟動全域記錄器會話](configuring-and-starting-the-global-logger-session.md)。

> [!Note]  
> ETW 支援 Windows Vista 和更新版本上的自動記錄器。 使用舊版作業系統上的 [全域記錄器](configuring-and-starting-the-global-logger-session.md) 。

 

您可以使用登錄來設定自動記錄器會話。 新增下列登錄機碼（如果尚未存在）：

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
```

在 [自動 **記錄器** ] 機碼底下，針對您想要設定的每個自動記錄器會話建立金鑰，如下列範例所示。

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
                  \Logger Session A
                  \Logger Session B
                  \Logger Session C
```

針對每個會話，為您想要啟用至會話的每個提供者建立金鑰。 使用提供者的 GUID 作為索引鍵。

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
                  \Logger Session A
                     \{ProviderGuid1}
                     \{ProviderGuid2}
                  \Logger Session B
                  \Logger Session C
```

下表描述您可以為每個自動記錄器會話定義的值。 您必須具有系統管理員許可權，才能指定這些登錄值。 **開始** 和 **Guid** 值是啟動自動記錄器會話所需的唯一值;如果登錄中沒有值，所有其他值都有預設的設定。 一般而言，您應該使用預設值。 如果您指定 ETW 無法支援的值，ETW 將會覆寫此值。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>類型</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>BufferSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>每個緩衝區的大小（以 kb 為單位）。 應小於 1 mb。 ETW 使用實體記憶體的大小來計算這個值。<br/></td>
</tr>
<tr class="even">
<td><strong>ClockType</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>記錄每個事件的時間戳記時要使用的計時器。
<ul>
<li>1 = 效能計數器值 (高解析度) </li>
<li>2 = 系統計時器</li>
<li>3 = CPU 週期計數器</li>
</ul>
如需每種頻率類型的描述，請參閱<a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>的<strong>ClientCoNtext</strong>成員。<br/> 在 Windows Vista 和更新版本上，預設值為 1 (效能計數器值) 。 在 Windows Vista 之前，預設值為 2 (系統計時器) 。<br/></td>
</tr>
<tr class="odd">
<td><strong>DisableRealtimePersistence</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>若要停用即時持續性，請將此值設定為1。 預設值為 0 (啟用即時會話) 。<br/> 如果已啟用即時持續性，則在關閉電腦時未傳遞的即時事件將會被保存。 然後，當取用者下次連接會話時，事件就會傳遞給取用者。 <br/></td>
</tr>
<tr class="even">
<td><strong>FileCounter</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>請勿設定或修改此值。 如果指定 <strong>FileMax</strong> ，則這個值是用來遞增記錄檔名稱的序號。 如果值無效，則會假設為1。<br/></td>
</tr>
<tr class="odd">
<td><strong>FileName</strong></td>
<td><strong>REG_SZ</strong></td>
<td>記錄檔的完整路徑。 這個檔案的路徑必須存在。 記錄檔是連續的記錄檔。 路徑的限制為1024個字元。<br/> 如果未指定 <strong>FileName</strong> ，則會將事件寫入%SystemRoot%\System32\LogFiles\WMI\ <sessionname> 。 <br/></td>
</tr>
<tr class="even">
<td><strong>FileMax</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>ETW 所建立記錄檔的最大實例數目。 如果 <strong>檔案名</strong> 中指定的記錄檔存在，ETW 會將 <strong>FileCounter</strong> 值附加至檔案名。 例如，如果使用預設的記錄檔名稱，則格式為%SystemRoot%\System32\LogFiles\WMI\ <sessionname> 。NNNN. <br/> 電腦第一次啟動時，檔案名是 <sessionname> .etl，第二次檔案名是 <sessionname> .etl. 0002，依此類推。 如果 <strong>FileMax</strong> 為3，則在第四次重新開機電腦時，ETW 會將計數器重設為1，並覆寫 <sessionname> .etl （如果存在的話）。<br/> 支援的記錄檔實例數目上限為16。<br/> 請勿將這項功能與 <a href="logging-mode-constants.md">EVENT_TRACE_FILE_MODE_NEWFILE</a> 記錄檔模式搭配使用。<br/></td>
</tr>
<tr class="odd">
<td><strong>FlushTimer</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>強制排清追蹤緩衝區的頻率（以秒為單位）。 最短排清時間為1秒。 這項強制排清是除了緩衝區已滿以及追蹤會話停止時所發生的自動排清之外。 <br/> 如果是即時記錄器， (預設值為零的值) 表示排清時間將會設定為1秒。 當 <strong>LogFileMode</strong> 設定為 <strong>EVENT_TRACE_REAL_TIME_MODE</strong>時，即時記錄器就是。<br/> 預設值為 0。 依預設，只有當緩衝區已滿時，才會排清緩衝區。 <br/></td>
</tr>
<tr class="even">
<td><strong>Guid</strong></td>
<td><strong>REG_SZ</strong></td>
<td>字串，包含可唯一識別會話的 GUID。 這是必要的值。</td>
</tr>
<tr class="odd">
<td><strong>LogFileMode</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>指定一或多個記錄模式。 如需可能的值，請參閱 <a href="logging-mode-constants.md">記錄模式常數</a>。 預設值為 <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>。 您可以指定 <strong>EVENT_TRACE_BUFFERING_MODE</strong> 或 <strong>EVENT_TRACE_REAL_TIME_MODE</strong>，而不是寫入記錄檔。<br/> 指定 <strong>EVENT_TRACE_BUFFERING_MODE</strong> 可避免在檔案系統變成可用時，將會話內容排清至磁片的成本。 <br/> 請注意，使用 <strong>EVENT_TRACE_BUFFERING_MODE</strong> 會導致系統忽略 <strong>MaximumBuffers</strong> 值，因為緩衝區大小是 <strong>MinimumBuffers</strong> 和 <strong>BufferSize</strong>的乘積。<br/> 自動記錄器會話不支援 <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> 記錄模式。<br/> 如果指定 <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> ，則必須明確提供 <strong>BufferSize</strong> ，而且在記錄器和附加的檔案中都必須相同。<br/></td>
</tr>
<tr class="even">
<td><strong>MaxFileSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>記錄檔的檔案大小上限（以 mb 為單位）。 當到達大小上限時，會關閉會話，除非您處於迴圈記錄檔模式。 若要指定無限制，請將值設定為0。 如果未設定，預設值為 100 MB。 當達到檔案大小上限時所發生的行為，取決於 <strong>LogFileMode</strong>的值。<br/></td>
</tr>
<tr class="odd">
<td><strong>MaximumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>要配置的緩衝區數目上限。 一般來說，此值是緩衝區數目下限加上二十。 ETW 使用緩衝區大小和實體記憶體的大小來計算這個值。 此值必須大於或等於 <strong>MinimumBuffers</strong>的值。<br/></td>
</tr>
<tr class="even">
<td><strong>MinimumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>啟動時要配置的緩衝區數目下限。 您可以指定的緩衝區數目下限為每個處理器兩個緩衝區。 例如，在單處理器電腦上，緩衝區的最小數目為二。<br/></td>
</tr>
<tr class="odd">
<td><strong>開始</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>若要在下次重新開機電腦時啟動重新開機記錄器會話，請將此值設為 1;否則，請將此值設定為0。<br/></td>
</tr>
<tr class="even">
<td><strong>狀態</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>自動記錄器的啟動狀態。 如果無法啟動自動記錄器，此機碼的值會是適當的 Win32 錯誤碼。 如果自動記錄器成功啟動，則此機碼的值會 <strong>ERROR_SUCCESS</strong> (0) 。<br/></td>
</tr>
</tbody>
</table>



 

下表描述您可以針對您想要啟用至會話的每個提供者定義的值。 您必須具有系統管理員許可權，才能指定這些登錄值。 如果您指定 ETW 無法支援的值，ETW 將會覆寫此值。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>類型</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Enabled</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>判斷是否已啟用提供者。 若要啟用提供者，請將此值設定為1。 若要停用提供者，請將此值設定為0。 預設值是 0。</td>
</tr>
<tr class="even">
<td><strong>EnableFlags</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>提供者定義的值，這個值會指定提供者產生事件的事件類別。 如需詳細資訊，請參閱<a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>EnableTrace</strong></a>函數的<em>EnableFlags</em>參數。 如果提供者不支援 <strong>MatchAnyKeyword</strong> 或 <strong>MatchAllKeyword</strong>，請指定此值名稱。</td>
</tr>
<tr class="odd">
<td><strong>EnableLevel</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>提供者定義的值，這個值會指定事件中包含的詳細層級。 例如，您可以使用這個值來指出事件的嚴重性層級 (提供者所產生的資訊、警告、錯誤) 。 如需預先定義的層級清單，請參閱<a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a>函數的<em>level</em>參數。</td>
</tr>
<tr class="even">
<td><strong>EnableProperty</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>使用此值可在記錄檔中包含下列一或多個專案：
<ul>
<li><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = 在擴充的資料中包含使用者的安全識別碼 (SID) 。</li>
<li><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = 將終端機會話識別碼包含在擴充的資料中。</li>
<li><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = 包含在擴充的資料中，使用 <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a>撰寫之事件的呼叫堆疊追蹤。</li>
<li><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = 篩選出未指定非零關鍵字的所有事件。</li>
<li><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = 表示這個 <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> 呼叫應該啟用 <a href="provider-traits.md">提供者群組</a> ，而不是個別事件提供者。</li>
<li><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = 在擴充的資料中包含處理常式啟動金鑰。</li>
<li><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = 在擴充的資料中包含事件索引鍵。</li>
<li><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRI加值稅E</strong> (0x00000200) = 篩選出標記為 inprivate 事件或來自標示為 inprivate 之進程的所有事件。</li>
</ul>
如需這些專案的詳細資訊，請參閱<a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a>結構的<strong>EnableProperty</strong> 。<br/></td>
</tr>
<tr class="odd">
<td><strong>MatchAnyKeyword</strong></td>
<td><strong>REG_QWORD</strong></td>
<td>關鍵字的位元遮罩，可決定您想要提供者寫入的事件類別。 如果任何事件的關鍵字位符合此遮罩中設定的任何位，則提供者會寫入事件。 若要指定提供者寫入所有事件，請將此值設定為零。 如需範例，請參閱 <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> 函數的備註一節。</td>
</tr>
<tr class="even">
<td><strong>MatchAllKeyword</strong></td>
<td><strong>REG_QWORD</strong></td>
<td>此位元遮罩是選擇性的。 這個遮罩會進一步限制您希望提供者寫入的事件類別。 如果事件的關鍵字符合 <em>MatchAnyKeyword</em> 條件，則只有在這個遮罩中的所有位都存在於事件的關鍵字時，提供者才會寫入事件。 如果 <em>MatchAnyKeyword</em> 為零，則不會使用這個遮罩。 如需範例，請參閱 <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> 函數的備註一節。</td>
</tr>
</tbody>
</table>



 

在修改登錄之後，下次電腦重新開機時，就會啟動重新開機記錄器會話。 自動記錄器會話會呼叫 [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) 函式來啟用提供者。

自動記錄器會話會增加系統開機時間，並應謹慎使用。 想要在開機過程中捕獲資訊的服務，應該考慮將控制器邏輯新增到本身，而不是使用自動記錄器會話。

若要停止自動記錄器會話，請呼叫 [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) 函數。 您傳遞給函式的會話名稱就是您在登錄中用來定義會話的登錄機碼名稱。

在 Windows 8.1、Windows Server 2012 R2 和更新版本上， [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) 函式可以使用事件承載、範圍和堆疊逐步篩選，以及 [**啟用 \_ 追蹤 \_ 參數**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) 和 [**事件 \_ 篩選 \_ 描述**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) 項結構，以篩選記錄器會話中的特定條件。 如需事件裝載篩選準則的詳細資訊，請參閱 [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)和 [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) 函式以及 **啟用 \_ 追蹤 \_ 參數**、 **事件 \_ 篩選器 \_ 描述** 元和承載 [**\_ 篩選 \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) 述詞結構。

如需啟動事件追蹤會話的詳細資訊，請參閱設定 [和啟動事件追蹤會話](configuring-and-starting-an-event-tracing-session.md)。

如需啟動私用記錄器會話的詳細資訊，請參閱設定 [和啟動私用記錄器會話](configuring-and-starting-a-private-logger-session.md)。

如需啟動 NT Kernel 記錄器會話的詳細資訊，請參閱設定 [和啟動 Nt Kernel 記錄器會話](configuring-and-starting-the-nt-kernel-logger-session.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定和啟動私用記錄器會話](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[設定並啟動 SystemTraceProvider 會話](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[設定和啟動事件追蹤會話](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[設定和啟動 NT Kernel 記錄器會話](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**啟用 \_ 追蹤 \_ 參數**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**事件 \_ 篩選器 \_ 描述項**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**裝載 \_ 篩選述詞 \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[更新事件追蹤會話](updating-an-event-tracing-session.md)
</dt> </dl>
