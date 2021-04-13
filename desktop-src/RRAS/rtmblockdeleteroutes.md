---
title: 'RtmBlockDeleteRoutes 函式 (Rtm. h) '
description: RtmBlockDeleteRoutes 函數會刪除資料表中指定之路由子集內的所有路由。
ms.assetid: d191883d-da3d-4a91-92e6-4979db96f4a4
keywords:
- RtmBlockDeleteRoutes 函式 RAS
topic_type:
- apiref
api_name:
- RtmBlockDeleteRoutes
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71090371fe8a84698b84b84391e5a782fdc636f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465837"
---
# <a name="rtmblockdeleteroutes-function"></a><span data-ttu-id="ef1a8-104">RtmBlockDeleteRoutes 函式</span><span class="sxs-lookup"><span data-stu-id="ef1a8-104">RtmBlockDeleteRoutes function</span></span>

<span data-ttu-id="ef1a8-105">\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。</span><span class="sxs-lookup"><span data-stu-id="ef1a8-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="ef1a8-106">應用程式應該使用路由表管理員第2版 API。\]</span><span class="sxs-lookup"><span data-stu-id="ef1a8-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="ef1a8-107">**RtmBlockDeleteRoutes** 函數會刪除資料表中指定之路由子集內的所有路由。</span><span class="sxs-lookup"><span data-stu-id="ef1a8-107">The **RtmBlockDeleteRoutes** function deletes all routes in the specified subset of routes in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef1a8-108">語法</span><span class="sxs-lookup"><span data-stu-id="ef1a8-108">Syntax</span></span>


```C++
HANDLE RtmBlockDeleteRoutes(
  _In_ HANDLE ClientHandle,
  _In_ DWORD  EnumerationFlags,
  _In_ PVOID  CriteriaRoute
);
```



## <a name="parameters"></a><span data-ttu-id="ef1a8-109">參數</span><span class="sxs-lookup"><span data-stu-id="ef1a8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef1a8-110">*ClientHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef1a8-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef1a8-111">識別要刪除之路由的用戶端和路由通訊協定的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ef1a8-111">Handle that identifies the client, and therefore the routing protocol, of the routes to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="ef1a8-112">*EnumerationFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef1a8-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef1a8-113">指定應列舉的路由。</span><span class="sxs-lookup"><span data-stu-id="ef1a8-113">Specifies which routes should be enumerated.</span></span> <span data-ttu-id="ef1a8-114">此參數會將已刪除的路由集合限制為下列旗標所定義子集，以及 *CriteriaRoute* 參數所指向之結構的對應成員中的值。</span><span class="sxs-lookup"><span data-stu-id="ef1a8-114">This parameter limits the set of deleted routes to a subset defined by the following flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="ef1a8-115">旗標與 [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md) 中使用的旗標相同，不同之處在于 RTM \_ 只有 \_ 最適合 \_ **RtmBlockDeleteRoutes** 的路由是多餘的。</span><span class="sxs-lookup"><span data-stu-id="ef1a8-115">The flags are the same as those used in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md) except that RTM\_ONLY\_BEST\_ROUTES is redundant for **RtmBlockDeleteRoutes**.</span></span> <span data-ttu-id="ef1a8-116">最好是在刪除路由時調整最理想的路由，因此函式最終會刪除子集中的所有路由。</span><span class="sxs-lookup"><span data-stu-id="ef1a8-116">The best-route designation is adjusted as routes are deleted, so the function eventually deletes all the routes in the subset.</span></span>

</dd> <dt>

<span data-ttu-id="ef1a8-117">*CriteriaRoute* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef1a8-117">*CriteriaRoute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef1a8-118">通訊協定系列特定路由結構的指標， ( [**rtm \_ IP \_ 路由**](rtm-ip-route.md) 或 [**rtm \_ IPX \_ 路由**](rtm-ipx-route.md)) 。</span><span class="sxs-lookup"><span data-stu-id="ef1a8-118">Pointer to a protocol-family-specific route structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span> <span data-ttu-id="ef1a8-119">此結構中的成員值會對應至 *EnumerationFlags* 參數所指定的旗標。</span><span class="sxs-lookup"><span data-stu-id="ef1a8-119">The member values in this structure correspond to the flags specified by the *EnumerationFlags* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef1a8-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="ef1a8-120">Return value</span></span>

<span data-ttu-id="ef1a8-121">如果函式成功，則傳回值不會是 \_ 錯誤。</span><span class="sxs-lookup"><span data-stu-id="ef1a8-121">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="ef1a8-122">如果函式失敗，則傳回值是下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ef1a8-122">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="ef1a8-123">值</span><span class="sxs-lookup"><span data-stu-id="ef1a8-123">Value</span></span>                                                                                                       | <span data-ttu-id="ef1a8-124">描述</span><span class="sxs-lookup"><span data-stu-id="ef1a8-124">Description</span></span>                                                                                                |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ef1a8-125"><dt>**錯誤 \_ 沒有 \_ 路由**</dt></span><span class="sxs-lookup"><span data-stu-id="ef1a8-125"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="ef1a8-126">沒有具有指定準則的路由。</span><span class="sxs-lookup"><span data-stu-id="ef1a8-126">There are no routes that have the specified criteria.</span></span><br/>                                           |
| <dl> <span data-ttu-id="ef1a8-127"><dt>**錯誤 \_ 不正確 \_ 控制碼**</dt></span><span class="sxs-lookup"><span data-stu-id="ef1a8-127"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="ef1a8-128">*ClientHandle* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="ef1a8-128">The *ClientHandle* parameter is not valid.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="ef1a8-129"><dt>**錯誤 \_ 不正確 \_ 參數**</dt></span><span class="sxs-lookup"><span data-stu-id="ef1a8-129"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="ef1a8-130">一或多個輸入參數無效，例如列舉旗標無效。</span><span class="sxs-lookup"><span data-stu-id="ef1a8-130">One or more of the input parameters is invalid, for example, the enumeration flags are invalid.</span></span><br/> |
| <dl> <span data-ttu-id="ef1a8-131"><dt>**錯誤 \_ 的 \_ 系統 \_ 資源**</dt></span><span class="sxs-lookup"><span data-stu-id="ef1a8-131"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="ef1a8-132">資源不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="ef1a8-132">There are insufficient resources to carry out the operation.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ef1a8-133"><dt>**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</dt></span><span class="sxs-lookup"><span data-stu-id="ef1a8-133"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="ef1a8-134">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="ef1a8-134">There is insufficient memory to carry out the operation.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="ef1a8-135">備註</span><span class="sxs-lookup"><span data-stu-id="ef1a8-135">Remarks</span></span>

<span data-ttu-id="ef1a8-136">函數會產生適當的通知訊息給所有已註冊的用戶端，包括呼叫者。</span><span class="sxs-lookup"><span data-stu-id="ef1a8-136">The function generates appropriate notification messages to all registered clients including the caller.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef1a8-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef1a8-137">Requirements</span></span>



| <span data-ttu-id="ef1a8-138">需求</span><span class="sxs-lookup"><span data-stu-id="ef1a8-138">Requirement</span></span> | <span data-ttu-id="ef1a8-139">值</span><span class="sxs-lookup"><span data-stu-id="ef1a8-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ef1a8-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ef1a8-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ef1a8-141">都不支援</span><span class="sxs-lookup"><span data-stu-id="ef1a8-141">None supported</span></span><br/>                                                          |
| <span data-ttu-id="ef1a8-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ef1a8-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ef1a8-143">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef1a8-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ef1a8-144">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="ef1a8-144">End of server support</span></span><br/>    | <span data-ttu-id="ef1a8-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ef1a8-145">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="ef1a8-146">標頭</span><span class="sxs-lookup"><span data-stu-id="ef1a8-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef1a8-147"><dt>Rtm. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef1a8-147"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef1a8-148">程式庫</span><span class="sxs-lookup"><span data-stu-id="ef1a8-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="ef1a8-149"><dt>Rtm .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef1a8-149"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="ef1a8-150">DLL</span><span class="sxs-lookup"><span data-stu-id="ef1a8-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef1a8-151"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef1a8-151"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef1a8-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef1a8-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef1a8-153">路由表管理員第1版參考</span><span class="sxs-lookup"><span data-stu-id="ef1a8-153">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="ef1a8-154">路由表管理員第1版函數</span><span class="sxs-lookup"><span data-stu-id="ef1a8-154">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="ef1a8-155">**RtmCreateEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="ef1a8-155">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="ef1a8-156">**RtmRegisterClient**</span><span class="sxs-lookup"><span data-stu-id="ef1a8-156">**RtmRegisterClient**</span></span>](rtmregisterclient.md)
</dt> </dl>

 

 





