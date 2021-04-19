---
description: 將設定資料匯出為傳入 Msvm CollectionSnapshotService 類別的 ExportSnapshot 方法 \_ 。
ms.assetid: 03b448ed-72bc-485e-bb31-4445c53baa1c
title: Msvm_CollectionSnapshotExportSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotExportSettingData
- Msvm_CollectionSnapshotExportSettingData.CopyVmStorage
- Msvm_CollectionSnapshotExportSettingData.DifferentialBackupBase
- Msvm_CollectionSnapshotExportSettingData.BackupIntent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3e146fe2e2af17223e792d86cff16bf1c4149dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973251"
---
# <a name="msvm_collectionsnapshotexportsettingdata-class"></a><span data-ttu-id="684ff-103">Msvm \_ CollectionSnapshotExportSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="684ff-103">Msvm\_CollectionSnapshotExportSettingData class</span></span>

<span data-ttu-id="684ff-104">將設定資料匯出為傳入 [**Msvm \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md) 類別的 ExportSnapshot 方法。</span><span class="sxs-lookup"><span data-stu-id="684ff-104">Export setting data to be passed in to the ExportSnapshot method of [**Msvm\_CollectionSnapshotService**](msvm-collectionsnapshotservice.md) class.</span></span>

<span data-ttu-id="684ff-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="684ff-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="684ff-106">語法</span><span class="sxs-lookup"><span data-stu-id="684ff-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionSnapshotExportSettingData : CIM_SettingData
{
  boolean CopyVmStorage;
  string  DifferentialBackupBase;
  uint16  BackupIntent;
};
```

## <a name="members"></a><span data-ttu-id="684ff-107">成員</span><span class="sxs-lookup"><span data-stu-id="684ff-107">Members</span></span>

<span data-ttu-id="684ff-108">**Msvm \_ CollectionSnapshotExportSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="684ff-108">The **Msvm\_CollectionSnapshotExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="684ff-109">屬性</span><span class="sxs-lookup"><span data-stu-id="684ff-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="684ff-110">屬性</span><span class="sxs-lookup"><span data-stu-id="684ff-110">Properties</span></span>

<span data-ttu-id="684ff-111">**Msvm \_ CollectionSnapshotExportSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="684ff-111">The **Msvm\_CollectionSnapshotExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="684ff-112">**BackupIntent**</span><span class="sxs-lookup"><span data-stu-id="684ff-112">**BackupIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="684ff-113">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="684ff-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="684ff-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="684ff-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="684ff-115">指出將如何使用匯出的備份組的意圖：</span><span class="sxs-lookup"><span data-stu-id="684ff-115">Indicates the intent how the exported backup sets would be used:</span></span>

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span data-ttu-id="684ff-116"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (1) </span><span class="sxs-lookup"><span data-stu-id="684ff-116"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (1)</span></span>


</dt> <dd>

<span data-ttu-id="684ff-117">所有匯出的完整和差異備份集都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="684ff-117">All exported full and differential backup sets would be preserved as they are.</span></span>

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span data-ttu-id="684ff-118"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (2) </span><span class="sxs-lookup"><span data-stu-id="684ff-118"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (2)</span></span>


</dt> <dd>

<span data-ttu-id="684ff-119">匯出的完整和差異備份集會合並到合成的完整備份集。</span><span class="sxs-lookup"><span data-stu-id="684ff-119">The exported full and differential backup sets would be merged to synthesize full backup sets.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="684ff-120">**CopyVmStorage**</span><span class="sxs-lookup"><span data-stu-id="684ff-120">**CopyVmStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="684ff-121">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="684ff-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="684ff-122">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="684ff-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="684ff-123">若 **為 true**，則會在匯出 vm 時複製 vm 儲存體。</span><span class="sxs-lookup"><span data-stu-id="684ff-123">if **true**, the VM storage will be copied when the VM is exported.</span></span> <span data-ttu-id="684ff-124">否則 **為 false。**</span><span class="sxs-lookup"><span data-stu-id="684ff-124">Otherwise, **false.**</span></span>

</dd> <dt>

<span data-ttu-id="684ff-125">**DifferentialBackupBase**</span><span class="sxs-lookup"><span data-stu-id="684ff-125">**DifferentialBackupBase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="684ff-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="684ff-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="684ff-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="684ff-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="684ff-128">差異匯出的基底。</span><span class="sxs-lookup"><span data-stu-id="684ff-128">Base for differential export.</span></span> <span data-ttu-id="684ff-129">這是代表參考點之 [**Msvm \_ ReferencePointCollection**](msvm-referencepointcollection.md) 實例的路徑，或 [**Msvm \_ SnapshotCollection**](msvm-snapshotcollection.md) 實例的路徑，代表要當做差異匯出基底使用的快照集。</span><span class="sxs-lookup"><span data-stu-id="684ff-129">This is either path to an [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) instance that represents the reference point, or path to an [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) instance that represents the snapshot to be used as a base for differential export.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="684ff-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="684ff-130">Requirements</span></span>



| <span data-ttu-id="684ff-131">需求</span><span class="sxs-lookup"><span data-stu-id="684ff-131">Requirement</span></span> | <span data-ttu-id="684ff-132">值</span><span class="sxs-lookup"><span data-stu-id="684ff-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="684ff-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="684ff-133">Minimum supported client</span></span><br/> | <span data-ttu-id="684ff-134">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="684ff-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="684ff-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="684ff-135">Minimum supported server</span></span><br/> | <span data-ttu-id="684ff-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="684ff-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="684ff-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="684ff-137">Namespace</span></span><br/>                | <span data-ttu-id="684ff-138">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="684ff-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="684ff-139">MOF</span><span class="sxs-lookup"><span data-stu-id="684ff-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="684ff-140"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="684ff-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="684ff-141">DLL</span><span class="sxs-lookup"><span data-stu-id="684ff-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="684ff-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="684ff-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="684ff-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="684ff-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="684ff-144">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="684ff-144">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




