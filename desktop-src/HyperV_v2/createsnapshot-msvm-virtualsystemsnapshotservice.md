---
description: 建立虛擬機器的快照集。
ms.assetid: 2de12fe7-5ec2-49d0-87ff-cd48c34fec46
title: 'Msvm_VirtualSystemSnapshotService 類別的 >icloudblob.createsnapshot 方法 (Dbdaoint) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c62b4abf60e367da1c4ac4b176e5f5d70f547c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319523"
---
# <a name="createsnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="c8da3-103">Msvm VirtualSystemSnapshotService 類別的 >icloudblob.createsnapshot 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c8da3-103">CreateSnapshot method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="c8da3-104">建立虛擬機器的快照集。</span><span class="sxs-lookup"><span data-stu-id="c8da3-104">Creates a snapshot of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8da3-105">語法</span><span class="sxs-lookup"><span data-stu-id="c8da3-105">Syntax</span></span>


```mof
uint32 CreateSnapshot(
  [in]      CIM_ComputerSystem           REF AffectedSystem,
  [in]      string                           SnapshotSettings,
  [in]      uint16                           SnapshotType,
  [in, out] CIM_VirtualSystemSettingData REF ResultingSnapshot,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c8da3-106">參數</span><span class="sxs-lookup"><span data-stu-id="c8da3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8da3-107">*AffectedSystem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8da3-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8da3-108">[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)電腦類型的參考，代表用來建立快照集的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c8da3-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine to create a snapshot of.</span></span>

</dd> <dt>

<span data-ttu-id="c8da3-109">*SnapshotSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8da3-109">*SnapshotSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8da3-110">字串，包含 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) 類別的內嵌實例，其中包含快照集的參數設定。</span><span class="sxs-lookup"><span data-stu-id="c8da3-110">A string that contains an embedded instance of a [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) class that contains the parameter settings for the snapshot.</span></span> <span data-ttu-id="c8da3-111">這個參數是選擇性的，而且可能是空字串。</span><span class="sxs-lookup"><span data-stu-id="c8da3-111">This parameter is optional and may be an empty string.</span></span>

</dd> <dt>

<span data-ttu-id="c8da3-112">*SnapshotType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8da3-112">*SnapshotType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8da3-113">指定所要求快照集的類型。</span><span class="sxs-lookup"><span data-stu-id="c8da3-113">Specifies the type of snapshot requested.</span></span> <span data-ttu-id="c8da3-114">這必須是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="c8da3-114">This must be one of the following values.</span></span>

<dt>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>

<span data-ttu-id="c8da3-115"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**完整快照** (2) </span><span class="sxs-lookup"><span data-stu-id="c8da3-115"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Full Snapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c8da3-116">完成虛擬機器的快照集。</span><span class="sxs-lookup"><span data-stu-id="c8da3-116">Complete snapshot of the virtual machine.</span></span>

</dd> <dt>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>

<span data-ttu-id="c8da3-117"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**磁片快照** (3) </span><span class="sxs-lookup"><span data-stu-id="c8da3-117"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Disk Snapshot** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c8da3-118">虛擬機器磁片的快照集。</span><span class="sxs-lookup"><span data-stu-id="c8da3-118">Snapshot of virtual machine disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c8da3-119"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="c8da3-119"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="c8da3-120"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="c8da3-120"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="c8da3-121">*ResultingSnapshot* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c8da3-121">*ResultingSnapshot* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8da3-122">[**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))物件的參考，該物件表示所產生的虛擬機器快照集。</span><span class="sxs-lookup"><span data-stu-id="c8da3-122">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) object that represents the resulting virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="c8da3-123">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c8da3-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8da3-124">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="c8da3-124">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8da3-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8da3-125">Return value</span></span>

<span data-ttu-id="c8da3-126">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c8da3-126">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c8da3-127">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="c8da3-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c8da3-128">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="c8da3-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c8da3-129">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="c8da3-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c8da3-130">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="c8da3-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c8da3-131">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="c8da3-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c8da3-132">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="c8da3-132">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c8da3-133">**不正確類型** (6) </span><span class="sxs-lookup"><span data-stu-id="c8da3-133">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c8da3-134">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="c8da3-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c8da3-135">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="c8da3-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c8da3-136">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="c8da3-136">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="c8da3-137">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="c8da3-137">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="c8da3-138">範例</span><span class="sxs-lookup"><span data-stu-id="c8da3-138">Examples</span></span>

<span data-ttu-id="c8da3-139">下列 c # 範例程式碼會建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c8da3-139">The following C# example code creates a virtual machine.</span></span> <span data-ttu-id="c8da3-140">您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。</span><span class="sxs-lookup"><span data-stu-id="c8da3-140">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8da3-141">若要正確運作，必須在虛擬機器主機伺服器上執行下列程式碼，且必須以系統管理員許可權執行。</span><span class="sxs-lookup"><span data-stu-id="c8da3-141">To function correctly, the following code must be run on the virtual machine host server, and it must be run with Administrator privileges.</span></span>

 


```CSharp
public static void CreateSnapshot(string vmName)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemSnapshotService");

    ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("CreateSnapshot");

    // Set the AffectedSystem property.
    ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
    if (null == vm)
    {
        throw new ArgumentException(string.Format("The virtual machine \"{0}\" could not be found.", vmName));
    }

    inParams["AffectedSystem"] = vm.Path.Path;

    // Set the SnapshotSettings property.
#if(true)
    inParams["SnapshotSettings"] = "";
#else
    ManagementObject snapshotSettings = Utility.GetServiceObject(scope, "CIM_SettingData"); 
    inParams["SnapshotSettings"] = snapshotSettings.ToString();
#endif       
    // Set the SnapshotType property.
    inParams["SnapshotType"] = 2; // Full snapshot.

    ManagementBaseObject outParams = virtualSystemService.InvokeMethod("CreateSnapshot", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("Snapshot was created successfully.");

            MiscClass.GetAffectedElement(outParams, scope);
        }
        else
        {
            Console.WriteLine("Failed to create snapshot VM");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        Console.WriteLine("Snapshot was created successfully.");
    }
    else
    {
        Console.WriteLine("Create virtual system snapshot failed with error {0}", outParams["ReturnValue"]);
    }

    inParams.Dispose();
    outParams.Dispose();
    vm.Dispose();
    virtualSystemService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="c8da3-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8da3-142">Requirements</span></span>



| <span data-ttu-id="c8da3-143">需求</span><span class="sxs-lookup"><span data-stu-id="c8da3-143">Requirement</span></span> | <span data-ttu-id="c8da3-144">值</span><span class="sxs-lookup"><span data-stu-id="c8da3-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8da3-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8da3-145">Minimum supported client</span></span><br/> | <span data-ttu-id="c8da3-146">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8da3-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c8da3-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8da3-147">Minimum supported server</span></span><br/> | <span data-ttu-id="c8da3-148">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8da3-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c8da3-149">命名空間</span><span class="sxs-lookup"><span data-stu-id="c8da3-149">Namespace</span></span><br/>                | <span data-ttu-id="c8da3-150">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="c8da3-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c8da3-151">標頭</span><span class="sxs-lookup"><span data-stu-id="c8da3-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8da3-152"><dt>Dbdaoint。h</dt></span><span class="sxs-lookup"><span data-stu-id="c8da3-152"><dt>Dbdaoint.h</dt></span></span> </dl>                   |
| <span data-ttu-id="c8da3-153">MOF</span><span class="sxs-lookup"><span data-stu-id="c8da3-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8da3-154"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="c8da3-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8da3-155">DLL</span><span class="sxs-lookup"><span data-stu-id="c8da3-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8da3-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c8da3-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c8da3-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8da3-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8da3-158">**Msvm \_ VirtualSystemSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="c8da3-158">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="c8da3-159">**CreateVirtualSystemSnapshot (V1)**</span><span class="sxs-lookup"><span data-stu-id="c8da3-159">**CreateVirtualSystemSnapshot (V1)**</span></span>](/previous-versions/windows/desktop/virtual/createvirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> </dl>

 

