---
description: 將機碼/值組加入至虛擬機器。
ms.assetid: D952EC3D-24EB-4A68-8527-5BF522957CB6
title: Msvm_VirtualSystemManagementService 類別的 AddKvpItems 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddKvpItems
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e9e01a02615b8bb395a589160a765dec4e08526e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969372"
---
# <a name="addkvpitems-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="f22f8-103">Msvm VirtualSystemManagementService 類別的 AddKvpItems 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f22f8-103">AddKvpItems method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="f22f8-104">將機碼/值組加入至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f22f8-104">Adds key-value pairs to a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="f22f8-105">語法</span><span class="sxs-lookup"><span data-stu-id="f22f8-105">Syntax</span></span>


```mof
uint32 AddKvpItems(
  [in]  CIM_ComputerSystem REF TargetSystem,
  [in]  string                 DataItems[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f22f8-106">參數</span><span class="sxs-lookup"><span data-stu-id="f22f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f22f8-107">*TargetSystem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f22f8-107">*TargetSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f22f8-108">類型： **[ **CIM \_** 操作一](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span><span class="sxs-lookup"><span data-stu-id="f22f8-108">Type: **[**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span></span>

<span data-ttu-id="f22f8-109">CIM 系統元件物件 [**\_**](/windows/desktop/CIMWin32Prov/cim-computersystem) 的參考，此物件代表將在其上新增索引鍵/值組的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f22f8-109">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object that represents the virtual machine on which the key-value pairs will be added.</span></span>

</dd> <dt>

<span data-ttu-id="f22f8-110">*Dataitem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f22f8-110">*DataItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f22f8-111">類型：**字串 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="f22f8-111">Type: **string\[\]**</span></span>

<span data-ttu-id="f22f8-112">要加入之索引鍵/值組的陣列。</span><span class="sxs-lookup"><span data-stu-id="f22f8-112">An array of key-value pairs to be added.</span></span> <span data-ttu-id="f22f8-113">陣列的每個元素都是 [**Msvm \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) 類別的內嵌實例。</span><span class="sxs-lookup"><span data-stu-id="f22f8-113">Each element of the array is an embedded instance of the [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) class.</span></span> <span data-ttu-id="f22f8-114">如果目標系統上已經有任何指定的索引鍵/值組，則這個方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="f22f8-114">This method fails if any of the specified key-value pairs already exists on the target system.</span></span> <span data-ttu-id="f22f8-115">這個陣列最多可包含128個元素。</span><span class="sxs-lookup"><span data-stu-id="f22f8-115">This array can contain at most 128 elements.</span></span>

</dd> <dt>

<span data-ttu-id="f22f8-116">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f22f8-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f22f8-117">類型： **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="f22f8-117">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="f22f8-118">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="f22f8-118">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f22f8-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="f22f8-119">Return value</span></span>

<span data-ttu-id="f22f8-120">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f22f8-120">Type: **uint32**</span></span>

<span data-ttu-id="f22f8-121">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f22f8-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f22f8-122">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="f22f8-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f22f8-123">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="f22f8-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f22f8-124">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="f22f8-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f22f8-125">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="f22f8-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f22f8-126">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="f22f8-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f22f8-127">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="f22f8-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f22f8-128">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="f22f8-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f22f8-129">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="f22f8-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f22f8-130">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="f22f8-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f22f8-131">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="f22f8-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f22f8-132">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="f22f8-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f22f8-133">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="f22f8-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f22f8-134">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="f22f8-134">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="f22f8-135">備註</span><span class="sxs-lookup"><span data-stu-id="f22f8-135">Remarks</span></span>

<span data-ttu-id="f22f8-136">存取 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="f22f8-136">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f22f8-137">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="f22f8-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="f22f8-138">範例</span><span class="sxs-lookup"><span data-stu-id="f22f8-138">Examples</span></span>

<span data-ttu-id="f22f8-139">下列 c # 範例會將索引鍵/值組加入至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f22f8-139">The following C# sample adds key-value pairs to a virtual machine.</span></span> <span data-ttu-id="f22f8-140">您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。</span><span class="sxs-lookup"><span data-stu-id="f22f8-140">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f22f8-141">若要正常運作，必須在虛擬機器主機伺服器上執行下列程式碼，且必須以系統管理員許可權執行。</span><span class="sxs-lookup"><span data-stu-id="f22f8-141">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
public static void AddKvpItems(string vmName, string itemName, string itemValue)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
    ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("AddKvpItems");
    ManagementClass kvpExchangeDataItem = new ManagementClass(scope, new ManagementPath("Msvm_KvpExchangeDataItem"), null);

    ManagementObject dataItem = kvpExchangeDataItem.CreateInstance();

    dataItem["Data"] = itemValue;
    dataItem["Name"] = itemName;
    dataItem["Source"] = 0;

    string[] dataItems = new string[1];
    dataItems[0] = dataItem.GetText(TextFormat.CimDtd20);

    ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
    inParams["TargetSystem"] = vm.Path.Path;
    inParams["DataItems"] = dataItems;

    ManagementBaseObject outParams = virtualSystemService.InvokeMethod("AddKvpItems", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("Resources were added successfully.");

        }
        else
        {
            Console.WriteLine("Failed to add resources");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        Console.WriteLine("Resources were added successfully.");
    }
    else
    {
        Console.WriteLine("Add virtual system Kvp items failed with error {0}", outParams["ReturnValue"]);
    }

    if (inParams != null)
    {
        inParams.Dispose();
    }

    if (outParams != null)
    {
        outParams.Dispose();
    }
}
```



<span data-ttu-id="f22f8-142">下列 Visual Basic Scripting Edition (VBScript) 範例會將機碼值組加入至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f22f8-142">The following Visual Basic Scripting Edition (VBScript) sample adds key-value pairs to a virtual machine.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f22f8-143">若要正常運作，必須在虛擬機器主機伺服器上執行下列程式碼，且必須以系統管理員許可權執行。</span><span class="sxs-lookup"><span data-stu-id="f22f8-143">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```VB
option explicit 

dim objWMIService
dim managementService
dim fileSystem


const JobStarting = 3
const JobRunning = 4
const JobCompleted = 7
const wmiStarted = 4096
const wmiSuccessful = 0

Main()

'-----------------------------------------------------------------
' Main
'-----------------------------------------------------------------
Sub Main()

    dim computer, vmName, itemName, itemValue, myVm, objArgs
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."

    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")
    set managementService = objWMIService.ExecQuery("select * from Msvm_VirtualSystemManagementService").ItemIndex(0)

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 3 then
        vmName = objArgs.Unnamed.Item(0)
        itemName = objArgs.Unnamed.Item(1)
        itemValue = objArgs.Unnamed.Item(2)
    else
        WScript.Echo "usage: cscript AddKvpItems.vbs vmName itemName itemValue"
        WScript.Quit(1)
    end if

    set myVm = GetComputerSystem(vmName)

    if AddKvpItems(myVm, itemName, itemValue) then

        WriteLog "Done"
        WScript.Quit(0)

    else
        WriteLog "AddKvpItems failed"
        WScript.Quit(1)
    end if

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
' AddKvpItems
'-----------------------------------------------------------------
Function AddKvpItems(computerSystem, itemName, itemValue)

    dim dataItem, dataItems, objInParam, objOutParams
    
    AddKvpItems = false
    
    set dataItem = objWMIService.Get("Msvm_KvpExchangeDataItem").SpawnInstance_()
    dataItem.Data = itemValue
    dataItem.Name = itemName
    dataItem.Source = 0
    
    dataItems = Array(1)
    dataItems(0) = dataItem.GetText_(1)
    
    set objInParam = managementService.Methods_("AddKvpItems").InParameters.SpawnInstance_()
    objInParam.TargetSystem = computerSystem.Path_.Path
    objInParam.DataItems = dataItems
    
    set objOutParams = managementService.ExecMethod_("AddKvpItems", objInParam)

    if objOutParams.ReturnValue = wmiStarted then
        if (WMIJobCompleted(objOutParams)) then
            AddKvpItems = true
        end if
    elseif (objOutParams.ReturnValue = wmiSuccessful) then
        AddKvpItems = true
    else
        WriteLog Format1("AddKvpItem failed with error {0}", objOutParams.ReturnValue)
    end if

End Function


'-----------------------------------------------------------------
' Handle wmi Job object
'-----------------------------------------------------------------
Function WMIJobCompleted(outParam)
    
    dim WMIJob, jobState
    WMIJobCompleted = true

    set WMIJob = objWMIService.Get(outParam.Job)
    
    jobState = WMIJob.JobState

    while jobState = JobRunning or jobState = JobStarting
        WriteLog Format1("In progress... {0}% completed.",WMIJob.PercentComplete)
        WScript.Sleep(1000)
        set WMIJob = objWMIService.Get(outParam.Job)
        jobState = WMIJob.JobState
    wend

    if (WMIJob.JobState <> JobCompleted) then
        WriteLog Format1("ErrorDescription:{0}", WMIJob.ErrorDescription)
        WriteLog Format1("ErrorCode:{0}", WMIJob.ErrorCode)
        WMIJobCompleted = false
    end if
    
End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\AddKvpItems.log", 8, true)
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



## <a name="requirements"></a><span data-ttu-id="f22f8-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="f22f8-144">Requirements</span></span>



| <span data-ttu-id="f22f8-145">需求</span><span class="sxs-lookup"><span data-stu-id="f22f8-145">Requirement</span></span> | <span data-ttu-id="f22f8-146">值</span><span class="sxs-lookup"><span data-stu-id="f22f8-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f22f8-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f22f8-147">Minimum supported client</span></span><br/> | <span data-ttu-id="f22f8-148">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f22f8-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f22f8-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f22f8-149">Minimum supported server</span></span><br/> | <span data-ttu-id="f22f8-150">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f22f8-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f22f8-151">命名空間</span><span class="sxs-lookup"><span data-stu-id="f22f8-151">Namespace</span></span><br/>                | <span data-ttu-id="f22f8-152">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="f22f8-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f22f8-153">MOF</span><span class="sxs-lookup"><span data-stu-id="f22f8-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f22f8-154"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="f22f8-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f22f8-155">DLL</span><span class="sxs-lookup"><span data-stu-id="f22f8-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f22f8-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f22f8-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f22f8-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f22f8-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f22f8-158">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="f22f8-158">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

