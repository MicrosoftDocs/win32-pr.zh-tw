---
description: 使用回呼函式訂閱服務狀態變更通知。
ms.assetid: d67113eb-2141-444c-9f09-eaa772bcad8a
title: 'SubscribeServiceChangeNotifications 函式 (Winsvcp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscribeServiceChangeNotifications
api_type:
- DllExport
api_location:
- SecHost.dll
- API-MS-Win-Service-Private-L1-1-0.dll
- API-MS-Win-Service-Private-L1-1-1.dll
- Advapi32.dll
- API-MS-Win-Service-Private-L1-1-2.dll
ms.openlocfilehash: e327a44d613b514123862b1ddcb1bf302fea63ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990372"
---
# <a name="subscribeservicechangenotifications-function"></a><span data-ttu-id="91166-103">SubscribeServiceChangeNotifications 函式</span><span class="sxs-lookup"><span data-stu-id="91166-103">SubscribeServiceChangeNotifications function</span></span>

<span data-ttu-id="91166-104">使用回呼函式訂閱服務狀態變更通知。</span><span class="sxs-lookup"><span data-stu-id="91166-104">Subscribes for service status change notifications using a callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="91166-105">語法</span><span class="sxs-lookup"><span data-stu-id="91166-105">Syntax</span></span>


```C++
DWORD WINAPI SubscribeServiceChangeNotifications(
  _In_     SC_HANDLE                     hService,
  _In_     SC_EVENT_TYPE                 eEventType,
  _In_     PSC_NOTIFICATION_CALLBACK     pCallback,
  _In_opt_ PVOID                         pCallbackContext,
  _Out_    PSC_NOTIFICATION_REGISTRATION *pSubscription
);
```



## <a name="parameters"></a><span data-ttu-id="91166-106">參數</span><span class="sxs-lookup"><span data-stu-id="91166-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91166-107">*hService* \[在\]</span><span class="sxs-lookup"><span data-stu-id="91166-107">*hService* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91166-108">服務的控制碼或服務控制管理員的控制碼 (SCM) 來監視變更。</span><span class="sxs-lookup"><span data-stu-id="91166-108">A handle to the service or a handle to the service control manager (SCM) to monitor for changes.</span></span>

<span data-ttu-id="91166-109">[**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)和 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)函式會傳回服務的控制碼，而且必須要有 **服務 \_ 查詢 \_ 狀態** 存取權限。</span><span class="sxs-lookup"><span data-stu-id="91166-109">Handles to services are returned by the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) and [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function and must have the **SERVICE\_QUERY\_STATUS** access right.</span></span> <span data-ttu-id="91166-110">[**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)函式會傳回服務控制管理員的控制碼，而且必須具有 **SC \_ 管理員 \_ 列舉 \_ 服務** 存取權限。</span><span class="sxs-lookup"><span data-stu-id="91166-110">Handles to the service control manager are returned by the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function and must have the **SC\_MANAGER\_ENUMERATE\_SERVICE** access right.</span></span>

</dd> <dt>

<span data-ttu-id="91166-111">*eEventType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="91166-111">*eEventType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91166-112">指定應回報的狀態變更類型。</span><span class="sxs-lookup"><span data-stu-id="91166-112">Specifies the type of status changes that should be reported.</span></span> <span data-ttu-id="91166-113">此參數會設定為 [**SC \_ 事件 \_ 類型**](sc-event-type.md)中指定的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="91166-113">This parameter is set to one of the values specified in [**SC\_EVENT\_TYPE**](sc-event-type.md).</span></span> <span data-ttu-id="91166-114">根據事件種類而定，此函式的行為會有所不同，如下所示。</span><span class="sxs-lookup"><span data-stu-id="91166-114">The behavior for this function is different depending on the event type as follows.</span></span>



| <span data-ttu-id="91166-115">值</span><span class="sxs-lookup"><span data-stu-id="91166-115">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="91166-116">意義</span><span class="sxs-lookup"><span data-stu-id="91166-116">Meaning</span></span>                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span><dl> <span data-ttu-id="91166-117"><dt>**SC \_事件 \_ 資料庫 \_ 變更**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="91166-117"><dt>**SC\_EVENT\_DATABASE\_CHANGE**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="91166-118">已新增或刪除服務。</span><span class="sxs-lookup"><span data-stu-id="91166-118">A service has been added or deleted.</span></span> <span data-ttu-id="91166-119">*HService* 參數必須是 SCM 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="91166-119">The *hService* parameter must be a handle to the SCM.</span></span><br/>                  |
| <span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span><dl> <span data-ttu-id="91166-120"><dt>**SC \_事件 \_ 屬性 \_ 變更**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="91166-120"><dt>**SC\_EVENT\_PROPERTY\_CHANGE**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="91166-121">已更新一或多個服務屬性。</span><span class="sxs-lookup"><span data-stu-id="91166-121">One or more service properties have been updated.</span></span> <span data-ttu-id="91166-122">*HService* 參數必須是服務的控制碼。</span><span class="sxs-lookup"><span data-stu-id="91166-122">The *hService* parameter must be a handle to the service.</span></span><br/> |
| <span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span><dl> <span data-ttu-id="91166-123"><dt>**SC \_事件 \_ 狀態 \_ 變更**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="91166-123"><dt>**SC\_EVENT\_STATUS\_CHANGE**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="91166-124">服務的狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="91166-124">The status of a service has changed.</span></span> <span data-ttu-id="91166-125">*HService* 參數必須是服務的控制碼。</span><span class="sxs-lookup"><span data-stu-id="91166-125">The *hService* parameter must be a handle to the service.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="91166-126">*pCallback* \[在\]</span><span class="sxs-lookup"><span data-stu-id="91166-126">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91166-127">指定回呼函數。</span><span class="sxs-lookup"><span data-stu-id="91166-127">Specifies the callback function.</span></span> <span data-ttu-id="91166-128">回呼必須定義為具有 **SC \_ 通知 \_ 回呼** 的類型。</span><span class="sxs-lookup"><span data-stu-id="91166-128">The callback must be defined as having a type of **SC\_NOTIFICATION\_CALLBACK**.</span></span> <span data-ttu-id="91166-129">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="91166-129">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="91166-130">*pCallbackCoNtext* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="91166-130">*pCallbackContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="91166-131">表示此通知回呼內容的指標。</span><span class="sxs-lookup"><span data-stu-id="91166-131">A pointer representing the context for this notification callback.</span></span>

</dd> <dt>

<span data-ttu-id="91166-132">*pSubscription* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="91166-132">*pSubscription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91166-133">傳回通知回呼註冊所產生之訂用帳戶的指標。</span><span class="sxs-lookup"><span data-stu-id="91166-133">Returns a pointer to the subscription resulting from the notification callback registration.</span></span> <span data-ttu-id="91166-134">呼叫端會負責呼叫 [**UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md) ，以停止接收通知。</span><span class="sxs-lookup"><span data-stu-id="91166-134">The caller is responsible for calling [**UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md) to stop receiving notifications.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91166-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="91166-135">Return value</span></span>

<span data-ttu-id="91166-136">如果函式成功，則傳回值為「 **錯誤 \_ 成功**」。</span><span class="sxs-lookup"><span data-stu-id="91166-136">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span>

<span data-ttu-id="91166-137">如果函式失敗，則傳回值是其中一個 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="91166-137">If the function fails, the return value is one of the [system error codes](/windows/desktop/Debug/system-error-codes).</span></span>

## <a name="remarks"></a><span data-ttu-id="91166-138">備註</span><span class="sxs-lookup"><span data-stu-id="91166-138">Remarks</span></span>

<span data-ttu-id="91166-139">回呼函數的宣告方式如下：</span><span class="sxs-lookup"><span data-stu-id="91166-139">The callback function is declared as follows:</span></span>


```C++
typedef VOID CALLBACK SC_NOTIFICATION_CALLBACK(
    _In_    DWORD                   dwNotify,
    _In_    PVOID                   pCallbackContext
);
typedef SC_NOTIFICATION_CALLBACK* PSC_NOTIFICATION_CALLBACK;
```



<span data-ttu-id="91166-140">回呼函式會接收呼叫端所提供內容的指標。</span><span class="sxs-lookup"><span data-stu-id="91166-140">The callback function receives a pointer to the context provided by the caller.</span></span> <span data-ttu-id="91166-141">由於服務狀態變更事件，會叫用回呼。</span><span class="sxs-lookup"><span data-stu-id="91166-141">The callback is invoked as a result of the service status change event.</span></span> <span data-ttu-id="91166-142">叫用回呼時，會提供 **服務 \_ 通知 \_ \* XXX**\* 值的位元遮罩，指出服務狀態變更的類型。</span><span class="sxs-lookup"><span data-stu-id="91166-142">When the callback is invoked, it is provided with a bitmask of **SERVICE\_NOTIFY\_\*XXX**\* values that indicating the type of service status change.</span></span> <span data-ttu-id="91166-143">以零（而不是有效的 **服務 \_ 通知 \_ \* XXX**\* 值）提供回呼時，應用程式必須確認變更了哪些內容。</span><span class="sxs-lookup"><span data-stu-id="91166-143">When the callback is provided with zero instead of a valid **SERVICE\_NOTIFY\_\*XXX**\* value, the application must verify what was changed.</span></span>

<span data-ttu-id="91166-144">回呼函數不能封鎖執行。</span><span class="sxs-lookup"><span data-stu-id="91166-144">The callback function must not block execution.</span></span> <span data-ttu-id="91166-145">如果您預期執行回呼函式需要一些時間，請將工作專案排入執行緒集區中的執行緒，以將回呼函式中執行的工作卸載至個別的執行緒。</span><span class="sxs-lookup"><span data-stu-id="91166-145">If you expect the execution of the callback function to take time, offload the work that you perform in the callback function to a separate thread by queuing a work item to a thread in a thread pool.</span></span> <span data-ttu-id="91166-146">某些可讓回呼函數執行的工作類型包括執行檔案 i/o、等候事件，以及進行外部遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="91166-146">Some types of work that can make the callback function take time include performing file I/O, waiting on an event, and making external remote procedure calls.</span></span>

## <a name="requirements"></a><span data-ttu-id="91166-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="91166-147">Requirements</span></span>



| <span data-ttu-id="91166-148">需求</span><span class="sxs-lookup"><span data-stu-id="91166-148">Requirement</span></span> | <span data-ttu-id="91166-149">值</span><span class="sxs-lookup"><span data-stu-id="91166-149">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="91166-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="91166-150">Minimum supported client</span></span><br/> | <span data-ttu-id="91166-151">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91166-151">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="91166-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="91166-152">Minimum supported server</span></span><br/> | <span data-ttu-id="91166-153">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91166-153">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="91166-154">標頭</span><span class="sxs-lookup"><span data-stu-id="91166-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="91166-155"><dt>Winsvcp。h</dt></span><span class="sxs-lookup"><span data-stu-id="91166-155"><dt>Winsvcp.h</dt></span></span> </dl>   |
| <span data-ttu-id="91166-156">DLL</span><span class="sxs-lookup"><span data-stu-id="91166-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91166-157"><dt>SecHost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91166-157"><dt>SecHost.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91166-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91166-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91166-159">**CreateService**</span><span class="sxs-lookup"><span data-stu-id="91166-159">**CreateService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)
</dt> <dt>

[<span data-ttu-id="91166-160">**OpenService**</span><span class="sxs-lookup"><span data-stu-id="91166-160">**OpenService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)
</dt> <dt>

[<span data-ttu-id="91166-161">**OpenSCManager**</span><span class="sxs-lookup"><span data-stu-id="91166-161">**OpenSCManager**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)
</dt> <dt>

[<span data-ttu-id="91166-162">**UnsubscribeServiceChangeNotifications**</span><span class="sxs-lookup"><span data-stu-id="91166-162">**UnsubscribeServiceChangeNotifications**</span></span>](unsubscribeservicechangenotifications.md)
</dt> <dt>

[<span data-ttu-id="91166-163">**QueryServiceDynamicInformation**</span><span class="sxs-lookup"><span data-stu-id="91166-163">**QueryServiceDynamicInformation**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

