---
title: 使用 WinRM Windows PowerShell Cmdlet 來管理 BITS 傳送工作
description: Windows 遠端管理 PowerShell Cmdlet 可以管理背景智慧型傳送服務 (BITS) 傳送作業。
ms.assetid: 9fbef8a1-ed3f-4277-9a07-ed427f60d7a8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eefd874a1056e959d1516d515891ae216e4aca3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510606"
---
# <a name="using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs"></a>使用 WinRM Windows PowerShell Cmdlet 來管理 BITS 傳送工作

Windows 遠端管理 PowerShell Cmdlet 可以管理背景智慧型傳送服務 (BITS) 傳送作業。 如需 BITS 遠端系統管理的詳細資訊，請參閱 [bits 提供者](/previous-versions/windows/desktop/bitsprov/bits-provider) 和 [bits 提供者類別]( /previous-versions//dd904507(v=vs.85))。

下列範例需要 [位提供者](/previous-versions/windows/desktop/bitsprov/bits-provider)。 安裝 BITS Compact 伺服器之後，就可以使用位提供者。 如需安裝 Compact server 的詳細資訊，請參閱 [BITS Compact server](bits-compact-server.md) 檔集。

1.  建立 BITS 傳送工作。

    ```PowerShell
    # Get the credentials to connect to the remote client computer
    $cred = Get-Credential
    $result = Invoke-WsmanAction -Action CreateJob –Resourceuri wmi/root/microsoft/bits/BitsClientJob `
    –Valueset @{DisplayName="TestJob"; RemoteUrl="https://Server01/servertestdir/testfile1.txt"; LocalFile="C:\clienttestdir\testfile1.txt";Type=0} `
    –ComputerName Client1  -Credential $cred
    ```

    

    [Credential 指令程式](/previous-versions//dd315327(v=technet.10))會要求使用者的認證連接到遠端電腦，並將認證指派給 $cred 物件。

    [Invoke-wsmanaction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1)指令程式會建立 [BitsClientJob](/previous-versions/windows/desktop/legacy/dd904502(v=vs.85))類別的實例，並使用 *Valueset* 參數中定義的雜湊表中的資訊，在 Client1 上建立 BITS 傳送工作。 *Valueset* 參數會指定填入 [>batchclient.joboperations.createjob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob)方法的參數所需的資訊。 在上述範例中，使用者會將 *類型* 參數設定為 0 (下載) 。 使用者也會指定下載作業的遠端和本機檔案的名稱。 如需有關建立 BITS 傳送工作的詳細資訊，以及有關參數的詳細資訊，請參閱 [>batchclient.joboperations.createjob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) 方法。

    [Invoke-wsmanaction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) Cmdlet 會將結果指派給 $result 變數。

    > [!Note]  
    > 使用「音符號」（ (\`) ）來表示分行符號。

     

2.  設定 BITS 傳送工作的優先順序。

    ```PowerShell
    Set-WsmanInstance  -ResourceURI  wmi/root/microsoft/bits/BitsClientJob -SelectorSet @{JobId=$result.JobId} `
    -ValueSet @{Priority=0} –ComputerName Client1  -Credential $cred
    ```

    

    [Set-wsmaninstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true)指令 Cmdlet 會將新的 BITS 傳送工作優先權變更為 0 (**BG \_ 作業 \_ 優先順序 \_ 前景**) 。 如需優先權層級的詳細資訊，請參閱 [**BG \_ 作業 \_ 優先權**](/windows/desktop/api/Bits/ne-bits-bg_job_priority) 列舉。

3.  繼續 BITS 傳送工作。

    ```PowerShell
    Invoke-WsmanAction -Action SetJobState -ResourceUri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
    -valueset @{JobState= 2} –ComputerName Client1  -Credential $cred
    ```

    

    [Invoke-wsmanaction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) Cmdlet 會呼叫[SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob)方法，將作業狀態設定為 2 (繼續作業) 。

4.  管理 BITS 傳送工作。

    ```PowerShell
    $IsPprocessing = $TRUE
    while ($IsPprocessing)
    {
        $result = Get-WsmanInstance  -ResourceURI  wmi/root/microsoft/bits/BitsClientJob -selectorset @{JobId = $result.JobId} `
               –ComputerName Client1  -Credential $cred
        if ($result.State -eq 6)
        {

    #Complete the job           
            Invoke-WsmanAction -action SetJobState -resourceuri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
                          -valueset @{JobState= 1} –ComputerName Client1  -Credential $cred
            "Job Successfully Transferred"
            $IsPprocessing = $FALSE;
        }
        elseif (($result.State -eq 4) -or ($result.State -eq 5))
        {

    #Cancel the job
            "Job is in Error " 
            Invoke-WsmanAction -action SetJobState -resourceuri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
                         -valueset @{JobState= 0} –ComputerName Client1  -Credential $cred
            # You can troubleshoot or delete the job
            $IsPprocessing = $FALSE;
        }
        else
        {
        "Job is processing\n" 
        }

    # Perform other action or poll in a tight loop. This example sleeps for 5 seconds
    sleep 5
    }
    ```

    

    上述範例是輪詢作業狀態的腳本，並根據狀態採取動作。 可能的動作如下：

    -   如果 $result，則為。狀態為 4 (**BG \_ 作業 \_ 狀態 \_ 錯誤**) ， [invoke-wsmanaction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) Cmdlet 會呼叫 [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) 方法，並取消作業。
    -   如果 $result，則為。狀態為 5 (**BG \_ 作業 \_ 狀態 \_ 暫時性 \_ 錯誤**) ， [invoke-wsmanaction 指令程式](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) 會呼叫 [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) 方法，並取消作業。
    -   如果 $result，則為。狀態為 6 (**BG \_ 作業 \_ 狀態已 \_ 傳輸**) ， [invoke-wsmanaction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) Cmdlet 會呼叫 [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) 方法，並將狀態設定為 [完成]。

    如需有關工作狀態的詳細資訊，請參閱 [**BG \_ 工作 \_ 狀態**](/windows/desktop/api/Bits/ne-bits-bg_job_state) 列舉。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Get-Credential](/previous-versions//dd315327(v=technet.10))
</dt> <dt>

[Invoke-Invoke-wsmanaction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true)
</dt> <dt>

[設定-Set-wsmaninstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true)
</dt> </dl>

 

 
