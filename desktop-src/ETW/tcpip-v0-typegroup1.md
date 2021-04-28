---
description: TcpIp_V0_TypeGroup1 類別-這個類別是 TCP/IP 事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 007f0744-8b74-4c57-85bc-f6bdb20bffa7
title: TcpIp_V0_TypeGroup1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_V0_TypeGroup1
- TcpIp_V0_TypeGroup1.daddr
- TcpIp_V0_TypeGroup1.saddr
- TcpIp_V0_TypeGroup1.dport
- TcpIp_V0_TypeGroup1.sport
- TcpIp_V0_TypeGroup1.size
- TcpIp_V0_TypeGroup1.PID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 96df2214aff9b5be6f10a1f08f6e6ea2e015c6b5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105786"
---
# <a name="tcpip_v0_typegroup1-class"></a><span data-ttu-id="97723-104">TcpIp \_ V0 \_ TypeGroup1 類別</span><span class="sxs-lookup"><span data-stu-id="97723-104">TcpIp\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="97723-105">這個類別是 TCP/IP 事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="97723-105">This class is the event type class for TCP/IP events.</span></span>

<span data-ttu-id="97723-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="97723-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="97723-107">語法</span><span class="sxs-lookup"><span data-stu-id="97723-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15}, EventTypeName{"Send", "Recv", "Connect", "Disconnect", "Retransmit", "Accept"}]
class TcpIp_V0_TypeGroup1 : TcpIp_V0
{
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 size;
  uint32 PID;
};
```

## <a name="members"></a><span data-ttu-id="97723-108">成員</span><span class="sxs-lookup"><span data-stu-id="97723-108">Members</span></span>

<span data-ttu-id="97723-109">**TcpIp \_ V0 \_ TypeGroup1** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="97723-109">The **TcpIp\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="97723-110">屬性</span><span class="sxs-lookup"><span data-stu-id="97723-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="97723-111">屬性</span><span class="sxs-lookup"><span data-stu-id="97723-111">Properties</span></span>

<span data-ttu-id="97723-112">**TcpIp \_ V0 \_ TypeGroup1** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="97723-112">The **TcpIp\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="97723-113">daddr</span><span class="sxs-lookup"><span data-stu-id="97723-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97723-114">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="97723-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="97723-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="97723-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97723-116">限定詞： WmiDataId (1) ，副檔名 ( "IPAddr" ) </span><span class="sxs-lookup"><span data-stu-id="97723-116">Qualifiers: WmiDataId(1), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="97723-117">目的地 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="97723-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="97723-118">dport</span><span class="sxs-lookup"><span data-stu-id="97723-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97723-119">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="97723-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="97723-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="97723-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97723-121">限定詞： WmiDataId (3) ，擴充 ( "Port" ) </span><span class="sxs-lookup"><span data-stu-id="97723-121">Qualifiers: WmiDataId(3), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="97723-122">目的地埠號碼。</span><span class="sxs-lookup"><span data-stu-id="97723-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="97723-123">PID</span><span class="sxs-lookup"><span data-stu-id="97723-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97723-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="97723-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="97723-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="97723-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97723-126">限定詞： WmiDataId (6) </span><span class="sxs-lookup"><span data-stu-id="97723-126">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="97723-127">與要求相關聯之進程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="97723-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="97723-128">saddr</span><span class="sxs-lookup"><span data-stu-id="97723-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97723-129">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="97723-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="97723-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="97723-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97723-131">限定詞： WmiDataId (2) ，副檔名 ( "IPAddr" ) </span><span class="sxs-lookup"><span data-stu-id="97723-131">Qualifiers: WmiDataId(2), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="97723-132">來源 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="97723-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="97723-133">{1}size{2}</span><span class="sxs-lookup"><span data-stu-id="97723-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97723-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="97723-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="97723-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="97723-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97723-136">限定詞： WmiDataId (5) </span><span class="sxs-lookup"><span data-stu-id="97723-136">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="97723-137">封包的大小。</span><span class="sxs-lookup"><span data-stu-id="97723-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="97723-138">運動</span><span class="sxs-lookup"><span data-stu-id="97723-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97723-139">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="97723-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="97723-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="97723-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97723-141">限定詞： WmiDataId (4) ，擴充 ( "Port" ) </span><span class="sxs-lookup"><span data-stu-id="97723-141">Qualifiers: WmiDataId(4), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="97723-142">來源埠號碼。</span><span class="sxs-lookup"><span data-stu-id="97723-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="97723-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="97723-143">Requirements</span></span>



| <span data-ttu-id="97723-144">需求</span><span class="sxs-lookup"><span data-stu-id="97723-144">Requirement</span></span> | <span data-ttu-id="97723-145">值</span><span class="sxs-lookup"><span data-stu-id="97723-145">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="97723-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="97723-146">Minimum supported client</span></span><br/> | <span data-ttu-id="97723-147">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97723-147">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="97723-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="97723-148">Minimum supported server</span></span><br/> | <span data-ttu-id="97723-149">都不支援</span><span class="sxs-lookup"><span data-stu-id="97723-149">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="97723-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97723-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97723-151">**TcpIp \_ V0**</span><span class="sxs-lookup"><span data-stu-id="97723-151">**TcpIp\_V0**</span></span>](tcpip-v0.md)
</dt> </dl>

 

 




