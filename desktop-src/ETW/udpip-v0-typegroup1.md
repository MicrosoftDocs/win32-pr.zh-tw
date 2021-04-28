---
description: UdpIp_V0_TypeGroup1 類別-這個類別是 UDP/IP 事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 834a761a-089b-4b93-9a6a-a1edf752b582
title: UdpIp_V0_TypeGroup1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_V0_TypeGroup1
- UdpIp_V0_TypeGroup1.context
- UdpIp_V0_TypeGroup1.saddr
- UdpIp_V0_TypeGroup1.sport
- UdpIp_V0_TypeGroup1.size
- UdpIp_V0_TypeGroup1.daddr
- UdpIp_V0_TypeGroup1.dport
- UdpIp_V0_TypeGroup1.dsize
api_type:
- NA
api_location: ''
ms.openlocfilehash: 78243a49e4504fd9e132407feebe98d9b48f7bdd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105496"
---
# <a name="udpip_v0_typegroup1-class"></a><span data-ttu-id="437ba-104">UdpIp \_ V0 \_ TypeGroup1 類別</span><span class="sxs-lookup"><span data-stu-id="437ba-104">UdpIp\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="437ba-105">此類別是 UDP/IP 事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="437ba-105">This class is the event type class for UDP/IP events.</span></span>

<span data-ttu-id="437ba-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="437ba-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="437ba-107">語法</span><span class="sxs-lookup"><span data-stu-id="437ba-107">Syntax</span></span>

``` syntax
[EventType{10, 11}, EventTypeName{"Send", "Recv"}]
class UdpIp_V0_TypeGroup1 : UdpIp_V0
{
  uint32 context;
  object saddr;
  object sport;
  uint16 size;
  object daddr;
  object dport;
  uint16 dsize;
};
```

## <a name="members"></a><span data-ttu-id="437ba-108">成員</span><span class="sxs-lookup"><span data-stu-id="437ba-108">Members</span></span>

<span data-ttu-id="437ba-109">**UdpIp \_ V0 \_ TypeGroup1** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="437ba-109">The **UdpIp\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="437ba-110">屬性</span><span class="sxs-lookup"><span data-stu-id="437ba-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="437ba-111">屬性</span><span class="sxs-lookup"><span data-stu-id="437ba-111">Properties</span></span>

<span data-ttu-id="437ba-112">**UdpIp \_ V0 \_ TypeGroup1** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="437ba-112">The **UdpIp\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="437ba-113">內容</span><span class="sxs-lookup"><span data-stu-id="437ba-113">context</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="437ba-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="437ba-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="437ba-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="437ba-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="437ba-116">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="437ba-116">Qualifiers: WmiDataId(1), pointer</span></span>
</dt> </dl>

<span data-ttu-id="437ba-117">發出或接收要求之位址物件的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="437ba-117">Process identifier for the Address Object that made or received the request.</span></span>

</dd> <dt>

<span data-ttu-id="437ba-118">daddr</span><span class="sxs-lookup"><span data-stu-id="437ba-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="437ba-119">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="437ba-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="437ba-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="437ba-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="437ba-121">限定詞： WmiDataId (5) ，副檔名 ( "IPAddr" ) </span><span class="sxs-lookup"><span data-stu-id="437ba-121">Qualifiers: WmiDataId(5), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="437ba-122">目的地 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="437ba-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="437ba-123">dport</span><span class="sxs-lookup"><span data-stu-id="437ba-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="437ba-124">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="437ba-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="437ba-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="437ba-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="437ba-126">限定詞： WmiDataId (6) ，擴充 ( "Port" ) </span><span class="sxs-lookup"><span data-stu-id="437ba-126">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="437ba-127">目的地埠號碼。</span><span class="sxs-lookup"><span data-stu-id="437ba-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="437ba-128">dsize</span><span class="sxs-lookup"><span data-stu-id="437ba-128">dsize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="437ba-129">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="437ba-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="437ba-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="437ba-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="437ba-131">限定詞： WmiDataId (7) </span><span class="sxs-lookup"><span data-stu-id="437ba-131">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="437ba-132">目的地封包的大小。</span><span class="sxs-lookup"><span data-stu-id="437ba-132">Size of the destination packet.</span></span>

</dd> <dt>

<span data-ttu-id="437ba-133">saddr</span><span class="sxs-lookup"><span data-stu-id="437ba-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="437ba-134">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="437ba-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="437ba-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="437ba-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="437ba-136">限定詞： WmiDataId (2) ，副檔名 ( "IPAddr" ) </span><span class="sxs-lookup"><span data-stu-id="437ba-136">Qualifiers: WmiDataId(2), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="437ba-137">來源 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="437ba-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="437ba-138">{1}size{2}</span><span class="sxs-lookup"><span data-stu-id="437ba-138">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="437ba-139">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="437ba-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="437ba-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="437ba-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="437ba-141">限定詞： WmiDataId (4) </span><span class="sxs-lookup"><span data-stu-id="437ba-141">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="437ba-142">來源封包的大小。</span><span class="sxs-lookup"><span data-stu-id="437ba-142">Size of the source packet.</span></span>

</dd> <dt>

<span data-ttu-id="437ba-143">運動</span><span class="sxs-lookup"><span data-stu-id="437ba-143">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="437ba-144">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="437ba-144">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="437ba-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="437ba-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="437ba-146">限定詞： WmiDataId (3) ，擴充 ( "Port" ) </span><span class="sxs-lookup"><span data-stu-id="437ba-146">Qualifiers: WmiDataId(3), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="437ba-147">來源埠號碼。</span><span class="sxs-lookup"><span data-stu-id="437ba-147">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="437ba-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="437ba-148">Requirements</span></span>



| <span data-ttu-id="437ba-149">需求</span><span class="sxs-lookup"><span data-stu-id="437ba-149">Requirement</span></span> | <span data-ttu-id="437ba-150">值</span><span class="sxs-lookup"><span data-stu-id="437ba-150">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="437ba-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="437ba-151">Minimum supported client</span></span><br/> | <span data-ttu-id="437ba-152">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="437ba-152">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="437ba-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="437ba-153">Minimum supported server</span></span><br/> | <span data-ttu-id="437ba-154">都不支援</span><span class="sxs-lookup"><span data-stu-id="437ba-154">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="437ba-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="437ba-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="437ba-156">**UdpIp \_ V0**</span><span class="sxs-lookup"><span data-stu-id="437ba-156">**UdpIp\_V0**</span></span>](udpip-v0.md)
</dt> </dl>

 

 




