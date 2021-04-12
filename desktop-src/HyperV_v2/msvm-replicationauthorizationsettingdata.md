---
description: 代表復原伺服器的授權專案。
ms.assetid: 8c057b39-7102-4fbf-b4be-f18627a88834
title: Msvm_ReplicationAuthorizationSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationAuthorizationSettingData
- Msvm_ReplicationAuthorizationSettingData.InstanceID
- Msvm_ReplicationAuthorizationSettingData.Caption
- Msvm_ReplicationAuthorizationSettingData.Description
- Msvm_ReplicationAuthorizationSettingData.ElementName
- Msvm_ReplicationAuthorizationSettingData.AllowedPrimaryHostSystem
- Msvm_ReplicationAuthorizationSettingData.TrustGroup
- Msvm_ReplicationAuthorizationSettingData.ReplicaStorageLocation
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ba069de1bbe005e8a2a06891db8218ab313baa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192985"
---
# <a name="msvm_replicationauthorizationsettingdata-class"></a><span data-ttu-id="74f62-103">Msvm \_ ReplicationAuthorizationSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="74f62-103">Msvm\_ReplicationAuthorizationSettingData class</span></span>

<span data-ttu-id="74f62-104">代表復原伺服器的授權專案。</span><span class="sxs-lookup"><span data-stu-id="74f62-104">Represents an authorization entry for a recovery server.</span></span>

<span data-ttu-id="74f62-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="74f62-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="74f62-106">語法</span><span class="sxs-lookup"><span data-stu-id="74f62-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationAuthorizationSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string AllowedPrimaryHostSystem;
  string TrustGroup;
  string ReplicaStorageLocation;
};
```

## <a name="members"></a><span data-ttu-id="74f62-107">成員</span><span class="sxs-lookup"><span data-stu-id="74f62-107">Members</span></span>

<span data-ttu-id="74f62-108">**Msvm \_ ReplicationAuthorizationSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="74f62-108">The **Msvm\_ReplicationAuthorizationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="74f62-109">屬性</span><span class="sxs-lookup"><span data-stu-id="74f62-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="74f62-110">屬性</span><span class="sxs-lookup"><span data-stu-id="74f62-110">Properties</span></span>

<span data-ttu-id="74f62-111">**Msvm \_ ReplicationAuthorizationSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="74f62-111">The **Msvm\_ReplicationAuthorizationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="74f62-112">**AllowedPrimaryHostSystem**</span><span class="sxs-lookup"><span data-stu-id="74f62-112">**AllowedPrimaryHostSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74f62-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="74f62-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74f62-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="74f62-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74f62-115">允許複寫到此復原伺服器之主伺服器的完整功能變數名稱或組名。</span><span class="sxs-lookup"><span data-stu-id="74f62-115">The fully qualified domain name or group name of the primary servers that are allowed to replicate to this recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="74f62-116">**標題**</span><span class="sxs-lookup"><span data-stu-id="74f62-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74f62-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="74f62-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74f62-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74f62-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74f62-119">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="74f62-119">A short description of the object.</span></span> <span data-ttu-id="74f62-120">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="74f62-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="74f62-121">**說明**</span><span class="sxs-lookup"><span data-stu-id="74f62-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74f62-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="74f62-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74f62-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74f62-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74f62-124">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="74f62-124">A description of the object.</span></span> <span data-ttu-id="74f62-125">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="74f62-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="74f62-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="74f62-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74f62-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="74f62-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74f62-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74f62-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74f62-129">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="74f62-129">A display name for the object.</span></span> <span data-ttu-id="74f62-130">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="74f62-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="74f62-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="74f62-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74f62-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="74f62-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74f62-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74f62-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74f62-134">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="74f62-134">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="74f62-135">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="74f62-135">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="74f62-136">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="74f62-136">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="74f62-137">**ReplicaStorageLocation**</span><span class="sxs-lookup"><span data-stu-id="74f62-137">**ReplicaStorageLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74f62-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="74f62-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74f62-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="74f62-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74f62-140">將從 **AllowedPrimaryHostSystem** 儲存複寫檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="74f62-140">The location where replication files from the **AllowedPrimaryHostSystem** will be stored.</span></span>

</dd> <dt>

<span data-ttu-id="74f62-141">**TrustGroup**</span><span class="sxs-lookup"><span data-stu-id="74f62-141">**TrustGroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74f62-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="74f62-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74f62-143">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="74f62-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74f62-144">授權專案的信任組名。</span><span class="sxs-lookup"><span data-stu-id="74f62-144">The name of the trust group for the authorization entry.</span></span> <span data-ttu-id="74f62-145">這會識別群組在一起的多個授權專案。</span><span class="sxs-lookup"><span data-stu-id="74f62-145">This identifies the multiple authorization entries that are grouped together.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="74f62-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="74f62-146">Requirements</span></span>



| <span data-ttu-id="74f62-147">需求</span><span class="sxs-lookup"><span data-stu-id="74f62-147">Requirement</span></span> | <span data-ttu-id="74f62-148">值</span><span class="sxs-lookup"><span data-stu-id="74f62-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74f62-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74f62-149">Minimum supported client</span></span><br/> | <span data-ttu-id="74f62-150">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74f62-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="74f62-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74f62-151">Minimum supported server</span></span><br/> | <span data-ttu-id="74f62-152">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74f62-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="74f62-153">命名空間</span><span class="sxs-lookup"><span data-stu-id="74f62-153">Namespace</span></span><br/>                | <span data-ttu-id="74f62-154">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="74f62-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="74f62-155">MOF</span><span class="sxs-lookup"><span data-stu-id="74f62-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74f62-156"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="74f62-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="74f62-157">DLL</span><span class="sxs-lookup"><span data-stu-id="74f62-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74f62-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="74f62-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="74f62-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74f62-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74f62-160">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="74f62-160">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="74f62-161">**AddAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="74f62-161">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="74f62-162">**ModifyAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="74f62-162">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="74f62-163">**RemoveAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="74f62-163">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> </dl>

 

