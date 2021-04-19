---
description: Create&\# 8194;WMI 類別方法會建立新的進程。
ms.assetid: be80abec-fab4-4403-bc29-d0d4a38e3c87
ms.tgt_platform: multiple
title: Win32_Process 類別的 Create 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 42c675f61fc8b42790aeb811ec275554b355a392
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970320"
---
# <a name="create-method-of-the-win32_process-class"></a><span data-ttu-id="b8b4d-103">Win32 進程類別的 Create 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b8b4d-103">Create method of the Win32\_Process class</span></span>

<span data-ttu-id="b8b4d-104">**建立** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會建立新的進程。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new process.</span></span>

<span data-ttu-id="b8b4d-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b8b4d-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b8b4d-107">語法</span><span class="sxs-lookup"><span data-stu-id="b8b4d-107">Syntax</span></span>


```mof
uint32 Create(
  [in]  string               CommandLine,
  [in]  string               CurrentDirectory,
  [in]  Win32_ProcessStartup ProcessStartupInformation,
  [out] uint32               ProcessId
);
```



## <a name="parameters"></a><span data-ttu-id="b8b4d-108">參數</span><span class="sxs-lookup"><span data-stu-id="b8b4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8b4d-109">*命令列* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8b4d-109">*CommandLine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8b4d-110">要執行的命令列。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-110">Command line to execute.</span></span> <span data-ttu-id="b8b4d-111">系統會將 null 字元新增至命令列，並視需要修剪字串，以指出實際使用的檔案。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-111">The system adds a null character to the command line, trimming the string if necessary, to indicate which file was actually used.</span></span>

</dd> <dt>

<span data-ttu-id="b8b4d-112">*CurrentDirectory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8b4d-112">*CurrentDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8b4d-113">子進程的目前磁片磁碟機和目錄。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-113">Current drive and directory for the child process.</span></span> <span data-ttu-id="b8b4d-114">字串要求目前的目錄解析為已知的路徑。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-114">The string requires that the current directory resolves to a known path.</span></span> <span data-ttu-id="b8b4d-115">使用者可以指定絕對路徑或相對於目前工作目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-115">A user can specify an absolute path or a path relative to the current working directory.</span></span> <span data-ttu-id="b8b4d-116">如果這個參數為 **Null**，則新的進程會有與呼叫進程相同的路徑。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-116">If this parameter is **NULL**, the new process will have the same path as the calling process.</span></span> <span data-ttu-id="b8b4d-117">此選項主要是針對必須啟動應用程式，並指定應用程式初始磁片磁碟機和工作目錄的 shell 所提供。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-117">This option is provided primarily for shells that must start an application and specify the application's initial drive and working directory.</span></span>

</dd> <dt>

<span data-ttu-id="b8b4d-118">*ProcessStartupInformation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8b4d-118">*ProcessStartupInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8b4d-119">Windows 進程的啟動設定。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-119">The startup configuration of a Windows process.</span></span> <span data-ttu-id="b8b4d-120">如需詳細資訊，請參閱 [**Win32 \_ ProcessStartup**](win32-processstartup.md)。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-120">For more information, see [**Win32\_ProcessStartup**](win32-processstartup.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b4d-121">*ProcessId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b8b4d-121">*ProcessId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8b4d-122">可以用來識別進程的全域處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-122">Global process identifier that can be used to identify a process.</span></span> <span data-ttu-id="b8b4d-123">此值是從建立程式到進程結束之前的有效時間。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-123">The value is valid from the time the process is created until the time the process is terminated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8b4d-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8b4d-124">Return value</span></span>

<span data-ttu-id="b8b4d-125">如果成功建立進程，則傳回 0 (零) ，以及表示錯誤的其他任何數位。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-125">Returns a value of 0 (zero) if the process was successfully created, and any other number to indicate an error.</span></span> <span data-ttu-id="b8b4d-126">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-126">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b8b4d-127">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-127">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b8b4d-128">**成功完成** (0) </span><span class="sxs-lookup"><span data-stu-id="b8b4d-128">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b8b4d-129">**拒絕存取** (2) </span><span class="sxs-lookup"><span data-stu-id="b8b4d-129">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b8b4d-130">**許可權不足** (3) </span><span class="sxs-lookup"><span data-stu-id="b8b4d-130">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b8b4d-131">**未知的失敗** (8) </span><span class="sxs-lookup"><span data-stu-id="b8b4d-131">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="b8b4d-132"> (9) **找不到路徑**</span><span class="sxs-lookup"><span data-stu-id="b8b4d-132">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="b8b4d-133">**不正確參數** (21) </span><span class="sxs-lookup"><span data-stu-id="b8b4d-133">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="b8b4d-134">**其他** (22 4294967295) </span><span class="sxs-lookup"><span data-stu-id="b8b4d-134">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="b8b4d-135">備註</span><span class="sxs-lookup"><span data-stu-id="b8b4d-135">Remarks</span></span>

<span data-ttu-id="b8b4d-136">您可以建立 [**Win32 \_ ProcessStartup**](win32-processstartup.md) 類別的實例，以在呼叫這個方法之前設定處理常式。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-136">You can create an instance of the [**Win32\_ProcessStartup**](win32-processstartup.md) class to configure the process before calling this method.</span></span>

<span data-ttu-id="b8b4d-137">如果要啟動的程式不在 Winmgmt.exe 的搜尋路徑中，就必須指定完整路徑。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-137">A fully qualified path must be specified in cases where the program to be launched is not in the search path of Winmgmt.exe.</span></span> <span data-ttu-id="b8b4d-138">如果新建立的進程嘗試與目標系統上的物件進行互動，但沒有適當的存取權限，它就會終止，而不會通知這個方法。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-138">If the newly created process attempts to interact with objects on the target system without the appropriate access privileges, it is terminated without notification to this method.</span></span>

<span data-ttu-id="b8b4d-139">基於安全性理由， **Win32 \_ 進程** 無法使用 Create 方法從遠端啟動互動式進程。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-139">For security reasons the **Win32\_Process.Create** method cannot be used to start an interactive process remotely.</span></span>

<span data-ttu-id="b8b4d-140">使用 **Win32 \_ 進程** 建立的進程。除非指定了 **create \_ BREAKAWAY \_ FROM \_ job** 旗標，否則 create 方法會受到工作物件的限制。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-140">Processes created with the **Win32\_Process.Create** method are limited by the job object unless the **CREATE\_BREAKAWAY\_FROM\_JOB** flag is specified.</span></span> <span data-ttu-id="b8b4d-141">如需詳細資訊，請參閱 [**Win32 \_ ProcessStartup**](win32-processstartup.md)和 [**\_ \_ ProviderHostQuotaConfiguration**](/windows/desktop/WmiSdk/--providerhostquotaconfiguration)。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-141">For more information, see [**Win32\_ProcessStartup**](win32-processstartup.md) and [**\_\_ProviderHostQuotaConfiguration**](/windows/desktop/WmiSdk/--providerhostquotaconfiguration).</span></span>

## <a name="examples"></a><span data-ttu-id="b8b4d-142">範例</span><span class="sxs-lookup"><span data-stu-id="b8b4d-142">Examples</span></span>

<span data-ttu-id="b8b4d-143">下列 VBScript 範例示範如何叫用 CIM 方法，如同它是 SWbemObject 的自動化方法。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-143">The following VBScript example demonstrates how to invoke a CIM method as if it were an automation method of SWbemObject.</span></span>


```VB
on error resume next

set process = GetObject("winmgmts:Win32_Process")

result = process.Create ("notepad.exe",null,null,processid)

WScript.Echo "Method returned result = " & result
WScript.Echo "Id of new process is " & processid

if err <>0 then
 WScript.Echo Err.Description, "0x" & Hex(Err.Number)
end if
```



<span data-ttu-id="b8b4d-144">下列 Perl 範例示範如何叫用 CIM 方法，如同它是 SWbemObject 的自動化方法。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-144">The following Perl example demonstrates how to invoke a CIM method as if it were an automation method of SWbemObject.</span></span>


```VB
use strict;
use Win32::OLE;

my ($process, $outParam, $processid, $inParam, $objMethod);

eval { $process = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2:Win32_Process"); };

if (!$@ && defined $process)
{
 $objMethod = $process->Methods_("Create");

 #Spawn an instance of inParameters and assign the values.
 $inParam = $objMethod->inParameters->SpawnInstance_ if (defined $objMethod);
 $inParam->{CommandLine} = "notepad.exe";
 $inParam->{CurrentDirectory} = undef;
 $inParam->{ProcessStartupInformation} = undef;

 $outParam = $process->ExecMethod_("Create", $inParam) if (defined $inParam);
 if ($outParam->{ReturnValue})
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
 else
 {
  print "Method returned result = $outParam->{ReturnValue}\n";
  print "Id of new process is $outParam->{ProcessId}\n"
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="b8b4d-145">下列 VBScript 程式碼範例會在本機電腦上建立「記事本」處理常式。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-145">The following VBScript code example creates a Notepad process on the local computer.</span></span> <span data-ttu-id="b8b4d-146">[**Win32 \_ProcessStartup**](win32-processstartup.md) 用來設定處理常式設定。</span><span class="sxs-lookup"><span data-stu-id="b8b4d-146">[**Win32\_ProcessStartup**](win32-processstartup.md) is used to configure the process settings.</span></span>


```VB
Const SW_NORMAL = 1
strComputer = "."
strCommand = "Notepad.exe" 
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" _
    & strComputer & "\root\cimv2")

' Configure the Notepad process to show a window
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = SW_NORMAL

' Create Notepad process
Set objProcess = objWMIService.Get("Win32_Process")
intReturn = objProcess.Create _
    (strCommand, Null, objConfig, intProcessID)
If intReturn <> 0 Then
    Wscript.Echo "Process could not be created." & _
        vbNewLine & "Command line: " & strCommand & _
        vbNewLine & "Return value: " & intReturn
Else
    Wscript.Echo "Process created." & _
        vbNewLine & "Command line: " & strCommand & _
        vbNewLine & "Process ID: " & intProcessID
End If
```



## <a name="requirements"></a><span data-ttu-id="b8b4d-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8b4d-147">Requirements</span></span>



| <span data-ttu-id="b8b4d-148">需求</span><span class="sxs-lookup"><span data-stu-id="b8b4d-148">Requirement</span></span> | <span data-ttu-id="b8b4d-149">值</span><span class="sxs-lookup"><span data-stu-id="b8b4d-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8b4d-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8b4d-150">Minimum supported client</span></span><br/> | <span data-ttu-id="b8b4d-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8b4d-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b8b4d-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8b4d-152">Minimum supported server</span></span><br/> | <span data-ttu-id="b8b4d-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8b4d-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b8b4d-154">命名空間</span><span class="sxs-lookup"><span data-stu-id="b8b4d-154">Namespace</span></span><br/>                | <span data-ttu-id="b8b4d-155">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b8b4d-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b8b4d-156">MOF</span><span class="sxs-lookup"><span data-stu-id="b8b4d-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8b4d-157"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8b4d-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8b4d-158">DLL</span><span class="sxs-lookup"><span data-stu-id="b8b4d-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8b4d-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8b4d-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8b4d-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8b4d-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="b8b4d-161">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b8b4d-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b8b4d-162">**Win32 \_ 進程**</span><span class="sxs-lookup"><span data-stu-id="b8b4d-162">**Win32\_Process**</span></span>](win32-process.md)
</dt> <dt>

[<span data-ttu-id="b8b4d-163">WMI 工作：進程</span><span class="sxs-lookup"><span data-stu-id="b8b4d-163">WMI Tasks: Processes</span></span>](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 

