---
description: 此類別是 IPv4 TCP/IP 連接和接受事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: a9b33ceb-7d50-4cd7-8224-0b2cf895b3b4
title: TcpIp_TypeGroup2 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup2
- TcpIp_TypeGroup2.PID
- TcpIp_TypeGroup2.size
- TcpIp_TypeGroup2.daddr
- TcpIp_TypeGroup2.saddr
- TcpIp_TypeGroup2.dport
- TcpIp_TypeGroup2.sport
- TcpIp_TypeGroup2.mss
- TcpIp_TypeGroup2.sackopt
- TcpIp_TypeGroup2.tsopt
- TcpIp_TypeGroup2.wsopt
- TcpIp_TypeGroup2.rcvwin
- TcpIp_TypeGroup2.rcvwinscale
- TcpIp_TypeGroup2.sndwinscale
- TcpIp_TypeGroup2.seqnum
- TcpIp_TypeGroup2.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 398b6b0e2b7e4684481f13f73bdd94ef4cd76829
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512808"
---
# <a name="tcpip_typegroup2-class"></a><span data-ttu-id="41fdb-104">TcpIp \_ TypeGroup2 類別</span><span class="sxs-lookup"><span data-stu-id="41fdb-104">TcpIp\_TypeGroup2 class</span></span>

<span data-ttu-id="41fdb-105">此類別是 IPv4 TCP/IP 連接和接受事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="41fdb-105">This class is the event type class for IPv4 TCP/IP connect and accept events.</span></span>

<span data-ttu-id="41fdb-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="41fdb-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="41fdb-107">語法</span><span class="sxs-lookup"><span data-stu-id="41fdb-107">Syntax</span></span>

``` syntax
[EventType{12, 15}, EventTypeName{"ConnectIPV4", "AcceptIPV4"}]
class TcpIp_TypeGroup2 : TcpIp
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

## <a name="members"></a><span data-ttu-id="41fdb-108">成員</span><span class="sxs-lookup"><span data-stu-id="41fdb-108">Members</span></span>

<span data-ttu-id="41fdb-109">**TcpIp \_ TypeGroup2** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="41fdb-109">The **TcpIp\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="41fdb-110">屬性</span><span class="sxs-lookup"><span data-stu-id="41fdb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="41fdb-111">屬性</span><span class="sxs-lookup"><span data-stu-id="41fdb-111">Properties</span></span>

<span data-ttu-id="41fdb-112">**TcpIp \_ TypeGroup2** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="41fdb-112">The **TcpIp\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="41fdb-113">**connid**</span><span class="sxs-lookup"><span data-stu-id="41fdb-113">**connid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41fdb-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41fdb-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41fdb-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-116">限定詞： **WmiDataId (15)**， **指標**</span><span class="sxs-lookup"><span data-stu-id="41fdb-116">Qualifiers: **WmiDataId(15)**, **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="41fdb-117">唯一的連接識別碼，可讓屬於相同連接的事件相互關聯。</span><span class="sxs-lookup"><span data-stu-id="41fdb-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="41fdb-118">**daddr**</span><span class="sxs-lookup"><span data-stu-id="41fdb-118">**daddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41fdb-119">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="41fdb-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41fdb-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-121">限定詞： **WmiDataId (3)**， **副檔名 ( "IPAddrV4" )**</span><span class="sxs-lookup"><span data-stu-id="41fdb-121">Qualifiers: **WmiDataId(3)**, **Extension("IPAddrV4")**</span></span>
</dt> </dl>

<span data-ttu-id="41fdb-122">目的地 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="41fdb-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="41fdb-123">**dport**</span><span class="sxs-lookup"><span data-stu-id="41fdb-123">**dport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41fdb-124">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="41fdb-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41fdb-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-126">限定詞： **WmiDataId (5)**， **擴充 ( "Port" )**</span><span class="sxs-lookup"><span data-stu-id="41fdb-126">Qualifiers: **WmiDataId(5)**, **Extension("Port")**</span></span>
</dt> </dl>

<span data-ttu-id="41fdb-127">目的地埠號碼。</span><span class="sxs-lookup"><span data-stu-id="41fdb-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="41fdb-128">**Mss**</span><span class="sxs-lookup"><span data-stu-id="41fdb-128">**mss**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41fdb-129">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="41fdb-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41fdb-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-131">限定詞： **WmiDataId (7)**</span><span class="sxs-lookup"><span data-stu-id="41fdb-131">Qualifiers: **WmiDataId(7)**</span></span>
</dt> </dl>

<span data-ttu-id="41fdb-132">區段大小上限。</span><span class="sxs-lookup"><span data-stu-id="41fdb-132">Maximum segment size.</span></span>

</dd> <dt>

<span data-ttu-id="41fdb-133">**Pid**</span><span class="sxs-lookup"><span data-stu-id="41fdb-133">**PID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41fdb-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41fdb-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41fdb-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-136">限定詞： **WmiDataId (1)**</span><span class="sxs-lookup"><span data-stu-id="41fdb-136">Qualifiers: **WmiDataId(1)**</span></span>
</dt> </dl>

<span data-ttu-id="41fdb-137">與要求相關聯之進程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="41fdb-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="41fdb-138">**rcvwin**</span><span class="sxs-lookup"><span data-stu-id="41fdb-138">**rcvwin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41fdb-139">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41fdb-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41fdb-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-141">限定詞： **WmiDataId (11)**</span><span class="sxs-lookup"><span data-stu-id="41fdb-141">Qualifiers: **WmiDataId(11)**</span></span>
</dt> </dl>

<span data-ttu-id="41fdb-142">TCP 接收視窗大小。</span><span class="sxs-lookup"><span data-stu-id="41fdb-142">TCP Receive Window size.</span></span>

</dd> <dt>

<span data-ttu-id="41fdb-143">**rcvwinscale**</span><span class="sxs-lookup"><span data-stu-id="41fdb-143">**rcvwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41fdb-144">資料類型： **sint16**</span><span class="sxs-lookup"><span data-stu-id="41fdb-144">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41fdb-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-146">限定詞： **WmiDataId (12)**</span><span class="sxs-lookup"><span data-stu-id="41fdb-146">Qualifiers: **WmiDataId(12)**</span></span>
</dt> </dl>

<span data-ttu-id="41fdb-147">TCP 接收視窗調整係數。</span><span class="sxs-lookup"><span data-stu-id="41fdb-147">TCP Receive Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="41fdb-148">**sackopt**</span><span class="sxs-lookup"><span data-stu-id="41fdb-148">**sackopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41fdb-149">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="41fdb-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41fdb-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-151">限定詞： **WmiDataId (8)**</span><span class="sxs-lookup"><span data-stu-id="41fdb-151">Qualifiers: **WmiDataId(8)**</span></span>
</dt> </dl>

<span data-ttu-id="41fdb-152">TCP 標頭中的選擇性確認 (SACK) 選項。</span><span class="sxs-lookup"><span data-stu-id="41fdb-152">Selective Acknowledgment (SACK) option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="41fdb-153">**saddr**</span><span class="sxs-lookup"><span data-stu-id="41fdb-153">**saddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41fdb-154">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="41fdb-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41fdb-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-156">限定詞： **WmiDataId (4)**， **副檔名 ( "IPAddrV4" )**</span><span class="sxs-lookup"><span data-stu-id="41fdb-156">Qualifiers: **WmiDataId(4)**, **Extension("IPAddrV4")**</span></span>
</dt> </dl>

<span data-ttu-id="41fdb-157">來源 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="41fdb-157">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="41fdb-158">**seqnum**</span><span class="sxs-lookup"><span data-stu-id="41fdb-158">**seqnum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41fdb-159">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41fdb-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41fdb-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-161">限定詞： **WmiDataId (14)**</span><span class="sxs-lookup"><span data-stu-id="41fdb-161">Qualifiers: **WmiDataId(14)**</span></span>
</dt> </dl>

<span data-ttu-id="41fdb-162">序號。</span><span class="sxs-lookup"><span data-stu-id="41fdb-162">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="41fdb-163">**size**</span><span class="sxs-lookup"><span data-stu-id="41fdb-163">**size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41fdb-164">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="41fdb-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41fdb-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-166">限定詞： **WmiDataId (2)**</span><span class="sxs-lookup"><span data-stu-id="41fdb-166">Qualifiers: **WmiDataId(2)**</span></span>
</dt> </dl>

<span data-ttu-id="41fdb-167">封包的大小。</span><span class="sxs-lookup"><span data-stu-id="41fdb-167">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="41fdb-168">**sndwinscale**</span><span class="sxs-lookup"><span data-stu-id="41fdb-168">**sndwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41fdb-169">資料類型： **sint16**</span><span class="sxs-lookup"><span data-stu-id="41fdb-169">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41fdb-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-171">限定詞： **WmiDataId (13)**</span><span class="sxs-lookup"><span data-stu-id="41fdb-171">Qualifiers: **WmiDataId(13)**</span></span>
</dt> </dl>

<span data-ttu-id="41fdb-172">TCP 傳送視窗調整係數。</span><span class="sxs-lookup"><span data-stu-id="41fdb-172">TCP Send Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="41fdb-173">**運動**</span><span class="sxs-lookup"><span data-stu-id="41fdb-173">**sport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41fdb-174">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="41fdb-174">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41fdb-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-176">限定詞： **WmiDataId (6)**， **擴充 ( "Port" )**</span><span class="sxs-lookup"><span data-stu-id="41fdb-176">Qualifiers: **WmiDataId(6)**, **Extension("Port")**</span></span>
</dt> </dl>

<span data-ttu-id="41fdb-177">來源埠號碼。</span><span class="sxs-lookup"><span data-stu-id="41fdb-177">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="41fdb-178">**tsopt**</span><span class="sxs-lookup"><span data-stu-id="41fdb-178">**tsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41fdb-179">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="41fdb-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41fdb-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-181">限定詞： **WmiDataId (9)**</span><span class="sxs-lookup"><span data-stu-id="41fdb-181">Qualifiers: **WmiDataId(9)**</span></span>
</dt> </dl>

<span data-ttu-id="41fdb-182">TCP 標頭中的時間戳記選項。</span><span class="sxs-lookup"><span data-stu-id="41fdb-182">Time Stamp option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="41fdb-183">**wsopt**</span><span class="sxs-lookup"><span data-stu-id="41fdb-183">**wsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41fdb-184">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="41fdb-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="41fdb-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41fdb-186">限定詞： **WmiDataId (10)**</span><span class="sxs-lookup"><span data-stu-id="41fdb-186">Qualifiers: **WmiDataId(10)**</span></span>
</dt> </dl>

<span data-ttu-id="41fdb-187">TCP 標頭中的視窗調整選項。</span><span class="sxs-lookup"><span data-stu-id="41fdb-187">Window Scale option in TCP header.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41fdb-188">規格需求</span><span class="sxs-lookup"><span data-stu-id="41fdb-188">Requirements</span></span>



| <span data-ttu-id="41fdb-189">需求</span><span class="sxs-lookup"><span data-stu-id="41fdb-189">Requirement</span></span> | <span data-ttu-id="41fdb-190">值</span><span class="sxs-lookup"><span data-stu-id="41fdb-190">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="41fdb-191">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41fdb-191">Minimum supported client</span></span><br/> | <span data-ttu-id="41fdb-192">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41fdb-192">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="41fdb-193">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41fdb-193">Minimum supported server</span></span><br/> | <span data-ttu-id="41fdb-194">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41fdb-194">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="41fdb-195">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41fdb-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41fdb-196">**Tcpip.sys**</span><span class="sxs-lookup"><span data-stu-id="41fdb-196">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




