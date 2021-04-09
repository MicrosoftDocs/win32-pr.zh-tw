---
title: 'InitializeNapAgentNotifier 函式 (NapUtil) '
description: 訂閱呼叫進程以 NapAgent 狀態變更通知和隔離狀態變更通知。
ms.assetid: 24180194-50d7-4f54-845d-25402af9cf9a
keywords:
- InitializeNapAgentNotifier 函數 NAP
topic_type:
- apiref
api_name:
- InitializeNapAgentNotifier
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f59c4c342f693038040f374bbdbcdb8ab226f74d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934159"
---
# <a name="initializenapagentnotifier-function"></a><span data-ttu-id="0e13f-104">InitializeNapAgentNotifier 函式</span><span class="sxs-lookup"><span data-stu-id="0e13f-104">InitializeNapAgentNotifier function</span></span>

> [!Note]  
> <span data-ttu-id="0e13f-105">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="0e13f-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0e13f-106">**InitializeNapAgentNotifier** 函式會訂閱呼叫進程，以 NapAgent 狀態變更通知和隔離狀態變更通知。</span><span class="sxs-lookup"><span data-stu-id="0e13f-106">The **InitializeNapAgentNotifier** function subscribes the calling process to NapAgent state change notifications and quarantine state change notifications.</span></span> <span data-ttu-id="0e13f-107">這些通知是由 NapAgent 服務所提供。</span><span class="sxs-lookup"><span data-stu-id="0e13f-107">These notifications are provided by the NapAgent service.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e13f-108">語法</span><span class="sxs-lookup"><span data-stu-id="0e13f-108">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI InitializeNapAgentNotifier(
  _In_ NapNotifyType type,
  _In_ HANDLE        hNotifyEvent
);
```



## <a name="parameters"></a><span data-ttu-id="0e13f-109">參數</span><span class="sxs-lookup"><span data-stu-id="0e13f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e13f-110">*類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0e13f-110">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e13f-111">[**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype)值，指定要接收的服務通知類型。</span><span class="sxs-lookup"><span data-stu-id="0e13f-111">A [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) value that specifies the type of service notifications to receive.</span></span>

</dd> <dt>

<span data-ttu-id="0e13f-112">*hNotifyEvent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0e13f-112">*hNotifyEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e13f-113">用於通知的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="0e13f-113">An event handle used for notification.</span></span> <span data-ttu-id="0e13f-114">呼叫端必須將開啟的控制碼傳遞給 *hNotifyEvent* 參數。</span><span class="sxs-lookup"><span data-stu-id="0e13f-114">The caller must pass an open handle to the *hNotifyEvent* parameter.</span></span> <span data-ttu-id="0e13f-115">當不再需要時，呼叫端也必須關閉事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="0e13f-115">The caller must also close the event handle when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e13f-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="0e13f-116">Return value</span></span>



| <span data-ttu-id="0e13f-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0e13f-117">Return code</span></span>                                                                                                | <span data-ttu-id="0e13f-118">Description</span><span class="sxs-lookup"><span data-stu-id="0e13f-118">Description</span></span>                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0e13f-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0e13f-119"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="0e13f-120">初始化已順利完成。</span><span class="sxs-lookup"><span data-stu-id="0e13f-120">Initialization completed successfully.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="0e13f-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="0e13f-121"><dt>**E\_FAIL**</dt></span></span> </dl>                     | <span data-ttu-id="0e13f-122">初始化失敗。</span><span class="sxs-lookup"><span data-stu-id="0e13f-122">Initialization failed.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="0e13f-123"><dt>**錯誤 \_ 已 \_ 初始化**</dt></span><span class="sxs-lookup"><span data-stu-id="0e13f-123"><dt>**ERROR\_ALREADY\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="0e13f-124">此處理程式已訂閱指定之 *類型* 的 NapAgent 服務通知。</span><span class="sxs-lookup"><span data-stu-id="0e13f-124">The process has already subscribed to NapAgent service notifications of the *type* specified.</span></span> <br/> |
| <dl> <span data-ttu-id="0e13f-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0e13f-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="0e13f-126">傳遞了無效的引數。</span><span class="sxs-lookup"><span data-stu-id="0e13f-126">An invalid argument was passed.</span></span> <br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="0e13f-127">備註</span><span class="sxs-lookup"><span data-stu-id="0e13f-127">Remarks</span></span>

<span data-ttu-id="0e13f-128">此函式不是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="0e13f-128">This function is not thread safe.</span></span>

<span data-ttu-id="0e13f-129">需要訂用帳戶才能 NapAgent 指定 *類型* 之服務通知的每個處理常式，都必須呼叫 **InitializeNapAgentNotifier** 來訂閱通知。</span><span class="sxs-lookup"><span data-stu-id="0e13f-129">Each process that requires a subscription to NapAgent service notifications of the specified *type* must call **InitializeNapAgentNotifier** to subscribe to notifications.</span></span> <span data-ttu-id="0e13f-130">如果處理常式必須訂閱一種以上的通知類型，則必須針對每一種類型的通知呼叫 **InitializeNapAgentNotifier** 一次。</span><span class="sxs-lookup"><span data-stu-id="0e13f-130">If a process must subscribe to more than one type of notification, it must call **InitializeNapAgentNotifier** once for each type of notification.</span></span>

<span data-ttu-id="0e13f-131">一旦進程不需要進一步的通知，處理常式就必須針對指定的 *型* 別呼叫 [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md) 。</span><span class="sxs-lookup"><span data-stu-id="0e13f-131">Once a process does not require further notifications, the process must call [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md) for the specified *type*.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e13f-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e13f-132">Requirements</span></span>



| <span data-ttu-id="0e13f-133">需求</span><span class="sxs-lookup"><span data-stu-id="0e13f-133">Requirement</span></span> | <span data-ttu-id="0e13f-134">值</span><span class="sxs-lookup"><span data-stu-id="0e13f-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0e13f-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0e13f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0e13f-136">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e13f-136">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0e13f-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0e13f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0e13f-138">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e13f-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0e13f-139">標頭</span><span class="sxs-lookup"><span data-stu-id="0e13f-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e13f-140"><dt>NapUtil。h</dt></span><span class="sxs-lookup"><span data-stu-id="0e13f-140"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="0e13f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0e13f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e13f-142"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e13f-142"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e13f-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e13f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e13f-144">**UninitializeNapAgentNotifier**</span><span class="sxs-lookup"><span data-stu-id="0e13f-144">**UninitializeNapAgentNotifier**</span></span>](uninitializenapagentnotifier.md)
</dt> </dl>

 

 





