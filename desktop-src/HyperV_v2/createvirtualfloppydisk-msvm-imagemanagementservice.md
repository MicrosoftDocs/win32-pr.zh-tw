---
description: 建立虛擬磁片檔案。
ms.assetid: C7B5712C-55DD-4784-8B2E-A8DE02E4CFD8
title: Msvm_ImageManagementService 類別的 CreateVirtualFloppyDisk 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.CreateVirtualFloppyDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 98781a4f72218ee61a4966dc76b21f7417353e0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980446"
---
# <a name="createvirtualfloppydisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="4caf6-103">Msvm ImageManagementService 類別的 CreateVirtualFloppyDisk 方法 \_</span><span class="sxs-lookup"><span data-stu-id="4caf6-103">CreateVirtualFloppyDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="4caf6-104">建立虛擬磁片檔案。</span><span class="sxs-lookup"><span data-stu-id="4caf6-104">Creates a virtual floppy disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="4caf6-105">語法</span><span class="sxs-lookup"><span data-stu-id="4caf6-105">Syntax</span></span>


```mof
uint32 CreateVirtualFloppyDisk(
  [in]  string              Path,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="4caf6-106">參數</span><span class="sxs-lookup"><span data-stu-id="4caf6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4caf6-107">*路徑* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4caf6-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4caf6-108">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4caf6-108">Type: **string**</span></span>

<span data-ttu-id="4caf6-109">指定新檔案位置的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="4caf6-109">A fully qualified path that specifies the location of the new file.</span></span>

</dd> <dt>

<span data-ttu-id="4caf6-110">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4caf6-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4caf6-111">類型： **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="4caf6-111">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="4caf6-112">如果工作已完成) ，則作業 (的參考可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="4caf6-112">A reference to the job (can be **Null** if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4caf6-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4caf6-113">Return value</span></span>

<span data-ttu-id="4caf6-114">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4caf6-114">Type: **uint32**</span></span>

<span data-ttu-id="4caf6-115">這個方法可能會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4caf6-115">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="4caf6-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="4caf6-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4caf6-117">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="4caf6-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4caf6-118">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="4caf6-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="4caf6-119">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="4caf6-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="4caf6-120">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="4caf6-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="4caf6-121">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="4caf6-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="4caf6-122">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="4caf6-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="4caf6-123">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="4caf6-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="4caf6-124">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="4caf6-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="4caf6-125">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="4caf6-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="4caf6-126">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="4caf6-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="4caf6-127">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="4caf6-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="4caf6-128">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="4caf6-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="4caf6-129">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="4caf6-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="4caf6-130">備註</span><span class="sxs-lookup"><span data-stu-id="4caf6-130">Remarks</span></span>

<span data-ttu-id="4caf6-131">存取 [**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="4caf6-131">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4caf6-132">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="4caf6-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="4caf6-133">範例</span><span class="sxs-lookup"><span data-stu-id="4caf6-133">Examples</span></span>

<span data-ttu-id="4caf6-134">下列 c # 範例會建立虛擬磁片檔案。</span><span class="sxs-lookup"><span data-stu-id="4caf6-134">The following C# example creates a virtual floppy disk file.</span></span> <span data-ttu-id="4caf6-135">您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。</span><span class="sxs-lookup"><span data-stu-id="4caf6-135">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class CreateVFD
    {
        static void CreateVirtualFlopy(string vhdPath)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

            ManagementBaseObject inParams = imageService.GetMethodParameters("CreateVirtualFloppyDisk");
            inParams["Path"] = vhdPath;
            ManagementBaseObject outParams = imageService.InvokeMethod("CreateVirtualFloppyDisk", inParams, null);
            if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
            {
                if (Utility.JobCompleted(outParams, scope))
                {
                    Console.WriteLine("{0} was created successfully.", inParams["Path"]);
                }
                else
                {
                    Console.WriteLine("Unable to create {0}", inParams["Path"]);
                }
            }

            inParams.Dispose();
            outParams.Dispose();
            imageService.Dispose();
        }

        static void Main(string[] args)
        {
            if (args != null && args.Length != 1)
            {
                Console.WriteLine("Usage: CreateVFD path");
                return;
            }
            CreateVirtualFlopy(args[0]);
        }
    }
}

```



<span data-ttu-id="4caf6-136">下列 Visual Basic Scripting Edition (VBScript) 範例會建立虛擬磁片檔案。</span><span class="sxs-lookup"><span data-stu-id="4caf6-136">The following Visual Basic Scripting Edition (VBScript) example creates a virtual floppy disk file.</span></span>


```VB
option explicit 

dim objWMIService
dim managementService
dim fileSystem


const JobStarting = 3
const JobRunning = 4
const JobCompleted = 7
const wmiStarted = 4096

const method = "CreateVirtualFloppyDisk"
Main()

'-----------------------------------------------------------------
' Main
'-----------------------------------------------------------------
Sub Main()

    dim computer, objArgs, vfdPath

    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")
    set managementService = objWMIService.ExecQuery("Select * from Msvm_ImageManagementService").ItemIndex(0)

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 1 then
       vfdPath = objArgs.Unnamed.Item(0)
    else
       WScript.Echo "usage: cscript CreateVFD.vbs VFDFilePath "
       WScript.Quit(1)
    end if

    if CreateVirtualFloppyDisk(vfdPath) then
        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "CreateVFD failed"
        WScript.Quit(1)
    end if

End Sub

'-----------------------------------------------------------------
' Execute CreateVirtualFloppyDisk method
'-----------------------------------------------------------------
Function CreateVirtualFloppyDisk(vfdPath)
    WriteLog Format1("Function CreateVirtualFloppyDisk({0})",  vfdPath)
    
    dim objInParam, objOutParams

    CreateVirtualFloppyDisk = false

    set objInParam = managementService.Methods_("CreateVirtualFloppyDisk").InParameters.SpawnInstance_()
    objInParam.Path = vfdPath

    set objOutParams = managementService.ExecMethod_("CreateVirtualFloppyDisk", objInParam)

    if (WMIMethodStarted(objOutParams)) then
        if (WMIJobCompleted(objOutParams)) then
            WriteLog Format1("VHD {0} was created successfully", vfdPath)
            CreateVirtualFloppyDisk = true
        end if
    end if

End Function


'-----------------------------------------------------------------
' Handle wmi return values
'-----------------------------------------------------------------
Function WMIMethodStarted(outParam)
    WriteLog "Function WMIMethodStarted"
    
    dim wmiStatus
    
    WMIMethodStarted = false

    if Not IsNull(outParam) then
        wmiStatus = outParam.ReturnValue

        if  wmiStatus = wmiStarted then
            WMIMethodStarted = true
        else
            WriteLog Format2("Failed to create VFD {0} ConcreteJob with error {1}", vfdPath, wmiStatus)
        end if
   end if

End Function

'-----------------------------------------------------------------
' Handle wmi Job object
'-----------------------------------------------------------------
Function WMIJobCompleted(outParam)
    WriteLog "Function WMIJobCompleted"
    dim WMIJob, jobState

    set WMIJob = objWMIService.Get(outParam.Job)

    WMIJobCompleted = true

    jobState = WMIJob.JobState

    while jobState = JobRunning or jobState = JobStarting
        WriteLog Format1("In progress... {0}% completed.",WMIJob.PercentComplete)
        WScript.Sleep(1000)
        set WMIJob = objWMIService.Get(outParam.Job)
        jobState = WMIJob.JobState
    wend

    if (jobState <> JobCompleted) then
        WriteLog Format1("ErrorCode:{0}", WMIJob.ErrorCode)
        WriteLog Format1("ErrorDescription:{0}", WMIJob.ErrorDescription)
        WMIJobCompleted = false
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\CreateVFD.log", 8, true)
    WScript.Echo line
    fileStream.WriteLine line
    fileStream.Close

End Sub

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format2(myString, arg0, arg1)
    Format2 = Format1(myString, arg0)
    Format2 = Replace(Format2, "{1}", arg1)
End Function

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format1(myString, arg0)
    Format1 = Replace(myString, "{0}", arg0)
End Function
```



## <a name="requirements"></a><span data-ttu-id="4caf6-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="4caf6-137">Requirements</span></span>



| <span data-ttu-id="4caf6-138">需求</span><span class="sxs-lookup"><span data-stu-id="4caf6-138">Requirement</span></span> | <span data-ttu-id="4caf6-139">值</span><span class="sxs-lookup"><span data-stu-id="4caf6-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4caf6-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4caf6-140">Minimum supported client</span></span><br/> | <span data-ttu-id="4caf6-141">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4caf6-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4caf6-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4caf6-142">Minimum supported server</span></span><br/> | <span data-ttu-id="4caf6-143">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4caf6-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4caf6-144">命名空間</span><span class="sxs-lookup"><span data-stu-id="4caf6-144">Namespace</span></span><br/>                | <span data-ttu-id="4caf6-145">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="4caf6-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4caf6-146">MOF</span><span class="sxs-lookup"><span data-stu-id="4caf6-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4caf6-147"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="4caf6-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4caf6-148">DLL</span><span class="sxs-lookup"><span data-stu-id="4caf6-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4caf6-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4caf6-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4caf6-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4caf6-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="4caf6-151">[**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4caf6-151">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4caf6-152">**Msvm \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="4caf6-152">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

