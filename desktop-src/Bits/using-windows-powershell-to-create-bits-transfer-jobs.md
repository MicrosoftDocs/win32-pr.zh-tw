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
# <a name="using-windows-powershell-to-create-bits-transfer-jobs"></a><span data-ttu-id="45afe-103">使用 Windows PowerShell 建立 BITS 傳送工作</span><span class="sxs-lookup"><span data-stu-id="45afe-103">Using Windows PowerShell to Create BITS Transfer Jobs</span></span>

<span data-ttu-id="45afe-104">您可以使用 PowerShell Cmdlet 來建立同步和非同步背景智慧型傳送服務 (BITS) 傳送作業。</span><span class="sxs-lookup"><span data-stu-id="45afe-104">You can use PowerShell cmdlets to create synchronous and asynchronous Background Intelligent Transfer Service (BITS) transfer jobs.</span></span>

<span data-ttu-id="45afe-105">本主題中的所有範例都使用 [BitsTransfer](/previous-versions//dd347701(v=technet.10)) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45afe-105">All of the examples in this topic use the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet.</span></span> <span data-ttu-id="45afe-106">若要使用 Cmdlet，請務必先匯入模組。</span><span class="sxs-lookup"><span data-stu-id="45afe-106">To use the cmdlet, be sure to import the module first.</span></span> <span data-ttu-id="45afe-107">若要安裝此模組，請執行下列命令： Import-Module BitsTransfer。</span><span class="sxs-lookup"><span data-stu-id="45afe-107">To install the module, run the following command: Import-Module BitsTransfer.</span></span> <span data-ttu-id="45afe-108">如需詳細資訊，請在 PowerShell 提示字元中輸入 **Get-help Start-BitsTransfer** 。</span><span class="sxs-lookup"><span data-stu-id="45afe-108">For more information, type **Get-Help Start-BitsTransfer** at the PowerShell prompt.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="45afe-109">當您在非互動式內容中執行的進程內（例如 Windows 服務）使用[ \* -BitsTransfer](/previous-versions//dd819413(v=technet.10)) Cmdlet 時，您可能無法將檔案加入至 BITS 作業，這可能會導致暫止狀態。</span><span class="sxs-lookup"><span data-stu-id="45afe-109">When you use [\*-BitsTransfer](/previous-versions//dd819413(v=technet.10)) cmdlets from within a process that runs in a noninteractive context, such as a Windows service, you may not be able to add files to BITS jobs, which can result in a suspended state.</span></span> <span data-ttu-id="45afe-110">若要繼續作業，用來建立傳送工作的身分識別必須登入。</span><span class="sxs-lookup"><span data-stu-id="45afe-110">For the job to proceed, the identity that was used to create a transfer job must be logged on.</span></span> <span data-ttu-id="45afe-111">例如，在以工作排程器工作的形式執行的 PowerShell 腳本中建立 BITS 工作時，除非已啟用工作排程器的工作設定 [只有在使用者登入時才執行]，否則 BITS 傳送將永遠不會完成。</span><span class="sxs-lookup"><span data-stu-id="45afe-111">For example, when creating a BITS job in a PowerShell script that was executed as a Task Scheduler job, the BITS transfer will never complete unless the Task Scheduler's task setting "Run only when user is logged on" is enabled.</span></span>

 

-   [<span data-ttu-id="45afe-112">建立同步 BITS 傳送工作</span><span class="sxs-lookup"><span data-stu-id="45afe-112">To create a synchronous BITS transfer job</span></span>](#to-create-a-synchronous-bits-transfer-job)
-   [<span data-ttu-id="45afe-113">若要建立具有多個檔案的同步 BITS 傳送工作</span><span class="sxs-lookup"><span data-stu-id="45afe-113">To create a synchronous BITS transfer job with multiple files</span></span>](#to-create-a-synchronous-bits-transfer-job-with-multiple-files)
-   [<span data-ttu-id="45afe-114">若要建立同步 BITS 傳送工作並指定遠端伺服器的認證</span><span class="sxs-lookup"><span data-stu-id="45afe-114">To create a synchronous BITS transfer job and specify credentials for a remote server</span></span>](#to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server)
-   [<span data-ttu-id="45afe-115">從 CSV 檔案建立同步 BITS 傳送工作</span><span class="sxs-lookup"><span data-stu-id="45afe-115">To create a synchronous BITS transfer job from a CSV file</span></span>](#to-create-a-synchronous-bits-transfer-job-from-a-csv-file)
-   [<span data-ttu-id="45afe-116">若要建立異步 BITS 傳送工作</span><span class="sxs-lookup"><span data-stu-id="45afe-116">To create an asynchronous BITS transfer job</span></span>](#to-create-an-asynchronous-bits-transfer-job)
-   [<span data-ttu-id="45afe-117">管理 PowerShell 遠端會話</span><span class="sxs-lookup"><span data-stu-id="45afe-117">To manage PowerShell Remote sessions</span></span>](#to-manage-powershell-remote-sessions)
-   [<span data-ttu-id="45afe-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="45afe-118">Related topics</span></span>](#related-topics)

## <a name="to-create-a-synchronous-bits-transfer-job"></a><span data-ttu-id="45afe-119">建立同步 BITS 傳送工作</span><span class="sxs-lookup"><span data-stu-id="45afe-119">To create a synchronous BITS transfer job</span></span>


```PowerShell
Start-BitsTransfer -Source https://Server01/serverdir/testfile1.txt `
-Destination C:\clientdir\testfile1.txt
```



> [!Note]  
> <span data-ttu-id="45afe-120">使用「音符號」（ (\`) ）來表示分行符號。</span><span class="sxs-lookup"><span data-stu-id="45afe-120">The grave-accent character (\`) is used to indicate a line break.</span></span>

 

<span data-ttu-id="45afe-121">在上述範例中，檔案的本機和遠端名稱會分別在 *來源* 和 *目的地* 參數中指定。</span><span class="sxs-lookup"><span data-stu-id="45afe-121">In the preceding example, the local and remote names of the file are specified in the *Source* and *Destination* parameters, respectively.</span></span> <span data-ttu-id="45afe-122">當檔案傳送完成或進入錯誤狀態時，命令提示字元就會出現。</span><span class="sxs-lookup"><span data-stu-id="45afe-122">The command prompt returns when the file transfer is complete or when it enters an error state.</span></span>

<span data-ttu-id="45afe-123">預設的傳輸類型為 [下載]。</span><span class="sxs-lookup"><span data-stu-id="45afe-123">The default transfer type is Download.</span></span> <span data-ttu-id="45afe-124">當您將檔案上傳到 HTTP 位置時， *TransferType* 參數必須設定為 [上傳]。</span><span class="sxs-lookup"><span data-stu-id="45afe-124">When you upload files to an HTTP location, the *TransferType* parameter must be set to Upload.</span></span>

<span data-ttu-id="45afe-125">因為 [BitsTransfer](/previous-versions//dd347701(v=technet.10)) Cmdlet 會強制執行參數位置，所以不需要為來源和目的地參數指定參數名稱。</span><span class="sxs-lookup"><span data-stu-id="45afe-125">Because parameter position is enforced for the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet, the parameter names do not need to be specified for the Source and Destination parameters.</span></span> <span data-ttu-id="45afe-126">因此，可以簡化此命令，如下所示。</span><span class="sxs-lookup"><span data-stu-id="45afe-126">Therefore, this command can be simplified as follows.</span></span>


```PowerShell
Start-BitsTransfer https://Server01/serverdir/testfile1.txt C:\clientdir\testfile1.txt
```



## <a name="to-create-a-synchronous-bits-transfer-job-with-multiple-files"></a><span data-ttu-id="45afe-127">若要建立具有多個檔案的同步 BITS 傳送工作</span><span class="sxs-lookup"><span data-stu-id="45afe-127">To create a synchronous BITS transfer job with multiple files</span></span>


```PowerShell
Start-BitsTransfer -Source C:\clientsourcedir\*.txt `
-Destination c:\clientdir\ -TransferType Download
```



<span data-ttu-id="45afe-128">在上述範例中， [BitsTransfer](/previous-versions//dd347701(v=technet.10)) 命令會建立新的 BITS 傳送工作。</span><span class="sxs-lookup"><span data-stu-id="45afe-128">In the preceding example, the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) command creates a new BITS transfer job.</span></span> <span data-ttu-id="45afe-129">所有檔案都會新增至此作業，並依序傳送給用戶端。</span><span class="sxs-lookup"><span data-stu-id="45afe-129">All of the files are added to this job and transferred sequentially to the client.</span></span>

> [!Note]  
> <span data-ttu-id="45afe-130">目的地路徑不可以使用萬用字元。</span><span class="sxs-lookup"><span data-stu-id="45afe-130">The destination path cannot use wildcard characters.</span></span> <span data-ttu-id="45afe-131">目的地路徑支援相對目錄、根路徑或隱含目錄， (也就是目前目錄) 。</span><span class="sxs-lookup"><span data-stu-id="45afe-131">The destination path supports relative directories, root paths, or implicit directories (that is, the current directory).</span></span> <span data-ttu-id="45afe-132">無法使用萬用字元重新命名目的地檔案。</span><span class="sxs-lookup"><span data-stu-id="45afe-132">Destination files cannot be renamed by using a wildcard character.</span></span> <span data-ttu-id="45afe-133">此外，HTTP 和 HTTPS Url 無法使用萬用字元。</span><span class="sxs-lookup"><span data-stu-id="45afe-133">Additionally, HTTP and HTTPS URLs do not work with wildcards.</span></span> <span data-ttu-id="45afe-134">萬用字元只有在 UNC 路徑和本機目錄中才有效。</span><span class="sxs-lookup"><span data-stu-id="45afe-134">Wildcards are only valid for UNC paths and local directories.</span></span>

 

## <a name="to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server"></a><span data-ttu-id="45afe-135">若要建立同步 BITS 傳送工作並指定遠端伺服器的認證</span><span class="sxs-lookup"><span data-stu-id="45afe-135">To create a synchronous BITS transfer job and specify credentials for a remote server</span></span>


```PowerShell
Start-BitsTransfer -DisplayName MyJob -Credential Username\Domain `
-Source https://server01/servertestdir/testfile1.txt -Destination c:\clienttestdir\testfile1.txt `
-ProxyUsage Override -ProxyList @(https://proxy1, 123.24.21.23, proxy3)
```



<span data-ttu-id="45afe-136">在上述範例中，使用者會建立 BITS 傳送工作，以從需要驗證的伺服器下載檔案。</span><span class="sxs-lookup"><span data-stu-id="45afe-136">In the preceding example, a user creates a BITS transfer job to download a file from a server that requires authentication.</span></span> <span data-ttu-id="45afe-137">系統會提示使用者輸入認證，而 *credential* 參數會將認證物件傳遞給 [BitsTransfer](/previous-versions//dd347701(v=technet.10)) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45afe-137">The user is prompted for credentials, and the *Credential* parameter passes a credential object to the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet.</span></span> <span data-ttu-id="45afe-138">使用者會設定明確的 proxy，而且 BITS 傳送工作只會使用 *ProxyList* 參數所定義的 proxy。</span><span class="sxs-lookup"><span data-stu-id="45afe-138">The user sets an explicit proxy, and the BITS transfer job uses only the proxies that are defined by the *ProxyList* parameter.</span></span> <span data-ttu-id="45afe-139">*DisplayName* 參數會為 BITS 傳送工作提供唯一的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="45afe-139">The *DisplayName* parameter gives the BITS transfer job a unique display name.</span></span>

## <a name="to-create-a-synchronous-bits-transfer-job-from-a-csv-file"></a><span data-ttu-id="45afe-140">從 CSV 檔案建立同步 BITS 傳送工作</span><span class="sxs-lookup"><span data-stu-id="45afe-140">To create a synchronous BITS transfer job from a CSV file</span></span>


```PowerShell
Import-CSV filelist.txt | Start-BitsTransfer -TransferType Upload
```



> [!Note]  
> <span data-ttu-id="45afe-141">" \| " 是管道字元。</span><span class="sxs-lookup"><span data-stu-id="45afe-141">The "\|" is the pipe character.</span></span>

 

<span data-ttu-id="45afe-142">在上述範例中，使用者會建立從用戶端上傳多個檔案的 BITS 傳送工作。</span><span class="sxs-lookup"><span data-stu-id="45afe-142">In the preceding example, a user creates a BITS transfer job that uploads multiple files from a client.</span></span> <span data-ttu-id="45afe-143">匯 [入 CSV](/previous-versions//dd347665(v=technet.10)) Cmdlet 會匯入來源和目的地檔案位置，並將它們傳送至 [BitsTransfer](/previous-versions//dd347701(v=technet.10)) 命令。</span><span class="sxs-lookup"><span data-stu-id="45afe-143">The [Import-CSV](/previous-versions//dd347665(v=technet.10)) cmdlet imports the source and destination file locations and pipes them to the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) command.</span></span> <span data-ttu-id="45afe-144">[BitsTransfer](/previous-versions//dd347701(v=technet.10))命令會為每個檔案建立新的 BITS 傳送工作、將檔案新增至作業，然後將它們依序傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="45afe-144">The [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) command creates a new BITS transfer job for each file, adds the files to the job, and then transfers them sequentially to the server.</span></span>

<span data-ttu-id="45afe-145">Filelist.txt 檔案的內容應該採用下列格式：</span><span class="sxs-lookup"><span data-stu-id="45afe-145">The contents of the Filelist.txt file should be in the following format:</span></span>

``` syntax
Source, Destination
c:\clienttestdir\testfile1.txt, https://server01/servertestdir/testfile1.txt
c:\clienttestdir\testfile2.txt, https://server01/servertestdir/testfile2.txt
c:\clienttestdir\testfile3.txt, https://server01/servertestdir/testfile3.txt
c:\clienttestdir\testfile4.txt, https://server01/servertestdir/testfile4.txt
```

## <a name="to-create-an-asynchronous-bits-transfer-job"></a><span data-ttu-id="45afe-146">若要建立異步 BITS 傳送工作</span><span class="sxs-lookup"><span data-stu-id="45afe-146">To create an asynchronous BITS transfer job</span></span>


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



<span data-ttu-id="45afe-147">在上述範例中，BITS 傳送工作已指派給 $Job 變數。</span><span class="sxs-lookup"><span data-stu-id="45afe-147">In the preceding example, the BITS transfer job was assigned to the $Job variable.</span></span> <span data-ttu-id="45afe-148">這些檔案會依順序下載。</span><span class="sxs-lookup"><span data-stu-id="45afe-148">The files are downloaded sequentially.</span></span> <span data-ttu-id="45afe-149">完成傳送作業之後，檔案會立即可用。</span><span class="sxs-lookup"><span data-stu-id="45afe-149">After the transfer job is complete, the files are immediately available.</span></span> <span data-ttu-id="45afe-150">如果 $Job JobState 傳回「已傳輸」，則 $Job 物件會傳送至 [BitsTransfer]( /previous-versions//dd347701(v=technet.10)) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45afe-150">If $Job.JobState returns "Transferred", the $Job object is sent to the [Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) cmdlet.</span></span>

<span data-ttu-id="45afe-151">如果 $Job JobState 傳回 "Error"，則 $Job 物件會傳送至 [格式清單]( /previous-versions//dd347700(v=technet.10)) Cmdlet 以列出錯誤。</span><span class="sxs-lookup"><span data-stu-id="45afe-151">If $Job.JobState returns "Error", the $Job object is sent to the [Format-List]( /previous-versions//dd347700(v=technet.10)) cmdlet to list the errors.</span></span>

## <a name="to-manage-powershell-remote-sessions"></a><span data-ttu-id="45afe-152">管理 PowerShell 遠端會話</span><span class="sxs-lookup"><span data-stu-id="45afe-152">To manage PowerShell Remote sessions</span></span>

<span data-ttu-id="45afe-153">從 Windows 10 （1607版）開始，您可以執行 PowerShell Cmdlet、BITSAdmin 或其他應用程式，這些應用程式會使用連線到另一部電腦 (實體或虛擬) 的 PowerShell 遠端命令列中的 BITS [介面](bits-interfaces.md) 。</span><span class="sxs-lookup"><span data-stu-id="45afe-153">Starting with Windows 10, version 1607, you can run PowerShell Cmdlets, BITSAdmin, or other applications that use the BITS [interfaces](bits-interfaces.md) from a PowerShell Remote command line connected to another machine (physical or virtual).</span></span> <span data-ttu-id="45afe-154">使用 PowerShell Direct 命令列將 [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) 命令列使用於相同實體電腦上的虛擬機器時，無法使用此功能。使用 WinRM Cmdlet 時，無法使用此功能。</span><span class="sxs-lookup"><span data-stu-id="45afe-154">This capability is not available when using a [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) command line to a virtual machine on the same physical machine, and it is not available when using WinRM cmdlets.</span></span>

<span data-ttu-id="45afe-155">從遠端 PowerShell 會話建立的 BITS 作業會在該會話的使用者帳戶內容下執行，而且只會在至少有一個作用中的本機登入會話或與該使用者帳戶相關聯的遠端 PowerShell 會話時才會進行。</span><span class="sxs-lookup"><span data-stu-id="45afe-155">A BITS Job created from a Remote PowerShell session runs under that session’s user account context and will only make progress when there is at least one active local logon session or Remote PowerShell session associated with that user account.</span></span> <span data-ttu-id="45afe-156">您可以使用 PowerShell 的持續性 Pssession 來執行遠端命令，而不需要為每個作業保持開啟 PowerShell 視窗以繼續進行進度，如 [PowerShell 基本概念：遠端系統管理](https://techgenix.com/remote-management-powershell-part1/)中所述。</span><span class="sxs-lookup"><span data-stu-id="45afe-156">You can use PowerShell's persistent PSSessions to run remote commands without the need to keep a PowerShell window open for each job to continue making progress, as described in [PowerShell Basics: Remote Management](https://techgenix.com/remote-management-powershell-part1/).</span></span>

-   <span data-ttu-id="45afe-157">[新的-PSSession](/powershell/module/microsoft.powershell.core/new-pssession?view=powershell-7&preserve-view=true) 會建立持續性遠端 PowerShell 會話。</span><span class="sxs-lookup"><span data-stu-id="45afe-157">[New-PSSession](/powershell/module/microsoft.powershell.core/new-pssession?view=powershell-7&preserve-view=true) creates a persistent Remote PowerShell session.</span></span> <span data-ttu-id="45afe-158">一旦建立之後，PSSession 物件會保存在遠端電腦中，直到明確刪除為止。</span><span class="sxs-lookup"><span data-stu-id="45afe-158">Once created, the PSSession objects persist in the remote machine until explicitly deleted.</span></span> <span data-ttu-id="45afe-159">即使在用戶端與會話中斷連線之後，在使用中的會話中起始的任何 BITS 工作也會進行資料傳輸。</span><span class="sxs-lookup"><span data-stu-id="45afe-159">Any BITS jobs initiated in an active session will make progress transferring data, even after the client has disconnected from the session.</span></span>
-   <span data-ttu-id="45afe-160">[中斷連線-PSSession](/powershell/module/microsoft.powershell.core/disconnect-pssession?view=powershell-7&preserve-view=true) 會中斷用戶端電腦與遠端 PowerShell 會話的連線，而會話的狀態會繼續由遠端電腦維護。</span><span class="sxs-lookup"><span data-stu-id="45afe-160">[Disconnect-PSSession](/powershell/module/microsoft.powershell.core/disconnect-pssession?view=powershell-7&preserve-view=true) disconnects the client machine from a Remote PowerShell session and the session’s state continues to be maintained by the remote machine.</span></span> <span data-ttu-id="45afe-161">最重要的是，遠端會話的進程會繼續執行，而 BITS 作業會繼續進行。</span><span class="sxs-lookup"><span data-stu-id="45afe-161">Most importantly, the remote session’s processes will continue executing, and BITS jobs will continue to make progress.</span></span> <span data-ttu-id="45afe-162">用戶端電腦甚至可以在呼叫中斷連線-PSSession 之後重新開機及/或關閉。</span><span class="sxs-lookup"><span data-stu-id="45afe-162">The client machine can even reboot and/or turn off after calling Disconnect-PSSession.</span></span>
-   <span data-ttu-id="45afe-163">[Connect-PSSession](/powershell/module/microsoft.powershell.core/connect-pssession?view=powershell-7&preserve-view=true) 將用戶端電腦重新連接到作用中的遠端 PowerShell 會話。</span><span class="sxs-lookup"><span data-stu-id="45afe-163">[Connect-PSSession](/powershell/module/microsoft.powershell.core/connect-pssession?view=powershell-7&preserve-view=true) re-connects the client machine to an active Remote PowerShell session.</span></span>
-   <span data-ttu-id="45afe-164">[移除-PSSession](/powershell/module/microsoft.powershell.core/remove-pssession?view=powershell-7&preserve-view=true) 眼淚遠端 PowerShell 會話。</span><span class="sxs-lookup"><span data-stu-id="45afe-164">[Remove-PSSession](/powershell/module/microsoft.powershell.core/remove-pssession?view=powershell-7&preserve-view=true) tears down a Remote PowerShell session.</span></span>

<span data-ttu-id="45afe-165">下列範例示範如何使用 PowerShell Remote 來處理非同步 BITS 傳送工作，讓作業可以繼續進行，即使您未主動連線到遠端會話也一樣。</span><span class="sxs-lookup"><span data-stu-id="45afe-165">The example below shows how to use PowerShell Remote to work with asynchronous BITS transfer jobs in a way that allows the job to continue to make progress even when you are not actively connected to the remote session.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="45afe-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="45afe-166">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="45afe-167">[開始-BitsTransfer](/previous-versions//dd347701(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="45afe-167">[Start-BitsTransfer](/previous-versions//dd347701(v=technet.10))</span></span>
</dt> <dt>

<span data-ttu-id="45afe-168">[完成-BitsTransfer]( /previous-versions//dd347701(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="45afe-168">[Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10))</span></span>
</dt> </dl>

 

 
