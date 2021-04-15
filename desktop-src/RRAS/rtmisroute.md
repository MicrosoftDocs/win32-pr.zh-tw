---
title: 'RtmIsRoute 函式 (Rtm. h) '
description: RtmIsRoute 函式會判斷是否有一或多個路由傳送至指定的目的地網路。 如果是，則函式會傳回最適合該網路的路由資訊。
ms.assetid: f9939790-d0a6-487e-9674-a01d436dc962
keywords:
- RtmIsRoute 函式 RAS
topic_type:
- apiref
api_name:
- RtmIsRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64621732f2f7a35223421e5f0fc86a309d332c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466312"
---
# <a name="rtmisroute-function"></a><span data-ttu-id="d8da2-105">RtmIsRoute 函式</span><span class="sxs-lookup"><span data-stu-id="d8da2-105">RtmIsRoute function</span></span>

<span data-ttu-id="d8da2-106">\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。</span><span class="sxs-lookup"><span data-stu-id="d8da2-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="d8da2-107">應用程式應該使用路由表管理員第2版 API。\]</span><span class="sxs-lookup"><span data-stu-id="d8da2-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="d8da2-108">**RtmIsRoute** 函式會判斷是否有一或多個路由傳送至指定的目的地網路。</span><span class="sxs-lookup"><span data-stu-id="d8da2-108">The **RtmIsRoute** function determines if one or more routes to a specified destination network exist.</span></span> <span data-ttu-id="d8da2-109">如果是，則函式會傳回最適合該網路的路由資訊。</span><span class="sxs-lookup"><span data-stu-id="d8da2-109">If so, the function returns information for the best route to that network.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8da2-110">語法</span><span class="sxs-lookup"><span data-stu-id="d8da2-110">Syntax</span></span>


```C++
BOOL RtmIsRoute(
  _In_  DWORD ProtocolFamily,
  _In_  PVOID Network,
  _Out_ PVOID BestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="d8da2-111">參數</span><span class="sxs-lookup"><span data-stu-id="d8da2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8da2-112">*ProtocolFamily* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d8da2-112">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8da2-113">指定 *Network* 參數所指向的資料結構類型，例如 [**IP \_ network**](ip-network.md)、 [**IPX \_ network**](ipx-network.md)。</span><span class="sxs-lookup"><span data-stu-id="d8da2-113">Specifies the type of data structure pointed to by the *Network* parameter, for example, [**IP\_NETWORK**](ip-network.md), [**IPX\_NETWORK**](ipx-network.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8da2-114">*網路* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d8da2-114">*Network* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8da2-115">結構的指標，指定通訊協定系列特定的網路編號資料。</span><span class="sxs-lookup"><span data-stu-id="d8da2-115">Pointer to a structure that specifies protocol-family-specific network number data.</span></span> <span data-ttu-id="d8da2-116">此資料會識別呼叫端搜尋路由資訊的網路。</span><span class="sxs-lookup"><span data-stu-id="d8da2-116">This data identifies the network for which the caller seeks route information.</span></span>

</dd> <dt>

<span data-ttu-id="d8da2-117">*BestRoute* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d8da2-117">*BestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8da2-118">通訊協定系列特定結構的指標，此結構會接收目前最佳的路由資訊（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="d8da2-118">Pointer to a protocol-family-specific structure that receives the current best route information, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8da2-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="d8da2-119">Return value</span></span>

<span data-ttu-id="d8da2-120">傳回值是下列其中一個程式碼。</span><span class="sxs-lookup"><span data-stu-id="d8da2-120">The return value is one of the following codes.</span></span>



| <span data-ttu-id="d8da2-121">值</span><span class="sxs-lookup"><span data-stu-id="d8da2-121">Value</span></span>                                                                                                       | <span data-ttu-id="d8da2-122">描述</span><span class="sxs-lookup"><span data-stu-id="d8da2-122">Description</span></span>                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d8da2-123"><dt>**真**</dt></span><span class="sxs-lookup"><span data-stu-id="d8da2-123"><dt>**TRUE**</dt></span></span> </dl>                         | <span data-ttu-id="d8da2-124">至少有一個指定網路的路由存在。</span><span class="sxs-lookup"><span data-stu-id="d8da2-124">At least one route to the specified network exists.</span></span> <span data-ttu-id="d8da2-125">最佳路由會傳回在 *BestRoute* 參數所指向的結構中。</span><span class="sxs-lookup"><span data-stu-id="d8da2-125">The best route is returned in the structure pointed to by the *BestRoute* parameter.</span></span><br/>      |
| <dl> <span data-ttu-id="d8da2-126"><dt>**假**</dt></span><span class="sxs-lookup"><span data-stu-id="d8da2-126"><dt>**FALSE**</dt></span></span> </dl>                        | <span data-ttu-id="d8da2-127">沒有指定網路的路由，或操作失敗。</span><span class="sxs-lookup"><span data-stu-id="d8da2-127">There is no route to the specified network, or the operation failed.</span></span> <span data-ttu-id="d8da2-128">呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 以取得詳細資訊：</span><span class="sxs-lookup"><span data-stu-id="d8da2-128">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain more information:</span></span><br/> |
| <dl> <span data-ttu-id="d8da2-129"><dt>**沒有 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="d8da2-129"><dt>**NO\_ERROR**</dt></span></span> </dl>                    | <span data-ttu-id="d8da2-130">作業成功，但沒有指定網路的路由。</span><span class="sxs-lookup"><span data-stu-id="d8da2-130">The operation succeeded, but there is no route to the specified network.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="d8da2-131"><dt>**錯誤 \_ 不正確 \_ 參數**</dt></span><span class="sxs-lookup"><span data-stu-id="d8da2-131"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="d8da2-132">*ProtocolFamily* 參數的值未對應到任何已安裝的通訊協定系列。</span><span class="sxs-lookup"><span data-stu-id="d8da2-132">The value of the *ProtocolFamily* parameter does not correspond to any installed protocol family.</span></span><br/>                                             |
| <dl> <span data-ttu-id="d8da2-133"><dt>**錯誤 \_ 的 \_ 系統 \_ 資源**</dt></span><span class="sxs-lookup"><span data-stu-id="d8da2-133"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="d8da2-134">資源不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="d8da2-134">There are insufficient resources to carry out the operation.</span></span><br/>                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="d8da2-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8da2-135">Requirements</span></span>



| <span data-ttu-id="d8da2-136">需求</span><span class="sxs-lookup"><span data-stu-id="d8da2-136">Requirement</span></span> | <span data-ttu-id="d8da2-137">值</span><span class="sxs-lookup"><span data-stu-id="d8da2-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d8da2-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d8da2-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d8da2-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="d8da2-139">None supported</span></span><br/>                                                          |
| <span data-ttu-id="d8da2-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d8da2-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d8da2-141">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8da2-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d8da2-142">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="d8da2-142">End of server support</span></span><br/>    | <span data-ttu-id="d8da2-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d8da2-143">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="d8da2-144">標頭</span><span class="sxs-lookup"><span data-stu-id="d8da2-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8da2-145"><dt>Rtm. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8da2-145"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="d8da2-146">程式庫</span><span class="sxs-lookup"><span data-stu-id="d8da2-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="d8da2-147"><dt>Rtm .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8da2-147"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="d8da2-148">DLL</span><span class="sxs-lookup"><span data-stu-id="d8da2-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8da2-149"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8da2-149"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8da2-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8da2-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8da2-151">路由表管理員第1版參考</span><span class="sxs-lookup"><span data-stu-id="d8da2-151">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="d8da2-152">路由表管理員第1版函數</span><span class="sxs-lookup"><span data-stu-id="d8da2-152">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

<span data-ttu-id="d8da2-153">[**3]。Getlasterror**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)</span><span class="sxs-lookup"><span data-stu-id="d8da2-153">[**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)</span></span>
</dt> <dt>

[<span data-ttu-id="d8da2-154">**IP \_ 網路**</span><span class="sxs-lookup"><span data-stu-id="d8da2-154">**IP\_NETWORK**</span></span>](ip-network.md)
</dt> <dt>

[<span data-ttu-id="d8da2-155">**IPX \_ 網路**</span><span class="sxs-lookup"><span data-stu-id="d8da2-155">**IPX\_NETWORK**</span></span>](ipx-network.md)
</dt> <dt>

[<span data-ttu-id="d8da2-156">RTMv1 通訊協定系列識別碼</span><span class="sxs-lookup"><span data-stu-id="d8da2-156">RTMv1 Protocol Family Identifiers</span></span>](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

