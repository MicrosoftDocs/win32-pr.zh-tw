---
title: 'RtmCloseEnumerationHandle 函式 (Rtm. h) '
description: RtmCloseEnumerationHandle 會終止指定的列舉，並釋出相關聯的資源。
ms.assetid: 8daea42f-4304-4749-9894-d37f6ba733da
keywords:
- RtmCloseEnumerationHandle 函式 RAS
topic_type:
- apiref
api_name:
- RtmCloseEnumerationHandle
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5adb47d40cb1300305c7ff6f9bb6f1c3c716f0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025241"
---
# <a name="rtmcloseenumerationhandle-function"></a><span data-ttu-id="a9d02-104">RtmCloseEnumerationHandle 函式</span><span class="sxs-lookup"><span data-stu-id="a9d02-104">RtmCloseEnumerationHandle function</span></span>

<span data-ttu-id="a9d02-105">\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。</span><span class="sxs-lookup"><span data-stu-id="a9d02-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="a9d02-106">應用程式應該使用路由表管理員第2版 API。\]</span><span class="sxs-lookup"><span data-stu-id="a9d02-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="a9d02-107">**RtmCloseEnumerationHandle** 會終止指定的列舉，並釋出相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="a9d02-107">The **RtmCloseEnumerationHandle** terminates a specified enumeration and frees the associated resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9d02-108">語法</span><span class="sxs-lookup"><span data-stu-id="a9d02-108">Syntax</span></span>


```C++
DWORD RtmCloseEnumerationHandle(
  _In_ HANDLE EnumerationHandle
);
```



## <a name="parameters"></a><span data-ttu-id="a9d02-109">參數</span><span class="sxs-lookup"><span data-stu-id="a9d02-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9d02-110">*EnumerationHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a9d02-110">*EnumerationHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d02-111">要終止之列舉的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a9d02-111">Handle to the enumeration to terminate.</span></span> <span data-ttu-id="a9d02-112">藉由呼叫 [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)來取得此控制碼。</span><span class="sxs-lookup"><span data-stu-id="a9d02-112">Obtain this handle by calling [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9d02-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a9d02-113">Return value</span></span>

<span data-ttu-id="a9d02-114">如果函式成功，則傳回值不會是 \_ 錯誤。</span><span class="sxs-lookup"><span data-stu-id="a9d02-114">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="a9d02-115">如果函式失敗，則傳回值是下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a9d02-115">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="a9d02-116">值</span><span class="sxs-lookup"><span data-stu-id="a9d02-116">Value</span></span>                                                                                                       | <span data-ttu-id="a9d02-117">描述</span><span class="sxs-lookup"><span data-stu-id="a9d02-117">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a9d02-118"><dt>**錯誤 \_ 不正確 \_ 控制碼**</dt></span><span class="sxs-lookup"><span data-stu-id="a9d02-118"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="a9d02-119">參數無效。</span><span class="sxs-lookup"><span data-stu-id="a9d02-119">The parameter is not valid.</span></span><br/>                                  |
| <dl> <span data-ttu-id="a9d02-120"><dt>**錯誤 \_ 的 \_ 系統 \_ 資源**</dt></span><span class="sxs-lookup"><span data-stu-id="a9d02-120"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="a9d02-121">資源不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="a9d02-121">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a9d02-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9d02-122">Requirements</span></span>



| <span data-ttu-id="a9d02-123">需求</span><span class="sxs-lookup"><span data-stu-id="a9d02-123">Requirement</span></span> | <span data-ttu-id="a9d02-124">值</span><span class="sxs-lookup"><span data-stu-id="a9d02-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a9d02-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a9d02-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a9d02-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="a9d02-126">None supported</span></span><br/>                                                          |
| <span data-ttu-id="a9d02-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a9d02-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a9d02-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9d02-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a9d02-129">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="a9d02-129">End of server support</span></span><br/>    | <span data-ttu-id="a9d02-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a9d02-130">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="a9d02-131">標頭</span><span class="sxs-lookup"><span data-stu-id="a9d02-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9d02-132"><dt>Rtm. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9d02-132"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="a9d02-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="a9d02-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="a9d02-134"><dt>Rtm .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9d02-134"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="a9d02-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a9d02-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9d02-136"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9d02-136"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9d02-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9d02-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9d02-138">路由表管理員第1版參考</span><span class="sxs-lookup"><span data-stu-id="a9d02-138">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="a9d02-139">路由表管理員第1版函數</span><span class="sxs-lookup"><span data-stu-id="a9d02-139">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="a9d02-140">**RtmCreateEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="a9d02-140">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="a9d02-141">**RtmEnumerateGetNextRoute**</span><span class="sxs-lookup"><span data-stu-id="a9d02-141">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> </dl>

 

 





