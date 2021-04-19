---
title: 'RtmAddRoute 函式 (Rtm. h) '
description: RtmAddRoute 函式會新增路由專案，或更新現有的路由專案。
ms.assetid: 09a9b57d-f10b-40b7-a3c1-2e0613f29431
keywords:
- RtmAddRoute 函式 RAS
topic_type:
- apiref
api_name:
- RtmAddRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c3ee68c9b026fc37457819777e69d2be7984e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965310"
---
# <a name="rtmaddroute-function"></a><span data-ttu-id="361f8-104">RtmAddRoute 函式</span><span class="sxs-lookup"><span data-stu-id="361f8-104">RtmAddRoute function</span></span>

<span data-ttu-id="361f8-105">\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。</span><span class="sxs-lookup"><span data-stu-id="361f8-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="361f8-106">應用程式應該使用路由表管理員第2版 API。\]</span><span class="sxs-lookup"><span data-stu-id="361f8-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="361f8-107">**RtmAddRoute** 函式會新增路由專案，或更新現有的路由專案。</span><span class="sxs-lookup"><span data-stu-id="361f8-107">The **RtmAddRoute** function adds a route entry or updates an existing route entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="361f8-108">語法</span><span class="sxs-lookup"><span data-stu-id="361f8-108">Syntax</span></span>


```C++
DWORD RtmAddRoute(
  _In_  HANDLE ClientHandle,
  _In_  PVOID  Route,
  _In_  DWORD  TimeToLive,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute,
  _Out_ PVOID  PrevBestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="361f8-109">參數</span><span class="sxs-lookup"><span data-stu-id="361f8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="361f8-110">*ClientHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="361f8-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="361f8-111">識別用戶端的控制碼，以及新增或更新路由的路由通訊協定。</span><span class="sxs-lookup"><span data-stu-id="361f8-111">Handle that identifies the client, and therefore the routing protocol, that added or updated the route.</span></span> <span data-ttu-id="361f8-112">藉由呼叫 [**RtmRegisterClient**](rtmregisterclient.md)來取得此控制碼。</span><span class="sxs-lookup"><span data-stu-id="361f8-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> <dt>

<span data-ttu-id="361f8-113">*路由* \[在\]</span><span class="sxs-lookup"><span data-stu-id="361f8-113">*Route* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="361f8-114">通訊協定系列特定結構的指標，指定新的或更新的路由。</span><span class="sxs-lookup"><span data-stu-id="361f8-114">Pointer to a protocol-family-specific structure that specifies the new or updated route.</span></span> <span data-ttu-id="361f8-115">路由表管理員會使用下欄欄位來更新路由表：</span><span class="sxs-lookup"><span data-stu-id="361f8-115">The following fields are used by the routing table manager to update the routing table:</span></span>



| <span data-ttu-id="361f8-116">值</span><span class="sxs-lookup"><span data-stu-id="361f8-116">Value</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="361f8-117">意義</span><span class="sxs-lookup"><span data-stu-id="361f8-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <span data-ttu-id="361f8-118"><dt>**RR \_ 網路**</dt></span><span class="sxs-lookup"><span data-stu-id="361f8-118"><dt>**RR\_Network**</dt></span></span> </dl>                                                     | <span data-ttu-id="361f8-119">指定目的地網路編號。</span><span class="sxs-lookup"><span data-stu-id="361f8-119">Specifies the destination network number.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <span data-ttu-id="361f8-120"><dt>**RR \_ InterfaceID**</dt></span><span class="sxs-lookup"><span data-stu-id="361f8-120"><dt>**RR\_InterfaceID**</dt></span></span> </dl>                                     | <span data-ttu-id="361f8-121">指定接收路由的介面索引。</span><span class="sxs-lookup"><span data-stu-id="361f8-121">Specifies the index of the interface through which the route was received.</span></span><br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <span data-ttu-id="361f8-122"><dt>**RR \_ NextHopAddress**</dt></span><span class="sxs-lookup"><span data-stu-id="361f8-122"><dt>**RR\_NextHopAddress**</dt></span></span> </dl>                         | <span data-ttu-id="361f8-123">指定下一個躍點路由器的位址。</span><span class="sxs-lookup"><span data-stu-id="361f8-123">Specifies the address of the next-hop router.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                  |
| <span id="RR_FamilySpecificData"></span><span id="rr_familyspecificdata"></span><span id="RR_FAMILYSPECIFICDATA"></span><dl> <span data-ttu-id="361f8-124"><dt>**RR \_ FamilySpecificData**</dt></span><span class="sxs-lookup"><span data-stu-id="361f8-124"><dt>**RR\_FamilySpecificData**</dt></span></span> </dl>         | <span data-ttu-id="361f8-125">指定通訊協定系列的特定資料。</span><span class="sxs-lookup"><span data-stu-id="361f8-125">Specifies data that is specific to the protocol family.</span></span> <span data-ttu-id="361f8-126">雖然資料對路由表管理員而言是透明的，但在比較路由以判斷路由資訊是否已變更時，會考慮這一點。</span><span class="sxs-lookup"><span data-stu-id="361f8-126">Although the data is transparent to the routing table manager, it is considered when comparing routes to determine if route information has changed.</span></span> <span data-ttu-id="361f8-127">資料也會用來設定與路由通訊協定無關的度量值。</span><span class="sxs-lookup"><span data-stu-id="361f8-127">The data is also used to set metric values that are independent of the routing protocol.</span></span> <span data-ttu-id="361f8-128">因此，此資料會用來決定目的地網路的最佳路由。</span><span class="sxs-lookup"><span data-stu-id="361f8-128">Consequently, this data is used to determine the best route for the destination network.</span></span><br/> |
| <span id="RR_ProtocolSpecificData"></span><span id="rr_protocolspecificdata"></span><span id="RR_PROTOCOLSPECIFICDATA"></span><dl> <span data-ttu-id="361f8-129"><dt>**RR \_ ProtocolSpecificData**</dt></span><span class="sxs-lookup"><span data-stu-id="361f8-129"><dt>**RR\_ProtocolSpecificData**</dt></span></span> </dl> | <span data-ttu-id="361f8-130">指定提供路由的路由通訊協定專用的資料。</span><span class="sxs-lookup"><span data-stu-id="361f8-130">Specifies data which is specific to the routing protocol that supplied the route.</span></span><br/>                                                                                                                                                                                                                                                                                                              |
| <span id="RR_TimeStamp"></span><span id="rr_timestamp"></span><span id="RR_TIMESTAMP"></span><dl> <span data-ttu-id="361f8-131"><dt>**RR \_ 時間戳記**</dt></span><span class="sxs-lookup"><span data-stu-id="361f8-131"><dt>**RR\_TimeStamp**</dt></span></span> </dl>                                             | <span data-ttu-id="361f8-132">指定目前的系統時間。</span><span class="sxs-lookup"><span data-stu-id="361f8-132">Specifies the current system time.</span></span> <span data-ttu-id="361f8-133">此欄位是由路由表管理員所設定。</span><span class="sxs-lookup"><span data-stu-id="361f8-133">This field is set by the routing table manager.</span></span><br/>                                                                                                                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="361f8-134">*TimeToLive* \[在\]</span><span class="sxs-lookup"><span data-stu-id="361f8-134">*TimeToLive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="361f8-135">指定指定路由應保留在路由表中的秒數。</span><span class="sxs-lookup"><span data-stu-id="361f8-135">Specifies the number of seconds the specified route should be kept in the routing table.</span></span> <span data-ttu-id="361f8-136">如果這個參數設為無限，路由會一直保留到明確刪除為止。</span><span class="sxs-lookup"><span data-stu-id="361f8-136">If this parameter is set to INFINITE, the route is kept until it is explicitly deleted.</span></span> <span data-ttu-id="361f8-137">目前的 *TimeToLive* 限制為2147483秒 (24 + 天) 。</span><span class="sxs-lookup"><span data-stu-id="361f8-137">The current limit for *TimeToLive* is 2147483 sec (24+ days).</span></span>

</dd> <dt>

<span data-ttu-id="361f8-138">*旗標* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="361f8-138">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="361f8-139">**DWORD** 變數的指標。</span><span class="sxs-lookup"><span data-stu-id="361f8-139">Pointer to a **DWORD** variable.</span></span> <span data-ttu-id="361f8-140">此變數的值是由路由表管理員所設定。</span><span class="sxs-lookup"><span data-stu-id="361f8-140">The value of this variable is set by the routing table manager.</span></span> <span data-ttu-id="361f8-141">值指出變更的類型，以及在提供的緩衝區中傳回的資訊。</span><span class="sxs-lookup"><span data-stu-id="361f8-141">The value indicates the type of the change, and what information was returned in the provided buffers.</span></span> <span data-ttu-id="361f8-142">此參數是下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="361f8-142">This parameter is one of the following.</span></span>



| <span data-ttu-id="361f8-143">Flags</span><span class="sxs-lookup"><span data-stu-id="361f8-143">Flags</span></span>                                                                                                                                                                      | <span data-ttu-id="361f8-144">意義</span><span class="sxs-lookup"><span data-stu-id="361f8-144">Meaning</span></span>                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <span data-ttu-id="361f8-145"><dt>**RTM \_ 無 \_ 變更**</dt></span><span class="sxs-lookup"><span data-stu-id="361f8-145"><dt>**RTM\_NO\_CHANGE**</dt></span></span> </dl>             | <span data-ttu-id="361f8-146">新增或更新可能不會變更任何重要的路由參數，或受影響的路由專案不是目的地網路專案之間的最佳路由。</span><span class="sxs-lookup"><span data-stu-id="361f8-146">The addition or update either did not change any of the significant route parameters, or the route entry affected is not the best route among the entries for the destination network.</span></span><br/>                                                                                                          |
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <span data-ttu-id="361f8-147"><dt>**\_ \_ 已新增 RTM 路由**</dt></span><span class="sxs-lookup"><span data-stu-id="361f8-147"><dt>**RTM\_ROUTE\_ADDED**</dt></span></span> </dl>       | <span data-ttu-id="361f8-148">已為目的地網路新增路由。</span><span class="sxs-lookup"><span data-stu-id="361f8-148">The route was added for the destination network.</span></span> <span data-ttu-id="361f8-149">*CurBestRoute* 參數會指向新增路由的資訊。</span><span class="sxs-lookup"><span data-stu-id="361f8-149">The *CurBestRoute* parameter points to the information for the added route.</span></span><br/>                                                                                                                                                                    |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <span data-ttu-id="361f8-150"><dt>**RTM \_ 路由 \_ 已變更**</dt></span><span class="sxs-lookup"><span data-stu-id="361f8-150"><dt>**RTM\_ROUTE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="361f8-151">至少有一個重要參數變更為目的地網路的最佳路由。</span><span class="sxs-lookup"><span data-stu-id="361f8-151">At least one of the significant parameters was changed for the best route to the destination network.</span></span> <span data-ttu-id="361f8-152">重要的參數包括：</span><span class="sxs-lookup"><span data-stu-id="361f8-152">The significant parameters are:</span></span> <br/> <span data-ttu-id="361f8-153">通訊協定識別碼</span><span class="sxs-lookup"><span data-stu-id="361f8-153">Protocol identifier</span></span><br/> <span data-ttu-id="361f8-154">介面索引</span><span class="sxs-lookup"><span data-stu-id="361f8-154">Interface index</span></span><br/> <span data-ttu-id="361f8-155">下個躍點位址</span><span class="sxs-lookup"><span data-stu-id="361f8-155">Next-hop address</span></span><br/> <span data-ttu-id="361f8-156">通訊協定系列特定的資料 (包括路由計量) </span><span class="sxs-lookup"><span data-stu-id="361f8-156">Protocol-family-specific data (including route metrics)</span></span><br/> |



 

<span data-ttu-id="361f8-157">*PrevBestRoute* 參數會指向變更之前的路由資訊。</span><span class="sxs-lookup"><span data-stu-id="361f8-157">The *PrevBestRoute* parameter points to the route information as it was before the change.</span></span> <span data-ttu-id="361f8-158">*CurBestRoute* 參數指向目前的 (，也就是變更後) 路由資訊。</span><span class="sxs-lookup"><span data-stu-id="361f8-158">The *CurBestRoute* parameter points to the current (that is, after-change) route information.</span></span>

</dd> <dt>

<span data-ttu-id="361f8-159">*CurBestRoute* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="361f8-159">*CurBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="361f8-160">結構的指標，此結構會接收目前的最佳路由資訊（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="361f8-160">Pointer to a structure that receives the current best-route information, if any.</span></span> <span data-ttu-id="361f8-161">結構的類型是通訊協定系列專用的，例如 IP 或 IPX。</span><span class="sxs-lookup"><span data-stu-id="361f8-161">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="361f8-162">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="361f8-162">This parameter is optional.</span></span> <span data-ttu-id="361f8-163">如果呼叫端為此參數指定 **Null** ，則不會傳回目前的最佳路由資訊。</span><span class="sxs-lookup"><span data-stu-id="361f8-163">If the caller specifies **NULL** for this parameter, the current best-route information is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="361f8-164">*PrevBestRoute* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="361f8-164">*PrevBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="361f8-165">結構的指標，此結構會接收先前的最佳路由資訊（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="361f8-165">Pointer to a structure that receives the previous best-route information, if any.</span></span> <span data-ttu-id="361f8-166">結構的類型是通訊協定系列專用的，例如 IP 或 IPX。</span><span class="sxs-lookup"><span data-stu-id="361f8-166">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="361f8-167">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="361f8-167">This parameter is optional.</span></span> <span data-ttu-id="361f8-168">如果呼叫端為此參數指定 **Null** ，則不會傳回先前的最佳路由資訊。</span><span class="sxs-lookup"><span data-stu-id="361f8-168">If the caller specifies **NULL** for this parameter the previous best-route information is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="361f8-169">傳回值</span><span class="sxs-lookup"><span data-stu-id="361f8-169">Return value</span></span>

<span data-ttu-id="361f8-170">傳回值是下列其中一個程式碼。</span><span class="sxs-lookup"><span data-stu-id="361f8-170">The return value is one of the following codes.</span></span>



| <span data-ttu-id="361f8-171">值</span><span class="sxs-lookup"><span data-stu-id="361f8-171">Value</span></span>                                                                                                       | <span data-ttu-id="361f8-172">描述</span><span class="sxs-lookup"><span data-stu-id="361f8-172">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="361f8-173"><dt>**沒有 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="361f8-173"><dt>**NO\_ERROR**</dt></span></span> </dl>                    | <span data-ttu-id="361f8-174">已成功新增或更新路由。</span><span class="sxs-lookup"><span data-stu-id="361f8-174">The route was added or updated successfully.</span></span><br/>                 |
| <dl> <span data-ttu-id="361f8-175"><dt>**錯誤 \_ 不正確 \_ 控制碼**</dt></span><span class="sxs-lookup"><span data-stu-id="361f8-175"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="361f8-176">用戶端控制碼參數不是有效的控制碼。</span><span class="sxs-lookup"><span data-stu-id="361f8-176">The client handle parameter is not a valid handle.</span></span><br/>           |
| <dl> <span data-ttu-id="361f8-177"><dt>**錯誤 \_ 不正確 \_ 參數**</dt></span><span class="sxs-lookup"><span data-stu-id="361f8-177"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="361f8-178">路由結構包含不正確參數。</span><span class="sxs-lookup"><span data-stu-id="361f8-178">The route structure contains an invalid parameter.</span></span><br/>           |
| <dl> <span data-ttu-id="361f8-179"><dt>**錯誤 \_ 的 \_ 系統 \_ 資源**</dt></span><span class="sxs-lookup"><span data-stu-id="361f8-179"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="361f8-180">資源不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="361f8-180">There are insufficient resources to carry out the operation.</span></span><br/> |
| <dl> <span data-ttu-id="361f8-181"><dt>**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</dt></span><span class="sxs-lookup"><span data-stu-id="361f8-181"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="361f8-182">記憶體不足，無法配置路由專案。</span><span class="sxs-lookup"><span data-stu-id="361f8-182">There is insufficient memory to allocate the route entry.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="361f8-183">備註</span><span class="sxs-lookup"><span data-stu-id="361f8-183">Remarks</span></span>

<span data-ttu-id="361f8-184">如果目的地網路的最佳路由因為這項作業的結果而變更，此函式會產生路由變更訊息。</span><span class="sxs-lookup"><span data-stu-id="361f8-184">The function generates a route-change message if the best route to a destination network has changed as the result of this operation.</span></span> <span data-ttu-id="361f8-185">但是，不會將路由變更訊息傳送給進行此呼叫的用戶端。</span><span class="sxs-lookup"><span data-stu-id="361f8-185">However, the route-change message is not sent to the client that makes this call.</span></span> <span data-ttu-id="361f8-186">相反地，此函式會透過 *Flags*、 *CurBestRoute* 和 *PrevBestRoute* 參數，將相關資訊直接傳回給該用戶端。</span><span class="sxs-lookup"><span data-stu-id="361f8-186">Instead, relevant information is returned by this function directly to that client through the *Flags*, *CurBestRoute*, and *PrevBestRoute* parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="361f8-187">規格需求</span><span class="sxs-lookup"><span data-stu-id="361f8-187">Requirements</span></span>



| <span data-ttu-id="361f8-188">需求</span><span class="sxs-lookup"><span data-stu-id="361f8-188">Requirement</span></span> | <span data-ttu-id="361f8-189">值</span><span class="sxs-lookup"><span data-stu-id="361f8-189">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="361f8-190">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="361f8-190">Minimum supported client</span></span><br/> | <span data-ttu-id="361f8-191">都不支援</span><span class="sxs-lookup"><span data-stu-id="361f8-191">None supported</span></span><br/>                                                          |
| <span data-ttu-id="361f8-192">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="361f8-192">Minimum supported server</span></span><br/> | <span data-ttu-id="361f8-193">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="361f8-193">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="361f8-194">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="361f8-194">End of server support</span></span><br/>    | <span data-ttu-id="361f8-195">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="361f8-195">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="361f8-196">標頭</span><span class="sxs-lookup"><span data-stu-id="361f8-196">Header</span></span><br/>                   | <dl> <span data-ttu-id="361f8-197"><dt>Rtm. h</dt></span><span class="sxs-lookup"><span data-stu-id="361f8-197"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="361f8-198">程式庫</span><span class="sxs-lookup"><span data-stu-id="361f8-198">Library</span></span><br/>                  | <dl> <span data-ttu-id="361f8-199"><dt>Rtm .lib</dt></span><span class="sxs-lookup"><span data-stu-id="361f8-199"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="361f8-200">DLL</span><span class="sxs-lookup"><span data-stu-id="361f8-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="361f8-201"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="361f8-201"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="361f8-202">另請參閱</span><span class="sxs-lookup"><span data-stu-id="361f8-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="361f8-203">路由表管理員第1版參考</span><span class="sxs-lookup"><span data-stu-id="361f8-203">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="361f8-204">路由表管理員第1版函數</span><span class="sxs-lookup"><span data-stu-id="361f8-204">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="361f8-205">**RtmDeleteRoute**</span><span class="sxs-lookup"><span data-stu-id="361f8-205">**RtmDeleteRoute**</span></span>](rtmdeleteroute.md)
</dt> <dt>

[<span data-ttu-id="361f8-206">**RtmDequeueRouteChangeMessage**</span><span class="sxs-lookup"><span data-stu-id="361f8-206">**RtmDequeueRouteChangeMessage**</span></span>](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





