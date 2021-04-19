---
description: 定義用戶端可針對乙太網路交換器功能探索預設設定之有效範圍的方法。
ms.assetid: 84ae7656-2cc4-4ca7-b4ae-95d9905c9aad
title: Msvm_EthernetSwitchFeatureCapabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchFeatureCapabilities
- Msvm_EthernetSwitchFeatureCapabilities.InstanceID
- Msvm_EthernetSwitchFeatureCapabilities.Caption
- Msvm_EthernetSwitchFeatureCapabilities.Description
- Msvm_EthernetSwitchFeatureCapabilities.ElementName
- Msvm_EthernetSwitchFeatureCapabilities.FeatureId
- Msvm_EthernetSwitchFeatureCapabilities.Applicability
- Msvm_EthernetSwitchFeatureCapabilities.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ba145ca6a43a2031a676e565f38210dc6771f40e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000497"
---
# <a name="msvm_ethernetswitchfeaturecapabilities-class"></a><span data-ttu-id="26a92-103">Msvm \_ EthernetSwitchFeatureCapabilities 類別</span><span class="sxs-lookup"><span data-stu-id="26a92-103">Msvm\_EthernetSwitchFeatureCapabilities class</span></span>

<span data-ttu-id="26a92-104">定義用戶端可針對乙太網路交換器功能探索預設設定之有效範圍的方法。</span><span class="sxs-lookup"><span data-stu-id="26a92-104">Defines the means by which a client can discover the valid range of default settings for an Ethernet switch feature.</span></span> <span data-ttu-id="26a92-105">針對交換器所支援的每個功能， **Msvm \_ EthernetSwitchFeatureCapabilities** 物件與每個虛擬乙太網路交換器相關聯。</span><span class="sxs-lookup"><span data-stu-id="26a92-105">An **Msvm\_EthernetSwitchFeatureCapabilities** object is associated with each virtual Ethernet switch, for each feature that the switch supports.</span></span> <span data-ttu-id="26a92-106">有四個 [**Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) 物件與 **Msvm \_ EthernetSwitchFeatureCapabilities** 物件相關聯，以描述指定參數功能功能的最小值、最大值、預設值和累加值。</span><span class="sxs-lookup"><span data-stu-id="26a92-106">Four [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) objects are associated with the **Msvm\_EthernetSwitchFeatureCapabilities** object to describe the minimum, maximum, default, and incremental values for the given switch's feature capabilities.</span></span>

<span data-ttu-id="26a92-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="26a92-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="26a92-108">語法</span><span class="sxs-lookup"><span data-stu-id="26a92-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchFeatureCapabilities : CIM_Capabilities
{
  string InstanceID;
  string Caption = " Ethernet Switch Feature Capabilities";
  string Description = "Microsoft Virtual Ethernet Switch Feature Capabilities";
  string ElementName = "Ethernet Switch Port Bandwidth Settings";
  string FeatureId;
  uint16 Applicability;
  string Version;
};
```

## <a name="members"></a><span data-ttu-id="26a92-109">成員</span><span class="sxs-lookup"><span data-stu-id="26a92-109">Members</span></span>

<span data-ttu-id="26a92-110">**Msvm \_ EthernetSwitchFeatureCapabilities** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="26a92-110">The **Msvm\_EthernetSwitchFeatureCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="26a92-111">屬性</span><span class="sxs-lookup"><span data-stu-id="26a92-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26a92-112">屬性</span><span class="sxs-lookup"><span data-stu-id="26a92-112">Properties</span></span>

<span data-ttu-id="26a92-113">**Msvm \_ EthernetSwitchFeatureCapabilities** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="26a92-113">The **Msvm\_EthernetSwitchFeatureCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="26a92-114">**適用性**</span><span class="sxs-lookup"><span data-stu-id="26a92-114">**Applicability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26a92-115">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="26a92-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="26a92-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="26a92-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26a92-117">描述這項功能是套用到乙太網路交換器或特定乙太網路交換器埠。</span><span class="sxs-lookup"><span data-stu-id="26a92-117">Describes whether this feature is applied to an Ethernet switch or a particular Ethernet switch port.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="26a92-118">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="26a92-118">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Port"></span><span id="port"></span><span id="PORT"></span>

<span data-ttu-id="26a92-119">**埠** (1) </span><span class="sxs-lookup"><span data-stu-id="26a92-119">**Port** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>

<span data-ttu-id="26a92-120">**切換** (2) </span><span class="sxs-lookup"><span data-stu-id="26a92-120">**Switch** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="26a92-121">**標題**</span><span class="sxs-lookup"><span data-stu-id="26a92-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26a92-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="26a92-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26a92-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="26a92-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26a92-124">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="26a92-124">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="26a92-125">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="26a92-125">A short description of the object.</span></span> <span data-ttu-id="26a92-126">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="26a92-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="26a92-127">**說明**</span><span class="sxs-lookup"><span data-stu-id="26a92-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26a92-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="26a92-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26a92-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="26a92-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26a92-130">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="26a92-130">A description of the object.</span></span> <span data-ttu-id="26a92-131">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="26a92-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="26a92-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="26a92-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26a92-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="26a92-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26a92-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="26a92-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26a92-135">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="26a92-135">A display name for the object.</span></span> <span data-ttu-id="26a92-136">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="26a92-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="26a92-137">**FeatureId**</span><span class="sxs-lookup"><span data-stu-id="26a92-137">**FeatureId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26a92-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="26a92-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26a92-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="26a92-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26a92-140">此物件提供其功能資訊的功能識別碼。</span><span class="sxs-lookup"><span data-stu-id="26a92-140">The identifier of the feature this object provides capabilities information for.</span></span>

</dd> <dt>

<span data-ttu-id="26a92-141">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="26a92-141">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26a92-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="26a92-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26a92-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="26a92-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26a92-144">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="26a92-144">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="26a92-145">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="26a92-145">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="26a92-146">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="26a92-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="26a92-147">**版本**</span><span class="sxs-lookup"><span data-stu-id="26a92-147">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26a92-148">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="26a92-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26a92-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="26a92-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26a92-150">格式為 "主要. 次要" 的功能版本，例如 "2.0"。</span><span class="sxs-lookup"><span data-stu-id="26a92-150">The version of the feature in a format of "major.minor", for example "2.0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26a92-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="26a92-151">Requirements</span></span>



| <span data-ttu-id="26a92-152">需求</span><span class="sxs-lookup"><span data-stu-id="26a92-152">Requirement</span></span> | <span data-ttu-id="26a92-153">值</span><span class="sxs-lookup"><span data-stu-id="26a92-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26a92-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26a92-154">Minimum supported client</span></span><br/> | <span data-ttu-id="26a92-155">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26a92-155">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="26a92-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26a92-156">Minimum supported server</span></span><br/> | <span data-ttu-id="26a92-157">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26a92-157">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="26a92-158">命名空間</span><span class="sxs-lookup"><span data-stu-id="26a92-158">Namespace</span></span><br/>                | <span data-ttu-id="26a92-159">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="26a92-159">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="26a92-160">MOF</span><span class="sxs-lookup"><span data-stu-id="26a92-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26a92-161"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="26a92-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="26a92-162">DLL</span><span class="sxs-lookup"><span data-stu-id="26a92-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26a92-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="26a92-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

