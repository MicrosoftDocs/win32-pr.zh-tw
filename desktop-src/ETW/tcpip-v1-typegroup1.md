---
description: TcpIp_V1_TypeGroup1 類別-這個類別是 TCP/IP 事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 1cde7e37-52da-4108-90ce-7647a5653f65
title: TcpIp_V1_TypeGroup1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_V1_TypeGroup1
- TcpIp_V1_TypeGroup1.PID
- TcpIp_V1_TypeGroup1.size
- TcpIp_V1_TypeGroup1.daddr
- TcpIp_V1_TypeGroup1.saddr
- TcpIp_V1_TypeGroup1.dport
- TcpIp_V1_TypeGroup1.sport
api_type:
- NA
api_location: ''
ms.openlocfilehash: 831dfdc228e2c8e128f328784046e833b0b45a39
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105756"
---
# <a name="tcpip_v1_typegroup1-class"></a><span data-ttu-id="1ee60-104">TcpIp \_ V1 \_ TypeGroup1 類別</span><span class="sxs-lookup"><span data-stu-id="1ee60-104">TcpIp\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="1ee60-105">這個類別是 TCP/IP 事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="1ee60-105">This class is the event type class for TCP/IP events.</span></span>

<span data-ttu-id="1ee60-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="1ee60-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ee60-107">語法</span><span class="sxs-lookup"><span data-stu-id="1ee60-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16}, EventTypeName{"Send", "Recv", "Connect", "Disconnect", "Retransmit", "Accept", "Reconnect"}]
class TcpIp_V1_TypeGroup1 : TcpIp_V1
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
};
```

## <a name="members"></a><span data-ttu-id="1ee60-108">成員</span><span class="sxs-lookup"><span data-stu-id="1ee60-108">Members</span></span>

<span data-ttu-id="1ee60-109">**TcpIp \_ V1 \_ TypeGroup1** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1ee60-109">The **TcpIp\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="1ee60-110">屬性</span><span class="sxs-lookup"><span data-stu-id="1ee60-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1ee60-111">屬性</span><span class="sxs-lookup"><span data-stu-id="1ee60-111">Properties</span></span>

<span data-ttu-id="1ee60-112">**TcpIp \_ V1 \_ TypeGroup1** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1ee60-112">The **TcpIp\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1ee60-113">daddr</span><span class="sxs-lookup"><span data-stu-id="1ee60-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ee60-114">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="1ee60-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="1ee60-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ee60-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ee60-116">限定詞： WmiDataId (3) ，副檔名 ( "IPAddr" ) </span><span class="sxs-lookup"><span data-stu-id="1ee60-116">Qualifiers: WmiDataId(3), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="1ee60-117">目的地 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="1ee60-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="1ee60-118">dport</span><span class="sxs-lookup"><span data-stu-id="1ee60-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ee60-119">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="1ee60-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="1ee60-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ee60-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ee60-121">限定詞： WmiDataId (5) ，擴充 ( "Port" ) </span><span class="sxs-lookup"><span data-stu-id="1ee60-121">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="1ee60-122">目的地埠號碼。</span><span class="sxs-lookup"><span data-stu-id="1ee60-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="1ee60-123">PID</span><span class="sxs-lookup"><span data-stu-id="1ee60-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ee60-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1ee60-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ee60-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ee60-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ee60-126">限定詞： WmiDataId (1) </span><span class="sxs-lookup"><span data-stu-id="1ee60-126">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="1ee60-127">與要求相關聯之進程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1ee60-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="1ee60-128">saddr</span><span class="sxs-lookup"><span data-stu-id="1ee60-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ee60-129">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="1ee60-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="1ee60-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ee60-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ee60-131">限定詞： WmiDataId (4) ，副檔名 ( "IPAddr" ) </span><span class="sxs-lookup"><span data-stu-id="1ee60-131">Qualifiers: WmiDataId(4), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="1ee60-132">來源 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="1ee60-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="1ee60-133">{1}size{2}</span><span class="sxs-lookup"><span data-stu-id="1ee60-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ee60-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1ee60-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ee60-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ee60-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ee60-136">限定詞： WmiDataId (2) </span><span class="sxs-lookup"><span data-stu-id="1ee60-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="1ee60-137">封包的大小。</span><span class="sxs-lookup"><span data-stu-id="1ee60-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="1ee60-138">運動</span><span class="sxs-lookup"><span data-stu-id="1ee60-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ee60-139">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="1ee60-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="1ee60-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ee60-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ee60-141">限定詞： WmiDataId (6) ，擴充 ( "Port" ) </span><span class="sxs-lookup"><span data-stu-id="1ee60-141">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="1ee60-142">來源埠號碼。</span><span class="sxs-lookup"><span data-stu-id="1ee60-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1ee60-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ee60-143">Requirements</span></span>



| <span data-ttu-id="1ee60-144">需求</span><span class="sxs-lookup"><span data-stu-id="1ee60-144">Requirement</span></span> | <span data-ttu-id="1ee60-145">值</span><span class="sxs-lookup"><span data-stu-id="1ee60-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1ee60-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ee60-146">Minimum supported client</span></span><br/> | <span data-ttu-id="1ee60-147">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ee60-147">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="1ee60-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ee60-148">Minimum supported server</span></span><br/> | <span data-ttu-id="1ee60-149">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ee60-149">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1ee60-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ee60-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ee60-151">**TcpIp \_ V1**</span><span class="sxs-lookup"><span data-stu-id="1ee60-151">**TcpIp\_V1**</span></span>](tcpip-v1.md)
</dt> </dl>

 

 




