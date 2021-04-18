---
title: 'RTM_IP_ROUTE 結構 (Rtm) '
description: RTM \_ ip \_ 路由結構包含描述 IP 通訊協定系列所擁有之路由的資訊。
ms.assetid: e752a4ae-a6bf-4cd3-9638-7615ff3901b7
keywords:
- RTM_IP_ROUTE 結構 RAS
- PRTM_IP_ROUTE 結構指標 RAS
topic_type:
- apiref
api_name:
- RTM_IP_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1978503a3ec37e0c39716569030d5ea6599e19d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966155"
---
# <a name="rtm_ip_route-structure"></a><span data-ttu-id="91211-105">RTM \_ IP \_ 路由結構</span><span class="sxs-lookup"><span data-stu-id="91211-105">RTM\_IP\_ROUTE structure</span></span>

<span data-ttu-id="91211-106">\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。</span><span class="sxs-lookup"><span data-stu-id="91211-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="91211-107">應用程式應該使用路由表管理員第2版 API。\]</span><span class="sxs-lookup"><span data-stu-id="91211-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="91211-108">**RTM \_ ip \_ 路由** 結構包含描述 IP 通訊協定系列所擁有之路由的資訊。</span><span class="sxs-lookup"><span data-stu-id="91211-108">The **RTM\_IP\_ROUTE** structure contains information that describes a route owned by the IP protocol family.</span></span>

## <a name="syntax"></a><span data-ttu-id="91211-109">語法</span><span class="sxs-lookup"><span data-stu-id="91211-109">Syntax</span></span>


```C++
typedef struct _RTM_IP_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IP_NETWORK             RR_Network;
  IP_NEXT_HOP_ADDRESS    RR_NextHopAddress;
  IP_SPECIFIC_DATA       RR_FamilySpecificData;
} RTM_IP_ROUTE, *PRTM_IP_ROUTE;
```



## <a name="members"></a><span data-ttu-id="91211-110">成員</span><span class="sxs-lookup"><span data-stu-id="91211-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="91211-111">**RR \_ 時間戳記**</span><span class="sxs-lookup"><span data-stu-id="91211-111">**RR\_TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="91211-112">指定建立或上次更新路由專案的時間。</span><span class="sxs-lookup"><span data-stu-id="91211-112">Specifies the time that the route entry was created or last updated.</span></span> <span data-ttu-id="91211-113">此成員是由路由表管理員所設定。</span><span class="sxs-lookup"><span data-stu-id="91211-113">This member is set by the routing table manager.</span></span> <span data-ttu-id="91211-114">時間會表示為 FILETIME 結構。</span><span class="sxs-lookup"><span data-stu-id="91211-114">The time is expressed as a FILETIME structure.</span></span>

</dd> <dt>

<span data-ttu-id="91211-115">**RR \_ RoutingProtocol**</span><span class="sxs-lookup"><span data-stu-id="91211-115">**RR\_RoutingProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="91211-116">指定新增路由的路由通訊協定。</span><span class="sxs-lookup"><span data-stu-id="91211-116">Specifies the routing protocol that added the route.</span></span>

</dd> <dt>

<span data-ttu-id="91211-117">**RR \_ InterfaceID**</span><span class="sxs-lookup"><span data-stu-id="91211-117">**RR\_InterfaceID**</span></span>
</dt> <dd>

<span data-ttu-id="91211-118">指定取得路由的介面。</span><span class="sxs-lookup"><span data-stu-id="91211-118">Specifies the interface through which the route was obtained.</span></span>

</dd> <dt>

<span data-ttu-id="91211-119">**RR \_ ProtocolSpecificData**</span><span class="sxs-lookup"><span data-stu-id="91211-119">**RR\_ProtocolSpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="91211-120">指定 [**通訊協定 \_ 特定的 \_ 資料**](protocol-specific-data.md) 結構，其中包含保留給路由通訊協定特定資料的記憶體。</span><span class="sxs-lookup"><span data-stu-id="91211-120">Specifies a [**PROTOCOL\_SPECIFIC\_DATA**](protocol-specific-data.md) structure that contains memory reserved for routing-protocol-specific data.</span></span>

</dd> <dt>

<span data-ttu-id="91211-121">**RR \_ 網路**</span><span class="sxs-lookup"><span data-stu-id="91211-121">**RR\_Network**</span></span>
</dt> <dd>

<span data-ttu-id="91211-122">指定包含 IP 網路位址的 [**ip \_ 網路**](ip-network.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="91211-122">Specifies an [**IP\_NETWORK**](ip-network.md) structure that contains an IP network address.</span></span>

</dd> <dt>

<span data-ttu-id="91211-123">**RR \_ NextHopAddress**</span><span class="sxs-lookup"><span data-stu-id="91211-123">**RR\_NextHopAddress**</span></span>
</dt> <dd>

<span data-ttu-id="91211-124">指定 [**IP \_ 下一個 \_ 躍點 \_ 位址**](ip-next-hop-address.md) 結構，其中包含下一個躍點路由器的位址。</span><span class="sxs-lookup"><span data-stu-id="91211-124">Specifies an [**IP\_NEXT\_HOP\_ADDRESS**](ip-next-hop-address.md) structure that contains the address of the next-hop router.</span></span>

</dd> <dt>

<span data-ttu-id="91211-125">**RR \_ FamilySpecificData**</span><span class="sxs-lookup"><span data-stu-id="91211-125">**RR\_FamilySpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="91211-126">指定包含 IP 通訊協定系列特定資料的 [**ip \_ 特定 \_ 資料**](ip-specific-data.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="91211-126">Specifies an [**IP\_SPECIFIC\_DATA**](ip-specific-data.md) structure that contains IP protocol-family-specific data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91211-127">備註</span><span class="sxs-lookup"><span data-stu-id="91211-127">Remarks</span></span>

<span data-ttu-id="91211-128">**RTM \_ IP \_ 路由** 結構的成員都已對齊 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="91211-128">The members of the **RTM\_IP\_ROUTE** structure are all **DWORD** aligned.</span></span>

## <a name="requirements"></a><span data-ttu-id="91211-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="91211-129">Requirements</span></span>



| <span data-ttu-id="91211-130">需求</span><span class="sxs-lookup"><span data-stu-id="91211-130">Requirement</span></span> | <span data-ttu-id="91211-131">值</span><span class="sxs-lookup"><span data-stu-id="91211-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="91211-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="91211-132">Minimum supported client</span></span><br/> | <span data-ttu-id="91211-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="91211-133">None supported</span></span><br/>                                                        |
| <span data-ttu-id="91211-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="91211-134">Minimum supported server</span></span><br/> | <span data-ttu-id="91211-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91211-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="91211-136">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="91211-136">End of server support</span></span><br/>    | <span data-ttu-id="91211-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="91211-137">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="91211-138">標頭</span><span class="sxs-lookup"><span data-stu-id="91211-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="91211-139"><dt>Rtm. h</dt></span><span class="sxs-lookup"><span data-stu-id="91211-139"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91211-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91211-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91211-141">路由表管理員第1版參考</span><span class="sxs-lookup"><span data-stu-id="91211-141">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="91211-142">路由表管理員第1版結構</span><span class="sxs-lookup"><span data-stu-id="91211-142">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="91211-143">**IP \_ 網路**</span><span class="sxs-lookup"><span data-stu-id="91211-143">**IP\_NETWORK**</span></span>](ip-network.md)
</dt> <dt>

[<span data-ttu-id="91211-144">**IP \_ 下一個 \_ 躍點 \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="91211-144">**IP\_NEXT\_HOP\_ADDRESS**</span></span>](ip-next-hop-address.md)
</dt> <dt>

[<span data-ttu-id="91211-145">**IP \_ 特定 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="91211-145">**IP\_SPECIFIC\_DATA**</span></span>](ip-specific-data.md)
</dt> </dl>

 

 





