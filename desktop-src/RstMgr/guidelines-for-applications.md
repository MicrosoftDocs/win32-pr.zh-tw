---
title: 應用程式的指導方針
description: 在 Windows Vista 和 Windows Server 2008 上執行的應用程式應該遵守這些指導方針，以確保重新開機管理員可以視需要關閉並重新啟動應用程式，以安裝更新。
ms.assetid: 97b1df63-65a9-47b4-891b-e4a754882b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebace21e09956c68d34c90775c5ea646a8b2dd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682939"
---
# <a name="guidelines-for-applications"></a>應用程式的指導方針

在 Windows Vista 和 Windows Server 2008 上執行的應用程式應該遵守這些指導方針，以確保重新開機管理員可以視需要關閉並重新啟動應用程式，以安裝更新。 服務可以使用 [服務指導方針](guidelines-for-services.md)中所述的指導方針。

-   重新開機管理員會將 *lParam* 參數設定為 **ENDSESSION \_ CLOSEAPP** (0x1) 的 [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession)通知，藉以查詢 GUI 應用程式是否有關機。 應用程式在收到 **WM \_ QUERYENDSESSION** 訊息時不應關機，因為另一個應用程式可能尚未準備好關閉。 如果應用程式已準備好要關閉和重新開機，GUI 應用程式應該接聽 **WM \_ QUERYENDSESSION** 訊息，並傳回 **TRUE** 值。 如果沒有任何應用程式傳回值 **FALSE**，重新開機管理員就會將 *lParam* 參數設定為 **ENDSESSION \_ CLOSEAPP** (0x1) ，並將 *Wparam* 參數設定為 **TRUE**，以傳送 [**WM \_ ENDSESSION**](/windows/desktop/Shutdown/wm-endsession)訊息。 只有在應用程式收到 **WM \_ ENDSESSION** 訊息時，才會關閉應用程式。 重新開機管理員也會針對在接收 **WM \_ ENDSESSION** 時未關機的 GUI 應用程式傳送 [**WM \_ 關閉**](../winmsg/wm-close.md)訊息。 如果任何 GUI 應用程式藉由傳回值 **FALSE** 來回應 **WM \_ QUERYENDSESSION** 訊息，則會取消關閉。 但是，如果強制關機，則不論是否已終止應用程式。
-   當 GUI 應用程式收到 [**WM \_ ENDSESSION**](/windows/desktop/Shutdown/wm-endsession) 訊息時，應用程式應該準備自己在指定的超時時間內關機。 應用程式至少應該藉由儲存重新開機後所需的任何使用者資料和狀態資訊來做好準備。 建議應用程式定期儲存使用者資料和狀態。
-   重新開機管理員會將 **CTRL \_ + \_ 事件** 通知傳送給必須關閉並重新啟動的主控台應用程式。 當主控台應用程式收到 **CTRL + \_ \_ 事件** 通知時，應用程式應該採取必要的動作，以便在指定的超時時間內準備關機。 主控台應用程式至少應定義 [*HandlerRoutine*](/windows/console/handlerroutine) 函式來處理 **CTRL + \_ \_ 事件** 通知，並且應儲存重新開機後將需要的任何使用者資料和狀態資訊。 建議應用程式定期儲存使用者資料和狀態。
-   如果有任何應用程式未關閉以回應關機訊息，則安裝程式可以使用 [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)函式的 **RmForceShutdown** 選項強制關閉應用程式。 當安裝程式指定強制關機時，重新開機管理員會嘗試透過傳送關機訊息來完全關閉應用程式，但如果失敗，則會強制關機。 GUI 應用程式和主控台應用程式可以強制關機，以啟用重大安全性更新的安裝。 因為這可能會導致資料遺失，所以應用程式應該處理關閉訊息，並在需要時完全關閉。
-   應用程式應該使用 [**RegisterApplicationRestart**](/windows/desktop/api/winbase/nf-winbase-registerapplicationrestart) 函式註冊重新開機。 重新開機管理員只能重新開機已註冊要重新開機的應用程式。 這是重新開機管理員可以判斷重新開機應用程式時所要使用之命令列命令的唯一方式。 如果應用程式必須以某些儲存的狀態或資料重新開啟，則該資訊必須包含在為應用程式註冊的命令列命令中。
    > [!Note]  
    > 如果重新開機的應用程式必須在其執行所在的相同目錄中執行，則應用程式必須儲存目錄資訊，然後在重新開機後變更為目錄。

     

    > [!Note]  
    > [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart)函式不會重新開機未以目前登入的使用者身分執行的應用程式。 例如， **RmRestart** 函式不會重新開機使用 **run as** 命令啟動的應用程式，該命令不會以目前登入的使用者身分執行。 這些應用程式必須以手動方式重新開機。

     

-   當重新開機管理員判斷需要重新開機系統以安裝更新時，它不會關閉任何應用程式和服務。 相反地，它會將此程式保留給安裝程式，以決定何時要排程系統重新開機並安裝更新。 安裝程式可以使用 [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) 函式搭配 **EWX \_ RESTARTAPPS** 旗標或 [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) 函式搭配 **SHUTDOWN \_ RESTARTAPPS** 旗標，減少需要重新開機系統的使用者所造成的中斷。 使用這些旗標可確保在系統重新開機後重新開機已註冊重新開機的應用程式，以將對使用者的影響降到最低。

 

 