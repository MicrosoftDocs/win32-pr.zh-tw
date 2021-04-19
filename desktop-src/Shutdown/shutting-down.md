---
description: 有三種方式可讓應用程式關閉本機或遠端電腦：將 systemshut 向下關閉系統，然後重新開機應用程式的 itshut，關閉並重新啟動系統，然後重新開機任何已註冊要重新開機的應用程式
ms.assetid: acadf58f-3f68-4fa1-bdcf-8f85c8479263
title: 關閉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e436dd9e3b115112e63b0440b4d51de4c7f9f619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994506"
---
# <a name="shutting-down"></a>關閉

有三種方式可讓應用程式關閉本機或遠端電腦：

-   關閉系統
-   將系統關機並重新啟動
-   關閉應用程式、關閉並重新啟動系統，然後重新開機任何已註冊要重新開機的應用程式

若要關閉系統，請使用 [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) 函式搭配 EWX \_ 關機旗標。 如需範例，請參閱 [如何關機系統](how-to-shut-down-the-system.md)。 若要關閉並重新啟動系統，請使用 EWX \_ 重新開機旗標。 若要使用 [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) 函式重新開機任何已註冊要重新開機的應用程式，請使用 EXW \_ RESTARTAPPS 旗標。

[**InitiateShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiateshutdowna)、 [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)和 [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)函式會啟動計時器，並顯示會提示使用者登出的對話方塊。 當這個對話方塊顯示時， [**AbortSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna) 函式可以停止計時器，並防止電腦關機。 但是，如果計時器過期，則會關閉電腦。 這些函式也可以在關機操作後重新開機電腦。 如需詳細資訊，請參閱 [顯示關閉對話方塊](displaying-the-shutdown-dialog-box.md)。

## <a name="shutdown-notifications"></a>關機通知

具有視窗和訊息佇列的應用程式會透過 [**wm \_ QUERYENDSESSION**](wm-queryendsession.md) 和 [**wm \_ ENDSESSION**](wm-endsession.md) 訊息接收關機通知。 這些應用程式應該會傳回 **TRUE** ，表示可以終止它們。 除非絕對必要，否則應用程式不應封鎖系統關機。 應用程式應該在處理 **WM \_ ENDSESSION** 時執行任何必要的清除。 具有未儲存資料的應用程式可以將資料儲存至暫存位置，並在應用程式下次啟動時還原資料。 建議應用程式經常儲存其資料和狀態。例如，會在使用者起始的儲存作業之間自動儲存資料，以減少在關機時要儲存的資料量。

主控台應用程式會在其處理常式常式中接收關機通知。 若要註冊主控台處理常式，請使用 [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) 函數。

服務應用程式會在其處理常式常式中接收關機通知。 若要註冊服務控制處理常式，請使用 [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) 函數。

## <a name="blocking-shutdown"></a>封鎖關機

如果應用程式必須封鎖可能的系統關閉，則可以呼叫 [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) 函數。 呼叫端會提供將向使用者顯示的原因字串。 原因字串應該簡短且清楚明瞭，提供使用者決定是否要繼續關閉系統所需的資訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何關機系統](how-to-shut-down-the-system.md)
</dt> </dl>

 

 
