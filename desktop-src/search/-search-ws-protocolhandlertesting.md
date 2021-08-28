---
description: 測試和偵測通訊協定處理常式的整數是瞭解通訊協定處理常式的啟動方式。
ms.assetid: 33c99620-7381-4719-9fc6-4c8284481411
title: 偵錯工具通訊協定處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b8946b0203c7bc56dd16606ca28e4811bc6328d0cfa87ae55eb2e752657e7da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944488"
---
# <a name="debugging-protocol-handlers"></a>偵錯工具通訊協定處理常式

測試和偵測通訊協定處理常式的整數是瞭解通訊協定處理常式的啟動方式。

本主題的組織方式如下：

-   [關於偵錯工具通訊協定處理常式](#about-debugging-protocol-handlers)
-   [設定調試](#setting-up-debugging)
-   [其他資源](#additional-resources)
-   [相關主題](#related-topics)

## <a name="about-debugging-protocol-handlers"></a>關於偵錯工具通訊協定處理常式

SearchIndexer 進程 (searchindexer.exe) 會在系統內容中啟動一份 SearchProtocolHost 程式 (SearchProtocolHost.exe) ，並在使用者內容中啟動另一個複本。 然後，您可以視需要在 SearchProtocolHost 程式中載入通訊協定處理常式。 在搜尋服務停止之前，它們不會被卸載。 當服務正在執行時，相同的通訊協定處理常式實例會重複使用任何次數。

SearchIndexer 和 SearchProtocolHost 進程會在編制索引期間經常進行通訊。 如果您暫停或停止 SearchProtocolHost 處理常式，SearchIndexer 將會啟動新的 SearchProtocolHost 進程，使您的偵錯工具失效。 此外，如果您將偵錯工具直接附加至 SearchProtocolHost 進程，您可以中斷控制碼繼承，從 searchindexer.exe 到 searchprotocolhost.exe，而這兩個進程將無法進行通訊。

若要避免這些問題，您必須通知搜尋服務您正在進行偵測，而且您必須將偵錯工具附加至 SearchIndexer 進程，並提供偵錯工具子進程的指示，如下所述。

## <a name="setting-up-debugging"></a>設定調試

請遵循下列步驟來設定通訊協定處理常式的偵錯工具。

1.  將登錄中的 DebugFilters 值設為1，以通知搜尋服務您正在進行偵錯工具：

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft
       Windows Search
          Gathering Manager
             DebugFilters = 1
    ```

2.  使用 [影像檔執行選項] 登錄機碼附加偵錯工具：

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion
       Image File Execution Options
          SearchIndexer.exe
             Debugger = <path to debugger> <debugger options> 
    ```

    下表說明範例偵錯工具的選項。

    

    **使用 ntsd 偵錯工具偵錯工具的範例**   *= C：偵錯工具 \\ \\ntsd.exe-odGx-C： "sxe ld mydll.dll; g"*<br/>

3.  使用 compmgmt.msc、services.msc 或命令視窗，在偵錯工具下重新開機 searchindexer.exe，如下所示：
    ```
    net stop wsearch
    <copy new DLLs for debugging>
    net start wsearch
            
    ```

    

若要區分在系統內容中執行的 SearchProtocolHost 程式，以及在使用者內容中執行的進程，您可以查看環境字串。 例如，有了 ntsd.exe，您可以使用延伸模組命令 **！ peb** ，在流程環境區塊 (peb) 中顯示資訊的格式化視圖。

## <a name="additional-resources"></a>其他資源

-   如需建立處理常式的詳細資訊，請參閱 [註冊 Shell 擴充](../shell/reg-shell-exts.md)功能。

## <a name="related-topics"></a>相關主題

<dl> <dt>**概念**</dt><dt><a href="-search-3x-wds-phaddins.md">開發通訊協定處理常式</a></dt><dt><a href="-search-3x-wds-extidx-prot-implementing.md">瞭解通訊協定處理常式</a></dt>會 <dt><a href="-search-3x-wds-notifyingofchanges.md">通知索引變更</a></dt><dt><a href="-search-3x-wds-ph-ui-extensions.md">新增圖示和內容功能表</a></dt>程式 <dt><a href="-search-3x-wds-ph-ui-samplecode.md">代碼範例：通訊協定處理常式的 Shell 擴充</a></dt>功能為通訊協定處理常式 <dt><a href="-search-3x-wds-ph-search-connector.md">建立搜尋連接器，以便</a></dt><dt><a href="-search-3x-wds-ph-install-registration.md">安裝和註冊通訊協定處理常式</a></dt> </dl>

 

 
