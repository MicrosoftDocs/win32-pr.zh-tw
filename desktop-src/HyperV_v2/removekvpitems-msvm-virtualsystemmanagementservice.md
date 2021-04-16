---
description: 從虛擬機器移除現有的機碼值組。
ms.assetid: B2ECF609-89BB-4117-982B-EF56D51E1321
title: Msvm_VirtualSystemManagementService 類別的 RemoveKvpItems 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveKvpItems
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4921805ade9538a4e05a15331f707b9356411aa7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514060"
---
# <a name="removekvpitems-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="4d03f-103">Msvm VirtualSystemManagementService 類別的 RemoveKvpItems 方法 \_</span><span class="sxs-lookup"><span data-stu-id="4d03f-103">RemoveKvpItems method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="4d03f-104">從虛擬機器移除現有的機碼值組。</span><span class="sxs-lookup"><span data-stu-id="4d03f-104">Removes existing key-value pairs from a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d03f-105">語法</span><span class="sxs-lookup"><span data-stu-id="4d03f-105">Syntax</span></span>


```mof
uint32 RemoveKvpItems(
  [in]  CIM_ComputerSystem REF TargetSystem,
  [in]  string                 DataItems[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="4d03f-106">參數</span><span class="sxs-lookup"><span data-stu-id="4d03f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d03f-107">*TargetSystem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d03f-107">*TargetSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d03f-108">類型： **[ **CIM \_** 操作一](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span><span class="sxs-lookup"><span data-stu-id="4d03f-108">Type: **[**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span></span>

<span data-ttu-id="4d03f-109">將移除索引鍵/值組之虛擬機器的參考。</span><span class="sxs-lookup"><span data-stu-id="4d03f-109">A reference to the virtual machine on which the key-value pairs will be removed.</span></span>

</dd> <dt>

<span data-ttu-id="4d03f-110">*Dataitem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d03f-110">*DataItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d03f-111">類型：**字串 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="4d03f-111">Type: **string\[\]**</span></span>

<span data-ttu-id="4d03f-112">要移除的索引鍵/值組陣列 (只需要符合) 的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="4d03f-112">An array of key-value pairs to be removed (only the keys need to match).</span></span> <span data-ttu-id="4d03f-113">陣列的每個元素都是 [**Msvm \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) 類別的內嵌實例。</span><span class="sxs-lookup"><span data-stu-id="4d03f-113">Each element of the array is an embedded instance of the [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) class.</span></span> <span data-ttu-id="4d03f-114">如果任何指定的索引鍵/值組不存在於目標系統上，則這個方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="4d03f-114">This method fails if any of the specified key-value pairs does not exist on the target system.</span></span> <span data-ttu-id="4d03f-115">這個陣列最多可包含128個元素。</span><span class="sxs-lookup"><span data-stu-id="4d03f-115">This array can contain at most 128 elements.</span></span>

</dd> <dt>

<span data-ttu-id="4d03f-116">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4d03f-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d03f-117">類型： **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="4d03f-117">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="4d03f-118">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="4d03f-118">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d03f-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d03f-119">Return value</span></span>

<span data-ttu-id="4d03f-120">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4d03f-120">Type: **uint32**</span></span>

<span data-ttu-id="4d03f-121">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4d03f-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="4d03f-122">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="4d03f-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4d03f-123">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="4d03f-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4d03f-124">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="4d03f-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="4d03f-125">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="4d03f-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="4d03f-126">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="4d03f-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="4d03f-127">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="4d03f-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="4d03f-128">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="4d03f-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="4d03f-129">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="4d03f-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="4d03f-130">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="4d03f-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="4d03f-131">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="4d03f-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="4d03f-132">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="4d03f-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="4d03f-133">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="4d03f-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="4d03f-134">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="4d03f-134">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="4d03f-135">備註</span><span class="sxs-lookup"><span data-stu-id="4d03f-135">Remarks</span></span>

<span data-ttu-id="4d03f-136">存取 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="4d03f-136">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4d03f-137">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="4d03f-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="4d03f-138">範例</span><span class="sxs-lookup"><span data-stu-id="4d03f-138">Examples</span></span>

<span data-ttu-id="4d03f-139">下列 c # 範例會從虛擬機器移除機碼值組。</span><span class="sxs-lookup"><span data-stu-id="4d03f-139">The following C# sample removes key-value pairs from a virtual machine.</span></span> <span data-ttu-id="4d03f-140">您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。</span><span class="sxs-lookup"><span data-stu-id="4d03f-140">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4d03f-141">若要正常運作，必須在虛擬機器主機伺服器上執行下列程式碼，且必須以系統管理員許可權執行。</span><span class="sxs-lookup"><span data-stu-id="4d03f-141">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
public static void RemoveKvpItems(string vmName, string itemName)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
    ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("RemoveKvpItems");
    ManagementClass kvpExchangeDataItem = new ManagementClass(scope, new ManagementPath("Msvm_KvpExchangeDataItem"), null);

    ManagementObject dataItem = kvpExchangeDataItem.CreateInstance();

    dataItem["Data"] = "";
    dataItem["Name"] = itemName;
    dataItem["Source"] = 0;

    string[] dataItems = new string[1];
    dataItems[0] = dataItem.GetText(TextFormat.CimDtd20);

    ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
    inParams["TargetSystem"] = vm.Path.Path;
    inParams["DataItems"] = dataItems;

    ManagementBaseObject outParams = virtualSystemService.InvokeMethod("RemoveKvpItems", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("KvpItems were removed successfully.");

        }
        else
        {
            Console.WriteLine("Failed to remove KvpItems");
        }
    } 
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        Console.WriteLine("KvpItems were removed successfully.");
    }
    else
    {
        Console.WriteLine("Remove KvpItems failed with error {0}", outParams["ReturnValue"]);
    }

    inParams.Dispose();
    outParams.Dispose();
    dataItem.Dispose();
    vm.Dispose();
    virtualSystemService.Dispose();
    
}
```



<span data-ttu-id="4d03f-142">下列 Visual Basic Scripting Edition (VBScript) 範例會從虛擬機器移除機碼值組。</span><span class="sxs-lookup"><span data-stu-id="4d03f-142">The following Visual Basic Scripting Edition (VBScript) sample removes key-value pairs from a virtual machine.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4d03f-143">若要正常運作，必須在虛擬機器主機伺服器上執行下列程式碼，且必須以系統管理員許可權執行。</span><span class="sxs-lookup"><span data-stu-id="4d03f-143">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


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

    dim computer, vmName, itemName, myVm, objArgs
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."

    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")
    set managementService = objWMIService.ExecQuery("select * from Msvm_VirtualSystemManagementService").ItemIndex(0)

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 3 then
        vmName = objArgs.Unnamed.Item(0)
        itemName = objArgs.Unnamed.Item(1)
    else
        WScript.Echo "usage: cscript AddKvpItems.vbs vmName itemName"
        WScript.Quit(1)
    end if

    set myVm = GetComputerSystem(vmName)

    if RemoveKvpItems(myVm, itemName) then

        WriteLog "Done"
        WScript.Quit(0)

    else
        WriteLog "RemoveKvpItems failed"
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
' RemoveKvpItems
'-----------------------------------------------------------------
Function RemoveKvpItems(computerSystem, itemName)

    dim dataItem, dataItems, objInParam, objOutParams
    
    RemoveKvpItems = false
    
    set dataItem = objWMIService.Get("Msvm_KvpExchangeDataItem").SpawnInstance_()
    dataItem.Data = ""
    dataItem.Name = itemName
    dataItem.Source = 0
    
    dataItems = Array(1)
    dataItems(0) = dataItem.GetText_(1)
    
    set objInParam = managementService.Methods_("RemoveKvpItems").InParameters.SpawnInstance_()
    objInParam.TargetSystem = computerSystem.Path_.Path
    objInParam.dataItems = dataItems
    
    set objOutParams = managementService.ExecMethod_("RemoveKvpItems", objInParam)

    if objOutParams.ReturnValue = wmiStarted then
        if (WMIJobCompleted(objOutParams)) then
            RemoveKvpItems = true
        end if
    elseif objOutParams.ReturnValue = wmiSuccessful then
        RemoveKvpItems = true
    else
        WriteLog Format1("RemoveKvpItems failed with {0}", objOutParams.ReturnValue )
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
    set fileStream = fileSystem.OpenTextFile(".\RemoveKvpItems.log", 8, true)
    WScript.Echo line
    fileStream.WriteLine line
    fileStream.Close

End Sub

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format1(myString, arg0)
    Format1 = Replace(myString, "{0}", arg0)
End Function
```



## <a name="requirements"></a><span data-ttu-id="4d03f-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d03f-144">Requirements</span></span>



| <span data-ttu-id="4d03f-145">需求</span><span class="sxs-lookup"><span data-stu-id="4d03f-145">Requirement</span></span> | <span data-ttu-id="4d03f-146">值</span><span class="sxs-lookup"><span data-stu-id="4d03f-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d03f-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d03f-147">Minimum supported client</span></span><br/> | <span data-ttu-id="4d03f-148">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d03f-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4d03f-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d03f-149">Minimum supported server</span></span><br/> | <span data-ttu-id="4d03f-150">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d03f-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4d03f-151">命名空間</span><span class="sxs-lookup"><span data-stu-id="4d03f-151">Namespace</span></span><br/>                | <span data-ttu-id="4d03f-152">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="4d03f-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4d03f-153">MOF</span><span class="sxs-lookup"><span data-stu-id="4d03f-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d03f-154"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="4d03f-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d03f-155">DLL</span><span class="sxs-lookup"><span data-stu-id="4d03f-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d03f-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4d03f-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4d03f-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d03f-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d03f-158">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="4d03f-158">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

