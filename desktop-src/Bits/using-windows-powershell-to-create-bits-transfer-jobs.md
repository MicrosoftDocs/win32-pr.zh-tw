---
title: 使用 Windows PowerShell 建立 BITS 傳送工作
description: 您可以使用 PowerShell Cmdlet 來建立同步和非同步背景智慧型傳送服務 (BITS) 傳送作業。
ms.assetid: 22bcf0d5-36f0-4677-84a7-502b98cfaac2
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: af4879d1fc8f1b25fa0b1b51816432aad3bed8bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688931"
---
# <a name="using-windows-powershell-to-create-bits-transfer-jobs"></a>使用 Windows PowerShell 建立 BITS 傳送工作

您可以使用 PowerShell Cmdlet 來建立同步和非同步背景智慧型傳送服務 (BITS) 傳送作業。

本主題中的所有範例都使用 [BitsTransfer](/previous-versions//dd347701(v=technet.10)) Cmdlet。 若要使用 Cmdlet，請務必先匯入模組。 若要安裝此模組，請執行下列命令： Import-Module BitsTransfer。 如需詳細資訊，請在 PowerShell 提示字元中輸入 **Get-help Start-BitsTransfer** 。

> [!IMPORTANT]
>
> 當您在非互動式內容中執行的進程內（例如 Windows 服務）使用[ \* -BitsTransfer](/previous-versions//dd819413(v=technet.10)) Cmdlet 時，您可能無法將檔案加入至 BITS 作業，這可能會導致暫止狀態。 若要繼續作業，用來建立傳送工作的身分識別必須登入。 例如，在以工作排程器工作的形式執行的 PowerShell 腳本中建立 BITS 工作時，除非已啟用工作排程器的工作設定 [只有在使用者登入時才執行]，否則 BITS 傳送將永遠不會完成。

 

-   [建立同步 BITS 傳送工作](#to-create-a-synchronous-bits-transfer-job)
-   [若要建立具有多個檔案的同步 BITS 傳送工作](#to-create-a-synchronous-bits-transfer-job-with-multiple-files)
-   [若要建立同步 BITS 傳送工作並指定遠端伺服器的認證](#to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server)
-   [從 CSV 檔案建立同步 BITS 傳送工作](#to-create-a-synchronous-bits-transfer-job-from-a-csv-file)
-   [若要建立異步 BITS 傳送工作](#to-create-an-asynchronous-bits-transfer-job)
-   [管理 PowerShell 遠端會話](#to-manage-powershell-remote-sessions)
-   [相關主題](#related-topics)

## <a name="to-create-a-synchronous-bits-transfer-job"></a>建立同步 BITS 傳送工作


```PowerShell
Start-BitsTransfer -Source https://Server01/serverdir/testfile1.txt `
-Destination C:\clientdir\testfile1.txt
```



> [!Note]  
> 使用「音符號」（ (\`) ）來表示分行符號。

 

在上述範例中，檔案的本機和遠端名稱會分別在 *來源* 和 *目的地* 參數中指定。 當檔案傳送完成或進入錯誤狀態時，命令提示字元就會出現。

預設的傳輸類型為 [下載]。 當您將檔案上傳到 HTTP 位置時， *TransferType* 參數必須設定為 [上傳]。

因為 [BitsTransfer](/previous-versions//dd347701(v=technet.10)) Cmdlet 會強制執行參數位置，所以不需要為來源和目的地參數指定參數名稱。 因此，可以簡化此命令，如下所示。


```PowerShell
Start-BitsTransfer https://Server01/serverdir/testfile1.txt C:\clientdir\testfile1.txt
```



## <a name="to-create-a-synchronous-bits-transfer-job-with-multiple-files"></a>若要建立具有多個檔案的同步 BITS 傳送工作


```PowerShell
Start-BitsTransfer -Source C:\clientsourcedir\*.txt `
-Destination c:\clientdir\ -TransferType Download
```



在上述範例中， [BitsTransfer](/previous-versions//dd347701(v=technet.10)) 命令會建立新的 BITS 傳送工作。 所有檔案都會新增至此作業，並依序傳送給用戶端。

> [!Note]  
> 目的地路徑不可以使用萬用字元。 目的地路徑支援相對目錄、根路徑或隱含目錄， (也就是目前目錄) 。 無法使用萬用字元重新命名目的地檔案。 此外，HTTP 和 HTTPS Url 無法使用萬用字元。 萬用字元只有在 UNC 路徑和本機目錄中才有效。

 

## <a name="to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server"></a>若要建立同步 BITS 傳送工作並指定遠端伺服器的認證


```PowerShell
Start-BitsTransfer -DisplayName MyJob -Credential Username\Domain `
-Source https://server01/servertestdir/testfile1.txt -Destination c:\clienttestdir\testfile1.txt `
-ProxyUsage Override -ProxyList @(https://proxy1, 123.24.21.23, proxy3)
```



在上述範例中，使用者會建立 BITS 傳送工作，以從需要驗證的伺服器下載檔案。 系統會提示使用者輸入認證，而 *credential* 參數會將認證物件傳遞給 [BitsTransfer](/previous-versions//dd347701(v=technet.10)) Cmdlet。 使用者會設定明確的 proxy，而且 BITS 傳送工作只會使用 *ProxyList* 參數所定義的 proxy。 *DisplayName* 參數會為 BITS 傳送工作提供唯一的顯示名稱。

## <a name="to-create-a-synchronous-bits-transfer-job-from-a-csv-file"></a>從 CSV 檔案建立同步 BITS 傳送工作


```PowerShell
Import-CSV filelist.txt | Start-BitsTransfer -TransferType Upload
```



> [!Note]  
> " \| " 是管道字元。

 

在上述範例中，使用者會建立從用戶端上傳多個檔案的 BITS 傳送工作。 匯 [入 CSV](/previous-versions//dd347665(v=technet.10)) Cmdlet 會匯入來源和目的地檔案位置，並將它們傳送至 [BitsTransfer](/previous-versions//dd347701(v=technet.10)) 命令。 [BitsTransfer](/previous-versions//dd347701(v=technet.10))命令會為每個檔案建立新的 BITS 傳送工作、將檔案新增至作業，然後將它們依序傳送至伺服器。

Filelist.txt 檔案的內容應該採用下列格式：

``` syntax
Source, Destination
c:\clienttestdir\testfile1.txt, https://server01/servertestdir/testfile1.txt
c:\clienttestdir\testfile2.txt, https://server01/servertestdir/testfile2.txt
c:\clienttestdir\testfile3.txt, https://server01/servertestdir/testfile3.txt
c:\clienttestdir\testfile4.txt, https://server01/servertestdir/testfile4.txt
```

## <a name="to-create-an-asynchronous-bits-transfer-job"></a>若要建立異步 BITS 傳送工作


```PowerShell
$Job = Start-BitsTransfer -Source https://Server1.TrustedDomain.com/File1.zip `
       -Destination d:\temp\downloads\ -Asynchronous

while (($Job.JobState -eq "Transferring") -or ($Job.JobState -eq "Connecting")) `
       { sleep 5;} # Poll for status, sleep for 5 seconds, or perform an action.

Switch($Job.JobState)
{
    "Transferred" {Complete-BitsTransfer -BitsJob $Job}
    "Error" {$Job | Format-List } # List the errors.
    default {"Other action"} #  Perform corrective action.
}

```



在上述範例中，BITS 傳送工作已指派給 $Job 變數。 這些檔案會依順序下載。 完成傳送作業之後，檔案會立即可用。 如果 $Job JobState 傳回「已傳輸」，則 $Job 物件會傳送至 [BitsTransfer]( /previous-versions//dd347701(v=technet.10)) Cmdlet。

如果 $Job JobState 傳回 "Error"，則 $Job 物件會傳送至 [格式清單]( /previous-versions//dd347700(v=technet.10)) Cmdlet 以列出錯誤。

## <a name="to-manage-powershell-remote-sessions"></a>管理 PowerShell 遠端會話

從 Windows 10 （1607版）開始，您可以執行 PowerShell Cmdlet、BITSAdmin 或其他應用程式，這些應用程式會使用連線到另一部電腦 (實體或虛擬) 的 PowerShell 遠端命令列中的 BITS [介面](bits-interfaces.md) 。 使用 PowerShell Direct 命令列將 [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) 命令列使用於相同實體電腦上的虛擬機器時，無法使用此功能。使用 WinRM Cmdlet 時，無法使用此功能。

從遠端 PowerShell 會話建立的 BITS 作業會在該會話的使用者帳戶內容下執行，而且只會在至少有一個作用中的本機登入會話或與該使用者帳戶相關聯的遠端 PowerShell 會話時才會進行。 您可以使用 PowerShell 的持續性 Pssession 來執行遠端命令，而不需要為每個作業保持開啟 PowerShell 視窗以繼續進行進度，如 [PowerShell 基本概念：遠端系統管理](https://techgenix.com/remote-management-powershell-part1/)中所述。

-   [新的-PSSession](/powershell/module/microsoft.powershell.core/new-pssession?view=powershell-7&preserve-view=true) 會建立持續性遠端 PowerShell 會話。 一旦建立之後，PSSession 物件會保存在遠端電腦中，直到明確刪除為止。 即使在用戶端與會話中斷連線之後，在使用中的會話中起始的任何 BITS 工作也會進行資料傳輸。
-   [中斷連線-PSSession](/powershell/module/microsoft.powershell.core/disconnect-pssession?view=powershell-7&preserve-view=true) 會中斷用戶端電腦與遠端 PowerShell 會話的連線，而會話的狀態會繼續由遠端電腦維護。 最重要的是，遠端會話的進程會繼續執行，而 BITS 作業會繼續進行。 用戶端電腦甚至可以在呼叫中斷連線-PSSession 之後重新開機及/或關閉。
-   [Connect-PSSession](/powershell/module/microsoft.powershell.core/connect-pssession?view=powershell-7&preserve-view=true) 將用戶端電腦重新連接到作用中的遠端 PowerShell 會話。
-   [移除-PSSession](/powershell/module/microsoft.powershell.core/remove-pssession?view=powershell-7&preserve-view=true) 眼淚遠端 PowerShell 會話。

下列範例示範如何使用 PowerShell Remote 來處理非同步 BITS 傳送工作，讓作業可以繼續進行，即使您未主動連線到遠端會話也一樣。


```PowerShell
# Establish a PowerShell Remote session in Server01 with name 'MyRemoteSession'
New-PSSession -ComputerName Server01 -Name MyRemoteSession -Credential Domain01\User01

# Enter the previously-established session to execute commands
Enter-PSSession -Name MyRemoteSession

# Enumerate active BITS transfers on the remote machine
Get-BitsTransfer

# While running in the context of the PowerShell Remote session, start a new BITS transfer
Start-BitsTransfer -Source https://Server1.TrustedDomain.com/File1.zip -Destination c:\temp\downloads\ -Asynchronous

# Exit the PowerShell Remote session's context
Exit-PSSession

# Disconnect the 'MyRemoteSession' PowerShell Remote session from the current PowerShell window
# After this command, it is safe to close the current PowerShell window and turn off the local machine
Disconnect-PSSession -Name MyRemoteSession


# The commands below can be executed from a different PowerShell window, even after rebooting the local machine
# Connect the 'MyRemoteSession' PowerShell Remote session to the current PowerShell window
Connect-PSSession -ComputerName Server01 -Name MyRemoteSession

# Enter the previously-established session to execute commands
Enter-PSSession -Name MyRemoteSession

# Enumerate active BITS transfers on the remote machine
Get-BitsTransfer

# Manage BITS transfers on the remote machine via Complete-BitsTransfer, Remove-BitsTransfer, etc.

# Exit the PowerShell Remote session's context
Exit-PSSession

# Destroy the 'MyRemoteSession' PowerShell Remote session when no longer needed
Remove-PSSession -Name MyRemoteSession
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[開始-BitsTransfer](/previous-versions//dd347701(v=technet.10))
</dt> <dt>

[完成-BitsTransfer]( /previous-versions//dd347701(v=technet.10))
</dt> </dl>

 

 
