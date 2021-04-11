---
description: 取消訂閱服務狀態變更通知。
ms.assetid: 8c04ebf7-4d61-4617-b120-dbe26b2f9ad2
title: 'UnsubscribeServiceChangeNotifications 函式 (Winsvcp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnsubscribeServiceChangeNotifications
api_type:
- DllExport
api_location:
- SecHost.dll
- API-MS-Win-Service-Private-L1-1-0.dll
- API-MS-Win-Service-Private-L1-1-1.dll
- Advapi32.dll
- API-MS-Win-Service-Private-L1-1-2.dll
ms.openlocfilehash: ebecfb133172c9c7a56ed6d28f7ad6b395d8afce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850511"
---
# <a name="unsubscribeservicechangenotifications-function"></a><span data-ttu-id="d4a18-103">UnsubscribeServiceChangeNotifications 函式</span><span class="sxs-lookup"><span data-stu-id="d4a18-103">UnsubscribeServiceChangeNotifications function</span></span>

<span data-ttu-id="d4a18-104">取消訂閱服務狀態變更通知。</span><span class="sxs-lookup"><span data-stu-id="d4a18-104">Unsubscribes from service status change notifications.</span></span> <span data-ttu-id="d4a18-105">此函數會使用 [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md)傳回的訂閱。</span><span class="sxs-lookup"><span data-stu-id="d4a18-105">This function uses subscriptions returned by [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d4a18-106">語法</span><span class="sxs-lookup"><span data-stu-id="d4a18-106">Syntax</span></span>


```C++
 VOID WINAPI UnsubscribeServiceChangeNotifications(
  _In_ PSC_NOTIFICATION_REGISTRATION pSubscription
);
```



## <a name="parameters"></a><span data-ttu-id="d4a18-107">參數</span><span class="sxs-lookup"><span data-stu-id="d4a18-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4a18-108">*pSubscription* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d4a18-108">*pSubscription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4a18-109">要取消訂閱之訂用帳戶的指標。</span><span class="sxs-lookup"><span data-stu-id="d4a18-109">A pointer to the subscription to be unsubscribed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4a18-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="d4a18-110">Return value</span></span>

<span data-ttu-id="d4a18-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d4a18-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4a18-112">備註</span><span class="sxs-lookup"><span data-stu-id="d4a18-112">Remarks</span></span>

<span data-ttu-id="d4a18-113">在完成的同進程回呼完成之前， **UnsubscribeServiceChangeNotifications** 不會傳回。</span><span class="sxs-lookup"><span data-stu-id="d4a18-113">**UnsubscribeServiceChangeNotifications** does not return until outstanding in-process callbacks are complete.</span></span> <span data-ttu-id="d4a18-114">因此，您無法在回呼內呼叫 **UnsubscribeServiceChangeNotifications** ，而不會造成鎖死。</span><span class="sxs-lookup"><span data-stu-id="d4a18-114">So, you cannot call **UnsubscribeServiceChangeNotifications** within the callback without causing a deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4a18-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4a18-115">Requirements</span></span>



| <span data-ttu-id="d4a18-116">需求</span><span class="sxs-lookup"><span data-stu-id="d4a18-116">Requirement</span></span> | <span data-ttu-id="d4a18-117">值</span><span class="sxs-lookup"><span data-stu-id="d4a18-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4a18-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d4a18-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d4a18-119">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4a18-119">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d4a18-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d4a18-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d4a18-121">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4a18-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d4a18-122">標頭</span><span class="sxs-lookup"><span data-stu-id="d4a18-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4a18-123"><dt>Winsvcp。h</dt></span><span class="sxs-lookup"><span data-stu-id="d4a18-123"><dt>Winsvcp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4a18-124">DLL</span><span class="sxs-lookup"><span data-stu-id="d4a18-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4a18-125"><dt>SecHost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4a18-125"><dt>SecHost.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4a18-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4a18-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4a18-127">**CreateService**</span><span class="sxs-lookup"><span data-stu-id="d4a18-127">**CreateService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)
</dt> <dt>

[<span data-ttu-id="d4a18-128">**OpenService**</span><span class="sxs-lookup"><span data-stu-id="d4a18-128">**OpenService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)
</dt> <dt>

[<span data-ttu-id="d4a18-129">**OpenSCManager**</span><span class="sxs-lookup"><span data-stu-id="d4a18-129">**OpenSCManager**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)
</dt> <dt>

[<span data-ttu-id="d4a18-130">**SubscribeServiceChangeNotifications**</span><span class="sxs-lookup"><span data-stu-id="d4a18-130">**SubscribeServiceChangeNotifications**</span></span>](subscribeservicechangenotifications.md)
</dt> <dt>

[<span data-ttu-id="d4a18-131">**QueryServiceDynamicInformation**</span><span class="sxs-lookup"><span data-stu-id="d4a18-131">**QueryServiceDynamicInformation**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

 




