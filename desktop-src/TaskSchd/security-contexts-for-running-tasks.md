---
title: 工作的安全性內容
description: 工作會在特定的安全性內容下註冊並執行。
ms.assetid: be86eb9f-f6ec-4dce-afe8-e3314a74062a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329f354518daeb11a5f330ae3fdc2c332b66d5c3
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104374598"
---
# <a name="security-contexts-for-tasks"></a>工作的安全性內容

工作會在特定的安全性內容下註冊並執行。 使用者可以建立成功註冊、更新、刪除或執行工作的應用程式，但使用者必須在註冊工作時提供正確的認證，而且應用程式必須以正確的許可權在進程中執行。

## <a name="specifying-credentials"></a>指定認證

您可以指定工作的安全性內容，方法是指定 [**ITaskFolder：： RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask)或 [**ITaskFolder：： RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)中的認證 ([**TaskFolder**](taskfolder-registertask.md)或 [**RegisterTask. TaskFolder**](taskfolder-registertaskdefinition.md) ，以編寫腳本) 方法，或是將主體指派給 RegisterTaskDefinition ([**ITaskDefinition**](taskdefinition-principal.md)的 [**principal 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal)) 的主體。 如果為工作定義建立主體，然後使用 **RegisterTaskDefinition** 方法來註冊工作定義，並在方法參數中指定不同的認證，則在 **RegisterTaskDefinition** 方法中指定的認證將會覆寫主體中的認證。 如果使用 XML 來建立工作定義的主體，然後使用 **RegisterTask** 方法來註冊工作的 xml，並在方法參數中指定不同的認證，則在 **RegisterTask** 方法中指定的認證將會覆寫主體中的認證。

您可以在註冊工作或指定工作的原則時，指定使用者帳戶或群組。 使用者帳戶或群組的安全性內容會用於工作的安全性內容。 在這些方法和屬性中，您也可以定義登入類型。 登入類型是由工作 [**\_ 登入 \_ 類型**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) 列舉中的其中一個常數所定義。

使用工作 \_ 登入 \_ 密碼或工作登入 S4U 旗標注冊的工作， \_ \_ 只會在指定的使用者已啟用 [登入為批次許可權] 時啟動。 系統管理員和備份操作員群組使用者預設會啟用此許可權。

當您呼叫 [**ITaskService：： connect**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-connect) ([**TaskService**](taskservice-connect.md) ，) 方法的腳本中，任何後續的方法呼叫工作排程器服務都會使用傳遞給 **Connect** 方法的認證。 使用互動式登入類型註冊工作時，請務必考慮這一點。 當您註冊的工作具有等於工作登入互動式權杖的登入類型，而且該工作在工作 \_ \_ 定義的 \_ [**Principal**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal) 屬性中指定的認證（在要 [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)的參數中指定或在傳遞至 [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask)的 XML 中指定）時，會使用呼叫 **Connect** 方法的使用者認證來註冊該工作。

## <a name="user-account-control-uac-security-for-tasks"></a> (UAC) 安全性的使用者帳戶控制

 (UAC) 的[使用者帳戶控制](https://www.microsoft.com/technet/windowsvista/security/uac.mspx)可讓使用者執行一般功能，例如執行程式和儲存和修改資料，而不需要公開系統管理許可權。 依預設，當 UAC 開啟時，會以低層級許可權執行工作。 工作可以藉由從 IPrincipal ([**Principal.) RUNLEVEL**](principal-runlevel.md)之 [**RUNLEVEL 屬性**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel)的工作 [**\_ RUNLEVEL \_**](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type)別列舉設定許可權等級，來指定要以較高的許可權或低許可權執行這些工作。 **RunLevel** 屬性的值會決定工作的動作將執行的許可權層級。 如果工作的動作必須具有較高的許可權才能執行，則您必須將 **RunLevel** 屬性設定為 [ **task \_ RunLevel \_ 最高**]。 如果工作是使用工作安全性內容的 Administrators 群組來註冊的，則您也必須將 [ **RunLevel** ] 屬性設定為 [ **task \_ RunLevel \_** ] （如果您想要執行此工作）。 如果工作是使用內建 \\ 系統管理員帳戶或本機系統或本地服務帳戶來註冊的，則會忽略 **RunLevel** 屬性。 如果已關閉使用者帳戶控制 (UAC) ，也會忽略屬性值。 **RunLevel** 屬性的值不會影響執行或刪除工作所需的許可權。

> [!Note]  
> 將作業系統從 Windows XP 升級至 Windows Vista 之後， \\ 在 WINDOWS xp 上使用內建系統管理員帳戶註冊的工作會將 [**RunLevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) 屬性設定為 **TASK \_ RunLevel \_ LUA**。 這可能會導致某些工作失敗。 您可以手動更新此屬性，以確保所有工作將會執行。

 

在低許可權的程式中，您無法註冊 [**RunLevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel)屬性等於 **task \_ RunLevel \_ 最高** 的工作，但您可以使用等於 **task \_ RunLevel \_ LUA** 的 **RunLevel** 屬性來註冊工作。 工作動作將以低許可權執行。 您不能將工作註冊為內建/系統管理員、本機系統或群組。

從提升許可權的程式中，您可以使用等於 **task \_ RunLevel \_ 最高** 或工作 **\_ RunLevel \_ LUA** 的 [**RunLevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel)屬性來註冊工作。 除非您使用的是系統管理員帳戶，否則工作會以 **RunLevel** 屬性所決定的許可權層級執行，而在此情況下，工作會以較高的許可權執行。

從提升許可權的程式中，您可以註冊工作排程器1.0 工作。 工作排程器服務會將工作的執行層級設定為 [工作 \_ RUNLEVEL] \_ 最高，且工作會以較高的許可權執行。

從低許可權的程式中，您也可以註冊工作排程器1.0 工作。 工作排程器服務會將工作的執行層級設定為 TASK \_ RUNLEVEL \_ LUA，而且工作會以低許可權執行。 如果這項工作是從提高許可權的進程更新，工作的執行層級將維持 TASK \_ RUNLEVEL \_ LUA。

## <a name="security-for-registering-tasks"></a>註冊工作的安全性

當您從屬於系統管理員群組成員的帳戶註冊工作時，您只需要在下列情況下，于註冊工作時指定密碼：

-   如果您在帳戶的安全性內容或不同的使用者帳戶下註冊要執行的工作，並在 \_ \_ [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) 或 [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) 方法中使用 [工作登入密碼] 旗標。
-   如果您註冊要在不同使用者帳戶的安全性內容下執行的工作，並在 \_ \_ [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) 或 [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) 方法中使用工作登入 S4U 旗標。

當您使用工作 \_ 登入 \_ S4U 旗標或 \_ \_ [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) 或 [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) 方法中的工作登入密碼旗標注冊工作時，您無法使用使用者群組做為工作的安全性內容。

當您從不是系統管理員群組成員的使用者帳戶註冊工作時，如果您在帳戶的安全性內容下註冊要執行的工作，而且您使用 S4U 或互動式登入類型，則在註冊工作時，不需要指定密碼。 否則，您必須在註冊工作時指定密碼。 此外，您無法使用本地服務帳戶或工作安全性內容的群組來註冊工作。

## <a name="security-for-reading-updating-deleting-and-running-tasks"></a>讀取、更新、刪除和執行工作的安全性

依預設，建立工作的使用者可以讀取、更新、刪除和執行工作。 使用者必須具有工作檔案的「檔案寫入」許可權，才能更新工作、使用工作檔案的「讀取」許可權來讀取工作、將工作檔案的「刪除」許可權用於刪除工作，以及使用 IRegisteredTask：： Run 或 RunEx 方法來執行工作，以使用 [**：： run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run)或 [](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex)方法來執行工作， ([**RegisteredTask. run**](registeredtask-run.md)和 [**RunEx**](registeredtask-runex.md)編寫腳本) 。 Administrators 群組的成員或系統帳戶可以讀取、更新、刪除和執行任何工作。 Users 群組、LocalService 帳戶和 NetworkService 帳戶的成員，只能讀取、更新、刪除和執行他們所建立的工作。 當工作檔案的 DACL 變更時，此預設行為會變更，在此情況下，DACL 會定義哪些使用者具有檔案寫入、讀取、執行和刪除許可權。 若要設定工作檔的許可權，請使用 IRegisteredTask. SetSecurityDescriptor 方法 (RegisteredTask. SetSecurityDescriptor 來撰寫腳本) 或在使用 [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) 或 [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) 方法註冊工作時設定安全描述項。

如果工作更新需要變更工作的 DACL，則除了讀取/寫入權限之外，使用者還必須具有 WriteDAC 許可權，才能更新工作。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作註冊資訊](task-registration-information.md)
</dt> <dt>

[關於工作排程器](about-the-task-scheduler.md)
</dt> <dt>

[工作安全性強化](task-security-hardening.md)
</dt> <dt>

[**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md)
</dt> <dt>

[**ITaskFolder：： RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)
</dt> <dt>

[**ITaskDefinition 的 Principal 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal)
</dt> <dt>

[**工作 \_ 登入 \_ 類型**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)
</dt> </dl>

 

 




