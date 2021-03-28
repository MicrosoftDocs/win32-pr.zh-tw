---
description: 此類別是網路介面卡設定事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 66b2c116-810e-489d-ad5e-f9c09902005b
title: SystemConfig_NIC 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_NIC
- SystemConfig_NIC.PhysicalAddr
- SystemConfig_NIC.PhysicalAddrLen
- SystemConfig_NIC.Ipv4Index
- SystemConfig_NIC.Ipv6Index
- SystemConfig_NIC.NICDescription
- SystemConfig_NIC.IpAddresses
- SystemConfig_NIC.DnsServerAddresses
api_type:
- NA
api_location: ''
ms.openlocfilehash: 63d522eee993f0766554eb9bc4fb09d842e9cd8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943457"
---
# <a name="systemconfig_nic-class"></a><span data-ttu-id="e8ebb-104">SystemConfig \_ NIC 類別</span><span class="sxs-lookup"><span data-stu-id="e8ebb-104">SystemConfig\_NIC class</span></span>

<span data-ttu-id="e8ebb-105">此類別是網路介面卡設定事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="e8ebb-105">This class is the event type class for network interface card configuration events.</span></span>

<span data-ttu-id="e8ebb-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="e8ebb-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8ebb-107">語法</span><span class="sxs-lookup"><span data-stu-id="e8ebb-107">Syntax</span></span>

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_NIC : SystemConfig
{
  uint64 PhysicalAddr;
  uint32 PhysicalAddrLen;
  uint32 Ipv4Index;
  uint32 Ipv6Index;
  string NICDescription;
  string IpAddresses;
  string DnsServerAddresses;
};
```

## <a name="members"></a><span data-ttu-id="e8ebb-108">成員</span><span class="sxs-lookup"><span data-stu-id="e8ebb-108">Members</span></span>

<span data-ttu-id="e8ebb-109">**SystemConfig \_ NIC** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e8ebb-109">The **SystemConfig\_NIC** class has these types of members:</span></span>

-   [<span data-ttu-id="e8ebb-110">屬性</span><span class="sxs-lookup"><span data-stu-id="e8ebb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e8ebb-111">屬性</span><span class="sxs-lookup"><span data-stu-id="e8ebb-111">Properties</span></span>

<span data-ttu-id="e8ebb-112">**SystemConfig \_ NIC** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e8ebb-112">The **SystemConfig\_NIC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e8ebb-113">DnsServerAddresses</span><span class="sxs-lookup"><span data-stu-id="e8ebb-113">DnsServerAddresses</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8ebb-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e8ebb-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8ebb-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e8ebb-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8ebb-116">限定詞： WmiDataId (7) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) </span><span class="sxs-lookup"><span data-stu-id="e8ebb-116">Qualifiers: WmiDataId(7), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="e8ebb-117">用來查詢 DNS 伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e8ebb-117">IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="e8ebb-118">地址清單會以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="e8ebb-118">The list of addresses is comma-delimited.</span></span>

</dd> <dt>

<span data-ttu-id="e8ebb-119">IpAddresses</span><span class="sxs-lookup"><span data-stu-id="e8ebb-119">IpAddresses</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8ebb-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e8ebb-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8ebb-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e8ebb-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8ebb-122">限定詞： WmiDataId (6) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) </span><span class="sxs-lookup"><span data-stu-id="e8ebb-122">Qualifiers: WmiDataId(6), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="e8ebb-123">與網路介面卡相關聯的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e8ebb-123">IP addresses associated with the network interface card.</span></span> <span data-ttu-id="e8ebb-124">地址清單會以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="e8ebb-124">The list of addresses is comma-delimited.</span></span>

</dd> <dt>

<span data-ttu-id="e8ebb-125">Ipv4Index</span><span class="sxs-lookup"><span data-stu-id="e8ebb-125">Ipv4Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8ebb-126">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e8ebb-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8ebb-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e8ebb-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8ebb-128">限定詞： WmiDataId (3) </span><span class="sxs-lookup"><span data-stu-id="e8ebb-128">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="e8ebb-129">IPv4 NIC 的介面卡索引。</span><span class="sxs-lookup"><span data-stu-id="e8ebb-129">Adapter index for IPv4 NIC.</span></span> <span data-ttu-id="e8ebb-130">介面卡已停用並啟用，或在其他情況下，介面卡索引可能會變更，而且不應該被視為持續性。</span><span class="sxs-lookup"><span data-stu-id="e8ebb-130">The adapter index may change when an adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.</span></span>

</dd> <dt>

<span data-ttu-id="e8ebb-131">Ipv6Index</span><span class="sxs-lookup"><span data-stu-id="e8ebb-131">Ipv6Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8ebb-132">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e8ebb-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8ebb-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e8ebb-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8ebb-134">限定詞： WmiDataId (4) </span><span class="sxs-lookup"><span data-stu-id="e8ebb-134">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="e8ebb-135">IPv6 NIC 的介面卡索引。</span><span class="sxs-lookup"><span data-stu-id="e8ebb-135">Adapter index for IPv6 NIC.</span></span> <span data-ttu-id="e8ebb-136">介面卡已停用並啟用，或在其他情況下，介面卡索引可能會變更，而且不應該被視為持續性。</span><span class="sxs-lookup"><span data-stu-id="e8ebb-136">The adapter index may change when an adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.</span></span>

</dd> <dt>

<span data-ttu-id="e8ebb-137">NICDescription</span><span class="sxs-lookup"><span data-stu-id="e8ebb-137">NICDescription</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8ebb-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e8ebb-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8ebb-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e8ebb-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8ebb-140">限定詞： WmiDataId (5) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) </span><span class="sxs-lookup"><span data-stu-id="e8ebb-140">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="e8ebb-141">介面卡的描述。</span><span class="sxs-lookup"><span data-stu-id="e8ebb-141">Description of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="e8ebb-142">PhysicalAddr</span><span class="sxs-lookup"><span data-stu-id="e8ebb-142">PhysicalAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8ebb-143">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e8ebb-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e8ebb-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e8ebb-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8ebb-145">限定詞： WmiDataId (1) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="e8ebb-145">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="e8ebb-146">介面卡的硬體位址。</span><span class="sxs-lookup"><span data-stu-id="e8ebb-146">Hardware address for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="e8ebb-147">PhysicalAddrLen</span><span class="sxs-lookup"><span data-stu-id="e8ebb-147">PhysicalAddrLen</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8ebb-148">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e8ebb-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8ebb-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e8ebb-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8ebb-150">限定詞： WmiDataId (2) </span><span class="sxs-lookup"><span data-stu-id="e8ebb-150">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="e8ebb-151">介面卡的硬體位址長度。</span><span class="sxs-lookup"><span data-stu-id="e8ebb-151">Length of the hardware address for the adapter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8ebb-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8ebb-152">Requirements</span></span>



| <span data-ttu-id="e8ebb-153">需求</span><span class="sxs-lookup"><span data-stu-id="e8ebb-153">Requirement</span></span> | <span data-ttu-id="e8ebb-154">值</span><span class="sxs-lookup"><span data-stu-id="e8ebb-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e8ebb-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e8ebb-155">Minimum supported client</span></span><br/> | <span data-ttu-id="e8ebb-156">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8ebb-156">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e8ebb-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e8ebb-157">Minimum supported server</span></span><br/> | <span data-ttu-id="e8ebb-158">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8ebb-158">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e8ebb-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8ebb-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8ebb-160">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="e8ebb-160">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




