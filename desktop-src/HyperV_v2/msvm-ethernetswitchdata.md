---
description: 抽象類別，表示乙太網路交換器之指定實例的資源。
ms.assetid: 5ae1be2a-8d59-4efe-a4ae-7cac1727cfa2
title: Msvm_EthernetSwitchData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchData
- Msvm_EthernetSwitchData.InstanceID
- Msvm_EthernetSwitchData.Caption
- Msvm_EthernetSwitchData.Description
- Msvm_EthernetSwitchData.ElementName
- Msvm_EthernetSwitchData.SystemCreationClassName
- Msvm_EthernetSwitchData.SystemName
- Msvm_EthernetSwitchData.CreationClassName
- Msvm_EthernetSwitchData.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dca2e4e01266a0a7da0f3ec85a86615406625f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997534"
---
# <a name="msvm_ethernetswitchdata-class"></a><span data-ttu-id="d1b5b-103">Msvm \_ EthernetSwitchData 類別</span><span class="sxs-lookup"><span data-stu-id="d1b5b-103">Msvm\_EthernetSwitchData class</span></span>

<span data-ttu-id="d1b5b-104">抽象類別，表示乙太網路交換器之指定實例的資源。</span><span class="sxs-lookup"><span data-stu-id="d1b5b-104">Abstract class that represents a resource for a given instance of an Ethernet switch.</span></span>

<span data-ttu-id="d1b5b-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d1b5b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1b5b-106">語法</span><span class="sxs-lookup"><span data-stu-id="d1b5b-106">Syntax</span></span>

``` syntax
[Abstract, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchData : CIM_ManagedElement
{
  string InstanceID;
  string Caption = "Ethernet Switch Bandwidth data";
  string Description = "Represents the switch bandwidth resource status.";
  string ElementName = "Ethernet Switch Bandwidth data";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string CreationClassName = " Msvm_EthernetSwitchBandwidthData";
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="d1b5b-107">成員</span><span class="sxs-lookup"><span data-stu-id="d1b5b-107">Members</span></span>

<span data-ttu-id="d1b5b-108">**Msvm \_ EthernetSwitchData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d1b5b-108">The **Msvm\_EthernetSwitchData** class has these types of members:</span></span>

-   [<span data-ttu-id="d1b5b-109">屬性</span><span class="sxs-lookup"><span data-stu-id="d1b5b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1b5b-110">屬性</span><span class="sxs-lookup"><span data-stu-id="d1b5b-110">Properties</span></span>

<span data-ttu-id="d1b5b-111">**Msvm \_ EthernetSwitchData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d1b5b-111">The **Msvm\_EthernetSwitchData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1b5b-112">**標題**</span><span class="sxs-lookup"><span data-stu-id="d1b5b-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1b5b-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d1b5b-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1b5b-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d1b5b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1b5b-115">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="d1b5b-115">A short description of the object.</span></span> <span data-ttu-id="d1b5b-116">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="d1b5b-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d1b5b-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d1b5b-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1b5b-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d1b5b-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1b5b-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d1b5b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1b5b-120">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="d1b5b-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d1b5b-121">建立這個實例時所使用的類別或子類別名稱。</span><span class="sxs-lookup"><span data-stu-id="d1b5b-121">The name of the class or subclass used in the creation of this instance.</span></span>

</dd> <dt>

<span data-ttu-id="d1b5b-122">**說明**</span><span class="sxs-lookup"><span data-stu-id="d1b5b-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1b5b-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d1b5b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1b5b-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d1b5b-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1b5b-125">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="d1b5b-125">A description of the object.</span></span> <span data-ttu-id="d1b5b-126">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="d1b5b-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d1b5b-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d1b5b-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1b5b-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d1b5b-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1b5b-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d1b5b-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1b5b-130">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="d1b5b-130">A display name for the object.</span></span> <span data-ttu-id="d1b5b-131">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="d1b5b-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d1b5b-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d1b5b-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1b5b-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d1b5b-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1b5b-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d1b5b-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1b5b-135">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="d1b5b-135">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d1b5b-136">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="d1b5b-136">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d1b5b-137">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="d1b5b-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d1b5b-138">**名稱**</span><span class="sxs-lookup"><span data-stu-id="d1b5b-138">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1b5b-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d1b5b-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1b5b-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d1b5b-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1b5b-141">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) 、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="d1b5b-141">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d1b5b-142">資源的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="d1b5b-142">The unique name of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="d1b5b-143">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d1b5b-143">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1b5b-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d1b5b-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1b5b-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d1b5b-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1b5b-146">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ System**](cim-system.md).**CreationClassName**") ， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="d1b5b-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d1b5b-147">裝載系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="d1b5b-147">The hosting system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="d1b5b-148">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d1b5b-148">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1b5b-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d1b5b-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1b5b-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d1b5b-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1b5b-151">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ System**](cim-system.md).**Name**") ， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="d1b5b-151">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d1b5b-152">相關聯的資源實例所系結之虛擬交換器的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1b5b-152">The name of the virtual switch to which the associated resource instance is bound.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d1b5b-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1b5b-153">Requirements</span></span>



| <span data-ttu-id="d1b5b-154">需求</span><span class="sxs-lookup"><span data-stu-id="d1b5b-154">Requirement</span></span> | <span data-ttu-id="d1b5b-155">值</span><span class="sxs-lookup"><span data-stu-id="d1b5b-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1b5b-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d1b5b-156">Minimum supported client</span></span><br/> | <span data-ttu-id="d1b5b-157">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1b5b-157">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d1b5b-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d1b5b-158">Minimum supported server</span></span><br/> | <span data-ttu-id="d1b5b-159">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1b5b-159">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d1b5b-160">命名空間</span><span class="sxs-lookup"><span data-stu-id="d1b5b-160">Namespace</span></span><br/>                | <span data-ttu-id="d1b5b-161">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="d1b5b-161">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d1b5b-162">MOF</span><span class="sxs-lookup"><span data-stu-id="d1b5b-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1b5b-163"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d1b5b-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1b5b-164">DLL</span><span class="sxs-lookup"><span data-stu-id="d1b5b-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1b5b-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d1b5b-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

