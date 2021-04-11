---
description: 代表客體作業系統內網路介面卡的設定。
ms.assetid: 154d4a0f-0c57-496a-a351-6caa74011544
title: Msvm_GuestNetworkAdapterConfiguration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestNetworkAdapterConfiguration
- Msvm_GuestNetworkAdapterConfiguration.InstanceID
- Msvm_GuestNetworkAdapterConfiguration.ProtocolIFType
- Msvm_GuestNetworkAdapterConfiguration.DHCPEnabled
- Msvm_GuestNetworkAdapterConfiguration.IPAddresses
- Msvm_GuestNetworkAdapterConfiguration.Subnets
- Msvm_GuestNetworkAdapterConfiguration.DefaultGateways
- Msvm_GuestNetworkAdapterConfiguration.DNSServers
- Msvm_GuestNetworkAdapterConfiguration.IPAddressOrigins
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ce5738bca4563aa77678cac2b7e33f5c4d5323e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113633"
---
# <a name="msvm_guestnetworkadapterconfiguration-class"></a><span data-ttu-id="87564-103">Msvm \_ GuestNetworkAdapterConfiguration 類別</span><span class="sxs-lookup"><span data-stu-id="87564-103">Msvm\_GuestNetworkAdapterConfiguration class</span></span>

<span data-ttu-id="87564-104">代表客體作業系統內網路介面卡的設定。</span><span class="sxs-lookup"><span data-stu-id="87564-104">Represents the configuration of a network adapter within the guest operating system.</span></span>

<span data-ttu-id="87564-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="87564-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="87564-106">語法</span><span class="sxs-lookup"><span data-stu-id="87564-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestNetworkAdapterConfiguration
{
  string  InstanceID;
  uint16  ProtocolIFType;
  boolean DHCPEnabled;
  string  IPAddresses[];
  string  Subnets[];
  string  DefaultGateways[];
  string  DNSServers[];
  UINT16  IPAddressOrigins[];
};
```

## <a name="members"></a><span data-ttu-id="87564-107">成員</span><span class="sxs-lookup"><span data-stu-id="87564-107">Members</span></span>

<span data-ttu-id="87564-108">**Msvm \_ GuestNetworkAdapterConfiguration** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="87564-108">The **Msvm\_GuestNetworkAdapterConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="87564-109">屬性</span><span class="sxs-lookup"><span data-stu-id="87564-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="87564-110">屬性</span><span class="sxs-lookup"><span data-stu-id="87564-110">Properties</span></span>

<span data-ttu-id="87564-111">**Msvm \_ GuestNetworkAdapterConfiguration** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="87564-111">The **Msvm\_GuestNetworkAdapterConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="87564-112">**DefaultGateways**</span><span class="sxs-lookup"><span data-stu-id="87564-112">**DefaultGateways**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87564-113">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="87564-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="87564-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="87564-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87564-115">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="87564-115">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="87564-116">字串陣列，其中包含在客體作業系統內的網路介面卡上設定的預設 IP 閘道。</span><span class="sxs-lookup"><span data-stu-id="87564-116">An array of strings that contain the default IP gateways configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="87564-117">可以在單一網路介面卡上設定之預設 IP 閘道的最大數目為五。</span><span class="sxs-lookup"><span data-stu-id="87564-117">The maximum number of default IP gateways that may be configured on a single network adapter is five.</span></span>

</dd> <dt>

<span data-ttu-id="87564-118">**DHCPEnabled**</span><span class="sxs-lookup"><span data-stu-id="87564-118">**DHCPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87564-119">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="87564-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="87564-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="87564-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87564-121">指定是否在客體作業系統內的網路介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="87564-121">Specifies whether DHCP is enabled on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="87564-122">**DNSServers**</span><span class="sxs-lookup"><span data-stu-id="87564-122">**DNSServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87564-123">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="87564-123">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="87564-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="87564-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87564-125">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="87564-125">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="87564-126">字串陣列，其中包含在客體作業系統內的網路介面卡上設定的 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="87564-126">An array of strings that contain the DNS servers configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="87564-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="87564-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87564-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="87564-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87564-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="87564-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87564-130">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="87564-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="87564-131">這個物件的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="87564-131">The unique identifier for this object.</span></span>

</dd> <dt>

<span data-ttu-id="87564-132">**IPAddresses**</span><span class="sxs-lookup"><span data-stu-id="87564-132">**IPAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87564-133">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="87564-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="87564-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="87564-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87564-135">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="87564-135">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="87564-136">字串陣列，其中包含在客體作業系統內的網路介面卡上設定的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="87564-136">An array of strings that contain the IP addresses configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="87564-137">**IPAddressOrigins**</span><span class="sxs-lookup"><span data-stu-id="87564-137">**IPAddressOrigins**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87564-138">資料類型： **UINT16** 陣列</span><span class="sxs-lookup"><span data-stu-id="87564-138">Data type: **UINT16** array</span></span>
</dt> <dt>

<span data-ttu-id="87564-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="87564-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87564-140">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="87564-140">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="87564-141">在客體作業系統內的網路介面卡上設定的 IP 位址來源。</span><span class="sxs-lookup"><span data-stu-id="87564-141">The source of the IP addresses configured on the network adapter within the guest operating system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="87564-142">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="87564-142">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="87564-143">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="87564-143">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Static"></span><span id="static"></span><span id="STATIC"></span>

<span data-ttu-id="87564-144">**靜態** (2) </span><span class="sxs-lookup"><span data-stu-id="87564-144">**Static** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="87564-145">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="87564-145">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87564-146">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="87564-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="87564-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="87564-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87564-148">識別此實例所指定的設定適用的 IP 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="87564-148">Identifies the IP protocols that the settings specified by this instance apply to.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="87564-149">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="87564-149">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="87564-150">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="87564-150">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="87564-151">**IPv4** (4096) </span><span class="sxs-lookup"><span data-stu-id="87564-151">**IPv4** (4096)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="87564-152">**IPv6** (4097) </span><span class="sxs-lookup"><span data-stu-id="87564-152">**IPv6** (4097)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

<span data-ttu-id="87564-153">**IPv4/v6** (4098) </span><span class="sxs-lookup"><span data-stu-id="87564-153">**IPv4/v6** (4098)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="87564-154">**子網路**</span><span class="sxs-lookup"><span data-stu-id="87564-154">**Subnets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87564-155">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="87564-155">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="87564-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="87564-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87564-157">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="87564-157">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="87564-158">字串陣列，其中包含在客體作業系統內的網路介面卡上設定的子網。</span><span class="sxs-lookup"><span data-stu-id="87564-158">An array of strings that contain the subnets configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="87564-159">這個陣列中的每個元素都會套用至 **IPAddresses** 陣列中的對應元素。</span><span class="sxs-lookup"><span data-stu-id="87564-159">Each element in this array applies to the corresponding element in the **IPAddresses** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="87564-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="87564-160">Requirements</span></span>



| <span data-ttu-id="87564-161">需求</span><span class="sxs-lookup"><span data-stu-id="87564-161">Requirement</span></span> | <span data-ttu-id="87564-162">值</span><span class="sxs-lookup"><span data-stu-id="87564-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87564-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87564-163">Minimum supported client</span></span><br/> | <span data-ttu-id="87564-164">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87564-164">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="87564-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87564-165">Minimum supported server</span></span><br/> | <span data-ttu-id="87564-166">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87564-166">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="87564-167">命名空間</span><span class="sxs-lookup"><span data-stu-id="87564-167">Namespace</span></span><br/>                | <span data-ttu-id="87564-168">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="87564-168">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="87564-169">MOF</span><span class="sxs-lookup"><span data-stu-id="87564-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87564-170"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="87564-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="87564-171">DLL</span><span class="sxs-lookup"><span data-stu-id="87564-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87564-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="87564-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

