---
title: 'DTN_WMKEYDOWN (Commctrl 的通知碼) '
description: 當使用者在回呼欄位中輸入時，日期和時間選擇器會傳送 (DTP) 控制項。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: e67e222d-28a1-4d30-ae64-8ec9a62fa321
keywords:
- DTN_WMKEYDOWN 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- DTN_WMKEYDOWN
- DTN_WMKEYDOWNA
- DTN_WMKEYDOWNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce2e7d0761308805746278d2f542f5e9458b56d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094011"
---
# <a name="dtn_wmkeydown-notification-code"></a><span data-ttu-id="7f64f-105">DTN \_ WMKEYDOWN 通知碼</span><span class="sxs-lookup"><span data-stu-id="7f64f-105">DTN\_WMKEYDOWN notification code</span></span>

<span data-ttu-id="7f64f-106">當使用者在回呼欄位中輸入時，日期和時間選擇器會傳送 (DTP) 控制項。</span><span class="sxs-lookup"><span data-stu-id="7f64f-106">Sent by a date and time picker (DTP) control when the user types in a callback field.</span></span> <span data-ttu-id="7f64f-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="7f64f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_WMKEYDOWN

    lpDTKeystroke = (LPNMDATETIMEWMKEYDOWN)lParam;
```



## <a name="parameters"></a><span data-ttu-id="7f64f-108">參數</span><span class="sxs-lookup"><span data-stu-id="7f64f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f64f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7f64f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f64f-110">[**NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna)結構的指標，其中包含此通知碼實例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7f64f-110">A pointer to an [**NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna) structure containing information about this instance of the notification code.</span></span> <span data-ttu-id="7f64f-111">結構包含使用者所輸入之金鑰的相關資訊、定義回呼欄位的子字串，以及目前的系統日期和時間。</span><span class="sxs-lookup"><span data-stu-id="7f64f-111">The structure includes information about the key that the user typed, the substring that defines the callback field, and the current system date and time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f64f-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="7f64f-112">Return value</span></span>

<span data-ttu-id="7f64f-113">控制項的擁有者必須傳回零。</span><span class="sxs-lookup"><span data-stu-id="7f64f-113">The owner of the control must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f64f-114">備註</span><span class="sxs-lookup"><span data-stu-id="7f64f-114">Remarks</span></span>

<span data-ttu-id="7f64f-115">處理此通知程式碼可讓控制項的擁有者在控制項的回呼欄位內提供對按鍵的特定回應。</span><span class="sxs-lookup"><span data-stu-id="7f64f-115">Handling this notification code allows the owner of the control to provide specific responses to keystrokes within the callback fields of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f64f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f64f-116">Requirements</span></span>



| <span data-ttu-id="7f64f-117">需求</span><span class="sxs-lookup"><span data-stu-id="7f64f-117">Requirement</span></span> | <span data-ttu-id="7f64f-118">值</span><span class="sxs-lookup"><span data-stu-id="7f64f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7f64f-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7f64f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7f64f-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f64f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7f64f-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7f64f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7f64f-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f64f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7f64f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="7f64f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f64f-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7f64f-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="7f64f-125">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="7f64f-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7f64f-126">**DTN \_WMKEYDOWNW** (Unicode) 和 **DTN \_ WMKEYDOWNA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="7f64f-126">**DTN\_WMKEYDOWNW** (Unicode) and **DTN\_WMKEYDOWNA** (ANSI)</span></span><br/>               |



 

 





