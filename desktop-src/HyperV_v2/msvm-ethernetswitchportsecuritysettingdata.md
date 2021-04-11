---
description: 表示設定資料的安全性功能。
ms.assetid: 98e0de24-ccdc-4fc7-86a5-b68d454fde9d
title: Msvm_EthernetSwitchPortSecuritySettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortSecuritySettingData
- Msvm_EthernetSwitchPortSecuritySettingData.InstanceID
- Msvm_EthernetSwitchPortSecuritySettingData.Caption
- Msvm_EthernetSwitchPortSecuritySettingData.Description
- Msvm_EthernetSwitchPortSecuritySettingData.ElementName
- Msvm_EthernetSwitchPortSecuritySettingData.AllowMacSpoofing
- Msvm_EthernetSwitchPortSecuritySettingData.EnableDhcpGuard
- Msvm_EthernetSwitchPortSecuritySettingData.EnableRouterGuard
- Msvm_EthernetSwitchPortSecuritySettingData.MonitorMode
- Msvm_EthernetSwitchPortSecuritySettingData.MonitorSession
- Msvm_EthernetSwitchPortSecuritySettingData.AllowIeeePriorityTag
- Msvm_EthernetSwitchPortSecuritySettingData.VirtualSubnetId
- Msvm_EthernetSwitchPortSecuritySettingData.AllowTeaming
- Msvm_EthernetSwitchPortSecuritySettingData.TeamName
- Msvm_EthernetSwitchPortSecuritySettingData.TeamNumber
- Msvm_EthernetSwitchPortSecuritySettingData.EnableFixSpeed10G
- Msvm_EthernetSwitchPortSecuritySettingData.Reserved
- Msvm_EthernetSwitchPortSecuritySettingData.DynamicIPAddressLimit
- Msvm_EthernetSwitchPortSecuritySettingData.StormLimit
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8d37913f015a3ffbfaa751a7bbb10f79cea2fb39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853152"
---
# <a name="msvm_ethernetswitchportsecuritysettingdata-class"></a><span data-ttu-id="94425-103">Msvm \_ EthernetSwitchPortSecuritySettingData 類別</span><span class="sxs-lookup"><span data-stu-id="94425-103">Msvm\_EthernetSwitchPortSecuritySettingData class</span></span>

<span data-ttu-id="94425-104">表示設定資料的安全性功能。</span><span class="sxs-lookup"><span data-stu-id="94425-104">Represents the security feature setting data.</span></span>

<span data-ttu-id="94425-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="94425-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="94425-106">語法</span><span class="sxs-lookup"><span data-stu-id="94425-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("776E0BA7-94A1-41C8-8F28-951F524251B5"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("3"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Security Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortSecuritySettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Security Settings";
  string  Description = "Represents the security feature setting data.";
  string  ElementName = "Ethernet Switch Port Security Settings";
  boolean AllowMacSpoofing = FALSE;
  boolean EnableDhcpGuard = FALSE;
  boolean EnableRouterGuard = FALSE;
  uint8   MonitorMode = 0;
  uint8   MonitorSession = 0;
  boolean AllowIeeePriorityTag = FALSE;
  uint32  VirtualSubnetId = 0;
  boolean AllowTeaming = FALSE;
  string  TeamName = ;
  uint32  TeamNumber = 0;
  boolean EnableFixSpeed10G = FALSE;
  boolean Reserved = FALSE;
  uint32  DynamicIPAddressLimit = 0;
  uint32  StormLimit = 0;
};
```

## <a name="members"></a><span data-ttu-id="94425-107">成員</span><span class="sxs-lookup"><span data-stu-id="94425-107">Members</span></span>

<span data-ttu-id="94425-108">**Msvm \_ EthernetSwitchPortSecuritySettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="94425-108">The **Msvm\_EthernetSwitchPortSecuritySettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="94425-109">屬性</span><span class="sxs-lookup"><span data-stu-id="94425-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="94425-110">屬性</span><span class="sxs-lookup"><span data-stu-id="94425-110">Properties</span></span>

<span data-ttu-id="94425-111">**Msvm \_ EthernetSwitchPortSecuritySettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="94425-111">The **Msvm\_EthernetSwitchPortSecuritySettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="94425-112">**AllowIeeePriorityTag**</span><span class="sxs-lookup"><span data-stu-id="94425-112">**AllowIeeePriorityTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94425-113">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="94425-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94425-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="94425-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="94425-115">限定詞： **WmiDataId** (6) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="94425-115">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="94425-116">指定進出埠的流量是否保留 802.1 P 資訊。</span><span class="sxs-lookup"><span data-stu-id="94425-116">Specifies whether traffic to/from the port retains 802.1P information.</span></span> <span data-ttu-id="94425-117">如果埠的流量保留 802.1 P 資訊，則包含 **True** ，否則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="94425-117">Contains **True** if traffic to/from the port retains 802.1P information or **False** otherwise.</span></span> <span data-ttu-id="94425-118">預設值為 **[False]** 。</span><span class="sxs-lookup"><span data-stu-id="94425-118">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="94425-119">**AllowMacSpoofing**</span><span class="sxs-lookup"><span data-stu-id="94425-119">**AllowMacSpoofing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94425-120">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="94425-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94425-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="94425-121">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="94425-122">限定詞： **WmiDataId** (1) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="94425-122">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="94425-123">指出埠是否會允許 MAC 詐騙。</span><span class="sxs-lookup"><span data-stu-id="94425-123">Indicates whether the port will allow MAC spoofing.</span></span> <span data-ttu-id="94425-124">如果這個屬性為 **True**，埠將允許 MAC 位址成為詐騙。</span><span class="sxs-lookup"><span data-stu-id="94425-124">If this property is **True**, the port will allow MAC addresses to be spoofed.</span></span> <span data-ttu-id="94425-125">允許所有有效的單播 MAC 位址值。</span><span class="sxs-lookup"><span data-stu-id="94425-125">All valid unicast MAC address values are allowed.</span></span> <span data-ttu-id="94425-126">如果此屬性為 **False**，埠將只允許使用在 hyper-v 管理內設定的 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="94425-126">If this property is **False**, the port will only allow MAC addresses that are configured within Hyper-V management to be used.</span></span> <span data-ttu-id="94425-127">預設值為 **[False]** 。</span><span class="sxs-lookup"><span data-stu-id="94425-127">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="94425-128">**AllowTeaming**</span><span class="sxs-lookup"><span data-stu-id="94425-128">**AllowTeaming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94425-129">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="94425-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94425-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="94425-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="94425-131">限定詞： **WmiDataId** (8) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="94425-131">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="94425-132">指出連線到埠的 Nic 是否可以是小組的一部分。</span><span class="sxs-lookup"><span data-stu-id="94425-132">Indicates whether the NICs connected to the port can be part of a team.</span></span> <span data-ttu-id="94425-133">這僅適用于連線至虛擬機器的 Nic。</span><span class="sxs-lookup"><span data-stu-id="94425-133">This applies only to NICs connected to virtual machines.</span></span> <span data-ttu-id="94425-134">如果允許 NIC 小組，則包含 **True** ，否則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="94425-134">Contains **True** if NIC teaming is allowed or **False** otherwise.</span></span> <span data-ttu-id="94425-135">預設值為 **[False]** 。</span><span class="sxs-lookup"><span data-stu-id="94425-135">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="94425-136">**標題**</span><span class="sxs-lookup"><span data-stu-id="94425-136">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94425-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="94425-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94425-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="94425-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94425-139">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="94425-139">A short description of the object.</span></span> <span data-ttu-id="94425-140">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器通訊埠安全性設定」。</span><span class="sxs-lookup"><span data-stu-id="94425-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Security Settings".</span></span>

</dd> <dt>

<span data-ttu-id="94425-141">**說明**</span><span class="sxs-lookup"><span data-stu-id="94425-141">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94425-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="94425-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94425-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="94425-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94425-144">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="94425-144">A description of the object.</span></span> <span data-ttu-id="94425-145">這個屬性是從 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)繼承而來，而且一律設定為「代表安全性功能設定資料」。</span><span class="sxs-lookup"><span data-stu-id="94425-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the security feature setting data.".</span></span>

</dd> <dt>

<span data-ttu-id="94425-146">**DynamicIPAddressLimit**</span><span class="sxs-lookup"><span data-stu-id="94425-146">**DynamicIPAddressLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94425-147">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="94425-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="94425-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="94425-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="94425-149">限定詞： **WmiDataId** (12) 、 **InterfaceVersion** (2) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="94425-149">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="94425-150">定義所學到的動態 IP 位址數目限制。</span><span class="sxs-lookup"><span data-stu-id="94425-150">Defines the limit for number of Dynamic IP addresses learned.</span></span> <span data-ttu-id="94425-151">預設值為 none。</span><span class="sxs-lookup"><span data-stu-id="94425-151">Default is none.</span></span>

</dd> <dt>

<span data-ttu-id="94425-152">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="94425-152">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94425-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="94425-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94425-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="94425-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94425-155">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="94425-155">A display name for the object.</span></span> <span data-ttu-id="94425-156">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器通訊埠安全性設定」。</span><span class="sxs-lookup"><span data-stu-id="94425-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Security Settings".</span></span>

</dd> <dt>

<span data-ttu-id="94425-157">**EnableDhcpGuard**</span><span class="sxs-lookup"><span data-stu-id="94425-157">**EnableDhcpGuard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94425-158">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="94425-158">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94425-159">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="94425-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="94425-160">限定詞： **WmiDataId** (2) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="94425-160">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="94425-161">指定是否封鎖來自埠的 DHCP 供應專案。</span><span class="sxs-lookup"><span data-stu-id="94425-161">Specifies whether DHCP offers are blocked from the port.</span></span> <span data-ttu-id="94425-162">如果從埠封鎖 DHCP 供應專案，則包含 **True** ，否則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="94425-162">Contains **True** if DHCP offers are blocked from the port or **False** otherwise.</span></span> <span data-ttu-id="94425-163">預設值為 **[False]** 。</span><span class="sxs-lookup"><span data-stu-id="94425-163">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="94425-164">**EnableFixSpeed10G**</span><span class="sxs-lookup"><span data-stu-id="94425-164">**EnableFixSpeed10G**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94425-165">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="94425-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94425-166">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="94425-166">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="94425-167">限定詞： **WmiDataId** (14) 、 **InterfaceVersion** (3) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="94425-167">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="94425-168">如果已啟用固定速度10G，則設定為 TRUE，否則為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="94425-168">Set to TRUE if Fixed Speed 10G is enabled else FALSE.</span></span> <span data-ttu-id="94425-169">預設值為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="94425-169">Default value is FALSE.</span></span>

> [!Note]  
> <span data-ttu-id="94425-170">在 Windows 10 中新增的屬性。</span><span class="sxs-lookup"><span data-stu-id="94425-170">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="94425-171">**EnableRouterGuard**</span><span class="sxs-lookup"><span data-stu-id="94425-171">**EnableRouterGuard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94425-172">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="94425-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94425-173">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="94425-173">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="94425-174">限定詞： **WmiDataId** (3) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="94425-174">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="94425-175">指定是否封鎖來自埠的路由器通告和路由器重新導向。</span><span class="sxs-lookup"><span data-stu-id="94425-175">Specifies whether router advertisements and router redirects are blocked from the port.</span></span> <span data-ttu-id="94425-176">如果從埠封鎖路由器通告和路由器重新導向，則包含 **True** ，否則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="94425-176">Contains **True** if router advertisements and router redirects are blocked from the port or **False** otherwise.</span></span> <span data-ttu-id="94425-177">預設值為 **[False]** 。</span><span class="sxs-lookup"><span data-stu-id="94425-177">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="94425-178">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="94425-178">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94425-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="94425-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94425-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="94425-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94425-181">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="94425-181">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="94425-182">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="94425-182">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="94425-183">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="94425-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="94425-184">**MonitorMode**</span><span class="sxs-lookup"><span data-stu-id="94425-184">**MonitorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94425-185">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="94425-185">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="94425-186">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="94425-186">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="94425-187">限定詞： **WmiDataId** (4) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="94425-187">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="94425-188">這表示埠的監視器模式。</span><span class="sxs-lookup"><span data-stu-id="94425-188">This indicates the monitor mode of the port.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="94425-189">**無** (0) </span><span class="sxs-lookup"><span data-stu-id="94425-189">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Destination"></span><span id="destination"></span><span id="DESTINATION"></span>

<span data-ttu-id="94425-190">**目的地** (1) </span><span class="sxs-lookup"><span data-stu-id="94425-190">**Destination** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>

<span data-ttu-id="94425-191">**來源** (2) </span><span class="sxs-lookup"><span data-stu-id="94425-191">**Source** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="94425-192">**MonitorSession**</span><span class="sxs-lookup"><span data-stu-id="94425-192">**MonitorSession**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94425-193">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="94425-193">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="94425-194">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="94425-194">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="94425-195">限定詞： **WmiDataId** (5) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="94425-195">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="94425-196">指定此埠所屬監視會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="94425-196">Specifies the identifier of the monitor session this port belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="94425-197">**已保留**</span><span class="sxs-lookup"><span data-stu-id="94425-197">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94425-198">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="94425-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94425-199">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="94425-199">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="94425-200">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「沒有值」 ) 、 **WmiDataId** (13) 、 **InterfaceVersion** (3) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="94425-200">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), **WmiDataId** (13), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="94425-201">保留</span><span class="sxs-lookup"><span data-stu-id="94425-201">Reserved</span></span>

> [!Note]  
> <span data-ttu-id="94425-202">在 Windows 10 中新增的屬性。</span><span class="sxs-lookup"><span data-stu-id="94425-202">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="94425-203">**StormLimit**</span><span class="sxs-lookup"><span data-stu-id="94425-203">**StormLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94425-204">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="94425-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="94425-205">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="94425-205">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="94425-206">限定詞： **WmiDataId** (11) 、 **InterfaceVersion** (2) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="94425-206">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="94425-207">定義廣播和多播流量的每秒封包限制。</span><span class="sxs-lookup"><span data-stu-id="94425-207">Defines the packets per second limit for broadcast and multicast traffic.</span></span> <span data-ttu-id="94425-208">預設值為 none。</span><span class="sxs-lookup"><span data-stu-id="94425-208">Default is none.</span></span>

</dd> <dt>

<span data-ttu-id="94425-209">**TeamName**</span><span class="sxs-lookup"><span data-stu-id="94425-209">**TeamName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94425-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="94425-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94425-211">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="94425-211">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="94425-212">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127) 、 **WmiDataId** (9) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="94425-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="94425-213">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="94425-213">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="94425-214">**TeamNumber**</span><span class="sxs-lookup"><span data-stu-id="94425-214">**TeamNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94425-215">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="94425-215">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="94425-216">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="94425-216">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="94425-217">限定詞： **WmiDataId** (10) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="94425-217">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="94425-218">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="94425-218">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="94425-219">**VirtualSubnetId**</span><span class="sxs-lookup"><span data-stu-id="94425-219">**VirtualSubnetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94425-220">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="94425-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="94425-221">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="94425-221">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="94425-222">限定詞： **WmiDataId** (7) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 、 [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0 [**) 、int32.maxvalue (16777215)**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="94425-222">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (16777215)</span></span>
</dt> </dl>

<span data-ttu-id="94425-223">指定埠為其成員之虛擬子網的識別碼。</span><span class="sxs-lookup"><span data-stu-id="94425-223">Specifies the identifier of the virtual subnet that the port is a member of.</span></span> <span data-ttu-id="94425-224">預設值是 [none]。</span><span class="sxs-lookup"><span data-stu-id="94425-224">The default is none.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94425-225">規格需求</span><span class="sxs-lookup"><span data-stu-id="94425-225">Requirements</span></span>



| <span data-ttu-id="94425-226">需求</span><span class="sxs-lookup"><span data-stu-id="94425-226">Requirement</span></span> | <span data-ttu-id="94425-227">值</span><span class="sxs-lookup"><span data-stu-id="94425-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94425-228">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="94425-228">Minimum supported client</span></span><br/> | <span data-ttu-id="94425-229">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="94425-229">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="94425-230">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="94425-230">Minimum supported server</span></span><br/> | <span data-ttu-id="94425-231">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="94425-231">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="94425-232">命名空間</span><span class="sxs-lookup"><span data-stu-id="94425-232">Namespace</span></span><br/>                | <span data-ttu-id="94425-233">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="94425-233">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="94425-234">MOF</span><span class="sxs-lookup"><span data-stu-id="94425-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94425-235"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="94425-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="94425-236">DLL</span><span class="sxs-lookup"><span data-stu-id="94425-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94425-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="94425-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

