---
description: 作業物件可讓您將處理序群組當作一個單位來管理。 工作物件是 namable、安全實體、可共用的物件，可控制與其相關聯之進程的屬性。
ms.assetid: 59296384-5e78-44dd-8019-f1df6668928b
title: 工作物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e6d9758faf2b66f047ca60dbba91601b202b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319164"
---
# <a name="job-objects"></a>工作物件

*工作物件* 允許將進程群組作為一個單位來管理。 工作物件是 namable、安全實體、可共用的物件，可控制與其相關聯之進程的屬性。 在作業物件上執行的作業會影響與該作業物件關聯的所有處理序。 範例包括強制執行限制，例如工作集大小和處理優先權，或終止與作業相關聯的所有進程。

-   [建立作業](#creating-jobs)
-   [管理作業中的進程](#managing-processes-in-jobs)
-   [作業限制和通知](#job-limits-and-notifications)
-   [作業的資源帳戶處理](#resource-accounting-for-jobs)
-   [管理工作物件](#managing-job-objects)
-   [管理使用工作物件的進程樹狀結構](#managing-a-process-tree-that-uses-job-objects)

## <a name="creating-jobs"></a>建立作業

若要建立工作物件，請使用 [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta) 函數。 建立作業時，不會有任何進程與作業相關聯。

若要將處理常式與作業產生關聯，請使用 [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) 函數。 在處理常式與作業相關聯之後，無法中斷關聯。 進程可以與嵌套作業階層中的多個作業相關聯。 如需詳細資訊，請參閱 [Nested 作業](nested-jobs.md)。

**Windows 7、Windows server 2008 R2、WINDOWS XP SP3、Windows server 2008、Windows Vista 和 Windows server 2003：** 進程只能與一個作業相關聯。 無法將作業嵌套。 在 Windows 8 和 Windows Server 2012 中新增了將作業加入的功能。

當您呼叫 [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta) 函式時，可以指定工作物件的安全描述項。 如需詳細資訊，請參閱 [工作物件安全性和存取權限](job-object-security-and-access-rights.md)。

## <a name="managing-processes-in-jobs"></a>管理作業中的進程

在處理常式與作業相關聯之後，依預設，它使用 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) 建立的任何子進程也會與作業產生關聯。  (使用 Win32 進程建立的子進程 [**\_ 。建立**](../cimwin32prov/create-method-in-class-win32-process.md) 未與作業相關聯 ) 。若要變更此預設行為，您可以設定 [擴充限制工作 \_ 物件 \_ 限制 \_ \_ ] BREAKAWAY [確定] 或 \_ [工作物件 \_ 限制無訊息 \_ \_ ] BREAKAWAY 作業的 [ \_ 確定]。

-   如果作業的 [延長限制工作 \_ 物件 \_ 限制 \_ ] BREAKAWAY \_ [確定]，而且父進程是以 [從工作建立 BREAKAWAY] 旗標建立的，則 \_ \_ \_ 父進程的子進程不會與作業產生關聯。
-   如果作業的 [擴充限制] 工作 \_ 物件 \_ 限制 \_ 無訊息 \_ BREAKAWAY \_ [確定]，則任何與作業相關聯之父進程的子進程都不會與作業產生關聯。 使用「從作業建立 BREAKAWAY」旗標建立父進程並不是必要的 \_ \_ \_ 。

如果作業是嵌套的，則階層中父工作的 breakaway 設定會影響子進程是否與階層中的另一個作業相關聯。 如需詳細資訊，請參閱 [Nested 作業](nested-jobs.md)。

若要判斷進程是否正在作業中執行，請使用 [**IsProcessInJob**](/windows/win32/api/jobapi/nf-jobapi-isprocessinjob) 函數。

若要終止目前與工作物件相關聯的所有處理常式，請使用 [**TerminateJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-terminatejobobject) 函數。

## <a name="job-limits-and-notifications"></a>作業限制和通知

作業可以在與作業相關聯的每個進程上強制執行限制，例如工作集大小、進程優先順序，以及工作的結束時間限制。 如果與作業相關聯的進程嘗試從作業所建立的限制增加其工作集大小或處理優先權，函式呼叫會成功，但會以無訊息方式略過。 作業也可以設定在超過通知時觸發通知，但允許工作繼續執行的限制。

若要設定作業的限制，請使用 [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) 函數。 如需可針對作業設定的可能限制清單，請參閱下列主題：

-   [**JOBOBJECT \_ 基本 \_ 限制 \_ 資訊**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_limit_information)
-   [**JOBOBJECT \_ 基本 \_ UI \_ 限制**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_ui_restrictions)
-   [**JOBOBJECT \_ CPU \_ 速率 \_ 控制 \_ 資訊**](/windows/desktop/api/Winnt/ns-winnt-jobobject_cpu_rate_control_information)
-   [**JOBOBJECT \_ 延伸的 \_ 限制 \_ 資訊**](/windows/desktop/api/WinNT/ns-winnt-jobobject_extended_limit_information)
-   [**JOBOBJECT \_ 通知 \_ 限制 \_ 資訊**](/windows/desktop/api/WinNT/ns-winnt-jobobject_notification_limit_information)

您必須針對與工作物件相關聯的每個進程個別設定安全性限制。 如需詳細資訊，請參閱 [進程安全性和存取權限](process-security-and-access-rights.md)。

**WINDOWS XP SP3 和 Windows Server 2003：**[**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject)函式可以用來設定與工作物件相關聯之所有進程的安全性限制。 從 Windows Vista 開始，必須針對與工作物件相關聯的每個進程個別設定安全性限制。

如果作業是嵌套的，則階層中的父作業會影響針對作業所強制執行的限制。 如需詳細資訊，請參閱 [Nested 作業](nested-jobs.md)。

如果作業有相關聯的 i/o 完成埠，則會在超過特定的作業限制時收到通知。 當超過限制或某些其他事件發生時，系統會將訊息傳送至完成通訊埠。 若要將完成埠與作業產生關聯，請使用 [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) 函式搭配工作物件資訊類別 **JobObjectAssociateCompletionPortInformation** 和 [**JOBOBJECT \_ 關聯 \_ 完成 \_ 埠**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port) 結構的指標。 當工作處於非使用中狀態時，最好這麼做，以降低在完成埠關聯期間變更狀態的進程可能遺失通知的機會。

所有訊息都會直接從作業傳送，就像作業已呼叫 [**PostQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-postqueuedcompletionstatus) 函數一樣。 執行緒必須使用 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函式來監視完成埠，以挑選訊息。 請注意，除了使用 **JobObjectNotificationLimitInformation** 資訊類別設定的限制以外，不保證會將訊息傳遞至完成埠;如果訊息無法送達，則不一定表示事件未發生。 具有 **JobObjectNotificationLimitInformation** 設定的限制通知會保證抵達完成的埠。 如需可能的訊息清單，請參閱 [**JOBOBJECT \_ 關聯 \_ 完成 \_ 埠**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port)。

## <a name="resource-accounting-for-jobs"></a>作業的資源帳戶處理

工作物件會記錄其所有相關進程（包括已終止的程式）的基本帳戶處理資訊。 若要取得此帳戶處理資訊，請使用 [**QueryInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-queryinformationjobobject) 函數。 如需針對工作維護的會計資訊清單，請參閱下列主題：

-   [**JOBOBJECT \_ 基本 \_ 帳戶處理 \_ 資訊**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_accounting_information)
-   [**JOBOBJECT \_ 基本 \_ 和 \_ IO 的 \_ 帳戶處理 \_ 資訊**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_and_io_accounting_information)

如果工作物件是嵌套的，每個子工作的計量資訊都會在其父工作中匯總。 如需詳細資訊，請參閱 [Nested 作業](nested-jobs.md)。

## <a name="managing-job-objects"></a>管理工作物件

工作物件的狀態會在其所有處理常式終止時設定為已終止，因為已超過指定的工作時間限制。 使用 [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) 或 [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) 來監視此事件的工作物件。

若要取得現有工作物件的控制碼，請使用 [**OpenJobObject**](/windows/desktop/api/WinBase/nf-winbase-openjobobjecta) 函式，並在建立物件時指定指定給該物件的名稱。 只有命名的工作物件可以開啟。

若要關閉工作物件控制碼，請使用 [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) 函數。 當最後一個控制碼已關閉，且所有相關聯的進程都已終止時，作業就會損毀。 但是，如果作業在 \_ \_ 指定的作業關閉旗標上有工作物件限制 \_ 終止 \_ ，則 \_ \_ 關閉最後一個工作物件控制碼會終止所有相關聯的處理常式，然後終結工作物件本身。 如果在 \_ \_ 指定的 \_ 作業關閉旗標上，將工作物件限制終止 \_ ，則 \_ \_ 關閉最後一個工作物件控制碼，就會終止階層中與作業及其子作業相關聯的所有進程。

## <a name="managing-a-process-tree-that-uses-job-objects"></a>管理使用工作物件的進程樹狀結構

從 Windows 8 和 Windows Server 2012 開始，應用程式可以使用 [嵌套作業](nested-jobs.md) 來管理使用多個工作物件的進程樹狀結構。 不過，必須在 Windows 7、Windows Server 2008 R2 或較早版本的 Windows 上執行且不支援嵌套作業的應用程式，必須以其他方式管理進程樹狀結構。

如果工具必須管理使用工作物件的流程樹狀結構，而且無法使用嵌套作業，則工具和流程樹狀結構的成員都必須合作。 使用下列其中一個選項：

-   使用工作 \_ 物件 \_ 限制無 \_ 訊息 \_ BREAKAWAY \_ 確定限制。 如果工具使用這種限制，則無法監視整個進程樹狀結構。 此工具只能監視它新增至作業的進程。 如果這些處理常式建立子進程，則它們不會與作業相關聯。 在此選項中，子進程可以與其他工作物件相關聯。
-   使用 [工作 \_ 物件 \_ 限制 \_ \_ ] BREAKAWAY [確定] 限制。 如果工具使用這項限制，則可以監視整個進程樹狀結構，但樹狀結構中任何成員明確地中斷樹狀結構的進程除外。 樹狀結構的成員可以在新的工作物件中建立子進程，方法是呼叫 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函式搭配 create \_ BREAKAWAY \_ FROM \_ job 旗標，然後呼叫 [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) 函數。 否則，成員必須處理 **AssignProcessToJobObject** 失敗的情況。

    \_ \_ \_ 如果工具未監視樹狀結構，則 [從作業建立 BREAKAWAY] 旗標沒有任何作用。 因此，這是慣用的選項，但需要事先瞭解受監視的進程。

-   藉由設定 [工作 \_ 物件 \_ 限制 \_ \_ ] BREAKAWAY [確定] 或 [工作 \_ 物件 \_ 限制無訊息 \_ \_ BREAKAWAY \_ 確定限制]，以防止任何種類的 breakaways。 在此選項中，工具可以監視整個進程樹狀結構。 但是，如果子進程嘗試透過呼叫 [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject)來將本身或另一個子進程與作業產生關聯，則呼叫會失敗。 如果程式是設計為與特定作業相關聯，此失敗可能會使進程無法正常運作。

 

 
