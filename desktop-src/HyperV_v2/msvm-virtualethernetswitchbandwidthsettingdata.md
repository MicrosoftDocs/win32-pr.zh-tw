---
description: 代表虛擬交換器的頻寬設定。
ms.assetid: bc6f8cd3-f74a-4f4a-9ffe-a88def3966d9
title: Msvm_VirtualEthernetSwitchBandwidthSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchBandwidthSettingData
- Msvm_VirtualEthernetSwitchBandwidthSettingData.InstanceID
- Msvm_VirtualEthernetSwitchBandwidthSettingData.Caption
- Msvm_VirtualEthernetSwitchBandwidthSettingData.Description
- Msvm_VirtualEthernetSwitchBandwidthSettingData.ElementName
- Msvm_VirtualEthernetSwitchBandwidthSettingData.DefaultFlowReservation
- Msvm_VirtualEthernetSwitchBandwidthSettingData.DefaultFlowWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ec94409366761ee208d3e8a6af59a4d07527d82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985212"
---
# <a name="msvm_virtualethernetswitchbandwidthsettingdata-class"></a><span data-ttu-id="8e0b6-103">Msvm \_ VirtualEthernetSwitchBandwidthSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="8e0b6-103">Msvm\_VirtualEthernetSwitchBandwidthSettingData class</span></span>

<span data-ttu-id="8e0b6-104">代表虛擬交換器的頻寬設定。</span><span class="sxs-lookup"><span data-stu-id="8e0b6-104">Represents the bandwidth settings for a virtual switch.</span></span>

<span data-ttu-id="8e0b6-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8e0b6-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e0b6-106">語法</span><span class="sxs-lookup"><span data-stu-id="8e0b6-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("3EB2B8E8-4ABF-4DBF-9071-16DD47481FBE"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Bandwidth Settings"), AMENDMENT]
class Msvm_VirtualEthernetSwitchBandwidthSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  string InstanceID = "Microsoft:Definition\GUID\Default";
  string Caption = "Ethernet Switch Bandwidth Settings";
  string Description = "Represents the switch bandwidth settings.";
  string ElementName = "Ethernet Switch Bandwidth Settings";
  UINT64 DefaultFlowReservation = 0;
  UINT64 DefaultFlowWeight = 0;
};
```

## <a name="members"></a><span data-ttu-id="8e0b6-107">成員</span><span class="sxs-lookup"><span data-stu-id="8e0b6-107">Members</span></span>

<span data-ttu-id="8e0b6-108">**Msvm \_ VirtualEthernetSwitchBandwidthSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8e0b6-108">The **Msvm\_VirtualEthernetSwitchBandwidthSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="8e0b6-109">屬性</span><span class="sxs-lookup"><span data-stu-id="8e0b6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8e0b6-110">屬性</span><span class="sxs-lookup"><span data-stu-id="8e0b6-110">Properties</span></span>

<span data-ttu-id="8e0b6-111">**Msvm \_ VirtualEthernetSwitchBandwidthSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8e0b6-111">The **Msvm\_VirtualEthernetSwitchBandwidthSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8e0b6-112">**標題**</span><span class="sxs-lookup"><span data-stu-id="8e0b6-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e0b6-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e0b6-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e0b6-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e0b6-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e0b6-115">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="8e0b6-115">A short description of the object.</span></span> <span data-ttu-id="8e0b6-116">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) 類別，一律設定為「乙太網路交換器頻寬設定」。</span><span class="sxs-lookup"><span data-stu-id="8e0b6-116">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Ethernet Switch Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="8e0b6-117">**DefaultFlowReservation**</span><span class="sxs-lookup"><span data-stu-id="8e0b6-117">**DefaultFlowReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e0b6-118">資料類型： **UINT64**</span><span class="sxs-lookup"><span data-stu-id="8e0b6-118">Data type: **UINT64**</span></span>
</dt> <dt>

<span data-ttu-id="8e0b6-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8e0b6-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8e0b6-120">限定詞： **WmiDataId** (1) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="8e0b6-120">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8e0b6-121">指定基礎介面卡上未分類流程的絕對頻寬保留。</span><span class="sxs-lookup"><span data-stu-id="8e0b6-121">Specifies the absolute bandwidth reservation for unclassified flows on the underlying adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8e0b6-122">**DefaultFlowWeight**</span><span class="sxs-lookup"><span data-stu-id="8e0b6-122">**DefaultFlowWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e0b6-123">資料類型： **UINT64**</span><span class="sxs-lookup"><span data-stu-id="8e0b6-123">Data type: **UINT64**</span></span>
</dt> <dt>

<span data-ttu-id="8e0b6-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8e0b6-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8e0b6-125">限定詞： **WmiDataId** (2) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="8e0b6-125">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="8e0b6-126">指定基礎介面卡上未分類流程的頻寬保留量。</span><span class="sxs-lookup"><span data-stu-id="8e0b6-126">Specifies the bandwidth reservation in weight for unclassified flows on the underlying adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8e0b6-127">**說明**</span><span class="sxs-lookup"><span data-stu-id="8e0b6-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e0b6-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e0b6-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e0b6-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e0b6-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e0b6-130">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="8e0b6-130">A description of the object.</span></span> <span data-ttu-id="8e0b6-131">這個屬性會繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，而且一律會設定為「代表交換器頻寬設定」。</span><span class="sxs-lookup"><span data-stu-id="8e0b6-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the switch bandwidth settings.".</span></span>

</dd> <dt>

<span data-ttu-id="8e0b6-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8e0b6-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e0b6-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e0b6-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e0b6-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e0b6-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e0b6-135">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="8e0b6-135">A display name for the object.</span></span> <span data-ttu-id="8e0b6-136">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))，一律設定為「乙太網路交換器頻寬設定」。</span><span class="sxs-lookup"><span data-stu-id="8e0b6-136">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Ethernet Switch Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="8e0b6-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8e0b6-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e0b6-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e0b6-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e0b6-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e0b6-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e0b6-140">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="8e0b6-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8e0b6-141">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="8e0b6-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8e0b6-142">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) ，一律設定為 "Microsoft： Definition \\ *GUID* \\ Default"。</span><span class="sxs-lookup"><span data-stu-id="8e0b6-142">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:Definition\\*GUID*\\Default".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8e0b6-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e0b6-143">Requirements</span></span>



| <span data-ttu-id="8e0b6-144">需求</span><span class="sxs-lookup"><span data-stu-id="8e0b6-144">Requirement</span></span> | <span data-ttu-id="8e0b6-145">值</span><span class="sxs-lookup"><span data-stu-id="8e0b6-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e0b6-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8e0b6-146">Minimum supported client</span></span><br/> | <span data-ttu-id="8e0b6-147">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8e0b6-147">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8e0b6-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8e0b6-148">Minimum supported server</span></span><br/> | <span data-ttu-id="8e0b6-149">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8e0b6-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8e0b6-150">命名空間</span><span class="sxs-lookup"><span data-stu-id="8e0b6-150">Namespace</span></span><br/>                | <span data-ttu-id="8e0b6-151">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="8e0b6-151">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8e0b6-152">MOF</span><span class="sxs-lookup"><span data-stu-id="8e0b6-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e0b6-153"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="8e0b6-153"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e0b6-154">DLL</span><span class="sxs-lookup"><span data-stu-id="8e0b6-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e0b6-155"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8e0b6-155"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

