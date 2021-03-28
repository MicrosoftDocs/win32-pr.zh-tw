---
description: 這個類別是 TCP/IP 失敗事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 552e63ef-70e4-4bc4-be33-bd77bd5acd61
title: UdpIp_Fail 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_Fail
- UdpIp_Fail.Proto
- UdpIp_Fail.FailureCode
api_type:
- NA
api_location: ''
ms.openlocfilehash: aef0194d296395501500022bf4cae8b9c8a8f188
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973824"
---
# <a name="udpip_fail-class"></a><span data-ttu-id="64c84-104">UdpIp \_ Fail 類別</span><span class="sxs-lookup"><span data-stu-id="64c84-104">UdpIp\_Fail class</span></span>

<span data-ttu-id="64c84-105">這個類別是 TCP/IP 失敗事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="64c84-105">This class is the event type class for TCP/IP failure events.</span></span>

<span data-ttu-id="64c84-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="64c84-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="64c84-107">語法</span><span class="sxs-lookup"><span data-stu-id="64c84-107">Syntax</span></span>

``` syntax
[EventType{17}, EventTypeName{"Fail"}]
class UdpIp_Fail : UdpIp
{
  uint16 Proto;
  uint16 FailureCode;
};
```

## <a name="members"></a><span data-ttu-id="64c84-108">成員</span><span class="sxs-lookup"><span data-stu-id="64c84-108">Members</span></span>

<span data-ttu-id="64c84-109">**UdpIp \_ Fail** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="64c84-109">The **UdpIp\_Fail** class has these types of members:</span></span>

-   [<span data-ttu-id="64c84-110">屬性</span><span class="sxs-lookup"><span data-stu-id="64c84-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="64c84-111">屬性</span><span class="sxs-lookup"><span data-stu-id="64c84-111">Properties</span></span>

<span data-ttu-id="64c84-112">**UdpIp \_ Fail** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="64c84-112">The **UdpIp\_Fail** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="64c84-113">**[FailureCode]**</span><span class="sxs-lookup"><span data-stu-id="64c84-113">**FailureCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c84-114">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="64c84-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="64c84-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c84-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64c84-116">失敗的原因。</span><span class="sxs-lookup"><span data-stu-id="64c84-116">Reason for the failure.</span></span> <span data-ttu-id="64c84-117">可以是下列其中一個程式碼：</span><span class="sxs-lookup"><span data-stu-id="64c84-117">Can be one of the following codes:</span></span>

<dl> <dt>

<span data-ttu-id="64c84-118"><span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**錯誤 \_\_資源不足** (1) </span><span class="sxs-lookup"><span data-stu-id="64c84-118"><span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**ERROR\_INSUFFICIENT\_RESOURCES** (1)</span></span>
</dt> <dt>

<span data-ttu-id="64c84-119"><span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**錯誤 \_太 \_ 多 \_ 位址** (2) </span><span class="sxs-lookup"><span data-stu-id="64c84-119"><span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**ERROR\_TOO\_MANY\_ADDRESSES** (2)</span></span>
</dt> <dt>

<span data-ttu-id="64c84-120"><span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**錯誤 \_位址 \_ 存在** (3) </span><span class="sxs-lookup"><span data-stu-id="64c84-120"><span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**ERROR\_ADDRESS\_EXISTS** (3)</span></span>
</dt> <dt>

<span data-ttu-id="64c84-121"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**錯誤 \_不正確 \_ 位址** (4) </span><span class="sxs-lookup"><span data-stu-id="64c84-121"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERROR\_INVALID\_ADDRESS** (4)</span></span>
</dt> <dt>

<span data-ttu-id="64c84-122"><span id="ERROR_OTHER"></span><span id="error_other"></span>**錯誤 \_其他** (5) </span><span class="sxs-lookup"><span data-stu-id="64c84-122"><span id="ERROR_OTHER"></span><span id="error_other"></span>**ERROR\_OTHER** (5)</span></span>
</dt> <dt>

<span data-ttu-id="64c84-123"><span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**錯誤 \_TIMEWAIT \_ 位址 \_ 存在** (6) </span><span class="sxs-lookup"><span data-stu-id="64c84-123"><span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**ERROR\_TIMEWAIT\_ADDRESS\_EXIST** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="64c84-124">**原**</span><span class="sxs-lookup"><span data-stu-id="64c84-124">**Proto**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c84-125">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="64c84-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="64c84-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c84-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64c84-127">識別通訊協定。</span><span class="sxs-lookup"><span data-stu-id="64c84-127">Identifies the protocol.</span></span> <span data-ttu-id="64c84-128">可以是下列值之一：</span><span class="sxs-lookup"><span data-stu-id="64c84-128">Can be one of the following values:</span></span>



| <span data-ttu-id="64c84-129">值</span><span class="sxs-lookup"><span data-stu-id="64c84-129">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="64c84-130">意義</span><span class="sxs-lookup"><span data-stu-id="64c84-130">Meaning</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <span data-ttu-id="64c84-131"><dt>**AF \_INET**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="64c84-131"><dt>**AF\_INET**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="64c84-132">第四版網際網路協定 (IPv4) 位址系列。</span><span class="sxs-lookup"><span data-stu-id="64c84-132">The Internet Protocol version 4 (IPv4) address family.</span></span><br/>  |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <span data-ttu-id="64c84-133"><dt>**AF \_INET6**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="64c84-133"><dt>**AF\_INET6**</dt> <dt>23</dt></span></span> </dl> | <span data-ttu-id="64c84-134">網際網路通訊協定第6版 (IPv6) 位址系列。</span><span class="sxs-lookup"><span data-stu-id="64c84-134">The Internet Protocol version 6 (IPv6) address family..</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="64c84-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="64c84-135">Requirements</span></span>



| <span data-ttu-id="64c84-136">需求</span><span class="sxs-lookup"><span data-stu-id="64c84-136">Requirement</span></span> | <span data-ttu-id="64c84-137">值</span><span class="sxs-lookup"><span data-stu-id="64c84-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="64c84-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="64c84-138">Minimum supported client</span></span><br/> | <span data-ttu-id="64c84-139">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64c84-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="64c84-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="64c84-140">Minimum supported server</span></span><br/> | <span data-ttu-id="64c84-141">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64c84-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="64c84-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64c84-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64c84-143">**UdpIp**</span><span class="sxs-lookup"><span data-stu-id="64c84-143">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




