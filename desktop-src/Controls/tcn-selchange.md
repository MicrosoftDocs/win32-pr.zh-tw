---
title: 'TCN_SELCHANGE (Commctrl 的通知碼) '
description: 通知索引標籤控制項的父視窗，指出目前選取的索引標籤已變更。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: f40e30f6-169b-4381-a300-12c3befb5fc5
keywords:
- TCN_SELCHANGE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8578ac9fee7754b1ae27c05c6ec1b15636090040
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685498"
---
# <a name="tcn_selchange-notification-code"></a><span data-ttu-id="adeca-105">TCN \_ SELCHANGE 通知碼</span><span class="sxs-lookup"><span data-stu-id="adeca-105">TCN\_SELCHANGE notification code</span></span>

<span data-ttu-id="adeca-106">通知索引標籤控制項的父視窗，指出目前選取的索引標籤已變更。</span><span class="sxs-lookup"><span data-stu-id="adeca-106">Notifies a tab control's parent window that the currently selected tab has changed.</span></span> <span data-ttu-id="adeca-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="adeca-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_SELCHANGE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="adeca-108">參數</span><span class="sxs-lookup"><span data-stu-id="adeca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adeca-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="adeca-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="adeca-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="adeca-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adeca-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="adeca-111">Return value</span></span>

<span data-ttu-id="adeca-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="adeca-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="adeca-113">備註</span><span class="sxs-lookup"><span data-stu-id="adeca-113">Remarks</span></span>

<span data-ttu-id="adeca-114">若要判斷目前選取的索引標籤，請使用 [**TabCtrl \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) 宏。</span><span class="sxs-lookup"><span data-stu-id="adeca-114">To determine the currently selected tab, use the [**TabCtrl\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="adeca-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="adeca-115">Requirements</span></span>



| <span data-ttu-id="adeca-116">需求</span><span class="sxs-lookup"><span data-stu-id="adeca-116">Requirement</span></span> | <span data-ttu-id="adeca-117">值</span><span class="sxs-lookup"><span data-stu-id="adeca-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="adeca-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="adeca-118">Minimum supported client</span></span><br/> | <span data-ttu-id="adeca-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="adeca-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="adeca-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="adeca-120">Minimum supported server</span></span><br/> | <span data-ttu-id="adeca-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="adeca-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="adeca-122">標頭</span><span class="sxs-lookup"><span data-stu-id="adeca-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="adeca-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="adeca-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adeca-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="adeca-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adeca-125">TCN \_ SELCHANGING</span><span class="sxs-lookup"><span data-stu-id="adeca-125">TCN\_SELCHANGING</span></span>](tcn-selchanging.md)
</dt> </dl>

 

 





