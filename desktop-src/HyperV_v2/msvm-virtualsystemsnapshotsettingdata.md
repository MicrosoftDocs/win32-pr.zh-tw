---
description: 提供要與 Msvm VirtualSystemSnapshotService 類別的 >icloudblob.createsnapshot 方法搭配使用的其他資訊 \_ 。
ms.assetid: d4a025c4-6a3c-4ae0-8f2c-421c1aa1eb23
title: Msvm_VirtualSystemSnapshotSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotSettingData
- Msvm_VirtualSystemSnapshotSettingData.ConsistencyLevel
- Msvm_VirtualSystemSnapshotSettingData.IgnoreNonSnapshottableDisks
- Msvm_VirtualSystemSnapshotSettingData.GuestBackupType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 32ab52da97e9fcc943c3a70548bb6b1a6d7994a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386104"
---
# <a name="msvm_virtualsystemsnapshotsettingdata-class"></a><span data-ttu-id="eacc5-103">Msvm \_ VirtualSystemSnapshotSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="eacc5-103">Msvm\_VirtualSystemSnapshotSettingData class</span></span>

<span data-ttu-id="eacc5-104">提供要與 [**Msvm \_ VirtualSystemSnapshotService**](msvm-virtualsystemsnapshotservice.md)類別的 [**>icloudblob.createsnapshot**](cim-virtualsystemsnapshotservice-createsnapshot.md)方法搭配使用的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="eacc5-104">Provides additional information to be used with the [**CreateSnapshot**](cim-virtualsystemsnapshotservice-createsnapshot.md) method of the [**Msvm\_VirtualSystemSnapshotService**](msvm-virtualsystemsnapshotservice.md) class.</span></span>

<span data-ttu-id="eacc5-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="eacc5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eacc5-106">語法</span><span class="sxs-lookup"><span data-stu-id="eacc5-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemSnapshotSettingData : CIM_SettingData
{
  uint8   ConsistencyLevel;
  boolean IgnoreNonSnapshottableDisks;
  uint8   GuestBackupType;
};
```

## <a name="members"></a><span data-ttu-id="eacc5-107">成員</span><span class="sxs-lookup"><span data-stu-id="eacc5-107">Members</span></span>

<span data-ttu-id="eacc5-108">**Msvm \_ VirtualSystemSnapshotSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="eacc5-108">The **Msvm\_VirtualSystemSnapshotSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="eacc5-109">屬性</span><span class="sxs-lookup"><span data-stu-id="eacc5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eacc5-110">屬性</span><span class="sxs-lookup"><span data-stu-id="eacc5-110">Properties</span></span>

<span data-ttu-id="eacc5-111">**Msvm \_ VirtualSystemSnapshotSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="eacc5-111">The **Msvm\_VirtualSystemSnapshotSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eacc5-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="eacc5-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eacc5-113">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="eacc5-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="eacc5-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eacc5-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eacc5-115">快照集的一致性層級。</span><span class="sxs-lookup"><span data-stu-id="eacc5-115">The consistency level of the snapshot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eacc5-116">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="eacc5-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="eacc5-117">**應用程式一致** (1) </span><span class="sxs-lookup"><span data-stu-id="eacc5-117">**Application Consistent** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="eacc5-118">損 **毀一致** (2) </span><span class="sxs-lookup"><span data-stu-id="eacc5-118">**Crash Consistent** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eacc5-119">**GuestBackupType**</span><span class="sxs-lookup"><span data-stu-id="eacc5-119">**GuestBackupType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eacc5-120">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="eacc5-120">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="eacc5-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eacc5-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eacc5-122">要在來賓內部使用的備份類型。</span><span class="sxs-lookup"><span data-stu-id="eacc5-122">Backup type to be used inside the guest.</span></span>

> [!Note]  
> <span data-ttu-id="eacc5-123">在 Windows 10 中新增的屬性，版本1703</span><span class="sxs-lookup"><span data-stu-id="eacc5-123">Property added in Windows 10, version 1703</span></span>

 

<dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="eacc5-124">**Undefined** (0)</span><span class="sxs-lookup"><span data-stu-id="eacc5-124">**Undefined** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Full"></span><span id="full"></span><span id="FULL"></span>

<span data-ttu-id="eacc5-125">**完整** (1) </span><span class="sxs-lookup"><span data-stu-id="eacc5-125">**Full** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Copy"></span><span id="copy"></span><span id="COPY"></span>

<span data-ttu-id="eacc5-126">**複製** (2) </span><span class="sxs-lookup"><span data-stu-id="eacc5-126">**Copy** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eacc5-127">**IgnoreNonSnapshottableDisks**</span><span class="sxs-lookup"><span data-stu-id="eacc5-127">**IgnoreNonSnapshottableDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eacc5-128">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="eacc5-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eacc5-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eacc5-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eacc5-130">指定在建立快照集時，是否要忽略非 snapshottable 磁片，例如傳遞磁片和光纖通道磁片。</span><span class="sxs-lookup"><span data-stu-id="eacc5-130">Specifies if non-snapshottable disks like passthrough disks and Fibre Channel Disks are to be ignored while creating the snapshot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eacc5-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="eacc5-131">Requirements</span></span>



| <span data-ttu-id="eacc5-132">需求</span><span class="sxs-lookup"><span data-stu-id="eacc5-132">Requirement</span></span> | <span data-ttu-id="eacc5-133">值</span><span class="sxs-lookup"><span data-stu-id="eacc5-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eacc5-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eacc5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="eacc5-135">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eacc5-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="eacc5-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eacc5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="eacc5-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="eacc5-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="eacc5-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="eacc5-138">Namespace</span></span><br/>                | <span data-ttu-id="eacc5-139">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="eacc5-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="eacc5-140">MOF</span><span class="sxs-lookup"><span data-stu-id="eacc5-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eacc5-141"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="eacc5-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eacc5-142">DLL</span><span class="sxs-lookup"><span data-stu-id="eacc5-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eacc5-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eacc5-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="eacc5-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eacc5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eacc5-145">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="eacc5-145">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




