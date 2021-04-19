---
description: 代表安裝在主機系統上的擴充元件實例。
ms.assetid: ad24fb08-36af-42a8-a910-63eae54fa5b8
title: Msvm_InstalledEthernetSwitchExtension 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InstalledEthernetSwitchExtension
- Msvm_InstalledEthernetSwitchExtension.InstanceID
- Msvm_InstalledEthernetSwitchExtension.Caption
- Msvm_InstalledEthernetSwitchExtension.Description
- Msvm_InstalledEthernetSwitchExtension.ElementName
- Msvm_InstalledEthernetSwitchExtension.InstallDate
- Msvm_InstalledEthernetSwitchExtension.Name
- Msvm_InstalledEthernetSwitchExtension.OperationalStatus
- Msvm_InstalledEthernetSwitchExtension.StatusDescriptions
- Msvm_InstalledEthernetSwitchExtension.Status
- Msvm_InstalledEthernetSwitchExtension.HealthState
- Msvm_InstalledEthernetSwitchExtension.CommunicationStatus
- Msvm_InstalledEthernetSwitchExtension.DetailedStatus
- Msvm_InstalledEthernetSwitchExtension.OperatingStatus
- Msvm_InstalledEthernetSwitchExtension.PrimaryStatus
- Msvm_InstalledEthernetSwitchExtension.ExtensionType
- Msvm_InstalledEthernetSwitchExtension.Vendor
- Msvm_InstalledEthernetSwitchExtension.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bfbe0b1996751613c31913447cb0d200d71b8168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971028"
---
# <a name="msvm_installedethernetswitchextension-class"></a><span data-ttu-id="1c96f-103">Msvm \_ InstalledEthernetSwitchExtension 類別</span><span class="sxs-lookup"><span data-stu-id="1c96f-103">Msvm\_InstalledEthernetSwitchExtension class</span></span>

<span data-ttu-id="1c96f-104">代表安裝在主機系統上的擴充元件實例。</span><span class="sxs-lookup"><span data-stu-id="1c96f-104">Represents an instance of an extension component installed on a host system.</span></span>

<span data-ttu-id="1c96f-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1c96f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c96f-106">語法</span><span class="sxs-lookup"><span data-stu-id="1c96f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InstalledEthernetSwitchExtension : CIM_ManagedSystemElement
{
  string   InstanceID;
  string   Caption = " System Virtual Ethernet Switch Extension";
  string   Description = "Microsoft NDIS Packet Capture Filter Driver";
  string   ElementName = "Microsoft NDIS Capture";
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint8    ExtensionType;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="1c96f-107">成員</span><span class="sxs-lookup"><span data-stu-id="1c96f-107">Members</span></span>

<span data-ttu-id="1c96f-108">**Msvm \_ InstalledEthernetSwitchExtension** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1c96f-108">The **Msvm\_InstalledEthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="1c96f-109">屬性</span><span class="sxs-lookup"><span data-stu-id="1c96f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1c96f-110">屬性</span><span class="sxs-lookup"><span data-stu-id="1c96f-110">Properties</span></span>

<span data-ttu-id="1c96f-111">**Msvm \_ InstalledEthernetSwitchExtension** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1c96f-111">The **Msvm\_InstalledEthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1c96f-112">**標題**</span><span class="sxs-lookup"><span data-stu-id="1c96f-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c96f-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1c96f-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1c96f-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-115">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="1c96f-115">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="1c96f-116">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="1c96f-116">A short description of the object.</span></span> <span data-ttu-id="1c96f-117">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="1c96f-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1c96f-118">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="1c96f-118">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c96f-119">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1c96f-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1c96f-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c96f-121">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="1c96f-121">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="1c96f-122">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="1c96f-122">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1c96f-123">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1c96f-123">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1c96f-124">**說明**</span><span class="sxs-lookup"><span data-stu-id="1c96f-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c96f-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1c96f-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1c96f-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c96f-127">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="1c96f-127">A description of the object.</span></span> <span data-ttu-id="1c96f-128">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="1c96f-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1c96f-129">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="1c96f-129">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c96f-130">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1c96f-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1c96f-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c96f-132">補充具有其他狀態詳細資料的 **PrimaryStatus** 屬性。</span><span class="sxs-lookup"><span data-stu-id="1c96f-132">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="1c96f-133">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="1c96f-133">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1c96f-134">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1c96f-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1c96f-135">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1c96f-135">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c96f-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1c96f-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1c96f-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c96f-138">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="1c96f-138">A display name for the object.</span></span> <span data-ttu-id="1c96f-139">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="1c96f-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1c96f-140">**ExtensionType**</span><span class="sxs-lookup"><span data-stu-id="1c96f-140">**ExtensionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c96f-141">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="1c96f-141">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1c96f-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c96f-143">指出擴充元件的類型。</span><span class="sxs-lookup"><span data-stu-id="1c96f-143">Indicates the type of the extension component.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1c96f-144">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="1c96f-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Capture"></span><span id="capture"></span><span id="CAPTURE"></span>

<span data-ttu-id="1c96f-145">**Capture** (1) </span><span class="sxs-lookup"><span data-stu-id="1c96f-145">**Capture** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>

<span data-ttu-id="1c96f-146">**篩選** (2) </span><span class="sxs-lookup"><span data-stu-id="1c96f-146">**Filter** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Forwarding"></span><span id="forwarding"></span><span id="FORWARDING"></span>

<span data-ttu-id="1c96f-147">**轉送** (3) </span><span class="sxs-lookup"><span data-stu-id="1c96f-147">**Forwarding** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Monitoring"></span><span id="monitoring"></span><span id="MONITORING"></span>

<span data-ttu-id="1c96f-148">**監視** (4) </span><span class="sxs-lookup"><span data-stu-id="1c96f-148">**Monitoring** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Native"></span><span id="native"></span><span id="NATIVE"></span>

<span data-ttu-id="1c96f-149">**原生** (5) </span><span class="sxs-lookup"><span data-stu-id="1c96f-149">**Native** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1c96f-150">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="1c96f-150">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c96f-151">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1c96f-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1c96f-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c96f-153">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="1c96f-153">The current health of the element.</span></span> <span data-ttu-id="1c96f-154">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="1c96f-154">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="1c96f-155">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="1c96f-155">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="1c96f-156">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="1c96f-156">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="1c96f-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1c96f-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c96f-158">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="1c96f-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1c96f-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c96f-160">安裝物件的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="1c96f-160">The date and time when the object was installed.</span></span> <span data-ttu-id="1c96f-161">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="1c96f-161">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="1c96f-162">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1c96f-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1c96f-163">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1c96f-163">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c96f-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1c96f-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1c96f-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-166">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="1c96f-166">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1c96f-167">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="1c96f-167">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1c96f-168">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="1c96f-168">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1c96f-169">**名稱**</span><span class="sxs-lookup"><span data-stu-id="1c96f-169">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c96f-170">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1c96f-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1c96f-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-172">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) 、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="1c96f-172">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1c96f-173">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="1c96f-173">The label by which the object is known.</span></span> <span data-ttu-id="1c96f-174">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1c96f-174">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1c96f-175">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="1c96f-175">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c96f-176">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1c96f-176">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1c96f-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c96f-178">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1c96f-178">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="1c96f-179">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="1c96f-179">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1c96f-180">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1c96f-180">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1c96f-181">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="1c96f-181">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c96f-182">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="1c96f-182">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1c96f-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c96f-184">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="1c96f-184">The current statuses of the object.</span></span> <span data-ttu-id="1c96f-185">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 2 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="1c96f-185">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="1c96f-186">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="1c96f-186">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c96f-187">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1c96f-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1c96f-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c96f-189">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="1c96f-189">Provides high level status information.</span></span> <span data-ttu-id="1c96f-190">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="1c96f-190">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="1c96f-191">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="1c96f-191">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1c96f-192">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1c96f-192">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1c96f-193">**狀態**</span><span class="sxs-lookup"><span data-stu-id="1c96f-193">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c96f-194">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1c96f-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1c96f-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c96f-196">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="1c96f-196">The current status of the object.</span></span> <span data-ttu-id="1c96f-197">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1c96f-197">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1c96f-198">正常</span><span class="sxs-lookup"><span data-stu-id="1c96f-198">"OK"</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-199"><span id="OK"></span><span id="ok"></span>**還行**</span><span class="sxs-lookup"><span data-stu-id="1c96f-199"><span id="OK"></span><span id="ok"></span>**OK**</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-200"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤**</span><span class="sxs-lookup"><span data-stu-id="1c96f-200"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error**</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-201"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**退化**</span><span class="sxs-lookup"><span data-stu-id="1c96f-201"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded**</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知**</span><span class="sxs-lookup"><span data-stu-id="1c96f-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-203"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Pred 失敗**</span><span class="sxs-lookup"><span data-stu-id="1c96f-203"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Pred Fail**</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-204"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始**</span><span class="sxs-lookup"><span data-stu-id="1c96f-204"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting**</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-205"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止**</span><span class="sxs-lookup"><span data-stu-id="1c96f-205"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping**</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-206"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**服務**</span><span class="sxs-lookup"><span data-stu-id="1c96f-206"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service**</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-207"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**強調**</span><span class="sxs-lookup"><span data-stu-id="1c96f-207"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed**</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-208"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**NonRecover**</span><span class="sxs-lookup"><span data-stu-id="1c96f-208"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**NonRecover**</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-209"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**無連絡人**</span><span class="sxs-lookup"><span data-stu-id="1c96f-209"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact**</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-210"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**遺失的通訊**</span><span class="sxs-lookup"><span data-stu-id="1c96f-210"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Lost Comm**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1c96f-211">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="1c96f-211">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c96f-212">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="1c96f-212">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1c96f-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c96f-214">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="1c96f-214">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="1c96f-215">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 "OK"。</span><span class="sxs-lookup"><span data-stu-id="1c96f-215">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="1c96f-216">**廠商**</span><span class="sxs-lookup"><span data-stu-id="1c96f-216">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c96f-217">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1c96f-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1c96f-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c96f-219">表示提供延伸模組的廠商。</span><span class="sxs-lookup"><span data-stu-id="1c96f-219">Indicates the vendor providing the extension.</span></span>

</dd> <dt>

<span data-ttu-id="1c96f-220">**版本**</span><span class="sxs-lookup"><span data-stu-id="1c96f-220">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c96f-221">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1c96f-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c96f-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1c96f-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c96f-223">副檔名的版本，格式為 "主要. 次要"，例如 "2.0"。</span><span class="sxs-lookup"><span data-stu-id="1c96f-223">The version of the extension in a format of "major.minor", for example "2.0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1c96f-224">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c96f-224">Requirements</span></span>



| <span data-ttu-id="1c96f-225">需求</span><span class="sxs-lookup"><span data-stu-id="1c96f-225">Requirement</span></span> | <span data-ttu-id="1c96f-226">值</span><span class="sxs-lookup"><span data-stu-id="1c96f-226">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c96f-227">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1c96f-227">Minimum supported client</span></span><br/> | <span data-ttu-id="1c96f-228">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1c96f-228">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1c96f-229">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1c96f-229">Minimum supported server</span></span><br/> | <span data-ttu-id="1c96f-230">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1c96f-230">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1c96f-231">命名空間</span><span class="sxs-lookup"><span data-stu-id="1c96f-231">Namespace</span></span><br/>                | <span data-ttu-id="1c96f-232">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="1c96f-232">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1c96f-233">MOF</span><span class="sxs-lookup"><span data-stu-id="1c96f-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c96f-234"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="1c96f-234"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c96f-235">DLL</span><span class="sxs-lookup"><span data-stu-id="1c96f-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c96f-236"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1c96f-236"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

