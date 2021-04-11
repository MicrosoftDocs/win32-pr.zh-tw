---
title: 'RtmCreateEnumerationHandle 函式 (Rtm. h) '
description: RtmCreateEnumerationHandle 函式會傳回要搭配 RtmEnumerateGetNextRoute 使用的控制碼，以掃描路由表管理員已知的所有路由或路由的子集。
ms.assetid: 73e3ac7d-498a-4d89-a6b5-17aaf4b17ec2
keywords:
- RtmCreateEnumerationHandle 函式 RAS
topic_type:
- apiref
api_name:
- RtmCreateEnumerationHandle
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14086639db299038139e0e7d02eb12bb892042bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094064"
---
# <a name="rtmcreateenumerationhandle-function"></a><span data-ttu-id="cb261-104">RtmCreateEnumerationHandle 函式</span><span class="sxs-lookup"><span data-stu-id="cb261-104">RtmCreateEnumerationHandle function</span></span>

<span data-ttu-id="cb261-105">\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。</span><span class="sxs-lookup"><span data-stu-id="cb261-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="cb261-106">應用程式應該使用路由表管理員第2版 API。\]</span><span class="sxs-lookup"><span data-stu-id="cb261-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="cb261-107">**RtmCreateEnumerationHandle** 函式會傳回要搭配 [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md)使用的控制碼，以掃描路由表管理員已知的所有路由或路由的子集。</span><span class="sxs-lookup"><span data-stu-id="cb261-107">The **RtmCreateEnumerationHandle** function returns a handle to use with [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md) to scan through all routes, or a subset of routes, known to the routing table manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb261-108">語法</span><span class="sxs-lookup"><span data-stu-id="cb261-108">Syntax</span></span>


```C++
HANDLE RtmCreateEnumerationHandle(
  _In_ DWORD ProtocolFamily,
  _In_ DWORD EnumerationFlags,
  _In_ PVOID CriteriaRoute
);
```



## <a name="parameters"></a><span data-ttu-id="cb261-109">參數</span><span class="sxs-lookup"><span data-stu-id="cb261-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb261-110">*ProtocolFamily* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb261-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb261-111">指定要列舉之路由的通訊協定系列。</span><span class="sxs-lookup"><span data-stu-id="cb261-111">Specifies the protocol family of the routes to enumerate.</span></span>

</dd> <dt>

<span data-ttu-id="cb261-112">*EnumerationFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb261-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb261-113">指定應列舉的路由。</span><span class="sxs-lookup"><span data-stu-id="cb261-113">Specifies which routes should be enumerated.</span></span> <span data-ttu-id="cb261-114">此參數會將列舉 API 傳回的路由集合，限制為下列旗標所定義的子集，以及 *CriteriaRoute* 參數所指向之結構的對應成員中的值。</span><span class="sxs-lookup"><span data-stu-id="cb261-114">This parameter limits the set of routes returned by the enumeration API to a subset defined by the following flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="cb261-115">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="cb261-115">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="cb261-116">EnumerationFlags</span><span class="sxs-lookup"><span data-stu-id="cb261-116">EnumerationFlags</span></span>                                                                                                                                                                              | <span data-ttu-id="cb261-117">意義</span><span class="sxs-lookup"><span data-stu-id="cb261-117">Meaning</span></span>                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ONLY_THIS_NETWORK"></span><span id="rtm_only_this_network"></span><dl> <span data-ttu-id="cb261-118"><dt>**\_僅 RTM \_ 此 \_ 網路**</dt></span><span class="sxs-lookup"><span data-stu-id="cb261-118"><dt>**RTM\_ONLY\_THIS\_NETWORK**</dt></span></span> </dl>       | <span data-ttu-id="cb261-119">只列舉與 \_ CriteriaRoute 所指向之結構的 RR 網路成員具有相同網路編號的路由。</span><span class="sxs-lookup"><span data-stu-id="cb261-119">Enumerate only those routes that have the same network number as the RR\_Network member of the structure pointed to by CriteriaRoute.</span></span><br/>                        |
| <span id="RTM_ONLY_THIS_INTERFACE"></span><span id="rtm_only_this_interface"></span><dl> <span data-ttu-id="cb261-120"><dt>**\_僅 RTM \_ 此 \_ 介面**</dt></span><span class="sxs-lookup"><span data-stu-id="cb261-120"><dt>**RTM\_ONLY\_THIS\_INTERFACE**</dt></span></span> </dl> | <span data-ttu-id="cb261-121">只列舉透過 \_ CriteriaRoute 所指向之結構的 RR InterfaceID 欄位所指定的介面所取得的路由。</span><span class="sxs-lookup"><span data-stu-id="cb261-121">Enumerate only those routes that were obtained through the interface specified by the RR\_InterfaceID field of the structure pointed to by CriteriaRoute.</span></span><br/>    |
| <span id="RTM_ONLY_THIS_PROTOCOL"></span><span id="rtm_only_this_protocol"></span><dl> <span data-ttu-id="cb261-122"><dt>**\_僅 RTM \_ 此 \_ 通訊協定**</dt></span><span class="sxs-lookup"><span data-stu-id="cb261-122"><dt>**RTM\_ONLY\_THIS\_PROTOCOL**</dt></span></span> </dl>    | <span data-ttu-id="cb261-123">只列舉由 \_ CriteriaRoute 所指向之結構的 RR RoutingProtocol 欄位所指定的路由通訊協定所加入的路由。</span><span class="sxs-lookup"><span data-stu-id="cb261-123">Enumerate only those routes that were added by the routing protocol specified by the RR\_RoutingProtocol field of the structure pointed to by CriteriaRoute.</span></span><br/> |
| <span id="RTM_ONLY_BEST_ROUTES"></span><span id="rtm_only_best_routes"></span><dl> <span data-ttu-id="cb261-124"><dt>**\_僅 RTM \_ 最適合的 \_ 路由**</dt></span><span class="sxs-lookup"><span data-stu-id="cb261-124"><dt>**RTM\_ONLY\_BEST\_ROUTES**</dt></span></span> </dl>          | <span data-ttu-id="cb261-125">只列舉集合中每個網路的最佳路由。</span><span class="sxs-lookup"><span data-stu-id="cb261-125">Enumerate only the best routes to each of the networks in the set.</span></span><br/>                                                                                           |



 

</dd> <dt>

<span data-ttu-id="cb261-126">*CriteriaRoute* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb261-126">*CriteriaRoute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb261-127">通訊協定系列特定路由結構的指標， ([**rtm \_ IP \_ 路由**](rtm-ip-route.md) 或 [**rtm \_ IPX \_ 路由**](rtm-ipx-route.md)) 。</span><span class="sxs-lookup"><span data-stu-id="cb261-127">Pointer to a protocol-family-specific route structure ([**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span> <span data-ttu-id="cb261-128">此結構中的成員值會對應至 *EnumerationFlags* 參數所指定的旗標。</span><span class="sxs-lookup"><span data-stu-id="cb261-128">The member values in this structure correspond to the flags specified by the *EnumerationFlags* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb261-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="cb261-129">Return value</span></span>

<span data-ttu-id="cb261-130">如果函式成功，則傳回值會是用於後續列舉呼叫的 **控制碼** 。</span><span class="sxs-lookup"><span data-stu-id="cb261-130">If the function succeeds, the return value is a **HANDLE** to use with subsequent enumeration calls.</span></span>

<span data-ttu-id="cb261-131">如果函式失敗，或沒有具有指定準則的路由存在，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="cb261-131">If the function fails, or no routes exist with the specified criteria, the return value is **NULL**.</span></span> <span data-ttu-id="cb261-132">呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 以取得詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="cb261-132">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain more information.</span></span>



| <span data-ttu-id="cb261-133">值</span><span class="sxs-lookup"><span data-stu-id="cb261-133">Value</span></span>                                                                                                       | <span data-ttu-id="cb261-134">描述</span><span class="sxs-lookup"><span data-stu-id="cb261-134">Description</span></span>                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cb261-135"><dt>**錯誤 \_ 沒有 \_ 路由**</dt></span><span class="sxs-lookup"><span data-stu-id="cb261-135"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="cb261-136">沒有具有指定準則的路由。</span><span class="sxs-lookup"><span data-stu-id="cb261-136">There are no routes that have the specified criteria.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="cb261-137"><dt>**錯誤 \_ 不正確 \_ 參數**</dt></span><span class="sxs-lookup"><span data-stu-id="cb261-137"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="cb261-138">一或多個輸入參數無效 (例如，未知的通訊協定系列、不正確列舉旗標) 。</span><span class="sxs-lookup"><span data-stu-id="cb261-138">One or more of the input parameters is invalid (for example, unknown protocol family, invalid enumeration flags).</span></span><br/> |
| <dl> <span data-ttu-id="cb261-139"><dt>**錯誤 \_ 的 \_ 系統 \_ 資源**</dt></span><span class="sxs-lookup"><span data-stu-id="cb261-139"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="cb261-140">資源不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="cb261-140">There are insufficient resources to carry out the operation.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="cb261-141"><dt>**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</dt></span><span class="sxs-lookup"><span data-stu-id="cb261-141"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="cb261-142">記憶體不足，無法配置此控制碼。</span><span class="sxs-lookup"><span data-stu-id="cb261-142">There is insufficient memory to allocate the handle.</span></span><br/>                                                              |



 

## <a name="requirements"></a><span data-ttu-id="cb261-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb261-143">Requirements</span></span>



| <span data-ttu-id="cb261-144">需求</span><span class="sxs-lookup"><span data-stu-id="cb261-144">Requirement</span></span> | <span data-ttu-id="cb261-145">值</span><span class="sxs-lookup"><span data-stu-id="cb261-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cb261-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb261-146">Minimum supported client</span></span><br/> | <span data-ttu-id="cb261-147">都不支援</span><span class="sxs-lookup"><span data-stu-id="cb261-147">None supported</span></span><br/>                                                          |
| <span data-ttu-id="cb261-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb261-148">Minimum supported server</span></span><br/> | <span data-ttu-id="cb261-149">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb261-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cb261-150">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="cb261-150">End of server support</span></span><br/>    | <span data-ttu-id="cb261-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cb261-151">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="cb261-152">標頭</span><span class="sxs-lookup"><span data-stu-id="cb261-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb261-153"><dt>Rtm. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb261-153"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="cb261-154">程式庫</span><span class="sxs-lookup"><span data-stu-id="cb261-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="cb261-155"><dt>Rtm .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb261-155"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="cb261-156">DLL</span><span class="sxs-lookup"><span data-stu-id="cb261-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb261-157"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb261-157"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb261-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb261-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb261-159">路由表管理員第1版參考</span><span class="sxs-lookup"><span data-stu-id="cb261-159">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="cb261-160">路由表管理員第1版函數</span><span class="sxs-lookup"><span data-stu-id="cb261-160">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

<span data-ttu-id="cb261-161">[**3]。Getlasterror**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)</span><span class="sxs-lookup"><span data-stu-id="cb261-161">[**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)</span></span>
</dt> <dt>

[<span data-ttu-id="cb261-162">**RTM \_ IP \_ 路由**</span><span class="sxs-lookup"><span data-stu-id="cb261-162">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="cb261-163">**RTM \_ IPX \_ 路由**</span><span class="sxs-lookup"><span data-stu-id="cb261-163">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> <dt>

[<span data-ttu-id="cb261-164">**RtmCloseEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="cb261-164">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="cb261-165">**RtmEnumerateGetNextRoute**</span><span class="sxs-lookup"><span data-stu-id="cb261-165">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> </dl>

 

