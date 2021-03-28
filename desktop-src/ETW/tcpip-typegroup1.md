---
description: 此類別是 IPv4 TCP/IP 事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: ed835df8-6f53-46a3-abf2-c66a1f13f987
title: TcpIp_TypeGroup1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup1
- TcpIp_TypeGroup1.PID
- TcpIp_TypeGroup1.size
- TcpIp_TypeGroup1.daddr
- TcpIp_TypeGroup1.saddr
- TcpIp_TypeGroup1.dport
- TcpIp_TypeGroup1.sport
- TcpIp_TypeGroup1.seqnum
- TcpIp_TypeGroup1.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 70ac95d3d3de5a9bcef610607f3b5a9046b63ea3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972504"
---
# <a name="tcpip_typegroup1-class"></a><span data-ttu-id="ab37d-104">TcpIp \_ TypeGroup1 類別</span><span class="sxs-lookup"><span data-stu-id="ab37d-104">TcpIp\_TypeGroup1 class</span></span>

<span data-ttu-id="ab37d-105">此類別是 IPv4 TCP/IP 事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="ab37d-105">This class is the event type class for IPv4 TCP/IP events.</span></span>

<span data-ttu-id="ab37d-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="ab37d-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab37d-107">語法</span><span class="sxs-lookup"><span data-stu-id="ab37d-107">Syntax</span></span>

``` syntax
[EventType{11, 13, 14, 16, 18}, EventTypeName{"RecvIPV4", "DisconnectIPV4", "RetransmitIPV4", "ReconnectIPV4", "TCPCopyIPV4"}]
class TcpIp_TypeGroup1 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a><span data-ttu-id="ab37d-108">成員</span><span class="sxs-lookup"><span data-stu-id="ab37d-108">Members</span></span>

<span data-ttu-id="ab37d-109">**TcpIp \_ TypeGroup1** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ab37d-109">The **TcpIp\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="ab37d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ab37d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab37d-111">屬性</span><span class="sxs-lookup"><span data-stu-id="ab37d-111">Properties</span></span>

<span data-ttu-id="ab37d-112">**TcpIp \_ TypeGroup1** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ab37d-112">The **TcpIp\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab37d-113">connid</span><span class="sxs-lookup"><span data-stu-id="ab37d-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab37d-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ab37d-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab37d-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab37d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab37d-116">限定詞： WmiDataId (8) ，指標</span><span class="sxs-lookup"><span data-stu-id="ab37d-116">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="ab37d-117">唯一的連接識別碼，可讓屬於相同連接的事件相互關聯。</span><span class="sxs-lookup"><span data-stu-id="ab37d-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="ab37d-118">daddr</span><span class="sxs-lookup"><span data-stu-id="ab37d-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab37d-119">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="ab37d-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="ab37d-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab37d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab37d-121">限定詞： WmiDataId (3) ，副檔名 ( "IPAddrV4" ) </span><span class="sxs-lookup"><span data-stu-id="ab37d-121">Qualifiers: WmiDataId(3), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="ab37d-122">目的地 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ab37d-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ab37d-123">dport</span><span class="sxs-lookup"><span data-stu-id="ab37d-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab37d-124">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="ab37d-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="ab37d-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab37d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab37d-126">限定詞： WmiDataId (5) ，擴充 ( "Port" ) </span><span class="sxs-lookup"><span data-stu-id="ab37d-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="ab37d-127">目的地埠號碼。</span><span class="sxs-lookup"><span data-stu-id="ab37d-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="ab37d-128">PID</span><span class="sxs-lookup"><span data-stu-id="ab37d-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab37d-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ab37d-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab37d-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab37d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab37d-131">限定詞： WmiDataId (1) </span><span class="sxs-lookup"><span data-stu-id="ab37d-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="ab37d-132">與要求相關聯之進程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ab37d-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="ab37d-133">saddr</span><span class="sxs-lookup"><span data-stu-id="ab37d-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab37d-134">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="ab37d-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="ab37d-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab37d-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab37d-136">限定詞： WmiDataId (4) ，副檔名 ( "IPAddrV4" ) </span><span class="sxs-lookup"><span data-stu-id="ab37d-136">Qualifiers: WmiDataId(4), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="ab37d-137">來源 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ab37d-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ab37d-138">seqnum</span><span class="sxs-lookup"><span data-stu-id="ab37d-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab37d-139">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ab37d-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab37d-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab37d-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab37d-141">限定詞： WmiDataId (7) </span><span class="sxs-lookup"><span data-stu-id="ab37d-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="ab37d-142">序號。</span><span class="sxs-lookup"><span data-stu-id="ab37d-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="ab37d-143">{1}size{2}</span><span class="sxs-lookup"><span data-stu-id="ab37d-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab37d-144">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ab37d-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab37d-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab37d-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab37d-146">限定詞： WmiDataId (2) </span><span class="sxs-lookup"><span data-stu-id="ab37d-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="ab37d-147">封包的大小。</span><span class="sxs-lookup"><span data-stu-id="ab37d-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="ab37d-148">運動</span><span class="sxs-lookup"><span data-stu-id="ab37d-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab37d-149">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="ab37d-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="ab37d-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ab37d-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab37d-151">限定詞： WmiDataId (6) ，擴充 ( "Port" ) </span><span class="sxs-lookup"><span data-stu-id="ab37d-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="ab37d-152">來源埠號碼。</span><span class="sxs-lookup"><span data-stu-id="ab37d-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ab37d-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab37d-153">Requirements</span></span>



| <span data-ttu-id="ab37d-154">需求</span><span class="sxs-lookup"><span data-stu-id="ab37d-154">Requirement</span></span> | <span data-ttu-id="ab37d-155">值</span><span class="sxs-lookup"><span data-stu-id="ab37d-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ab37d-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab37d-156">Minimum supported client</span></span><br/> | <span data-ttu-id="ab37d-157">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab37d-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ab37d-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab37d-158">Minimum supported server</span></span><br/> | <span data-ttu-id="ab37d-159">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab37d-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ab37d-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab37d-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab37d-161">**Tcpip.sys**</span><span class="sxs-lookup"><span data-stu-id="ab37d-161">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




