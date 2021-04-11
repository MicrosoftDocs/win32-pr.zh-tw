---
description: 表示乙太網路交換器擴充功能所收集之埠執行時間資料的抽象類別。
ms.assetid: bc41ad1d-e7ab-4d04-96a8-26eb68ea6601
title: Msvm_EthernetPortData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortData
- Msvm_EthernetPortData.InstanceID
- Msvm_EthernetPortData.Caption
- Msvm_EthernetPortData.Description
- Msvm_EthernetPortData.ElementName
- Msvm_EthernetPortData.SystemCreationClassName
- Msvm_EthernetPortData.SystemName
- Msvm_EthernetPortData.DeviceCreationClassName
- Msvm_EthernetPortData.DeviceID
- Msvm_EthernetPortData.CreationClassName
- Msvm_EthernetPortData.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 36167d4acad3c0da6b96efb9f9cc1fe58bd41a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849500"
---
# <a name="msvm_ethernetportdata-class"></a><span data-ttu-id="04b6f-103">Msvm \_ EthernetPortData 類別</span><span class="sxs-lookup"><span data-stu-id="04b6f-103">Msvm\_EthernetPortData class</span></span>

<span data-ttu-id="04b6f-104">表示乙太網路交換器擴充功能所收集之埠執行時間資料的抽象類別。</span><span class="sxs-lookup"><span data-stu-id="04b6f-104">An abstract class that represents port runtime data collected by an Ethernet switch extension.</span></span> <span data-ttu-id="04b6f-105">所有 Ethernet 埠資料類別都必須衍生自此抽象類別。</span><span class="sxs-lookup"><span data-stu-id="04b6f-105">All Ethernet port data classes must derive from this abstract class.</span></span>

<span data-ttu-id="04b6f-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="04b6f-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="04b6f-107">語法</span><span class="sxs-lookup"><span data-stu-id="04b6f-107">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortData : CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string SystemCreationClassName;
  string SystemName;
  string DeviceCreationClassName = "Msvm_EthernetSwitchPort";
  string DeviceID;
  string CreationClassName;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="04b6f-108">成員</span><span class="sxs-lookup"><span data-stu-id="04b6f-108">Members</span></span>

<span data-ttu-id="04b6f-109">**Msvm \_ EthernetPortData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="04b6f-109">The **Msvm\_EthernetPortData** class has these types of members:</span></span>

-   [<span data-ttu-id="04b6f-110">屬性</span><span class="sxs-lookup"><span data-stu-id="04b6f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="04b6f-111">屬性</span><span class="sxs-lookup"><span data-stu-id="04b6f-111">Properties</span></span>

<span data-ttu-id="04b6f-112">**Msvm \_ EthernetPortData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="04b6f-112">The **Msvm\_EthernetPortData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="04b6f-113">**標題**</span><span class="sxs-lookup"><span data-stu-id="04b6f-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04b6f-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04b6f-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04b6f-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04b6f-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04b6f-116">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="04b6f-116">A short description of the object.</span></span> <span data-ttu-id="04b6f-117">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="04b6f-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="04b6f-118">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="04b6f-118">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04b6f-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04b6f-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04b6f-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04b6f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04b6f-121">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="04b6f-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="04b6f-122">建立此埠資料實例時所使用的子類別名稱。</span><span class="sxs-lookup"><span data-stu-id="04b6f-122">The name of the subclass used in the creation of this port data instance.</span></span>

</dd> <dt>

<span data-ttu-id="04b6f-123">**說明**</span><span class="sxs-lookup"><span data-stu-id="04b6f-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04b6f-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04b6f-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04b6f-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04b6f-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04b6f-126">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="04b6f-126">A description of the object.</span></span> <span data-ttu-id="04b6f-127">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="04b6f-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="04b6f-128">**DeviceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="04b6f-128">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04b6f-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04b6f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04b6f-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04b6f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04b6f-131">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ LogicalDevice**](cim-logicaldevice.md)。**CreationClassName**") ， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="04b6f-131">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="04b6f-132">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="04b6f-132">The scoping system's creation class name.</span></span> <span data-ttu-id="04b6f-133">此屬性一律設定為 "Msvm \_ EthernetSwitchPort"。</span><span class="sxs-lookup"><span data-stu-id="04b6f-133">This property is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="04b6f-134">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="04b6f-134">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04b6f-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04b6f-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04b6f-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04b6f-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04b6f-137">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ LogicalDevice**](cim-logicaldevice.md)。**DeviceID**") ， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="04b6f-137">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**DeviceID**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="04b6f-138">範圍此埠資料實例之埠的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="04b6f-138">The Device ID of the port that scopes this port data instance.</span></span>

</dd> <dt>

<span data-ttu-id="04b6f-139">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="04b6f-139">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04b6f-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04b6f-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04b6f-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04b6f-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04b6f-142">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="04b6f-142">A display name for the object.</span></span> <span data-ttu-id="04b6f-143">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="04b6f-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="04b6f-144">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="04b6f-144">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04b6f-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04b6f-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04b6f-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04b6f-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04b6f-147">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="04b6f-147">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="04b6f-148">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="04b6f-148">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="04b6f-149">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="04b6f-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="04b6f-150">**名稱**</span><span class="sxs-lookup"><span data-stu-id="04b6f-150">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04b6f-151">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04b6f-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04b6f-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04b6f-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04b6f-153">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="04b6f-153">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="04b6f-154">在切換和埠範圍內唯一識別此埠資料實例的字串。</span><span class="sxs-lookup"><span data-stu-id="04b6f-154">A string that uniquely identifies this port data instance within the scope of the switch and port.</span></span>

</dd> <dt>

<span data-ttu-id="04b6f-155">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="04b6f-155">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04b6f-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04b6f-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04b6f-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04b6f-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04b6f-158">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ System**](cim-system.md).**CreationClassName**") ， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="04b6f-158">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="04b6f-159">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="04b6f-159">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="04b6f-160">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="04b6f-160">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04b6f-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04b6f-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04b6f-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04b6f-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04b6f-163">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ System**](cim-system.md).**Name**") ， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="04b6f-163">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="04b6f-164">範圍此埠資料實例的虛擬交換器名稱。</span><span class="sxs-lookup"><span data-stu-id="04b6f-164">The name of the virtual switch that scopes this port data instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="04b6f-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="04b6f-165">Requirements</span></span>



| <span data-ttu-id="04b6f-166">需求</span><span class="sxs-lookup"><span data-stu-id="04b6f-166">Requirement</span></span> | <span data-ttu-id="04b6f-167">值</span><span class="sxs-lookup"><span data-stu-id="04b6f-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04b6f-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04b6f-168">Minimum supported client</span></span><br/> | <span data-ttu-id="04b6f-169">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04b6f-169">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="04b6f-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04b6f-170">Minimum supported server</span></span><br/> | <span data-ttu-id="04b6f-171">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04b6f-171">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="04b6f-172">命名空間</span><span class="sxs-lookup"><span data-stu-id="04b6f-172">Namespace</span></span><br/>                | <span data-ttu-id="04b6f-173">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="04b6f-173">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="04b6f-174">MOF</span><span class="sxs-lookup"><span data-stu-id="04b6f-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04b6f-175"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="04b6f-175"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="04b6f-176">DLL</span><span class="sxs-lookup"><span data-stu-id="04b6f-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04b6f-177"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="04b6f-177"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

