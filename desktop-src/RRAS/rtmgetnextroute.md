---
title: 'RtmGetNextRoute 函式 (Rtm. h) '
description: RtmGetNextRoute 函數會從資料表中指定的路由子集傳回下一個路由。
ms.assetid: 0f413276-2ace-4216-a1a0-1b3061bacc4a
keywords:
- RtmGetNextRoute 函式 RAS
topic_type:
- apiref
api_name:
- RtmGetNextRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da8592855e0c30cef2ed43b7818badd336bc2ab6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508783"
---
# <a name="rtmgetnextroute-function"></a><span data-ttu-id="1576a-104">RtmGetNextRoute 函式</span><span class="sxs-lookup"><span data-stu-id="1576a-104">RtmGetNextRoute function</span></span>

<span data-ttu-id="1576a-105">\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。</span><span class="sxs-lookup"><span data-stu-id="1576a-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="1576a-106">應用程式應該使用路由表管理員第2版 API。\]</span><span class="sxs-lookup"><span data-stu-id="1576a-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="1576a-107">**RtmGetNextRoute** 函數會從資料表中指定的路由子集傳回下一個路由。</span><span class="sxs-lookup"><span data-stu-id="1576a-107">The **RtmGetNextRoute** function returns the next route from the specified subset of routes in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="1576a-108">語法</span><span class="sxs-lookup"><span data-stu-id="1576a-108">Syntax</span></span>


```C++
DWORD RtmGetNextRoute(
  _In_    DWORD ProtocolFamily,
  _In_    DWORD EnumerationFlags,
  _Inout_ PVOID Route
);
```



## <a name="parameters"></a><span data-ttu-id="1576a-109">參數</span><span class="sxs-lookup"><span data-stu-id="1576a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1576a-110">*ProtocolFamily* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1576a-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1576a-111">指定要取出的通訊協定系列（例如 IP 或 IPX）。</span><span class="sxs-lookup"><span data-stu-id="1576a-111">Specifies the protocol family of routes to retrieve, for example, IP or IPX.</span></span>

</dd> <dt>

<span data-ttu-id="1576a-112">*EnumerationFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1576a-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1576a-113">指定應列舉的路由。</span><span class="sxs-lookup"><span data-stu-id="1576a-113">Specifies which routes should be enumerated.</span></span> <span data-ttu-id="1576a-114">此參數會將已刪除的路由集合限制為下列旗標所定義子集，以及 *CriteriaRoute* 參數所指向之結構的對應成員中的值。</span><span class="sxs-lookup"><span data-stu-id="1576a-114">This parameter limits the set of deleted routes to a subset defined by the following flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="1576a-115">旗標與 [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)中使用的旗標相同。</span><span class="sxs-lookup"><span data-stu-id="1576a-115">The flags are the same as those used in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="1576a-116">*路由* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1576a-116">*Route* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1576a-117">在輸入時， *路由* 指向通訊協定系列特定的結構， ( [**rtm \_ IP \_ 路由**](rtm-ip-route.md) 或 [**rtm \_ IPX \_ 路由**](rtm-ipx-route.md)) 。</span><span class="sxs-lookup"><span data-stu-id="1576a-117">On input, *Route* points to a protocol-family-specific structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span>

<span data-ttu-id="1576a-118">呼叫的函式會提供此結構的成員值。</span><span class="sxs-lookup"><span data-stu-id="1576a-118">The calling function provides member values for this structure.</span></span> <span data-ttu-id="1576a-119">這些值與 *EnumerationFlags* 參數搭配使用時，會指定要從中傳回路由的集合。</span><span class="sxs-lookup"><span data-stu-id="1576a-119">These values, in conjunction with the *EnumerationFlags* parameter, specify the set from which to return routes.</span></span>

<span data-ttu-id="1576a-120">在輸出中， *路由* 會指向接收符合指定準則之第一個路由的結構。</span><span class="sxs-lookup"><span data-stu-id="1576a-120">On output, *Route* points to a structure that receives the first route that matched the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1576a-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="1576a-121">Return value</span></span>

<span data-ttu-id="1576a-122">如果函式成功，則傳回值不會是 **\_ 錯誤**。</span><span class="sxs-lookup"><span data-stu-id="1576a-122">If the function succeeds, the return value is **NO\_ERROR**.</span></span>

<span data-ttu-id="1576a-123">如果函式失敗，則傳回值是下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1576a-123">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="1576a-124">值</span><span class="sxs-lookup"><span data-stu-id="1576a-124">Value</span></span>                                                                                                       | <span data-ttu-id="1576a-125">描述</span><span class="sxs-lookup"><span data-stu-id="1576a-125">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1576a-126"><dt>**錯誤 \_ 不正確 \_ 參數**</dt></span><span class="sxs-lookup"><span data-stu-id="1576a-126"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="1576a-127">其中一個參數無效。</span><span class="sxs-lookup"><span data-stu-id="1576a-127">One of the parameters is invalid.</span></span><br/>                            |
| <dl> <span data-ttu-id="1576a-128"><dt>**錯誤 \_ 沒有 \_ 路由**</dt></span><span class="sxs-lookup"><span data-stu-id="1576a-128"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="1576a-129">沒有符合指定準則的路由。</span><span class="sxs-lookup"><span data-stu-id="1576a-129">There are no routes that match the specified criteria.</span></span><br/>       |
| <dl> <span data-ttu-id="1576a-130"><dt>**錯誤 \_ 的 \_ 系統 \_ 資源**</dt></span><span class="sxs-lookup"><span data-stu-id="1576a-130"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="1576a-131">資源不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="1576a-131">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1576a-132">備註</span><span class="sxs-lookup"><span data-stu-id="1576a-132">Remarks</span></span>

<span data-ttu-id="1576a-133">路由會依下列順序傳回：</span><span class="sxs-lookup"><span data-stu-id="1576a-133">The routes are returned in the following order:</span></span>

1.  <span data-ttu-id="1576a-134">網路編號</span><span class="sxs-lookup"><span data-stu-id="1576a-134">Network number</span></span>
2.  <span data-ttu-id="1576a-135">路由通訊協定</span><span class="sxs-lookup"><span data-stu-id="1576a-135">Routing protocol</span></span>
3.  <span data-ttu-id="1576a-136">介面識別碼</span><span class="sxs-lookup"><span data-stu-id="1576a-136">Interface identifier</span></span>
4.  <span data-ttu-id="1576a-137">下個躍點位址</span><span class="sxs-lookup"><span data-stu-id="1576a-137">Next-hop address</span></span>

<span data-ttu-id="1576a-138">這個函式的效率比對應的列舉控制碼函數低。</span><span class="sxs-lookup"><span data-stu-id="1576a-138">This function is less efficient than the corresponding enumeration handle functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="1576a-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="1576a-139">Requirements</span></span>



| <span data-ttu-id="1576a-140">需求</span><span class="sxs-lookup"><span data-stu-id="1576a-140">Requirement</span></span> | <span data-ttu-id="1576a-141">值</span><span class="sxs-lookup"><span data-stu-id="1576a-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1576a-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1576a-142">Minimum supported client</span></span><br/> | <span data-ttu-id="1576a-143">都不支援</span><span class="sxs-lookup"><span data-stu-id="1576a-143">None supported</span></span><br/>                                                          |
| <span data-ttu-id="1576a-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1576a-144">Minimum supported server</span></span><br/> | <span data-ttu-id="1576a-145">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1576a-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1576a-146">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="1576a-146">End of server support</span></span><br/>    | <span data-ttu-id="1576a-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1576a-147">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="1576a-148">標頭</span><span class="sxs-lookup"><span data-stu-id="1576a-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="1576a-149"><dt>Rtm. h</dt></span><span class="sxs-lookup"><span data-stu-id="1576a-149"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="1576a-150">程式庫</span><span class="sxs-lookup"><span data-stu-id="1576a-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="1576a-151"><dt>Rtm .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1576a-151"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="1576a-152">DLL</span><span class="sxs-lookup"><span data-stu-id="1576a-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1576a-153"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1576a-153"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1576a-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1576a-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1576a-155">路由表管理員第1版參考</span><span class="sxs-lookup"><span data-stu-id="1576a-155">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="1576a-156">路由表管理員第1版函數</span><span class="sxs-lookup"><span data-stu-id="1576a-156">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="1576a-157">**RtmCloseEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="1576a-157">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="1576a-158">**RtmCreateEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="1576a-158">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="1576a-159">**RtmEnumerateGetNextRoute**</span><span class="sxs-lookup"><span data-stu-id="1576a-159">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> <dt>

[<span data-ttu-id="1576a-160">**RtmGetFirstRoute**</span><span class="sxs-lookup"><span data-stu-id="1576a-160">**RtmGetFirstRoute**</span></span>](rtmgetfirstroute.md)
</dt> </dl>

 

 





