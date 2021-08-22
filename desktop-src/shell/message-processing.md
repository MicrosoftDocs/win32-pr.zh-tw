---
description: CPlApplet 回呼函式會藉由 Windows 來處理傳送至主控台專案的所有訊息。 傳送至函式的訊息會以特定的順序排列。 根據相同的 token，.cpl 專案需要以特定方式處理訊息。
ms.assetid: 70302698-f9d5-4de4-a662-4815002eea52
title: 主控台訊息處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e697c603b69790d17c4d6771666a1111fa6f968eb97a30256696921f133530d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719949"
---
# <a name="control-panel-message-processing"></a>主控台訊息處理

[**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc)回呼函式會藉由 Windows 來處理傳送至主控台專案的所有訊息。 傳送至函式的訊息會以特定的順序排列。 根據相同的 token，.cpl 專案需要以特定方式處理訊息。

首先， [](/windows/win32/api/cpl/nc-cpl-applet_proc) \_ 當 Windows 第一次載入主控台專案時，CPlApplet 函式會接收 CPL 初始訊息。 函數應該執行任何初始化，例如配置記憶體，並傳回非零值。 如果 **CPlApplet** 無法完成初始化，它必須傳回零，將 Windows 導向終止通訊並釋放 DLL。

接下來，如果 cpl \_ 初始訊息成功，Windows 傳送 cpl \_ GETCOUNT 訊息。 接著，函式必須傳回 .dll 檔案所支援的主控台專案數。

然後， [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式會 \_ \_ 針對 .dll 檔案所支援的每個主控台專案，接收一個 cpl 查詢訊息和一個 cpl NEWINQUIRE 訊息。 函數會以您的專案相關資訊填入 [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) 或 [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) 結構，例如其名稱、圖示和描述性字串。 大部分的應用程式都應該處理 CPL \_ 查詢訊息，並忽略 cpl \_ NEWINQUIRE 訊息。 CPL \_ 查詢訊息以 Windows 可快取的形式提供資訊，進而提升效能。 \_只有當您需要變更專案的圖示，或根據電腦的狀態顯示字串時，才會使用 CPL NEWINQUIRE 訊息。 \_Windows Vista 中的 [**開始**] 功能表搜尋時，找不到使用 CPL NEWINQUIRE 主控台專案，因為它依賴快取。

接著， [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式會接收 CPL \_ DBLCLK 訊息作為通知，表示使用者已選擇代表主控台專案的圖示。 函式可能會在任何次數的情況下接收此訊息。 此訊息包含在對 [**CPL \_ INQUIRE**](cpl-inquire.md)或 [**cpl \_ NEWINQUIRE**](cpl-newinquire.md)的呼叫中，于 [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo)或 [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa)結構中傳回的專案識別碼和 **lpData** 指標。 函數應該會顯示對應的對話方塊，並處理後續的使用者輸入。

除了 CPL \_ DBLCLK， \_ 如果使用輸入參數叫用主控台專案（例如從命令提示字元或從其他程式），就可以傳送 cpl STARTWPARMS 訊息。 訊息包含專案識別碼以及其他參數字串。

在控制應用程式終止之前， [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 會 \_ 針對 .dll 檔案所支援的每個主控台專案，接收一次 CPL 停止訊息。 此訊息包含主控台專案的識別碼，以及在對 [**CPL \_ INQUIRE**](cpl-inquire.md)或 [**cpl \_ NEWINQUIRE**](cpl-newinquire.md)的呼叫中， [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo)或 [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa)結構中傳回的 **lpData** 指標。 函數應該釋放它為指定對話方塊配置的任何記憶體。

在最後一個 CPL \_ 停止訊息之後， [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 會接收 CPL 結束 \_ 訊息。 函式應該釋放所有剩餘的已配置記憶體，並取消註冊任何可能已註冊的私用視窗類別。 在函式從此訊息傳回之後，Windows 藉由呼叫 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)函式來釋放主控台專案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[主控台專案](control-panel-applications.md)
</dt> <dt>

[使用者體驗指南](user-experience-guidelines.md)
</dt> <dt>

[註冊主控台專案](registering-control-panel-items.md)
</dt> <dt>

[使用 CPLApplet](using-cplapplet.md)
</dt> <dt>

[執行主控台專案](executing-control-panel-items.md)
</dt> <dt>

[擴充系統主控台專案](extending-system-control-panel-items.md)
</dt> <dt>

[指派主控台分類](assigning-control-panel-categories.md)
</dt> <dt>

[建立主控台專案的可搜尋工作連結](creating-searchable-task-links.md)
</dt> <dt>

[在 Windows Vista 下存取保管庫模式下的主控台](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
