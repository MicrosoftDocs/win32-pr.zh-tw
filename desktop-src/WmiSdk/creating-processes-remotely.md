---
description: 您可以使用 Win32 \_ 進程建立，在遠端電腦上執行腳本或應用程式。 不過，基於安全性理由，此程式不能是互動式的。 在 \_ 本機電腦上呼叫 Win32 進程時，進程可以是互動式的。
ms.assetid: 11fea8b1-7d05-4f44-9103-ea804a1d4b38
ms.tgt_platform: multiple
title: 使用 WMI 從遠端建立進程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e7b97f8f4fdddd608f6ee8c3368bde6ad6e854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694472"
---
# <a name="creating-processes-remotely-using-wmi"></a><span data-ttu-id="7c608-105">使用 WMI 從遠端建立進程</span><span class="sxs-lookup"><span data-stu-id="7c608-105">Creating Processes Remotely using WMI</span></span>

<span data-ttu-id="7c608-106">您可以使用 [**Win32 \_ 進程建立**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) ，在遠端電腦上執行腳本或應用程式。</span><span class="sxs-lookup"><span data-stu-id="7c608-106">You can use [**Win32\_Process.Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) to execute a script or application on a remote computer.</span></span> <span data-ttu-id="7c608-107">不過，基於安全性理由，此程式不能是互動式的。</span><span class="sxs-lookup"><span data-stu-id="7c608-107">However, for security reasons, the process cannot be interactive.</span></span> <span data-ttu-id="7c608-108">在本機電腦上呼叫 **Win32 \_ 進程** 時，進程可以是互動式的。</span><span class="sxs-lookup"><span data-stu-id="7c608-108">When **Win32\_Process.Create** is called on the local computer, the process can be interactive.</span></span>

> [!WARNING]
> <span data-ttu-id="7c608-109">本主題說明使用 WMI 建立遠端進程的一般程式。</span><span class="sxs-lookup"><span data-stu-id="7c608-109">This topic describes the general procedure for creating a remote process with WMI.</span></span> <span data-ttu-id="7c608-110">如果您只是想要在遠端系統上執行腳本，請參閱 [從 Windows Vista 開始遠端連線到 wmi](connecting-to-wmi-remotely-starting-with-vista.md)，或 [使用 Windows PowerShell 連接到遠端電腦上的 wmi](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)。</span><span class="sxs-lookup"><span data-stu-id="7c608-110">If you are simply looking to run a script on a remote system, see [Connecting to WMI Remotely Starting with Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md), or [Connecting to WMI on a Remote Computer by Using Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).</span></span> <span data-ttu-id="7c608-111">如需有關使用 PowerShell 進行遠端處理的一般資訊，請參閱執行 [遠端命令](https://technet.microsoft.com/library/dd819505.aspx)。</span><span class="sxs-lookup"><span data-stu-id="7c608-111">For more general information on remoting with PowerShell, see [Running Remote Commands](https://technet.microsoft.com/library/dd819505.aspx).</span></span>

 

<span data-ttu-id="7c608-112">遠端進程沒有使用者介面，但會列在 **工作管理員** 中。</span><span class="sxs-lookup"><span data-stu-id="7c608-112">The remote process has no user interface but it is listed in the **Task Manager**.</span></span> <span data-ttu-id="7c608-113">如果帳戶具有根 cimv2 命名空間的 **Execute 方法** 許可權，在本機建立的進程可以在任何帳戶下執行 \\ 。</span><span class="sxs-lookup"><span data-stu-id="7c608-113">A process created locally can run under any account if the account has the **Execute Method** permission for the root\\cimv2 namespace.</span></span> <span data-ttu-id="7c608-114">如果帳戶具有 [ **執行方法** ] 和 [ **遠端啟用** 根 cimv2 的許可權]，則遠端建立的進程可以在任何帳戶下執行 \\ 。</span><span class="sxs-lookup"><span data-stu-id="7c608-114">A process created remotely can run under any account if the account has the **Execute Method** and **Remote Enable** permissions for root\\cimv2.</span></span> <span data-ttu-id="7c608-115">[ **執行方法** ] 和 [ **遠端啟用** ] 許可權是在主控台的 WMI 控制中設定。</span><span class="sxs-lookup"><span data-stu-id="7c608-115">The **Execute Method** and **Remote Enable** permissions are set in WMI Control in the Control Panel.</span></span> <span data-ttu-id="7c608-116">如需詳細資訊，請參閱 [使用 WMI 控制項設定命名空間安全性](setting-namespace-security-with-the-wmi-control.md)。</span><span class="sxs-lookup"><span data-stu-id="7c608-116">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>

<span data-ttu-id="7c608-117">您可以使用 [**Win32 \_ register-scheduledjob**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob) 建立遠端的互動式進程。</span><span class="sxs-lookup"><span data-stu-id="7c608-117">You can use [**Win32\_ScheduledJob.Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob) to create an interactive process remotely.</span></span> <span data-ttu-id="7c608-118">但是由 **Win32 \_ register-scheduledjob** 啟動的進程會在 LocalSystem 帳戶下執行，而該帳戶可授與過多的許可權。</span><span class="sxs-lookup"><span data-stu-id="7c608-118">But processes started by **Win32\_ScheduledJob.Create** run under the LocalSystem account that can confer too much privilege.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c608-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="7c608-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c608-120">保護遠端 WMI 連接</span><span class="sxs-lookup"><span data-stu-id="7c608-120">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> <dt>

[<span data-ttu-id="7c608-121">連接到第三台電腦-委派</span><span class="sxs-lookup"><span data-stu-id="7c608-121">Connecting to a 3rd Computer-Delegation</span></span>](connecting-to-a-3rd-computer-delegation.md)
</dt> </dl>

 

 
