---
description: 驗證指定的計畫系統。
ms.assetid: cb969b38-f36d-4c70-b234-590f1c219d22
title: Msvm_VirtualSystemManagementService 類別的 ValidatePlannedSystem 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ValidatePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 96137c3774291e06bfffdea3843658a427e36950
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694672"
---
# <a name="validateplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="36751-103">Msvm VirtualSystemManagementService 類別的 ValidatePlannedSystem 方法 \_</span><span class="sxs-lookup"><span data-stu-id="36751-103">ValidatePlannedSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="36751-104">驗證指定的計畫系統。</span><span class="sxs-lookup"><span data-stu-id="36751-104">Validates the specified planned system.</span></span> <span data-ttu-id="36751-105">這牽涉到檢查虛擬機器設定、裝置、快照集設定、快照裝置、儲存的狀態檔案和儲存體檔案。</span><span class="sxs-lookup"><span data-stu-id="36751-105">This involves checks of the virtual machine configuration, devices, snapshot configuration, snapshot devices, saved state files and storage files.</span></span>

## <a name="syntax"></a><span data-ttu-id="36751-106">語法</span><span class="sxs-lookup"><span data-stu-id="36751-106">Syntax</span></span>


```mof
uint32 ValidatePlannedSystem(
  [in]  Msvm_PlannedComputerSystem REF PlannedSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="36751-107">參數</span><span class="sxs-lookup"><span data-stu-id="36751-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36751-108">*PlannedSystem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="36751-108">*PlannedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36751-109">[**Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md)物件的參考，該物件代表要驗證的計畫系統。</span><span class="sxs-lookup"><span data-stu-id="36751-109">A reference to an [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) object that represents the planned system to be validated.</span></span>

</dd> <dt>

<span data-ttu-id="36751-110">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="36751-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36751-111">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="36751-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36751-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="36751-112">Return value</span></span>

<span data-ttu-id="36751-113">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="36751-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="36751-114">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="36751-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="36751-115">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="36751-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="36751-116">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="36751-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="36751-117">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="36751-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="36751-118">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="36751-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="36751-119">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="36751-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="36751-120">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="36751-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="36751-121">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="36751-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="36751-122">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="36751-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="36751-123">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="36751-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="36751-124">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="36751-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="36751-125">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="36751-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="36751-126">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="36751-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="36751-127">**使用中的** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="36751-127">**File in Use** (32779)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="36751-128">範例</span><span class="sxs-lookup"><span data-stu-id="36751-128">Examples</span></span>

<span data-ttu-id="36751-129">下列 c # 範例會使用 **ValidatePlannedSystem** 方法來驗證已規劃的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="36751-129">The following C# sample uses the **ValidatePlannedSystem** method to validate a planned virtual machine.</span></span> <span data-ttu-id="36751-130">這段程式碼取自 [hyper-v 規劃的虛擬機器範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm)。</span><span class="sxs-lookup"><span data-stu-id="36751-130">This code is taken from the [Hyper-V planned virtual machines sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span></span> <span data-ttu-id="36751-131">您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。</span><span class="sxs-lookup"><span data-stu-id="36751-131">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="36751-132">若要正常運作，必須在虛擬機器主機伺服器上執行下列程式碼，且必須以系統管理員許可權執行。</span><span class="sxs-lookup"><span data-stu-id="36751-132">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and validates it, displaying
/// any warnings produced.
/// </summary>
/// <param name="pvmName">The name of the PVM to be validated.</param>
internal static void
ValidatePvm(
    string pvmName
    )
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams = 
        managementService.GetMethodParameters("ValidatePlannedSystem"))
    {
        inParams["PlannedSystem"] = pvm.Path;

        Console.WriteLine("Validating Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams = 
            managementService.InvokeMethod("ValidatePlannedSystem", inParams, null))
        {
            if (WmiUtilities.ValidateOutput(outParams, scope))
            {
                using (ManagementObject job = 
                    new ManagementObject((string)outParams["Job"]))
                {
                    WmiUtilities.PrintMsvmErrors(job);
                }
            }
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="36751-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="36751-133">Requirements</span></span>



| <span data-ttu-id="36751-134">需求</span><span class="sxs-lookup"><span data-stu-id="36751-134">Requirement</span></span> | <span data-ttu-id="36751-135">值</span><span class="sxs-lookup"><span data-stu-id="36751-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36751-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36751-136">Minimum supported client</span></span><br/> | <span data-ttu-id="36751-137">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36751-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="36751-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36751-138">Minimum supported server</span></span><br/> | <span data-ttu-id="36751-139">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36751-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="36751-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="36751-140">Namespace</span></span><br/>                | <span data-ttu-id="36751-141">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="36751-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="36751-142">MOF</span><span class="sxs-lookup"><span data-stu-id="36751-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36751-143"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="36751-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="36751-144">DLL</span><span class="sxs-lookup"><span data-stu-id="36751-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36751-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="36751-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="36751-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36751-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36751-147">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="36751-147">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

