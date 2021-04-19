---
title: 'RtmEnumerateGetNextRoute 函式 (Rtm. h) '
description: RtmEnumerateGetNextRoute 函式會傳回列舉中由 RtmCreateEnumerationHandle 呼叫開始的下一個路由專案。
ms.assetid: fff6fb58-8a37-49f0-abc5-354b5bc340f8
keywords:
- RtmEnumerateGetNextRoute 函式 RAS
topic_type:
- apiref
api_name:
- RtmEnumerateGetNextRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e74cc5aa15c1014056075e876efca296556066d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968974"
---
# <a name="rtmenumerategetnextroute-function"></a><span data-ttu-id="c1b2f-104">RtmEnumerateGetNextRoute 函式</span><span class="sxs-lookup"><span data-stu-id="c1b2f-104">RtmEnumerateGetNextRoute function</span></span>

<span data-ttu-id="c1b2f-105">\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。</span><span class="sxs-lookup"><span data-stu-id="c1b2f-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="c1b2f-106">應用程式應該使用路由表管理員第2版 API。\]</span><span class="sxs-lookup"><span data-stu-id="c1b2f-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="c1b2f-107">**RtmEnumerateGetNextRoute** 函式會傳回列舉中由 [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)呼叫開始的下一個路由專案。</span><span class="sxs-lookup"><span data-stu-id="c1b2f-107">The **RtmEnumerateGetNextRoute** function returns the next-route entry in the enumeration started by a call to [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c1b2f-108">語法</span><span class="sxs-lookup"><span data-stu-id="c1b2f-108">Syntax</span></span>


```C++
DWORD RtmEnumerateGetNextRoute(
  _In_  HANDLE EnumerationHandle,
  _Out_ PVOID  Route
);
```



## <a name="parameters"></a><span data-ttu-id="c1b2f-109">參數</span><span class="sxs-lookup"><span data-stu-id="c1b2f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1b2f-110">*EnumerationHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c1b2f-110">*EnumerationHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1b2f-111">識別列舉的控制碼，並指定其範圍。</span><span class="sxs-lookup"><span data-stu-id="c1b2f-111">Handle that identifies the enumeration and specifies its scope.</span></span> <span data-ttu-id="c1b2f-112">藉由呼叫 [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)來取得此控制碼。</span><span class="sxs-lookup"><span data-stu-id="c1b2f-112">Obtain this handle by calling [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1b2f-113">*路由* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c1b2f-113">*Route* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1b2f-114">通訊協定系列特定路由結構的指標， ( [**rtm \_ IP \_ 路由**](rtm-ip-route.md) 或 [**rtm \_ IPX \_ 路由**](rtm-ipx-route.md)) 。</span><span class="sxs-lookup"><span data-stu-id="c1b2f-114">Pointer to a protocol-family-specific route structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span> <span data-ttu-id="c1b2f-115">此結構會接收列舉中的下一個路由。</span><span class="sxs-lookup"><span data-stu-id="c1b2f-115">This structure will receive the next route in the enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1b2f-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1b2f-116">Return value</span></span>

<span data-ttu-id="c1b2f-117">如果函式成功，則傳回值不會是 \_ 錯誤。</span><span class="sxs-lookup"><span data-stu-id="c1b2f-117">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="c1b2f-118">如果函式失敗，則傳回值是下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c1b2f-118">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="c1b2f-119">值</span><span class="sxs-lookup"><span data-stu-id="c1b2f-119">Value</span></span>                                                                                                       | <span data-ttu-id="c1b2f-120">描述</span><span class="sxs-lookup"><span data-stu-id="c1b2f-120">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c1b2f-121"><dt>**錯誤 \_ 不正確 \_ 控制碼**</dt></span><span class="sxs-lookup"><span data-stu-id="c1b2f-121"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="c1b2f-122">*EnumerationHandle* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="c1b2f-122">The *EnumerationHandle* parameter is not valid.</span></span><br/>              |
| <dl> <span data-ttu-id="c1b2f-123"><dt>**錯誤 \_ 沒有 \_ 其他 \_ 路由**</dt></span><span class="sxs-lookup"><span data-stu-id="c1b2f-123"><dt>**ERROR\_NO\_MORE\_ROUTES**</dt></span></span> </dl>      | <span data-ttu-id="c1b2f-124">列舉中沒有任何路由。</span><span class="sxs-lookup"><span data-stu-id="c1b2f-124">There are no more routes in the enumeration.</span></span><br/>                 |
| <dl> <span data-ttu-id="c1b2f-125"><dt>**錯誤 \_ 的 \_ 系統 \_ 資源**</dt></span><span class="sxs-lookup"><span data-stu-id="c1b2f-125"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="c1b2f-126">資源不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="c1b2f-126">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c1b2f-127">備註</span><span class="sxs-lookup"><span data-stu-id="c1b2f-127">Remarks</span></span>

<span data-ttu-id="c1b2f-128">雖然路由不會以任何特定順序傳回，但是列舉中的每個路由只會傳回一次。</span><span class="sxs-lookup"><span data-stu-id="c1b2f-128">Although routes are not returned in any particular order, each route in the enumeration is returned only once.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1b2f-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1b2f-129">Requirements</span></span>



| <span data-ttu-id="c1b2f-130">需求</span><span class="sxs-lookup"><span data-stu-id="c1b2f-130">Requirement</span></span> | <span data-ttu-id="c1b2f-131">值</span><span class="sxs-lookup"><span data-stu-id="c1b2f-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c1b2f-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c1b2f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c1b2f-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="c1b2f-133">None supported</span></span><br/>                                                          |
| <span data-ttu-id="c1b2f-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c1b2f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c1b2f-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1b2f-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c1b2f-136">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="c1b2f-136">End of server support</span></span><br/>    | <span data-ttu-id="c1b2f-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c1b2f-137">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="c1b2f-138">標頭</span><span class="sxs-lookup"><span data-stu-id="c1b2f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1b2f-139"><dt>Rtm. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1b2f-139"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="c1b2f-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="c1b2f-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="c1b2f-141"><dt>Rtm .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1b2f-141"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="c1b2f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c1b2f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1b2f-143"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1b2f-143"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1b2f-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1b2f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1b2f-145">路由表管理員第1版參考</span><span class="sxs-lookup"><span data-stu-id="c1b2f-145">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="c1b2f-146">路由表管理員第1版函數</span><span class="sxs-lookup"><span data-stu-id="c1b2f-146">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="c1b2f-147">**RTM \_ IP \_ 路由**</span><span class="sxs-lookup"><span data-stu-id="c1b2f-147">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="c1b2f-148">**RTM \_ IPX \_ 路由**</span><span class="sxs-lookup"><span data-stu-id="c1b2f-148">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> <dt>

[<span data-ttu-id="c1b2f-149">**RtmCloseEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="c1b2f-149">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="c1b2f-150">**RtmCreateEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="c1b2f-150">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> </dl>

 

 





