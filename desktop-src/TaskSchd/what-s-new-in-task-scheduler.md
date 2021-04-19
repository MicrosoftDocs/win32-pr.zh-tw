---
title: 工作排程器的新功能
description: 不同工作排程器版本所引進的新功能清單。
ms.assetid: 43fbbbd2-6e97-4ba5-9474-23c5e2b33612
keywords:
- 工作排程器工作排程器，新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5245ab4e681af937924cfbd217095009d80d6a11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991655"
---
# <a name="whats-new-in-task-scheduler"></a>工作排程器的新功能

下列變更摘要說明不同工作排程器版本的新功能。

## <a name="windows-10-and-windows-server-2016"></a>Windows 10 (和 Windows Server 2016) 

Windows 10 引進了下列工作排程器變更。

-   當省電模式開啟時，只有當工作為時，才會觸發 Windows 工作排程器工作：

    -   未設定為 **只在電腦閒置時才啟動工作** ... (工作不使用 [**IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings)) 
    -   未設定為在自動維護期間執行 (工作不會使用 [**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings)) 
    -   設定為 **只有在使用者登入時才會執行** (工作 [**LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) 是工作 **登入 \_ \_ 互動式 \_ 權杖** 或工作 **登入 \_ \_ 群組**) 

    所有其他觸發程式都會延遲到省電模式關閉為止。 如需有關在應用程式中存取省電模式狀態的詳細資訊，請參閱 [**系統 \_ 電源 \_ 狀態**](/windows/desktop/api/winbase/ns-winbase-system_power_status)。 如需有關省電模式的一般資訊，請參閱 [硬體元件指導方針中的省電模式 () ](/windows-hardware/design/component-guidelines/battery-saver)。

-   基於安全性理由，非系統管理員使用者無法查看或管理另一位使用者所建立的 Windows 工作排程器工作。

## <a name="windows-8"></a>Windows 8

Windows 8 引進下列工作排程器2.0 變更：

-   Powershell 支援：使用者可以使用 ScheduledTasks powershell 模組來管理 (建立、刪除、修改、明確啟動、停止等 ) Windows 工作排程器工作。
-   受控密碼：系統管理員可以使用 Active Directory 管理的密碼帳戶做為工作主體。 這些工作不再需要強制執行的密碼重設原則。
-   API 變更：引進兩個具有 [**ITaskSettings3**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings3) 介面的新工作設定。
    -   [**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings)：使用這些設定的工作會被視為一種新的排程工作，這些工作會根據指定的週期和期限，在 OS 自動維護期間叫用。
    -   [**Volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile)：設定為 volatile 的工作一律會在 OS 開機時停用，而且必須在必要時明確重新啟用。 「容錯移轉叢集」會利用 Volatile 工作，以確保一次只在一個叢集上排程一個工作實例。
-   整合排程引擎現在支援下列功能：
    -   S4U 登入類型（透過 [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) 元素）。
    -   事件觸發程式的 XPath 查詢值（透過 [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) 元素）。
    -   不允許透過 [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md) 元素進行工作硬終止。
-   此版本中已淘汰的功能
    -   Action： [**sendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) (您可以使用 [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction)搭配 [Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx)的 [傳送 send-mailmessage](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) Cmdlet 作為因應措施) 。
    -   Action： [**showMessage**](taskschedulerschema-showmessage-actiongroup-element.md)。
    -   AT.exe cmdline 公用程式

## <a name="windows-7"></a>Windows 7

Windows 7 中引進了下列工作排程器2.0 變更：

-   使用基礎作業系統所提供的統一排程引擎。
-   能夠拒絕遠端應用程式中的啟動工作，這些工作是在遠端應用程式的本機 (滑軌) 會話
-   工作安全性強化 (針對以「網路服務」或「本機服務」執行的工作，只) ：

    -   能夠將進程權杖安全識別碼指派 (SID) 類型 (例如，不受限制或無) 至工作。
    -   允許工作開發人員要求其工作所需的一組完整許可權。

-   API 變更：

    -   工作安全性強化支援：新的 IPrincipal2 介面引進了新的任務安全性強化功能。
    -   引進了新的 ITaskSettings2 介面的兩個新工作設定。

        -   DisallowStartOnRemoteAppSession：如果是在 [遠端應用程式中，在遠端應用程式中進行 (整合，) ](/openspecs/windows_protocols/MS-WINPROTLP/df36f95e-6a6b-48d6-a3ae-35a17674f546) 會話，則新的 DisallowStartOnRemoteAppSession 設定可能會拒絕工作啟動。
        -   UseUnifiedSchedulingEngine：使用 UseUnifiedSchedulingEngine 設定可為 Windows 工作和服務提供一致的行為，因為它是以統一的方式，由一般全系統排程引擎進行管理。 雖然建議使用整合引擎，但不支援某些工作排程器功能。 如果屬性的組合不允許在統一引擎下執行工作，則會拒絕這類的註冊。
        -   整合排程引擎不支援的工作功能包括：

            -   登入類型：

                -   [工作 \_ 登入 \_ 互動式 \_ 權杖 \_ 或 \_ 密碼](./taskschedulerschema-logontype-principaltype-element.md)

            -   多個實例原則：

                -   [**工作 \_ 實例 \_ 停止 \_ 現有的**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)

            -   動作：

                -   [傳送電子郵件](./taskschedulerschema-sendemail-actiongroup-element.md)
                -   [顯示訊息](./taskschedulerschema-showmessage-actiongroup-element.md)

            -   設定：

                -   [工作網路設定](./taskschedulerschema-networksettings-settingstype-element.md)
                -   [不允許工作硬終止](./taskschedulerschema-allowhardterminate-settingstype-element.md)

            -   觸發程序：

                -   [觸發程式執行時間限制](./taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
                -   [行事曆觸發程式的重複模式]( ./taskschedulerschema-repetition-triggerbasetype-element.md)
                -   [事件觸發程式的 XPath 查詢值]( ./taskschedulerschema-valuequeries-eventtriggertype-element.md)
                -   [每月](./taskschedulerschema-schedulebymonth-calendartriggertype-element.md) 和 [每月星期幾](./taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) 觸發程式類型

## <a name="windows-vista"></a>Windows Vista

工作排程器 2.0 API 應該用於開發在 Windows Vista 上使用工作排程器服務的應用程式。 如需詳細資訊，請參閱 [工作排程器參考](task-scheduler-reference.md) 和 [使用工作排程器](using-the-task-scheduler.md)。

## <a name="windows-2000-windows-xp-and-windows-server-2003"></a>Windows 2000、Windows XP 及 Windows Server 2003

無法使用工作排程器 2.0 API。 使用工作排程器1.0。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> <dt>

[關於工作排程器](about-the-task-scheduler.md)
</dt> </dl>

 

 
