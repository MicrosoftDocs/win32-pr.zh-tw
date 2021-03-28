---
description: 此類別是 IPv6 TCP/IP 傳送事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 231ef62f-e3a5-497d-b10a-79449dc73c71
title: TcpIp_SendIPV6 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_SendIPV6
- TcpIp_SendIPV6.PID
- TcpIp_SendIPV6.size
- TcpIp_SendIPV6.daddr
- TcpIp_SendIPV6.saddr
- TcpIp_SendIPV6.dport
- TcpIp_SendIPV6.sport
- TcpIp_SendIPV6.startime
- TcpIp_SendIPV6.endtime
- TcpIp_SendIPV6.seqnum
- TcpIp_SendIPV6.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 190b7d4fc64660b1e12240b6461e73066102b6a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972501"
---
# <a name="tcpip_sendipv6-class"></a><span data-ttu-id="a5bb3-104">TcpIp \_ SendIPV6 類別</span><span class="sxs-lookup"><span data-stu-id="a5bb3-104">TcpIp\_SendIPV6 class</span></span>

<span data-ttu-id="a5bb3-105">此類別是 IPv6 TCP/IP 傳送事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="a5bb3-105">This class is the event type class for IPv6 TCP/IP send events.</span></span>

<span data-ttu-id="a5bb3-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="a5bb3-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5bb3-107">語法</span><span class="sxs-lookup"><span data-stu-id="a5bb3-107">Syntax</span></span>

``` syntax
[EventType{26}, EventTypeName{"SendIPV6"}]
class TcpIp_SendIPV6 : TcpIp
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

## <a name="members"></a><span data-ttu-id="a5bb3-108">成員</span><span class="sxs-lookup"><span data-stu-id="a5bb3-108">Members</span></span>

<span data-ttu-id="a5bb3-109">**TcpIp \_ SendIPV6** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a5bb3-109">The **TcpIp\_SendIPV6** class has these types of members:</span></span>

-   [<span data-ttu-id="a5bb3-110">屬性</span><span class="sxs-lookup"><span data-stu-id="a5bb3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a5bb3-111">屬性</span><span class="sxs-lookup"><span data-stu-id="a5bb3-111">Properties</span></span>

<span data-ttu-id="a5bb3-112">**TcpIp \_ SendIPV6** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a5bb3-112">The **TcpIp\_SendIPV6** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a5bb3-113">connid</span><span class="sxs-lookup"><span data-stu-id="a5bb3-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bb3-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a5bb3-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a5bb3-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5bb3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5bb3-116">限定詞： WmiDataId (10) ，指標</span><span class="sxs-lookup"><span data-stu-id="a5bb3-116">Qualifiers: WmiDataId(10), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="a5bb3-117">唯一的連接識別碼，可讓屬於相同連接的事件相互關聯。</span><span class="sxs-lookup"><span data-stu-id="a5bb3-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="a5bb3-118">daddr</span><span class="sxs-lookup"><span data-stu-id="a5bb3-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bb3-119">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="a5bb3-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a5bb3-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5bb3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5bb3-121">限定詞： WmiDataId (3) ，副檔名 ( "IPAddrV6" ) </span><span class="sxs-lookup"><span data-stu-id="a5bb3-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="a5bb3-122">目的地 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a5bb3-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a5bb3-123">dport</span><span class="sxs-lookup"><span data-stu-id="a5bb3-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bb3-124">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="a5bb3-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a5bb3-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5bb3-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5bb3-126">限定詞： WmiDataId (5) ，擴充 ( "Port" ) </span><span class="sxs-lookup"><span data-stu-id="a5bb3-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="a5bb3-127">目的地埠號碼。</span><span class="sxs-lookup"><span data-stu-id="a5bb3-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="a5bb3-128">**endtime**</span><span class="sxs-lookup"><span data-stu-id="a5bb3-128">**endtime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bb3-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a5bb3-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a5bb3-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5bb3-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5bb3-131">限定詞： WmiDataId (8) </span><span class="sxs-lookup"><span data-stu-id="a5bb3-131">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="a5bb3-132">結束傳送要求時間。</span><span class="sxs-lookup"><span data-stu-id="a5bb3-132">End send request time.</span></span>

</dd> <dt>

<span data-ttu-id="a5bb3-133">PID</span><span class="sxs-lookup"><span data-stu-id="a5bb3-133">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bb3-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a5bb3-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a5bb3-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5bb3-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5bb3-136">限定詞： WmiDataId (1) </span><span class="sxs-lookup"><span data-stu-id="a5bb3-136">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="a5bb3-137">與要求相關聯之進程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a5bb3-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="a5bb3-138">saddr</span><span class="sxs-lookup"><span data-stu-id="a5bb3-138">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bb3-139">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="a5bb3-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a5bb3-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5bb3-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5bb3-141">限定詞： WmiDataId (4) ，副檔名 ( "IPAddrV6" ) </span><span class="sxs-lookup"><span data-stu-id="a5bb3-141">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="a5bb3-142">來源 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a5bb3-142">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a5bb3-143">seqnum</span><span class="sxs-lookup"><span data-stu-id="a5bb3-143">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bb3-144">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a5bb3-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a5bb3-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5bb3-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5bb3-146">限定詞： WmiDataId (9) </span><span class="sxs-lookup"><span data-stu-id="a5bb3-146">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="a5bb3-147">序號。</span><span class="sxs-lookup"><span data-stu-id="a5bb3-147">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="a5bb3-148">{1}size{2}</span><span class="sxs-lookup"><span data-stu-id="a5bb3-148">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bb3-149">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a5bb3-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a5bb3-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5bb3-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5bb3-151">限定詞： WmiDataId (2) </span><span class="sxs-lookup"><span data-stu-id="a5bb3-151">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="a5bb3-152">封包的大小。</span><span class="sxs-lookup"><span data-stu-id="a5bb3-152">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="a5bb3-153">運動</span><span class="sxs-lookup"><span data-stu-id="a5bb3-153">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bb3-154">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="a5bb3-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a5bb3-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5bb3-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5bb3-156">限定詞： WmiDataId (6) ，擴充 ( "Port" ) </span><span class="sxs-lookup"><span data-stu-id="a5bb3-156">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="a5bb3-157">來源埠號碼。</span><span class="sxs-lookup"><span data-stu-id="a5bb3-157">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="a5bb3-158">**startime**</span><span class="sxs-lookup"><span data-stu-id="a5bb3-158">**startime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5bb3-159">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a5bb3-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a5bb3-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a5bb3-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5bb3-161">限定詞： WmiDataId (7) </span><span class="sxs-lookup"><span data-stu-id="a5bb3-161">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="a5bb3-162">開始傳送要求時間。</span><span class="sxs-lookup"><span data-stu-id="a5bb3-162">Start send request time.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5bb3-163">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5bb3-163">Requirements</span></span>



| <span data-ttu-id="a5bb3-164">需求</span><span class="sxs-lookup"><span data-stu-id="a5bb3-164">Requirement</span></span> | <span data-ttu-id="a5bb3-165">值</span><span class="sxs-lookup"><span data-stu-id="a5bb3-165">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a5bb3-166">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a5bb3-166">Minimum supported client</span></span><br/> | <span data-ttu-id="a5bb3-167">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5bb3-167">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a5bb3-168">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a5bb3-168">Minimum supported server</span></span><br/> | <span data-ttu-id="a5bb3-169">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5bb3-169">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a5bb3-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5bb3-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5bb3-171">**Tcpip.sys**</span><span class="sxs-lookup"><span data-stu-id="a5bb3-171">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




