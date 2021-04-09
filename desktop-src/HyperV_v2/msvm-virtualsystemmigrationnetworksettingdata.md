---
description: 代表虛擬系統移轉服務接聽傳入虛擬系統移轉的網路。
ms.assetid: 24458602-ff5c-45c2-8053-00315b59d3bb
title: Msvm_VirtualSystemMigrationNetworkSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationNetworkSettingData
- Msvm_VirtualSystemMigrationNetworkSettingData.InstanceID
- Msvm_VirtualSystemMigrationNetworkSettingData.Caption
- Msvm_VirtualSystemMigrationNetworkSettingData.Description
- Msvm_VirtualSystemMigrationNetworkSettingData.ElementName
- Msvm_VirtualSystemMigrationNetworkSettingData.SubnetNumber
- Msvm_VirtualSystemMigrationNetworkSettingData.PrefixLength
- Msvm_VirtualSystemMigrationNetworkSettingData.Metric
- Msvm_VirtualSystemMigrationNetworkSettingData.Tags
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4f7c24bb754148fa8ede12292f308164512af646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847761"
---
# <a name="msvm_virtualsystemmigrationnetworksettingdata-class"></a><span data-ttu-id="18b3a-103">Msvm \_ VirtualSystemMigrationNetworkSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="18b3a-103">Msvm\_VirtualSystemMigrationNetworkSettingData class</span></span>

<span data-ttu-id="18b3a-104">代表虛擬系統移轉服務接聽傳入虛擬系統移轉的網路。</span><span class="sxs-lookup"><span data-stu-id="18b3a-104">Represents the network on which the virtual system migration service is listening for incoming virtual system migration.</span></span>

<span data-ttu-id="18b3a-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="18b3a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="18b3a-106">語法</span><span class="sxs-lookup"><span data-stu-id="18b3a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationNetworkSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string SubnetNumber;
  uint8  PrefixLength;
  uint32 Metric;
  string Tags[];
};
```

## <a name="members"></a><span data-ttu-id="18b3a-107">成員</span><span class="sxs-lookup"><span data-stu-id="18b3a-107">Members</span></span>

<span data-ttu-id="18b3a-108">**Msvm \_ VirtualSystemMigrationNetworkSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="18b3a-108">The **Msvm\_VirtualSystemMigrationNetworkSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="18b3a-109">屬性</span><span class="sxs-lookup"><span data-stu-id="18b3a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18b3a-110">屬性</span><span class="sxs-lookup"><span data-stu-id="18b3a-110">Properties</span></span>

<span data-ttu-id="18b3a-111">**Msvm \_ VirtualSystemMigrationNetworkSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="18b3a-111">The **Msvm\_VirtualSystemMigrationNetworkSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18b3a-112">**標題**</span><span class="sxs-lookup"><span data-stu-id="18b3a-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b3a-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b3a-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b3a-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18b3a-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18b3a-115">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="18b3a-115">A short description of the object.</span></span> <span data-ttu-id="18b3a-116">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) 類別。</span><span class="sxs-lookup"><span data-stu-id="18b3a-116">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class.</span></span>

</dd> <dt>

<span data-ttu-id="18b3a-117">**說明**</span><span class="sxs-lookup"><span data-stu-id="18b3a-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b3a-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b3a-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b3a-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18b3a-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18b3a-120">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="18b3a-120">A description of the object.</span></span> <span data-ttu-id="18b3a-121">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="18b3a-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="18b3a-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="18b3a-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b3a-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b3a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b3a-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18b3a-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18b3a-125">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="18b3a-125">A display name for the object.</span></span> <span data-ttu-id="18b3a-126">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="18b3a-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="18b3a-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="18b3a-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b3a-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b3a-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b3a-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18b3a-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18b3a-130">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="18b3a-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="18b3a-131">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="18b3a-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="18b3a-132">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="18b3a-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="18b3a-133">**計量**</span><span class="sxs-lookup"><span data-stu-id="18b3a-133">**Metric**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b3a-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="18b3a-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18b3a-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18b3a-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18b3a-136">此網路用於遷移的優先順序度量。</span><span class="sxs-lookup"><span data-stu-id="18b3a-136">The priority metric of this network for migration.</span></span> <span data-ttu-id="18b3a-137">較低的值會在優先順序較高。</span><span class="sxs-lookup"><span data-stu-id="18b3a-137">Lower values are higher in priority.</span></span>

</dd> <dt>

<span data-ttu-id="18b3a-138">**PrefixLength**</span><span class="sxs-lookup"><span data-stu-id="18b3a-138">**PrefixLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b3a-139">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="18b3a-139">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="18b3a-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18b3a-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18b3a-141">遷移網路子網前置長度。</span><span class="sxs-lookup"><span data-stu-id="18b3a-141">The migration network subnet prefix length.</span></span>

</dd> <dt>

<span data-ttu-id="18b3a-142">**SubnetNumber**</span><span class="sxs-lookup"><span data-stu-id="18b3a-142">**SubnetNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b3a-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18b3a-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18b3a-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18b3a-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18b3a-145">遷移網路子網號碼。</span><span class="sxs-lookup"><span data-stu-id="18b3a-145">The migration network subnet number.</span></span>

</dd> <dt>

<span data-ttu-id="18b3a-146">**Tags** (標籤)</span><span class="sxs-lookup"><span data-stu-id="18b3a-146">**Tags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18b3a-147">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="18b3a-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="18b3a-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18b3a-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18b3a-149">標記的陣列，代表哪個管理系統已為虛擬系統移轉服務設定此網路。</span><span class="sxs-lookup"><span data-stu-id="18b3a-149">An array of tags to represent which management system has set this network for virtual system migration service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18b3a-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="18b3a-150">Requirements</span></span>



| <span data-ttu-id="18b3a-151">需求</span><span class="sxs-lookup"><span data-stu-id="18b3a-151">Requirement</span></span> | <span data-ttu-id="18b3a-152">值</span><span class="sxs-lookup"><span data-stu-id="18b3a-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18b3a-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18b3a-153">Minimum supported client</span></span><br/> | <span data-ttu-id="18b3a-154">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18b3a-154">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="18b3a-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18b3a-155">Minimum supported server</span></span><br/> | <span data-ttu-id="18b3a-156">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18b3a-156">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="18b3a-157">命名空間</span><span class="sxs-lookup"><span data-stu-id="18b3a-157">Namespace</span></span><br/>                | <span data-ttu-id="18b3a-158">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="18b3a-158">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="18b3a-159">MOF</span><span class="sxs-lookup"><span data-stu-id="18b3a-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18b3a-160"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="18b3a-160"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="18b3a-161">DLL</span><span class="sxs-lookup"><span data-stu-id="18b3a-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18b3a-162"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="18b3a-162"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="18b3a-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18b3a-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18b3a-164">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="18b3a-164">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="18b3a-165">**ModifyNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="18b3a-165">**ModifyNetworkSettings**</span></span>](modifynetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

