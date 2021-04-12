---
title: 'UninitializeNapAgentNotifier 函式 (NapUtil) '
description: 從 NapAgent 狀態變更通知和隔離狀態變更通知取消訂閱呼叫的進程。
ms.assetid: b676ee33-caf6-48f0-acf8-5be1b23c62fe
keywords:
- UninitializeNapAgentNotifier 函數 NAP
topic_type:
- apiref
api_name:
- UninitializeNapAgentNotifier
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5d68b43fba64be82908d73803113f871b08c93c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384382"
---
# <a name="uninitializenapagentnotifier-function"></a><span data-ttu-id="c31be-104">UninitializeNapAgentNotifier 函式</span><span class="sxs-lookup"><span data-stu-id="c31be-104">UninitializeNapAgentNotifier function</span></span>

> [!Note]  
> <span data-ttu-id="c31be-105">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="c31be-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c31be-106">**UninitializeNapAgentNotifier** 函式會從 NapAgent 狀態變更通知和隔離狀態變更通知，取消訂閱呼叫的進程。</span><span class="sxs-lookup"><span data-stu-id="c31be-106">The **UninitializeNapAgentNotifier** function unsubscribes the calling process from NapAgent state change notifications and quarantine state change notifications.</span></span> <span data-ttu-id="c31be-107">這些通知是由 NapAgent 服務所提供。</span><span class="sxs-lookup"><span data-stu-id="c31be-107">These notifications are provided by the NapAgent service.</span></span>

## <a name="syntax"></a><span data-ttu-id="c31be-108">語法</span><span class="sxs-lookup"><span data-stu-id="c31be-108">Syntax</span></span>


```C++
NAPAPI VOID WINAPI UninitializeNapAgentNotifier(
  _In_ NapNotifyType type
);
```



## <a name="parameters"></a><span data-ttu-id="c31be-109">參數</span><span class="sxs-lookup"><span data-stu-id="c31be-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c31be-110">*類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c31be-110">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c31be-111">[**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype)值，指定要取消訂閱的服務通知類型。</span><span class="sxs-lookup"><span data-stu-id="c31be-111">A [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) value that specifies the type of service notifications to unsubscribe from.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c31be-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c31be-112">Return value</span></span>

<span data-ttu-id="c31be-113">此函數沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="c31be-113">This function has no return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="c31be-114">備註</span><span class="sxs-lookup"><span data-stu-id="c31be-114">Remarks</span></span>

<span data-ttu-id="c31be-115">此函式不是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="c31be-115">This function is not thread safe.</span></span>

<span data-ttu-id="c31be-116">每個訂閱 NapAgent 指定 *型* 別之服務通知的進程都必須呼叫 **UninitializeNapAgentNotifier** ，才能取消訂閱通知。</span><span class="sxs-lookup"><span data-stu-id="c31be-116">Each process subscribed to NapAgent service notifications of the specified *type* must call **UninitializeNapAgentNotifier** to unsubscribe from notifications.</span></span> <span data-ttu-id="c31be-117">如果有一或多個通知的處理常式，它必須針對每一種類型的通知呼叫 **UninitializeNapAgentNotifier** 一次。</span><span class="sxs-lookup"><span data-stu-id="c31be-117">If a process is subscribed to more than one type of notification, it must call **UninitializeNapAgentNotifier** once for each type of notification.</span></span>

<span data-ttu-id="c31be-118">如果進程先前未針對通知類型呼叫 [**InitializeNapAgentNotifier**](initializenapagentnotifier.md) ，此函式將會以無訊息模式失敗。</span><span class="sxs-lookup"><span data-stu-id="c31be-118">This function will fail silently if the process had not previously called [**InitializeNapAgentNotifier**](initializenapagentnotifier.md) for the notification type.</span></span>

## <a name="requirements"></a><span data-ttu-id="c31be-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c31be-119">Requirements</span></span>



| <span data-ttu-id="c31be-120">需求</span><span class="sxs-lookup"><span data-stu-id="c31be-120">Requirement</span></span> | <span data-ttu-id="c31be-121">值</span><span class="sxs-lookup"><span data-stu-id="c31be-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c31be-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c31be-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c31be-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c31be-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c31be-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c31be-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c31be-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c31be-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c31be-126">標頭</span><span class="sxs-lookup"><span data-stu-id="c31be-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c31be-127"><dt>NapUtil。h</dt></span><span class="sxs-lookup"><span data-stu-id="c31be-127"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="c31be-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c31be-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c31be-129"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c31be-129"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c31be-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c31be-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c31be-131">**InitializeNapAgentNotifier**</span><span class="sxs-lookup"><span data-stu-id="c31be-131">**InitializeNapAgentNotifier**</span></span>](initializenapagentnotifier.md)
</dt> </dl>

 

 





