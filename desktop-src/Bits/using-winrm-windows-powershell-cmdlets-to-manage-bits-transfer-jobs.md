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
# <a name="using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs"></a><span data-ttu-id="322f9-103">使用 WinRM Windows PowerShell Cmdlet 來管理 BITS 傳送工作</span><span class="sxs-lookup"><span data-stu-id="322f9-103">Using WinRM Windows PowerShell Cmdlets to Manage BITS Transfer Jobs</span></span>

<span data-ttu-id="322f9-104">Windows 遠端管理 PowerShell Cmdlet 可以管理背景智慧型傳送服務 (BITS) 傳送作業。</span><span class="sxs-lookup"><span data-stu-id="322f9-104">Windows Remote Management PowerShell cmdlets can manage Background Intelligent Transfer Service (BITS) transfer jobs.</span></span> <span data-ttu-id="322f9-105">如需 BITS 遠端系統管理的詳細資訊，請參閱 [bits 提供者](/previous-versions/windows/desktop/bitsprov/bits-provider) 和 [bits 提供者類別]( /previous-versions//dd904507(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="322f9-105">For more information about BITS remote management, see [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider) and [BITS provider classes]( /previous-versions//dd904507(v=vs.85)).</span></span>

<span data-ttu-id="322f9-106">下列範例需要 [位提供者](/previous-versions/windows/desktop/bitsprov/bits-provider)。</span><span class="sxs-lookup"><span data-stu-id="322f9-106">The following examples require the [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider).</span></span> <span data-ttu-id="322f9-107">安裝 BITS Compact 伺服器之後，就可以使用位提供者。</span><span class="sxs-lookup"><span data-stu-id="322f9-107">The BITS provider is available after the BITS Compact server is installed.</span></span> <span data-ttu-id="322f9-108">如需安裝 Compact server 的詳細資訊，請參閱 [BITS Compact server](bits-compact-server.md) 檔集。</span><span class="sxs-lookup"><span data-stu-id="322f9-108">For information about installing the Compact server, see the [BITS Compact Server](bits-compact-server.md) documentation.</span></span>

1.  <span data-ttu-id="322f9-109">建立 BITS 傳送工作。</span><span class="sxs-lookup"><span data-stu-id="322f9-109">Create a BITS transfer job.</span></span>

    ```PowerShell
    # Get the credentials to connect to the remote client computer
    $cred = Get-Credential
    $result = Invoke-WsmanAction -Action CreateJob –Resourceuri wmi/root/microsoft/bits/BitsClientJob `
    –Valueset @{DisplayName="TestJob"; RemoteUrl="https://Server01/servertestdir/testfile1.txt"; LocalFile="C:\clienttestdir\testfile1.txt";Type=0} `
    –ComputerName Client1  -Credential $cred
    ```

    

    <span data-ttu-id="322f9-110">[Credential 指令程式](/previous-versions//dd315327(v=technet.10))會要求使用者的認證連接到遠端電腦，並將認證指派給 $cred 物件。</span><span class="sxs-lookup"><span data-stu-id="322f9-110">The [Get-Credential](/previous-versions//dd315327(v=technet.10)) cmdlet requests the user's credentials to connect to the remote computer and assigns the credentials to the $cred object.</span></span>

    <span data-ttu-id="322f9-111">[Invoke-wsmanaction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1)指令程式會建立 [BitsClientJob](/previous-versions/windows/desktop/legacy/dd904502(v=vs.85))類別的實例，並使用 *Valueset* 參數中定義的雜湊表中的資訊，在 Client1 上建立 BITS 傳送工作。</span><span class="sxs-lookup"><span data-stu-id="322f9-111">The [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1) cmdlet creates the BITS transfer job on Client1 by creating an instance of the [BitsClientJob](/previous-versions/windows/desktop/legacy/dd904502(v=vs.85)) class and using the information in the hash table defined in the *Valueset* parameter.</span></span> <span data-ttu-id="322f9-112">*Valueset* 參數會指定填入 [>batchclient.joboperations.createjob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob)方法的參數所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="322f9-112">The *Valueset* parameter specifies the information needed to populate the parameters of the [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) method.</span></span> <span data-ttu-id="322f9-113">在上述範例中，使用者會將 *類型* 參數設定為 0 (下載) 。</span><span class="sxs-lookup"><span data-stu-id="322f9-113">In the preceding example, the user is sets the *Type* parameter to 0 (download).</span></span> <span data-ttu-id="322f9-114">使用者也會指定下載作業的遠端和本機檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="322f9-114">The user also specifies the name of both the remote and local files for the download job.</span></span> <span data-ttu-id="322f9-115">如需有關建立 BITS 傳送工作的詳細資訊，以及有關參數的詳細資訊，請參閱 [>batchclient.joboperations.createjob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) 方法。</span><span class="sxs-lookup"><span data-stu-id="322f9-115">For more information about creating BITS transfer jobs and for detailed information about parameters, see [CreateJob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) method.</span></span>

    <span data-ttu-id="322f9-116">[Invoke-wsmanaction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) Cmdlet 會將結果指派給 $result 變數。</span><span class="sxs-lookup"><span data-stu-id="322f9-116">The [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet assigns the result to the $result variable.</span></span>

    > [!Note]  
    > <span data-ttu-id="322f9-117">使用「音符號」（ (\`) ）來表示分行符號。</span><span class="sxs-lookup"><span data-stu-id="322f9-117">The grave-accent character (\`) is used to indicate a line break.</span></span>

     

2.  <span data-ttu-id="322f9-118">設定 BITS 傳送工作的優先順序。</span><span class="sxs-lookup"><span data-stu-id="322f9-118">Set the Priority of the BITS transfer job.</span></span>

    ```PowerShell
    Set-WsmanInstance  -ResourceURI  wmi/root/microsoft/bits/BitsClientJob -SelectorSet @{JobId=$result.JobId} `
    -ValueSet @{Priority=0} –ComputerName Client1  -Credential $cred
    ```

    

    <span data-ttu-id="322f9-119">[Set-wsmaninstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true)指令 Cmdlet 會將新的 BITS 傳送工作優先權變更為 0 (**BG \_ 作業 \_ 優先順序 \_ 前景**) 。</span><span class="sxs-lookup"><span data-stu-id="322f9-119">The [Set-WsmanInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) cmdlet changes the new BITS transfer job priority to 0 (**BG\_JOB\_PRIORITY\_FOREGROUND**).</span></span> <span data-ttu-id="322f9-120">如需優先權層級的詳細資訊，請參閱 [**BG \_ 作業 \_ 優先權**](/windows/desktop/api/Bits/ne-bits-bg_job_priority) 列舉。</span><span class="sxs-lookup"><span data-stu-id="322f9-120">For more information about the priority levels, see the [**BG\_JOB\_PRIORITY**](/windows/desktop/api/Bits/ne-bits-bg_job_priority) enumeration.</span></span>

3.  <span data-ttu-id="322f9-121">繼續 BITS 傳送工作。</span><span class="sxs-lookup"><span data-stu-id="322f9-121">Resume the BITS transfer job.</span></span>

    ```PowerShell
    Invoke-WsmanAction -Action SetJobState -ResourceUri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
    -valueset @{JobState= 2} –ComputerName Client1  -Credential $cred
    ```

    

    <span data-ttu-id="322f9-122">[Invoke-wsmanaction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) Cmdlet 會呼叫[SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob)方法，將作業狀態設定為 2 (繼續作業) 。</span><span class="sxs-lookup"><span data-stu-id="322f9-122">The [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method, which sets the job state to 2 (Resume the Job).</span></span>

4.  <span data-ttu-id="322f9-123">管理 BITS 傳送工作。</span><span class="sxs-lookup"><span data-stu-id="322f9-123">Manage the BITS transfer job.</span></span>

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

    

    <span data-ttu-id="322f9-124">上述範例是輪詢作業狀態的腳本，並根據狀態採取動作。</span><span class="sxs-lookup"><span data-stu-id="322f9-124">The preceding example is a script to poll the status of the job and take an action based on the status.</span></span> <span data-ttu-id="322f9-125">可能的動作如下：</span><span class="sxs-lookup"><span data-stu-id="322f9-125">The following actions are possible:</span></span>

    -   <span data-ttu-id="322f9-126">如果 $result，則為。狀態為 4 (**BG \_ 作業 \_ 狀態 \_ 錯誤**) ， [invoke-wsmanaction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) Cmdlet 會呼叫 [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) 方法，並取消作業。</span><span class="sxs-lookup"><span data-stu-id="322f9-126">If $result.State is 4 (**BG\_JOB\_STATE\_ERROR**), the [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method and cancels the job.</span></span>
    -   <span data-ttu-id="322f9-127">如果 $result，則為。狀態為 5 (**BG \_ 作業 \_ 狀態 \_ 暫時性 \_ 錯誤**) ， [invoke-wsmanaction 指令程式](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) 會呼叫 [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) 方法，並取消作業。</span><span class="sxs-lookup"><span data-stu-id="322f9-127">If $result.State is 5 (**BG\_JOB\_STATE\_TRANSIENT\_ERROR**), the [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method and cancels the job.</span></span>
    -   <span data-ttu-id="322f9-128">如果 $result，則為。狀態為 6 (**BG \_ 作業 \_ 狀態已 \_ 傳輸**) ， [invoke-wsmanaction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) Cmdlet 會呼叫 [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) 方法，並將狀態設定為 [完成]。</span><span class="sxs-lookup"><span data-stu-id="322f9-128">If $result.State is 6 (**BG\_JOB\_STATE\_TRANSFERRED**), the [Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) cmdlet calls the [SetJobState](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) method and sets the state to complete.</span></span>

    <span data-ttu-id="322f9-129">如需有關工作狀態的詳細資訊，請參閱 [**BG \_ 工作 \_ 狀態**](/windows/desktop/api/Bits/ne-bits-bg_job_state) 列舉。</span><span class="sxs-lookup"><span data-stu-id="322f9-129">For more information about job states, see the [**BG\_JOB\_STATE**](/windows/desktop/api/Bits/ne-bits-bg_job_state) enumeration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="322f9-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="322f9-130">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="322f9-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="322f9-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span></span>
</dt> <dt>

[<span data-ttu-id="322f9-132">Invoke-Invoke-wsmanaction</span><span class="sxs-lookup"><span data-stu-id="322f9-132">Invoke-WsmanAction</span></span>](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true)
</dt> <dt>

[<span data-ttu-id="322f9-133">設定-Set-wsmaninstance</span><span class="sxs-lookup"><span data-stu-id="322f9-133">Set-WsmanInstance</span></span>](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true)
</dt> </dl>

 

 
