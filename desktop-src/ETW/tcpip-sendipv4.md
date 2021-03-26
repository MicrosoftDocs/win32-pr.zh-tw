---
description: 此類別是 IPv4 TCP/IP 傳送事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 51a61257-fcbf-4724-80e4-12bdf45b359e
title: TcpIp_SendIPV4 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_SendIPV4
- TcpIp_SendIPV4.PID
- TcpIp_SendIPV4.size
- TcpIp_SendIPV4.daddr
- TcpIp_SendIPV4.saddr
- TcpIp_SendIPV4.dport
- TcpIp_SendIPV4.sport
- TcpIp_SendIPV4.startime
- TcpIp_SendIPV4.endtime
- TcpIp_SendIPV4.seqnum
- TcpIp_SendIPV4.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: a255c8a262c53e6dad4654946171fc19a43c6f5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943778"
---
# <a name="tcpip_sendipv4-class"></a><span data-ttu-id="92099-104">TcpIp \_ SendIPV4 類別</span><span class="sxs-lookup"><span data-stu-id="92099-104">TcpIp\_SendIPV4 class</span></span>

<span data-ttu-id="92099-105">此類別是 IPv4 TCP/IP 傳送事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="92099-105">This class is the event type class for IPv4 TCP/IP send events.</span></span>

<span data-ttu-id="92099-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="92099-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="92099-107">語法</span><span class="sxs-lookup"><span data-stu-id="92099-107">Syntax</span></span>

``` syntax
[EventType{10}, EventTypeName{"SendIPV4"}]
class TcpIp_SendIPV4 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 startime;
  uint32 endtime;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a><span data-ttu-id="92099-108">成員</span><span class="sxs-lookup"><span data-stu-id="92099-108">Members</span></span>

<span data-ttu-id="92099-109">**TcpIp \_ SendIPV4** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="92099-109">The **TcpIp\_SendIPV4** class has these types of members:</span></span>

-   [<span data-ttu-id="92099-110">屬性</span><span class="sxs-lookup"><span data-stu-id="92099-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="92099-111">屬性</span><span class="sxs-lookup"><span data-stu-id="92099-111">Properties</span></span>

<span data-ttu-id="92099-112">**TcpIp \_ SendIPV4** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="92099-112">The **TcpIp\_SendIPV4** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="92099-113">connid</span><span class="sxs-lookup"><span data-stu-id="92099-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92099-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92099-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92099-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92099-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92099-116">限定詞： WmiDataId (10) ，指標</span><span class="sxs-lookup"><span data-stu-id="92099-116">Qualifiers: WmiDataId(10), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="92099-117">唯一的連接識別碼，可讓屬於相同連接的事件相互關聯。</span><span class="sxs-lookup"><span data-stu-id="92099-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="92099-118">daddr</span><span class="sxs-lookup"><span data-stu-id="92099-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92099-119">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="92099-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="92099-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92099-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92099-121">限定詞： WmiDataId (3) ，副檔名 ( "IPAddrV4" ) </span><span class="sxs-lookup"><span data-stu-id="92099-121">Qualifiers: WmiDataId(3), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="92099-122">目的地 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="92099-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="92099-123">dport</span><span class="sxs-lookup"><span data-stu-id="92099-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92099-124">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="92099-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="92099-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92099-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92099-126">限定詞： WmiDataId (5) ，擴充 ( "Port" ) </span><span class="sxs-lookup"><span data-stu-id="92099-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="92099-127">目的地埠號碼。</span><span class="sxs-lookup"><span data-stu-id="92099-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="92099-128">**endtime**</span><span class="sxs-lookup"><span data-stu-id="92099-128">**endtime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92099-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92099-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92099-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92099-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92099-131">限定詞： WmiDataId (8) </span><span class="sxs-lookup"><span data-stu-id="92099-131">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="92099-132">結束傳送要求時間。</span><span class="sxs-lookup"><span data-stu-id="92099-132">End send request time.</span></span>

</dd> <dt>

<span data-ttu-id="92099-133">PID</span><span class="sxs-lookup"><span data-stu-id="92099-133">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92099-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92099-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92099-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92099-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92099-136">限定詞： WmiDataId (1) </span><span class="sxs-lookup"><span data-stu-id="92099-136">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="92099-137">與要求相關聯之進程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="92099-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="92099-138">saddr</span><span class="sxs-lookup"><span data-stu-id="92099-138">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92099-139">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="92099-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="92099-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92099-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92099-141">限定詞： WmiDataId (4) ，副檔名 ( "IPAddrV4" ) </span><span class="sxs-lookup"><span data-stu-id="92099-141">Qualifiers: WmiDataId(4), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="92099-142">來源 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="92099-142">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="92099-143">seqnum</span><span class="sxs-lookup"><span data-stu-id="92099-143">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92099-144">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92099-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92099-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92099-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92099-146">限定詞： WmiDataId (9) </span><span class="sxs-lookup"><span data-stu-id="92099-146">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="92099-147">序號。</span><span class="sxs-lookup"><span data-stu-id="92099-147">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="92099-148">{1}size{2}</span><span class="sxs-lookup"><span data-stu-id="92099-148">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92099-149">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92099-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92099-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92099-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92099-151">限定詞： WmiDataId (2) </span><span class="sxs-lookup"><span data-stu-id="92099-151">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="92099-152">封包的大小。</span><span class="sxs-lookup"><span data-stu-id="92099-152">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="92099-153">運動</span><span class="sxs-lookup"><span data-stu-id="92099-153">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92099-154">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="92099-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="92099-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92099-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92099-156">限定詞： WmiDataId (6) ，擴充 ( "Port" ) </span><span class="sxs-lookup"><span data-stu-id="92099-156">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="92099-157">來源埠號碼。</span><span class="sxs-lookup"><span data-stu-id="92099-157">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="92099-158">**startime**</span><span class="sxs-lookup"><span data-stu-id="92099-158">**startime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92099-159">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92099-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92099-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92099-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92099-161">限定詞： WmiDataId (7) </span><span class="sxs-lookup"><span data-stu-id="92099-161">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="92099-162">開始傳送要求時間。</span><span class="sxs-lookup"><span data-stu-id="92099-162">Start send request time.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92099-163">規格需求</span><span class="sxs-lookup"><span data-stu-id="92099-163">Requirements</span></span>



| <span data-ttu-id="92099-164">需求</span><span class="sxs-lookup"><span data-stu-id="92099-164">Requirement</span></span> | <span data-ttu-id="92099-165">值</span><span class="sxs-lookup"><span data-stu-id="92099-165">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="92099-166">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="92099-166">Minimum supported client</span></span><br/> | <span data-ttu-id="92099-167">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="92099-167">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="92099-168">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="92099-168">Minimum supported server</span></span><br/> | <span data-ttu-id="92099-169">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="92099-169">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92099-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="92099-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92099-171">**Tcpip.sys**</span><span class="sxs-lookup"><span data-stu-id="92099-171">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




