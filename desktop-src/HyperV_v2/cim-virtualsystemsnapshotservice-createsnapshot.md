---
description: 建立虛擬系統的快照集。
ms.assetid: cad4cb4f-523f-4fda-ac88-8cece7abc227
title: CIM_VirtualSystemSnapshotService 類別的 >icloudblob.createsnapshot 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ee96098477501123cffc1fd59a52734bbbea35d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985005"
---
# <a name="createsnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="b2e7f-103">CIM VirtualSystemSnapshotService 類別的 >icloudblob.createsnapshot 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b2e7f-103">CreateSnapshot method of the CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="b2e7f-104">建立虛擬系統的快照集。</span><span class="sxs-lookup"><span data-stu-id="b2e7f-104">Creates a snapshot of a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2e7f-105">語法</span><span class="sxs-lookup"><span data-stu-id="b2e7f-105">Syntax</span></span>


```mof
uint32 CreateSnapshot(
  [in]      CIM_ComputerSystem           REF AffectedSystem,
  [in]      string                           SnapshotSettings,
  [in]      uint16                           SnapshotType,
  [in, out] CIM_VirtualSystemSettingData REF ResultingSnapshot,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b2e7f-106">參數</span><span class="sxs-lookup"><span data-stu-id="b2e7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2e7f-107">*AffectedSystem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b2e7f-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2e7f-108">受影響之虛擬系統的 CIM 系統可參考。 [**\_**](cim-computersystem.md)</span><span class="sxs-lookup"><span data-stu-id="b2e7f-108">A [**CIM\_ComputerSystem**](cim-computersystem.md) reference to the affected virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="b2e7f-109">*SnapshotSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b2e7f-109">*SnapshotSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2e7f-110">參數設定。</span><span class="sxs-lookup"><span data-stu-id="b2e7f-110">Parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="b2e7f-111">*SnapshotType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b2e7f-111">*SnapshotType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2e7f-112">要求的快照集類型：</span><span class="sxs-lookup"><span data-stu-id="b2e7f-112">Requested snapshot type:</span></span>

<dt>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>

<span data-ttu-id="b2e7f-113"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**完整快照** (2) </span><span class="sxs-lookup"><span data-stu-id="b2e7f-113"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Full Snapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b2e7f-114">虛擬系統的完整快照集。</span><span class="sxs-lookup"><span data-stu-id="b2e7f-114">Complete snapshot of the virtual system.</span></span>

</dd> <dt>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>

<span data-ttu-id="b2e7f-115"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**磁片快照** (3) </span><span class="sxs-lookup"><span data-stu-id="b2e7f-115"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Disk Snapshot** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b2e7f-116">虛擬系統磁片的快照集。</span><span class="sxs-lookup"><span data-stu-id="b2e7f-116">Snapshot of virtual system disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="b2e7f-117"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="b2e7f-117"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="b2e7f-118"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="b2e7f-118"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="b2e7f-119">*ResultingSnapshot* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="b2e7f-119">*ResultingSnapshot* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2e7f-120">產生的虛擬系統快照集的 [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) 參考。</span><span class="sxs-lookup"><span data-stu-id="b2e7f-120">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the resulting virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="b2e7f-121">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b2e7f-121">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2e7f-122">如果作業的執行時間很長，則可以選擇性地傳回作業。</span><span class="sxs-lookup"><span data-stu-id="b2e7f-122">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="b2e7f-123">在此情況下，代表新虛擬系統快照集的 [**cim \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) 類別的實例會透過 [**cim \_ AffectedJobElement**](cim-affectedjobelement.md) 關聯來呈現，而 **AffectedElement** 屬性的值會參考代表虛擬系統快照的 **cim \_ VirtualSystemSettingData** 類別的新實例，而 **ElementEffects** 的值則會設定為 5 (建立) 。</span><span class="sxs-lookup"><span data-stu-id="b2e7f-123">In this case, the instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing the new virtual system snapshot is presented via the [**CIM\_AffectedJobElement**](cim-affectedjobelement.md) association with the value of the **AffectedElement** property referring to the new instance of the **CIM\_VirtualSystemSettingData** class representing the virtual system snapshot and the value of the **ElementEffects** set to 5 (Create).</span></span>

> [!Note]  
> <span data-ttu-id="b2e7f-124">此參數在 Windows 8.1 中是讀取/寫入。</span><span class="sxs-lookup"><span data-stu-id="b2e7f-124">This parameter was read/write in Windows 8.1.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2e7f-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="b2e7f-125">Return value</span></span>

<span data-ttu-id="b2e7f-126">成功時，會傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="b2e7f-126">On success, returns 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="b2e7f-127">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="b2e7f-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b2e7f-128">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="b2e7f-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b2e7f-129">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="b2e7f-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b2e7f-130">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="b2e7f-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b2e7f-131">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="b2e7f-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b2e7f-132">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="b2e7f-132">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b2e7f-133">**不正確類型** (6) </span><span class="sxs-lookup"><span data-stu-id="b2e7f-133">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="b2e7f-134">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="b2e7f-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b2e7f-135">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="b2e7f-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b2e7f-136">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="b2e7f-136">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="b2e7f-137">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="b2e7f-137">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b2e7f-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2e7f-138">Requirements</span></span>



| <span data-ttu-id="b2e7f-139">需求</span><span class="sxs-lookup"><span data-stu-id="b2e7f-139">Requirement</span></span> | <span data-ttu-id="b2e7f-140">值</span><span class="sxs-lookup"><span data-stu-id="b2e7f-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2e7f-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2e7f-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b2e7f-142">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b2e7f-142">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b2e7f-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2e7f-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b2e7f-144">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b2e7f-144">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b2e7f-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="b2e7f-145">Namespace</span></span><br/>                | <span data-ttu-id="b2e7f-146">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="b2e7f-146">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b2e7f-147">MOF</span><span class="sxs-lookup"><span data-stu-id="b2e7f-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2e7f-148"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b2e7f-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2e7f-149">DLL</span><span class="sxs-lookup"><span data-stu-id="b2e7f-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2e7f-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b2e7f-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b2e7f-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2e7f-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2e7f-152">**CIM \_ VirtualSystemSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="b2e7f-152">**CIM\_VirtualSystemSnapshotService**</span></span>](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




