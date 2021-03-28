---
description: 此類別是 UDP/IP 事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
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
ms.openlocfilehash: 2813476bc2c820d1872e787dc047fafccd3b7d52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944855"
---
# <a name="udpip_v0_typegroup1-class"></a><span data-ttu-id="963b4-104">UdpIp \_ V0 \_ TypeGroup1 類別</span><span class="sxs-lookup"><span data-stu-id="963b4-104">UdpIp\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="963b4-105">此類別是 UDP/IP 事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="963b4-105">This class is the event type class for UDP/IP events.</span></span>

<span data-ttu-id="963b4-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="963b4-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="963b4-107">語法</span><span class="sxs-lookup"><span data-stu-id="963b4-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="963b4-108">成員</span><span class="sxs-lookup"><span data-stu-id="963b4-108">Members</span></span>

<span data-ttu-id="963b4-109">**UdpIp \_ V0 \_ TypeGroup1** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="963b4-109">The **UdpIp\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="963b4-110">屬性</span><span class="sxs-lookup"><span data-stu-id="963b4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="963b4-111">屬性</span><span class="sxs-lookup"><span data-stu-id="963b4-111">Properties</span></span>

<span data-ttu-id="963b4-112">**UdpIp \_ V0 \_ TypeGroup1** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="963b4-112">The **UdpIp\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="963b4-113">內容</span><span class="sxs-lookup"><span data-stu-id="963b4-113">context</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="963b4-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="963b4-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="963b4-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="963b4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="963b4-116">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="963b4-116">Qualifiers: WmiDataId(1), pointer</span></span>
</dt> </dl>

<span data-ttu-id="963b4-117">發出或接收要求之位址物件的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="963b4-117">Process identifier for the Address Object that made or received the request.</span></span>

</dd> <dt>

<span data-ttu-id="963b4-118">daddr</span><span class="sxs-lookup"><span data-stu-id="963b4-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="963b4-119">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="963b4-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="963b4-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="963b4-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="963b4-121">限定詞： WmiDataId (5) ，副檔名 ( "IPAddr" ) </span><span class="sxs-lookup"><span data-stu-id="963b4-121">Qualifiers: WmiDataId(5), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="963b4-122">目的地 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="963b4-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="963b4-123">dport</span><span class="sxs-lookup"><span data-stu-id="963b4-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="963b4-124">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="963b4-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="963b4-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="963b4-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="963b4-126">限定詞： WmiDataId (6) ，擴充 ( "Port" ) </span><span class="sxs-lookup"><span data-stu-id="963b4-126">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="963b4-127">目的地埠號碼。</span><span class="sxs-lookup"><span data-stu-id="963b4-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="963b4-128">dsize</span><span class="sxs-lookup"><span data-stu-id="963b4-128">dsize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="963b4-129">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="963b4-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="963b4-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="963b4-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="963b4-131">限定詞： WmiDataId (7) </span><span class="sxs-lookup"><span data-stu-id="963b4-131">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="963b4-132">目的地封包的大小。</span><span class="sxs-lookup"><span data-stu-id="963b4-132">Size of the destination packet.</span></span>

</dd> <dt>

<span data-ttu-id="963b4-133">saddr</span><span class="sxs-lookup"><span data-stu-id="963b4-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="963b4-134">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="963b4-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="963b4-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="963b4-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="963b4-136">限定詞： WmiDataId (2) ，副檔名 ( "IPAddr" ) </span><span class="sxs-lookup"><span data-stu-id="963b4-136">Qualifiers: WmiDataId(2), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="963b4-137">來源 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="963b4-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="963b4-138">{1}size{2}</span><span class="sxs-lookup"><span data-stu-id="963b4-138">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="963b4-139">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="963b4-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="963b4-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="963b4-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="963b4-141">限定詞： WmiDataId (4) </span><span class="sxs-lookup"><span data-stu-id="963b4-141">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="963b4-142">來源封包的大小。</span><span class="sxs-lookup"><span data-stu-id="963b4-142">Size of the source packet.</span></span>

</dd> <dt>

<span data-ttu-id="963b4-143">運動</span><span class="sxs-lookup"><span data-stu-id="963b4-143">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="963b4-144">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="963b4-144">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="963b4-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="963b4-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="963b4-146">限定詞： WmiDataId (3) ，擴充 ( "Port" ) </span><span class="sxs-lookup"><span data-stu-id="963b4-146">Qualifiers: WmiDataId(3), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="963b4-147">來源埠號碼。</span><span class="sxs-lookup"><span data-stu-id="963b4-147">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="963b4-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="963b4-148">Requirements</span></span>



| <span data-ttu-id="963b4-149">需求</span><span class="sxs-lookup"><span data-stu-id="963b4-149">Requirement</span></span> | <span data-ttu-id="963b4-150">值</span><span class="sxs-lookup"><span data-stu-id="963b4-150">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="963b4-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="963b4-151">Minimum supported client</span></span><br/> | <span data-ttu-id="963b4-152">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="963b4-152">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="963b4-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="963b4-153">Minimum supported server</span></span><br/> | <span data-ttu-id="963b4-154">都不支援</span><span class="sxs-lookup"><span data-stu-id="963b4-154">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="963b4-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="963b4-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="963b4-156">**UdpIp \_ V0**</span><span class="sxs-lookup"><span data-stu-id="963b4-156">**UdpIp\_V0**</span></span>](udpip-v0.md)
</dt> </dl>

 

 




