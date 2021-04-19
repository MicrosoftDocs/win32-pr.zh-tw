---
description: 表示之安全性設定的設定狀態。
ms.assetid: c57ab966-591e-4dd9-87be-0d2b81611d5d
title: Msvm_SecuritySettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecuritySettingData
- Msvm_SecuritySettingData.TpmEnabled
- Msvm_SecuritySettingData.KsdEnabled
- Msvm_SecuritySettingData.ShieldingRequested
- Msvm_SecuritySettingData.DataProtectionRequested
- Msvm_SecuritySettingData.EncryptStateAndVmMigrationTraffic
- Msvm_SecuritySettingData.VirtualizationBasedSecurityOptOut
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b7125e06ad4ce33e70a8cf84b24933e7390e7a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986960"
---
# <a name="msvm_securitysettingdata-class"></a><span data-ttu-id="3603a-103">Msvm \_ SecuritySettingData 類別</span><span class="sxs-lookup"><span data-stu-id="3603a-103">Msvm\_SecuritySettingData class</span></span>

<span data-ttu-id="3603a-104">代表虛擬機器之安全性設定的設定狀態。</span><span class="sxs-lookup"><span data-stu-id="3603a-104">Represents the configured state of the security settings for a virtual machine.</span></span>

<span data-ttu-id="3603a-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3603a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3603a-106">語法</span><span class="sxs-lookup"><span data-stu-id="3603a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecuritySettingData : CIM_SettingData
{
  boolean TpmEnabled;
  boolean KsdEnabled;
  boolean ShieldingRequested;
  boolean DataProtectionRequested;
  boolean EncryptStateAndVmMigrationTraffic;
  boolean VirtualizationBasedSecurityOptOut;
};
```

## <a name="members"></a><span data-ttu-id="3603a-107">成員</span><span class="sxs-lookup"><span data-stu-id="3603a-107">Members</span></span>

<span data-ttu-id="3603a-108">**Msvm \_ SecuritySettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3603a-108">The **Msvm\_SecuritySettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="3603a-109">屬性</span><span class="sxs-lookup"><span data-stu-id="3603a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3603a-110">屬性</span><span class="sxs-lookup"><span data-stu-id="3603a-110">Properties</span></span>

<span data-ttu-id="3603a-111">**Msvm \_ SecuritySettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3603a-111">The **Msvm\_SecuritySettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3603a-112">**DataProtectionRequested**</span><span class="sxs-lookup"><span data-stu-id="3603a-112">**DataProtectionRequested**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3603a-113">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3603a-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3603a-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3603a-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3603a-115">限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3603a-115">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3603a-116">**true** 表示要求 VM 的資料保護;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="3603a-116">**true** to request data protection for a VM; otherwise, **false**.</span></span> <span data-ttu-id="3603a-117">預設值為 **false**。</span><span class="sxs-lookup"><span data-stu-id="3603a-117">The default value is **false.**</span></span>

</dd> <dt>

<span data-ttu-id="3603a-118">**EncryptStateAndVmMigrationTraffic**</span><span class="sxs-lookup"><span data-stu-id="3603a-118">**EncryptStateAndVmMigrationTraffic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3603a-119">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3603a-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3603a-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3603a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3603a-121">限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3603a-121">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3603a-122">**true** 表示已加密 VM 的狀態和遷移流量;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="3603a-122">**true** to have the state and migration traffic of a VM encrypted; otherwise, **false**.</span></span> <span data-ttu-id="3603a-123">新建立之 VM 的預設值為 **false**。</span><span class="sxs-lookup"><span data-stu-id="3603a-123">The default value for a newly-created VM is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="3603a-124">**KsdEnabled**</span><span class="sxs-lookup"><span data-stu-id="3603a-124">**KsdEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3603a-125">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3603a-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3603a-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3603a-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3603a-127">限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3603a-127">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3603a-128">**true** 表示為此虛擬機器啟用金鑰存放裝置 (KSD) ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="3603a-128">**true** to enable a key storage device (KSD) for this virtual machine; otherwise, **false**.</span></span> <span data-ttu-id="3603a-129">新建立的 VM 具有停用的 KSD。</span><span class="sxs-lookup"><span data-stu-id="3603a-129">A newly-created VM has a disable KSD.</span></span>

</dd> <dt>

<span data-ttu-id="3603a-130">**ShieldingRequested**</span><span class="sxs-lookup"><span data-stu-id="3603a-130">**ShieldingRequested**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3603a-131">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3603a-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3603a-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3603a-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3603a-133">限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3603a-133">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3603a-134">**true** 表示要求防護 VM;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="3603a-134">**true** to request shielding for a VM; otherwise, **false**.</span></span> <span data-ttu-id="3603a-135">新建立的 VM 具有要求的初始防護狀態 **false**。</span><span class="sxs-lookup"><span data-stu-id="3603a-135">A newly-created VM has an initial shielding requested state of **false**.</span></span>

</dd> <dt>

<span data-ttu-id="3603a-136">**TpmEnabled**</span><span class="sxs-lookup"><span data-stu-id="3603a-136">**TpmEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3603a-137">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3603a-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3603a-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3603a-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3603a-139">限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3603a-139">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3603a-140">**true** 表示啟用受信任的平臺 nodule (此虛擬機器的 TPM) ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="3603a-140">**true** to enable a trusted platform nodule (TPM) for this virtual machine; otherwise, **false**.</span></span> <span data-ttu-id="3603a-141">新建立的 VM 具有停用 TPM。</span><span class="sxs-lookup"><span data-stu-id="3603a-141">A newly-created VM has a disable TPM.</span></span>

</dd> <dt>

<span data-ttu-id="3603a-142">**VirtualizationBasedSecurityOptOut**</span><span class="sxs-lookup"><span data-stu-id="3603a-142">**VirtualizationBasedSecurityOptOut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3603a-143">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3603a-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3603a-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3603a-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3603a-145">限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3603a-145">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3603a-146">**true** 表示不提供 VM 虛擬化型安全性;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="3603a-146">**true** to not offer a VM virtualization-based security; otherwise, **false**.</span></span> <span data-ttu-id="3603a-147">新建立的 VM 退出狀態預設設定為 **false**。</span><span class="sxs-lookup"><span data-stu-id="3603a-147">The default setting for a newly-crated VM's opt-out state is **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3603a-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="3603a-148">Requirements</span></span>



| <span data-ttu-id="3603a-149">需求</span><span class="sxs-lookup"><span data-stu-id="3603a-149">Requirement</span></span> | <span data-ttu-id="3603a-150">值</span><span class="sxs-lookup"><span data-stu-id="3603a-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3603a-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3603a-151">Minimum supported client</span></span><br/> | <span data-ttu-id="3603a-152">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3603a-152">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3603a-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3603a-153">Minimum supported server</span></span><br/> | <span data-ttu-id="3603a-154">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3603a-154">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3603a-155">命名空間</span><span class="sxs-lookup"><span data-stu-id="3603a-155">Namespace</span></span><br/>                | <span data-ttu-id="3603a-156">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="3603a-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3603a-157">MOF</span><span class="sxs-lookup"><span data-stu-id="3603a-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3603a-158"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="3603a-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3603a-159">DLL</span><span class="sxs-lookup"><span data-stu-id="3603a-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3603a-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3603a-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3603a-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3603a-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3603a-162">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="3603a-162">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

