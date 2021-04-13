---
title: 遠端 Shell 的配額管理
description: 配額管理可讓使用者更有效率地管理系統資源。
ms.assetid: 6651a500-a95a-45a1-b46a-27b2e9b36a1c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1310efd37b913ae0bf8394015f6df792711ac6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301759"
---
# <a name="quota-management-for-remote-shells"></a><span data-ttu-id="70a23-103">遠端 Shell 的配額管理</span><span class="sxs-lookup"><span data-stu-id="70a23-103">Quota Management for Remote Shells</span></span>

<span data-ttu-id="70a23-104">配額管理可讓使用者更有效率地管理系統資源。</span><span class="sxs-lookup"><span data-stu-id="70a23-104">Quota management allows users to manage system resources more efficiently.</span></span> <span data-ttu-id="70a23-105">Windows 遠端管理 (WinRM) 已新增一組特定的配額，以提供更好的服務品質、協助防止阻絕服務問題，以及將伺服器資源配置給並行使用者。</span><span class="sxs-lookup"><span data-stu-id="70a23-105">Windows Remote Management (WinRM) has added a specific set of quotas that provide a better quality of service, help prevent denial of service issues, and allocate server resources to concurrent users.</span></span> <span data-ttu-id="70a23-106">WinRM 配額的設定是以針對 Internet Information Services (IIS) 服務所執行的配額基礎結構為基礎。</span><span class="sxs-lookup"><span data-stu-id="70a23-106">The WinRM quota set is based on the quota infrastructure that is implemented for the Internet Information Services (IIS) service.</span></span>

<span data-ttu-id="70a23-107">藉由執行下列動作，執行配額有助於防止效能降低和拒絕服務問題：</span><span class="sxs-lookup"><span data-stu-id="70a23-107">Implementing quotas will help to prevent performance degradation and denial of service issues by doing the following:</span></span>

-   <span data-ttu-id="70a23-108">限制使用者可以建立的 shell 和 shell 進程數目</span><span class="sxs-lookup"><span data-stu-id="70a23-108">Limiting the number of shells and shell processes that a user can create</span></span>
-   <span data-ttu-id="70a23-109">限制並行使用者數目上限</span><span class="sxs-lookup"><span data-stu-id="70a23-109">Limiting the maximum number of concurrent users</span></span>
-   <span data-ttu-id="70a23-110">管理配置給 shell 的記憶體數量</span><span class="sxs-lookup"><span data-stu-id="70a23-110">Managing the amount of memory that is allocated to a shell</span></span>
-   <span data-ttu-id="70a23-111">為非使用中的 shell 設定超時時間</span><span class="sxs-lookup"><span data-stu-id="70a23-111">Setting a time-out for shells that are inactive</span></span>

## <a name="quota-settings"></a><span data-ttu-id="70a23-112">配額設定</span><span class="sxs-lookup"><span data-stu-id="70a23-112">Quota Settings</span></span>

<span data-ttu-id="70a23-113">下列配額需要針對遠端 shell 管理強制執行。</span><span class="sxs-lookup"><span data-stu-id="70a23-113">The following quotas need to be enforced for remote shell management.</span></span> <span data-ttu-id="70a23-114">您可以透過 winrm 公用程式或群組原則設定來設定這些配額。</span><span class="sxs-lookup"><span data-stu-id="70a23-114">These quotas can be configured through the winrm utility or through Group Policy settings.</span></span> <span data-ttu-id="70a23-115">群組原則設定的設定會取代 winrm 公用程式所設定的配額。</span><span class="sxs-lookup"><span data-stu-id="70a23-115">Settings configured by a Group Policy supersede the quotas set by the winrm utility.</span></span> <span data-ttu-id="70a23-116">如需設定 WinRM 群組原則的詳細資訊，請參閱 [Windows 遠端管理的安裝和](installation-and-configuration-for-windows-remote-management.md)設定。</span><span class="sxs-lookup"><span data-stu-id="70a23-116">For more information about setting Group Policies for WinRM, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

<dl> <dt>

<span data-ttu-id="70a23-117"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="70a23-117"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span></span>
</dt> <dd>

<span data-ttu-id="70a23-118">刪除非作用中遠端 shell 之前的最長時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="70a23-118">The maximum time in milliseconds before an inactive remote shell is deleted.</span></span> <span data-ttu-id="70a23-119">預設值為180000毫秒。</span><span class="sxs-lookup"><span data-stu-id="70a23-119">The default is 180000 milliseconds.</span></span> <span data-ttu-id="70a23-120">最短時間是1000毫秒。</span><span class="sxs-lookup"><span data-stu-id="70a23-120">The minimum time is 1000 milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="70a23-121"><span id="MaxProcessesPerShell"></span><span id="maxprocessespershell"></span><span id="MAXPROCESSESPERSHELL"></span>MaxProcessesPerShell</span><span class="sxs-lookup"><span data-stu-id="70a23-121"><span id="MaxProcessesPerShell"></span><span id="maxprocessespershell"></span><span id="MAXPROCESSESPERSHELL"></span>MaxProcessesPerShell</span></span>
</dt> <dd>

<span data-ttu-id="70a23-122">每個 shell 允許的進程數目上限，包括 shell 的子進程。</span><span class="sxs-lookup"><span data-stu-id="70a23-122">The maximum number of processes allowed per shell, including the shell's child processes.</span></span> <span data-ttu-id="70a23-123">預設值為 25。</span><span class="sxs-lookup"><span data-stu-id="70a23-123">The default is 25.</span></span>

</dd> <dt>

<span data-ttu-id="70a23-124"><span id="MaxMemoryPerShellMB"></span><span id="maxmemorypershellmb"></span><span id="MAXMEMORYPERSHELLMB"></span>MaxMemoryPerShellMB</span><span class="sxs-lookup"><span data-stu-id="70a23-124"><span id="MaxMemoryPerShellMB"></span><span id="maxmemorypershellmb"></span><span id="MAXMEMORYPERSHELLMB"></span>MaxMemoryPerShellMB</span></span>
</dt> <dd>

<span data-ttu-id="70a23-125">每個 shell 配置的記憶體數量上限，包括 shell 的子進程。</span><span class="sxs-lookup"><span data-stu-id="70a23-125">The maximum amount of memory allocated per shell, including the shell's child processes.</span></span> <span data-ttu-id="70a23-126">預設值為 1024 MB。</span><span class="sxs-lookup"><span data-stu-id="70a23-126">The default is 1024 MB.</span></span>

> [!Note]  
> <span data-ttu-id="70a23-127">如果將 MaxMemoryPerShellMB 設定為小於預設值，則不支援此行為。</span><span class="sxs-lookup"><span data-stu-id="70a23-127">The behavior is unsupported if the MaxMemoryPerShellMB is set to a value that is less than the default.</span></span>

 

</dd> <dt>

<span data-ttu-id="70a23-128"><span id="MaxShellsPerUser"></span><span id="maxshellsperuser"></span><span id="MAXSHELLSPERUSER"></span>MaxShellsPerUser</span><span class="sxs-lookup"><span data-stu-id="70a23-128"><span id="MaxShellsPerUser"></span><span id="maxshellsperuser"></span><span id="MAXSHELLSPERUSER"></span>MaxShellsPerUser</span></span>
</dt> <dd>

<span data-ttu-id="70a23-129">每位使用者的最大 shell 數目。</span><span class="sxs-lookup"><span data-stu-id="70a23-129">The maximum number of shells per user.</span></span> <span data-ttu-id="70a23-130">預設值是 30。</span><span class="sxs-lookup"><span data-stu-id="70a23-130">The default is 30.</span></span>

</dd> <dt>

<span data-ttu-id="70a23-131"><span id="MaxConcurrentUsers"></span><span id="maxconcurrentusers"></span><span id="MAXCONCURRENTUSERS"></span>MaxConcurrentUsers</span><span class="sxs-lookup"><span data-stu-id="70a23-131"><span id="MaxConcurrentUsers"></span><span id="maxconcurrentusers"></span><span id="MAXCONCURRENTUSERS"></span>MaxConcurrentUsers</span></span>
</dt> <dd>

<span data-ttu-id="70a23-132">可以開啟 shell 的並行使用者數目上限。</span><span class="sxs-lookup"><span data-stu-id="70a23-132">The maximum number of concurrent users who can open shells.</span></span> <span data-ttu-id="70a23-133">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="70a23-133">The default is 10.</span></span>

</dd> </dl>

## <a name="deprecated-quotas"></a><span data-ttu-id="70a23-134">已淘汰配額</span><span class="sxs-lookup"><span data-stu-id="70a23-134">Deprecated Quotas</span></span>

<span data-ttu-id="70a23-135">WinRM 2.0 將 MaxShellRunTime 配額設定為唯讀。</span><span class="sxs-lookup"><span data-stu-id="70a23-135">WinRM 2.0 sets the MaxShellRunTime quota to read-only.</span></span> <span data-ttu-id="70a23-136">變更此配額的值將不會影響遠端 shell。</span><span class="sxs-lookup"><span data-stu-id="70a23-136">Changing the value for this quota will have no effect on the remote shells.</span></span>

## <a name="retrieving-quota-configuration-information"></a><span data-ttu-id="70a23-137">正在抓取配額設定資訊</span><span class="sxs-lookup"><span data-stu-id="70a23-137">Retrieving Quota Configuration Information</span></span>

<span data-ttu-id="70a23-138">若要檢查配額設定，請輸入 **winrm get winrm/config**。</span><span class="sxs-lookup"><span data-stu-id="70a23-138">To check the quota configuration settings, type **winrm get winrm/config**.</span></span>

<span data-ttu-id="70a23-139">下列程式碼片段是以文字為基礎的 WinRM 設定範例，具有預設配額設定。</span><span class="sxs-lookup"><span data-stu-id="70a23-139">The following snippet is a text-based example of a WinRM configuration with the default quota settings.</span></span>

``` syntax
Config

          ...         

          Winrs

                   AllowRemoteShellAccess = true

                   IdleTimeout = 7200000

                   MaxConcurrentUsers = 10

                   MaxProcessesPerShell = 25

                   MaxMemoryPerShellMB = 1024

                   MaxShellsPerUser = 30
```

## <a name="configuring-shell-quotas"></a><span data-ttu-id="70a23-140">設定 Shell 配額</span><span class="sxs-lookup"><span data-stu-id="70a23-140">Configuring Shell Quotas</span></span>

<span data-ttu-id="70a23-141">您可以透過群組原則設定或手動設定配額。</span><span class="sxs-lookup"><span data-stu-id="70a23-141">Quotas can be set through a Group Policy setting or manually.</span></span> <span data-ttu-id="70a23-142">如需特定設定的詳細資訊，請參閱 [Windows 遠端管理的安裝和](installation-and-configuration-for-windows-remote-management.md)設定。</span><span class="sxs-lookup"><span data-stu-id="70a23-142">For more information about specific configuration settings, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

<span data-ttu-id="70a23-143">**使用群組原則設定配額**</span><span class="sxs-lookup"><span data-stu-id="70a23-143">**To set a quota with Group Policy**</span></span>

1.  <span data-ttu-id="70a23-144">以系統管理員身分開啟 [命令提示字元] 視窗。</span><span class="sxs-lookup"><span data-stu-id="70a23-144">Open a Command Prompt window as an administrator.</span></span>
2.  <span data-ttu-id="70a23-145">在命令提示字元中，輸入 **gpedit.msc**。</span><span class="sxs-lookup"><span data-stu-id="70a23-145">At the Command Prompt, type **gpedit.msc**.</span></span> <span data-ttu-id="70a23-146">**群組原則物件編輯器**] 視窗隨即開啟。</span><span class="sxs-lookup"><span data-stu-id="70a23-146">The **Group Policy Object Editor** window opens.</span></span>
3.  <span data-ttu-id="70a23-147">在 [電腦設定] **\\ 系統管理範本 [ \\ windows 元件**] 下的 [電腦設定] 底下，尋找 **Windows 遠端管理** 和 **WINDOWS 遠端 Shell** 群組原則物件 () GPO</span><span class="sxs-lookup"><span data-stu-id="70a23-147">Find the **Windows Remote Management** and **Windows Remote Shell** Group Policy Objects (GPO) under **Computer Configuration\\Administrative Templates\\Windows Components**.</span></span>
4.  <span data-ttu-id="70a23-148">在 [ **擴充** ] 索引標籤上，選取設定以查看描述。</span><span class="sxs-lookup"><span data-stu-id="70a23-148">On the **Extended** tab, select a setting to see a description.</span></span> <span data-ttu-id="70a23-149">按兩下設定以進行編輯。</span><span class="sxs-lookup"><span data-stu-id="70a23-149">Double click a setting to edit it.</span></span>

<span data-ttu-id="70a23-150">**手動設定配額**</span><span class="sxs-lookup"><span data-stu-id="70a23-150">**To set a quota manually**</span></span>

1.  <span data-ttu-id="70a23-151">以系統管理員身分開啟 [命令提示字元] 視窗。</span><span class="sxs-lookup"><span data-stu-id="70a23-151">Open a Command Prompt window as an administrator.</span></span>
2.  <span data-ttu-id="70a23-152">在命令提示字元中，輸入 **winrm set winrm/config/winrs ' @ { ***<Quota>*** = " ***<Value>*** "} '**</span><span class="sxs-lookup"><span data-stu-id="70a23-152">At the Command Prompt, type **winrm set winrm/config/winrs '@{***<Quota>***="***<Value>***"}'**</span></span>

<span data-ttu-id="70a23-153">例如，若要將每位使用者的最大 shell 數目從5增加到7，請輸入 **winrm set winrm/config/winrs ' @ {MaxShellsPerUser = "7"} '**。</span><span class="sxs-lookup"><span data-stu-id="70a23-153">For example, to increase the maximum number of shells per user from 5 to 7, type **winrm set winrm/config/winrs '@{MaxShellsPerUser="7"}'**.</span></span>

 

 




