---
title: 'RtmGetNetworkCount 函式 (Rtm. h) '
description: RtmGetNetworkCount 函式會抓取路由表管理員已路由傳送的網路數目。
ms.assetid: d0c04b8d-a6c4-44bf-a3f2-de822d635131
keywords:
- RtmGetNetworkCount 函式 RAS
topic_type:
- apiref
api_name:
- RtmGetNetworkCount
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eab4babd1e9d98071b2fbe6ab30c9b92d4a23f0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685885"
---
# <a name="rtmgetnetworkcount-function"></a><span data-ttu-id="9990d-104">RtmGetNetworkCount 函式</span><span class="sxs-lookup"><span data-stu-id="9990d-104">RtmGetNetworkCount function</span></span>

<span data-ttu-id="9990d-105">\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。</span><span class="sxs-lookup"><span data-stu-id="9990d-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="9990d-106">應用程式應該使用路由表管理員第2版 API。\]</span><span class="sxs-lookup"><span data-stu-id="9990d-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="9990d-107">**RtmGetNetworkCount** 函式會抓取路由表管理員已路由傳送的網路數目。</span><span class="sxs-lookup"><span data-stu-id="9990d-107">The **RtmGetNetworkCount** function retrieves the number of networks to which the routing table manager has routes.</span></span>

## <a name="syntax"></a><span data-ttu-id="9990d-108">語法</span><span class="sxs-lookup"><span data-stu-id="9990d-108">Syntax</span></span>


```C++
ULONG RtmGetNetworkCount(
  _In_ DWORD ProtocolFamily
);
```



## <a name="parameters"></a><span data-ttu-id="9990d-109">參數</span><span class="sxs-lookup"><span data-stu-id="9990d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9990d-110">*ProtocolFamily* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9990d-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9990d-111">指定要取得路由資訊的網路類型，例如 IP 或 IPX。</span><span class="sxs-lookup"><span data-stu-id="9990d-111">Specifies for which type of network to obtain route information, for example, IP or IPX.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9990d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="9990d-112">Return value</span></span>

<span data-ttu-id="9990d-113">如果函式成功，則傳回值是網路計數，也就是指定之通訊協定系列的路由通訊協定所知道的網路數目。</span><span class="sxs-lookup"><span data-stu-id="9990d-113">If the function succeeds, the return value is the network count, the number of networks known to the routing protocols of the specified protocol family.</span></span>

<span data-ttu-id="9990d-114">如果傳回值為零，表示沒有可用的路由，或作業失敗。</span><span class="sxs-lookup"><span data-stu-id="9990d-114">If the return value is zero, either no routes are available, or the operation failed.</span></span> <span data-ttu-id="9990d-115">呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 以取得詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="9990d-115">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain more information.</span></span>



| <span data-ttu-id="9990d-116">值</span><span class="sxs-lookup"><span data-stu-id="9990d-116">Value</span></span>                                                                                                    | <span data-ttu-id="9990d-117">描述</span><span class="sxs-lookup"><span data-stu-id="9990d-117">Description</span></span>                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9990d-118"><dt>**沒有 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="9990d-118"><dt>**NO\_ERROR**</dt></span></span> </dl>                 | <span data-ttu-id="9990d-119">作業成功，但沒有可用的路由。</span><span class="sxs-lookup"><span data-stu-id="9990d-119">The operation succeeded, but no routes are available.</span></span><br/>                                             |
| <dl> <span data-ttu-id="9990d-120"><dt>**錯誤 \_ 不正確 \_ 參數**</dt></span><span class="sxs-lookup"><span data-stu-id="9990d-120"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="9990d-121">*ProtocolFamily* 參數的值未對應到任何已安裝的通訊協定系列。</span><span class="sxs-lookup"><span data-stu-id="9990d-121">The value of the *ProtocolFamily* parameter does not correspond to any installed protocol family.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9990d-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="9990d-122">Requirements</span></span>



| <span data-ttu-id="9990d-123">需求</span><span class="sxs-lookup"><span data-stu-id="9990d-123">Requirement</span></span> | <span data-ttu-id="9990d-124">值</span><span class="sxs-lookup"><span data-stu-id="9990d-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9990d-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9990d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9990d-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="9990d-126">None supported</span></span><br/>                                                          |
| <span data-ttu-id="9990d-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9990d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9990d-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9990d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9990d-129">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="9990d-129">End of server support</span></span><br/>    | <span data-ttu-id="9990d-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9990d-130">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="9990d-131">標頭</span><span class="sxs-lookup"><span data-stu-id="9990d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9990d-132"><dt>Rtm. h</dt></span><span class="sxs-lookup"><span data-stu-id="9990d-132"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="9990d-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="9990d-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="9990d-134"><dt>Rtm .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9990d-134"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="9990d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9990d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9990d-136"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9990d-136"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9990d-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9990d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9990d-138">路由表管理員第1版參考</span><span class="sxs-lookup"><span data-stu-id="9990d-138">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="9990d-139">路由表管理員第1版函數</span><span class="sxs-lookup"><span data-stu-id="9990d-139">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

<span data-ttu-id="9990d-140">[**3]。Getlasterror**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)</span><span class="sxs-lookup"><span data-stu-id="9990d-140">[**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)</span></span>
</dt> <dt>

[<span data-ttu-id="9990d-141">RTMv1 通訊協定系列識別碼</span><span class="sxs-lookup"><span data-stu-id="9990d-141">RTMv1 Protocol Family Identifiers</span></span>](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

