---
description: 代表客體作業系統內網路介面卡的設定，這些設定將在容錯移轉時套用。
ms.assetid: d7f2d471-7328-4181-b94e-b9127814706e
title: Msvm_FailoverNetworkAdapterSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FailoverNetworkAdapterSettingData
- Msvm_FailoverNetworkAdapterSettingData.InstanceID
- Msvm_FailoverNetworkAdapterSettingData.Caption
- Msvm_FailoverNetworkAdapterSettingData.Description
- Msvm_FailoverNetworkAdapterSettingData.ElementName
- Msvm_FailoverNetworkAdapterSettingData.ProtocolIFType
- Msvm_FailoverNetworkAdapterSettingData.DHCPEnabled
- Msvm_FailoverNetworkAdapterSettingData.IPAddresses
- Msvm_FailoverNetworkAdapterSettingData.Subnets
- Msvm_FailoverNetworkAdapterSettingData.DefaultGateways
- Msvm_FailoverNetworkAdapterSettingData.DNSServers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d4989c43dda823be13d604e3ac9b575b62f2f9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972889"
---
# <a name="msvm_failovernetworkadaptersettingdata-class"></a><span data-ttu-id="15834-103">Msvm \_ FailoverNetworkAdapterSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="15834-103">Msvm\_FailoverNetworkAdapterSettingData class</span></span>

<span data-ttu-id="15834-104">代表客體作業系統內網路介面卡的設定，這些設定將在容錯移轉時套用。</span><span class="sxs-lookup"><span data-stu-id="15834-104">Represents the settings for a network adapter within the guest operating system, which will be applied at the time of a failover.</span></span>

<span data-ttu-id="15834-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="15834-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="15834-106">語法</span><span class="sxs-lookup"><span data-stu-id="15834-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FailoverNetworkAdapterSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  uint16  ProtocolIFType;
  boolean DHCPEnabled;
  string  IPAddresses[];
  string  Subnets[];
  string  DefaultGateways[];
  string  DNSServers[];
};
```

## <a name="members"></a><span data-ttu-id="15834-107">成員</span><span class="sxs-lookup"><span data-stu-id="15834-107">Members</span></span>

<span data-ttu-id="15834-108">**Msvm \_ FailoverNetworkAdapterSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="15834-108">The **Msvm\_FailoverNetworkAdapterSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="15834-109">屬性</span><span class="sxs-lookup"><span data-stu-id="15834-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15834-110">屬性</span><span class="sxs-lookup"><span data-stu-id="15834-110">Properties</span></span>

<span data-ttu-id="15834-111">**Msvm \_ FailoverNetworkAdapterSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="15834-111">The **Msvm\_FailoverNetworkAdapterSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15834-112">**標題**</span><span class="sxs-lookup"><span data-stu-id="15834-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15834-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="15834-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15834-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15834-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15834-115">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="15834-115">A short description of the object.</span></span> <span data-ttu-id="15834-116">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="15834-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="15834-117">**DefaultGateways**</span><span class="sxs-lookup"><span data-stu-id="15834-117">**DefaultGateways**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15834-118">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="15834-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="15834-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15834-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15834-120">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="15834-120">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="15834-121">字串陣列，指定客體作業系統內網路介面卡上設定的預設 IP 閘道。</span><span class="sxs-lookup"><span data-stu-id="15834-121">An array of strings that specify the default IP gateways configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="15834-122">可以在單一網路介面卡上設定之預設 IP 閘道的最大數目為五。</span><span class="sxs-lookup"><span data-stu-id="15834-122">The maximum number of default IP gateways that may be configured on a single network adapter is five.</span></span>

</dd> <dt>

<span data-ttu-id="15834-123">**說明**</span><span class="sxs-lookup"><span data-stu-id="15834-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15834-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="15834-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15834-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15834-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15834-126">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="15834-126">A description of the object.</span></span> <span data-ttu-id="15834-127">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="15834-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="15834-128">**DHCPEnabled**</span><span class="sxs-lookup"><span data-stu-id="15834-128">**DHCPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15834-129">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="15834-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="15834-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15834-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15834-131">指定是否在客體作業系統內網路介面卡的 IPv4 介面上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="15834-131">Specifies whether DHCP is enabled on the IPv4 interface of the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="15834-132">**DNSServers**</span><span class="sxs-lookup"><span data-stu-id="15834-132">**DNSServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15834-133">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="15834-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="15834-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15834-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15834-135">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="15834-135">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="15834-136">字串陣列，指定客體作業系統內網路介面卡上設定的 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="15834-136">An array of strings that specify the DNS servers configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="15834-137">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="15834-137">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15834-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="15834-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15834-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15834-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15834-140">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="15834-140">A display name for the object.</span></span> <span data-ttu-id="15834-141">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="15834-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="15834-142">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="15834-142">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15834-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="15834-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15834-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15834-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15834-145">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="15834-145">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="15834-146">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="15834-146">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="15834-147">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="15834-147">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="15834-148">**IPAddresses**</span><span class="sxs-lookup"><span data-stu-id="15834-148">**IPAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15834-149">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="15834-149">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="15834-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15834-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15834-151">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="15834-151">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="15834-152">字串陣列，指定客體作業系統內網路介面卡上設定的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="15834-152">An array of strings that specify the IP addresses configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="15834-153">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="15834-153">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15834-154">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="15834-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15834-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15834-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15834-156">識別此實例所指定的設定適用的網際網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="15834-156">Identifies the Internet protocols that the settings specified by this instance apply to.</span></span> <span data-ttu-id="15834-157">這必須是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="15834-157">This must be one of the following values.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="15834-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="15834-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="15834-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="15834-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="15834-160"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096) </span><span class="sxs-lookup"><span data-stu-id="15834-160"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="15834-161"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097) </span><span class="sxs-lookup"><span data-stu-id="15834-161"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

<span data-ttu-id="15834-162"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098) </span><span class="sxs-lookup"><span data-stu-id="15834-162"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098)</span></span>


</dt> <dd>

<span data-ttu-id="15834-163">IPv4/IPv6</span><span class="sxs-lookup"><span data-stu-id="15834-163">IPv4/IPv6</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="15834-164">**子網路**</span><span class="sxs-lookup"><span data-stu-id="15834-164">**Subnets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15834-165">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="15834-165">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="15834-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15834-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15834-167">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="15834-167">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="15834-168">字串陣列，指定客體作業系統內網路介面卡上設定的子網。</span><span class="sxs-lookup"><span data-stu-id="15834-168">An array of strings that specify the subnets configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="15834-169">這個陣列中的每個元素都會套用至 **IPAddresses** 陣列中的對應元素。</span><span class="sxs-lookup"><span data-stu-id="15834-169">Each element in this array applies to the corresponding element in the **IPAddresses** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15834-170">規格需求</span><span class="sxs-lookup"><span data-stu-id="15834-170">Requirements</span></span>



| <span data-ttu-id="15834-171">需求</span><span class="sxs-lookup"><span data-stu-id="15834-171">Requirement</span></span> | <span data-ttu-id="15834-172">值</span><span class="sxs-lookup"><span data-stu-id="15834-172">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15834-173">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15834-173">Minimum supported client</span></span><br/> | <span data-ttu-id="15834-174">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15834-174">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="15834-175">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15834-175">Minimum supported server</span></span><br/> | <span data-ttu-id="15834-176">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15834-176">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="15834-177">命名空間</span><span class="sxs-lookup"><span data-stu-id="15834-177">Namespace</span></span><br/>                | <span data-ttu-id="15834-178">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="15834-178">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="15834-179">MOF</span><span class="sxs-lookup"><span data-stu-id="15834-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15834-180"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="15834-180"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="15834-181">DLL</span><span class="sxs-lookup"><span data-stu-id="15834-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15834-182"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="15834-182"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

