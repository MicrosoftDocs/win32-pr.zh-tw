---
description: 表示埠頻寬設定。
ms.assetid: 62a42c4c-8ea1-47c6-8ae6-e9252f2ed0e4
title: Msvm_EthernetSwitchPortBandwidthSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortBandwidthSettingData
- Msvm_EthernetSwitchPortBandwidthSettingData.InstanceID
- Msvm_EthernetSwitchPortBandwidthSettingData.Caption
- Msvm_EthernetSwitchPortBandwidthSettingData.Description
- Msvm_EthernetSwitchPortBandwidthSettingData.ElementName
- Msvm_EthernetSwitchPortBandwidthSettingData.Reservation
- Msvm_EthernetSwitchPortBandwidthSettingData.Weight
- Msvm_EthernetSwitchPortBandwidthSettingData.Limit
- Msvm_EthernetSwitchPortBandwidthSettingData.BurstLimit
- Msvm_EthernetSwitchPortBandwidthSettingData.BurstSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 932207a8157e34c5f42894c31efa78090a6a80f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980003"
---
# <a name="msvm_ethernetswitchportbandwidthsettingdata-class"></a><span data-ttu-id="a1d78-103">Msvm \_ EthernetSwitchPortBandwidthSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="a1d78-103">Msvm\_EthernetSwitchPortBandwidthSettingData class</span></span>

<span data-ttu-id="a1d78-104">表示埠頻寬設定。</span><span class="sxs-lookup"><span data-stu-id="a1d78-104">Represents the port bandwidth settings.</span></span>

<span data-ttu-id="a1d78-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a1d78-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1d78-106">語法</span><span class="sxs-lookup"><span data-stu-id="a1d78-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("24AD3CE1-69BD-4978-B2AC-DAAD389D699C"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Bandwidth Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortBandwidthSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Bandwidth Settings";
  string Description = "Represents the port bandwidth settings.";
  string ElementName = "Ethernet Switch Port Bandwidth Settings";
  uint64 Reservation = 0;
  uint64 Weight = 0;
  uint64 Limit = 0;
  uint64 BurstLimit = 0;
  uint64 BurstSize = 0;
};
```

## <a name="members"></a><span data-ttu-id="a1d78-107">成員</span><span class="sxs-lookup"><span data-stu-id="a1d78-107">Members</span></span>

<span data-ttu-id="a1d78-108">**Msvm \_ EthernetSwitchPortBandwidthSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a1d78-108">The **Msvm\_EthernetSwitchPortBandwidthSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="a1d78-109">屬性</span><span class="sxs-lookup"><span data-stu-id="a1d78-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a1d78-110">屬性</span><span class="sxs-lookup"><span data-stu-id="a1d78-110">Properties</span></span>

<span data-ttu-id="a1d78-111">**Msvm \_ EthernetSwitchPortBandwidthSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a1d78-111">The **Msvm\_EthernetSwitchPortBandwidthSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a1d78-112">**BurstLimit**</span><span class="sxs-lookup"><span data-stu-id="a1d78-112">**BurstLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1d78-113">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="a1d78-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a1d78-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a1d78-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a1d78-115">限定詞： **WmiDataId** (4) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="a1d78-115">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="a1d78-116">在高載期間從埠允許的尖峰頻寬。</span><span class="sxs-lookup"><span data-stu-id="a1d78-116">The peak bandwidth allowed from the port during bursts.</span></span>

</dd> <dt>

<span data-ttu-id="a1d78-117">**BurstSize**</span><span class="sxs-lookup"><span data-stu-id="a1d78-117">**BurstSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1d78-118">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="a1d78-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a1d78-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a1d78-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a1d78-120">限定詞： **WmiDataId** (5) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="a1d78-120">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="a1d78-121">允許的高載大小上限。</span><span class="sxs-lookup"><span data-stu-id="a1d78-121">The maximum burst size allowed.</span></span>

</dd> <dt>

<span data-ttu-id="a1d78-122">**標題**</span><span class="sxs-lookup"><span data-stu-id="a1d78-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1d78-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a1d78-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1d78-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1d78-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1d78-125">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="a1d78-125">A short description of the object.</span></span> <span data-ttu-id="a1d78-126">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器埠頻寬設定」。</span><span class="sxs-lookup"><span data-stu-id="a1d78-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="a1d78-127">**說明**</span><span class="sxs-lookup"><span data-stu-id="a1d78-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1d78-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a1d78-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1d78-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1d78-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1d78-130">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="a1d78-130">A description of the object.</span></span> <span data-ttu-id="a1d78-131">這個屬性會繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，而且一律會設定為「代表埠頻寬設定」。</span><span class="sxs-lookup"><span data-stu-id="a1d78-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port bandwidth settings.".</span></span>

</dd> <dt>

<span data-ttu-id="a1d78-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a1d78-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1d78-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a1d78-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1d78-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1d78-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1d78-135">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a1d78-135">A display name for the object.</span></span> <span data-ttu-id="a1d78-136">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器埠頻寬設定」。</span><span class="sxs-lookup"><span data-stu-id="a1d78-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="a1d78-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a1d78-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1d78-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a1d78-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1d78-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1d78-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1d78-140">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="a1d78-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a1d78-141">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="a1d78-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a1d78-142">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="a1d78-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a1d78-143">**限制**</span><span class="sxs-lookup"><span data-stu-id="a1d78-143">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1d78-144">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="a1d78-144">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a1d78-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a1d78-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a1d78-146">限定詞： **WmiDataId** (3) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="a1d78-146">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="a1d78-147">埠允許的頻寬限制。</span><span class="sxs-lookup"><span data-stu-id="a1d78-147">The bandwidth limit allowed for the port.</span></span>

</dd> <dt>

<span data-ttu-id="a1d78-148">**保留容量**</span><span class="sxs-lookup"><span data-stu-id="a1d78-148">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1d78-149">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="a1d78-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a1d78-150">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a1d78-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a1d78-151">限定詞： **WmiDataId** (1) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="a1d78-151">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="a1d78-152">保證埠的最小絕對頻寬。</span><span class="sxs-lookup"><span data-stu-id="a1d78-152">The minimum absolute bandwidth guaranteed for the port.</span></span>

</dd> <dt>

<span data-ttu-id="a1d78-153">**Weight**</span><span class="sxs-lookup"><span data-stu-id="a1d78-153">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1d78-154">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="a1d78-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a1d78-155">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a1d78-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a1d78-156">限定詞： **WmiDataId** (2) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="a1d78-156">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="a1d78-157">針對埠保證的最小頻寬（加權）。</span><span class="sxs-lookup"><span data-stu-id="a1d78-157">The minimum bandwidth in weight guaranteed for the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1d78-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1d78-158">Requirements</span></span>



| <span data-ttu-id="a1d78-159">需求</span><span class="sxs-lookup"><span data-stu-id="a1d78-159">Requirement</span></span> | <span data-ttu-id="a1d78-160">值</span><span class="sxs-lookup"><span data-stu-id="a1d78-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1d78-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a1d78-161">Minimum supported client</span></span><br/> | <span data-ttu-id="a1d78-162">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a1d78-162">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a1d78-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a1d78-163">Minimum supported server</span></span><br/> | <span data-ttu-id="a1d78-164">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a1d78-164">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a1d78-165">命名空間</span><span class="sxs-lookup"><span data-stu-id="a1d78-165">Namespace</span></span><br/>                | <span data-ttu-id="a1d78-166">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="a1d78-166">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a1d78-167">MOF</span><span class="sxs-lookup"><span data-stu-id="a1d78-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a1d78-168"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a1d78-168"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a1d78-169">DLL</span><span class="sxs-lookup"><span data-stu-id="a1d78-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1d78-170"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a1d78-170"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

