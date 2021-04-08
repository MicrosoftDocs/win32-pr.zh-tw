---
description: 從 Windows Vista 開始，WMI 服務不會使用 WMI 記錄檔。 相反地，它會使用 Windows 的事件追蹤 (ETW) 而事件可透過事件檢視器或 Wevtutil 命令列工具取得。
ms.assetid: bb6401e8-caf7-4f39-ab64-b7532723ce9a
ms.tgt_platform: multiple
title: 追蹤 WMI 活動
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14371a4f18b81019073cd2b428500b12385719e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693979"
---
# <a name="tracing-wmi-activity"></a>追蹤 WMI 活動

從 Windows Vista 開始，WMI 服務不會使用 [Wmi 記錄](wmi-log-files.md)檔。 相反地，它會使用 [Windows 的事件追蹤 (ETW)](/windows/desktop/ETW/event-tracing-portal) 而事件可透過 **事件檢視器** 或 Wevtutil 命令列工具取得。

本主題將討論下列各節：

-   [透過事件檢視器取得 WMI 事件](#obtaining-wmi-events-through-event-viewer)
-   [在命令提示字元中啟用 WMI 追蹤](#enabling-wmi-tracing-at-command-prompt)
-   [使用以 WPP 為基礎的 WMI 追蹤](#using-wpp-based-wmi-tracing)
-   [相關主題](#related-topics)

## <a name="obtaining-wmi-events-through-event-viewer"></a>透過事件檢視器取得 WMI 事件

WMITracing 記錄檔包含 WMI 追蹤的事件。 不過，這是二進位檔案。 若要以人類可讀取的格式查看這些事件，請使用 **事件檢視器**。

根據預設，不會追蹤 WMI 事件。 此程式描述如何使用 **事件檢視器** 來啟用 wmi 事件追蹤和尋找 wmi 事件。 您可以透過 wevtutil 命令列工具執行相同的作業。

**若要在事件檢視器中查看 WMI 事件**

1.  開啟 [事件檢視器]。 在 [ **View** ] 功能表上，按一下 [ **顯示分析和調試記錄**]。 在 [ 應用程式和服務記錄檔 \| Microsoft \| Windows WMI 活動] 下找出 WMI 的追蹤通道記錄檔 \| 。
2.  以滑鼠右鍵按一下 **追蹤** 記錄檔，然後選取 [ **記錄檔屬性**]。 按一下 [ **啟用記錄** ] 核取方塊，以啟動 WMI 事件追蹤。 如需通道的詳細資訊，請參閱 [Windows 事件記錄檔中的事件記錄檔和通道](/previous-versions//aa385225(v=vs.85))。
3.  Wmi 事件會顯示在 **Wmi 活動** 的事件視窗中。 按兩下清單中的事件以查看詳細資訊。 您可以使用 **XML 視圖** 或 **易記的視圖** 格式來查看事件。

[ **事件識別碼** ] 欄位會顯示包含下列資訊的值。

<dl> <dt>

<span id="Event_1"></span><span id="event_1"></span><span id="EVENT_1"></span>事件1
</dt> <dd>

特定作業的事件順序開始。 每個序列都會出現一次。

事件1的事件欄位如下：

-   **GroupOperationID** 是唯一的識別碼，用於針對特定用戶端回報的所有事件。
-   **OperationId** 表示作業順序。
-   作業 **會指定對** WMI 的連接或要求。
-   **使用者** 指出透過執行腳本或透過 CIM STUDIO 對 WMI 提出要求的帳戶。
-   **命名空間** 會顯示連接的目標 WMI 命名空間。

例如，腳本可能會要求 WMI 類別的所有實例，例如 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)。 第一個作業可能是與 WMI 的連接。

</dd> <dt>

<span id="Event_2"></span><span id="event_2"></span><span id="EVENT_2"></span>事件2
</dt> <dd>

組成作業的事件。 順序中的一或多個出現次數。

事件2的事件欄位如下：

-   **GroupOperationID** 指出事件發生的順序。
-   **GroupOperationID** 指出事件發生的順序。
-   **ProviderName** 表示提供資料的提供者名稱。
-   **Path** 是物件的 WMI 路徑。

例如，作業可能是 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)的列舉。

</dd> <dt>

<span id="Event_3"></span><span id="event_3"></span><span id="EVENT_3"></span>事件3
</dt> <dd>

特定作業的事件序列結尾。 每個序列都會出現一次。

只會顯示 **GroupOperationID** 。

</dd> </dl>

## <a name="enabling-wmi-tracing-at-command-prompt"></a>在命令提示字元中啟用 WMI 追蹤

您也可以透過 Wevtutil 命令列工具啟用 WMI 事件追蹤。 使用下列命令： **Wevtutil.exe Sl Microsoft-Windows-WMI-活動/追蹤/e： true**。 WMI 事件來源是 Microsoft Windows-WMI。 如需 Wevtutil.exe 的詳細資訊，請參閱 [關於 Windows 事件記錄](/previous-versions//aa382610(v=vs.85))檔。

## <a name="using-wpp-based-wmi-tracing"></a>使用以 WPP 為基礎的 WMI 追蹤

從 Windows Vista 開始，在 Windows 作業系統中，WMI 會在開機程式期間建立作用中的追蹤通道。 通道的名稱是 WMI \_ 追蹤 \_ 會話。 只有錯誤會記錄到通道。

Windows 軟體追蹤預處理器 (WPP) 會在二進位檔案中記錄資訊。 若要讀取檔案，您必須先將它轉譯成可讀取的文字格式。 您可以使用稱為 tracefmt.exe 的工具（ [Windows 驅動程式套件 (WDK) ](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) ）來進行轉譯。 此工具需要儲存在某些相關檔案中的資訊。 這些檔案位於% SystemRoot% \\ System32 \\ wbem \\ tmf 目錄中，而且副檔名為 tmf。 此工具實際上需要單一 tmf 檔案。 您可以藉由將所有的 tmf 檔案串連至另一個 tmf 檔案，來建立該單一檔案。 如需 tmf 檔案的詳細資訊，請參閱 [追蹤訊息格式](/windows-hardware/drivers/devtest/trace-message-format-file)檔案。

安裝 [Windows 驅動程式套件 (WDK) ](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) 以取得 tracelog.exe 和 tracefmt.exe 命令列工具之後，請執行下列步驟來收集以 WPP 為基礎的 WMI 追蹤。

**若要查看以 WPP 為基礎的 WMI 追蹤**

1.  若要建立單一 tmf 檔案，請開啟提升許可權的命令提示字元視窗，然後流覽至% SystemRoot% \\ System32 \\ wbem \\ tmf 目錄。

2.  輸入 **copy/y% SystemRoot% \\ system32 \\ wbem \\ Tmf \\ \* . tmf% systemroot% \\ system32 \\ wbem \\ tmf \\ wmi. tmf**。 這會建立名為 tmf 的檔案，其中包含所有 tmf 檔案的內容。

3.  輸入 **tracelog.exe-FLUSH WMI \_ Trace \_ Session**。 這會清除磁片上的 WPP 緩衝區。
4.  輸入 **集追蹤 \_ 格式 \_ 前置詞 \[ = %9！ d！ \]%8！04X！。%3！04X！。%3！04X！：： %4！ s！ \[%1！ s！ \] (%！COMPNAME!:%!FUNC！： %2！ s！ )**。 Tracefmt 工具會在每個追蹤訊息中加入一些預設資訊。 您可以設定追蹤 \_ 格式前置詞環境變數來設定所包含的資訊 \_ 。 若要瞭解所使用的語法，請參閱 [追蹤訊息前置](https://msdn.microsoft.com/library/aa139695.aspx)詞。
5.  輸入 **tracefmt-tmf% systemroot% \\ system32 \\ wbem \\ tmf \\ wmi. tmf-o OUTPUT.TXT% systemroot% \\ system32 \\ wbem \\ 記錄 \\ WMITracing .log**。 這會執行從二進位格式到可讀取文字格式的轉譯。
6.  輸入 **notepad% systemroot% \\ system32 \\ wbem \\ tmf \\OUTPUT.TXT**。 這將會在 [記事本] 中開啟追蹤檔案。

以下是一些您可能需要執行的其他 WPP 相關工作。

**停止以 WPP 為基礎的 WMI 追蹤**

-   輸入 **tracelog.exe-STOP WMI \_ Trace \_ Session**。

**啟動以 WPP 為基礎的 WMI 追蹤**

-   輸入 **tracelog.exe-啟動 WMI \_ 追蹤 \_ 會話-guid \# 1FF6B227-2CA7-40f9-9A66-980EADAA602E-rt-層級 5-旗標 0x7-f MYTRACE。BIN**

**Windows Vista：** 根據預設，會將以 WPP 為基礎的 WMI 追蹤設定為層級2，其中只包含錯誤訊息。 若要同時包含資訊訊息，請將層級設定為4。 預設會追蹤 WMI 的所有區域。 有三個可追蹤的不同區域： Core (旗標 = 0x1) 、ESS (旗標 = 0x2) 和 >prov (旗標 = 0x4) 。 在上述的 start 命令中， **旗標 0x7** 會追蹤所有三個區域。

**Windows 7：** 根據預設，會停用以 WPP 為基礎的 WMI 追蹤，並將其設定為層級0。 若要使用以 WPP 為基礎的 WMI 追蹤，必須啟用這項功能，並將錯誤訊息的層級2設為，並將錯誤和參考用訊息設定為層級4。

**列出所有的 WPP 追蹤會話**

-   輸入 **tracelog.exe-l**。

**列出 WMI WPP 追蹤會話的相關資訊**

-   輸入 **tracelog.exe-l \| findstr/i "wmi \_ trace"**。

**若要查看 WMI WPP 追蹤會話參數**

-   輸入 **tracelog.exe-q WMI \_ Trace \_ Session**。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 疑難排解](wmi-troubleshooting.md) \(英文\)
</dt> <dt>

[WMI 記錄檔](wmi-log-files.md)
</dt> </dl>

 

 
