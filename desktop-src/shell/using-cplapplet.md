---
description: 在 Windows Vista 之前，您建立了一個 .dll 檔案，並將它命名為 cpl 副檔名來建立主控台專案。
ms.assetid: 258dae28-c054-4392-b0e9-99493f23c814
title: 使用 CPLApplet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1e59b29dd7c082822ed63d425dd4967a542b5d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973112"
---
# <a name="using-cplapplet"></a>使用 CPLApplet

在 Windows Vista 之前，您建立了一個 .dll 檔案，並將它命名為 cpl 副檔名來建立主控台專案。 此檔案已匯出 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式。 在 Windows Vista 和更新版本中仍支援此配置，本主題將討論此配置。 不過，新主控台專案的指導方針會建議更簡單的方法，並以使用工作流程配置的 .exe 檔案形式來建立主控台專案。

當主控台載入 .dll (或 cpl) 檔案時，它會呼叫 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式來取得資訊，例如檔案所裝載的主控台專案數，以及每個專案的相關資訊。 主控台也會在專案的視窗初始化、開啟或關閉時呼叫函式。

當 Windows 第一次載入主控台專案時，它會抓取 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式的位址，並接著使用該位址呼叫函式並傳遞訊息。 它可能會傳送下列訊息。



| 訊息                                     | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CPL \_ DBLCLK**](cpl-dblclk.md)           | 傳送以通知 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) ，使用者已選擇與指定主控台專案相關聯的圖示。 **CPlApplet** 應該會顯示指定專案的對話方塊，並執行任何使用者指定的工作。 **CPlApplet** *lParam1* 參數是一個整數，代表主控台專案的以零為基底的索引。 *LParam2* 參數是在 [**CPL \_ INQUIRE**](cpl-inquire.md)或 [**Cpl \_ NEWINQUIRE**](cpl-newinquire.md)訊息 [**的 CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo)或 [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa)結構中傳回的 **lpData** 指標。 傳回值會被忽略。                                                                |
| [**CPL \_ 結束**](cpl-exit.md)               | 在最後一個 CPL \_ 停止訊息之後傳送，而且在 Windows 使用 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) 函式釋放包含主控台專案的 DLL 之前。 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 應該釋放任何剩餘的記憶體，並準備關閉。 傳回值會被忽略。                                                                                                                                                                                                                                                                                                                                                                                                |
| [**CPL \_ GETCOUNT**](cpl-getcount.md)       | 在 CPL \_ INIT 訊息之後傳送，以 [**提示 CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 傳回數位，指出它所支援的 subprograms 數目。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**CPL \_ INIT**](cpl-init.md)               | 在載入包含主控台專案的 DLL 之後立即傳送。 訊息會提示 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 執行初始化程式，包括記憶體配置。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**CPL \_ 查詢**](cpl-inquire.md)         | 在 CPL \_ GETCOUNT 訊息之後傳送，以提示 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 提供指定之 subprogram 的相關資訊。 *LParam1* 值是一個整數，代表所要求的資訊之 subprogram 的以零為基底的索引。 **CPlApplet** 的 *lParam2* 參數會指向 [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo)結構。 傳回值會被忽略。                                                                                                                                                                                                                                                                                                    |
| [**CPL \_ NEWINQUIRE**](cpl-newinquire.md)   | 在 CPL \_ GETCOUNT 訊息之後傳送，以提示 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 提供指定主控台專案的相關資訊。 *LParam1* 值是一個整數，代表所要求的資訊之 subprogram 的以零為基底的索引。 *LParam2* 參數是指向 [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa)結構的指標。 \_通常應忽略 CPL NEWINQUIRE。 您的應用程式應該只處理 \_ Windows 95、Microsoft Windows NT 4.0 和更新版本系統上的 cpl 查詢，因為當使用 CPL NEWINQUIRE 時，主控台的效能會受到影響 \_ 。 這是因為無法快取傳回的字串和圖示。 傳回值會被忽略。 |
| [**CPL \_ 選取**](cpl-select.md)           | 已過時。 目前的 Windows 版本不會傳送此訊息。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**CPL \_ STARTWPARMS**](cpl-startwparms.md) | 傳送以通知 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) ，使用者已選擇與指定對話方塊相關聯的圖示。 **CPlApplet** 應該會顯示對應的對話方塊，並執行任何使用者指定的工作。 這則訊息類似于 CPL \_ DBLCLK，但可能會有一些額外的資訊。 *LParam1* 參數是主控台專案編號，而 *lParam2* 則是可能需要的任何額外方向的 **LPCTSTR** 。 如果處理此訊息，則傳回 **TRUE** ;否則 **為 FALSE**。 此訊息適用于 [5.00 版](versions.md) 和更新版本的 Shell32.dll。                                                                                         |
| [**CPL \_ 停止**](cpl-stop.md)               | 在 Windows 卸載主控台擴充功能之前，為 cpl 檔中的每個主控台專案傳送一次。 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 應該釋放與 *lParam1* 中提供之專案編號相關聯的任何記憶體。 *LParam2* 參數是在 [**CPL \_ INQUIRE**](cpl-inquire.md)或 [**Cpl \_ NEWINQUIRE**](cpl-newinquire.md)訊息的 [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo)或 [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa)結構中傳回的 **lpData** 指標。 傳回值會被忽略。                                                                                                                                                                                                       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[主控台專案](control-panel-applications.md)
</dt> <dt>

[使用者體驗指南](user-experience-guidelines.md)
</dt> <dt>

[註冊主控台專案](registering-control-panel-items.md)
</dt> <dt>

[主控台訊息處理](message-processing.md)
</dt> <dt>

[執行主控台專案](executing-control-panel-items.md)
</dt> <dt>

[擴充系統主控台專案](extending-system-control-panel-items.md)
</dt> <dt>

[指派主控台分類](assigning-control-panel-categories.md)
</dt> <dt>

[建立主控台專案的可搜尋工作連結](creating-searchable-task-links.md)
</dt> <dt>

[在 Windows Vista 下存取安全模式下的主控台](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
