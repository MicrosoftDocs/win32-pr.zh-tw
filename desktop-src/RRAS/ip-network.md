---
title: 'IP_NETWORK 結構 (Rtm) '
description: IP \_ 網路結構描述 ip 網路位址。
ms.assetid: 5dcc733f-c86f-407e-8727-64f3ae71dd48
keywords:
- IP_NETWORK 結構 RAS
- PIP_NETWORK 結構指標 RAS
topic_type:
- apiref
api_name:
- IP_NETWORK
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2541c493b1b2e3805e3705c71e890c6a6aaa98ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686152"
---
# <a name="ip_network-structure"></a><span data-ttu-id="c5d70-105">IP \_ 網路結構</span><span class="sxs-lookup"><span data-stu-id="c5d70-105">IP\_NETWORK structure</span></span>

<span data-ttu-id="c5d70-106">\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。</span><span class="sxs-lookup"><span data-stu-id="c5d70-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="c5d70-107">應用程式應該使用路由表管理員第2版 API。\]</span><span class="sxs-lookup"><span data-stu-id="c5d70-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="c5d70-108">**Ip \_ 網路** 結構描述 ip 網路位址。</span><span class="sxs-lookup"><span data-stu-id="c5d70-108">The **IP\_NETWORK** structure describes an IP network address.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5d70-109">語法</span><span class="sxs-lookup"><span data-stu-id="c5d70-109">Syntax</span></span>


```C++
typedef struct _IP_NETWORK {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NETWORK, *PIP_NETWORK;
```



## <a name="members"></a><span data-ttu-id="c5d70-110">成員</span><span class="sxs-lookup"><span data-stu-id="c5d70-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="c5d70-111">**N \_ NetNumber**</span><span class="sxs-lookup"><span data-stu-id="c5d70-111">**N\_NetNumber**</span></span>
</dt> <dd>

<span data-ttu-id="c5d70-112">指定以電腦位元組順序表示的 ip 網路編號（以 IP 位址表示）。</span><span class="sxs-lookup"><span data-stu-id="c5d70-112">Specifies the IP network number expressed as an IP address in machine-byte order.</span></span>

</dd> <dt>

<span data-ttu-id="c5d70-113">**N \_ 網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="c5d70-113">**N\_NetMask**</span></span>
</dt> <dd>

<span data-ttu-id="c5d70-114">指定網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="c5d70-114">Specifies the network mask.</span></span> <span data-ttu-id="c5d70-115">將此遮罩套用至 IP 位址，以便將網路位址解壓縮。</span><span class="sxs-lookup"><span data-stu-id="c5d70-115">Apply this mask to the IP address in order to extract the network address.</span></span> <span data-ttu-id="c5d70-116">網路遮罩是以電腦位元組順序排列。</span><span class="sxs-lookup"><span data-stu-id="c5d70-116">The network mask is in machine-byte order.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5d70-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5d70-117">Requirements</span></span>



| <span data-ttu-id="c5d70-118">需求</span><span class="sxs-lookup"><span data-stu-id="c5d70-118">Requirement</span></span> | <span data-ttu-id="c5d70-119">值</span><span class="sxs-lookup"><span data-stu-id="c5d70-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c5d70-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5d70-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c5d70-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="c5d70-121">None supported</span></span><br/>                                                        |
| <span data-ttu-id="c5d70-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5d70-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c5d70-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5d70-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c5d70-124">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="c5d70-124">End of server support</span></span><br/>    | <span data-ttu-id="c5d70-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c5d70-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="c5d70-126">標頭</span><span class="sxs-lookup"><span data-stu-id="c5d70-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5d70-127"><dt>Rtm. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5d70-127"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5d70-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5d70-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5d70-129">路由表管理員第1版參考</span><span class="sxs-lookup"><span data-stu-id="c5d70-129">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="c5d70-130">路由表管理員第1版結構</span><span class="sxs-lookup"><span data-stu-id="c5d70-130">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="c5d70-131">**RTM \_ IP \_ 路由**</span><span class="sxs-lookup"><span data-stu-id="c5d70-131">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> </dl>

 

 





