---
title: 'RtmDeregisterClient 函式 (Rtm. h) '
description: RtmDeregisterClient 函式會取消註冊用戶端，並釋出與用戶端相關聯的資源。
ms.assetid: 5d04f276-86a7-4e63-8266-e93f0d6e5241
keywords:
- RtmDeregisterClient 函式 RAS
topic_type:
- apiref
api_name:
- RtmDeregisterClient
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab1f56d3d65e13c083d8952f500cfba4638ab83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384637"
---
# <a name="rtmderegisterclient-function"></a><span data-ttu-id="d6f8d-104">RtmDeregisterClient 函式</span><span class="sxs-lookup"><span data-stu-id="d6f8d-104">RtmDeregisterClient function</span></span>

<span data-ttu-id="d6f8d-105">\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。</span><span class="sxs-lookup"><span data-stu-id="d6f8d-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="d6f8d-106">應用程式應該使用路由表管理員第2版 API。\]</span><span class="sxs-lookup"><span data-stu-id="d6f8d-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="d6f8d-107">**RtmDeregisterClient** 函式會取消註冊用戶端，並釋出與用戶端相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="d6f8d-107">The **RtmDeregisterClient** function deregisters the client, and frees resources associated with the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6f8d-108">語法</span><span class="sxs-lookup"><span data-stu-id="d6f8d-108">Syntax</span></span>


```C++
DWORD RtmDeregisterClient(
  _In_ HANDLE ClientHandle
);
```



## <a name="parameters"></a><span data-ttu-id="d6f8d-109">參數</span><span class="sxs-lookup"><span data-stu-id="d6f8d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6f8d-110">*ClientHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d6f8d-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6f8d-111">識別要取消註冊之用戶端的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d6f8d-111">Handle that identifies the client to deregister.</span></span> <span data-ttu-id="d6f8d-112">藉由呼叫 [**RtmRegisterClient**](rtmregisterclient.md)來取得此控制碼。</span><span class="sxs-lookup"><span data-stu-id="d6f8d-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6f8d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6f8d-113">Return value</span></span>

<span data-ttu-id="d6f8d-114">如果函式成功，則傳回值不會是 \_ 錯誤。</span><span class="sxs-lookup"><span data-stu-id="d6f8d-114">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="d6f8d-115">如果函式失敗，則傳回值是下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d6f8d-115">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="d6f8d-116">值</span><span class="sxs-lookup"><span data-stu-id="d6f8d-116">Value</span></span>                                                                                                       | <span data-ttu-id="d6f8d-117">描述</span><span class="sxs-lookup"><span data-stu-id="d6f8d-117">Description</span></span>                                                    |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="d6f8d-118"><dt>**錯誤 \_ 不正確 \_ 控制碼**</dt></span><span class="sxs-lookup"><span data-stu-id="d6f8d-118"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="d6f8d-119">*ClientHandle* 參數不是有效的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d6f8d-119">The *ClientHandle* parameter is not a valid handle.</span></span><br/> |
| <dl> <span data-ttu-id="d6f8d-120"><dt>**錯誤 \_ 的 \_ 系統 \_ 資源**</dt></span><span class="sxs-lookup"><span data-stu-id="d6f8d-120"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="d6f8d-121">資源不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="d6f8d-121">Insufficient resources to carry out the operation.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="d6f8d-122">備註</span><span class="sxs-lookup"><span data-stu-id="d6f8d-122">Remarks</span></span>

<span data-ttu-id="d6f8d-123">此函式會移除用戶端新增的所有路由。</span><span class="sxs-lookup"><span data-stu-id="d6f8d-123">This function removes all routes that were added by the client.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6f8d-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6f8d-124">Requirements</span></span>



| <span data-ttu-id="d6f8d-125">需求</span><span class="sxs-lookup"><span data-stu-id="d6f8d-125">Requirement</span></span> | <span data-ttu-id="d6f8d-126">值</span><span class="sxs-lookup"><span data-stu-id="d6f8d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f8d-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d6f8d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d6f8d-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="d6f8d-128">None supported</span></span><br/>                                                          |
| <span data-ttu-id="d6f8d-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d6f8d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d6f8d-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6f8d-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d6f8d-131">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="d6f8d-131">End of server support</span></span><br/>    | <span data-ttu-id="d6f8d-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d6f8d-132">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="d6f8d-133">標頭</span><span class="sxs-lookup"><span data-stu-id="d6f8d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6f8d-134"><dt>Rtm. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6f8d-134"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="d6f8d-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="d6f8d-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="d6f8d-136"><dt>Rtm .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6f8d-136"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="d6f8d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="d6f8d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6f8d-138"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6f8d-138"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6f8d-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6f8d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6f8d-140">路由表管理員第1版參考</span><span class="sxs-lookup"><span data-stu-id="d6f8d-140">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="d6f8d-141">路由表管理員第1版函數</span><span class="sxs-lookup"><span data-stu-id="d6f8d-141">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="d6f8d-142">**RtmRegisterClient**</span><span class="sxs-lookup"><span data-stu-id="d6f8d-142">**RtmRegisterClient**</span></span>](rtmregisterclient.md)
</dt> </dl>

 

 





