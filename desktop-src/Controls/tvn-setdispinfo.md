---
title: 'TVN_SETDISPINFO (Commctrl 的通知碼) '
description: 通知樹狀檢視控制項的父視窗，它必須更新它針對某個專案所維護的資訊。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 40fa61bc-c043-4001-ada9-b627d68bd737
keywords:
- TVN_SETDISPINFO 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_SETDISPINFO
- TVN_SETDISPINFOA
- TVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b03e60ba7d8e6d7851c62fac030bd252cf957d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969147"
---
# <a name="tvn_setdispinfo-notification-code"></a><span data-ttu-id="4e4b5-105">IZDEBSKI \_ SETDISPINFO 通知碼</span><span class="sxs-lookup"><span data-stu-id="4e4b5-105">TVN\_SETDISPINFO notification code</span></span>

<span data-ttu-id="4e4b5-106">通知樹狀檢視控制項的父視窗，它必須更新它針對某個專案所維護的資訊。</span><span class="sxs-lookup"><span data-stu-id="4e4b5-106">Notifies a tree-view control's parent window that it must update the information it maintains about an item.</span></span> <span data-ttu-id="4e4b5-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="4e4b5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="4e4b5-108">參數</span><span class="sxs-lookup"><span data-stu-id="4e4b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e4b5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4e4b5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e4b5-110">描述正在更新之專案的 [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="4e4b5-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure that describes the item being updated.</span></span> <span data-ttu-id="4e4b5-111">[**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構的 **hItem** 成員會指定要更新的專案，而 **遮罩** 成員會指定要更新專案的哪些屬性。</span><span class="sxs-lookup"><span data-stu-id="4e4b5-111">The **hItem** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure specifies the item being updated, and the **mask** member specifies which attributes of the item are being updated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e4b5-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="4e4b5-112">Return value</span></span>

<span data-ttu-id="4e4b5-113">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="4e4b5-113">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e4b5-114">備註</span><span class="sxs-lookup"><span data-stu-id="4e4b5-114">Remarks</span></span>

<span data-ttu-id="4e4b5-115">如果專案的 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構的 **PSZTEXT** 成員是 LPSTR \_ TEXTCALLBACK 值，控制項會傳送此通知來設定專案的文字。</span><span class="sxs-lookup"><span data-stu-id="4e4b5-115">If the **pszText** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the LPSTR\_TEXTCALLBACK value, the control sends this notification to set the item's text.</span></span> <span data-ttu-id="4e4b5-116">在此情況下， *lParam* 的 **mask** 成員將會設定 TVIF \_ 文字旗標。</span><span class="sxs-lookup"><span data-stu-id="4e4b5-116">In this case, the **mask** member of *lParam* will have the TVIF\_TEXT flag set.</span></span>

<span data-ttu-id="4e4b5-117">如果專案 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構的 **iImage** 或 **iSelectedImage** 成員是 I \_ IMAGECALLBACK 值，控制項會傳送此通知，以取得要顯示之圖示影像的索引。</span><span class="sxs-lookup"><span data-stu-id="4e4b5-117">If the **iImage** or **iSelectedImage** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the I\_IMAGECALLBACK value, the control sends this notification to retrieve the index of the icon image to display.</span></span> <span data-ttu-id="4e4b5-118">在此情況下， *lParam* 的 **mask** 成員將會設定 TVIF \_ IMAGE 或 TVIF \_ SELECTEDIMAGE 旗標。</span><span class="sxs-lookup"><span data-stu-id="4e4b5-118">In this case, the **mask** member of *lParam* will have the TVIF\_IMAGE or TVIF\_SELECTEDIMAGE flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e4b5-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e4b5-119">Requirements</span></span>



| <span data-ttu-id="4e4b5-120">需求</span><span class="sxs-lookup"><span data-stu-id="4e4b5-120">Requirement</span></span> | <span data-ttu-id="4e4b5-121">值</span><span class="sxs-lookup"><span data-stu-id="4e4b5-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e4b5-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4e4b5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4e4b5-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e4b5-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4e4b5-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4e4b5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4e4b5-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e4b5-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4e4b5-126">標頭</span><span class="sxs-lookup"><span data-stu-id="4e4b5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e4b5-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4e4b5-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="4e4b5-128">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="4e4b5-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4e4b5-129">**Izdebski \_SETDISPINFOW** (Unicode) 和 **izdebski \_ SETDISPINFOA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="4e4b5-129">**TVN\_SETDISPINFOW** (Unicode) and **TVN\_SETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="4e4b5-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e4b5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e4b5-131">**TVITEM**</span><span class="sxs-lookup"><span data-stu-id="4e4b5-131">**TVITEM**</span></span>](/windows/win32/api/commctrl/ns-commctrl-tvitema)
</dt> <dt>

[<span data-ttu-id="4e4b5-132">**TVITEMEX**</span><span class="sxs-lookup"><span data-stu-id="4e4b5-132">**TVITEMEX**</span></span>](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)
</dt> <dt>

[<span data-ttu-id="4e4b5-133">IZDEBSKI \_ GETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="4e4b5-133">TVN\_GETDISPINFO</span></span>](tvn-getdispinfo.md)
</dt> </dl>

 

 





