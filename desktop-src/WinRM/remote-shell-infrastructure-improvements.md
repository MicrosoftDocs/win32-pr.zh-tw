---
title: 遠端 Shell 基礎結構改進
description: Windows 遠端管理2.0 版 (WinRM 2.0) 提供許多遠端 shell 基礎結構的增強功能。
ms.assetid: b22693ba-fa43-44bb-9b2d-0c64fad6e3cc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c67752222f1ca969ea254164a25144168d1eb3
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/24/2020
ms.locfileid: "104022959"
---
# <a name="remote-shell-infrastructure-improvements"></a><span data-ttu-id="9d7b6-103">遠端 Shell 基礎結構改進</span><span class="sxs-lookup"><span data-stu-id="9d7b6-103">Remote Shell Infrastructure Improvements</span></span>

<span data-ttu-id="9d7b6-104">Windows 遠端管理2.0 版 (WinRM 2.0) 提供許多遠端 shell 基礎結構的增強功能。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-104">Windows Remote Management version 2.0 (WinRM 2.0) offers many remote shell infrastructure improvements.</span></span> <span data-ttu-id="9d7b6-105">下列主題將詳細說明這些改進：</span><span class="sxs-lookup"><span data-stu-id="9d7b6-105">The following topics describe these improvements in detail:</span></span>

-   [<span data-ttu-id="9d7b6-106">多重躍點支援</span><span class="sxs-lookup"><span data-stu-id="9d7b6-106">Multi-Hop Support</span></span>](multi-hop-support.md)
-   [<span data-ttu-id="9d7b6-107">遠端 Shell 的配額管理</span><span class="sxs-lookup"><span data-stu-id="9d7b6-107">Quota Management for Remote Shells</span></span>](quotas.md)

<span data-ttu-id="9d7b6-108">WinRM 遠端 shell 基礎結構的其中一項改進，是加入更健全的 shell 管理員來維護使用者特定的 shell 資訊。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-108">One of the improvements to the WinRM remote shell infrastructure is the addition of a more robust shell manager that maintains user-specific shell information.</span></span> <span data-ttu-id="9d7b6-109">WinRM 使用者可以在遠端電腦上建立 shell 來執行命令或腳本。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-109">WinRM users can create shells on remote computers to run commands or scripts.</span></span> <span data-ttu-id="9d7b6-110">此外，使用者可以在電腦上建立多個 shell。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-110">In addition, users can create multiple shells on a computer.</span></span> <span data-ttu-id="9d7b6-111">使用者和系統管理員都需要管理 shell 的能力。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-111">Users and administrators both need the ability to manage shells.</span></span> <span data-ttu-id="9d7b6-112">使用者可以列舉、取得和刪除其所建立的 shell。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-112">Users can enumerate, get, and delete the shells that they have created.</span></span> <span data-ttu-id="9d7b6-113">系統管理員可以列舉所有使用中的 shell，並取得本機或遠端主機上特定 shell 的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-113">Administrators can enumerate over all active shells and retrieve details about specific shells on a local or remote host.</span></span> <span data-ttu-id="9d7b6-114">系統管理員也可以刪除本機或遠端主機上的任何作用中 shell。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-114">Administrators can also delete any active shells on a local or remote host.</span></span>

<span data-ttu-id="9d7b6-115">當使用者或系統管理員列舉使用中的 shell 時，WinRM 服務可以傳回下列資訊。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-115">When a user or administrator enumerates the active shells, the following information can be returned by the WinRM service.</span></span>

<dl> <dt>

<span data-ttu-id="9d7b6-116"><span id="ShellId"></span><span id="shellid"></span><span id="SHELLID"></span>ShellId</span><span class="sxs-lookup"><span data-stu-id="9d7b6-116"><span id="ShellId"></span><span id="shellid"></span><span id="SHELLID"></span>ShellId</span></span>
</dt> <dd>

<span data-ttu-id="9d7b6-117">指定 shell 的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-117">Specifies the unique identifier for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="9d7b6-118"><span id="Environment_variables"></span><span id="environment_variables"></span><span id="ENVIRONMENT_VARIABLES"></span>環境變數</span><span class="sxs-lookup"><span data-stu-id="9d7b6-118"><span id="Environment_variables"></span><span id="environment_variables"></span><span id="ENVIRONMENT_VARIABLES"></span>Environment variables</span></span>
</dt> <dd>

<span data-ttu-id="9d7b6-119">指定使用者所設定的任何環境變數。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-119">Specifies any environment variables set by the user.</span></span>

</dd> <dt>

<span data-ttu-id="9d7b6-120"><span id="WorkingDirectory"></span><span id="workingdirectory"></span><span id="WORKINGDIRECTORY"></span>WorkingDirectory</span><span class="sxs-lookup"><span data-stu-id="9d7b6-120"><span id="WorkingDirectory"></span><span id="workingdirectory"></span><span id="WORKINGDIRECTORY"></span>WorkingDirectory</span></span>
</dt> <dd>

<span data-ttu-id="9d7b6-121">指定 shell 的起始目錄。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-121">Specifies the starting directory for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="9d7b6-122"><span id="ResourceURI"></span><span id="resourceuri"></span><span id="RESOURCEURI"></span>ResourceURI</span><span class="sxs-lookup"><span data-stu-id="9d7b6-122"><span id="ResourceURI"></span><span id="resourceuri"></span><span id="RESOURCEURI"></span>ResourceURI</span></span>
</dt> <dd>

<span data-ttu-id="9d7b6-123">指定 shell 作業的資源 URI。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-123">Specifies the resource URI for the shell operation.</span></span> <span data-ttu-id="9d7b6-124">資源 URI 可以用來抓取 shell 實例特定的外掛程式設定。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-124">The resource URI can be used to retrieve plug-in configuration that is specific to the shell instance.</span></span>

</dd> <dt>

<span data-ttu-id="9d7b6-125"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="9d7b6-125"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span></span>
</dt> <dd>

<span data-ttu-id="9d7b6-126">指定在沒有任何要求的情況下，shell 將保持開啟狀態的最大持續時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-126">Specifies the maximum duration, in milliseconds, that the shell will stay open without any request.</span></span>

</dd> <dt>

<span data-ttu-id="9d7b6-127"><span id="InputStreams"></span><span id="inputstreams"></span><span id="INPUTSTREAMS"></span>InputStreams</span><span class="sxs-lookup"><span data-stu-id="9d7b6-127"><span id="InputStreams"></span><span id="inputstreams"></span><span id="INPUTSTREAMS"></span>InputStreams</span></span>
</dt> <dd>

<span data-ttu-id="9d7b6-128">指定 shell 的輸入資料流程。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-128">Specifies the input streams for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="9d7b6-129"><span id="OutputStreams"></span><span id="outputstreams"></span><span id="OUTPUTSTREAMS"></span>OutputStreams</span><span class="sxs-lookup"><span data-stu-id="9d7b6-129"><span id="OutputStreams"></span><span id="outputstreams"></span><span id="OUTPUTSTREAMS"></span>OutputStreams</span></span>
</dt> <dd>

<span data-ttu-id="9d7b6-130">指定 shell 的輸出資料流程。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-130">Specifies the output streams for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="9d7b6-131"><span id="Shell_creation_time"></span><span id="shell_creation_time"></span><span id="SHELL_CREATION_TIME"></span>Shell 建立時間</span><span class="sxs-lookup"><span data-stu-id="9d7b6-131"><span id="Shell_creation_time"></span><span id="shell_creation_time"></span><span id="SHELL_CREATION_TIME"></span>Shell creation time</span></span>
</dt> <dd>

<span data-ttu-id="9d7b6-132">指定 shell 的建立時間戳記。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-132">Specifies the creation timestamp for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="9d7b6-133"><span id="IdleTime"></span><span id="idletime"></span><span id="IDLETIME"></span>IdleTime</span><span class="sxs-lookup"><span data-stu-id="9d7b6-133"><span id="IdleTime"></span><span id="idletime"></span><span id="IDLETIME"></span>IdleTime</span></span>
</dt> <dd>

<span data-ttu-id="9d7b6-134">指定 shell 已閒置的持續時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-134">Specifies the duration, in milliseconds, that the shell has been idle.</span></span>

</dd> <dt>

<span data-ttu-id="9d7b6-135"><span id="UserId"></span><span id="userid"></span><span id="USERID"></span>UserId</span><span class="sxs-lookup"><span data-stu-id="9d7b6-135"><span id="UserId"></span><span id="userid"></span><span id="USERID"></span>UserId</span></span>
</dt> <dd>

<span data-ttu-id="9d7b6-136">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-136">Specifies the user ID.</span></span>

</dd> <dt>

<span data-ttu-id="9d7b6-137"><span id="Hostname_or_IP_address"></span><span id="hostname_or_ip_address"></span><span id="HOSTNAME_OR_IP_ADDRESS"></span>主機名稱或 IP 位址</span><span class="sxs-lookup"><span data-stu-id="9d7b6-137"><span id="Hostname_or_IP_address"></span><span id="hostname_or_ip_address"></span><span id="HOSTNAME_OR_IP_ADDRESS"></span>Hostname or IP address</span></span>
</dt> <dd>

<span data-ttu-id="9d7b6-138">指定建立 shell 之電腦的主機名稱或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-138">Specifies either the host name or IP address of the computer that created the shell.</span></span>

</dd> <dt>

<span data-ttu-id="9d7b6-139"><span id="Shell_memory_usage"></span><span id="shell_memory_usage"></span><span id="SHELL_MEMORY_USAGE"></span>Shell 記憶體使用量</span><span class="sxs-lookup"><span data-stu-id="9d7b6-139"><span id="Shell_memory_usage"></span><span id="shell_memory_usage"></span><span id="SHELL_MEMORY_USAGE"></span>Shell memory usage</span></span>
</dt> <dd>

<span data-ttu-id="9d7b6-140">指定 shell 已使用的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-140">Specifies the amount of memory that has been used by the shell.</span></span>

</dd> <dt>

<span data-ttu-id="9d7b6-141"><span id="Number_of_processes"></span><span id="number_of_processes"></span><span id="NUMBER_OF_PROCESSES"></span>進程數目</span><span class="sxs-lookup"><span data-stu-id="9d7b6-141"><span id="Number_of_processes"></span><span id="number_of_processes"></span><span id="NUMBER_OF_PROCESSES"></span>Number of processes</span></span>
</dt> <dd>

<span data-ttu-id="9d7b6-142">指定 shell 所建立的進程數目。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-142">Specifies the number of processes that have been created by the shell.</span></span>

</dd> </dl>

## <a name="enumerating-a-shell-on-a-local-host"></a><span data-ttu-id="9d7b6-143">列舉本機主機上的 Shell</span><span class="sxs-lookup"><span data-stu-id="9d7b6-143">Enumerating a Shell on a Local Host</span></span>

<span data-ttu-id="9d7b6-144">下列命令示範如何使用 winrm 公用程式來列舉 WinRM 用戶端上的 shell： **winrm 列舉 shell**。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-144">The following command demonstrates how to use the winrm utility to enumerate shells on a WinRM client: **winrm enumerate shell**.</span></span>

<span data-ttu-id="9d7b6-145">下列以文字為基礎的範例會顯示 shell 列舉的輸出：</span><span class="sxs-lookup"><span data-stu-id="9d7b6-145">The following text-based example displays the output for shell enumeration:</span></span>

``` syntax
Shell
    ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E
    ResourceUri = http://schemas.microsoft.com/wbem/wsman/1/windows/shell/cmd
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin
    OutputStreams = stdout stderr
    ShellRunTime = P0DT0H0M36S
    ShellInactivity = P0DT0H0M35S

Shell
    ShellId = EE3F11CE-FB3C-4C4E-B113-6F4D643C97D8
    ResourceUri = http://schemas.microsoft.com/powershell/Microsoft.PowerShell
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin pr
    OutputStreams = stdout
    ShellRunTime = P0DT0H1M46S
    ShellInactivity = P0DT0H0M45S
    MemoryUsed = 48MB
    ChildProcesses = 0

Shell
    ShellId = 8FD7F2C4-A434-4D58-A7E8-46F8BF202D0B
    ResourceUri = http://schemas.microsoft.com/powershell/Microsoft.PowerShell
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin pr
    OutputStreams = stdout
    ShellRunTime = P0DT0H1M47S
    ShellInactivity = P0DT0H0M47S
    MemoryUsed = 48MB
    ChildProcesses = 0
```

<span data-ttu-id="9d7b6-146">如需詳細資訊，請參閱下列命令所提供的線上說明： **winrm 列舉-？**。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-146">For more information, see the online help provided by running the following command: **winrm enumerate -?**.</span></span>

## <a name="retrieving-information-about-a-specific-shell"></a><span data-ttu-id="9d7b6-147">正在抓取特定 Shell 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="9d7b6-147">Retrieving Information About a Specific Shell</span></span>

<span data-ttu-id="9d7b6-148">系統管理員或使用者也可以使用 ShellId 識別碼來取得 shell 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-148">An administrator or user can also use the ShellId identifier to retrieve information about the shell.</span></span> <span data-ttu-id="9d7b6-149">下列命令示範如何使用 winrm 公用程式來取得特定 shell 的相關資訊： **winrm get shell？ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E**。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-149">The following command demonstrates how to use the winrm utility to get information about a specific shell: **winrm get shell?ShellId=0A6E6A01-8AB2-4037-86CC-BFC826A1244E**.</span></span>

<span data-ttu-id="9d7b6-150">下列以文字為基礎的範例會顯示 shell 資訊的輸出：</span><span class="sxs-lookup"><span data-stu-id="9d7b6-150">The following text-based example displays the output for shell information:</span></span>

``` syntax
Shell
    ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E
    ResourceUri = http://schemas.microsoft.com/wbem/wsman/1/windows/shell/cmd
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin
    OutputStreams = stdout stderr
    ShellRunTime = P0DT0H0M36S
    ShellInactivity = P0DT0H0M35S
```

<span data-ttu-id="9d7b6-151">如需詳細資訊，請參閱下列命令所提供的線上說明： **winrm get-？**。</span><span class="sxs-lookup"><span data-stu-id="9d7b6-151">For more information, see the online help provided by the following command: **winrm get -?**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d7b6-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="9d7b6-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d7b6-153">多重躍點支援</span><span class="sxs-lookup"><span data-stu-id="9d7b6-153">Multi-Hop Support</span></span>](multi-hop-support.md)
</dt> <dt>

[<span data-ttu-id="9d7b6-154">遠端 Shell 的配額管理</span><span class="sxs-lookup"><span data-stu-id="9d7b6-154">Quota Management for Remote Shells</span></span>](quotas.md)
</dt> <dt>

[<span data-ttu-id="9d7b6-155">WS-Management PowerShell 命令的受控參考</span><span class="sxs-lookup"><span data-stu-id="9d7b6-155">Managed Reference for WS-Management PowerShell Commands</span></span>](winrm-powershell-commandlets.md)
</dt> </dl>

 

 




