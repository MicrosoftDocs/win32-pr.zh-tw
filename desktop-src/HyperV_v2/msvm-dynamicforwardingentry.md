---
description: 表示轉送 (篩選與透明橋接服務相關聯) 資料庫中的專案。
ms.assetid: 3C9FAE99-9543-4A6A-B578-3F4626598DB3
title: Msvm_DynamicForwardingEntry 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DynamicForwardingEntry
- Msvm_DynamicForwardingEntry.InstanceID
- Msvm_DynamicForwardingEntry.Caption
- Msvm_DynamicForwardingEntry.Description
- Msvm_DynamicForwardingEntry.ElementName
- Msvm_DynamicForwardingEntry.InstallDate
- Msvm_DynamicForwardingEntry.Name
- Msvm_DynamicForwardingEntry.OperationalStatus
- Msvm_DynamicForwardingEntry.StatusDescriptions
- Msvm_DynamicForwardingEntry.Status
- Msvm_DynamicForwardingEntry.HealthState
- Msvm_DynamicForwardingEntry.CommunicationStatus
- Msvm_DynamicForwardingEntry.DetailedStatus
- Msvm_DynamicForwardingEntry.OperatingStatus
- Msvm_DynamicForwardingEntry.PrimaryStatus
- Msvm_DynamicForwardingEntry.SystemCreationClassName
- Msvm_DynamicForwardingEntry.SystemName
- Msvm_DynamicForwardingEntry.ServiceCreationClassName
- Msvm_DynamicForwardingEntry.ServiceName
- Msvm_DynamicForwardingEntry.CreationClassName
- Msvm_DynamicForwardingEntry.MACAddress
- Msvm_DynamicForwardingEntry.DynamicStatus
- Msvm_DynamicForwardingEntry.VlanId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f14f8b3a8f5f62e1a474b3d7b7f832b6acd530f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975356"
---
# <a name="msvm_dynamicforwardingentry-class"></a><span data-ttu-id="22f55-103">Msvm \_ DynamicForwardingEntry 類別</span><span class="sxs-lookup"><span data-stu-id="22f55-103">Msvm\_DynamicForwardingEntry class</span></span>

<span data-ttu-id="22f55-104">表示轉送 (篩選與透明橋接服務相關聯) 資料庫中的專案。</span><span class="sxs-lookup"><span data-stu-id="22f55-104">Represents an entry in the forwarding (filtering) database that is associated with the transparent bridging service.</span></span> <span data-ttu-id="22f55-105">專案是服務的弱式，如 [**Msvm \_ TransparentBridgingDynamicForwarding**](msvm-transparentbridgingdynamicforwarding.md)所指定。</span><span class="sxs-lookup"><span data-stu-id="22f55-105">The entry is weak to the service, as specified by [**Msvm\_TransparentBridgingDynamicForwarding**](msvm-transparentbridgingdynamicforwarding.md).</span></span>

<span data-ttu-id="22f55-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="22f55-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="22f55-107">語法</span><span class="sxs-lookup"><span data-stu-id="22f55-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DynamicForwardingEntry : CIM_DynamicForwardingEntry
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   SystemCreationClassName;
  string   SystemName;
  string   ServiceCreationClassName;
  string   ServiceName;
  string   CreationClassName;
  string   MACAddress;
  uint16   DynamicStatus;
  uint16   VlanId;
};
```

## <a name="members"></a><span data-ttu-id="22f55-108">成員</span><span class="sxs-lookup"><span data-stu-id="22f55-108">Members</span></span>

<span data-ttu-id="22f55-109">**Msvm \_ DynamicForwardingEntry** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="22f55-109">The **Msvm\_DynamicForwardingEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="22f55-110">屬性</span><span class="sxs-lookup"><span data-stu-id="22f55-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="22f55-111">屬性</span><span class="sxs-lookup"><span data-stu-id="22f55-111">Properties</span></span>

<span data-ttu-id="22f55-112">**Msvm \_ DynamicForwardingEntry** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="22f55-112">The **Msvm\_DynamicForwardingEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="22f55-113">**標題**</span><span class="sxs-lookup"><span data-stu-id="22f55-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f55-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="22f55-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f55-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22f55-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22f55-116">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="22f55-116">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="22f55-117">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="22f55-117">A short description of the object.</span></span> <span data-ttu-id="22f55-118">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="22f55-118">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="22f55-119">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="22f55-119">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f55-120">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="22f55-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22f55-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22f55-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f55-122">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="22f55-122">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="22f55-123">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="22f55-123">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="22f55-124">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="22f55-124">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22f55-125">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="22f55-125">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f55-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="22f55-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f55-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22f55-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22f55-128">限定詞： **Key**、 **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="22f55-128">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="22f55-129">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="22f55-129">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="22f55-130">搭配這個類別的其他重要屬性使用時，此屬性可讓這個類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="22f55-130">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="22f55-131">這個屬性繼承自 [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="22f55-131">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="22f55-132">**說明**</span><span class="sxs-lookup"><span data-stu-id="22f55-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f55-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="22f55-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f55-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22f55-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f55-135">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="22f55-135">A description of the object.</span></span> <span data-ttu-id="22f55-136">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="22f55-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="22f55-137">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="22f55-137">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f55-138">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="22f55-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22f55-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22f55-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f55-140">補充具有其他狀態詳細資料的 **PrimaryStatus** 屬性。</span><span class="sxs-lookup"><span data-stu-id="22f55-140">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="22f55-141">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="22f55-141">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="22f55-142">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="22f55-142">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22f55-143">**DynamicStatus**</span><span class="sxs-lookup"><span data-stu-id="22f55-143">**DynamicStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f55-144">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="22f55-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22f55-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22f55-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f55-146">專案的狀態。</span><span class="sxs-lookup"><span data-stu-id="22f55-146">The status of the entry.</span></span> <span data-ttu-id="22f55-147">這個屬性繼承自 [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="22f55-147">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="22f55-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="22f55-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="22f55-149"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**無效** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="22f55-149"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Invalid** (2)</span></span>
</dt> <dt>

<span data-ttu-id="22f55-150"><span id="Learned"></span><span id="learned"></span><span id="LEARNED"></span>**學習** (3) </span><span class="sxs-lookup"><span data-stu-id="22f55-150"><span id="Learned"></span><span id="learned"></span><span id="LEARNED"></span>**Learned** (3)</span></span>
</dt> <dt>

<span data-ttu-id="22f55-151"><span id="Self"></span><span id="self"></span><span id="SELF"></span>**Self** (4) </span><span class="sxs-lookup"><span data-stu-id="22f55-151"><span id="Self"></span><span id="self"></span><span id="SELF"></span>**Self** (4)</span></span>
</dt> <dt>

<span data-ttu-id="22f55-152"><span id="Mgmt"></span><span id="mgmt"></span><span id="MGMT"></span>**管理** (5) </span><span class="sxs-lookup"><span data-stu-id="22f55-152"><span id="Mgmt"></span><span id="mgmt"></span><span id="MGMT"></span>**Mgmt** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="22f55-153">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="22f55-153">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f55-154">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="22f55-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f55-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22f55-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f55-156">元素的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="22f55-156">A display name for the element.</span></span> <span data-ttu-id="22f55-157">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="22f55-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="22f55-158">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="22f55-158">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f55-159">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="22f55-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22f55-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22f55-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f55-161">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="22f55-161">The current health of the element.</span></span> <span data-ttu-id="22f55-162">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 ( 「確定」 ) 。</span><span class="sxs-lookup"><span data-stu-id="22f55-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 ("OK").</span></span>

</dd> <dt>

<span data-ttu-id="22f55-163">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="22f55-163">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f55-164">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="22f55-164">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="22f55-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22f55-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f55-166">當虛擬機器建立時自動填入。</span><span class="sxs-lookup"><span data-stu-id="22f55-166">Automatically populated when the virtual machine is created.</span></span> <span data-ttu-id="22f55-167">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="22f55-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22f55-168">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="22f55-168">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f55-169">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="22f55-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f55-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22f55-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22f55-171">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="22f55-171">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="22f55-172">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="22f55-172">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="22f55-173">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="22f55-173">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="22f55-174">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="22f55-174">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f55-175">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="22f55-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f55-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22f55-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22f55-177">限定詞： **Key**、 **MaxLen** (12) </span><span class="sxs-lookup"><span data-stu-id="22f55-177">Qualifiers: **Key**, **MaxLen** (12)</span></span>
</dt> </dl>

<span data-ttu-id="22f55-178">透明橋接服務具有轉送和篩選資訊的單播 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="22f55-178">Unicast MAC address for which the transparent bridging service has forwarding and filtering information.</span></span> <span data-ttu-id="22f55-179">MAC 位址的格式為十二個十六進位數位 (例如 "010203040506" ) ，其中每一組代表根據 RFC 2469 以「標準」位順序表示的其中六個 MAC 位址八位。</span><span class="sxs-lookup"><span data-stu-id="22f55-179">The MAC address is formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in "canonical" bit order according to RFC 2469.</span></span> <span data-ttu-id="22f55-180">這個屬性繼承自 [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="22f55-180">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="22f55-181">**名稱**</span><span class="sxs-lookup"><span data-stu-id="22f55-181">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f55-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="22f55-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f55-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22f55-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f55-184">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="22f55-184">The label by which the object is known.</span></span> <span data-ttu-id="22f55-185">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="22f55-185">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22f55-186">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="22f55-186">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f55-187">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="22f55-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22f55-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22f55-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f55-189">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="22f55-189">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="22f55-190">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="22f55-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="22f55-191">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="22f55-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22f55-192">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="22f55-192">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f55-193">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="22f55-193">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="22f55-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22f55-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f55-195">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不受支援。</span><span class="sxs-lookup"><span data-stu-id="22f55-195">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="22f55-196">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="22f55-196">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f55-197">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="22f55-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22f55-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22f55-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f55-199">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="22f55-199">Provides high level status information.</span></span> <span data-ttu-id="22f55-200">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="22f55-200">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="22f55-201">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="22f55-201">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="22f55-202">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="22f55-202">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22f55-203">**ServiceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="22f55-203">**ServiceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f55-204">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="22f55-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f55-205">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22f55-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22f55-206">限定詞： **Key**、 **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="22f55-206">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="22f55-207">範圍服務的 **CreationClassName**。</span><span class="sxs-lookup"><span data-stu-id="22f55-207">The scoping service's **CreationClassName**.</span></span> <span data-ttu-id="22f55-208">這個屬性繼承自 [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="22f55-208">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="22f55-209">**ServiceName**</span><span class="sxs-lookup"><span data-stu-id="22f55-209">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f55-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="22f55-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f55-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22f55-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22f55-212">限定詞： **Key**、 **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="22f55-212">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="22f55-213">範圍服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="22f55-213">The scoping service's name.</span></span> <span data-ttu-id="22f55-214">這個屬性繼承自 [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="22f55-214">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="22f55-215">**狀態**</span><span class="sxs-lookup"><span data-stu-id="22f55-215">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f55-216">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="22f55-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f55-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22f55-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f55-218">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="22f55-218">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="22f55-219">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="22f55-219">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f55-220">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="22f55-220">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="22f55-221">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22f55-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f55-222">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不受支援。</span><span class="sxs-lookup"><span data-stu-id="22f55-222">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="22f55-223">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="22f55-223">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f55-224">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="22f55-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f55-225">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22f55-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22f55-226">限定詞： **Key**、 **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="22f55-226">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="22f55-227">範圍系統的 **CreationClassName**。</span><span class="sxs-lookup"><span data-stu-id="22f55-227">The scoping system's **CreationClassName**.</span></span> <span data-ttu-id="22f55-228">這個屬性繼承自 [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="22f55-228">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="22f55-229">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="22f55-229">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f55-230">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="22f55-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f55-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22f55-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22f55-232">限定詞： **Key**、 **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="22f55-232">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="22f55-233">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="22f55-233">The scoping system's name.</span></span> <span data-ttu-id="22f55-234">這個屬性繼承自 [**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="22f55-234">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="22f55-235">**VlanId**</span><span class="sxs-lookup"><span data-stu-id="22f55-235">**VlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f55-236">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="22f55-236">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22f55-237">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="22f55-237">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="22f55-238">與此專案相關聯的虛擬 LAN 識別碼。</span><span class="sxs-lookup"><span data-stu-id="22f55-238">The virtual LAN identifier associated with this entry.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="22f55-239">備註</span><span class="sxs-lookup"><span data-stu-id="22f55-239">Remarks</span></span>

<span data-ttu-id="22f55-240">存取 **Msvm \_ DynamicForwardingEntry** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="22f55-240">Access to the **Msvm\_DynamicForwardingEntry** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="22f55-241">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="22f55-241">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="22f55-242">範例</span><span class="sxs-lookup"><span data-stu-id="22f55-242">Examples</span></span>

<span data-ttu-id="22f55-243">請參閱 [查詢網路物件](querying-networking-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="22f55-243">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="22f55-244">規格需求</span><span class="sxs-lookup"><span data-stu-id="22f55-244">Requirements</span></span>



| <span data-ttu-id="22f55-245">需求</span><span class="sxs-lookup"><span data-stu-id="22f55-245">Requirement</span></span> | <span data-ttu-id="22f55-246">值</span><span class="sxs-lookup"><span data-stu-id="22f55-246">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22f55-247">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="22f55-247">Minimum supported client</span></span><br/> | <span data-ttu-id="22f55-248">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22f55-248">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="22f55-249">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="22f55-249">Minimum supported server</span></span><br/> | <span data-ttu-id="22f55-250">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22f55-250">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="22f55-251">命名空間</span><span class="sxs-lookup"><span data-stu-id="22f55-251">Namespace</span></span><br/>                | <span data-ttu-id="22f55-252">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="22f55-252">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="22f55-253">MOF</span><span class="sxs-lookup"><span data-stu-id="22f55-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22f55-254"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="22f55-254"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="22f55-255">DLL</span><span class="sxs-lookup"><span data-stu-id="22f55-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22f55-256"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="22f55-256"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="22f55-257">另請參閱</span><span class="sxs-lookup"><span data-stu-id="22f55-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22f55-258">**CIM \_ DynamicForwardingEntry**</span><span class="sxs-lookup"><span data-stu-id="22f55-258">**CIM\_DynamicForwardingEntry**</span></span>](cim-dynamicforwardingentry.md)
</dt> <dt>

<span data-ttu-id="22f55-259">[**CIM \_ DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="22f55-259">[**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85))</span></span>
</dt> </dl>

 

