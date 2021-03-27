---
description: 此類別是 IPv6 TCP/IP 連接和接受事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: c6c0463a-0058-47cf-9235-d2b621f30fb4
title: TcpIp_TypeGroup4 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup4
- TcpIp_TypeGroup4.PID
- TcpIp_TypeGroup4.size
- TcpIp_TypeGroup4.daddr
- TcpIp_TypeGroup4.saddr
- TcpIp_TypeGroup4.dport
- TcpIp_TypeGroup4.sport
- TcpIp_TypeGroup4.mss
- TcpIp_TypeGroup4.sackopt
- TcpIp_TypeGroup4.tsopt
- TcpIp_TypeGroup4.wsopt
- TcpIp_TypeGroup4.rcvwin
- TcpIp_TypeGroup4.rcvwinscale
- TcpIp_TypeGroup4.sndwinscale
- TcpIp_TypeGroup4.seqnum
- TcpIp_TypeGroup4.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 942e5897db6771c0c3a9df965e5e889eaf71c841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691803"
---
# <a name="tcpip_typegroup4-class"></a><span data-ttu-id="a5276-104">TcpIp \_ TypeGroup4 類別</span><span class="sxs-lookup"><span data-stu-id="a5276-104">TcpIp\_TypeGroup4 class</span></span>

<span data-ttu-id="a5276-105">此類別是 IPv6 TCP/IP 連接和接受事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="a5276-105">This class is the event type class for IPv6 TCP/IP connect and accept events.</span></span>

<span data-ttu-id="a5276-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="a5276-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5276-107">語法</span><span class="sxs-lookup"><span data-stu-id="a5276-107">Syntax</span></span>

``` syntax
[EventType{28, 31}, EventTypeName{"ConnectIPV6", "AcceptIPV6"}]
class TcpIp_TypeGroup4 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint16 mss;
  uint16 sackopt;
  uint16 tsopt;
  uint16 wsopt;
  uint32 rcvwin;
  sint16 rcvwinscale;
  sint16 sndwinscale;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a><span data-ttu-id="a5276-108">成員</span><span class="sxs-lookup"><span data-stu-id="a5276-108">Members</span></span>

<span data-ttu-id="a5276-109">**TcpIp \_ TypeGroup4** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a5276-109">The **TcpIp\_TypeGroup4** class has these types of members:</span></span>

-   [<span data-ttu-id="a5276-110">屬性</span><span class="sxs-lookup"><span data-stu-id="a5276-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a5276-111">屬性</span><span class="sxs-lookup"><span data-stu-id="a5276-111">Properties</span></span>

<span data-ttu-id="a5276-112">**TcpIp \_ TypeGroup4** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a5276-112">The **TcpIp\_TypeGroup4** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a5276-113">connid</span><span class="sxs-lookup"><span data-stu-id="a5276-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5276-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a5276-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a5276-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5276-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5276-116">限定詞： WmiDataId (15) ，指標</span><span class="sxs-lookup"><span data-stu-id="a5276-116">Qualifiers: WmiDataId(15), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="a5276-117">唯一的連接識別碼，可讓屬於相同連接的事件相互關聯。</span><span class="sxs-lookup"><span data-stu-id="a5276-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="a5276-118">daddr</span><span class="sxs-lookup"><span data-stu-id="a5276-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5276-119">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="a5276-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a5276-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5276-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5276-121">限定詞： WmiDataId (3) ，副檔名 ( "IPAddrV6" ) </span><span class="sxs-lookup"><span data-stu-id="a5276-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="a5276-122">目的地 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a5276-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a5276-123">dport</span><span class="sxs-lookup"><span data-stu-id="a5276-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5276-124">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="a5276-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a5276-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5276-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5276-126">限定詞： WmiDataId (5) ，擴充 ( "Port" ) </span><span class="sxs-lookup"><span data-stu-id="a5276-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="a5276-127">目的地埠號碼。</span><span class="sxs-lookup"><span data-stu-id="a5276-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="a5276-128">**Mss**</span><span class="sxs-lookup"><span data-stu-id="a5276-128">**mss**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5276-129">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a5276-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5276-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5276-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5276-131">限定詞： WmiDataId (7) </span><span class="sxs-lookup"><span data-stu-id="a5276-131">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="a5276-132">區段大小上限。</span><span class="sxs-lookup"><span data-stu-id="a5276-132">Maximum segment size.</span></span>

</dd> <dt>

<span data-ttu-id="a5276-133">PID</span><span class="sxs-lookup"><span data-stu-id="a5276-133">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5276-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a5276-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a5276-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5276-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5276-136">限定詞： WmiDataId (1) </span><span class="sxs-lookup"><span data-stu-id="a5276-136">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="a5276-137">與要求相關聯之進程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a5276-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="a5276-138">**rcvwin**</span><span class="sxs-lookup"><span data-stu-id="a5276-138">**rcvwin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5276-139">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a5276-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a5276-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5276-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5276-141">限定詞： WmiDataId (11) </span><span class="sxs-lookup"><span data-stu-id="a5276-141">Qualifiers: WmiDataId(11)</span></span>
</dt> </dl>

<span data-ttu-id="a5276-142">TCP 接收視窗大小。</span><span class="sxs-lookup"><span data-stu-id="a5276-142">TCP Receive Window size.</span></span>

</dd> <dt>

<span data-ttu-id="a5276-143">**rcvwinscale**</span><span class="sxs-lookup"><span data-stu-id="a5276-143">**rcvwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5276-144">資料類型： **sint16**</span><span class="sxs-lookup"><span data-stu-id="a5276-144">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5276-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5276-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5276-146">限定詞： WmiDataId (12) </span><span class="sxs-lookup"><span data-stu-id="a5276-146">Qualifiers: WmiDataId(12)</span></span>
</dt> </dl>

<span data-ttu-id="a5276-147">TCP 接收視窗調整係數。</span><span class="sxs-lookup"><span data-stu-id="a5276-147">TCP Receive Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="a5276-148">**sackopt**</span><span class="sxs-lookup"><span data-stu-id="a5276-148">**sackopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5276-149">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a5276-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5276-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5276-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5276-151">限定詞： **WmiDataId** (8) </span><span class="sxs-lookup"><span data-stu-id="a5276-151">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="a5276-152">TCP 標頭中的選擇性確認 (SACK) 選項。</span><span class="sxs-lookup"><span data-stu-id="a5276-152">Selective Acknowledgment (SACK) option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="a5276-153">saddr</span><span class="sxs-lookup"><span data-stu-id="a5276-153">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5276-154">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="a5276-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a5276-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5276-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5276-156">限定詞： WmiDataId (4) ，副檔名 ( "IPAddrV6" ) </span><span class="sxs-lookup"><span data-stu-id="a5276-156">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="a5276-157">來源 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a5276-157">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a5276-158">seqnum</span><span class="sxs-lookup"><span data-stu-id="a5276-158">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5276-159">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a5276-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a5276-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5276-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5276-161">限定詞： WmiDataId (14) </span><span class="sxs-lookup"><span data-stu-id="a5276-161">Qualifiers: WmiDataId(14)</span></span>
</dt> </dl>

<span data-ttu-id="a5276-162">序號。</span><span class="sxs-lookup"><span data-stu-id="a5276-162">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="a5276-163">{1}size{2}</span><span class="sxs-lookup"><span data-stu-id="a5276-163">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5276-164">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a5276-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a5276-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5276-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5276-166">限定詞： WmiDataId (2) </span><span class="sxs-lookup"><span data-stu-id="a5276-166">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="a5276-167">封包的大小。</span><span class="sxs-lookup"><span data-stu-id="a5276-167">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="a5276-168">**sndwinscale**</span><span class="sxs-lookup"><span data-stu-id="a5276-168">**sndwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5276-169">資料類型： **sint16**</span><span class="sxs-lookup"><span data-stu-id="a5276-169">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5276-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5276-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5276-171">限定詞： WmiDataId (13) </span><span class="sxs-lookup"><span data-stu-id="a5276-171">Qualifiers: WmiDataId(13)</span></span>
</dt> </dl>

<span data-ttu-id="a5276-172">TCP 傳送視窗調整係數。</span><span class="sxs-lookup"><span data-stu-id="a5276-172">TCP Send Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="a5276-173">運動</span><span class="sxs-lookup"><span data-stu-id="a5276-173">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5276-174">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="a5276-174">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a5276-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5276-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5276-176">限定詞： WmiDataId (6) ，擴充 ( "Port" ) </span><span class="sxs-lookup"><span data-stu-id="a5276-176">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="a5276-177">來源埠號碼。</span><span class="sxs-lookup"><span data-stu-id="a5276-177">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="a5276-178">**tsopt**</span><span class="sxs-lookup"><span data-stu-id="a5276-178">**tsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5276-179">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a5276-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5276-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5276-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5276-181">限定詞： WmiDataId (9) </span><span class="sxs-lookup"><span data-stu-id="a5276-181">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="a5276-182">TCP 標頭中的時間戳記選項。</span><span class="sxs-lookup"><span data-stu-id="a5276-182">Time Stamp option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="a5276-183">**wsopt**</span><span class="sxs-lookup"><span data-stu-id="a5276-183">**wsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5276-184">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a5276-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a5276-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5276-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5276-186">限定詞： WmiDataId (10) </span><span class="sxs-lookup"><span data-stu-id="a5276-186">Qualifiers: WmiDataId(10)</span></span>
</dt> </dl>

<span data-ttu-id="a5276-187">TCP 標頭中的視窗調整選項。</span><span class="sxs-lookup"><span data-stu-id="a5276-187">Window Scale option in TCP header.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5276-188">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5276-188">Requirements</span></span>



| <span data-ttu-id="a5276-189">需求</span><span class="sxs-lookup"><span data-stu-id="a5276-189">Requirement</span></span> | <span data-ttu-id="a5276-190">值</span><span class="sxs-lookup"><span data-stu-id="a5276-190">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a5276-191">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a5276-191">Minimum supported client</span></span><br/> | <span data-ttu-id="a5276-192">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5276-192">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a5276-193">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a5276-193">Minimum supported server</span></span><br/> | <span data-ttu-id="a5276-194">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5276-194">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a5276-195">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5276-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5276-196">**Tcpip.sys**</span><span class="sxs-lookup"><span data-stu-id="a5276-196">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




