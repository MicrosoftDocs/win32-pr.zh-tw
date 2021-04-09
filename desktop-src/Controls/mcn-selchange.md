---
title: 'MCN_SELCHANGE (Commctrl 的通知碼) '
description: 月曆控制項在目前選取日期或日期範圍變更時傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 8923524f-d257-409d-bd3e-021684b88856
keywords:
- MCN_SELCHANGE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- MCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffa328ca0173afd3a577f6cf14e0204cd5c0f7d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024728"
---
# <a name="mcn_selchange-notification-code"></a><span data-ttu-id="acd61-105">MCN \_ SELCHANGE 通知碼</span><span class="sxs-lookup"><span data-stu-id="acd61-105">MCN\_SELCHANGE notification code</span></span>

<span data-ttu-id="acd61-106">月曆控制項在目前選取日期或日期範圍變更時傳送。</span><span class="sxs-lookup"><span data-stu-id="acd61-106">Sent by a month calendar control when the currently selected date or range of dates changes.</span></span> <span data-ttu-id="acd61-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="acd61-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_SELCHANGE

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="acd61-108">參數</span><span class="sxs-lookup"><span data-stu-id="acd61-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acd61-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="acd61-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="acd61-110">[**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange)結構的指標，其中包含目前所選取日期範圍的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="acd61-110">Pointer to an [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) structure that contains information about the currently selected date range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acd61-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="acd61-111">Return value</span></span>

<span data-ttu-id="acd61-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="acd61-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="acd61-113">備註</span><span class="sxs-lookup"><span data-stu-id="acd61-113">Remarks</span></span>

<span data-ttu-id="acd61-114">例如， \_ 當使用者在目前月份內明確變更選取範圍，或在回應下一個/上一個月導覽時，以隱含方式變更選取範圍時，控制項會傳送 MCN SELCHANGE。</span><span class="sxs-lookup"><span data-stu-id="acd61-114">For example, the control sends MCN\_SELCHANGE when the user explicitly changes the selection within the current month or when the selection is implicitly changed in response to next/previous month navigation.</span></span> <span data-ttu-id="acd61-115">系統也會定期傳送此通知碼，讓控制項可以回應日期變更。</span><span class="sxs-lookup"><span data-stu-id="acd61-115">This notification code is also sent by the system at regular intervals so that the control can respond to date changes.</span></span>

<span data-ttu-id="acd61-116">此通知碼類似于 [MCN \_ SELECT](mcn-select.md)，但會傳送以回應任何選取專案的變更。</span><span class="sxs-lookup"><span data-stu-id="acd61-116">This notification code is similar to [MCN\_SELECT](mcn-select.md), but it is sent in response to any selection change.</span></span> <span data-ttu-id="acd61-117">MCN \_ SELECT 只傳送給明確的日期選擇。</span><span class="sxs-lookup"><span data-stu-id="acd61-117">MCN\_SELECT is sent only for an explicit date selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="acd61-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="acd61-118">Requirements</span></span>



| <span data-ttu-id="acd61-119">需求</span><span class="sxs-lookup"><span data-stu-id="acd61-119">Requirement</span></span> | <span data-ttu-id="acd61-120">值</span><span class="sxs-lookup"><span data-stu-id="acd61-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="acd61-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="acd61-121">Minimum supported client</span></span><br/> | <span data-ttu-id="acd61-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="acd61-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="acd61-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="acd61-123">Minimum supported server</span></span><br/> | <span data-ttu-id="acd61-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="acd61-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="acd61-125">標頭</span><span class="sxs-lookup"><span data-stu-id="acd61-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="acd61-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="acd61-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





