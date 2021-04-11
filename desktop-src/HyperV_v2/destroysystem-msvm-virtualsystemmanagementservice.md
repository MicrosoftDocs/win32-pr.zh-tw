---
description: 從主機系統的管理範圍移除先前定義的虛擬機器。
ms.assetid: 16E6EEB0-CB29-4FFC-AEFF-872E099337FA
title: Msvm_VirtualSystemManagementService 類別的 DestroySystem 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1caf4e4a590bdbfe2f7543e23d5ca00018300fb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850959"
---
# <a name="destroysystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="d89b0-103">Msvm VirtualSystemManagementService 類別的 DestroySystem 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d89b0-103">DestroySystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="d89b0-104">從主機系統的管理範圍移除先前定義的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="d89b0-104">Removes the previously defined virtual machine from the management scope of the host system.</span></span> <span data-ttu-id="d89b0-105">也會移除任何相關聯的資源定義。</span><span class="sxs-lookup"><span data-stu-id="d89b0-105">Any associated resource definitions will also be removed.</span></span> <span data-ttu-id="d89b0-106">在呼叫這個方法之前，虛擬機器必須處於 [已關閉電源] 或 [已儲存] 狀態。</span><span class="sxs-lookup"><span data-stu-id="d89b0-106">The virtual machine must be in the powered off or saved state prior to calling this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d89b0-107">語法</span><span class="sxs-lookup"><span data-stu-id="d89b0-107">Syntax</span></span>


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d89b0-108">參數</span><span class="sxs-lookup"><span data-stu-id="d89b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d89b0-109">*AffectedSystem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d89b0-109">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d89b0-110">類型： **CIM \_** 操作一</span><span class="sxs-lookup"><span data-stu-id="d89b0-110">Type: **CIM\_ComputerSystem**</span></span>

<span data-ttu-id="d89b0-111">CIM 電腦實例的參考，代表 [**要 \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) 終結的虛擬機器實例。</span><span class="sxs-lookup"><span data-stu-id="d89b0-111">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) that represents the virtual machine instance to be destroyed.</span></span>

</dd> <dt>

<span data-ttu-id="d89b0-112">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d89b0-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d89b0-113">類型： **CIM \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="d89b0-113">Type: **CIM\_ConcreteJob**</span></span>

<span data-ttu-id="d89b0-114">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="d89b0-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d89b0-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="d89b0-115">Return value</span></span>

<span data-ttu-id="d89b0-116">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d89b0-116">Type: **uint32**</span></span>

<span data-ttu-id="d89b0-117">如果這個方法是以同步方式執行，它會在成功時傳回0。</span><span class="sxs-lookup"><span data-stu-id="d89b0-117">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="d89b0-118">如果這個方法是以非同步方式執行，它會傳回4096，而 *作業* 輸出參數可以用來追蹤非同步作業的進度。</span><span class="sxs-lookup"><span data-stu-id="d89b0-118">If this method is executed asynchronously, it returns 4096 and the *Job* output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="d89b0-119">任何其他傳回值表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="d89b0-119">Any other return value indicates an error.</span></span>

<dl> <dt>

<span data-ttu-id="d89b0-120">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="d89b0-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d89b0-121">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="d89b0-121">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d89b0-122">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="d89b0-122">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d89b0-123">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="d89b0-123">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d89b0-124">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="d89b0-124">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d89b0-125">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="d89b0-125">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d89b0-126">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="d89b0-126">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d89b0-127">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="d89b0-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d89b0-128">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="d89b0-128">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="d89b0-129">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="d89b0-129">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="d89b0-130">備註</span><span class="sxs-lookup"><span data-stu-id="d89b0-130">Remarks</span></span>

<span data-ttu-id="d89b0-131">存取 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="d89b0-131">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d89b0-132">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="d89b0-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="d89b0-133">範例</span><span class="sxs-lookup"><span data-stu-id="d89b0-133">Examples</span></span>

<span data-ttu-id="d89b0-134">下列 c # 範例會使用 **DestroySystem** 方法來移除已規劃的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="d89b0-134">The following C# sample uses the **DestroySystem** method to remove a planned virtual machine.</span></span> <span data-ttu-id="d89b0-135">這段程式碼取自 [hyper-v 規劃的虛擬機器範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm)。</span><span class="sxs-lookup"><span data-stu-id="d89b0-135">This code is taken from the [Hyper-V planned virtual machines sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span></span> <span data-ttu-id="d89b0-136">您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。</span><span class="sxs-lookup"><span data-stu-id="d89b0-136">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d89b0-137">若要正常運作，必須在虛擬機器主機伺服器上執行下列程式碼，且必須以系統管理員許可權執行。</span><span class="sxs-lookup"><span data-stu-id="d89b0-137">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and removes it.
/// </summary>
/// <param name="pvmName">The name of the PVM to be removed.</param>
internal static void
RemovePvm(
    string pvmName
    )
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams =
        managementService.GetMethodParameters("DestroySystem"))
    {
        inParams["AffectedSystem"] = pvm.Path;

        Console.WriteLine("Removing Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams =
            managementService.InvokeMethod("DestroySystem", inParams, null))
        {
            WmiUtilities.ValidateOutput(outParams, scope);
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="d89b0-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="d89b0-138">Requirements</span></span>



| <span data-ttu-id="d89b0-139">需求</span><span class="sxs-lookup"><span data-stu-id="d89b0-139">Requirement</span></span> | <span data-ttu-id="d89b0-140">值</span><span class="sxs-lookup"><span data-stu-id="d89b0-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d89b0-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d89b0-141">Minimum supported client</span></span><br/> | <span data-ttu-id="d89b0-142">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d89b0-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d89b0-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d89b0-143">Minimum supported server</span></span><br/> | <span data-ttu-id="d89b0-144">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d89b0-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d89b0-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="d89b0-145">Namespace</span></span><br/>                | <span data-ttu-id="d89b0-146">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="d89b0-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d89b0-147">MOF</span><span class="sxs-lookup"><span data-stu-id="d89b0-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d89b0-148"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d89b0-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d89b0-149">DLL</span><span class="sxs-lookup"><span data-stu-id="d89b0-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d89b0-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d89b0-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d89b0-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d89b0-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d89b0-152">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="d89b0-152">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

