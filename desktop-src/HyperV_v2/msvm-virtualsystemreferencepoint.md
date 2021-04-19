---
description: 表示虛擬系統的參考點。
ms.assetid: b3ba4fa7-3b77-4a1d-ab8f-d38af12ab5dd
title: Msvm_VirtualSystemReferencePoint 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePoint
- Msvm_VirtualSystemReferencePoint.InstanceID
- Msvm_VirtualSystemReferencePoint.ReferencePointType
- Msvm_VirtualSystemReferencePoint.ConsistencyLevel
- Msvm_VirtualSystemReferencePoint.VirtualSystemIdentifier
- Msvm_VirtualSystemReferencePoint.HasAssociatedData
- Msvm_VirtualSystemReferencePoint.VirtualDiskIdentifiers
- Msvm_VirtualSystemReferencePoint.ResilientChangeTrackingIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: add160cf44a592462634704ddf783cd8f4084068
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106986448"
---
# <a name="msvm_virtualsystemreferencepoint-class"></a><span data-ttu-id="d8b39-103">Msvm \_ VirtualSystemReferencePoint 類別</span><span class="sxs-lookup"><span data-stu-id="d8b39-103">Msvm\_VirtualSystemReferencePoint class</span></span>

<span data-ttu-id="d8b39-104">表示虛擬系統的參考點。</span><span class="sxs-lookup"><span data-stu-id="d8b39-104">Represents a reference point for a virtual system.</span></span>

<span data-ttu-id="d8b39-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d8b39-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8b39-106">語法</span><span class="sxs-lookup"><span data-stu-id="d8b39-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePoint : CIM_ManagedElement
{
  string  InstanceID;
  uint16  ReferencePointType;
  uint16  ConsistencyLevel;
  string  VirtualSystemIdentifier;
  boolean HasAssociatedData;
  string  VirtualDiskIdentifiers[];
  string  ResilientChangeTrackingIdentifiers[];
};
```

## <a name="members"></a><span data-ttu-id="d8b39-107">成員</span><span class="sxs-lookup"><span data-stu-id="d8b39-107">Members</span></span>

<span data-ttu-id="d8b39-108">**Msvm \_ VirtualSystemReferencePoint** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d8b39-108">The **Msvm\_VirtualSystemReferencePoint** class has these types of members:</span></span>

-   [<span data-ttu-id="d8b39-109">屬性</span><span class="sxs-lookup"><span data-stu-id="d8b39-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d8b39-110">屬性</span><span class="sxs-lookup"><span data-stu-id="d8b39-110">Properties</span></span>

<span data-ttu-id="d8b39-111">**Msvm \_ VirtualSystemReferencePoint** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d8b39-111">The **Msvm\_VirtualSystemReferencePoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d8b39-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="d8b39-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8b39-113">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d8b39-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8b39-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d8b39-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d8b39-115">參考點的一致性層級。</span><span class="sxs-lookup"><span data-stu-id="d8b39-115">The consistency level of the reference point.</span></span>

<dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="d8b39-116"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**應用程式一致** (1) </span><span class="sxs-lookup"><span data-stu-id="d8b39-116"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d8b39-117">參考點表示虛擬系統處於應用程式一致狀態的時間點。</span><span class="sxs-lookup"><span data-stu-id="d8b39-117">The reference point indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="d8b39-118"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>損 **毀一致** (2) </span><span class="sxs-lookup"><span data-stu-id="d8b39-118"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d8b39-119">參考點表示虛擬系統處於損毀一致狀態的時間點。</span><span class="sxs-lookup"><span data-stu-id="d8b39-119">The reference point indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d8b39-120">**HasAssociatedData**</span><span class="sxs-lookup"><span data-stu-id="d8b39-120">**HasAssociatedData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8b39-121">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d8b39-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d8b39-122">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d8b39-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d8b39-123">如果參考點具有相關聯的資料，則設定為 **true** 。</span><span class="sxs-lookup"><span data-stu-id="d8b39-123">Set to **true** if the reference point has associated data.</span></span> <span data-ttu-id="d8b39-124">這僅適用于以記錄為基礎的參考點。</span><span class="sxs-lookup"><span data-stu-id="d8b39-124">This is valid only for log based reference points.</span></span> <span data-ttu-id="d8b39-125">若為 .RCT 參考點， **HasAssociatedData** 會設為 **false**。</span><span class="sxs-lookup"><span data-stu-id="d8b39-125">For RCT-based reference points, **HasAssociatedData** is set to **false**.</span></span> <span data-ttu-id="d8b39-126">針對以記錄為基礎的參考點，一旦捨棄記錄檔， **HasAssociatedData** 就會變成 **false**。</span><span class="sxs-lookup"><span data-stu-id="d8b39-126">For log based reference points, once the log is discarded **HasAssociatedData** becomes **false**.</span></span>

</dd> <dt>

<span data-ttu-id="d8b39-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d8b39-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8b39-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d8b39-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8b39-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8b39-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8b39-130">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "InstanceID" ) 、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="d8b39-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d8b39-131">參考點物件的唯一識別。</span><span class="sxs-lookup"><span data-stu-id="d8b39-131">Unique identification of a reference point object.</span></span>

</dd> <dt>

<span data-ttu-id="d8b39-132">**ReferencePointType**</span><span class="sxs-lookup"><span data-stu-id="d8b39-132">**ReferencePointType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8b39-133">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d8b39-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8b39-134">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d8b39-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d8b39-135">指出參考點的型別。</span><span class="sxs-lookup"><span data-stu-id="d8b39-135">Indicates the type of the reference point.</span></span>

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="d8b39-136"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>以 **記錄為基礎** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="d8b39-136"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d8b39-137">Hyper-v 複本記錄追蹤。</span><span class="sxs-lookup"><span data-stu-id="d8b39-137">Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="d8b39-138"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**依** (2) 的 .rct</span><span class="sxs-lookup"><span data-stu-id="d8b39-138"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d8b39-139">以虛擬磁片的復原變更追蹤為基礎。</span><span class="sxs-lookup"><span data-stu-id="d8b39-139">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d8b39-140">**ResilientChangeTrackingIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="d8b39-140">**ResilientChangeTrackingIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8b39-141">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="d8b39-141">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d8b39-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8b39-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8b39-143">在建立此參考點時，對應至 VM 虛擬磁片的 .RCT 識別碼陣列。</span><span class="sxs-lookup"><span data-stu-id="d8b39-143">An array of RCT IDs corresponding to the virtual disks of the VM at the time this reference point was created.</span></span> <span data-ttu-id="d8b39-144">此欄位僅適用于以 .RCT 為基礎的參考點。</span><span class="sxs-lookup"><span data-stu-id="d8b39-144">This field is valid only for RCT-based reference points.</span></span>

</dd> <dt>

<span data-ttu-id="d8b39-145">**VirtualDiskIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="d8b39-145">**VirtualDiskIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8b39-146">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="d8b39-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d8b39-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8b39-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8b39-148">WMI 實例識別碼的陣列，這個陣列會在建立此參考點時對應至 VM 的虛擬磁片。</span><span class="sxs-lookup"><span data-stu-id="d8b39-148">An array of WMI instance IDs corresponding to the virtual disks of the VM at the time this reference point was created.</span></span> <span data-ttu-id="d8b39-149">這些虛擬磁片具有與它們相關聯的 .RCT 識別碼。</span><span class="sxs-lookup"><span data-stu-id="d8b39-149">These virtual disks have RCT IDs associated with them.</span></span>

</dd> <dt>

<span data-ttu-id="d8b39-150">**VirtualSystemIdentifier**</span><span class="sxs-lookup"><span data-stu-id="d8b39-150">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8b39-151">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d8b39-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8b39-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d8b39-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8b39-153">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_**](cim-computersystem.md)未執行。**名稱**") </span><span class="sxs-lookup"><span data-stu-id="d8b39-153">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="d8b39-154">此參考點所屬 [**的 \_ CIM**](cim-computersystem.md) 程式名稱</span><span class="sxs-lookup"><span data-stu-id="d8b39-154">The name of the [**CIM\_ComputerSystem**](cim-computersystem.md) to which this reference point belongs</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8b39-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8b39-155">Requirements</span></span>



| <span data-ttu-id="d8b39-156">需求</span><span class="sxs-lookup"><span data-stu-id="d8b39-156">Requirement</span></span> | <span data-ttu-id="d8b39-157">值</span><span class="sxs-lookup"><span data-stu-id="d8b39-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8b39-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d8b39-158">Minimum supported client</span></span><br/> | <span data-ttu-id="d8b39-159">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8b39-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="d8b39-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d8b39-160">Minimum supported server</span></span><br/> | <span data-ttu-id="d8b39-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d8b39-161">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d8b39-162">命名空間</span><span class="sxs-lookup"><span data-stu-id="d8b39-162">Namespace</span></span><br/>                | <span data-ttu-id="d8b39-163">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="d8b39-163">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d8b39-164">MOF</span><span class="sxs-lookup"><span data-stu-id="d8b39-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8b39-165"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d8b39-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8b39-166">DLL</span><span class="sxs-lookup"><span data-stu-id="d8b39-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8b39-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d8b39-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d8b39-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8b39-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8b39-169">**CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="d8b39-169">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

