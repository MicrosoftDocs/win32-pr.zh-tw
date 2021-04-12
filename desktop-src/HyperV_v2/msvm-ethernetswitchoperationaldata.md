---
description: 表示 switch 指令引數。
ms.assetid: f225d321-8f40-4e6c-b30d-8fab3f84761d
title: Msvm_EthernetSwitchOperationalData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchOperationalData
- Msvm_EthernetSwitchOperationalData.InstanceID
- Msvm_EthernetSwitchOperationalData.Caption
- Msvm_EthernetSwitchOperationalData.Description
- Msvm_EthernetSwitchOperationalData.ElementName
- Msvm_EthernetSwitchOperationalData.SystemCreationClassName
- Msvm_EthernetSwitchOperationalData.SystemName
- Msvm_EthernetSwitchOperationalData.CreationClassName
- Msvm_EthernetSwitchOperationalData.Name
- Msvm_EthernetSwitchOperationalData.CurrentSwitchingMode
- Msvm_EthernetSwitchOperationalData.SupportedSwitchingModes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3d9aacd8380650ddaf2790aeacf4a2327b54f973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321240"
---
# <a name="msvm_ethernetswitchoperationaldata-class"></a><span data-ttu-id="b1a8f-103">Msvm \_ EthernetSwitchOperationalData 類別</span><span class="sxs-lookup"><span data-stu-id="b1a8f-103">Msvm\_EthernetSwitchOperationalData class</span></span>

<span data-ttu-id="b1a8f-104">表示 switch 指令引數。</span><span class="sxs-lookup"><span data-stu-id="b1a8f-104">Represents switch operational parameters.</span></span>

<span data-ttu-id="b1a8f-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b1a8f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1a8f-106">語法</span><span class="sxs-lookup"><span data-stu-id="b1a8f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1D18CDCF-209E-4172-875D-6D208A0A8375"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Modes Supported "), AMENDMENT]
class Msvm_EthernetSwitchOperationalData : Msvm_EthernetSwitchData
{
  string InstanceID;
  string Caption = "Ethernet Switch Modes Supported";
  string Description = "Represents switch operational parameters.";
  string ElementName = "Ethernet Switch Modes Supported";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string CreationClassName = " Msvm_EthernetSwitchOperationalData";
  string Name;
  uint32 CurrentSwitchingMode = 1;
  uint32 SupportedSwitchingModes[] = {1};
};
```

## <a name="members"></a><span data-ttu-id="b1a8f-107">成員</span><span class="sxs-lookup"><span data-stu-id="b1a8f-107">Members</span></span>

<span data-ttu-id="b1a8f-108">**Msvm \_ EthernetSwitchOperationalData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b1a8f-108">The **Msvm\_EthernetSwitchOperationalData** class has these types of members:</span></span>

-   [<span data-ttu-id="b1a8f-109">屬性</span><span class="sxs-lookup"><span data-stu-id="b1a8f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b1a8f-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b1a8f-110">Properties</span></span>

<span data-ttu-id="b1a8f-111">**Msvm \_ EthernetSwitchOperationalData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b1a8f-111">The **Msvm\_EthernetSwitchOperationalData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b1a8f-112">**標題**</span><span class="sxs-lookup"><span data-stu-id="b1a8f-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1a8f-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b1a8f-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1a8f-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1a8f-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1a8f-115">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="b1a8f-115">A short description of the object.</span></span> <span data-ttu-id="b1a8f-116">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="b1a8f-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b1a8f-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b1a8f-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1a8f-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b1a8f-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1a8f-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1a8f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1a8f-120">限定詞： **Key**、 **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="b1a8f-120">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="b1a8f-121">建立這個實例時所使用的類別或子類別名稱。</span><span class="sxs-lookup"><span data-stu-id="b1a8f-121">The name of the class or subclass used in the creation of this instance.</span></span> <span data-ttu-id="b1a8f-122">這個屬性繼承自 [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md)。</span><span class="sxs-lookup"><span data-stu-id="b1a8f-122">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1a8f-123">**CurrentSwitchingMode**</span><span class="sxs-lookup"><span data-stu-id="b1a8f-123">**CurrentSwitchingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1a8f-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b1a8f-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1a8f-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1a8f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1a8f-126">限定詞： **WmiDataId** (1) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="b1a8f-126">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="b1a8f-127">切換上目前的切換模式。</span><span class="sxs-lookup"><span data-stu-id="b1a8f-127">The current switching mode on the switch.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1a8f-128">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b1a8f-128">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1Q"></span><span id="802.1q"></span>

<span data-ttu-id="b1a8f-129">**802.1 q** (1) </span><span class="sxs-lookup"><span data-stu-id="b1a8f-129">**802.1Q** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1Qbg"></span><span id="802.1qbg"></span><span id="802.1QBG"></span>

<span data-ttu-id="b1a8f-130">**802.1 qbg** (2) </span><span class="sxs-lookup"><span data-stu-id="b1a8f-130">**802.1Qbg** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1Qbh"></span><span id="802.1qbh"></span><span id="802.1QBH"></span>

<span data-ttu-id="b1a8f-131">**802.1 qbh** (3) </span><span class="sxs-lookup"><span data-stu-id="b1a8f-131">**802.1Qbh** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1a8f-132">**說明**</span><span class="sxs-lookup"><span data-stu-id="b1a8f-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1a8f-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b1a8f-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1a8f-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1a8f-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1a8f-135">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="b1a8f-135">A description of the object.</span></span> <span data-ttu-id="b1a8f-136">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="b1a8f-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b1a8f-137">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b1a8f-137">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1a8f-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b1a8f-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1a8f-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1a8f-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1a8f-140">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="b1a8f-140">A display name for the object.</span></span> <span data-ttu-id="b1a8f-141">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="b1a8f-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b1a8f-142">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b1a8f-142">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1a8f-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b1a8f-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1a8f-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1a8f-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1a8f-145">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="b1a8f-145">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b1a8f-146">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="b1a8f-146">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b1a8f-147">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="b1a8f-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b1a8f-148">**名稱**</span><span class="sxs-lookup"><span data-stu-id="b1a8f-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1a8f-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b1a8f-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1a8f-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1a8f-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1a8f-151">限定詞： **Key**、 **Override**、 **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="b1a8f-151">Qualifiers: **Key**, **Override**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="b1a8f-152">資源的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="b1a8f-152">The unique name of the resource.</span></span> <span data-ttu-id="b1a8f-153">這個屬性繼承自 [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md)。</span><span class="sxs-lookup"><span data-stu-id="b1a8f-153">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1a8f-154">**SupportedSwitchingModes**</span><span class="sxs-lookup"><span data-stu-id="b1a8f-154">**SupportedSwitchingModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1a8f-155">資料類型： **uint32** 陣列</span><span class="sxs-lookup"><span data-stu-id="b1a8f-155">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="b1a8f-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1a8f-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1a8f-157">限定詞： **WmiDataId** (2) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="b1a8f-157">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="b1a8f-158">切換所支援的切換模式。</span><span class="sxs-lookup"><span data-stu-id="b1a8f-158">The switching modes supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="b1a8f-159">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b1a8f-159">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1a8f-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b1a8f-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1a8f-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1a8f-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1a8f-162">限定詞： **Key**、 **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="b1a8f-162">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="b1a8f-163">裝載系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="b1a8f-163">The hosting system's creation class name.</span></span> <span data-ttu-id="b1a8f-164">這個屬性繼承自 [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md)。</span><span class="sxs-lookup"><span data-stu-id="b1a8f-164">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1a8f-165">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b1a8f-165">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1a8f-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b1a8f-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1a8f-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b1a8f-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1a8f-168">限定詞： **Key**、 **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="b1a8f-168">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="b1a8f-169">相關聯的資源實例所系結之虛擬交換器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1a8f-169">The name of the virtual switch to which the associated resource instance is bound.</span></span> <span data-ttu-id="b1a8f-170">這個屬性繼承自 [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md)。</span><span class="sxs-lookup"><span data-stu-id="b1a8f-170">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1a8f-171">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1a8f-171">Requirements</span></span>



| <span data-ttu-id="b1a8f-172">需求</span><span class="sxs-lookup"><span data-stu-id="b1a8f-172">Requirement</span></span> | <span data-ttu-id="b1a8f-173">值</span><span class="sxs-lookup"><span data-stu-id="b1a8f-173">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1a8f-174">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b1a8f-174">Minimum supported client</span></span><br/> | <span data-ttu-id="b1a8f-175">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1a8f-175">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b1a8f-176">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b1a8f-176">Minimum supported server</span></span><br/> | <span data-ttu-id="b1a8f-177">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1a8f-177">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b1a8f-178">命名空間</span><span class="sxs-lookup"><span data-stu-id="b1a8f-178">Namespace</span></span><br/>                | <span data-ttu-id="b1a8f-179">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="b1a8f-179">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b1a8f-180">MOF</span><span class="sxs-lookup"><span data-stu-id="b1a8f-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1a8f-181"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b1a8f-181"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1a8f-182">DLL</span><span class="sxs-lookup"><span data-stu-id="b1a8f-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1a8f-183"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b1a8f-183"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

