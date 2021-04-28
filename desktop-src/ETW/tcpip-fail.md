---
description: TcpIp_Fail 類別-這個類別是 TCP/IP 失敗事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 1fe20b8c-b8f1-4db0-af78-1ebfc40b2bbd
title: TcpIp_Fail 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_Fail
- TcpIp_Fail.Proto
- TcpIp_Fail.FailureCode
api_type:
- NA
api_location: ''
ms.openlocfilehash: 897c42a1c2530d3e41d1f937d5d59356a2913e2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105846"
---
# <a name="tcpip_fail-class"></a><span data-ttu-id="f254d-104">TcpIp \_ 失敗類別</span><span class="sxs-lookup"><span data-stu-id="f254d-104">TcpIp\_Fail class</span></span>

<span data-ttu-id="f254d-105">這個類別是 TCP/IP 失敗事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="f254d-105">This class is the event type class for TCP/IP failure events.</span></span>

<span data-ttu-id="f254d-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="f254d-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f254d-107">語法</span><span class="sxs-lookup"><span data-stu-id="f254d-107">Syntax</span></span>

``` syntax
[EventType{17}, EventTypeName{"Fail"}]
class TcpIp_Fail : TcpIp
{
  uint16 Proto;
  uint16 FailureCode;
};
```

## <a name="members"></a><span data-ttu-id="f254d-108">成員</span><span class="sxs-lookup"><span data-stu-id="f254d-108">Members</span></span>

<span data-ttu-id="f254d-109">**TcpIp \_ Fail** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f254d-109">The **TcpIp\_Fail** class has these types of members:</span></span>

-   [<span data-ttu-id="f254d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="f254d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f254d-111">屬性</span><span class="sxs-lookup"><span data-stu-id="f254d-111">Properties</span></span>

<span data-ttu-id="f254d-112">**TcpIp \_ 失敗** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f254d-112">The **TcpIp\_Fail** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f254d-113">**[FailureCode]**</span><span class="sxs-lookup"><span data-stu-id="f254d-113">**FailureCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f254d-114">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f254d-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f254d-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f254d-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f254d-116">失敗的原因。</span><span class="sxs-lookup"><span data-stu-id="f254d-116">Reason for the failure.</span></span> <span data-ttu-id="f254d-117">可以是下列其中一個程式碼：</span><span class="sxs-lookup"><span data-stu-id="f254d-117">Can be one of the following codes:</span></span>

<dl> <dt>

<span data-ttu-id="f254d-118"><span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**錯誤 \_\_資源不足** (1) </span><span class="sxs-lookup"><span data-stu-id="f254d-118"><span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**ERROR\_INSUFFICIENT\_RESOURCES** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f254d-119"><span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**錯誤 \_太 \_ 多 \_ 位址** (2) </span><span class="sxs-lookup"><span data-stu-id="f254d-119"><span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**ERROR\_TOO\_MANY\_ADDRESSES** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f254d-120"><span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**錯誤 \_位址 \_ 存在** (3) </span><span class="sxs-lookup"><span data-stu-id="f254d-120"><span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**ERROR\_ADDRESS\_EXISTS** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f254d-121"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**錯誤 \_不正確 \_ 位址** (4) </span><span class="sxs-lookup"><span data-stu-id="f254d-121"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERROR\_INVALID\_ADDRESS** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f254d-122"><span id="ERROR_OTHER"></span><span id="error_other"></span>**錯誤 \_其他** (5) </span><span class="sxs-lookup"><span data-stu-id="f254d-122"><span id="ERROR_OTHER"></span><span id="error_other"></span>**ERROR\_OTHER** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f254d-123"><span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**錯誤 \_TIMEWAIT \_ 位址 \_ 存在** (6) </span><span class="sxs-lookup"><span data-stu-id="f254d-123"><span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**ERROR\_TIMEWAIT\_ADDRESS\_EXIST** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f254d-124">**原**</span><span class="sxs-lookup"><span data-stu-id="f254d-124">**Proto**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f254d-125">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f254d-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f254d-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f254d-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f254d-127">識別通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f254d-127">Identifies the protocol.</span></span> <span data-ttu-id="f254d-128">可以是下列值之一：</span><span class="sxs-lookup"><span data-stu-id="f254d-128">Can be one of the following values:</span></span>



| <span data-ttu-id="f254d-129">值</span><span class="sxs-lookup"><span data-stu-id="f254d-129">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="f254d-130">意義</span><span class="sxs-lookup"><span data-stu-id="f254d-130">Meaning</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <span data-ttu-id="f254d-131"><dt>**AF \_INET**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f254d-131"><dt>**AF\_INET**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="f254d-132">第四版網際網路協定 (IPv4) 位址系列。</span><span class="sxs-lookup"><span data-stu-id="f254d-132">The Internet Protocol version 4 (IPv4) address family.</span></span><br/>  |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <span data-ttu-id="f254d-133"><dt>**AF \_INET6**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="f254d-133"><dt>**AF\_INET6**</dt> <dt>23</dt></span></span> </dl> | <span data-ttu-id="f254d-134">網際網路通訊協定第6版 (IPv6) 位址系列。</span><span class="sxs-lookup"><span data-stu-id="f254d-134">The Internet Protocol version 6 (IPv6) address family..</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f254d-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="f254d-135">Requirements</span></span>



| <span data-ttu-id="f254d-136">需求</span><span class="sxs-lookup"><span data-stu-id="f254d-136">Requirement</span></span> | <span data-ttu-id="f254d-137">值</span><span class="sxs-lookup"><span data-stu-id="f254d-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f254d-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f254d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f254d-139">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f254d-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f254d-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f254d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f254d-141">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f254d-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f254d-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f254d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f254d-143">**Tcpip.sys**</span><span class="sxs-lookup"><span data-stu-id="f254d-143">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




