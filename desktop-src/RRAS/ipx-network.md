---
title: 'IPX_NETWORK 結構 (Rtm) '
description: IPX \_ 網路結構描述的是 ipx 網路位址。
ms.assetid: 83fc4022-8515-4a51-ac47-f92572447fbf
keywords:
- IPX_NETWORK 結構 RAS
- PIPX_NETWORK 結構指標 RAS
topic_type:
- apiref
api_name:
- IPX_NETWORK
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04aabf363c0152ba520bb5c8894142715b5bff56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933886"
---
# <a name="ipx_network-structure"></a><span data-ttu-id="9365d-105">IPX \_ 網路結構</span><span class="sxs-lookup"><span data-stu-id="9365d-105">IPX\_NETWORK structure</span></span>

<span data-ttu-id="9365d-106">\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。</span><span class="sxs-lookup"><span data-stu-id="9365d-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="9365d-107">應用程式應該使用路由表管理員第2版 API。\]</span><span class="sxs-lookup"><span data-stu-id="9365d-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="9365d-108">**Ipx \_ 網路** 結構描述的是 ipx 網路位址。</span><span class="sxs-lookup"><span data-stu-id="9365d-108">The **IPX\_NETWORK** structure describes an IPX network address.</span></span>

## <a name="syntax"></a><span data-ttu-id="9365d-109">語法</span><span class="sxs-lookup"><span data-stu-id="9365d-109">Syntax</span></span>


```C++
typedef struct _IPX_NETWORK {
  DWORD N_NetNumber;
} IPX_NETWORK, *PIPX_NETWORK;
```



## <a name="members"></a><span data-ttu-id="9365d-110">成員</span><span class="sxs-lookup"><span data-stu-id="9365d-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="9365d-111">**N \_ NetNumber**</span><span class="sxs-lookup"><span data-stu-id="9365d-111">**N\_NetNumber**</span></span>
</dt> <dd>

<span data-ttu-id="9365d-112">包含以電腦位元組順序排列的 IPX 網路編號。</span><span class="sxs-lookup"><span data-stu-id="9365d-112">Contains the IPX network number in machine-byte order.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9365d-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9365d-113">Requirements</span></span>



| <span data-ttu-id="9365d-114">需求</span><span class="sxs-lookup"><span data-stu-id="9365d-114">Requirement</span></span> | <span data-ttu-id="9365d-115">值</span><span class="sxs-lookup"><span data-stu-id="9365d-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9365d-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9365d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9365d-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="9365d-117">None supported</span></span><br/>                                                        |
| <span data-ttu-id="9365d-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9365d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9365d-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9365d-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9365d-120">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="9365d-120">End of server support</span></span><br/>    | <span data-ttu-id="9365d-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9365d-121">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="9365d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="9365d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9365d-123"><dt>Rtm. h</dt></span><span class="sxs-lookup"><span data-stu-id="9365d-123"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9365d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9365d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9365d-125">路由表管理員第1版參考</span><span class="sxs-lookup"><span data-stu-id="9365d-125">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="9365d-126">路由表管理員第1版結構</span><span class="sxs-lookup"><span data-stu-id="9365d-126">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="9365d-127">**RTM \_ IPX \_ 路由**</span><span class="sxs-lookup"><span data-stu-id="9365d-127">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 





