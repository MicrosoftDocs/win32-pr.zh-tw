---
description: 驗證已規劃的虛擬機器設定，並將其轉換為實現的虛擬機器。
ms.assetid: bddbdc35-4603-45c3-96b4-04f445dbb3a6
title: Msvm_VirtualSystemManagementService 類別的 RealizePlannedSystem 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RealizePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fc69cbc9be9fc72bc7c1184ec30d9e2b58ba2b6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194556"
---
# <a name="realizeplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="7c0fa-103">Msvm VirtualSystemManagementService 類別的 RealizePlannedSystem 方法 \_</span><span class="sxs-lookup"><span data-stu-id="7c0fa-103">RealizePlannedSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="7c0fa-104">驗證已規劃的虛擬機器設定，並將其轉換為實現的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="7c0fa-104">Validates the configuration of a planned virtual machine and converts it to a realized virtual machine.</span></span> <span data-ttu-id="7c0fa-105">與虛擬機器相關聯的任何執行時間或儲存狀態檔案，都會從匯入目錄複寫到虛擬機器的資料根目錄（如果適用）。</span><span class="sxs-lookup"><span data-stu-id="7c0fa-105">Any runtime or saved state files associated with the virtual machine will be copied from the import directory to the virtual machine's data root, if applicable.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c0fa-106">語法</span><span class="sxs-lookup"><span data-stu-id="7c0fa-106">Syntax</span></span>


```mof
uint32 RealizePlannedSystem(
  [in]  Msvm_PlannedComputerSystem REF PlannedSystem,
  [out] CIM_ComputerSystem         REF ResultingSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7c0fa-107">參數</span><span class="sxs-lookup"><span data-stu-id="7c0fa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c0fa-108">*PlannedSystem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7c0fa-108">*PlannedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c0fa-109">[**Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md)實例的參考，該實例會轉換成已實現的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="7c0fa-109">A reference to the [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) instance which is to be converted into a realized virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="7c0fa-110">*ResultingSystem* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7c0fa-110">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c0fa-111">如果作業是以同步方式完成，則會參考代表所產生之已實現虛擬機器的 CIM 電腦類型物件。 [**\_**](msvm-computersystem.md)</span><span class="sxs-lookup"><span data-stu-id="7c0fa-111">If the operation is completed synchronously, a reference to a [**CIM\_ComputerSystem**](msvm-computersystem.md) object that represents the resulting realized virtual machine.</span></span>

<span data-ttu-id="7c0fa-112">Msvm 中的 [**資料 \_ 類型**](msvm-computersystem.md) 在 Windows 10 1703 版中更新。</span><span class="sxs-lookup"><span data-stu-id="7c0fa-112">Datatype updated from [**Msvm\_ComputerSystem**](msvm-computersystem.md) in Windows 10, version 1703.</span></span>

</dd> <dt>

<span data-ttu-id="7c0fa-113">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7c0fa-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c0fa-114">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="7c0fa-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c0fa-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="7c0fa-115">Return value</span></span>

<span data-ttu-id="7c0fa-116">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="7c0fa-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7c0fa-117">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="7c0fa-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7c0fa-118">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="7c0fa-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7c0fa-119">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="7c0fa-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="7c0fa-120">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="7c0fa-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="7c0fa-121">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="7c0fa-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="7c0fa-122">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="7c0fa-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="7c0fa-123">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="7c0fa-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="7c0fa-124">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="7c0fa-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="7c0fa-125">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="7c0fa-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="7c0fa-126">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="7c0fa-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="7c0fa-127">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="7c0fa-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="7c0fa-128">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="7c0fa-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="7c0fa-129">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="7c0fa-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="7c0fa-130">範例</span><span class="sxs-lookup"><span data-stu-id="7c0fa-130">Examples</span></span>

<span data-ttu-id="7c0fa-131">下列 c # 範例會使用 **RealizePlannedSystem** 方法來實現規劃的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="7c0fa-131">The following C# sample uses the **RealizePlannedSystem** method to realize a planned virtual machine.</span></span> <span data-ttu-id="7c0fa-132">這段程式碼取自 [hyper-v 規劃的虛擬機器範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm)。</span><span class="sxs-lookup"><span data-stu-id="7c0fa-132">This code is taken from the [Hyper-V planned virtual machines sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span></span> <span data-ttu-id="7c0fa-133">您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。</span><span class="sxs-lookup"><span data-stu-id="7c0fa-133">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7c0fa-134">若要正常運作，必須在虛擬機器主機伺服器上執行下列程式碼，且必須以系統管理員許可權執行。</span><span class="sxs-lookup"><span data-stu-id="7c0fa-134">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and realizes it.
/// </summary>
/// <param name="pvmName">The name of the PVM to be realized.</param>
/// <returns>The Realized Virtual Machine.</returns>
internal static ManagementObject
RealizePvm(
    string pvmName
    )
{
    ManagementObject vm = null;
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams =
        managementService.GetMethodParameters("RealizePlannedSystem"))
    {
        inParams["PlannedSystem"] = pvm.Path;

        Console.WriteLine("Realizing Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams =
            managementService.InvokeMethod("RealizePlannedSystem", inParams, null))
        {
            if (WmiUtilities.ValidateOutput(outParams, scope, true, true))
            {
                using (ManagementObject job =
                    new ManagementObject((string)outParams["Job"]))
                using (ManagementObjectCollection pvmCollection =
                    job.GetRelated("Msvm_ComputerSystem",
                        "Msvm_AffectedJobElement", null, null, null, null, false, null))
                {
                    vm = WmiUtilities.GetFirstObjectFromCollection(pvmCollection);
                }
            }
        }
    }

    return vm;
}
```



## <a name="requirements"></a><span data-ttu-id="7c0fa-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c0fa-135">Requirements</span></span>



| <span data-ttu-id="7c0fa-136">需求</span><span class="sxs-lookup"><span data-stu-id="7c0fa-136">Requirement</span></span> | <span data-ttu-id="7c0fa-137">值</span><span class="sxs-lookup"><span data-stu-id="7c0fa-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c0fa-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7c0fa-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7c0fa-139">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c0fa-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7c0fa-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7c0fa-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7c0fa-141">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c0fa-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7c0fa-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="7c0fa-142">Namespace</span></span><br/>                | <span data-ttu-id="7c0fa-143">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="7c0fa-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7c0fa-144">MOF</span><span class="sxs-lookup"><span data-stu-id="7c0fa-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c0fa-145"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="7c0fa-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c0fa-146">DLL</span><span class="sxs-lookup"><span data-stu-id="7c0fa-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c0fa-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7c0fa-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7c0fa-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c0fa-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c0fa-149">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="7c0fa-149">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

