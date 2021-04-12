---
title: 'RtmGetFirstRoute 函式 (Rtm. h) '
description: RtmGetFirstRoute 函數會傳回資料表中指定之路由子集的第一個路由。
ms.assetid: f2071b50-4b06-432f-8dbf-45696f8a5cb1
keywords:
- RtmGetFirstRoute 函式 RAS
topic_type:
- apiref
api_name:
- RtmGetFirstRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32e98a5deb0f925fbf3b27c21302060bbe4869b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104387"
---
# <a name="rtmgetfirstroute-function"></a><span data-ttu-id="8df52-104">RtmGetFirstRoute 函式</span><span class="sxs-lookup"><span data-stu-id="8df52-104">RtmGetFirstRoute function</span></span>

<span data-ttu-id="8df52-105">\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。</span><span class="sxs-lookup"><span data-stu-id="8df52-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="8df52-106">應用程式應該使用路由表管理員第2版 API。\]</span><span class="sxs-lookup"><span data-stu-id="8df52-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="8df52-107">**RtmGetFirstRoute** 函數會傳回資料表中指定之路由子集的第一個路由。</span><span class="sxs-lookup"><span data-stu-id="8df52-107">The **RtmGetFirstRoute** function returns the first route from the specified subset of routes in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="8df52-108">語法</span><span class="sxs-lookup"><span data-stu-id="8df52-108">Syntax</span></span>


```C++
DWORD RtmGetFirstRoute(
  _In_    DWORD ProtocolFamily,
  _In_    DWORD EnumerationFlags,
  _Inout_ PVOID Route
);
```



## <a name="parameters"></a><span data-ttu-id="8df52-109">參數</span><span class="sxs-lookup"><span data-stu-id="8df52-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8df52-110">*ProtocolFamily* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8df52-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8df52-111">指定要取出的通訊協定系列（例如 IP 或 IPX）。</span><span class="sxs-lookup"><span data-stu-id="8df52-111">Specifies the protocol family of routes to retrieve, for example, IP or IPX.</span></span>

</dd> <dt>

<span data-ttu-id="8df52-112">*EnumerationFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8df52-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8df52-113">指定將已刪除的路由集合限制為這些旗標所定義的子集，以及 *CriteriaRoute* 參數所指向之結構的對應成員中的值。</span><span class="sxs-lookup"><span data-stu-id="8df52-113">Specifies the limits the set of deleted routes to a subset defined by these flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="8df52-114">旗標與 [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)中使用的旗標相同。</span><span class="sxs-lookup"><span data-stu-id="8df52-114">The flags are the same as those used in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="8df52-115">*路由* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="8df52-115">*Route* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8df52-116">在輸入時， *路由* 指向通訊協定系列特定的結構， ( [**rtm \_ IP \_ 路由**](rtm-ip-route.md) 或 [**rtm \_ IPX \_ 路由**](rtm-ipx-route.md)) 。</span><span class="sxs-lookup"><span data-stu-id="8df52-116">On input, *Route* points to a protocol-family-specific structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span>

<span data-ttu-id="8df52-117">呼叫的函式會提供此結構的成員值。</span><span class="sxs-lookup"><span data-stu-id="8df52-117">The calling function provides member values for this structure.</span></span> <span data-ttu-id="8df52-118">這些值與 *EnumerationFlags* 參數搭配使用時，會指定要從中傳回路由的集合。</span><span class="sxs-lookup"><span data-stu-id="8df52-118">These values, in conjunction with the *EnumerationFlags* parameter, specify the set from which to return routes.</span></span>

<span data-ttu-id="8df52-119">輸出， *路由* 指向符合指定準則的第一個路由。</span><span class="sxs-lookup"><span data-stu-id="8df52-119">Out output, *Route* points to the first route that matched the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8df52-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="8df52-120">Return value</span></span>

<span data-ttu-id="8df52-121">如果函式成功，則傳回值不會是 \_ 錯誤。</span><span class="sxs-lookup"><span data-stu-id="8df52-121">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="8df52-122">如果函式失敗，則傳回值是下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8df52-122">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="8df52-123">值</span><span class="sxs-lookup"><span data-stu-id="8df52-123">Value</span></span>                                                                                                       | <span data-ttu-id="8df52-124">描述</span><span class="sxs-lookup"><span data-stu-id="8df52-124">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8df52-125"><dt>**錯誤 \_ 不正確 \_ 參數**</dt></span><span class="sxs-lookup"><span data-stu-id="8df52-125"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="8df52-126">其中一個參數無效。</span><span class="sxs-lookup"><span data-stu-id="8df52-126">One of the parameters is invalid.</span></span><br/>                            |
| <dl> <span data-ttu-id="8df52-127"><dt>**錯誤 \_ 沒有 \_ 路由**</dt></span><span class="sxs-lookup"><span data-stu-id="8df52-127"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="8df52-128">沒有符合指定準則的路由。</span><span class="sxs-lookup"><span data-stu-id="8df52-128">There are no routes that match the specified criteria.</span></span><br/>       |
| <dl> <span data-ttu-id="8df52-129"><dt>**錯誤 \_ 的 \_ 系統 \_ 資源**</dt></span><span class="sxs-lookup"><span data-stu-id="8df52-129"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="8df52-130">資源不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="8df52-130">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8df52-131">備註</span><span class="sxs-lookup"><span data-stu-id="8df52-131">Remarks</span></span>

<span data-ttu-id="8df52-132">路由會依下列順序傳回：</span><span class="sxs-lookup"><span data-stu-id="8df52-132">The routes are returned in the following order:</span></span>

1.  <span data-ttu-id="8df52-133">網路編號</span><span class="sxs-lookup"><span data-stu-id="8df52-133">Network number</span></span>
2.  <span data-ttu-id="8df52-134">路由通訊協定</span><span class="sxs-lookup"><span data-stu-id="8df52-134">Routing protocol</span></span>
3.  <span data-ttu-id="8df52-135">介面識別碼</span><span class="sxs-lookup"><span data-stu-id="8df52-135">Interface identifier</span></span>
4.  <span data-ttu-id="8df52-136">下個躍點位址</span><span class="sxs-lookup"><span data-stu-id="8df52-136">Next-hop address</span></span>

<span data-ttu-id="8df52-137">相較于對應的列舉控制碼函式 [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md)，此函式的效率較低。</span><span class="sxs-lookup"><span data-stu-id="8df52-137">This function is less efficient than the corresponding enumeration handle function, [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8df52-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="8df52-138">Requirements</span></span>



| <span data-ttu-id="8df52-139">需求</span><span class="sxs-lookup"><span data-stu-id="8df52-139">Requirement</span></span> | <span data-ttu-id="8df52-140">值</span><span class="sxs-lookup"><span data-stu-id="8df52-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8df52-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8df52-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8df52-142">都不支援</span><span class="sxs-lookup"><span data-stu-id="8df52-142">None supported</span></span><br/>                                                          |
| <span data-ttu-id="8df52-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8df52-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8df52-144">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8df52-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8df52-145">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="8df52-145">End of server support</span></span><br/>    | <span data-ttu-id="8df52-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8df52-146">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="8df52-147">標頭</span><span class="sxs-lookup"><span data-stu-id="8df52-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="8df52-148"><dt>Rtm. h</dt></span><span class="sxs-lookup"><span data-stu-id="8df52-148"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="8df52-149">程式庫</span><span class="sxs-lookup"><span data-stu-id="8df52-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="8df52-150"><dt>Rtm .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8df52-150"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="8df52-151">DLL</span><span class="sxs-lookup"><span data-stu-id="8df52-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8df52-152"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8df52-152"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8df52-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8df52-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8df52-154">路由表管理員第1版參考</span><span class="sxs-lookup"><span data-stu-id="8df52-154">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="8df52-155">路由表管理員第1版函數</span><span class="sxs-lookup"><span data-stu-id="8df52-155">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="8df52-156">**RtmCloseEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="8df52-156">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="8df52-157">**RtmCreateEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="8df52-157">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="8df52-158">**RtmEnumerateGetNextRoute**</span><span class="sxs-lookup"><span data-stu-id="8df52-158">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> <dt>

[<span data-ttu-id="8df52-159">**RtmGetNextRoute**</span><span class="sxs-lookup"><span data-stu-id="8df52-159">**RtmGetNextRoute**</span></span>](rtmgetnextroute.md)
</dt> </dl>

 

 





