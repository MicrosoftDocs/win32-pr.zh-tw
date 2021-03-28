---
description: 全域記錄器事件追蹤會話會記錄在作業系統開機程式初期發生的事件。
ms.assetid: 1462bbef-ef32-4053-9930-5b4a0ab46b47
title: 設定和啟動全域記錄器會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8692e1f7321acc163e48cda7e3323f3d24adc1c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973433"
---
# <a name="configuring-and-starting-the-global-logger-session"></a>設定和啟動全域記錄器會話

全域記錄器事件追蹤會話會記錄在作業系統開機程式初期發生的事件。 在使用者登入之前，應用程式和設備磁碟機可以使用全域記錄器會話來捕捉追蹤。 請注意，某些設備磁碟機（例如磁片設備磁碟機）在全域記錄器會話開始時不會載入。

> [!Note]  
> 如果您要在 Windows Vista 上建立全域記錄器會話，您應該考慮改為建立自動記錄器 [會話](configuring-and-starting-an-autologger-session.md) 。

 

您可以使用登錄來設定全域記錄器會話。 如果下列登錄機碼尚未存在，請將其新增至 **GlobalLogger** 機碼：

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
```

下表描述您可以為 **GlobalLogger** 索引鍵定義的值。 您必須具有系統管理員許可權，才能指定這些登錄值。 登錄值會影響將事件記錄到全域記錄器會話的所有提供者。 **開始** 值是啟動全域記錄器會話所需的唯一值;如果登錄中沒有值，所有其他值都有預設的設定。 一般而言，您應該使用預設值。 如果您指定 ETW 無法支援的值，ETW 將會覆寫此值。



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
<td><strong>開始</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>在) 上將此值設定為 1 (，以在下次系統啟動時啟動全域記錄器會話。 若要停止會話開始，請將此值設定為 0 (off) 。 <br/></td>
</tr>
<tr class="even">
<td><strong>BufferSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>每個緩衝區的大小（以 kb 為單位）。 此值應小於 1 mb。 ETW 使用實體記憶體的大小來計算這個值。 <br/></td>
</tr>
<tr class="odd">
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
<tr class="even">
<td><strong>EnableKernelFlags</strong></td>
<td><strong>REG_BINARY</strong></td>
<td>使用此值可啟用一或多個核心提供者。 如果您啟用核心提供者，全域記錄器會話就會在啟動時將本身重新命名為 NT Kernel 記錄器。 如需可能的值，請參閱<a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a>的<strong>EnableFlags</strong>成員。<br/></td>
</tr>
<tr class="odd">
<td><strong>FileCounter</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>全域記錄器會話所產生的事件追蹤記錄檔數目。 系統會遞增此值，直到達到 <strong>FileMax</strong>的值為止。 然後，它會將值重設為0。 此計數器可防止系統覆寫全域記錄器追蹤記錄檔。 <br/></td>
</tr>
<tr class="even">
<td><strong>FileMax</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>系統上允許的事件追蹤記錄檔數目上限。 當追蹤記錄檔的數目達到指定的最大值時，系統就會開始覆寫記錄，從最舊的開始。 <br/> 如果 <strong>檔案名</strong> 中指定的記錄檔存在，ETW 會將 <strong>FileCounter</strong> 值附加至檔案名。 例如，如果使用預設記錄檔名稱，則表單為%SystemRoot%\System32\LogFiles\WMI\GlobalLogger.etl.NNNN。 <br/> 預設值為0，表示沒有最大值。 <br/></td>
</tr>
<tr class="odd">
<td><strong>FileName</strong></td>
<td><strong>REG_SZ</strong></td>
<td>記錄檔的完整路徑。 這個檔案的路徑必須存在。 記錄檔是連續的記錄檔。 請注意，所有提供者將事件寫入全域記錄器會話的提供者都會將事件寫入此記錄檔。 路徑的限制為1024個字元。如果未指定 <strong>FileName</strong> ，則會將事件寫入至%SystemRoot%\System32\LogFiles\WMI\GlobalLogger.etl。 <strong>在 Windows Vista 之前：</strong> 預設檔案為%SystemRoot%\System32\LogFiles\WMI\Trace.log。<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>FlushTimer</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>強制排清追蹤緩衝區的頻率（以秒為單位）。 最短排清時間為1秒。 這項強制排清是除了緩衝區已滿以及追蹤會話停止時所發生的自動排清之外。 <br/> 如果是即時記錄器， (預設值為零的值) 表示排清時間將會設定為1秒。 當 <strong>LogFileMode</strong> 設定為 <strong>EVENT_TRACE_REAL_TIME_MODE</strong>時，即時記錄器就是。<br/> 預設值為 0。 依預設，只有當緩衝區已滿時，才會排清緩衝區。 <br/></td>
</tr>
<tr class="odd">
<td><strong>LogFileMode</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>指定記錄會話選項。 如需值，請參閱 <a href="logging-mode-constants.md">記錄模式常數</a>。 Windows Vista 及更新版本支援此值。 <br/></td>
</tr>
<tr class="even">
<td><strong>MaximumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>要配置的緩衝區數目上限。 一般來說，此值是緩衝區數目下限加上二十。 ETW 使用緩衝區大小和實體記憶體的大小來計算這個值。 此值必須大於或等於 <strong>MinimumBuffers</strong>的值。<br/></td>
</tr>
<tr class="odd">
<td><strong>MaxFileSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>事件追蹤記錄檔的大小上限（以 mb 為單位）。 根據預設值，沒有檔案大小限制。<br/></td>
</tr>
<tr class="even">
<td><strong>MinimumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>全域記錄器會話啟動時要配置的緩衝區數目下限。 您可以指定的緩衝區數目下限為每個處理器兩個緩衝區。 例如，在單處理器電腦上，緩衝區的最小數目為二。 <br/> 單處理器系統上的預設值為0x3。<br/></td>
</tr>
<tr class="odd">
<td><strong>狀態</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>全域記錄器的啟動狀態。 如果全域記錄器無法啟動，則此機碼的值會是適當的 Win32 錯誤碼。 如果全域記錄器成功啟動，則此索引鍵的值為 ERROR_SUCCESS (0) 。<br/></td>
</tr>
</tbody>
</table>



 

在修改登錄並重新啟動電腦之後，全域記錄器會話就會自動啟動，並且與任何其他會話一樣使用，但有一個例外狀況：您 \_ 使用 \_ \_) Wmistr 中定義的 WMI 全域記錄器識別碼常數控制碼 (，以參考全域記錄器會話。 這個常數可用來當做接受會話控制碼之任何事件追蹤函數的引數。 在接受會話名稱的函式中，使用全域 \_ 記錄器 \_ 名稱。

全域記錄器控制器不會呼叫 [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) 函數來啟用提供者。 提供者負責判斷全域記錄器會話是否已啟動，然後再啟用它本身。

若要判斷全域記錄器會話是否已啟動，您可以呼叫 [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) 函式，將 *SESSIONHANDLE* 設定為 WMI \_ 全域 \_ 記錄器識別碼， \_ 並 *ControlCode* 至 **事件 \_ 追蹤 \_ 控制 \_ 查詢**。 如果 **ControlTrace** 呼叫成功，全域記錄器會話就會存在，而提供者可以啟用本身，並將事件記錄到全域記錄器會話 (**ControlTrace** 函式會 \_ 在 \_ \_ \_ 全域記錄器) 不是使用中時，傳回錯誤的 WMI 實例。

一般而言，控制器會負責在啟用提供者時，將啟用旗標和層級傳遞給提供者，但由於全域記錄器控制器未啟用提供者，因此，提供者會負責在需要時將這項資訊傳遞給本身。

全域記錄器會話是受限的資源，應謹慎使用。 想要在開機過程中捕獲資訊的服務，應該考慮將控制器邏輯新增到本身，而不是使用全域記錄器會話。

如需啟動事件追蹤會話的詳細資訊，請參閱設定 [和啟動事件追蹤會話](configuring-and-starting-an-event-tracing-session.md)。

如需啟動私用記錄器會話的詳細資訊，請參閱設定 [和啟動私用記錄器會話](configuring-and-starting-a-private-logger-session.md)。

如需啟動 NT Kernel 記錄器會話的詳細資訊，請參閱設定 [和啟動 Nt Kernel 記錄器會話](configuring-and-starting-the-nt-kernel-logger-session.md)。

