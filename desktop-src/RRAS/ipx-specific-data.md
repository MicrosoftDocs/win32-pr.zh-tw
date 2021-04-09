---
title: 'IPX_SPECIFIC_DATA 結構 (Rtm) '
description: IPX \_ 特定 \_ 資料結構包含 ipx 特定資料。
ms.assetid: 4d97092d-692c-4dc7-af7f-260dc76c6c08
keywords:
- IPX_SPECIFIC_DATA 結構 RAS
- PIPX_SPECIFIC_DATA 結構指標 RAS
topic_type:
- apiref
api_name:
- IPX_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56badfb6149e416c71b447aca93564b5eb5aba7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933885"
---
# <a name="ipx_specific_data-structure"></a><span data-ttu-id="d7c13-105">IPX \_ 特定 \_ 資料結構</span><span class="sxs-lookup"><span data-stu-id="d7c13-105">IPX\_SPECIFIC\_DATA structure</span></span>

<span data-ttu-id="d7c13-106">\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。</span><span class="sxs-lookup"><span data-stu-id="d7c13-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="d7c13-107">應用程式應該使用路由表管理員第2版 API。\]</span><span class="sxs-lookup"><span data-stu-id="d7c13-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="d7c13-108">**Ipx \_ 特定 \_ 資料** 結構包含 ipx 特定資料。</span><span class="sxs-lookup"><span data-stu-id="d7c13-108">The **IPX\_SPECIFIC\_DATA** structure contains IPX-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7c13-109">語法</span><span class="sxs-lookup"><span data-stu-id="d7c13-109">Syntax</span></span>


```C++
typedef struct _IPX_SPECIFIC_DATA {
  DWORD  FSD_Flags;
  USHORT FSD_TickCount;
  USHORT FSD_HopCount;
} IPX_SPECIFIC_DATA, *PIPX_SPECIFIC_DATA;
```



## <a name="members"></a><span data-ttu-id="d7c13-110">成員</span><span class="sxs-lookup"><span data-stu-id="d7c13-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="d7c13-111">**FSD \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="d7c13-111">**FSD\_Flags**</span></span>
</dt> <dd>

<span data-ttu-id="d7c13-112">指定描述路由的旗標。</span><span class="sxs-lookup"><span data-stu-id="d7c13-112">Specifies flags that describe the route.</span></span> <span data-ttu-id="d7c13-113">目前，這個成員是零或下列旗標值。</span><span class="sxs-lookup"><span data-stu-id="d7c13-113">Currently, this member is either zero or the following flag value.</span></span>



| <span data-ttu-id="d7c13-114">值</span><span class="sxs-lookup"><span data-stu-id="d7c13-114">Value</span></span>                                                                                                                                                                                                      | <span data-ttu-id="d7c13-115">意義</span><span class="sxs-lookup"><span data-stu-id="d7c13-115">Meaning</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="IPX_GLOBAL_CLIENT_WAN_ROUTE"></span><span id="ipx_global_client_wan_route"></span><dl> <span data-ttu-id="d7c13-116"><dt>**IPX \_ 全域 \_ 用戶端 \_ WAN \_ 路由**</dt></span><span class="sxs-lookup"><span data-stu-id="d7c13-116"><dt>**IPX\_GLOBAL\_CLIENT\_WAN\_ROUTE**</dt></span></span> </dl> | <span data-ttu-id="d7c13-117">指定此路由適用于配置給所有 WAN 用戶端的全域網路。</span><span class="sxs-lookup"><span data-stu-id="d7c13-117">Specifies that this route is for the global network allocated for all WAN clients.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d7c13-118">**FSD \_ TickCount**</span><span class="sxs-lookup"><span data-stu-id="d7c13-118">**FSD\_TickCount**</span></span>
</dt> <dd>

<span data-ttu-id="d7c13-119">指定到達目的地網路所花費的刻度數目。</span><span class="sxs-lookup"><span data-stu-id="d7c13-119">Specifies the number of ticks it takes to reach the destination network.</span></span> <span data-ttu-id="d7c13-120">RIP 以外的路由通訊協定應該將其計量轉換成刻度。</span><span class="sxs-lookup"><span data-stu-id="d7c13-120">Routing protocols other than RIP should convert their metrics into ticks.</span></span>

</dd> <dt>

<span data-ttu-id="d7c13-121">**FSD \_ HopCount**</span><span class="sxs-lookup"><span data-stu-id="d7c13-121">**FSD\_HopCount**</span></span>
</dt> <dd>

<span data-ttu-id="d7c13-122">指定與路由相關聯的躍點計數。</span><span class="sxs-lookup"><span data-stu-id="d7c13-122">Specifies the hop count associated with the route.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d7c13-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7c13-123">Requirements</span></span>



| <span data-ttu-id="d7c13-124">需求</span><span class="sxs-lookup"><span data-stu-id="d7c13-124">Requirement</span></span> | <span data-ttu-id="d7c13-125">值</span><span class="sxs-lookup"><span data-stu-id="d7c13-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d7c13-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7c13-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d7c13-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="d7c13-127">None supported</span></span><br/>                                                        |
| <span data-ttu-id="d7c13-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7c13-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d7c13-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7c13-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d7c13-130">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="d7c13-130">End of server support</span></span><br/>    | <span data-ttu-id="d7c13-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d7c13-131">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="d7c13-132">標頭</span><span class="sxs-lookup"><span data-stu-id="d7c13-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7c13-133"><dt>Rtm. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7c13-133"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7c13-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7c13-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7c13-135">路由表管理員第1版參考</span><span class="sxs-lookup"><span data-stu-id="d7c13-135">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="d7c13-136">路由表管理員第1版結構</span><span class="sxs-lookup"><span data-stu-id="d7c13-136">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="d7c13-137">**RTM \_ IPX \_ 路由**</span><span class="sxs-lookup"><span data-stu-id="d7c13-137">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 





