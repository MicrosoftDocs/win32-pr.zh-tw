---
title: 'RtmGetRouteAge 函式 (Rtm. h) '
description: RtmGetRouteAge 函數會傳回路由的年齡。 Age 是建立或上次更新之後的時間（以秒為單位）。
ms.assetid: 93052412-227f-4c9e-978b-3ec4bde4a256
keywords:
- RtmGetRouteAge 函式 RAS
topic_type:
- apiref
api_name:
- RtmGetRouteAge
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a484bb5684fde974ce5fa704c0d0cca38c320851
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686078"
---
# <a name="rtmgetrouteage-function"></a><span data-ttu-id="438b2-105">RtmGetRouteAge 函式</span><span class="sxs-lookup"><span data-stu-id="438b2-105">RtmGetRouteAge function</span></span>

<span data-ttu-id="438b2-106">\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。</span><span class="sxs-lookup"><span data-stu-id="438b2-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="438b2-107">應用程式應該使用路由表管理員第2版 API。\]</span><span class="sxs-lookup"><span data-stu-id="438b2-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="438b2-108">**RtmGetRouteAge** 函數會傳回路由的年齡。</span><span class="sxs-lookup"><span data-stu-id="438b2-108">The **RtmGetRouteAge** function returns the age of a route.</span></span> <span data-ttu-id="438b2-109">Age 是建立或上次更新之後的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="438b2-109">The age is the time, in seconds, since it was created or last updated.</span></span>

## <a name="syntax"></a><span data-ttu-id="438b2-110">語法</span><span class="sxs-lookup"><span data-stu-id="438b2-110">Syntax</span></span>


```C++
ULONG RtmGetRouteAge(
  _In_ PVOID Route
);
```



## <a name="parameters"></a><span data-ttu-id="438b2-111">參數</span><span class="sxs-lookup"><span data-stu-id="438b2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="438b2-112">*路由* \[在\]</span><span class="sxs-lookup"><span data-stu-id="438b2-112">*Route* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="438b2-113">通訊協定系列特定結構的指標，指定最近從路由表管理員取得的路由資料。</span><span class="sxs-lookup"><span data-stu-id="438b2-113">Pointer to a protocol-family-specific structure that specifies route data recently obtained from the routing table manager.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="438b2-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="438b2-114">Return value</span></span>

<span data-ttu-id="438b2-115">傳回值是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="438b2-115">The return value is one of the following values.</span></span>



| <span data-ttu-id="438b2-116">值</span><span class="sxs-lookup"><span data-stu-id="438b2-116">Value</span></span>                                                                                   | <span data-ttu-id="438b2-117">描述</span><span class="sxs-lookup"><span data-stu-id="438b2-117">Description</span></span>                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="438b2-118"><dt>**RouteAge**</dt></span><span class="sxs-lookup"><span data-stu-id="438b2-118"><dt>**RouteAge**</dt></span></span> </dl> | <span data-ttu-id="438b2-119">建立路由或上次更新之後的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="438b2-119">The time in seconds since a route was created or last updated.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="438b2-120"><dt>**INFINITE**</dt></span><span class="sxs-lookup"><span data-stu-id="438b2-120"><dt>**INFINITE**</dt></span></span> </dl> | <span data-ttu-id="438b2-121">路由結構的內容無效。</span><span class="sxs-lookup"><span data-stu-id="438b2-121">The content of the route structure is invalid.</span></span> <span data-ttu-id="438b2-122">在此情況下，對 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 的呼叫會傳回錯誤 \_ 無效 \_ 的參數。</span><span class="sxs-lookup"><span data-stu-id="438b2-122">In this case, a call to [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INVALID\_PARAMETER.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="438b2-123">備註</span><span class="sxs-lookup"><span data-stu-id="438b2-123">Remarks</span></span>

<span data-ttu-id="438b2-124">路由存留期是從 \_ *路由* 參數所指向之結構的 RR TimeStamp 成員計算而來。</span><span class="sxs-lookup"><span data-stu-id="438b2-124">The route age is computed from the RR\_TimeStamp member of the structure that is pointed to by the *Route* parameter.</span></span> <span data-ttu-id="438b2-125">當新增或更新路由時，路由表管理員會設定這個成員的值。</span><span class="sxs-lookup"><span data-stu-id="438b2-125">The routing table manager sets the value of this member when a route is added or updated.</span></span>

## <a name="requirements"></a><span data-ttu-id="438b2-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="438b2-126">Requirements</span></span>



| <span data-ttu-id="438b2-127">需求</span><span class="sxs-lookup"><span data-stu-id="438b2-127">Requirement</span></span> | <span data-ttu-id="438b2-128">值</span><span class="sxs-lookup"><span data-stu-id="438b2-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="438b2-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="438b2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="438b2-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="438b2-130">None supported</span></span><br/>                                                          |
| <span data-ttu-id="438b2-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="438b2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="438b2-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="438b2-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="438b2-133">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="438b2-133">End of server support</span></span><br/>    | <span data-ttu-id="438b2-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="438b2-134">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="438b2-135">標頭</span><span class="sxs-lookup"><span data-stu-id="438b2-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="438b2-136"><dt>Rtm. h</dt></span><span class="sxs-lookup"><span data-stu-id="438b2-136"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="438b2-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="438b2-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="438b2-138"><dt>Rtm .lib</dt></span><span class="sxs-lookup"><span data-stu-id="438b2-138"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="438b2-139">DLL</span><span class="sxs-lookup"><span data-stu-id="438b2-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="438b2-140"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="438b2-140"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="438b2-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="438b2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="438b2-142">路由表管理員 \_ 第1版參考</span><span class="sxs-lookup"><span data-stu-id="438b2-142">Routing Table Manager Version\_1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="438b2-143">路由表管理員第1版函數</span><span class="sxs-lookup"><span data-stu-id="438b2-143">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

<span data-ttu-id="438b2-144">[**3]。Getlasterror**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)</span><span class="sxs-lookup"><span data-stu-id="438b2-144">[**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)</span></span>
</dt> <dt>

[<span data-ttu-id="438b2-145">**RTM \_ IP \_ 路由**</span><span class="sxs-lookup"><span data-stu-id="438b2-145">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="438b2-146">**RTM \_ IPX \_ 路由**</span><span class="sxs-lookup"><span data-stu-id="438b2-146">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

