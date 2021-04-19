---
description: Windows 具有 Api 和服務，可支援您的桌面應用程式中的診斷。
ms.assetid: 8dbc4807-e634-4204-8be7-e200f99ac6e2
title: 診斷
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9127429c3c6b5073906ec94aec404bc3c82c5f44
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973397"
---
# <a name="diagnostics"></a>診斷

Windows 具有 Api 和服務，可支援您的桌面應用程式中的診斷。 它們提供：

-   調試和錯誤處理。
-   支援程式碼剖析應用程式的效能。
-   支援疑難排解和錯誤報表。
-   系統監視和事件通知。
-   網路監視與診斷。
-   系統狀態的評量。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                   | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [評量執行引擎](/previous-versions/windows/desktop/axe/axe-access-portal)<br/>                                            | Windows 評定執行引擎 (AXE) 可讓您管理和執行 Windows 系統評定。 評量可協助人員瞭解系統的狀態，並解決效能、可靠性或功能方面的問題。 AXE 提供使用 UX 工具或腳本管理評量所需的基礎結構、執行評量、進行測量、將原始資料處理成結果、執行診斷，以及發佈結果。<br/>                                                                                                                                 |
| [調試和錯誤處理](./debugging-and-error-handling.md)<br/>                             | 描述調試和錯誤處理。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [硬體計數器分析](/previous-versions/windows/desktop/hcp/hardware-counter-profiling-portal)<br/>                          | 應用程式會使用硬體計數器分析 (HCP) SDK 來捕捉執行緒分析資料，例如週期時間和內容切換的原因。 您也可以使用 HCP 來捕捉您已在系統上設定之硬體效能計數器的計數器資料。<br/>                                                                                                                                                                                                                                                                                                             |
| [網路診斷架構](./ndf/portal.md)<br/>                                                  | 網路診斷架構 (NDF) 提供一種方法讓元件和應用程式開發人員簡化使用者的網路疑難排解。 使用者可以使用單一疑難排解工具來嘗試診斷和修復網路問題。 <br/>                                                                                                                                                                                                                                                                                                                                        |
| [網路監視器](./netmon2/network-monitor.md)<br/>                                      | 網路監視器會捕捉顯示和分析的網路流量。 它可讓您執行工作，例如分析先前在使用者定義方法中所捕獲的資料，以及從定義的通訊協定剖析器中提取資料。<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| [效能計數器](./perfctrs/performance-counters-portal.md)<br/>                                     | 計數器是用來提供與作業系統或應用程式、服務或驅動程式的執行狀況有關的資訊。 計數器資料有助於判斷系統瓶頸並微調系統和應用程式效能。 作業系統、網路和裝置提供應用程式可取用的計數器資料，讓使用者能夠以圖形方式查看系統的執行狀況。<br/>                                                                                                                                                                |
| [效能記錄檔及警示](/previous-versions/windows/desktop/pla/pla-portal)<br/>                                                | 效能記錄檔及警示 (PLA) 提供應用程式設計人員根據效能計數器閾值產生警示通知的能力。 程式設計人員也可以使用 PLA 來查詢效能資料、建立事件追蹤會話、捕捉電腦的設定，以及追蹤某些 Win32 系統 Dll 中的 API 呼叫。<br/>                                                                                                                                                                                                                                           |
| [進程快照](/previous-versions/windows/desktop/proc_snap/process-snapshotting-portal)<br/>                                | 進程快照可讓您在部分或整個中捕獲進程狀態。 它類似于 [工具](./toolhelp/tool-help-library.md) 說明 API，但有一個重要的優點：它可以有效率地使用 WINDOWS internal POSIX 派生複製功能來捕獲進程的虛擬位址內容。 您可以使用 [**MiniDumpWriteDump**](/windows/win32/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) 函式將進程快照集傾印到檔案中。<br/>                                                                                                                                                       |
| [進程狀態 API](./psapi/process-status-helper.md)<br/>                                            | 進程狀態應用程式開發介面 (PSAPI.DLL) 是協助程式程式庫，可讓您更輕鬆地取得處理常式和設備磁碟機的相關資訊。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| [系統事件通知服務](./sens/system-event-notification-service-portal.md)<br/>           | 專為行動使用者所設計的應用程式需要一組獨特的連接功能和通知。 在過去，這些個別的應用程式必須在內部執行這些功能。 系統事件通知服務 (SENS) 現在會在作業系統中提供這些功能，為應用程式建立統一的連線和通知介面。 使用 SENS 開發人員可以從應用程式內判斷連接頻寬和延遲資訊，並根據這些條件將應用程式的作業優化。 <br/> |
| [系統監視器](./sysmon/system-monitor-portal.md)<br/>                                               | 系統監視器 (SYSMON) 是您用來設定 Microsoft System Monitor ActiveX 控制項 (API) 的應用程式開發介面。 [系統監視器] 控制項可讓您查看即時和先前記錄的效能計數器資料，例如記憶體、磁片和處理器計數器資料。<br/>                                                                                                                                                                                                                                                                                     |
| [Tool Help Library](./toolhelp/tool-help-library.md)<br/>                                              | 工具說明程式庫所提供的功能，可讓您更輕鬆地取得目前執行中應用程式的相關資訊。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Windows 錯誤報告](./wer/windows-error-reporting.md)<br/>                                       | 錯誤報表功能可讓使用者通知 Microsoft 應用程式錯誤、核心錯誤、無回應的應用程式，以及其他應用程式特定的問題。 Microsoft 可以使用錯誤報表功能，為客戶提供針對其特定問題的疑難排解資訊、解決方案或更新。 開發人員可以使用這個基礎結構來接收可用來改善其應用程式的資訊。<br/>                                                                                                                                          |
| [Windows 事件](./events/windows-events.md)<br/>                                                      | 描述事件追蹤和記錄。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Windows Performance Analyzer (WPA)](/previous-versions/windows/desktop/xperf/windows-performance-analyzer--wpa-)<br/> | Windows Performance Analyzer (WPA) 是一組效能監視工具，可用來產生 Microsoft Windows 作業系統和應用程式的深入效能設定檔。<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| [Windows 效能工具組 (WPT) ](/previous-versions/windows/it-pro/windows-8.1-and-8/hh162945(v=win.10))<br/>                    | Windows 效能工具組包含效能監視工具，可產生 Microsoft Windows 作業系統和應用程式的深入效能設定檔。 此文件討論 Windows Performance Recorder (WPR) 和 Windows Performance Analyzer (WPA)。<br/>                                                                                                                                                                                                                                                                                              |
| [Windows 疑難排解平臺](/previous-versions/windows/desktop/wintt/windows-troubleshooting-toolkit-portal)<br/>             | Windows 疑難排解 Platform (WTP) 提供 Isv、Oem 和系統管理員撰寫疑難排解套件的能力，用來探索和解決電腦上發現的問題。<br/>                                                                                                                                                                                                                                                                                                                                                                                          |



 

 

 
