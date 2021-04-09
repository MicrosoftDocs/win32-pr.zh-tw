---
title: 'RTM_IPX_ROUTE 結構 (Rtm) '
description: RTM \_ ipx \_ 路由結構包含描述 IPX 通訊協定系列之路由的資訊。
ms.assetid: ffa0637c-2197-4ebd-a5ef-e174dd0ccb15
keywords:
- RTM_IPX_ROUTE 結構 RAS
- PRTM_IPX_ROUTE 結構指標 RAS
topic_type:
- apiref
api_name:
- RTM_IPX_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32333dd6a6b53ee4600dda388a318bdf9404b6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934151"
---
# <a name="rtm_ipx_route-structure"></a><span data-ttu-id="5e998-105">RTM \_ IPX \_ 路由結構</span><span class="sxs-lookup"><span data-stu-id="5e998-105">RTM\_IPX\_ROUTE structure</span></span>

<span data-ttu-id="5e998-106">\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。</span><span class="sxs-lookup"><span data-stu-id="5e998-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="5e998-107">應用程式應該使用路由表管理員第2版 API。\]</span><span class="sxs-lookup"><span data-stu-id="5e998-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="5e998-108">**RTM \_ ipx \_ 路由** 結構包含描述 IPX 通訊協定系列之路由的資訊。</span><span class="sxs-lookup"><span data-stu-id="5e998-108">The **RTM\_IPX\_ROUTE** structure contains information that describes a route for the IPX protocol family.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e998-109">語法</span><span class="sxs-lookup"><span data-stu-id="5e998-109">Syntax</span></span>


```C++
typedef struct _RTM_IPX_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IPX_NETWORK            RR_Network;
  IPX_NEXT_HOP_ADDRESS   RR_NextHopAddress;
  IPX_SPECIFIC_DATA      RR_FamilySpecificData;
} RTM_IPX_ROUTE, *PRTM_IPX_ROUTE;
```



## <a name="members"></a><span data-ttu-id="5e998-110">成員</span><span class="sxs-lookup"><span data-stu-id="5e998-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="5e998-111">**RR \_ 時間戳記**</span><span class="sxs-lookup"><span data-stu-id="5e998-111">**RR\_TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="5e998-112">指定建立或上次更新路由專案的時間。</span><span class="sxs-lookup"><span data-stu-id="5e998-112">Specifies the time that the route entry was created or last updated.</span></span> <span data-ttu-id="5e998-113">此成員是由路由表管理員所設定。</span><span class="sxs-lookup"><span data-stu-id="5e998-113">This member is set by the routing table manager.</span></span> <span data-ttu-id="5e998-114">時間會表示為 FILETIME 結構。</span><span class="sxs-lookup"><span data-stu-id="5e998-114">The time is expressed as a FILETIME structure.</span></span>

</dd> <dt>

<span data-ttu-id="5e998-115">**RR \_ RoutingProtocol**</span><span class="sxs-lookup"><span data-stu-id="5e998-115">**RR\_RoutingProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="5e998-116">指定新增路由的路由通訊協定。</span><span class="sxs-lookup"><span data-stu-id="5e998-116">Specifies the routing protocol that added the route.</span></span>

</dd> <dt>

<span data-ttu-id="5e998-117">**RR \_ InterfaceID**</span><span class="sxs-lookup"><span data-stu-id="5e998-117">**RR\_InterfaceID**</span></span>
</dt> <dd>

<span data-ttu-id="5e998-118">指定取得路由的介面。</span><span class="sxs-lookup"><span data-stu-id="5e998-118">Specifies the interface through which the route was obtained.</span></span>

</dd> <dt>

<span data-ttu-id="5e998-119">**RR \_ ProtocolSpecificData**</span><span class="sxs-lookup"><span data-stu-id="5e998-119">**RR\_ProtocolSpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="5e998-120">指定 [**通訊協定 \_ 特定的 \_ 資料**](protocol-specific-data.md) 結構，其中包含針對路由通訊協定特定資料所保留的記憶體。</span><span class="sxs-lookup"><span data-stu-id="5e998-120">Specifies a [**PROTOCOL\_SPECIFIC\_DATA**](protocol-specific-data.md) structure containing memory reserved for data specific to routing protocols.</span></span>

</dd> <dt>

<span data-ttu-id="5e998-121">**RR \_ 網路**</span><span class="sxs-lookup"><span data-stu-id="5e998-121">**RR\_Network**</span></span>
</dt> <dd>

<span data-ttu-id="5e998-122">指定包含 IP 網路位址的 [**IPX \_ 網路**](ipx-network.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="5e998-122">Specifies an [**IPX\_NETWORK**](ipx-network.md) structure that contains an IP network address.</span></span>

</dd> <dt>

<span data-ttu-id="5e998-123">**RR \_ NextHopAddress**</span><span class="sxs-lookup"><span data-stu-id="5e998-123">**RR\_NextHopAddress**</span></span>
</dt> <dd>

<span data-ttu-id="5e998-124">指定包含下一個躍點路由器位址的 [**IPX \_ 下一個 \_ 躍點 \_ 位址**](ipx-next-hop-address.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="5e998-124">Specifies an [**IPX\_NEXT\_HOP\_ADDRESS**](ipx-next-hop-address.md) structure that contains the address of the next-hop router.</span></span>

</dd> <dt>

<span data-ttu-id="5e998-125">**RR \_ FamilySpecificData**</span><span class="sxs-lookup"><span data-stu-id="5e998-125">**RR\_FamilySpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="5e998-126">指定包含 IPX 通訊協定系列專屬資料的 [**\_ 特定 ipx \_ 資料**](ipx-specific-data.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="5e998-126">Specifies an [**IPX\_SPECIFIC\_DATA**](ipx-specific-data.md) structure that contains data specific to the IPX protocol family.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e998-127">備註</span><span class="sxs-lookup"><span data-stu-id="5e998-127">Remarks</span></span>

<span data-ttu-id="5e998-128">**RTM \_ IPX \_ 路由** 結構的成員都已對齊 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="5e998-128">The members of the **RTM\_IPX\_ROUTE** structure are all **DWORD** aligned.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e998-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e998-129">Requirements</span></span>



| <span data-ttu-id="5e998-130">需求</span><span class="sxs-lookup"><span data-stu-id="5e998-130">Requirement</span></span> | <span data-ttu-id="5e998-131">值</span><span class="sxs-lookup"><span data-stu-id="5e998-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5e998-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5e998-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5e998-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="5e998-133">None supported</span></span><br/>                                                        |
| <span data-ttu-id="5e998-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5e998-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5e998-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e998-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5e998-136">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="5e998-136">End of server support</span></span><br/>    | <span data-ttu-id="5e998-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5e998-137">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="5e998-138">標頭</span><span class="sxs-lookup"><span data-stu-id="5e998-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e998-139"><dt>Rtm. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e998-139"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e998-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5e998-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e998-141">路由表管理員第1版參考</span><span class="sxs-lookup"><span data-stu-id="5e998-141">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="5e998-142">路由表管理員 \_ 第1版 \_ 結構</span><span class="sxs-lookup"><span data-stu-id="5e998-142">Routing Table Manager Version\_1\_Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="5e998-143">**IPX \_ 網路**</span><span class="sxs-lookup"><span data-stu-id="5e998-143">**IPX\_NETWORK**</span></span>](ipx-network.md)
</dt> <dt>

[<span data-ttu-id="5e998-144">**IPX \_ 下一個 \_ 躍點 \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="5e998-144">**IPX\_NEXT\_HOP\_ADDRESS**</span></span>](ipx-next-hop-address.md)
</dt> <dt>

[<span data-ttu-id="5e998-145">**\_特定 IPX \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="5e998-145">**IPX\_SPECIFIC\_DATA**</span></span>](ipx-specific-data.md)
</dt> </dl>

 

 





