---
description: 代表虛擬機器的磁片合併設定的設定狀態。
ms.assetid: b4c0afeb-ce37-4eec-8aba-0d74115c463f
title: Msvm_DiskMergeSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskMergeSettingData
- Msvm_DiskMergeSettingData.InstanceID
- Msvm_DiskMergeSettingData.Caption
- Msvm_DiskMergeSettingData.Description
- Msvm_DiskMergeSettingData.ElementName
- Msvm_DiskMergeSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fe702c382fb0636579a8ab1355bfd1299657b214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979332"
---
# <a name="msvm_diskmergesettingdata-class"></a><span data-ttu-id="12b27-103">Msvm \_ DiskMergeSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="12b27-103">Msvm\_DiskMergeSettingData class</span></span>

<span data-ttu-id="12b27-104">代表虛擬機器的磁片合併設定的設定狀態。</span><span class="sxs-lookup"><span data-stu-id="12b27-104">Represents the configuration state of the disk merge settings for a virtual machine.</span></span>

<span data-ttu-id="12b27-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="12b27-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="12b27-106">語法</span><span class="sxs-lookup"><span data-stu-id="12b27-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DiskMergeSettingData : CIM_SettingData
{
  string InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string Caption = "Disk Merge Setting Data";
  string Description = "Microsoft Disk Merge Setting Data";
  string ElementName = "Disk Merge Setting Data";
  uint32 EnabledState = 1;
};
```

## <a name="members"></a><span data-ttu-id="12b27-107">成員</span><span class="sxs-lookup"><span data-stu-id="12b27-107">Members</span></span>

<span data-ttu-id="12b27-108">**Msvm \_ DiskMergeSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="12b27-108">The **Msvm\_DiskMergeSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="12b27-109">屬性</span><span class="sxs-lookup"><span data-stu-id="12b27-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="12b27-110">屬性</span><span class="sxs-lookup"><span data-stu-id="12b27-110">Properties</span></span>

<span data-ttu-id="12b27-111">**Msvm \_ DiskMergeSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="12b27-111">The **Msvm\_DiskMergeSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="12b27-112">**標題**</span><span class="sxs-lookup"><span data-stu-id="12b27-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12b27-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="12b27-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12b27-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="12b27-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12b27-115">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="12b27-115">A short description of the object.</span></span> <span data-ttu-id="12b27-116">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) 類別，一律設定為「磁片合併設定資料」。</span><span class="sxs-lookup"><span data-stu-id="12b27-116">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Disk Merge Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="12b27-117">**說明**</span><span class="sxs-lookup"><span data-stu-id="12b27-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12b27-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="12b27-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12b27-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="12b27-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12b27-120">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="12b27-120">A description of the object.</span></span> <span data-ttu-id="12b27-121">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「Microsoft 磁片合併設定資料」。</span><span class="sxs-lookup"><span data-stu-id="12b27-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Disk Merge Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="12b27-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="12b27-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12b27-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="12b27-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12b27-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="12b27-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12b27-125">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="12b27-125">A display name for the object.</span></span> <span data-ttu-id="12b27-126">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))，一律設為「磁片合併設定資料」。</span><span class="sxs-lookup"><span data-stu-id="12b27-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Disk Merge Setting Data".</span></span> <span data-ttu-id="12b27-127">變更這個屬性將會變更相關聯之 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)衍生的 **ElementName** 屬性。</span><span class="sxs-lookup"><span data-stu-id="12b27-127">Changing this property will change the **ElementName** property of the associated [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) derivative.</span></span>

<span data-ttu-id="12b27-128">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="12b27-128">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="12b27-129">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="12b27-129">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12b27-130">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="12b27-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="12b27-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="12b27-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12b27-132">指定磁片合併功能的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="12b27-132">Specifies the enabled state of the disk merge functionality.</span></span>

<dt>

<span id="Temporarily_disabled"></span><span id="temporarily_disabled"></span><span id="TEMPORARILY_DISABLED"></span>

<span data-ttu-id="12b27-133">**暫時停用** (0) </span><span class="sxs-lookup"><span data-stu-id="12b27-133">**Temporarily disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="12b27-134">**已啟用** (1) </span><span class="sxs-lookup"><span data-stu-id="12b27-134">**Enabled** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="12b27-135">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="12b27-135">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12b27-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="12b27-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12b27-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="12b27-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12b27-138">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="12b27-138">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="12b27-139">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="12b27-139">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="12b27-140">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) ，一律設定為 "Microsoft：*GUID* \\ *DeviceSpecificData*"。</span><span class="sxs-lookup"><span data-stu-id="12b27-140">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12b27-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="12b27-141">Requirements</span></span>



| <span data-ttu-id="12b27-142">需求</span><span class="sxs-lookup"><span data-stu-id="12b27-142">Requirement</span></span> | <span data-ttu-id="12b27-143">值</span><span class="sxs-lookup"><span data-stu-id="12b27-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12b27-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="12b27-144">Minimum supported client</span></span><br/> | <span data-ttu-id="12b27-145">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12b27-145">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="12b27-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="12b27-146">Minimum supported server</span></span><br/> | <span data-ttu-id="12b27-147">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12b27-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="12b27-148">命名空間</span><span class="sxs-lookup"><span data-stu-id="12b27-148">Namespace</span></span><br/>                | <span data-ttu-id="12b27-149">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="12b27-149">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="12b27-150">MOF</span><span class="sxs-lookup"><span data-stu-id="12b27-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12b27-151"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="12b27-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="12b27-152">DLL</span><span class="sxs-lookup"><span data-stu-id="12b27-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12b27-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="12b27-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

