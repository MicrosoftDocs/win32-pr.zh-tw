---
description: 此類別是 UDP/IP IPv6 傳送和接收事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 059041f6-bf34-4bf8-8e1a-2dfbc6c30edc
title: UdpIp_TypeGroup2 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_TypeGroup2
- UdpIp_TypeGroup2.PID
- UdpIp_TypeGroup2.size
- UdpIp_TypeGroup2.daddr
- UdpIp_TypeGroup2.saddr
- UdpIp_TypeGroup2.dport
- UdpIp_TypeGroup2.sport
- UdpIp_TypeGroup2.seqnum
- UdpIp_TypeGroup2.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 88d9cb4935d005f3c25f1fb6c3c421328fb285bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972805"
---
# <a name="udpip_typegroup2-class"></a><span data-ttu-id="96279-104">UdpIp \_ TypeGroup2 類別</span><span class="sxs-lookup"><span data-stu-id="96279-104">UdpIp\_TypeGroup2 class</span></span>

<span data-ttu-id="96279-105">此類別是 UDP/IP IPv6 傳送和接收事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="96279-105">This class is the event type class for UDP/IP IPv6 send and receive events.</span></span>

<span data-ttu-id="96279-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="96279-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="96279-107">語法</span><span class="sxs-lookup"><span data-stu-id="96279-107">Syntax</span></span>

``` syntax
[EventType{26, 27}, EventTypeName{"SendIPV6", "RecvIPV6"}]
class UdpIp_TypeGroup2 : UdpIp
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

## <a name="members"></a><span data-ttu-id="96279-108">成員</span><span class="sxs-lookup"><span data-stu-id="96279-108">Members</span></span>

<span data-ttu-id="96279-109">**UdpIp \_ TypeGroup2** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="96279-109">The **UdpIp\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="96279-110">屬性</span><span class="sxs-lookup"><span data-stu-id="96279-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="96279-111">屬性</span><span class="sxs-lookup"><span data-stu-id="96279-111">Properties</span></span>

<span data-ttu-id="96279-112">**UdpIp \_ TypeGroup2** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="96279-112">The **UdpIp\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="96279-113">connid</span><span class="sxs-lookup"><span data-stu-id="96279-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96279-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="96279-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96279-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="96279-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96279-116">限定詞： WmiDataId (8) ，指標</span><span class="sxs-lookup"><span data-stu-id="96279-116">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="96279-117">唯一的連接識別碼，可讓屬於相同連接的事件相互關聯。</span><span class="sxs-lookup"><span data-stu-id="96279-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="96279-118">daddr</span><span class="sxs-lookup"><span data-stu-id="96279-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96279-119">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="96279-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="96279-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="96279-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96279-121">限定詞： WmiDataId (3) ，副檔名 ( "IPAddrV6" ) </span><span class="sxs-lookup"><span data-stu-id="96279-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="96279-122">目的地 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="96279-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="96279-123">dport</span><span class="sxs-lookup"><span data-stu-id="96279-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96279-124">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="96279-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="96279-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="96279-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96279-126">限定詞： WmiDataId (5) ，擴充 ( "Port" ) </span><span class="sxs-lookup"><span data-stu-id="96279-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="96279-127">目的地埠號碼。</span><span class="sxs-lookup"><span data-stu-id="96279-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="96279-128">PID</span><span class="sxs-lookup"><span data-stu-id="96279-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96279-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="96279-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96279-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="96279-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96279-131">限定詞： WmiDataId (1) </span><span class="sxs-lookup"><span data-stu-id="96279-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="96279-132">與要求相關聯之進程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="96279-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="96279-133">saddr</span><span class="sxs-lookup"><span data-stu-id="96279-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96279-134">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="96279-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="96279-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="96279-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96279-136">限定詞： WmiDataId (4) ，副檔名 ( "IPAddrV6" ) </span><span class="sxs-lookup"><span data-stu-id="96279-136">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="96279-137">來源 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="96279-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="96279-138">seqnum</span><span class="sxs-lookup"><span data-stu-id="96279-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96279-139">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="96279-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96279-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="96279-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96279-141">限定詞： WmiDataId (7) </span><span class="sxs-lookup"><span data-stu-id="96279-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="96279-142">序號。</span><span class="sxs-lookup"><span data-stu-id="96279-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="96279-143">{1}size{2}</span><span class="sxs-lookup"><span data-stu-id="96279-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96279-144">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="96279-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96279-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="96279-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96279-146">限定詞： WmiDataId (2) </span><span class="sxs-lookup"><span data-stu-id="96279-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="96279-147">封包的大小。</span><span class="sxs-lookup"><span data-stu-id="96279-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="96279-148">運動</span><span class="sxs-lookup"><span data-stu-id="96279-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96279-149">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="96279-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="96279-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="96279-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96279-151">限定詞： WmiDataId (6) ，擴充 ( "Port" ) </span><span class="sxs-lookup"><span data-stu-id="96279-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="96279-152">來源埠號碼。</span><span class="sxs-lookup"><span data-stu-id="96279-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96279-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="96279-153">Requirements</span></span>



| <span data-ttu-id="96279-154">需求</span><span class="sxs-lookup"><span data-stu-id="96279-154">Requirement</span></span> | <span data-ttu-id="96279-155">值</span><span class="sxs-lookup"><span data-stu-id="96279-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="96279-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="96279-156">Minimum supported client</span></span><br/> | <span data-ttu-id="96279-157">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96279-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="96279-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="96279-158">Minimum supported server</span></span><br/> | <span data-ttu-id="96279-159">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96279-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="96279-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96279-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96279-161">**UdpIp**</span><span class="sxs-lookup"><span data-stu-id="96279-161">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




