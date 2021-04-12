---
title: 'IPX_NEXT_HOP_ADDRESS 結構 (Rtm) '
description: IPX \_ 下一個 \_ 躍點 \_ 位址結構包含 ipx 路由的下個躍點路由器的位址。
ms.assetid: 079e3284-6238-4bcf-a17f-68ff86775f18
keywords:
- IPX_NEXT_HOP_ADDRESS 結構 RAS
- PIPX_NEXT_HOP_ADDRESS 結構指標 RAS
topic_type:
- apiref
api_name:
- IPX_NEXT_HOP_ADDRESS
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c3eb135f1d87050cd190fe47d0088fd1ab86f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464201"
---
# <a name="ipx_next_hop_address-structure"></a><span data-ttu-id="61745-105">IPX \_ 下一個 \_ 躍點 \_ 位址結構</span><span class="sxs-lookup"><span data-stu-id="61745-105">IPX\_NEXT\_HOP\_ADDRESS structure</span></span>

<span data-ttu-id="61745-106">\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。</span><span class="sxs-lookup"><span data-stu-id="61745-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="61745-107">應用程式應該使用路由表管理員第2版 API。\]</span><span class="sxs-lookup"><span data-stu-id="61745-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="61745-108">**Ipx \_ 下一個 \_ 躍點 \_ 位址** 結構包含 ipx 路由的下個躍點路由器的位址。</span><span class="sxs-lookup"><span data-stu-id="61745-108">The **IPX\_NEXT\_HOP\_ADDRESS** structure contains the address for the next-hop router for an IPX route.</span></span>

## <a name="syntax"></a><span data-ttu-id="61745-109">語法</span><span class="sxs-lookup"><span data-stu-id="61745-109">Syntax</span></span>


```C++
typedef struct _IPX_NEXT_HOP_ADDRESS {
  BYTE NHA_Mac[6];
} IPX_NEXT_HOP_ADDRESS, *PIPX_NEXT_HOP_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="61745-110">成員</span><span class="sxs-lookup"><span data-stu-id="61745-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="61745-111">**NHA \_ Mac**</span><span class="sxs-lookup"><span data-stu-id="61745-111">**NHA\_Mac**</span></span>
</dt> <dd>

<span data-ttu-id="61745-112">指定下一個躍點路由器的 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="61745-112">Specifies the MAC address of next-hop router.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61745-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="61745-113">Requirements</span></span>



| <span data-ttu-id="61745-114">需求</span><span class="sxs-lookup"><span data-stu-id="61745-114">Requirement</span></span> | <span data-ttu-id="61745-115">值</span><span class="sxs-lookup"><span data-stu-id="61745-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="61745-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61745-116">Minimum supported client</span></span><br/> | <span data-ttu-id="61745-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="61745-117">None supported</span></span><br/>                                                        |
| <span data-ttu-id="61745-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61745-118">Minimum supported server</span></span><br/> | <span data-ttu-id="61745-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61745-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="61745-120">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="61745-120">End of server support</span></span><br/>    | <span data-ttu-id="61745-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="61745-121">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="61745-122">標頭</span><span class="sxs-lookup"><span data-stu-id="61745-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="61745-123"><dt>Rtm. h</dt></span><span class="sxs-lookup"><span data-stu-id="61745-123"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61745-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61745-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61745-125">路由表管理員第1版參考</span><span class="sxs-lookup"><span data-stu-id="61745-125">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="61745-126">路由表管理員第1版結構</span><span class="sxs-lookup"><span data-stu-id="61745-126">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="61745-127">**RTM \_ IPX \_ 路由**</span><span class="sxs-lookup"><span data-stu-id="61745-127">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 





