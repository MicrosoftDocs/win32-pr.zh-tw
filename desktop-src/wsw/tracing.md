---
title: 追蹤
description: 追蹤會使用 Windows (ETW) 的事件追蹤。
ms.assetid: b008bae2-9423-4e72-ae03-9cd50f73d812
keywords:
- Windows 的追蹤 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da2bcd5c07c2c5ebf3a28620e39efe3034d3c2bc024ac487caaec38e3c69fca9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707258"
---
# <a name="tracing"></a>追蹤

追蹤會使用 Windows (ETW) 的事件追蹤。 若要利用 Windows Server 2008 R2 所提供的追蹤工具，請從[MSDN 下載](https://www.microsoft.com/download/details.aspx?id=8279)網站安裝 Microsoft Windows SDK。


支援的追蹤層級有三種：

-   詳細資訊 (所有可用的追蹤) 。
-   資訊 (資訊追蹤) 。
-   錯誤追蹤)  (錯誤。

追蹤下列事件：

-   任何錯誤 (層級 = 錯誤、層級 = 資訊或層級 = 詳細) 。
-   API 的進入/離開 (Level = Info 或 Level = Verbose) 。
-   開始及完成任何 IO (Level = Info 或 Level = Verbose) 
-   交換的 SOAP 訊息 (Level = Verbose，可在 Windows 2003 SP1 和更新版本上使用) 

## <a name="generating-and-viewing-wwsapi-traces"></a>產生和查看 WWSAPI 追蹤

WWSAPI 會使用 Windows Vista 和更新版本上以資訊清單為基礎的事件。 因此，追蹤體驗會根據作業系統版本而有所差異。 您可以在所有支援的平臺上使用內建的 ETW 工具來產生 ETW 追蹤。 不過，以美觀的格式來觀看 ETW 追蹤需要 Windows XP SP2 和 Windows 2003 SP1 的自訂工具。 根據作業系統版本而定，有幾種不同的方式可以收集和查看 WWSAPI ETW 事件追蹤。

## <a name="enabling-and-viewing-wwsapi-traces-in-event-viewer-works-on-windows-vista-and-above"></a>在事件檢視器 (中啟用和觀看 WWSAPI 追蹤適用于 Windows Vista 和更新版本) 

-   從命令列或 [執行] 功能表執行 eventvwr.msc。
-   在右側的 [動作] 窗格中，按一下 [view] 連結，然後啟用 [顯示分析和調試記錄] 選項。
-   流覽至 [應用程式及服務記錄檔]， \\ Microsoft \\ Windows \\ WebServices 提供者的左窗格。
-   以滑鼠右鍵按一下追蹤提供者，然後選取 [啟用記錄]。
-   執行您的案例。
-   重新整理 [事件檢視器] 頁面時，您應該會開始看到 WWSAPI 追蹤專案。

## <a name="enabling-and-viewing-wwsapi-traces-using-wstracebat-script-works-on-xpsp2-and-above"></a>使用 Wstrace.bat 腳本來啟用和觀看 WWSAPI 追蹤 (適用于 XPSP2 和更新版本) 

wstrace.bat 批次檔提供便利的方式來執行下列動作：

-   建立追蹤記錄
-   刪除追蹤記錄
-   啟用和停用追蹤
-   更新追蹤層級 (info/error/verbose) 
-   將追蹤記錄轉換成 CSV 檔案

批次檔會針對所有命令使用 logman.exe，但將記錄檔轉換為 CSV 檔案（需要自訂工具 (wstracedump.exe) ）除外。

## <a name="using-tracing-commands"></a>使用追蹤命令

下列命令會建立使用資訊、錯誤或詳細資訊層級的記錄。 此命令需要較高的許可權。

**wstrace.bat 建立 \[ 資訊 \| 錯誤 \| 詳細資訊\]**

下列命令會刪除記錄檔。 此命令需要較高的許可權。

**wstrace.bat 刪除**

下列命令會啟用追蹤。 您必須先建立記錄檔。

**wstrace.bat 開啟**

您可以依照下列方式修改 [資訊]、[錯誤] 或 [詳細資訊]) 的追蹤層級 (：

**wstrace.bat 更新 \[ 資訊 \| 錯誤 \| 詳細資訊\]**

若要傾印追蹤輸出，請使用下列命令：

**wstrace.bat 傾印 > temp.csv**

事件會傾印至 CSV 檔案，直到按下 Ctrl + C 或停用追蹤為止。

## <a name="tracing-file-format"></a>追蹤檔案格式

wstrace.bat 所建立的 CSV 檔案是簡單的逗號分隔變數文字檔。 這些檔案可能會在 Excel、記事本等等中開啟。

檔案的資料行如下所示：

-   記錄事件時的時間戳記時間戳記
-   ProcessID-記錄事件之進程的 ULONG 識別碼
-   ThreadID-記錄事件之執行緒的 ULONG 識別碼
-   事件種類的事件列舉值可能 ( "api enter" \| "api pending" \| "api ExitSyncSuccess" \| "api ExitSyncFailure" \| "api ExitAsyncSuccess" \| "api ExitAsyncFailure" " \| io 已啟動" " \| io 已完成 \| 「io 失敗 \| \| 」「錯誤」「 \| \| \| \| \| 已收到訊息」「已收到訊息」「收到的訊息」「收到的訊息」「收到的訊息」「收到的訊息」「傳送訊息開始」」 ) 
-   Operation-正在叫用的作業名稱。 這通常會對應至所呼叫的 API。
-   錯誤-選擇性的 HRESULT 錯誤號碼
-   資訊-事件的選擇性資訊

## <a name="collecting-wwsapi-etw-trace-file-using-etw-tools-works-on-xpsp2-and-above"></a>使用 ETW 工具收集 WWSAPI ETW 追蹤檔案 (可在 XPSP2 和更新版本上運作) 

啟用 WWSAPI 的 ETW 追蹤

**logman start wstrace-bs 64-ft 1-rt-p Microsoft-Windows-WebServices \[ flags \[ level \] \] \[ -o <EtlLogFileName> \] -ets**

建立並啟動 ETW 追蹤會話。 Logman.exe 是可在所有支援的平臺上使用的內建 ETW 工具。 請注意，您必須 \_ \_ 在 XPSP2 和 W2K3 上使用 Microsoft Windows WebServices 作為提供者名稱。 您可以執行 logman 查詢提供者，以查看已註冊之提供者的清單。 除非未註冊，否則應列出 microsoft Windows WebServices (或 microsoft \_ Windows \_ WebServices) 提供者。 提供者通常會在安裝期間註冊。 不過，您也可以手動註冊，方法是 <ManifestFileName> 在 Windows Vista 和更新版本上執行 wevtutil.exe im (，) 或 <MofFileName> 在 XPSP2 和 W2K3 mofcomp.exe 上 () 。

旗標可以用來依類別篩選追蹤。 它可以是或值下列追蹤種類。 如果未提供，則會啟用所有的追蹤類型。

-   0x1-API 進入/離開追蹤。
-   0x2-錯誤追蹤。
-   0x4-IO 追蹤。
-   0x8-SOAP 訊息追蹤。
-   0x10-二進位訊息追蹤。

層級可以用來依層級篩選追蹤。 它應該是下列其中一個值。 如果未提供，則會啟用所有追蹤層級。

-   0x1-嚴重追蹤。
-   0x2-錯誤追蹤。
-   0x3-警告追蹤。
-   0x4-資訊追蹤。
-   0x5-詳細追蹤。

EtlLogFileName 是要建立之 ETW 事件記錄檔的路徑， (使用 etl 延伸模組) 。 如果未提供，ETW 將會挑選可以稍後查詢的隨機名稱。 此檔案不應位於使用者的設定檔目錄中。  ( etl 檔案) 的 ETW 事件記錄檔是二進位格式。 它可由 ETW 應用程式取用，但不是人類看得懂的格式。 下一步說明如何查看其內容。

執行您的案例

正在收集 ETW 事件記錄檔。

**logman stop wstrace-ets**

停止 ETW 追蹤會話。 這是 ETW 停止記錄事件的時間。 在 EtlLogFileName 參數中指定的 ETW 事件記錄檔 () 已準備好可供使用。 您可以在本機觀看 (指示) 或傳送至產品群組以進行調查。

使用 ETW 工具的端對端範例：

**logman start wstrace-bs 64-ft 1-rt-p Microsoft-Windows-WebServices-o mytrace .etl-ets**

**回波。。執行您的案例。**

**logman stop wstrace-ets**

**tracerpt mytrace .etl-o mytrace.xml**

**wstrace.htm**

**回波。。在開啟的頁面中使用 mytrace.xml 和 wstrace。**

## <a name="viewing-wwsapi-etw-trace-file-traces-using-wstracedumpexe-tool-works-on-windows-xp-and-above"></a>使用 wstracedump.exe 工具來觀看 WWSAPI ETW 追蹤檔案追蹤 (適用于 Windows XP 和更新版本) 

Wstracedump.exe 是自訂開發的 ETW 取用者工具，可處理 WWSAPI ETW 追蹤檔中的事件，並產生人類看得懂的輸出。 它可以從所有支援的平臺產生輸出。 如需詳細資訊，請參閱其使用方式 (wstracedump.exe-？ ) 。

## <a name="viewing-wwsapi-etw-trace-file-traces-using-etw-tools-works-on-windows-vista-and-above"></a>使用 etw 工具來觀看 WWSAPI etw 追蹤檔案追蹤 (可在 Windows Vista 和更新版本上運作) 

Tracerpt.exe 是用來查看 ETW 事件記錄檔內容的工具，並可在所有支援的平臺上使用。 可以用來從 ETW 事件記錄檔產生 CSV、.EVTX 或 XML 傾印檔案。 不過，產生的輸出檔只會在 Windows Vista 和更新版本上擁有人類可讀取的追蹤。 這些指示說明如何產生 XML 傾印檔案，並將它與 xsl 檔案一起使用，以美觀的格式顯示追蹤 (xsl 檔案非常簡單，而且如果需要) 不同的格式，則可能會改變。

-   執行

    **tracerpt <EtlLogFileName> -o <OutputXMLFileName>**

    若要從二進位 ETL 檔案建立 XML 傾印 (tracerpt.exe 預設會建立 XML 格式的輸出檔。 執行 tracerpt-？ 可) 查看其他可用的格式。

-   此時，您可以在 XML 檔案中看到追蹤資訊。 此外，您還可以開啟 wstrace.htm 檔案，並使用 xml 傾印檔案和 wstrace xsl 檔案，以更好格式查看追蹤。 請注意，檔案必須位於本機電腦上，才能在 IE 上使用此 html 檔案。

## <a name="security"></a>安全性

啟用追蹤時，系統管理員應該考慮它是否耗用額外的磁碟空間和計算能力。 除非以合理的限制設定追蹤設定，否則惡意用戶端或應用程式可能會耗盡系統資源。 使用訊息追蹤功能時，攜帶機密資訊（例如認證、個人資訊等等）的訊息可能會保存到磁片中，或由可存取系統事件檢視器的任何人來查看。 基於這個問題的風險降低，系統或系統管理員使用者可以在 Windows 2003 和更新版本上啟用追蹤。 Windows XP 上已停用訊息追蹤，讓任何使用者都可以開啟追蹤。

下列列舉會搭配追蹤使用：

-   [**WS \_ 追蹤 \_ API**](/windows/desktop/api/WebServices/ne-webservices-ws_trace_api)

 

 




