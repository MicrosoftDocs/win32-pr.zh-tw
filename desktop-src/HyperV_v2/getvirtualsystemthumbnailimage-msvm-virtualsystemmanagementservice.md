---
description: 抓取現有虛擬機器的縮圖影像。
ms.assetid: 8D670D2E-EAD7-47FF-B13C-764EFFDF4547
title: Msvm_VirtualSystemManagementService 類別的 GetVirtualSystemThumbnailImage 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetVirtualSystemThumbnailImage
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2c8288d2acee5816c4546b968a9a26c083cbbc88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980791"
---
# <a name="getvirtualsystemthumbnailimage-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="5cc31-103">Msvm VirtualSystemManagementService 類別的 GetVirtualSystemThumbnailImage 方法 \_</span><span class="sxs-lookup"><span data-stu-id="5cc31-103">GetVirtualSystemThumbnailImage method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="5cc31-104">抓取現有虛擬機器的縮圖影像。</span><span class="sxs-lookup"><span data-stu-id="5cc31-104">Retrieves the thumbnail image of an existing virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cc31-105">語法</span><span class="sxs-lookup"><span data-stu-id="5cc31-105">Syntax</span></span>


```mof
uint32 GetVirtualSystemThumbnailImage(
  [in]  CIM_VirtualSystemSettingData REF TargetSystem,
  [in]  uint16                           WidthPixels,
  [in]  uint16                           HeightPixels,
  [out] uint8                            ImageData[]
);
```



## <a name="parameters"></a><span data-ttu-id="5cc31-106">參數</span><span class="sxs-lookup"><span data-stu-id="5cc31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cc31-107">*TargetSystem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5cc31-107">*TargetSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cc31-108">類型： **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="5cc31-108">Type: **CIM\_VirtualSystemSettingData**</span></span>

<span data-ttu-id="5cc31-109">要抓取其縮圖影像之 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) 實例的參考。</span><span class="sxs-lookup"><span data-stu-id="5cc31-109">A reference to the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance whose thumbnail image is to be retrieved.</span></span> <span data-ttu-id="5cc31-110">此實例可能代表虛擬機器的目前具現化，或虛擬機器快照集的實例。</span><span class="sxs-lookup"><span data-stu-id="5cc31-110">This instance may represent either the current instantiation of the virtual machine, or an instance of a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="5cc31-111">*WidthPixels* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5cc31-111">*WidthPixels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cc31-112">類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5cc31-112">Type: **uint16**</span></span>

<span data-ttu-id="5cc31-113">所需影像的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="5cc31-113">The width of the desired image, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="5cc31-114">*HeightPixels* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5cc31-114">*HeightPixels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cc31-115">類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5cc31-115">Type: **uint16**</span></span>

<span data-ttu-id="5cc31-116">所需影像的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="5cc31-116">The height of the desired image, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="5cc31-117">*ImageData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5cc31-117">*ImageData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5cc31-118">類型： **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="5cc31-118">Type: **uint8\[\]**</span></span>

<span data-ttu-id="5cc31-119">要求的影像資料，以 raw RGB 565 格式。</span><span class="sxs-lookup"><span data-stu-id="5cc31-119">The requested image data, in raw RGB 565 format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cc31-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="5cc31-120">Return value</span></span>

<span data-ttu-id="5cc31-121">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5cc31-121">Type: **uint32**</span></span>

<span data-ttu-id="5cc31-122">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5cc31-122">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="5cc31-123">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="5cc31-123">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5cc31-124">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="5cc31-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5cc31-125">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="5cc31-125">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="5cc31-126">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="5cc31-126">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="5cc31-127">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="5cc31-127">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="5cc31-128">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="5cc31-128">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="5cc31-129">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="5cc31-129">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="5cc31-130">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="5cc31-130">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="5cc31-131">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="5cc31-131">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="5cc31-132">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="5cc31-132">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="5cc31-133">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="5cc31-133">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="5cc31-134">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="5cc31-134">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="5cc31-135">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="5cc31-135">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="5cc31-136">備註</span><span class="sxs-lookup"><span data-stu-id="5cc31-136">Remarks</span></span>

<span data-ttu-id="5cc31-137">存取 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="5cc31-137">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="5cc31-138">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="5cc31-138">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="5cc31-139">範例</span><span class="sxs-lookup"><span data-stu-id="5cc31-139">Examples</span></span>

<span data-ttu-id="5cc31-140">下列 c # 範例會抓取虛擬機器的縮圖影像。</span><span class="sxs-lookup"><span data-stu-id="5cc31-140">The following C# sample retrieves the thumbnail image of a virtual machine.</span></span> <span data-ttu-id="5cc31-141">您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。</span><span class="sxs-lookup"><span data-stu-id="5cc31-141">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5cc31-142">若要正常運作，必須在虛擬機器主機伺服器上執行下列程式碼，且必須以系統管理員許可權執行。</span><span class="sxs-lookup"><span data-stu-id="5cc31-142">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
static void SaveImageData(byte[] imageData)
{
    FileStream fs = new FileStream(@"c:\test.bin", FileMode.Create, FileAccess.Write);
    fs.Write(imageData, 0, imageData.Length);
    fs.Flush();
    fs.Close();
}

public static void GetVirtualSystemThumbnailImage(string vmName)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");

    ManagementObject vm = Utility.GetTargetComputer(vmName, scope);

    ManagementObjectCollection vmsettingDatas = vm.GetRelated(
        "Msvm_VirtualSystemsettingData",
        "Msvm_SettingsDefineState",
        null,
        null,
        "SettingData",
        "ManagedElement",
        false,
        null);

    ManagementObject settingData = null;

    foreach (ManagementObject data in vmsettingDatas)
    {
        settingData = data;
        break;
    }


    ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("GetVirtualSystemThumbnailImage");
    inParams["HeightPixels"] = 16;
    inParams["WidthPixels"] = 16;
    inParams["TargetSystem"] = settingData.Path.Path;


    ManagementBaseObject outParams = virtualSystemService.InvokeMethod("GetVirtualSystemThumbnailImage", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            SaveImageData((byte[])outParams["ImageData"]);
            Console.WriteLine("VM '{0}' thumbnail were retrieved successfully.", vm["ElementName"]);
        }
        else
        {
            Console.WriteLine("Failed to retrieve VM thumbnail");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        SaveImageData((byte[])outParams["ImageData"]);
        Console.WriteLine("VM '{0}' thumbnail were retrieved successfully.", vm["ElementName"]);
    }
    else
    {
        Console.WriteLine("Failed to retrieve VM thumbnail with error {0}", (UInt32)outParams["ReturnValue"]);
    }

    inParams.Dispose();
    outParams.Dispose();
    settingData.Dispose();
    vm.Dispose();
    virtualSystemService.Dispose();
}
```



<span data-ttu-id="5cc31-143">下列 Visual Basic Scripting Edition (VBScript) 範例會抓取虛擬機器的縮圖影像。</span><span class="sxs-lookup"><span data-stu-id="5cc31-143">The following Visual Basic Scripting Edition (VBScript) sample retrieves the thumbnail image of a virtual machine.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5cc31-144">若要正常運作，必須在虛擬機器主機伺服器上執行下列程式碼，且必須以系統管理員許可權執行。</span><span class="sxs-lookup"><span data-stu-id="5cc31-144">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```VB
option explicit 

dim objWMIService
dim managementService
dim fileSystem

const wmiStarted = 4096
const wmiSuccessful = 0

Main()


'-----------------------------------------------------------------
' Main
'-----------------------------------------------------------------
Sub Main()

    dim computer, objArgs, vmName, vm
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")
    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")
    set managementService = objWMIService.ExecQuery("select * from Msvm_VirtualSystemManagementService").ItemIndex(0)
    
    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 1 then
        vmName = objArgs.Unnamed.Item(0)
    else
        WScript.Echo "usage: cscript GetVirtualSystemThumbnailImage.vbs vmName"
        WScript.Quit(1)
    end if
    
    set vm = GetComputerSystem(vmName)
    
    if StartVm(vm) then
        if GetVirtualSystemThumbnailImage(vm) then
            WriteLog "Done"
            WScript.Quit(0)
         End if
    end if
    
    WriteLog "GetVirtualSystemThumbnailImage Failed."
    WScript.Quit(1)
    
End Sub

'-----------------------------------------------------------------
' Retrieve Msvm_VirtualComputerSystem from base on its ElementName
'-----------------------------------------------------------------
Function GetComputerSystem(vmElementName)
    On Error Resume Next
    dim query
    query = Format1("select * from Msvm_ComputerSystem where ElementName = '{0}'", vmElementName)
    set GetComputerSystem = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function

'-----------------------------------------------------------------
' Save the thumbnail
'-----------------------------------------------------------------
Sub SaveThumbnailImage(thumbnailBytes)

    dim stream 
    Const adTypeText = 2
    Const adSaveCreateOverWrite = 2  
    
    set stream = CreateObject("ADODB.Stream")
    stream.Type = adTypeText
  
    stream.Open
    Redim text(ubound(thumbnailBytes) \ 2)
    for i = lbound(thumbnailBytes) to ubound(thumbnailBytes) step 2
        text(i\2) = ChrW(thumbnailBytes(i + 1) * &HFF + thumbnailBytes(i))
    next
    stream.WriteText text
  
    stream.SaveToFile ".\thumbnail.bin", adSaveCreateOverWrite
    stream.Close
    
  
End Sub

'-----------------------------------------------------------------
' Start the virtual machine 
'-----------------------------------------------------------------
Function StartVm(computerSystem)
    
    dim objInParam, objOutParams
    StartVm = false
    if computerSystem.OperationalStatus(0) = 2 then
        StartVm = true
        Exit Function
    end if
    
    set objInParam = computerSystem.Methods_("RequestStateChange").InParameters.SpawnInstance_()
    objInParam.RequestedState = 2
    set objOutParams = computerSystem.ExecMethod_("RequestStateChange", objInParam)
    
    if objOutParams.ReturnValue = wmiStarted then
        if (WMIJobCompleted(objOutParams)) then
            StartVm = true
        end if
    elseif objOutParams.ReturnValue = wmiSuccessful then
        StartVm = true
    else
        WriteLog Format1("StartVM failed with ReturnValue {0}", wmiStatus)
    end if
    
End Function


'-----------------------------------------------------------------
' Print the thumbnail data
'-----------------------------------------------------------------
Sub PrintThumbnailImage(thumbnailBytes)
    dim index
    for index = lbound(thumbnailBytes) to ubound(thumbnailBytes)
        WriteLog Format2("{0}:{1} ", index, thumbnailBytes(i))
    next
End Sub
'-----------------------------------------------------------------
' Define a virtual system
'-----------------------------------------------------------------
Function GetVirtualSystemThumbnailImage(computerSystem)
    dim query, objInParam, objOutParams, virtualSystemsetting
    
    GetVirtualSystemThumbnailImage = false
    
    query = Format1("ASSOCIATORS OF {{0}} WHERE resultClass = Msvm_VirtualSystemsettingData", computerSystem.Path_.Path)
    set virtualSystemsetting = objWMIService.ExecQuery(query).ItemIndex(0)
    
    set objInParam = managementService.Methods_("GetVirtualSystemThumbnailImage").InParameters.SpawnInstance_()

    objInParam.HeightPixels = 16
    objInParam.WidthPixels = 16
    objInParam.TargetSystem = virtualSystemsetting.Path_.Path
    
    set objOutParams = managementService.ExecMethod_("GetVirtualSystemThumbnailImage", objInParam)
    
    if objOutParams.ReturnValue = wmiStarted then
        if (WMIJobCompleted(objOutParams)) then
            GetVirtualSystemThumbnailImage = true
        end if
    elseif objOutParams.ReturnValue = wmiSuccessful then
        GetVirtualSystemThumbnailImage = true
    else
        WriteLog Format1("GetVirtualSystemThumbnailImage failed with ReturnValue {0}", wmiStatus)
    end if

End Function


'-----------------------------------------------------------------
' Handle wmi Job object
'-----------------------------------------------------------------
Function WMIJobCompleted(outParam)
    
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
    set fileStream = fileSystem.OpenTextFile(".\GetVirtualSystemThumbnailImage.log", 8, true)
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



## <a name="requirements"></a><span data-ttu-id="5cc31-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="5cc31-145">Requirements</span></span>



| <span data-ttu-id="5cc31-146">需求</span><span class="sxs-lookup"><span data-stu-id="5cc31-146">Requirement</span></span> | <span data-ttu-id="5cc31-147">值</span><span class="sxs-lookup"><span data-stu-id="5cc31-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cc31-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5cc31-148">Minimum supported client</span></span><br/> | <span data-ttu-id="5cc31-149">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5cc31-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5cc31-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5cc31-150">Minimum supported server</span></span><br/> | <span data-ttu-id="5cc31-151">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5cc31-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5cc31-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="5cc31-152">Namespace</span></span><br/>                | <span data-ttu-id="5cc31-153">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="5cc31-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5cc31-154">MOF</span><span class="sxs-lookup"><span data-stu-id="5cc31-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5cc31-155"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="5cc31-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5cc31-156">DLL</span><span class="sxs-lookup"><span data-stu-id="5cc31-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5cc31-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5cc31-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5cc31-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5cc31-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cc31-159">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="5cc31-159">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

