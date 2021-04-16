---
description: 代表 TPM 裝置設定的狀態。
ms.assetid: 948ccb47-3626-48f1-b18f-ef1d05978b21
title: Msvm_TPMSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TPMSettingData
- Msvm_TPMSettingData.Shielded
- Msvm_TPMSettingData.DataProtected
- Msvm_TPMSettingData.EnabledState
- Msvm_TPMSettingData.KeyProtector
- Msvm_TPMSettingData.LastKnownGoodKeyProtector
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8a14f50f01212129ed34cc7e45ee28facbdb991f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512440"
---
# <a name="msvm_tpmsettingdata-class"></a><span data-ttu-id="e490a-103">Msvm \_ TPMSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="e490a-103">Msvm\_TPMSettingData class</span></span>

<span data-ttu-id="e490a-104">代表 TPM 裝置設定的狀態。</span><span class="sxs-lookup"><span data-stu-id="e490a-104">Represents the configured state of the TPM device.</span></span>

<span data-ttu-id="e490a-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e490a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e490a-106">語法</span><span class="sxs-lookup"><span data-stu-id="e490a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TPMSettingData : CIM_ResourceAllocationSettingData
{
  boolean Shielded = FALSE;
  boolean DataProtected = FALSE;
  uint16  EnabledState = 3;
  uint8   KeyProtector[];
  uint8   LastKnownGoodKeyProtector[];
};
```

## <a name="members"></a><span data-ttu-id="e490a-107">成員</span><span class="sxs-lookup"><span data-stu-id="e490a-107">Members</span></span>

<span data-ttu-id="e490a-108">**Msvm \_ TPMSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e490a-108">The **Msvm\_TPMSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="e490a-109">屬性</span><span class="sxs-lookup"><span data-stu-id="e490a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e490a-110">屬性</span><span class="sxs-lookup"><span data-stu-id="e490a-110">Properties</span></span>

<span data-ttu-id="e490a-111">**Msvm \_ TPMSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e490a-111">The **Msvm\_TPMSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e490a-112">**DataProtected**</span><span class="sxs-lookup"><span data-stu-id="e490a-112">**DataProtected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e490a-113">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e490a-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e490a-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e490a-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e490a-115">限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e490a-115">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e490a-116">**true** 表示設定原則來保護 VM 的資料;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="e490a-116">**true** to set a policy to protect a VM's data; otherwise, **false**.</span></span> <span data-ttu-id="e490a-117">新建立的 TPM 已停用，因此初始資料保護狀態為 **false**。</span><span class="sxs-lookup"><span data-stu-id="e490a-117">A newly created TPM is disabled, so the initial data protection state is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="e490a-118">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="e490a-118">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e490a-119">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e490a-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e490a-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e490a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e490a-121">限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e490a-121">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e490a-122">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="e490a-122">The enabled and disabled states of an element.</span></span> <span data-ttu-id="e490a-123">預設值為 **Disabled**。</span><span class="sxs-lookup"><span data-stu-id="e490a-123">The default value is **Disabled**.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e490a-124">**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="e490a-124">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e490a-125">**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="e490a-125">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e490a-126">**KeyProtector**</span><span class="sxs-lookup"><span data-stu-id="e490a-126">**KeyProtector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e490a-127">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="e490a-127">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e490a-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e490a-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e490a-129">限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)、 **OctetString**</span><span class="sxs-lookup"><span data-stu-id="e490a-129">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**</span></span>
</dt> </dl>

<span data-ttu-id="e490a-130">主機守護者服務用戶端的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="e490a-130">The key protector from Host Guardian Service client.</span></span>

</dd> <dt>

<span data-ttu-id="e490a-131">**LastKnownGoodKeyProtector**</span><span class="sxs-lookup"><span data-stu-id="e490a-131">**LastKnownGoodKeyProtector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e490a-132">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="e490a-132">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e490a-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e490a-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e490a-134">限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)、 **OctetString**</span><span class="sxs-lookup"><span data-stu-id="e490a-134">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**</span></span>
</dt> </dl>

<span data-ttu-id="e490a-135">最後一個已知良好的金鑰保護裝置在上一次 VM 開機中成功加密 TPM 裝置狀態。</span><span class="sxs-lookup"><span data-stu-id="e490a-135">The last known good key protector successfully encrypted TPM device state in the last VM boot.</span></span>

<span data-ttu-id="e490a-136">針對 WMI 用戶端，此屬性是唯讀的，而且只能由 VM TPM 裝置進行修改。</span><span class="sxs-lookup"><span data-stu-id="e490a-136">This property is read-only for the WMI client, and can only be modified by the VM TPM device.</span></span>

</dd> <dt>

<span data-ttu-id="e490a-137">**受防護**</span><span class="sxs-lookup"><span data-stu-id="e490a-137">**Shielded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e490a-138">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e490a-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e490a-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e490a-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e490a-140">限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e490a-140">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e490a-141">**true** 表示定義防護虛擬機器的原則;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="e490a-141">**true** to define a policy that shields a virtual machine; otherwise, **false**.</span></span> <span data-ttu-id="e490a-142">新建立的 TPM 已停用，因此初始防護狀態為 **false**。</span><span class="sxs-lookup"><span data-stu-id="e490a-142">A newly created TPM is disabled, so the initial shielding state is **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e490a-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="e490a-143">Requirements</span></span>



| <span data-ttu-id="e490a-144">需求</span><span class="sxs-lookup"><span data-stu-id="e490a-144">Requirement</span></span> | <span data-ttu-id="e490a-145">值</span><span class="sxs-lookup"><span data-stu-id="e490a-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e490a-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e490a-146">Minimum supported client</span></span><br/> | <span data-ttu-id="e490a-147">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e490a-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e490a-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e490a-148">Minimum supported server</span></span><br/> | <span data-ttu-id="e490a-149">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e490a-149">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e490a-150">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e490a-150">End of client support</span></span><br/>    | <span data-ttu-id="e490a-151">Windows 10</span><span class="sxs-lookup"><span data-stu-id="e490a-151">Windows 10</span></span><br/>                                                                                   |
| <span data-ttu-id="e490a-152">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="e490a-152">End of server support</span></span><br/>    | <span data-ttu-id="e490a-153">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e490a-153">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e490a-154">命名空間</span><span class="sxs-lookup"><span data-stu-id="e490a-154">Namespace</span></span><br/>                | <span data-ttu-id="e490a-155">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="e490a-155">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e490a-156">MOF</span><span class="sxs-lookup"><span data-stu-id="e490a-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e490a-157"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e490a-157"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e490a-158">DLL</span><span class="sxs-lookup"><span data-stu-id="e490a-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e490a-159"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e490a-159"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e490a-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e490a-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e490a-161">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="e490a-161">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

