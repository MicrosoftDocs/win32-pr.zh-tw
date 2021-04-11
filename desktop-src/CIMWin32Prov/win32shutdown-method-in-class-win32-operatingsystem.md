---
description: Win32Shutdown &\# 8194;WMI 類別方法提供 Win32 作業系統所支援的一組完整關機選項。 這些包括登出、關機、重新開機，以及強制登出、關機或重新開機。
ms.assetid: 7108570a-81ba-46d5-8b05-de6194f93f18
ms.tgt_platform: multiple
title: Win32_OperatingSystem 類別的 Win32Shutdown 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2cca60c376859438b40ca35be26a99b115634c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847517"
---
# <a name="win32shutdown-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="93291-104">Win32 作業系統類別的 Win32Shutdown 方法 \_</span><span class="sxs-lookup"><span data-stu-id="93291-104">Win32Shutdown method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="93291-105">**Win32Shutdown**   [WMI 類別](../wmisdk/retrieving-a-class.md)方法提供 Win32 作業系統所支援的一組完整關機選項。</span><span class="sxs-lookup"><span data-stu-id="93291-105">The **Win32Shutdown**   [WMI class](../wmisdk/retrieving-a-class.md) method provides the full set of shutdown options supported by Win32 operating systems.</span></span> <span data-ttu-id="93291-106">這些包括登出、關機、重新開機，以及強制登出、關機或重新開機。</span><span class="sxs-lookup"><span data-stu-id="93291-106">These include logoff, shutdown, reboot, and forcing a logoff, shutdown, or reboot.</span></span>

<span data-ttu-id="93291-107">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="93291-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="93291-108">如需使用此方法的詳細資訊，請參閱 [呼叫方法](../wmisdk/calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="93291-108">For more information about using this method, see [Calling a Method](../wmisdk/calling-a-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="93291-109">語法</span><span class="sxs-lookup"><span data-stu-id="93291-109">Syntax</span></span>


```mof
uint32 Win32Shutdown(
  [in] sint32 Flags,
  [in] sint32 Reserved = 
);
```



## <a name="parameters"></a><span data-ttu-id="93291-110">參數</span><span class="sxs-lookup"><span data-stu-id="93291-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93291-111">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="93291-111">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93291-112">用來關閉電腦的一組點陣圖旗標。</span><span class="sxs-lookup"><span data-stu-id="93291-112">Bitmapped set of flags to shut the computer down.</span></span> <span data-ttu-id="93291-113">若要強制執行命令，請將 Force 旗標 (4) 新增至命令值。</span><span class="sxs-lookup"><span data-stu-id="93291-113">To force a command, add the Force flag (4) to the command value.</span></span> <span data-ttu-id="93291-114">在遠端電腦上使用 Force 搭配關機或重新開機，會立即關閉所有 (包括 WMI、COM 等等) ，或重新開機遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="93291-114">Using Force in conjunction with Shutdown or Reboot on a remote computer immediately shuts down everything (including WMI, COM, and so on), or reboots the remote computer.</span></span> <span data-ttu-id="93291-115">這會產生不定的傳回值。</span><span class="sxs-lookup"><span data-stu-id="93291-115">This results in an indeterminate return value.</span></span>

<dt>

<span data-ttu-id="93291-116">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="93291-116">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="93291-117">**登出-登出** 電腦的使用者。</span><span class="sxs-lookup"><span data-stu-id="93291-117">**Log Off** - Logs the user off the computer.</span></span> <span data-ttu-id="93291-118">登出會停止所有與呼叫 exit 函式之進程的安全性內容相關聯的處理常式、將目前的使用者登出系統，並顯示 [登入] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="93291-118">Logging off stops all processes associated with the security context of the process that called the exit function, logs the current user off the system, and displays the logon dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="93291-119">4 (0x4) </span><span class="sxs-lookup"><span data-stu-id="93291-119">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="93291-120">**強制登出 (0 + 4)** -立即將使用者登出電腦，而且不會通知應用程式登入會話即將結束。</span><span class="sxs-lookup"><span data-stu-id="93291-120">**Forced Log Off (0 + 4)** - Logs the user off the computer immediately and does not notify applications that the logon session is ending.</span></span> <span data-ttu-id="93291-121">這可能會導致資料遺失。</span><span class="sxs-lookup"><span data-stu-id="93291-121">This can result in a loss of data.</span></span>

</dd> <dt>

<span data-ttu-id="93291-122">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="93291-122">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="93291-123">**關機** -將電腦關機至關閉電源的安全點。</span><span class="sxs-lookup"><span data-stu-id="93291-123">**Shutdown** - Shuts down the computer to a point where it is safe to turn off the power.</span></span> <span data-ttu-id="93291-124"> (所有的檔案緩衝區都會排清至磁片，並停止所有執行中的處理常式。 ) 使用者會看到訊息， `It is now safe to turn off your computer.`</span><span class="sxs-lookup"><span data-stu-id="93291-124">(All file buffers are flushed to disk, and all running processes are stopped.) Users see the message, `It is now safe to turn off your computer.`</span></span>

<span data-ttu-id="93291-125">在關機期間，系統會將訊息傳送至每個執行中的應用程式。</span><span class="sxs-lookup"><span data-stu-id="93291-125">During shutdown the system sends a message to each running application.</span></span> <span data-ttu-id="93291-126">應用程式會在處理訊息時執行任何清除，並傳回 True 以表示可以終止它們。</span><span class="sxs-lookup"><span data-stu-id="93291-126">The applications perform any cleanup while processing the message and return True to indicate that they can be terminated.</span></span>

</dd> <dt>

<span data-ttu-id="93291-127">5 (0x5) </span><span class="sxs-lookup"><span data-stu-id="93291-127">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="93291-128">**強制關機 (1 + 4)** -將電腦關閉，以關閉電源的安全點。</span><span class="sxs-lookup"><span data-stu-id="93291-128">**Forced Shutdown (1 + 4)** - Shuts down the computer to a point where it is safe to turn off the power.</span></span> <span data-ttu-id="93291-129"> (所有的檔案緩衝區都會排清至磁片，並停止所有執行中的處理常式。 ) 使用者會看到訊息，` It is now safe to turn off your computer.`</span><span class="sxs-lookup"><span data-stu-id="93291-129">(All file buffers are flushed to disk, and all running processes are stopped.) Users see the message,` It is now safe to turn off your computer.`</span></span>

<span data-ttu-id="93291-130">使用強制關機方法時，所有服務（包括 WMI）都會立即關閉。</span><span class="sxs-lookup"><span data-stu-id="93291-130">When the forced shutdown approach is used, all services, including WMI, are shut down immediately.</span></span> <span data-ttu-id="93291-131">因此，如果您在遠端電腦上執行腳本，您將無法接收傳回值。</span><span class="sxs-lookup"><span data-stu-id="93291-131">Because of this, you will not be able to receive a return value if you are running the script against a remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="93291-132">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="93291-132">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="93291-133">**重新開機** -關機，然後重新開機電腦。</span><span class="sxs-lookup"><span data-stu-id="93291-133">**Reboot** - Shuts down and then restarts the computer.</span></span>

</dd> <dt>

<span data-ttu-id="93291-134">6 (0x6) </span><span class="sxs-lookup"><span data-stu-id="93291-134">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="93291-135">**強制重新開機 (2 + 4)** -關閉然後重新開機電腦。</span><span class="sxs-lookup"><span data-stu-id="93291-135">**Forced Reboot (2 + 4)** - Shuts down and then restarts the computer.</span></span>

<span data-ttu-id="93291-136">使用強制重新開機方法時，所有服務（包括 WMI）都會立即關閉。</span><span class="sxs-lookup"><span data-stu-id="93291-136">When the forced reboot approach is used, all services, including WMI, are shut down immediately.</span></span> <span data-ttu-id="93291-137">因此，如果您在遠端電腦上執行腳本，您將無法接收傳回值。</span><span class="sxs-lookup"><span data-stu-id="93291-137">Because of this, you will not be able to receive a return value if you are running the script against a remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="93291-138">8 (0x8) </span><span class="sxs-lookup"><span data-stu-id="93291-138">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="93291-139">**關閉電腦電源** ，並關閉電源 (（如果有) 問題的電腦支援的話）。</span><span class="sxs-lookup"><span data-stu-id="93291-139">**Power Off** - Shuts down the computer and turns off the power (if supported by the computer in question).</span></span>

</dd> <dt>

<span data-ttu-id="93291-140">12 (0xC) </span><span class="sxs-lookup"><span data-stu-id="93291-140">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="93291-141">**強制關閉 (8 + 4)** -關閉電腦並關閉電源 (（如果有) 問題的電腦支援的話）。</span><span class="sxs-lookup"><span data-stu-id="93291-141">**Forced Power Off (8 + 4)** - Shuts down the computer and turns off the power (if supported by the computer in question).</span></span>

<span data-ttu-id="93291-142">使用強制關機方法時，所有服務（包括 WMI）都會立即關閉。</span><span class="sxs-lookup"><span data-stu-id="93291-142">When the forced power off approach is used, all services, including WMI, are shut down immediately.</span></span> <span data-ttu-id="93291-143">因此，如果您在遠端電腦上執行腳本，您將無法接收傳回值。</span><span class="sxs-lookup"><span data-stu-id="93291-143">Because of this, you will not be able to receive a return value if you are running the script against a remote computer.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="93291-144">*保留* \[在\]</span><span class="sxs-lookup"><span data-stu-id="93291-144">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93291-145">擴充 **Win32Shutdown** 的方法。</span><span class="sxs-lookup"><span data-stu-id="93291-145">A means to extend **Win32Shutdown**.</span></span> <span data-ttu-id="93291-146">目前， *保留* 的參數會被忽略。</span><span class="sxs-lookup"><span data-stu-id="93291-146">Currently, the *Reserved* parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93291-147">傳回值</span><span class="sxs-lookup"><span data-stu-id="93291-147">Return value</span></span>

<span data-ttu-id="93291-148">傳回零 (0) 表示成功。</span><span class="sxs-lookup"><span data-stu-id="93291-148">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="93291-149">任何其他數字表示發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="93291-149">Any other number indicates an error.</span></span> <span data-ttu-id="93291-150">如需錯誤碼，請參閱 [**WMI 錯誤常數**](../wmisdk/wmi-error-constants.md) 或 [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="93291-150">For error codes, see [**WMI Error Constants**](../wmisdk/wmi-error-constants.md) or [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="93291-151">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](../debug/system-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="93291-151">For general **HRESULT** values, see [System Error Codes](../debug/system-error-codes.md).</span></span>

<dl> <dt>

<span data-ttu-id="93291-152">**成功** (0) </span><span class="sxs-lookup"><span data-stu-id="93291-152">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="93291-153">**其他** (1 – 4294967295) </span><span class="sxs-lookup"><span data-stu-id="93291-153">**Other** (1–4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="93291-154">備註</span><span class="sxs-lookup"><span data-stu-id="93291-154">Remarks</span></span>

<span data-ttu-id="93291-155">若要更有效率地管理組織中的電腦，系統管理員必須能夠從遠端關機或重新開機電腦，或是從遠端登出使用者。</span><span class="sxs-lookup"><span data-stu-id="93291-155">For more efficient management of computers in an organization, administrators need the ability to remotely shut down or restart a computer, or to remotely log off a user.</span></span> <span data-ttu-id="93291-156">執行這些工作的能力可讓系統管理員安裝軟體、重新設定電腦設定、從網路移除電腦，以及執行其他工作，而不需要手動將每部電腦關機或重新開機。</span><span class="sxs-lookup"><span data-stu-id="93291-156">The ability to carry out these tasks allows administrators to install software, reconfigure computer settings, remove computers from the network, and perform other tasks without having to manually shut down or restart each computer.</span></span>

<span data-ttu-id="93291-157">例如，若要執行網路升級，您可能需要關閉在特定網路區段上執行的所有電腦。</span><span class="sxs-lookup"><span data-stu-id="93291-157">For example, to perform a network upgrade, you might need to shut down all the computers running on a particular network segment.</span></span> <span data-ttu-id="93291-158">若要強制群組原則升級，您需要將使用者登出其電腦。</span><span class="sxs-lookup"><span data-stu-id="93291-158">To force a Group Policy upgrade, you need to log users off their computers.</span></span> <span data-ttu-id="93291-159">如果您組織中的任何地方都有電腦病毒，您可能會想要盡可能關閉電腦的數量，然後才能讓病毒擴散。</span><span class="sxs-lookup"><span data-stu-id="93291-159">If a computer virus is present anywhere in your organization, you might want to shut down as many computers as possible, before the virus has an opportunity to spread.</span></span> <span data-ttu-id="93291-160">關閉和重新開機電腦，並以程式設計方式（而不是手動）登出使用者的能力，可能是相當耗時的時間。</span><span class="sxs-lookup"><span data-stu-id="93291-160">The ability to shut down and restart computers and to log off users programmatically instead of manually can be an enormous time-saver.</span></span>

<span data-ttu-id="93291-161">呼叫進程必須具有 **SE \_ SHUTDOWN \_ 名稱** 許可權。</span><span class="sxs-lookup"><span data-stu-id="93291-161">The calling process must have the **SE\_SHUTDOWN\_NAME** privilege.</span></span>

<span data-ttu-id="93291-162">[**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md)方法提供 [**Win32 \_ 作業系統**](win32-operatingsystem.md)中的 **Win32Shutdown** 方法所支援的一組相同關機選項，但是它也可讓您指定批註、關機原因或超時。</span><span class="sxs-lookup"><span data-stu-id="93291-162">The [**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) method provides the same set of shutdown options supported by the **Win32Shutdown** method in [**Win32\_OperatingSystem**](win32-operatingsystem.md) but it also allows you to specify comments, a reason for shutdown, or a timeout.</span></span>

<span data-ttu-id="93291-163">Win32Shutdown 方法沒有鎖定工作站的參數，讓使用者登入。</span><span class="sxs-lookup"><span data-stu-id="93291-163">The Win32Shutdown method does not have a parameter for locking a workstation, leaving the user logged on.</span></span> <span data-ttu-id="93291-164">不過，您可以使用下列命令，從命令列鎖定工作站：</span><span class="sxs-lookup"><span data-stu-id="93291-164">However, workstations can be locked from the command line by using the following command:</span></span>

`% windir %\System32\rundll32.exe user32.dll,LockWorkStation`

## <a name="examples"></a><span data-ttu-id="93291-165">範例</span><span class="sxs-lookup"><span data-stu-id="93291-165">Examples</span></span>

<span data-ttu-id="93291-166">在 TechNet 資源庫上 [登出、重新開機或關機多部電腦](https://Gallery.TechNet.Microsoft.Com/2e88d504-a4e5-499b-b09a-f90617a6d87d) VBScript 範例會使用 Win32Shutdown 來登出、關機、重新開機或關閉 (，視伺服器陣列中列出的電腦) 選取專案而定。</span><span class="sxs-lookup"><span data-stu-id="93291-166">The [Log Out, Reboot, or Shut Down Multiple Computers](https://Gallery.TechNet.Microsoft.Com/2e88d504-a4e5-499b-b09a-f90617a6d87d) VBScript sample on TechNet Gallery uses Win32Shutdown to log off, shut down, reboot, or power off (depending on the selection) the computers listed in the Server array.</span></span>

<span data-ttu-id="93291-167">TechNet 元件庫上的 [ComputerManagement.ps1](https://Gallery.TechNet.Microsoft.Com/ef8de213-45b6-4751-8c77-01d1b6623e16) PowerShell 範例包含一個方法，該方法會在遠端電腦上呼叫 Win32Shutdown。</span><span class="sxs-lookup"><span data-stu-id="93291-167">The [ComputerManagement.ps1](https://Gallery.TechNet.Microsoft.Com/ef8de213-45b6-4751-8c77-01d1b6623e16) PowerShell sample on TechNet Gallery includes a method that calls Win32Shutdown on a remote computer.</span></span>

<span data-ttu-id="93291-168">下列 PowerShell 範例會使用 Win32Shutdown 方法來關閉指定的電腦。</span><span class="sxs-lookup"><span data-stu-id="93291-168">The following PowerShell example uses the Win32Shutdown method to shut down the specified computer.</span></span>


```PowerShell
$computername= "."
$win32OS = get-wmiobject win32_operatingsystem -computername $computername
$win32OS.psbase.Scope.Options.EnablePrivileges = $true
$win32OS.win32shutdown(8)
```



<span data-ttu-id="93291-169">下列 PowerShell 程式碼範例會使用 EnableAllPrivileges from >get-wmiobject Cmdlet 來完成適當的許可權。</span><span class="sxs-lookup"><span data-stu-id="93291-169">The following PowerShell code sample uses the EnableAllPrivileges from get-wmiobject cmdlet to achieve the proper priviliges.</span></span>


```PowerShell
$win32OS = get-wmiobject win32_operatingsystem -computername $computername -EnableAllPrivileges
$win32OS.win32shutdown(8)
```



<span data-ttu-id="93291-170">下列 VB.NET 範例程式碼會使用 Shutdown 方法來重新開機或登出系統。</span><span class="sxs-lookup"><span data-stu-id="93291-170">The following VB.NET sample code uses the Shutdown method to reboot or log off a system.</span></span>


```VB
Dim

testResult AsSingle

Dim WMIServiceObject, ComputerObject AsObject 

'Now get some privileges 

WMIServiceObject = GetObject(
"Winmgmts:{impersonationLevel=impersonate,(Debug,Shutdown)}")
ForEach ComputerObject In WMIServiceObject.InstancesOf("Win32_OperatingSystem") 
    testResult = ComputerObject.Win32Shutdown(2 + 4, 0) 
    'reboot
    'testResult = ComputerObject.Win32Shutdown(0, 0) 'logoff 
    ' testResult = ComputerObject.Win32Shutdown(8 + 4, 0) 'shutdown 

If testResult <> 0 Then 

MsgBox("Sorry, an error has occurred while trying to perform selected operation") 

Else 

'Operation selected in statement above if condition would be carried out 

EndIf 

Next
```



## <a name="requirements"></a><span data-ttu-id="93291-171">規格需求</span><span class="sxs-lookup"><span data-stu-id="93291-171">Requirements</span></span>



| <span data-ttu-id="93291-172">需求</span><span class="sxs-lookup"><span data-stu-id="93291-172">Requirement</span></span> | <span data-ttu-id="93291-173">值</span><span class="sxs-lookup"><span data-stu-id="93291-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93291-174">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93291-174">Minimum supported client</span></span><br/> | <span data-ttu-id="93291-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93291-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="93291-176">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93291-176">Minimum supported server</span></span><br/> | <span data-ttu-id="93291-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93291-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="93291-178">命名空間</span><span class="sxs-lookup"><span data-stu-id="93291-178">Namespace</span></span><br/>                | <span data-ttu-id="93291-179">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="93291-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="93291-180">MOF</span><span class="sxs-lookup"><span data-stu-id="93291-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93291-181"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="93291-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="93291-182">DLL</span><span class="sxs-lookup"><span data-stu-id="93291-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93291-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93291-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93291-184">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93291-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93291-185">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="93291-185">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="93291-186">**Win32 \_ 作業系統**</span><span class="sxs-lookup"><span data-stu-id="93291-186">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="93291-187">**Win32ShutdownTracker**</span><span class="sxs-lookup"><span data-stu-id="93291-187">**Win32ShutdownTracker**</span></span>](win32shutdowntracker-method-in-class-win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="93291-188">WMI 工作：桌面管理</span><span class="sxs-lookup"><span data-stu-id="93291-188">WMI Tasks: Desktop Management</span></span>](../wmisdk/wmi-tasks--desktop-management.md)
</dt> <dt>

[<span data-ttu-id="93291-189">使用 VBScript 執行特殊許可權作業</span><span class="sxs-lookup"><span data-stu-id="93291-189">Executing Privileged Operations Using VBScript</span></span>](../wmisdk/executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

 
