---
title: 'DTN_DATETIMECHANGE (Commctrl 的通知碼) '
description: 每次發生變更時，日期和時間選擇器都會傳送 (的 DTP) 控制。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 65cdd8fb-1f07-4447-b503-d40fdfa37202
keywords:
- DTN_DATETIMECHANGE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- DTN_DATETIMECHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40072a54732a0a3575e3153ddb901ca1df291b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843939"
---
# <a name="dtn_datetimechange-notification-code"></a><span data-ttu-id="fb7e3-105">DTN \_ DATETIMECHANGE 通知碼</span><span class="sxs-lookup"><span data-stu-id="fb7e3-105">DTN\_DATETIMECHANGE notification code</span></span>

<span data-ttu-id="fb7e3-106">每次發生變更時，日期和時間選擇器都會傳送 (的 DTP) 控制。</span><span class="sxs-lookup"><span data-stu-id="fb7e3-106">Sent by a date and time picker (DTP) control whenever a change occurs.</span></span> <span data-ttu-id="fb7e3-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="fb7e3-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_DATETIMECHANGE

    lpChange = (LPNMDATETIMECHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="fb7e3-108">參數</span><span class="sxs-lookup"><span data-stu-id="fb7e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb7e3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fb7e3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb7e3-110">[**NMDATETIMECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange)結構的指標，其中包含在控制項中發生之變更的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fb7e3-110">A pointer to an [**NMDATETIMECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange) structure containing information about the change that took place in the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb7e3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fb7e3-111">Return value</span></span>

<span data-ttu-id="fb7e3-112">控制項的擁有者必須傳回零。</span><span class="sxs-lookup"><span data-stu-id="fb7e3-112">The owner of the control must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb7e3-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb7e3-113">Requirements</span></span>



| <span data-ttu-id="fb7e3-114">需求</span><span class="sxs-lookup"><span data-stu-id="fb7e3-114">Requirement</span></span> | <span data-ttu-id="fb7e3-115">值</span><span class="sxs-lookup"><span data-stu-id="fb7e3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fb7e3-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fb7e3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fb7e3-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb7e3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fb7e3-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fb7e3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fb7e3-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb7e3-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fb7e3-120">標頭</span><span class="sxs-lookup"><span data-stu-id="fb7e3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb7e3-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="fb7e3-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





