---
title: 使用 BITS
description: 使用 BITS
ms.assetid: 65b69ccb-b413-4690-ac0d-774d88608bdf
keywords:
- 背景智慧型傳送服務
- 背景智慧型傳送服務，工作
- 檔案傳輸位
- 使用位位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5158e183ef7e7c142a481f1d89e329a9b04f422b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965254"
---
# <a name="using-bits"></a><span data-ttu-id="26d6e-107">使用 BITS</span><span class="sxs-lookup"><span data-stu-id="26d6e-107">Using BITS</span></span>

<span data-ttu-id="26d6e-108">下列步驟示範如何使用背景智慧型傳送服務 (位)  [介面](bits-interfaces.md)來執行檔案傳輸。</span><span class="sxs-lookup"><span data-stu-id="26d6e-108">The following steps show how to perform a file transfer using the Background Intelligent Transfer Service (BITS)  [interfaces](bits-interfaces.md).</span></span>

<span data-ttu-id="26d6e-109">**執行檔案傳輸**</span><span class="sxs-lookup"><span data-stu-id="26d6e-109">**To perform a file transfer**</span></span>

1.  [<span data-ttu-id="26d6e-110">連接到 BITS 服務</span><span class="sxs-lookup"><span data-stu-id="26d6e-110">Connect to the BITS service</span></span>](connecting-to-the-bits-service.md)
2.  [<span data-ttu-id="26d6e-111">建立傳送作業</span><span class="sxs-lookup"><span data-stu-id="26d6e-111">Create a transfer job</span></span>](creating-a-job.md)
3.  [<span data-ttu-id="26d6e-112">將檔案新增至作業</span><span class="sxs-lookup"><span data-stu-id="26d6e-112">Add files to the job</span></span>](adding-files-to-a-job.md)
4.  [<span data-ttu-id="26d6e-113">啟動工作</span><span class="sxs-lookup"><span data-stu-id="26d6e-113">Start the job</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)
5.  [<span data-ttu-id="26d6e-114">判斷 BITS 是否已成功傳輸檔案</span><span class="sxs-lookup"><span data-stu-id="26d6e-114">Determine if BITS successfully transferred the files</span></span>](determining-the-status-of-a-job.md)
6.  [<span data-ttu-id="26d6e-115">完成工作</span><span class="sxs-lookup"><span data-stu-id="26d6e-115">Complete the job</span></span>](completing-and-canceling-a-job.md)

<span data-ttu-id="26d6e-116">先前的步驟示範如何使用作業的預設屬性值來傳送檔案。</span><span class="sxs-lookup"><span data-stu-id="26d6e-116">The previous steps show how to transfer files using the default property values for a job.</span></span> <span data-ttu-id="26d6e-117">您可以藉由變更一或多個作業的屬性值來變更預設行為。</span><span class="sxs-lookup"><span data-stu-id="26d6e-117">You can change the default behavior by changing one or more of the job's property values.</span></span> <span data-ttu-id="26d6e-118">例如，您可以變更作業相對於佇列中其他作業的處理優先權、指定您自己的 proxy 設定，以及註冊在 BITS 傳輸檔案時接收事件通知。</span><span class="sxs-lookup"><span data-stu-id="26d6e-118">For example, you can change the priority that the job is processed relative to other jobs in the queue, specify your own proxy setting, and register to receive event notification when BITS has transferred the files.</span></span> <span data-ttu-id="26d6e-119">如需詳細資訊，請參閱 [設定和取出作業的屬性](setting-and-retrieving-the-properties-of-a-job.md)。</span><span class="sxs-lookup"><span data-stu-id="26d6e-119">For more information, see [Setting and Retrieving the Properties of a Job](setting-and-retrieving-the-properties-of-a-job.md).</span></span>

<span data-ttu-id="26d6e-120">Windows PowerShell 提供簡單的機制來管理許多 BITS 工作。</span><span class="sxs-lookup"><span data-stu-id="26d6e-120">Windows PowerShell provides a simple mechanism to manage many BITS tasks.</span></span> <span data-ttu-id="26d6e-121">本節包含下列主題，說明如何搭配使用 Windows PowerShell Cmdlet 與位：</span><span class="sxs-lookup"><span data-stu-id="26d6e-121">This section contains the following topics that show how to use Windows PowerShell cmdlets with BITS:</span></span>

-   [<span data-ttu-id="26d6e-122">使用 Windows PowerShell 建立 BITS 傳送工作</span><span class="sxs-lookup"><span data-stu-id="26d6e-122">Using Windows PowerShell to Create BITS Transfer Jobs</span></span>](using-windows-powershell-to-create-bits-transfer-jobs.md)
-   [<span data-ttu-id="26d6e-123">使用 WinRM Windows PowerShell Cmdlet 來管理 BITS 傳送工作</span><span class="sxs-lookup"><span data-stu-id="26d6e-123">Using WinRM Windows PowerShell Cmdlets to Manage BITS Transfer Jobs</span></span>](using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs.md)
-   [<span data-ttu-id="26d6e-124">使用 WMI Windows PowerShell Cmdlet 來管理 BITS Compact Server</span><span class="sxs-lookup"><span data-stu-id="26d6e-124">Using WMI Windows PowerShell Cmdlets to Manage the BITS Compact Server</span></span>](using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server.md)

> [!Note]
>
> <span data-ttu-id="26d6e-125">從1607版 Windows 10 開始，您也可以執行 PowerShell Cmdlet，並使用 BITSAdmin 或其他應用程式，從連線到另一部電腦的 PowerShell 遠端命令列（ (實體或虛擬) ）使用 BITS [介面](bits-interfaces.md) 。</span><span class="sxs-lookup"><span data-stu-id="26d6e-125">Starting with Windows 10, version 1607, you can also run PowerShell Cmdlets and use BITSAdmin or other applications that use the BITS [interfaces](bits-interfaces.md) from a PowerShell Remote command line connected to another machine (physical or virtual).</span></span> <span data-ttu-id="26d6e-126">使用 PowerShell Direct 命令列將 [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) 命令列使用於相同實體電腦上的虛擬機器時，無法使用此功能。使用 WinRM Cmdlet 時，無法使用此功能。</span><span class="sxs-lookup"><span data-stu-id="26d6e-126">This capability is not available when using a [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) command line to a virtual machine on the same physical machine, and it is not available when using WinRM cmdlets.</span></span>
>
> <span data-ttu-id="26d6e-127">從遠端 PowerShell 會話建立的 BITS 作業將會在該會話的使用者帳戶內容下執行，而且只有在至少有一個作用中的本機登入會話或與該使用者帳戶相關聯的遠端 PowerShell 會話時，才會進行進度。</span><span class="sxs-lookup"><span data-stu-id="26d6e-127">A BITS Job created from a Remote PowerShell session will run under that session’s user account context and will only make progress when there is at least one active local logon session or Remote PowerShell session associated with that user account.</span></span> <span data-ttu-id="26d6e-128">如需詳細資訊，請參閱 [管理 PowerShell 遠端會話](using-windows-powershell-to-create-bits-transfer-jobs.md)。</span><span class="sxs-lookup"><span data-stu-id="26d6e-128">For more information, see [To manage PowerShell Remote sessions](using-windows-powershell-to-create-bits-transfer-jobs.md).</span></span>

 

<span data-ttu-id="26d6e-129">本節也包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="26d6e-129">This section also contains the following topics:</span></span>

-   [<span data-ttu-id="26d6e-130">使用 BITS 的最佳作法</span><span class="sxs-lookup"><span data-stu-id="26d6e-130">Best Practices When Using BITS</span></span>](best-practices-when-using-bits.md)
-   [<span data-ttu-id="26d6e-131">列舉傳送佇列中的作業</span><span class="sxs-lookup"><span data-stu-id="26d6e-131">Enumerating jobs in the transfer queue</span></span>](enumerating-jobs-in-the-transfer-queue.md)
-   [<span data-ttu-id="26d6e-132">列舉作業中的檔案</span><span class="sxs-lookup"><span data-stu-id="26d6e-132">Enumerating files in a job</span></span>](enumerating-files-in-a-job.md)
-   [<span data-ttu-id="26d6e-133">處理錯誤</span><span class="sxs-lookup"><span data-stu-id="26d6e-133">Handling errors</span></span>](handling-errors.md)
-   [<span data-ttu-id="26d6e-134">從上傳-回復作業取出回復</span><span class="sxs-lookup"><span data-stu-id="26d6e-134">Retrieve the reply from an upload-reply job</span></span>](retrieving-the-reply-from-an-upload-reply-job.md)

<span data-ttu-id="26d6e-135">如需使用 BITS 介面的範例程式碼，請參閱 [Bits 範例和工具](bits-samples-and-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="26d6e-135">For sample code that uses the BITS interfaces, see [BITS Samples and Tools](bits-samples-and-tools.md).</span></span>

 

 