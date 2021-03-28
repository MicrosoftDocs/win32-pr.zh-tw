---
description: 此類別是 IPv6 TCP/IP 事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: d24e667e-ec7f-492a-989e-a02ff4c8ac10
title: TcpIp_TypeGroup3 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup3
- TcpIp_TypeGroup3.PID
- TcpIp_TypeGroup3.size
- TcpIp_TypeGroup3.daddr
- TcpIp_TypeGroup3.saddr
- TcpIp_TypeGroup3.dport
- TcpIp_TypeGroup3.sport
- TcpIp_TypeGroup3.seqnum
- TcpIp_TypeGroup3.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 82aa119c0d770a26060b1e8d6ab74433146bb3c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972496"
---
# <a name="tcpip_typegroup3-class"></a><span data-ttu-id="b11ae-104">TcpIp \_ TypeGroup3 類別</span><span class="sxs-lookup"><span data-stu-id="b11ae-104">TcpIp\_TypeGroup3 class</span></span>

<span data-ttu-id="b11ae-105">此類別是 IPv6 TCP/IP 事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="b11ae-105">This class is the event type class for IPv6 TCP/IP events.</span></span>

<span data-ttu-id="b11ae-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="b11ae-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b11ae-107">語法</span><span class="sxs-lookup"><span data-stu-id="b11ae-107">Syntax</span></span>

``` syntax
[EventType{27, 29, 30, 32, 34}, EventTypeName{"RecvIPV6", "DisconnectIPV6", "RetransmitIPV6", "ReconnectIPV6", "TCPCopyIPV6"}]
class TcpIp_TypeGroup3 : TcpIp
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

## <a name="members"></a><span data-ttu-id="b11ae-108">成員</span><span class="sxs-lookup"><span data-stu-id="b11ae-108">Members</span></span>

<span data-ttu-id="b11ae-109">**TcpIp \_ TypeGroup3** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b11ae-109">The **TcpIp\_TypeGroup3** class has these types of members:</span></span>

-   [<span data-ttu-id="b11ae-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b11ae-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b11ae-111">屬性</span><span class="sxs-lookup"><span data-stu-id="b11ae-111">Properties</span></span>

<span data-ttu-id="b11ae-112">**TcpIp \_ TypeGroup3** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b11ae-112">The **TcpIp\_TypeGroup3** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b11ae-113">connid</span><span class="sxs-lookup"><span data-stu-id="b11ae-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b11ae-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b11ae-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b11ae-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b11ae-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b11ae-116">限定詞： WmiDataId (6) ，指標</span><span class="sxs-lookup"><span data-stu-id="b11ae-116">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b11ae-117">唯一的連接識別碼，可讓屬於相同連接的事件相互關聯。</span><span class="sxs-lookup"><span data-stu-id="b11ae-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="b11ae-118">daddr</span><span class="sxs-lookup"><span data-stu-id="b11ae-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b11ae-119">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="b11ae-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="b11ae-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b11ae-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b11ae-121">限定詞： WmiDataId (3) ，副檔名 ( "IPAddrV6" ) </span><span class="sxs-lookup"><span data-stu-id="b11ae-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="b11ae-122">目的地 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b11ae-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="b11ae-123">dport</span><span class="sxs-lookup"><span data-stu-id="b11ae-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b11ae-124">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="b11ae-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="b11ae-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b11ae-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b11ae-126">限定詞： WmiDataId (5) ，擴充 ( "Port" ) </span><span class="sxs-lookup"><span data-stu-id="b11ae-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="b11ae-127">目的地埠號碼。</span><span class="sxs-lookup"><span data-stu-id="b11ae-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="b11ae-128">PID</span><span class="sxs-lookup"><span data-stu-id="b11ae-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b11ae-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b11ae-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b11ae-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b11ae-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b11ae-131">限定詞： WmiDataId (1) </span><span class="sxs-lookup"><span data-stu-id="b11ae-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="b11ae-132">與要求相關聯之進程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b11ae-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="b11ae-133">saddr</span><span class="sxs-lookup"><span data-stu-id="b11ae-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b11ae-134">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="b11ae-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="b11ae-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b11ae-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b11ae-136">限定詞： WmiDataId (4) ，副檔名 ( "IPAddrV6" ) </span><span class="sxs-lookup"><span data-stu-id="b11ae-136">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="b11ae-137">來源 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b11ae-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="b11ae-138">seqnum</span><span class="sxs-lookup"><span data-stu-id="b11ae-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b11ae-139">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b11ae-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b11ae-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b11ae-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b11ae-141">限定詞： WmiDataId (7) </span><span class="sxs-lookup"><span data-stu-id="b11ae-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="b11ae-142">序號。</span><span class="sxs-lookup"><span data-stu-id="b11ae-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="b11ae-143">{1}size{2}</span><span class="sxs-lookup"><span data-stu-id="b11ae-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b11ae-144">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b11ae-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b11ae-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b11ae-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b11ae-146">限定詞： WmiDataId (2) </span><span class="sxs-lookup"><span data-stu-id="b11ae-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="b11ae-147">封包的大小。</span><span class="sxs-lookup"><span data-stu-id="b11ae-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="b11ae-148">運動</span><span class="sxs-lookup"><span data-stu-id="b11ae-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b11ae-149">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="b11ae-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="b11ae-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b11ae-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b11ae-151">限定詞： WmiDataId (6) ，擴充 ( "Port" ) </span><span class="sxs-lookup"><span data-stu-id="b11ae-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="b11ae-152">來源埠號碼。</span><span class="sxs-lookup"><span data-stu-id="b11ae-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b11ae-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="b11ae-153">Requirements</span></span>



| <span data-ttu-id="b11ae-154">需求</span><span class="sxs-lookup"><span data-stu-id="b11ae-154">Requirement</span></span> | <span data-ttu-id="b11ae-155">值</span><span class="sxs-lookup"><span data-stu-id="b11ae-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b11ae-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b11ae-156">Minimum supported client</span></span><br/> | <span data-ttu-id="b11ae-157">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b11ae-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b11ae-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b11ae-158">Minimum supported server</span></span><br/> | <span data-ttu-id="b11ae-159">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b11ae-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b11ae-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b11ae-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b11ae-161">**Tcpip.sys**</span><span class="sxs-lookup"><span data-stu-id="b11ae-161">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




