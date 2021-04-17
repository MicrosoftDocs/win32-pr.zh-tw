---
title: 使用 ETW 追蹤和 Netsh 命令的案例 1 HTTP Timeout 範例
description: 透過 ETW 追蹤，可以檢查透過 HTTP 伺服器 API 元件進行的資料流程，以診斷問題。
ms.assetid: b6b24161-c3da-4972-b49f-c545da2fc81e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa50f438aca664651b24db822f2b9e3a30da4682
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104567309"
---
# <a name="scenario-1-http-timeout-example-using-etw-tracing-and-netsh-commands"></a>案例1：使用 ETW 追蹤和 Netsh 命令的 HTTP Timeout 範例

透過 ETW 追蹤，可以檢查透過 HTTP 伺服器 API 元件進行的資料流程，以診斷問題。 例如，web 應用程式的使用者可能會在其瀏覽器中看到網頁無法顯示的錯誤訊息。 在裝載 web 應用程式的伺服器上，IT 專業人員也會看到 HTTP 錯誤記錄檔中的連接逾時專案，如下面的 [圖 1] 所示。 您可以在下列目錄中找到 HTTP 錯誤記錄檔：% windir% \\ System32 記錄檔 \\ \\ HTTPERR \\ 。

![顯示 netsh H T P 命令視窗的螢幕擷取畫面，其中顯示 timeout 的 H T T 錯誤記錄檔。](images/httperrorlog.png)

圖1： HTTP 錯誤記錄檔中的超時時間

## <a name="generating-an-etw-trace-report"></a>產生 ETW 追蹤報告

若要產生 HTTP 伺服器 API 元件的 ETW 追蹤報告，請從命令提示字元執行下列步驟。 在此範例中，追蹤是在伺服器上執行，因為它會裝載 web 應用程式。

下列步驟會產生名為 HTTPtrace 的追蹤，然後將追蹤轉換成稱為 httptrace.csv 的 CSV 檔案。 如下所示，HTTP 伺服器 API 的 ETW 提供者稱為 Microsoft Windows-HttpService。 0xFFF 命令列選項表示應捕捉此提供者的所有 ETW 事件。

**產生 ETW 追蹤報告**

1.  啟動 HTTP 伺服器 API 元件的 ETW 追蹤： l **ogman.exe 啟動 HTTPtrace-p Microsoft-Windows-HttpService 0xffff-o HTTPtrace. etl – ets**
2.  重現問題，讓它可以在追蹤中捕捉。 在此範例中，從用戶端電腦存取 web 應用程式，而導致在用戶端上顯示「**無法顯示頁面**」訊息。
3.  現在已重現問題，請停止追蹤： **logman.exe 停止 HTTPtrace – ets**
4.  將報表轉換成 CSV 格式： **tracerpt.exe HTTPtrace---------------httptrace.csv**
5.  查看追蹤報表。 CSV 追蹤的摘錄如下表1所示。

## <a name="viewing-the-trace-and-diagnosing"></a>查看追蹤和診斷

您可以在 Excel 或支援 CSV 格式的任何工具中，查看所產生的追蹤 CSV 檔案。 下表1顯示範例追蹤檔 (httptrace.csv) 的摘錄。 在追蹤報表中，[層級] 資料行會顯示值為 "3" 的專案，這會對應至 ETW 中的警告。 HTTP 伺服器 API 元件會遵循下列文章中定義的 ETW 層級： (https://msdn2.microsoft.com/library/aa382793.aspx) 。 ETW 層級包括：



| 層級 | 意義      |
|-------|--------------|
| 1     | 重大     |
| 2     | 錯誤        |
| 3     | 警告      |
| 4     | Infomational |
| 5     | 「詳細資訊」      |



 

使用此警告時，事件種類 (類型資料行) 報告 "ConnTimedOut"。 在 ConnTimeOut 事件的後續資料行中，過期的特定計時器會回報為「計時器 \_ ConnectionIdle」。 請注意，資料表中包含 "Timer \_ ConnectionIdle" 專案的資料行未包含在資料表中，以求簡潔，並避免 excerpting 不連續的資料行。



| 事件名稱                    | 類型            | 事件識別碼 | 版本 | 通路 | 層級 |
|-------------------------------|-----------------|----------|---------|---------|-------|
| EventTrace                    | 標頭          | 0        | 2       | 0       | 0     |
| Microsoft-Windows-HttpService | ChgUrlGrpProp   | 28       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | AddUrl          | 31       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ChgReqQueueProp | 30       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ChgUrlGrpProp   | 28       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ChgSrvSesProp   | 29       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ChgSrvSesProp   | 29       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnConnect     | 21       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnIdAssgn     | 22       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | RecvReq         | 1        | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | 剖析           | 2        | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | LogFileWrite    | 51       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnCleanup     | 24       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnTimedOut    | 53       | 0       | 16      | 3     |



 

表1：從計時器問題的範例追蹤報表摘錄

在此範例中，標頭計時器的到期 (ConnTimeOut 事件)  (計時器 \_ ConnectionIdle) 是終端使用者在其 web 用戶端中看到「無法顯示頁面」訊息的原因。 可能的超時原因可能是因為連線速度很慢，所以 Web 用戶端傳送速度很慢。 若要解決此問題，可以透過 Netsh 命令來調整超時值。

## <a name="adjusting-timeout-through-netsh-and-verifying-the-solution"></a>透過 Netsh 調整 Timeout 並驗證解決方案

下列適用于 HTTP 的 Netsh 命令可讓 IT 專業人員查看和設定 HTTP 伺服器 API 元件上的設定值。 透過 Netsh HTTP 命令進行的變更會影響該電腦的 HTTP 伺服器 API 元件所裝載的所有伺服器應用程式。 這些變更會保存在元件重新開機後重新開機電腦。 Netsh HTTP 命令可在 windows Vista 和 Windows Server 2008 中使用，並在 Windows Vista 和 Windows Server 2008 上執行時取代 Windows Server 2003 資源套件的 HttpCfg.exe 工具。 在此案例中，我們會調整超時值，然後驗證解決方案。 HTTP 伺服器 API 元件中有計時器，可確保可用性並防止不正確或惡意的使用者過度耗用。 從預設值調整計時器應謹慎地針對潛在的 DoS 攻擊進行評估。

在此範例中，web 用戶端位於低速網路連線後方，導致計時器 \_ CONNECTIONIDLE ETW 事件。 在考慮到因為對伺服器負載造成的超時和平衡的原因之後，會決定將超時值增加為240秒的值。 您可以使用下列程式來查看並設定計時器。

**\_使用 Netsh (timer ConnectionIdle) 設定閒置連接計時器**

1.  在伺服器上，開啟提高許可權的命令視窗，然後執行下列步驟來查看和設定 timeout 值。 [圖 2] 顯示 Netsh HTTP 命令的螢幕擷取畫面。
2.  顯示目前的超時值： **Netsh HTTP show timeout**
3.  設定計時器 \_ ConnectionIdle timeout 值。 在此範例中，值會變更為240秒： **Netsh HTTP add timeout timeouttype = idleconnectiontimeout value = 240**

![netsh HTTP 命令視窗](images/netshhttpcommand.png)

圖2： Netsh HTTP 命令視窗

設定 timeout 值之後，請重新執行 ETW 診斷步驟。 如果錯誤狀況已更正，ETW 追蹤應該不會再顯示連接閒置計時器之 ETW 層級為 "3" 的超時時間。

 

 




