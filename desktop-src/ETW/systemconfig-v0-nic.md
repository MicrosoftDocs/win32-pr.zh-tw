---
description: 此類別是網路介面卡設定事件的事件種類類別。
ms.assetid: 1cae611b-fb6a-4416-8fd4-0c882e8aa5e6
title: SystemConfig_V0_NIC 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_NIC
- SystemConfig_V0_NIC.NICName
- SystemConfig_V0_NIC.Index
- SystemConfig_V0_NIC.PhysicalAddrLen
- SystemConfig_V0_NIC.PhysicalAddr
- SystemConfig_V0_NIC.Size
- SystemConfig_V0_NIC.IpAddress
- SystemConfig_V0_NIC.SubnetMask
- SystemConfig_V0_NIC.DhcpServer
- SystemConfig_V0_NIC.Gateway
- SystemConfig_V0_NIC.PrimaryWinsServer
- SystemConfig_V0_NIC.SecondaryWinsServer
- SystemConfig_V0_NIC.DnsServer1
- SystemConfig_V0_NIC.DnsServer2
- SystemConfig_V0_NIC.DnsServer3
- SystemConfig_V0_NIC.DnsServer4
- SystemConfig_V0_NIC.Data
api_type:
- NA
api_location: ''
ms.openlocfilehash: 040c409564c0ad37e5208c1e91962d3f04de5fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973648"
---
# <a name="systemconfig_v0_nic-class"></a><span data-ttu-id="c1990-103">SystemConfig \_ V0 \_ NIC 類別</span><span class="sxs-lookup"><span data-stu-id="c1990-103">SystemConfig\_V0\_NIC class</span></span>

<span data-ttu-id="c1990-104">此類別是網路介面卡設定事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="c1990-104">This class is the event type class for network interface card configuration events.</span></span>

<span data-ttu-id="c1990-105">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="c1990-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1990-106">語法</span><span class="sxs-lookup"><span data-stu-id="c1990-106">Syntax</span></span>

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_V0_NIC : SystemConfig_V0
{
  char16 NICName[];
  uint32 Index;
  uint32 PhysicalAddrLen;
  char16 PhysicalAddr;
  uint32 Size;
  sint32 IpAddress;
  sint32 SubnetMask;
  sint32 DhcpServer;
  sint32 Gateway;
  sint32 PrimaryWinsServer;
  sint32 SecondaryWinsServer;
  sint32 DnsServer1;
  sint32 DnsServer2;
  sint32 DnsServer3;
  sint32 DnsServer4;
  uint32 Data;
};
```

## <a name="members"></a><span data-ttu-id="c1990-107">成員</span><span class="sxs-lookup"><span data-stu-id="c1990-107">Members</span></span>

<span data-ttu-id="c1990-108">**SystemConfig \_ V0 \_ NIC** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c1990-108">The **SystemConfig\_V0\_NIC** class has these types of members:</span></span>

-   [<span data-ttu-id="c1990-109">屬性</span><span class="sxs-lookup"><span data-stu-id="c1990-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c1990-110">屬性</span><span class="sxs-lookup"><span data-stu-id="c1990-110">Properties</span></span>

<span data-ttu-id="c1990-111">**SystemConfig \_ V0 \_ NIC** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c1990-111">The **SystemConfig\_V0\_NIC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c1990-112">**資料**</span><span class="sxs-lookup"><span data-stu-id="c1990-112">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1990-113">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c1990-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1990-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c1990-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1990-115">限定詞： **WmiDataId** (16) </span><span class="sxs-lookup"><span data-stu-id="c1990-115">Qualifiers: **WmiDataId** (16)</span></span>
</dt> </dl>

<span data-ttu-id="c1990-116">資料欄位。</span><span class="sxs-lookup"><span data-stu-id="c1990-116">Data field.</span></span>

</dd> <dt>

<span data-ttu-id="c1990-117">**DhcpServer**</span><span class="sxs-lookup"><span data-stu-id="c1990-117">**DhcpServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1990-118">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1990-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1990-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c1990-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1990-120">限定詞： **WmiDataId** (8) </span><span class="sxs-lookup"><span data-stu-id="c1990-120">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="c1990-121">動態主機設定通訊協定 (DHCP) server 的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c1990-121">IP address of the dynamic host configuration protocol (DHCP) server.</span></span> <span data-ttu-id="c1990-122">值為255.255.255.255 表示無法連線到 DHCP 伺服器，或正在到達。</span><span class="sxs-lookup"><span data-stu-id="c1990-122">A value of 255.255.255.255 indicates the DHCP server could not be reached, or is in the process of being reached.</span></span> <span data-ttu-id="c1990-123">Sint32 的每個位元組都代表 IP 位址的四個部分中的其中一個)  (p1. p4。</span><span class="sxs-lookup"><span data-stu-id="c1990-123">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="c1990-124">低序位位元組包含 p1 的值，下一個位元組則包含 p2 的值，依此類推。</span><span class="sxs-lookup"><span data-stu-id="c1990-124">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="c1990-125">**DnsServer1**</span><span class="sxs-lookup"><span data-stu-id="c1990-125">**DnsServer1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1990-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1990-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1990-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c1990-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1990-128">限定詞： **WmiDataId** (12) </span><span class="sxs-lookup"><span data-stu-id="c1990-128">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="c1990-129">要用於查詢 DNS 伺服器的第一個伺服器 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c1990-129">First server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="c1990-130">Sint32 的每個位元組都代表 IP 位址的四個部分中的其中一個)  (p1. p4。</span><span class="sxs-lookup"><span data-stu-id="c1990-130">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="c1990-131">低序位位元組包含 p1 的值，下一個位元組則包含 p2 的值，依此類推。</span><span class="sxs-lookup"><span data-stu-id="c1990-131">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="c1990-132">**DnsServer2**</span><span class="sxs-lookup"><span data-stu-id="c1990-132">**DnsServer2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1990-133">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1990-133">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1990-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c1990-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1990-135">限定詞： **WmiDataId** (13) </span><span class="sxs-lookup"><span data-stu-id="c1990-135">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="c1990-136">用來查詢 DNS 伺服器的第二個伺服器 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c1990-136">Second server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="c1990-137">Sint32 的每個位元組都代表 IP 位址的四個部分中的其中一個)  (p1. p4。</span><span class="sxs-lookup"><span data-stu-id="c1990-137">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="c1990-138">低序位位元組包含 p1 的值，下一個位元組則包含 p2 的值，依此類推。</span><span class="sxs-lookup"><span data-stu-id="c1990-138">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="c1990-139">**DnsServer3**</span><span class="sxs-lookup"><span data-stu-id="c1990-139">**DnsServer3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1990-140">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1990-140">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1990-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c1990-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1990-142">限定詞： **WmiDataId** (14) </span><span class="sxs-lookup"><span data-stu-id="c1990-142">Qualifiers: **WmiDataId** (14)</span></span>
</dt> </dl>

<span data-ttu-id="c1990-143">用來查詢 DNS 伺服器的第三個伺服器 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c1990-143">Third server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="c1990-144">Sint32 的每個位元組都代表 IP 位址的四個部分中的其中一個)  (p1. p4。</span><span class="sxs-lookup"><span data-stu-id="c1990-144">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="c1990-145">低序位位元組包含 p1 的值，下一個位元組則包含 p2 的值，依此類推。</span><span class="sxs-lookup"><span data-stu-id="c1990-145">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="c1990-146">**DnsServer4**</span><span class="sxs-lookup"><span data-stu-id="c1990-146">**DnsServer4**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1990-147">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1990-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1990-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c1990-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1990-149">限定詞： **WmiDataId** (15) </span><span class="sxs-lookup"><span data-stu-id="c1990-149">Qualifiers: **WmiDataId** (15)</span></span>
</dt> </dl>

<span data-ttu-id="c1990-150">用來查詢 DNS 伺服器的第四個伺服器 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c1990-150">Fourth server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="c1990-151">Sint32 的每個位元組都代表 IP 位址的四個部分中的其中一個)  (p1. p4。</span><span class="sxs-lookup"><span data-stu-id="c1990-151">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="c1990-152">低序位位元組包含 p1 的值，下一個位元組則包含 p2 的值，依此類推。</span><span class="sxs-lookup"><span data-stu-id="c1990-152">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="c1990-153">**閘道**</span><span class="sxs-lookup"><span data-stu-id="c1990-153">**Gateway**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1990-154">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1990-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1990-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c1990-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1990-156">限定詞： **WmiDataId** (9) </span><span class="sxs-lookup"><span data-stu-id="c1990-156">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="c1990-157">電腦系統使用的預設閘道 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c1990-157">IP address of default gateway that the computer system uses.</span></span> <span data-ttu-id="c1990-158">Sint32 的每個位元組都代表 IP 位址的四個部分中的其中一個)  (p1. p4。</span><span class="sxs-lookup"><span data-stu-id="c1990-158">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="c1990-159">低序位位元組包含 p1 的值，下一個位元組則包含 p2 的值，依此類推。</span><span class="sxs-lookup"><span data-stu-id="c1990-159">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="c1990-160">**Index**</span><span class="sxs-lookup"><span data-stu-id="c1990-160">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1990-161">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c1990-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1990-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c1990-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1990-163">限定詞： **WmiDataId** (2) </span><span class="sxs-lookup"><span data-stu-id="c1990-163">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="c1990-164">介面卡索引。</span><span class="sxs-lookup"><span data-stu-id="c1990-164">Adapter index.</span></span> <span data-ttu-id="c1990-165">介面卡已停用並啟用，或在其他情況下，介面卡索引可能會變更，而且不應該被視為持續性。</span><span class="sxs-lookup"><span data-stu-id="c1990-165">The adapter index may change when an adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.</span></span>

</dd> <dt>

<span data-ttu-id="c1990-166">**IpAddress**</span><span class="sxs-lookup"><span data-stu-id="c1990-166">**IpAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1990-167">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1990-167">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1990-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c1990-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1990-169">限定詞： **WmiDataId** (6) </span><span class="sxs-lookup"><span data-stu-id="c1990-169">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="c1990-170">與網路介面卡相關聯的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c1990-170">IP addresses associated with the network interface card.</span></span> <span data-ttu-id="c1990-171">Sint32 的每個位元組都代表 IP 位址的四個部分中的其中一個)  (p1. p4。</span><span class="sxs-lookup"><span data-stu-id="c1990-171">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="c1990-172">低序位位元組包含 p1 的值，下一個位元組則包含 p2 的值，依此類推。</span><span class="sxs-lookup"><span data-stu-id="c1990-172">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="c1990-173">**NICName**</span><span class="sxs-lookup"><span data-stu-id="c1990-173">**NICName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1990-174">資料類型： **char16** 陣列</span><span class="sxs-lookup"><span data-stu-id="c1990-174">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="c1990-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c1990-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1990-176">限定詞： **WmiDataId** (1) ， **最大** (256) </span><span class="sxs-lookup"><span data-stu-id="c1990-176">Qualifiers: **WmiDataId** (1), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="c1990-177">網路介面卡的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1990-177">Name of the network interface card.</span></span>

</dd> <dt>

<span data-ttu-id="c1990-178">**PhysicalAddr**</span><span class="sxs-lookup"><span data-stu-id="c1990-178">**PhysicalAddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1990-179">資料類型： **char16**</span><span class="sxs-lookup"><span data-stu-id="c1990-179">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="c1990-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c1990-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1990-181">限定詞： **WmiDataId** (4) ， **最大** (8) </span><span class="sxs-lookup"><span data-stu-id="c1990-181">Qualifiers: **WmiDataId** (4), **Max** (8)</span></span>
</dt> </dl>

<span data-ttu-id="c1990-182">介面卡的硬體位址。</span><span class="sxs-lookup"><span data-stu-id="c1990-182">Hardware address for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c1990-183">**PhysicalAddrLen**</span><span class="sxs-lookup"><span data-stu-id="c1990-183">**PhysicalAddrLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1990-184">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c1990-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1990-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c1990-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1990-186">限定詞： **WmiDataId** (3) </span><span class="sxs-lookup"><span data-stu-id="c1990-186">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="c1990-187">介面卡的硬體位址長度。</span><span class="sxs-lookup"><span data-stu-id="c1990-187">Length of the hardware address for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c1990-188">**PrimaryWinsServer**</span><span class="sxs-lookup"><span data-stu-id="c1990-188">**PrimaryWinsServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1990-189">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1990-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1990-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c1990-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1990-191">限定詞： **WmiDataId** (10) </span><span class="sxs-lookup"><span data-stu-id="c1990-191">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="c1990-192">主要 WINS 伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c1990-192">IP address for the primary WINS server.</span></span> <span data-ttu-id="c1990-193">Sint32 的每個位元組都代表 IP 位址的四個部分中的其中一個)  (p1. p4。</span><span class="sxs-lookup"><span data-stu-id="c1990-193">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="c1990-194">低序位位元組包含 p1 的值，下一個位元組則包含 p2 的值，依此類推。</span><span class="sxs-lookup"><span data-stu-id="c1990-194">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="c1990-195">**SecondaryWinsServer**</span><span class="sxs-lookup"><span data-stu-id="c1990-195">**SecondaryWinsServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1990-196">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1990-196">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1990-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c1990-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1990-198">限定詞： **WmiDataId** (11) </span><span class="sxs-lookup"><span data-stu-id="c1990-198">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="c1990-199">次要 WINS 伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c1990-199">IP address for the secondary WINS server.</span></span> <span data-ttu-id="c1990-200">Sint32 的每個位元組都代表 IP 位址的四個部分中的其中一個)  (p1. p4。</span><span class="sxs-lookup"><span data-stu-id="c1990-200">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="c1990-201">低序位位元組包含 p1 的值，下一個位元組則包含 p2 的值，依此類推。</span><span class="sxs-lookup"><span data-stu-id="c1990-201">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="c1990-202">**大小**</span><span class="sxs-lookup"><span data-stu-id="c1990-202">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1990-203">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c1990-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1990-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c1990-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1990-205">限定詞： **WmiDataId** (5) </span><span class="sxs-lookup"><span data-stu-id="c1990-205">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="c1990-206">資料屬性的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c1990-206">Size, in bytes, of the Data property.</span></span>

</dd> <dt>

<span data-ttu-id="c1990-207">**SubnetMask**</span><span class="sxs-lookup"><span data-stu-id="c1990-207">**SubnetMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1990-208">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="c1990-208">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1990-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c1990-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1990-210">限定詞： **WmiDataId** (7) </span><span class="sxs-lookup"><span data-stu-id="c1990-210">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="c1990-211">與網路介面卡相關聯的子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="c1990-211">Subnet mask associated with the network interface card.</span></span> <span data-ttu-id="c1990-212">Sint32 的每個位元組都代表 IP 位址的四個部分中的其中一個)  (p1. p4。</span><span class="sxs-lookup"><span data-stu-id="c1990-212">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="c1990-213">低序位位元組包含 p1 的值，下一個位元組則包含 p2 的值，依此類推。</span><span class="sxs-lookup"><span data-stu-id="c1990-213">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c1990-214">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1990-214">Requirements</span></span>



| <span data-ttu-id="c1990-215">需求</span><span class="sxs-lookup"><span data-stu-id="c1990-215">Requirement</span></span> | <span data-ttu-id="c1990-216">值</span><span class="sxs-lookup"><span data-stu-id="c1990-216">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c1990-217">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c1990-217">Minimum supported client</span></span><br/> | <span data-ttu-id="c1990-218">都不支援</span><span class="sxs-lookup"><span data-stu-id="c1990-218">None supported</span></span><br/>                            |
| <span data-ttu-id="c1990-219">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c1990-219">Minimum supported server</span></span><br/> | <span data-ttu-id="c1990-220">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1990-220">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c1990-221">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1990-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1990-222">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="c1990-222">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




