---
title: 'IP_NEXT_HOP_ADDRESS 結構 (Rtm) '
description: IP \_ 下一個 \_ 躍點 \_ 位址結構包含 ip 路由之下一個躍點路由器的位址。
ms.assetid: a97b3995-dfaa-4e53-be86-3ad46b8be691
keywords:
- IP_NEXT_HOP_ADDRESS 結構 RAS
- PIP_NEXT_HOP_ADDRESS 結構 RAS
topic_type:
- apiref
api_name:
- IP_NEXT_HOP_ADDRESS
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1818a49e7977dbb4dfa31ebac1dae7651adb8d45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965316"
---
# <a name="ip_next_hop_address-structure"></a><span data-ttu-id="dc7ea-105">IP \_ 下一個 \_ 躍點 \_ 位址結構</span><span class="sxs-lookup"><span data-stu-id="dc7ea-105">IP\_NEXT\_HOP\_ADDRESS structure</span></span>

<span data-ttu-id="dc7ea-106">\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。</span><span class="sxs-lookup"><span data-stu-id="dc7ea-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="dc7ea-107">應用程式應該使用路由表管理員第2版 API。\]</span><span class="sxs-lookup"><span data-stu-id="dc7ea-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="dc7ea-108">**Ip \_ 下一個 \_ 躍點 \_ 位址** 結構包含 ip 路由之下一個躍點路由器的位址。</span><span class="sxs-lookup"><span data-stu-id="dc7ea-108">The **IP\_NEXT\_HOP\_ADDRESS** structure contains the address for the next-hop router for an IP route.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc7ea-109">語法</span><span class="sxs-lookup"><span data-stu-id="dc7ea-109">Syntax</span></span>


```C++
typedef struct _IP_NEXT_HOP_ADDRESS {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NEXT_HOP_ADDRESS, *PIP_NEXT_HOP_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="dc7ea-110">成員</span><span class="sxs-lookup"><span data-stu-id="dc7ea-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="dc7ea-111">**N \_ NetNumber**</span><span class="sxs-lookup"><span data-stu-id="dc7ea-111">**N\_NetNumber**</span></span>
</dt> <dd>

<span data-ttu-id="dc7ea-112">以電腦位元組順序指定以 IP 位址表示的 IP 網路位址。</span><span class="sxs-lookup"><span data-stu-id="dc7ea-112">Specifies the IP network address expressed as an IP address in machine-byte order.</span></span>

</dd> <dt>

<span data-ttu-id="dc7ea-113">**N \_ 網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="dc7ea-113">**N\_NetMask**</span></span>
</dt> <dd>

<span data-ttu-id="dc7ea-114">指定網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="dc7ea-114">Specifies the network mask.</span></span> <span data-ttu-id="dc7ea-115">將此遮罩套用至 IP 位址，以便將網路位址解壓縮。</span><span class="sxs-lookup"><span data-stu-id="dc7ea-115">Apply this mask to the IP address in order to extract the network address.</span></span> <span data-ttu-id="dc7ea-116">網路遮罩是以電腦位元組順序排列。</span><span class="sxs-lookup"><span data-stu-id="dc7ea-116">The network mask is in machine-byte order.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc7ea-117">備註</span><span class="sxs-lookup"><span data-stu-id="dc7ea-117">Remarks</span></span>

<span data-ttu-id="dc7ea-118">**Ip \_ 下一個 \_ 躍點 \_ 位址** 結構是 [**ip \_ 網路**](ip-network.md)結構的 typedef。</span><span class="sxs-lookup"><span data-stu-id="dc7ea-118">The **IP\_NEXT\_HOP\_ADDRESS** structure is a typedef of the [**IP\_NETWORK**](ip-network.md) structure.</span></span> <span data-ttu-id="dc7ea-119">Typedef 位於 Rtm. h 中。</span><span class="sxs-lookup"><span data-stu-id="dc7ea-119">The typedef is in Rtm.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc7ea-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc7ea-120">Requirements</span></span>



| <span data-ttu-id="dc7ea-121">需求</span><span class="sxs-lookup"><span data-stu-id="dc7ea-121">Requirement</span></span> | <span data-ttu-id="dc7ea-122">值</span><span class="sxs-lookup"><span data-stu-id="dc7ea-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="dc7ea-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc7ea-123">Minimum supported client</span></span><br/> | <span data-ttu-id="dc7ea-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="dc7ea-124">None supported</span></span><br/>                                                        |
| <span data-ttu-id="dc7ea-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc7ea-125">Minimum supported server</span></span><br/> | <span data-ttu-id="dc7ea-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc7ea-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="dc7ea-127">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="dc7ea-127">End of server support</span></span><br/>    | <span data-ttu-id="dc7ea-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dc7ea-128">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="dc7ea-129">標頭</span><span class="sxs-lookup"><span data-stu-id="dc7ea-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc7ea-130"><dt>Rtm. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc7ea-130"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc7ea-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc7ea-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc7ea-132">路由表管理員第1版參考</span><span class="sxs-lookup"><span data-stu-id="dc7ea-132">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="dc7ea-133">路由表管理員第1版結構</span><span class="sxs-lookup"><span data-stu-id="dc7ea-133">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="dc7ea-134">**IP \_ 網路**</span><span class="sxs-lookup"><span data-stu-id="dc7ea-134">**IP\_NETWORK**</span></span>](ip-network.md)
</dt> <dt>

[<span data-ttu-id="dc7ea-135">**RTM \_ IP \_ 路由**</span><span class="sxs-lookup"><span data-stu-id="dc7ea-135">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> </dl>

 

 





