---
title: 'RtmRegisterClient 函式 (Rtm. h) '
description: RtmRegisterClient 函數會將用戶端註冊為指定之通訊協定的處理常式。 它會建立用戶端的路由變更通知機制，並設定通訊協定選項。
ms.assetid: 70426601-695d-47ed-b71a-1df3fb8ddf10
keywords:
- RtmRegisterClient 函式 RAS
topic_type:
- apiref
api_name:
- RtmRegisterClient
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 564f47e68fd6cdce3d5437fe184bac1ed74d8322
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686310"
---
# <a name="rtmregisterclient-function"></a><span data-ttu-id="41c59-105">RtmRegisterClient 函式</span><span class="sxs-lookup"><span data-stu-id="41c59-105">RtmRegisterClient function</span></span>

<span data-ttu-id="41c59-106">\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。</span><span class="sxs-lookup"><span data-stu-id="41c59-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="41c59-107">應用程式應該使用路由表管理員第2版 API。\]</span><span class="sxs-lookup"><span data-stu-id="41c59-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="41c59-108">**RtmRegisterClient** 函數會將用戶端註冊為指定之通訊協定的處理常式。</span><span class="sxs-lookup"><span data-stu-id="41c59-108">The **RtmRegisterClient** function registers a client as a handler of the specified protocol.</span></span> <span data-ttu-id="41c59-109">它會建立用戶端的路由變更通知機制，並設定通訊協定選項。</span><span class="sxs-lookup"><span data-stu-id="41c59-109">It establishes a route change notification mechanism for the client, and sets protocol options.</span></span>

## <a name="syntax"></a><span data-ttu-id="41c59-110">語法</span><span class="sxs-lookup"><span data-stu-id="41c59-110">Syntax</span></span>


```C++
HANDLE RtmRegisterClient(
  _In_ DWORD  ProtocolFamily,
  _In_ DWORD  RoutingProtocol,
  _In_ HANDLE ChangeEvent,
  _In_ DWORD  Flags
);
```



## <a name="parameters"></a><span data-ttu-id="41c59-111">參數</span><span class="sxs-lookup"><span data-stu-id="41c59-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41c59-112">*ProtocolFamily* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41c59-112">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41c59-113">指定要註冊之路由通訊協定的通訊協定系列。</span><span class="sxs-lookup"><span data-stu-id="41c59-113">Specifies the protocol family of the routing protocol to register.</span></span>

</dd> <dt>

<span data-ttu-id="41c59-114">*RoutingProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41c59-114">*RoutingProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41c59-115">指定路由通訊協定識別碼，與向路由器管理員註冊時所使用的相同。</span><span class="sxs-lookup"><span data-stu-id="41c59-115">Specifies the routing protocol identifier, the same as that used when registering with the router manager.</span></span> <span data-ttu-id="41c59-116">請參閱 [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol)。</span><span class="sxs-lookup"><span data-stu-id="41c59-116">See [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol).</span></span>

</dd> <dt>

<span data-ttu-id="41c59-117">*ChangeEvent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41c59-117">*ChangeEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41c59-118">指定資料表中網路的最佳路由已變更。</span><span class="sxs-lookup"><span data-stu-id="41c59-118">Specifies that a best route to a network in the table has changed.</span></span> <span data-ttu-id="41c59-119">路由表管理員會在變更為資料表中任何網路的最佳路由之後，對此事件發出信號。</span><span class="sxs-lookup"><span data-stu-id="41c59-119">The routing table manager signals this event after a change to the best route to any network in the table.</span></span> <span data-ttu-id="41c59-120">如需路由變更通知的詳細資訊，請參閱 [**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md) 。</span><span class="sxs-lookup"><span data-stu-id="41c59-120">See [**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md) for more information about route-change notification.</span></span>

<span data-ttu-id="41c59-121">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="41c59-121">This parameter is optional.</span></span> <span data-ttu-id="41c59-122">如果呼叫端為此參數指定 **Null** ，則路由表管理員不會通知用戶端最適合路由狀態的變更。</span><span class="sxs-lookup"><span data-stu-id="41c59-122">If the caller specifies **NULL** for this parameter, the routing table manager does not notify the client of changes in best route status.</span></span>

</dd> <dt>

<span data-ttu-id="41c59-123">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="41c59-123">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41c59-124">指定路由通訊協定特殊處理的其他選項。</span><span class="sxs-lookup"><span data-stu-id="41c59-124">Specifies miscellaneous options for special handling of the routing protocol.</span></span> <span data-ttu-id="41c59-125">目前支援下列值。</span><span class="sxs-lookup"><span data-stu-id="41c59-125">The following value is currently supported.</span></span>



| <span data-ttu-id="41c59-126">Flags</span><span class="sxs-lookup"><span data-stu-id="41c59-126">Flags</span></span>                                                                                                                                                                                               | <span data-ttu-id="41c59-127">意義</span><span class="sxs-lookup"><span data-stu-id="41c59-127">Meaning</span></span>                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_PROTOCOL_SINGLE_ROUTE"></span><span id="rtm_protocol_single_route"></span><dl> <span data-ttu-id="41c59-128"><dt>**RTM \_ 通訊協定 \_ 單一 \_ 路由**</dt></span><span class="sxs-lookup"><span data-stu-id="41c59-128"><dt>**RTM\_PROTOCOL\_SINGLE\_ROUTE**</dt></span></span> </dl> | <span data-ttu-id="41c59-129">路由表管理員只會針對路由通訊協定的每個目的地網路保留一個路由。</span><span class="sxs-lookup"><span data-stu-id="41c59-129">The routing table manager keeps only one route per destination network for the routing protocol.</span></span> <span data-ttu-id="41c59-130">換句話說，路由表管理員會取代具有相同目的地網路編號的路由專案，而不是加入新的。</span><span class="sxs-lookup"><span data-stu-id="41c59-130">In other words, the routing table manager replaces route entries that have the same destination network numbers instead of adding new ones.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41c59-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="41c59-131">Return value</span></span>

<span data-ttu-id="41c59-132">在成功傳回時，會在後續的路由表管理員呼叫中識別用戶端的 **控制碼** 值。</span><span class="sxs-lookup"><span data-stu-id="41c59-132">On successful return, a **HANDLE** value that identifies the client in subsequent calls to the routing table manager.</span></span>

<span data-ttu-id="41c59-133">**Null** 控制碼指出路由表管理員無法註冊用戶端。</span><span class="sxs-lookup"><span data-stu-id="41c59-133">A **NULL** handle indicates that the routing table manager was unable to register the client.</span></span> <span data-ttu-id="41c59-134">呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 以取得失敗的原因。</span><span class="sxs-lookup"><span data-stu-id="41c59-134">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain the reason for the failure.</span></span>



| <span data-ttu-id="41c59-135">值</span><span class="sxs-lookup"><span data-stu-id="41c59-135">Value</span></span>                                                                                                         | <span data-ttu-id="41c59-136">描述</span><span class="sxs-lookup"><span data-stu-id="41c59-136">Description</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="41c59-137"><dt>**錯誤 \_ 用戶端 \_ 已 \_ 存在**</dt></span><span class="sxs-lookup"><span data-stu-id="41c59-137"><dt>**ERROR\_CLIENT\_ALREADY\_EXISTS**</dt></span></span> </dl> | <span data-ttu-id="41c59-138">另一個用戶端已註冊來處理指定的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="41c59-138">Another client has already registered to handle the specified protocol.</span></span><br/>              |
| <dl> <span data-ttu-id="41c59-139"><dt>**錯誤 \_ 不正確 \_ 參數**</dt></span><span class="sxs-lookup"><span data-stu-id="41c59-139"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>      | <span data-ttu-id="41c59-140">不支援指定的通訊協定系列，或 *旗標* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="41c59-140">The specified protocol family is not supported, or the *Flags* parameter is invalid.</span></span><br/> |
| <dl> <span data-ttu-id="41c59-141"><dt>**錯誤 \_ 的 \_ 系統 \_ 資源**</dt></span><span class="sxs-lookup"><span data-stu-id="41c59-141"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl>   | <span data-ttu-id="41c59-142">資源不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="41c59-142">Insufficient resources to carry out the operation.</span></span><br/>                                   |
| <dl> <span data-ttu-id="41c59-143"><dt>**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</dt></span><span class="sxs-lookup"><span data-stu-id="41c59-143"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>     | <span data-ttu-id="41c59-144">記憶體不足，無法配置用戶端的資料結構。</span><span class="sxs-lookup"><span data-stu-id="41c59-144">Insufficient memory to allocate data structures for the client.</span></span><br/>                      |



 

## <a name="requirements"></a><span data-ttu-id="41c59-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="41c59-145">Requirements</span></span>



| <span data-ttu-id="41c59-146">需求</span><span class="sxs-lookup"><span data-stu-id="41c59-146">Requirement</span></span> | <span data-ttu-id="41c59-147">值</span><span class="sxs-lookup"><span data-stu-id="41c59-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="41c59-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41c59-148">Minimum supported client</span></span><br/> | <span data-ttu-id="41c59-149">都不支援</span><span class="sxs-lookup"><span data-stu-id="41c59-149">None supported</span></span><br/>                                                          |
| <span data-ttu-id="41c59-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41c59-150">Minimum supported server</span></span><br/> | <span data-ttu-id="41c59-151">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41c59-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="41c59-152">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="41c59-152">End of server support</span></span><br/>    | <span data-ttu-id="41c59-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="41c59-153">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="41c59-154">標頭</span><span class="sxs-lookup"><span data-stu-id="41c59-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="41c59-155"><dt>Rtm. h</dt></span><span class="sxs-lookup"><span data-stu-id="41c59-155"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="41c59-156">程式庫</span><span class="sxs-lookup"><span data-stu-id="41c59-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="41c59-157"><dt>Rtm .lib</dt></span><span class="sxs-lookup"><span data-stu-id="41c59-157"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="41c59-158">DLL</span><span class="sxs-lookup"><span data-stu-id="41c59-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41c59-159"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41c59-159"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41c59-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41c59-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41c59-161">路由表管理員第1版參考</span><span class="sxs-lookup"><span data-stu-id="41c59-161">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="41c59-162">路由表管理員第1版函數</span><span class="sxs-lookup"><span data-stu-id="41c59-162">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

<span data-ttu-id="41c59-163">[**3]。Getlasterror**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)</span><span class="sxs-lookup"><span data-stu-id="41c59-163">[**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)</span></span>
</dt> <dt>

[<span data-ttu-id="41c59-164">**RegisterProtocol**</span><span class="sxs-lookup"><span data-stu-id="41c59-164">**RegisterProtocol**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol)
</dt> <dt>

[<span data-ttu-id="41c59-165">RTMv1 通訊協定系列識別碼</span><span class="sxs-lookup"><span data-stu-id="41c59-165">RTMv1 Protocol Family Identifiers</span></span>](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> <dt>

[<span data-ttu-id="41c59-166">**RtmDequeueRouteChangeMessage**</span><span class="sxs-lookup"><span data-stu-id="41c59-166">**RtmDequeueRouteChangeMessage**</span></span>](rtmdequeueroutechangemessage.md)
</dt> <dt>

[<span data-ttu-id="41c59-167">**RtmDeregisterClient**</span><span class="sxs-lookup"><span data-stu-id="41c59-167">**RtmDeregisterClient**</span></span>](rtmderegisterclient.md)
</dt> </dl>

 

