---
description: 代表切換埠設定 (ACL) 的存取控制清單。
ms.assetid: c0d6dfa1-017c-4e66-9ee3-425182d84231
title: Msvm_EthernetSwitchPortAclSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortAclSettingData
- Msvm_EthernetSwitchPortAclSettingData.InstanceID
- Msvm_EthernetSwitchPortAclSettingData.Caption
- Msvm_EthernetSwitchPortAclSettingData.Description
- Msvm_EthernetSwitchPortAclSettingData.ElementName
- Msvm_EthernetSwitchPortAclSettingData.Name
- Msvm_EthernetSwitchPortAclSettingData.Direction
- Msvm_EthernetSwitchPortAclSettingData.Applicability
- Msvm_EthernetSwitchPortAclSettingData.AclType
- Msvm_EthernetSwitchPortAclSettingData.Action
- Msvm_EthernetSwitchPortAclSettingData.LocalAddress
- Msvm_EthernetSwitchPortAclSettingData.LocalAddressPrefixLength
- Msvm_EthernetSwitchPortAclSettingData.RemoteAddress
- Msvm_EthernetSwitchPortAclSettingData.RemoteAddressPrefixLength
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 92735718e339a0caf33910dec703276aea946a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985509"
---
# <a name="msvm_ethernetswitchportaclsettingdata-class"></a><span data-ttu-id="7b22f-103">Msvm \_ EthernetSwitchPortAclSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="7b22f-103">Msvm\_EthernetSwitchPortAclSettingData class</span></span>

<span data-ttu-id="7b22f-104">代表切換埠設定 (ACL) 的存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="7b22f-104">Represents the access control list (ACL) for switch port settings.</span></span>

<span data-ttu-id="7b22f-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="7b22f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b22f-106">語法</span><span class="sxs-lookup"><span data-stu-id="7b22f-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("998BEF4A-5D55-492A-9C43-8B2F5EAE9F2B"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), Provider("VmmsWmiInstanceAndMethodProvider"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port ACL Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortAclSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port ACL Settings";
  string Description = "Represents the base class for switch port settings.";
  string ElementName = "Ethernet Switch Port ACL Settings";
  string Name = "";
  uint8  Direction = 0;
  uint8  Applicability = 0;
  uint8  AclType = 0;
  uint8  Action = 0;
  string LocalAddress = "";
  uint8  LocalAddressPrefixLength = 0;
  string RemoteAddress = length = 0;
  uint8  RemoteAddressPrefixLength = 0;
};
```

## <a name="members"></a><span data-ttu-id="7b22f-107">成員</span><span class="sxs-lookup"><span data-stu-id="7b22f-107">Members</span></span>

<span data-ttu-id="7b22f-108">**Msvm \_ EthernetSwitchPortAclSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7b22f-108">The **Msvm\_EthernetSwitchPortAclSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="7b22f-109">屬性</span><span class="sxs-lookup"><span data-stu-id="7b22f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b22f-110">屬性</span><span class="sxs-lookup"><span data-stu-id="7b22f-110">Properties</span></span>

<span data-ttu-id="7b22f-111">**Msvm \_ EthernetSwitchPortAclSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7b22f-111">The **Msvm\_EthernetSwitchPortAclSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b22f-112">**AclType**</span><span class="sxs-lookup"><span data-stu-id="7b22f-112">**AclType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22f-113">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="7b22f-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7b22f-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7b22f-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7b22f-115">限定詞： **WmiDataId** (4) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="7b22f-115">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="7b22f-116">這表示 ACL 端點的類型。</span><span class="sxs-lookup"><span data-stu-id="7b22f-116">This indicates the type of ACL endpoint.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7b22f-117">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="7b22f-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="MAC_Acl"></span><span id="mac_acl"></span><span id="MAC_ACL"></span>

<span data-ttu-id="7b22f-118">**MAC Acl** (1) </span><span class="sxs-lookup"><span data-stu-id="7b22f-118">**MAC Acl** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_Acl"></span><span id="ipv4_acl"></span><span id="IPV4_ACL"></span>

<span data-ttu-id="7b22f-119">**IPv4 Acl** (2) </span><span class="sxs-lookup"><span data-stu-id="7b22f-119">**IPv4 Acl** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6_Acl"></span><span id="ipv6_acl"></span><span id="IPV6_ACL"></span>

<span data-ttu-id="7b22f-120">**IPv6 Acl** (3) </span><span class="sxs-lookup"><span data-stu-id="7b22f-120">**IPv6 Acl** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7b22f-121">**動作**</span><span class="sxs-lookup"><span data-stu-id="7b22f-121">**Action**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22f-122">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="7b22f-122">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7b22f-123">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7b22f-123">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7b22f-124">限定詞： **WmiDataId** (5) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="7b22f-124">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="7b22f-125">這表示 ACL 的動作。</span><span class="sxs-lookup"><span data-stu-id="7b22f-125">This indicates the action of the ACL.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7b22f-126">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="7b22f-126">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="7b22f-127">**允許** (1) </span><span class="sxs-lookup"><span data-stu-id="7b22f-127">**Allow** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Deny"></span><span id="deny"></span><span id="DENY"></span>

<span data-ttu-id="7b22f-128">**拒絕** (2) </span><span class="sxs-lookup"><span data-stu-id="7b22f-128">**Deny** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Meter"></span><span id="meter"></span><span id="METER"></span>

<span data-ttu-id="7b22f-129">**計量** (3) </span><span class="sxs-lookup"><span data-stu-id="7b22f-129">**Meter** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7b22f-130">**適用性**</span><span class="sxs-lookup"><span data-stu-id="7b22f-130">**Applicability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22f-131">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="7b22f-131">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7b22f-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7b22f-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7b22f-133">限定詞： **WmiDataId** (3) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="7b22f-133">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="7b22f-134">這表示 ACL 是否適用于本機或遠端端點。</span><span class="sxs-lookup"><span data-stu-id="7b22f-134">This indicates whether the ACL applies to the local or remote endpoint.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7b22f-135">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="7b22f-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Local"></span><span id="local"></span><span id="LOCAL"></span>

<span data-ttu-id="7b22f-136">**本機** (1) </span><span class="sxs-lookup"><span data-stu-id="7b22f-136">**Local** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Remote"></span><span id="remote"></span><span id="REMOTE"></span>

<span data-ttu-id="7b22f-137">**遠端** (2) </span><span class="sxs-lookup"><span data-stu-id="7b22f-137">**Remote** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7b22f-138">**標題**</span><span class="sxs-lookup"><span data-stu-id="7b22f-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22f-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7b22f-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b22f-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b22f-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22f-141">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="7b22f-141">A short description of the object.</span></span> <span data-ttu-id="7b22f-142">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器通訊埠 ACL 設定」。</span><span class="sxs-lookup"><span data-stu-id="7b22f-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port ACL Settings".</span></span>

</dd> <dt>

<span data-ttu-id="7b22f-143">**說明**</span><span class="sxs-lookup"><span data-stu-id="7b22f-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22f-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7b22f-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b22f-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b22f-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22f-146">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="7b22f-146">A description of the object.</span></span> <span data-ttu-id="7b22f-147">這個屬性是從 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)繼承而來，而且一律設定為「代表交換器埠設定的基類」。</span><span class="sxs-lookup"><span data-stu-id="7b22f-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the base class for switch port settings.".</span></span>

</dd> <dt>

<span data-ttu-id="7b22f-148">[方向]</span><span class="sxs-lookup"><span data-stu-id="7b22f-148">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22f-149">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="7b22f-149">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7b22f-150">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7b22f-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7b22f-151">限定詞： **WmiDataId** (2) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="7b22f-151">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="7b22f-152">這表示 ACL 是否適用于輸入或輸出方向。</span><span class="sxs-lookup"><span data-stu-id="7b22f-152">This indicates whether the ACL applies to ingress or egress direction.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7b22f-153">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="7b22f-153">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Incoming"></span><span id="incoming"></span><span id="INCOMING"></span>

<span data-ttu-id="7b22f-154">**傳入** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="7b22f-154">**Incoming** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Outgoing"></span><span id="outgoing"></span><span id="OUTGOING"></span>

<span data-ttu-id="7b22f-155">連 **出** (2) </span><span class="sxs-lookup"><span data-stu-id="7b22f-155">**Outgoing** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7b22f-156">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7b22f-156">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22f-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7b22f-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b22f-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b22f-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22f-159">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="7b22f-159">A display name for the object.</span></span> <span data-ttu-id="7b22f-160">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器通訊埠 ACL 設定」。</span><span class="sxs-lookup"><span data-stu-id="7b22f-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port ACL Settings".</span></span>

</dd> <dt>

<span data-ttu-id="7b22f-161">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7b22f-161">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22f-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7b22f-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b22f-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b22f-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b22f-164">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="7b22f-164">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7b22f-165">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="7b22f-165">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="7b22f-166">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="7b22f-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7b22f-167">**LocalAddress**</span><span class="sxs-lookup"><span data-stu-id="7b22f-167">**LocalAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22f-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7b22f-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b22f-169">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7b22f-169">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7b22f-170">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40) 、 **WmiDataId** (6) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="7b22f-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="7b22f-171">虛擬機器的本機位址。</span><span class="sxs-lookup"><span data-stu-id="7b22f-171">The local address of the virtual machine.</span></span> <span data-ttu-id="7b22f-172">這可以是 IPv4、IPv6 或 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="7b22f-172">This can be an IPv4, IPv6, or a MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="7b22f-173">**LocalAddressPrefixLength**</span><span class="sxs-lookup"><span data-stu-id="7b22f-173">**LocalAddressPrefixLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22f-174">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="7b22f-174">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7b22f-175">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7b22f-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7b22f-176">限定詞： **WmiDataId** (7) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="7b22f-176">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="7b22f-177">本機位址前置長度。</span><span class="sxs-lookup"><span data-stu-id="7b22f-177">The local address prefix length.</span></span>

</dd> <dt>

<span data-ttu-id="7b22f-178">**名稱**</span><span class="sxs-lookup"><span data-stu-id="7b22f-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22f-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7b22f-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b22f-180">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7b22f-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7b22f-181">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 、 **WmiDataId** (1) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="7b22f-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="7b22f-182">ACL 的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="7b22f-182">The display name of the ACL.</span></span>

</dd> <dt>

<span data-ttu-id="7b22f-183">**RemoteAddress**</span><span class="sxs-lookup"><span data-stu-id="7b22f-183">**RemoteAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22f-184">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7b22f-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b22f-185">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7b22f-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7b22f-186">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40) 、 **WmiDataId** (8) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="7b22f-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="7b22f-187">虛擬機器的遠端位址。</span><span class="sxs-lookup"><span data-stu-id="7b22f-187">The remote address of the virtual machine.</span></span> <span data-ttu-id="7b22f-188">這可以是 IPv4、IPv6 或 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="7b22f-188">This can be IPv4, IPv6, or a MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="7b22f-189">**RemoteAddressPrefixLength**</span><span class="sxs-lookup"><span data-stu-id="7b22f-189">**RemoteAddressPrefixLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22f-190">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="7b22f-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7b22f-191">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7b22f-191">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7b22f-192">限定詞： **WmiDataId** (9) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="7b22f-192">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="7b22f-193">遠端位址前置長度。</span><span class="sxs-lookup"><span data-stu-id="7b22f-193">The remote address prefix length.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b22f-194">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b22f-194">Requirements</span></span>



| <span data-ttu-id="7b22f-195">需求</span><span class="sxs-lookup"><span data-stu-id="7b22f-195">Requirement</span></span> | <span data-ttu-id="7b22f-196">值</span><span class="sxs-lookup"><span data-stu-id="7b22f-196">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b22f-197">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7b22f-197">Minimum supported client</span></span><br/> | <span data-ttu-id="7b22f-198">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b22f-198">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7b22f-199">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7b22f-199">Minimum supported server</span></span><br/> | <span data-ttu-id="7b22f-200">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b22f-200">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7b22f-201">命名空間</span><span class="sxs-lookup"><span data-stu-id="7b22f-201">Namespace</span></span><br/>                | <span data-ttu-id="7b22f-202">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="7b22f-202">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7b22f-203">MOF</span><span class="sxs-lookup"><span data-stu-id="7b22f-203">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b22f-204"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="7b22f-204"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b22f-205">DLL</span><span class="sxs-lookup"><span data-stu-id="7b22f-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b22f-206"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7b22f-206"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

