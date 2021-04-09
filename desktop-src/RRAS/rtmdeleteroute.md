---
title: 'RtmDeleteRoute 函式 (Rtm. h) '
description: RtmDeleteRoute 函式會刪除路由專案。
ms.assetid: a98026e9-40f5-42e9-943c-dfc561feef6d
keywords:
- RtmDeleteRoute 函式 RAS
topic_type:
- apiref
api_name:
- RtmDeleteRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 310364bdb6e6ba7daf285316fcaaf16884e53929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934602"
---
# <a name="rtmdeleteroute-function"></a><span data-ttu-id="1349d-104">RtmDeleteRoute 函式</span><span class="sxs-lookup"><span data-stu-id="1349d-104">RtmDeleteRoute function</span></span>

<span data-ttu-id="1349d-105">\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。</span><span class="sxs-lookup"><span data-stu-id="1349d-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="1349d-106">應用程式應該使用路由表管理員第2版 API。\]</span><span class="sxs-lookup"><span data-stu-id="1349d-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="1349d-107">**RtmDeleteRoute** 函式會刪除路由專案。</span><span class="sxs-lookup"><span data-stu-id="1349d-107">The **RtmDeleteRoute** function deletes a route entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="1349d-108">語法</span><span class="sxs-lookup"><span data-stu-id="1349d-108">Syntax</span></span>


```C++
DWORD RtmDeleteRoute(
  _In_  HANDLE ClientHandle,
  _In_  PVOID  Route,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="1349d-109">參數</span><span class="sxs-lookup"><span data-stu-id="1349d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1349d-110">*ClientHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1349d-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1349d-111">識別用戶端的控制碼，因此是已新增或更新路由的路由通訊協定。</span><span class="sxs-lookup"><span data-stu-id="1349d-111">Handle that identifies the client and therefore the routing protocol of the added or updated route.</span></span> <span data-ttu-id="1349d-112">藉由呼叫 [**RtmRegisterClient**](rtmregisterclient.md)來取得此控制碼。</span><span class="sxs-lookup"><span data-stu-id="1349d-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> <dt>

<span data-ttu-id="1349d-113">*路由* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1349d-113">*Route* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1349d-114">通訊協定系列特定結構的指標，指定新的或更新的路由。</span><span class="sxs-lookup"><span data-stu-id="1349d-114">Pointer to a protocol-family-specific structure that specifies the new or updated route.</span></span> <span data-ttu-id="1349d-115">路由表管理員會使用下欄欄位來更新路由表：</span><span class="sxs-lookup"><span data-stu-id="1349d-115">The following fields are used by the routing table manager to update the routing table:</span></span>



| <span data-ttu-id="1349d-116">值</span><span class="sxs-lookup"><span data-stu-id="1349d-116">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="1349d-117">意義</span><span class="sxs-lookup"><span data-stu-id="1349d-117">Meaning</span></span>                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <span data-ttu-id="1349d-118"><dt>**RR \_ 網路**</dt></span><span class="sxs-lookup"><span data-stu-id="1349d-118"><dt>**RR\_Network**</dt></span></span> </dl>                             | <span data-ttu-id="1349d-119">指定目的地網路編號。</span><span class="sxs-lookup"><span data-stu-id="1349d-119">Specifies the destination network number.</span></span> <br/>                                 |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <span data-ttu-id="1349d-120"><dt>**RR \_ InterfaceID**</dt></span><span class="sxs-lookup"><span data-stu-id="1349d-120"><dt>**RR\_InterfaceID**</dt></span></span> </dl>             | <span data-ttu-id="1349d-121">指定接收路由的介面索引。</span><span class="sxs-lookup"><span data-stu-id="1349d-121">Specifies the index of the interface through which the route was received.</span></span><br/> |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <span data-ttu-id="1349d-122"><dt>**RR \_ NextHopAddress**</dt></span><span class="sxs-lookup"><span data-stu-id="1349d-122"><dt>**RR\_NextHopAddress**</dt></span></span> </dl> | <span data-ttu-id="1349d-123">指定下一個躍點路由器的網路位址。</span><span class="sxs-lookup"><span data-stu-id="1349d-123">Specifies the network address of the next-hop router.</span></span><br/>                      |



 

</dd> <dt>

<span data-ttu-id="1349d-124">*旗標* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1349d-124">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1349d-125">一組旗標的指標，指出變更訊息的類型，以及在提供的緩衝區中放置哪些資訊。</span><span class="sxs-lookup"><span data-stu-id="1349d-125">Pointer to a set of flags that indicate the type of the change message, and what information was placed in the provided buffers.</span></span> <span data-ttu-id="1349d-126">此參數是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1349d-126">This parameter is one of the following values.</span></span>



| <span data-ttu-id="1349d-127">Flags</span><span class="sxs-lookup"><span data-stu-id="1349d-127">Flags</span></span>                                                                                                                                                                      | <span data-ttu-id="1349d-128">意義</span><span class="sxs-lookup"><span data-stu-id="1349d-128">Meaning</span></span>                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <span data-ttu-id="1349d-129"><dt>**RTM \_ 無 \_ 變更**</dt></span><span class="sxs-lookup"><span data-stu-id="1349d-129"><dt>**RTM\_NO\_CHANGE**</dt></span></span> </dl>             | <span data-ttu-id="1349d-130">刪除路由並不會影響到任何目的地網路的最佳路由。</span><span class="sxs-lookup"><span data-stu-id="1349d-130">Deleting the route did not affect the best route to any destination network.</span></span> <span data-ttu-id="1349d-131">換句話說，另一個專案代表相同目的地網路的路由，且具有較低的度量。</span><span class="sxs-lookup"><span data-stu-id="1349d-131">In other words, another entry represents a route to the same destination network and has a lower metric.</span></span><br/> |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <span data-ttu-id="1349d-132"><dt>**\_ \_ 已刪除 RTM 路由**</dt></span><span class="sxs-lookup"><span data-stu-id="1349d-132"><dt>**RTM\_ROUTE\_DELETED**</dt></span></span> </dl> | <span data-ttu-id="1349d-133">已刪除的路由是特定目的地網路唯一可用的路由。</span><span class="sxs-lookup"><span data-stu-id="1349d-133">The route deleted was the only route available for a particular destination network.</span></span><br/>                                                                                                  |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <span data-ttu-id="1349d-134"><dt>**RTM \_ 路由 \_ 已變更**</dt></span><span class="sxs-lookup"><span data-stu-id="1349d-134"><dt>**RTM\_ROUTE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="1349d-135">刪除此路由之後，另一個路由就會成為特定目的地網路的最佳路由。</span><span class="sxs-lookup"><span data-stu-id="1349d-135">After this route was deleted, another route became the best route to a particular destination network.</span></span> <span data-ttu-id="1349d-136">*CurBestRoute* 會指向新的最佳路由資訊。</span><span class="sxs-lookup"><span data-stu-id="1349d-136">*CurBestRoute* points to the information for the new best route.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="1349d-137">*CurBestRoute* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1349d-137">*CurBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1349d-138">結構的指標，此結構會接收目前的最佳路由資訊（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="1349d-138">Pointer to a structure that receives the current best-route information, if any.</span></span> <span data-ttu-id="1349d-139">結構的類型是通訊協定系列專用的，例如 IP 或 IPX。</span><span class="sxs-lookup"><span data-stu-id="1349d-139">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="1349d-140">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="1349d-140">This parameter is optional.</span></span> <span data-ttu-id="1349d-141">如果呼叫端為此參數指定 **Null** ，則不會傳回目前的最佳路由資訊。</span><span class="sxs-lookup"><span data-stu-id="1349d-141">If the caller specifies **NULL** for this parameter, the current best-route information is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1349d-142">傳回值</span><span class="sxs-lookup"><span data-stu-id="1349d-142">Return value</span></span>

<span data-ttu-id="1349d-143">如果函式成功，則傳回值不會是 **\_ 錯誤**。</span><span class="sxs-lookup"><span data-stu-id="1349d-143">If the function succeeds, the return value is **NO\_ERROR**.</span></span>

<span data-ttu-id="1349d-144">如果函式失敗，則傳回值是下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1349d-144">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="1349d-145">值</span><span class="sxs-lookup"><span data-stu-id="1349d-145">Value</span></span>                                                                                                       | <span data-ttu-id="1349d-146">描述</span><span class="sxs-lookup"><span data-stu-id="1349d-146">Description</span></span>                                                                                            |
|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1349d-147"><dt>**錯誤 \_ 不正確 \_ 控制碼**</dt></span><span class="sxs-lookup"><span data-stu-id="1349d-147"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="1349d-148">用戶端控制碼參數不是有效的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1349d-148">The client handle parameter is not a valid handle.</span></span><br/>                                          |
| <dl> <span data-ttu-id="1349d-149"><dt>**錯誤 \_ 不正確 \_ 參數**</dt></span><span class="sxs-lookup"><span data-stu-id="1349d-149"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="1349d-150">*Route* 參數所指向的路由結構包含成員值。</span><span class="sxs-lookup"><span data-stu-id="1349d-150">The route structure pointed to by the *Route* parameter contains a member value.</span></span><br/>            |
| <dl> <span data-ttu-id="1349d-151"><dt>**錯誤 \_ 沒有 \_ 這類 \_ 路由**</dt></span><span class="sxs-lookup"><span data-stu-id="1349d-151"><dt>**ERROR\_NO\_SUCH\_ROUTE**</dt></span></span> </dl>       | <span data-ttu-id="1349d-152">路由表中沒有任何專案符合指定路由的參數。</span><span class="sxs-lookup"><span data-stu-id="1349d-152">There are no entries in the routing table that match the parameters of the specified route.</span></span><br/> |
| <dl> <span data-ttu-id="1349d-153"><dt>**錯誤 \_ 的 \_ 系統 \_ 資源**</dt></span><span class="sxs-lookup"><span data-stu-id="1349d-153"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="1349d-154">資源不足，無法執行此作業。</span><span class="sxs-lookup"><span data-stu-id="1349d-154">There are insufficient resources to perform the operation.</span></span> <br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="1349d-155">備註</span><span class="sxs-lookup"><span data-stu-id="1349d-155">Remarks</span></span>

<span data-ttu-id="1349d-156">如果目的地網路的最佳路由變更為刪除的結果，此函式會產生路由變更訊息。</span><span class="sxs-lookup"><span data-stu-id="1349d-156">The function generates a route-change message if the best route to a destination network has changed as the result of the deletion.</span></span> <span data-ttu-id="1349d-157">但是，不會將路由變更訊息傳送給進行此呼叫的用戶端。</span><span class="sxs-lookup"><span data-stu-id="1349d-157">However, the route-change message is not sent to the client that makes this call.</span></span> <span data-ttu-id="1349d-158">相反地，此函式會將相關資訊直接傳回給該用戶端。</span><span class="sxs-lookup"><span data-stu-id="1349d-158">Instead, relevant information is returned by this function directly to that client.</span></span>

## <a name="requirements"></a><span data-ttu-id="1349d-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="1349d-159">Requirements</span></span>



| <span data-ttu-id="1349d-160">需求</span><span class="sxs-lookup"><span data-stu-id="1349d-160">Requirement</span></span> | <span data-ttu-id="1349d-161">值</span><span class="sxs-lookup"><span data-stu-id="1349d-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1349d-162">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1349d-162">Minimum supported client</span></span><br/> | <span data-ttu-id="1349d-163">都不支援</span><span class="sxs-lookup"><span data-stu-id="1349d-163">None supported</span></span><br/>                                                          |
| <span data-ttu-id="1349d-164">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1349d-164">Minimum supported server</span></span><br/> | <span data-ttu-id="1349d-165">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1349d-165">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1349d-166">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="1349d-166">End of server support</span></span><br/>    | <span data-ttu-id="1349d-167">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1349d-167">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="1349d-168">標頭</span><span class="sxs-lookup"><span data-stu-id="1349d-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="1349d-169"><dt>Rtm. h</dt></span><span class="sxs-lookup"><span data-stu-id="1349d-169"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="1349d-170">程式庫</span><span class="sxs-lookup"><span data-stu-id="1349d-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="1349d-171"><dt>Rtm .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1349d-171"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="1349d-172">DLL</span><span class="sxs-lookup"><span data-stu-id="1349d-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1349d-173"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1349d-173"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1349d-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1349d-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1349d-175">路由表管理員第1版參考</span><span class="sxs-lookup"><span data-stu-id="1349d-175">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="1349d-176">路由表管理員第1版函數</span><span class="sxs-lookup"><span data-stu-id="1349d-176">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="1349d-177">**RtmAddRoute**</span><span class="sxs-lookup"><span data-stu-id="1349d-177">**RtmAddRoute**</span></span>](rtmaddroute.md)
</dt> <dt>

[<span data-ttu-id="1349d-178">**RtmDequeueRouteChangeMessage**</span><span class="sxs-lookup"><span data-stu-id="1349d-178">**RtmDequeueRouteChangeMessage**</span></span>](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





