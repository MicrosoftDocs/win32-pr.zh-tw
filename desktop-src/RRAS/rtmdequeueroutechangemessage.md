---
title: 'RtmDequeueRouteChangeMessage 函式 (Rtm. h) '
description: RtmDequeueRouteChangeMessage 函式會傳回與指定之用戶端相關聯之佇列中的下一個路由變更訊息。
ms.assetid: 44f2116a-3c8d-4ac6-896e-b12930b218a5
keywords:
- RtmDequeueRouteChangeMessage 函式 RAS
topic_type:
- apiref
api_name:
- RtmDequeueRouteChangeMessage
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 448df230742b03f82294de102bf14b50fefa035c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104388"
---
# <a name="rtmdequeueroutechangemessage-function"></a><span data-ttu-id="645b0-104">RtmDequeueRouteChangeMessage 函式</span><span class="sxs-lookup"><span data-stu-id="645b0-104">RtmDequeueRouteChangeMessage function</span></span>

<span data-ttu-id="645b0-105">\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。</span><span class="sxs-lookup"><span data-stu-id="645b0-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="645b0-106">應用程式應該使用路由表管理員第2版 API。\]</span><span class="sxs-lookup"><span data-stu-id="645b0-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="645b0-107">**RtmDequeueRouteChangeMessage** 函式會傳回與指定之用戶端相關聯之佇列中的下一個路由變更訊息。</span><span class="sxs-lookup"><span data-stu-id="645b0-107">The **RtmDequeueRouteChangeMessage** function returns the next route-change message in the queue associated with the specified client.</span></span>

## <a name="syntax"></a><span data-ttu-id="645b0-108">語法</span><span class="sxs-lookup"><span data-stu-id="645b0-108">Syntax</span></span>


```C++
DWORD RtmDequeueRouteChangeMessage(
  _In_  HANDLE ClientHandle,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute,
  _Out_ PVOID  PrevBestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="645b0-109">參數</span><span class="sxs-lookup"><span data-stu-id="645b0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="645b0-110">*ClientHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="645b0-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="645b0-111">識別要執行作業之用戶端的控制碼。</span><span class="sxs-lookup"><span data-stu-id="645b0-111">Handle that identifies the client for which the operation is performed.</span></span> <span data-ttu-id="645b0-112">藉由呼叫 [**RtmRegisterClient**](rtmregisterclient.md)來取得此控制碼。</span><span class="sxs-lookup"><span data-stu-id="645b0-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> <dt>

<span data-ttu-id="645b0-113">*旗標* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="645b0-113">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="645b0-114">**DWORD** 變數的指標。</span><span class="sxs-lookup"><span data-stu-id="645b0-114">Pointer to a **DWORD** variable.</span></span> <span data-ttu-id="645b0-115">此變數的值是由路由表管理員所設定。</span><span class="sxs-lookup"><span data-stu-id="645b0-115">The value of this variable is set by the routing table manager.</span></span> <span data-ttu-id="645b0-116">值會指定變更訊息的類型，以及在提供的緩衝區中傳回的資訊。</span><span class="sxs-lookup"><span data-stu-id="645b0-116">The value specifies the type of the change message, and what information was returned in the provided buffers.</span></span> <span data-ttu-id="645b0-117">此參數是下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="645b0-117">This parameter is one of the following.</span></span>



| <span data-ttu-id="645b0-118">Flags</span><span class="sxs-lookup"><span data-stu-id="645b0-118">Flags</span></span>                                                                                                                                                                      | <span data-ttu-id="645b0-119">意義</span><span class="sxs-lookup"><span data-stu-id="645b0-119">Meaning</span></span>                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <span data-ttu-id="645b0-120"><dt>**\_ \_ 已新增 RTM 路由**</dt></span><span class="sxs-lookup"><span data-stu-id="645b0-120"><dt>**RTM\_ROUTE\_ADDED**</dt></span></span> </dl>       | <span data-ttu-id="645b0-121">已針對特定目的地網路新增第一個路由。</span><span class="sxs-lookup"><span data-stu-id="645b0-121">The first route was added for a particular destination network.</span></span> <span data-ttu-id="645b0-122">*CurBestRoute* 參數會指向新增路由的資訊。</span><span class="sxs-lookup"><span data-stu-id="645b0-122">The *CurBestRoute* parameter points to the information for the added route.</span></span><br/>                                                                                                                                                            |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <span data-ttu-id="645b0-123"><dt>**\_ \_ 已刪除 RTM 路由**</dt></span><span class="sxs-lookup"><span data-stu-id="645b0-123"><dt>**RTM\_ROUTE\_DELETED**</dt></span></span> </dl> | <span data-ttu-id="645b0-124">特定目的地網路唯一可用的路由已刪除。</span><span class="sxs-lookup"><span data-stu-id="645b0-124">The only route available for a particular destination network was deleted.</span></span> <span data-ttu-id="645b0-125">*PrevBestRoute* 參數會指向已刪除之路由的資訊。</span><span class="sxs-lookup"><span data-stu-id="645b0-125">The *PrevBestRoute* parameter points to the information for the deleted route.</span></span><br/>                                                                                                                                              |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <span data-ttu-id="645b0-126"><dt>**RTM \_ 路由 \_ 已變更**</dt></span><span class="sxs-lookup"><span data-stu-id="645b0-126"><dt>**RTM\_ROUTE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="645b0-127">至少有一個重要的參數變更，以取得特定目的地網路的最佳路由。</span><span class="sxs-lookup"><span data-stu-id="645b0-127">At least one of the significant parameters was changed for a best route to a particular destination network.</span></span> <span data-ttu-id="645b0-128">重要的參數包括：</span><span class="sxs-lookup"><span data-stu-id="645b0-128">The significant parameters are:</span></span> <br/> <span data-ttu-id="645b0-129">通訊協定識別碼</span><span class="sxs-lookup"><span data-stu-id="645b0-129">Protocol identifier</span></span><br/> <span data-ttu-id="645b0-130">介面索引</span><span class="sxs-lookup"><span data-stu-id="645b0-130">Interface index</span></span><br/> <span data-ttu-id="645b0-131">下個躍點位址</span><span class="sxs-lookup"><span data-stu-id="645b0-131">Next-hop address</span></span><br/> <span data-ttu-id="645b0-132">通訊協定系列特定的資料 (包括路由計量) </span><span class="sxs-lookup"><span data-stu-id="645b0-132">Protocol-family-specific data (including route metrics)</span></span><br/> |



 

<span data-ttu-id="645b0-133">*PrevBestRoute* 參數會指向變更之前的路由資訊。</span><span class="sxs-lookup"><span data-stu-id="645b0-133">The *PrevBestRoute* parameter points to the route information as it was before the change.</span></span> <span data-ttu-id="645b0-134">*CurBestRoute* 參數會指向目前的 (，也就是變更後) 路由資訊。</span><span class="sxs-lookup"><span data-stu-id="645b0-134">The *CurBestRoute* parameter points to current (that is, after-change) route information.</span></span>

</dd> <dt>

<span data-ttu-id="645b0-135">*CurBestRoute* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="645b0-135">*CurBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="645b0-136">結構的指標，此結構會接收目前的最佳路由資訊 (是否有任何) 。</span><span class="sxs-lookup"><span data-stu-id="645b0-136">Pointer to a structure that receives the current best-route information (if any).</span></span> <span data-ttu-id="645b0-137">結構的類型是通訊協定系列專用的，例如 IP 或 IPX。</span><span class="sxs-lookup"><span data-stu-id="645b0-137">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="645b0-138">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="645b0-138">This parameter is optional.</span></span> <span data-ttu-id="645b0-139">如果呼叫端為此參數指定 **Null** ，則不會傳回目前的最佳路由資訊。</span><span class="sxs-lookup"><span data-stu-id="645b0-139">If the caller specifies **NULL** for this parameter, the current best-route information is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="645b0-140">*PrevBestRoute* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="645b0-140">*PrevBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="645b0-141">結構的指標，此結構會接收先前的最佳路由資訊（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="645b0-141">Pointer to a structure that receives the previous best-route information, if any.</span></span> <span data-ttu-id="645b0-142">結構的類型是通訊協定系列專用的，例如 IP 或 IPX。</span><span class="sxs-lookup"><span data-stu-id="645b0-142">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="645b0-143">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="645b0-143">This parameter is optional.</span></span> <span data-ttu-id="645b0-144">如果呼叫端為此參數指定 **Null** ，則不會傳回先前的最佳路由資訊。</span><span class="sxs-lookup"><span data-stu-id="645b0-144">If the caller specifies **NULL** for this parameter, the previous best-route information is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="645b0-145">傳回值</span><span class="sxs-lookup"><span data-stu-id="645b0-145">Return value</span></span>

<span data-ttu-id="645b0-146">傳回值是下列其中一個程式碼。</span><span class="sxs-lookup"><span data-stu-id="645b0-146">The return value is one of the following codes.</span></span>



| <span data-ttu-id="645b0-147">值</span><span class="sxs-lookup"><span data-stu-id="645b0-147">Value</span></span>                                                                                                       | <span data-ttu-id="645b0-148">描述</span><span class="sxs-lookup"><span data-stu-id="645b0-148">Description</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="645b0-149"><dt>**沒有 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="645b0-149"><dt>**NO\_ERROR**</dt></span></span> </dl>                    | <span data-ttu-id="645b0-150">此訊息是用戶端佇列中的最後一則訊息。</span><span class="sxs-lookup"><span data-stu-id="645b0-150">This message was the last message in the client's queue.</span></span> <span data-ttu-id="645b0-151">事件物件已重設。</span><span class="sxs-lookup"><span data-stu-id="645b0-151">The event object is reset.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="645b0-152"><dt>**錯誤 \_ 不正確 \_ 控制碼**</dt></span><span class="sxs-lookup"><span data-stu-id="645b0-152"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="645b0-153">*ClientHandle* 參數不是有效的控制碼，或在註冊時，用戶端未提供變更訊息通知的事件物件 (請參閱 [**RtmRegisterClient**](rtmregisterclient.md)) 。</span><span class="sxs-lookup"><span data-stu-id="645b0-153">The *ClientHandle* parameter is not a valid handle, or at registration the client did not provide an event object for change message notification (see [**RtmRegisterClient**](rtmregisterclient.md)).</span></span><br/>                           |
| <dl> <span data-ttu-id="645b0-154"><dt>**錯誤 \_ 的 \_ 訊息**</dt></span><span class="sxs-lookup"><span data-stu-id="645b0-154"><dt>**ERROR\_MORE\_MESSAGES**</dt></span></span> </dl>        | <span data-ttu-id="645b0-155">用戶端的佇列包含額外的訊息。</span><span class="sxs-lookup"><span data-stu-id="645b0-155">The client's queue contains additional messages.</span></span> <span data-ttu-id="645b0-156">用戶端應該儘快呼叫 **RtmDequeueRouteChangeMessage** ，以允許路由表管理員釋放與擱置中訊息相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="645b0-156">The client should call **RtmDequeueRouteChangeMessage** again as soon as possible to allow the routing table manager to free the resources associated with the pending messages.</span></span><br/> |
| <dl> <span data-ttu-id="645b0-157"><dt>**錯誤 \_ \_ 訊息**</dt></span><span class="sxs-lookup"><span data-stu-id="645b0-157"><dt>**ERROR\_NO\_MESSAGES**</dt></span></span> </dl>          | <span data-ttu-id="645b0-158">用戶端的佇列不包含任何訊息;呼叫未經要求。</span><span class="sxs-lookup"><span data-stu-id="645b0-158">The client's queue contains no messages; the call was unsolicited.</span></span> <span data-ttu-id="645b0-159">此事件已重設。</span><span class="sxs-lookup"><span data-stu-id="645b0-159">The event is reset.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="645b0-160"><dt>**錯誤 \_ 的 \_ 系統 \_ 資源**</dt></span><span class="sxs-lookup"><span data-stu-id="645b0-160"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="645b0-161">資源不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="645b0-161">There are insufficient resources to carry out the operation.</span></span><br/>                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="645b0-162">規格需求</span><span class="sxs-lookup"><span data-stu-id="645b0-162">Requirements</span></span>



| <span data-ttu-id="645b0-163">需求</span><span class="sxs-lookup"><span data-stu-id="645b0-163">Requirement</span></span> | <span data-ttu-id="645b0-164">值</span><span class="sxs-lookup"><span data-stu-id="645b0-164">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="645b0-165">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="645b0-165">Minimum supported client</span></span><br/> | <span data-ttu-id="645b0-166">都不支援</span><span class="sxs-lookup"><span data-stu-id="645b0-166">None supported</span></span><br/>                                                          |
| <span data-ttu-id="645b0-167">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="645b0-167">Minimum supported server</span></span><br/> | <span data-ttu-id="645b0-168">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="645b0-168">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="645b0-169">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="645b0-169">End of server support</span></span><br/>    | <span data-ttu-id="645b0-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="645b0-170">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="645b0-171">標頭</span><span class="sxs-lookup"><span data-stu-id="645b0-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="645b0-172"><dt>Rtm. h</dt></span><span class="sxs-lookup"><span data-stu-id="645b0-172"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="645b0-173">程式庫</span><span class="sxs-lookup"><span data-stu-id="645b0-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="645b0-174"><dt>Rtm .lib</dt></span><span class="sxs-lookup"><span data-stu-id="645b0-174"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="645b0-175">DLL</span><span class="sxs-lookup"><span data-stu-id="645b0-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="645b0-176"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="645b0-176"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="645b0-177">另請參閱</span><span class="sxs-lookup"><span data-stu-id="645b0-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="645b0-178">路由表管理員第1版參考</span><span class="sxs-lookup"><span data-stu-id="645b0-178">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="645b0-179">路由表管理員第1版函數</span><span class="sxs-lookup"><span data-stu-id="645b0-179">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="645b0-180">**RtmRegisterClient**</span><span class="sxs-lookup"><span data-stu-id="645b0-180">**RtmRegisterClient**</span></span>](rtmregisterclient.md)
</dt> </dl>

 

 





