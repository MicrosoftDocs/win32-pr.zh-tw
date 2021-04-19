---
title: 'TCN_SELCHANGING (Commctrl 的通知碼) '
description: 通知索引標籤控制項的父視窗，指出目前選取的索引標籤即將變更。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: ec7b1bd3-8932-4418-9eed-ecb7c748e4dd
keywords:
- TCN_SELCHANGING 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TCN_SELCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6ba7dcf25d243d9b42876425564fba0e01c803f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968139"
---
# <a name="tcn_selchanging-notification-code"></a><span data-ttu-id="c5303-105">TCN \_ SELCHANGING 通知碼</span><span class="sxs-lookup"><span data-stu-id="c5303-105">TCN\_SELCHANGING notification code</span></span>

<span data-ttu-id="c5303-106">通知索引標籤控制項的父視窗，指出目前選取的索引標籤即將變更。</span><span class="sxs-lookup"><span data-stu-id="c5303-106">Notifies a tab control's parent window that the currently selected tab is about to change.</span></span> <span data-ttu-id="c5303-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="c5303-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_SELCHANGING 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c5303-108">參數</span><span class="sxs-lookup"><span data-stu-id="c5303-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5303-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c5303-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5303-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c5303-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5303-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5303-111">Return value</span></span>

<span data-ttu-id="c5303-112">若為 TRUE，則會傳回 **TRUE** 以防止選取範圍變更，或傳回 **FALSE** 表示允許變更選取專案。</span><span class="sxs-lookup"><span data-stu-id="c5303-112">Returns **TRUE** to prevent the selection from changing, or **FALSE** to allow the selection to change.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5303-113">備註</span><span class="sxs-lookup"><span data-stu-id="c5303-113">Remarks</span></span>

<span data-ttu-id="c5303-114">若要判斷目前選取的索引標籤，請使用 [**TabCtrl \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) 宏。</span><span class="sxs-lookup"><span data-stu-id="c5303-114">To determine the currently selected tab, use the [**TabCtrl\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5303-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5303-115">Requirements</span></span>



| <span data-ttu-id="c5303-116">需求</span><span class="sxs-lookup"><span data-stu-id="c5303-116">Requirement</span></span> | <span data-ttu-id="c5303-117">值</span><span class="sxs-lookup"><span data-stu-id="c5303-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5303-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5303-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c5303-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5303-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c5303-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5303-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c5303-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5303-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c5303-122">標頭</span><span class="sxs-lookup"><span data-stu-id="c5303-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5303-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c5303-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5303-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5303-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5303-125">TCN \_ SELCHANGE</span><span class="sxs-lookup"><span data-stu-id="c5303-125">TCN\_SELCHANGE</span></span>](tcn-selchange.md)
</dt> </dl>

 

 





