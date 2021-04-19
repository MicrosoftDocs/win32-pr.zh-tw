---
description: 代表主機上虛擬系統移轉服務的設定。
ms.assetid: 56711134-9a4a-49bd-8a0e-ce679b959adf
title: Msvm_VirtualSystemMigrationServiceSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationServiceSettingData
- Msvm_VirtualSystemMigrationServiceSettingData.InstanceID
- Msvm_VirtualSystemMigrationServiceSettingData.Caption
- Msvm_VirtualSystemMigrationServiceSettingData.Description
- Msvm_VirtualSystemMigrationServiceSettingData.ElementName
- Msvm_VirtualSystemMigrationServiceSettingData.EnableVirtualSystemMigration
- Msvm_VirtualSystemMigrationServiceSettingData.MaximumActiveVirtualSystemMigration
- Msvm_VirtualSystemMigrationServiceSettingData.MaximumActiveStorageMigration
- Msvm_VirtualSystemMigrationServiceSettingData.AuthenticationType
- Msvm_VirtualSystemMigrationServiceSettingData.EnableCompression
- Msvm_VirtualSystemMigrationServiceSettingData.EnableSmbTransport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8c8685e468d60983408c52a985169c61be91f632
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973609"
---
# <a name="msvm_virtualsystemmigrationservicesettingdata-class"></a><span data-ttu-id="e10ff-103">Msvm \_ VirtualSystemMigrationServiceSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="e10ff-103">Msvm\_VirtualSystemMigrationServiceSettingData class</span></span>

<span data-ttu-id="e10ff-104">代表主機上虛擬系統移轉服務的設定。</span><span class="sxs-lookup"><span data-stu-id="e10ff-104">Represents the settings for the virtual system migration service on a host.</span></span> <span data-ttu-id="e10ff-105">無法直接修改這個類別的屬性。</span><span class="sxs-lookup"><span data-stu-id="e10ff-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="e10ff-106">用戶端必須呼叫 **Msvm \_ VirtualSystemMigrationService. ModifyServiceSettings** 方法來修改任何這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e10ff-106">The client must call the **Msvm\_VirtualSystemMigrationService.ModifyServiceSettings** method to modify any of these properties.</span></span>

<span data-ttu-id="e10ff-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e10ff-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e10ff-108">語法</span><span class="sxs-lookup"><span data-stu-id="e10ff-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  boolean EnableVirtualSystemMigration;
  uint32  MaximumActiveVirtualSystemMigration;
  uint32  MaximumActiveStorageMigration;
  uint32  AuthenticationType;
  boolean EnableCompression = True;
  boolean EnableSmbTransport = False;
};
```

## <a name="members"></a><span data-ttu-id="e10ff-109">成員</span><span class="sxs-lookup"><span data-stu-id="e10ff-109">Members</span></span>

<span data-ttu-id="e10ff-110">**Msvm \_ VirtualSystemMigrationServiceSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e10ff-110">The **Msvm\_VirtualSystemMigrationServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="e10ff-111">屬性</span><span class="sxs-lookup"><span data-stu-id="e10ff-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e10ff-112">屬性</span><span class="sxs-lookup"><span data-stu-id="e10ff-112">Properties</span></span>

<span data-ttu-id="e10ff-113">**Msvm \_ VirtualSystemMigrationServiceSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e10ff-113">The **Msvm\_VirtualSystemMigrationServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e10ff-114">**AuthenticationType**</span><span class="sxs-lookup"><span data-stu-id="e10ff-114">**AuthenticationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10ff-115">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e10ff-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e10ff-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e10ff-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e10ff-117">指定用於虛擬系統移轉網路連接的驗證機制。</span><span class="sxs-lookup"><span data-stu-id="e10ff-117">Specifies the authentication mechanism used for virtual system migration network connections.</span></span> <span data-ttu-id="e10ff-118">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="e10ff-118">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

<dt>

<span id="CredSSP"></span><span id="credssp"></span><span id="CREDSSP"></span>

<span data-ttu-id="e10ff-119">**CredSSP** (0) </span><span class="sxs-lookup"><span data-stu-id="e10ff-119">**CredSSP** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Kerberos"></span><span id="kerberos"></span><span id="KERBEROS"></span>

<span data-ttu-id="e10ff-120">**Kerberos** (1) </span><span class="sxs-lookup"><span data-stu-id="e10ff-120">**Kerberos** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e10ff-121">**標題**</span><span class="sxs-lookup"><span data-stu-id="e10ff-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10ff-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e10ff-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e10ff-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e10ff-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e10ff-124">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="e10ff-124">A short description of the object.</span></span> <span data-ttu-id="e10ff-125">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) 類別。</span><span class="sxs-lookup"><span data-stu-id="e10ff-125">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class.</span></span>

</dd> <dt>

<span data-ttu-id="e10ff-126">**說明**</span><span class="sxs-lookup"><span data-stu-id="e10ff-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10ff-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e10ff-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e10ff-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e10ff-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e10ff-129">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="e10ff-129">A description of the object.</span></span> <span data-ttu-id="e10ff-130">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="e10ff-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e10ff-131">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e10ff-131">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10ff-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e10ff-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e10ff-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e10ff-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e10ff-134">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="e10ff-134">A display name for the object.</span></span> <span data-ttu-id="e10ff-135">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="e10ff-135">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e10ff-136">**EnableCompression**</span><span class="sxs-lookup"><span data-stu-id="e10ff-136">**EnableCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10ff-137">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e10ff-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e10ff-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e10ff-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e10ff-139">指出是否啟用或停用即時移轉流量的壓縮。</span><span class="sxs-lookup"><span data-stu-id="e10ff-139">Indicates whether compression of live migration traffic is enabled or disabled.</span></span> <span data-ttu-id="e10ff-140">True 表示已啟用。</span><span class="sxs-lookup"><span data-stu-id="e10ff-140">True indicates enabled.</span></span>

<span data-ttu-id="e10ff-141">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="e10ff-141">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="e10ff-142">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="e10ff-142">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="e10ff-143">**EnableSmbTransport**</span><span class="sxs-lookup"><span data-stu-id="e10ff-143">**EnableSmbTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10ff-144">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e10ff-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e10ff-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e10ff-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e10ff-146">指出是否在啟用或停用虛擬系統移轉期間，使用 SMB 做為傳輸類型，以在 Hyper-v 主機之間傳輸 VM 狀態。</span><span class="sxs-lookup"><span data-stu-id="e10ff-146">Indicates whether use of SMB as a transport type for transferring VM state between the Hyper-V hosts during virtual system migration is enabled or disabled.</span></span> <span data-ttu-id="e10ff-147">**True** 表示已啟用。</span><span class="sxs-lookup"><span data-stu-id="e10ff-147">**True** indicates enabled.</span></span> <span data-ttu-id="e10ff-148">如果 RDMA Nic 是在 VM 即時移轉期間設定為 SMB 傳輸，則會達到較高的效能。</span><span class="sxs-lookup"><span data-stu-id="e10ff-148">A higher performance is achieved if RDMA NICs are configured for SMB transport during VM live migration.</span></span> <span data-ttu-id="e10ff-149">如果 **EnableSmbTransport** 值為 true，則會忽略 **EnableCompression** 的值。</span><span class="sxs-lookup"><span data-stu-id="e10ff-149">If **EnableSmbTransport** value is true, the value of **EnableCompression** is ignored.</span></span>

<span data-ttu-id="e10ff-150">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="e10ff-150">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="e10ff-151">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="e10ff-151">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="e10ff-152">**EnableVirtualSystemMigration**</span><span class="sxs-lookup"><span data-stu-id="e10ff-152">**EnableVirtualSystemMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10ff-153">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e10ff-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e10ff-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e10ff-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e10ff-155">指定虛擬系統移轉是否已啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="e10ff-155">Specifies whether virtual system migration is enabled or disabled.</span></span> <span data-ttu-id="e10ff-156">儲存體遷移一律為啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="e10ff-156">Storage migration is always enabled.</span></span> <span data-ttu-id="e10ff-157">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="e10ff-157">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="e10ff-158">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e10ff-158">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10ff-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e10ff-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e10ff-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e10ff-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10ff-161">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="e10ff-161">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e10ff-162">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="e10ff-162">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e10ff-163">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="e10ff-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e10ff-164">**MaximumActiveStorageMigration**</span><span class="sxs-lookup"><span data-stu-id="e10ff-164">**MaximumActiveStorageMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10ff-165">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e10ff-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e10ff-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e10ff-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e10ff-167">指定允許的主動式儲存體遷移數目上限。</span><span class="sxs-lookup"><span data-stu-id="e10ff-167">Specifies the maximum number of active storage migrations allowed.</span></span> <span data-ttu-id="e10ff-168">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="e10ff-168">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="e10ff-169">**MaximumActiveVirtualSystemMigration**</span><span class="sxs-lookup"><span data-stu-id="e10ff-169">**MaximumActiveVirtualSystemMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10ff-170">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e10ff-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e10ff-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e10ff-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e10ff-172">指定允許的主動式虛擬系統移轉數目上限。</span><span class="sxs-lookup"><span data-stu-id="e10ff-172">Specifies the maximum number of active virtual system migrations allowed.</span></span> <span data-ttu-id="e10ff-173">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="e10ff-173">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e10ff-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="e10ff-174">Requirements</span></span>



| <span data-ttu-id="e10ff-175">需求</span><span class="sxs-lookup"><span data-stu-id="e10ff-175">Requirement</span></span> | <span data-ttu-id="e10ff-176">值</span><span class="sxs-lookup"><span data-stu-id="e10ff-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e10ff-177">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e10ff-177">Minimum supported client</span></span><br/> | <span data-ttu-id="e10ff-178">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e10ff-178">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e10ff-179">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e10ff-179">Minimum supported server</span></span><br/> | <span data-ttu-id="e10ff-180">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e10ff-180">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e10ff-181">命名空間</span><span class="sxs-lookup"><span data-stu-id="e10ff-181">Namespace</span></span><br/>                | <span data-ttu-id="e10ff-182">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="e10ff-182">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e10ff-183">MOF</span><span class="sxs-lookup"><span data-stu-id="e10ff-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e10ff-184"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e10ff-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e10ff-185">DLL</span><span class="sxs-lookup"><span data-stu-id="e10ff-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e10ff-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e10ff-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e10ff-187">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e10ff-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e10ff-188">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="e10ff-188">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="e10ff-189">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="e10ff-189">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

