---
title: 'TVN_GETDISPINFO (Commctrl 的通知碼) '
description: 要求樹狀檢視控制項的父視窗提供顯示或排序專案所需的資訊。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 2dfe41d8-1164-481b-ac07-8faba43c562a
keywords:
- TVN_GETDISPINFO 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_GETDISPINFO
- TVN_GETDISPINFOA
- TVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a09bcc683ba9cf2d89a796e63812381254588a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508608"
---
# <a name="tvn_getdispinfo-notification-code"></a><span data-ttu-id="cb15a-105">IZDEBSKI \_ GETDISPINFO 通知碼</span><span class="sxs-lookup"><span data-stu-id="cb15a-105">TVN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="cb15a-106">要求樹狀檢視控制項的父視窗提供顯示或排序專案所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="cb15a-106">Requests that a tree-view control's parent window provide information needed to display or sort an item.</span></span> <span data-ttu-id="cb15a-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="cb15a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_GETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="cb15a-108">參數</span><span class="sxs-lookup"><span data-stu-id="cb15a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb15a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb15a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb15a-110">[**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="cb15a-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure.</span></span> <span data-ttu-id="cb15a-111">**專案** 成員是 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構，其 **mask**、 **hItem**、 **state** 和 **lParam** 成員會指定所需的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="cb15a-111">The **item** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure whose **mask**, **hItem**, **state**, and **lParam** members specify the type of information required.</span></span> <span data-ttu-id="cb15a-112">您必須以適當的資訊填入結構的成員。</span><span class="sxs-lookup"><span data-stu-id="cb15a-112">You must fill the members of the structure with the appropriate information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb15a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="cb15a-113">Return value</span></span>

<span data-ttu-id="cb15a-114">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="cb15a-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb15a-115">備註</span><span class="sxs-lookup"><span data-stu-id="cb15a-115">Remarks</span></span>

<span data-ttu-id="cb15a-116">此通知碼會在下列情況下傳送：</span><span class="sxs-lookup"><span data-stu-id="cb15a-116">This notification code is sent under the following circumstances:</span></span>

-   <span data-ttu-id="cb15a-117">如果專案的 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構的 **PSZTEXT** 成員是 LPSTR \_ TEXTCALLBACK 值，控制項會傳送此通知碼以取得專案的文字。</span><span class="sxs-lookup"><span data-stu-id="cb15a-117">If the **pszText** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the LPSTR\_TEXTCALLBACK value, the control sends this notification code to retrieve the item's text.</span></span> <span data-ttu-id="cb15a-118">在此情況下， *lParam* 的 **mask** 成員將會設定 TVIF \_ 文字旗標。</span><span class="sxs-lookup"><span data-stu-id="cb15a-118">In this case, the **mask** member of *lParam* will have the TVIF\_TEXT flag set.</span></span>
-   <span data-ttu-id="cb15a-119">如果專案 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構的 **iImage** 或 **iSelectedImage** 成員是 I \_ IMAGECALLBACK 值，控制項會傳送此通知碼，以抓取控制項影像清單中專案圖示的索引。</span><span class="sxs-lookup"><span data-stu-id="cb15a-119">If the **iImage** or **iSelectedImage** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the I\_IMAGECALLBACK value, the control sends this notification code to retrieve the index of an item's icons in the control's image list.</span></span> <span data-ttu-id="cb15a-120">在此情況下，如果選取專案， *lParam* 的 **mask** 成員將會 \_ 設定 TVIF SELECTEDIMAGE 旗標。</span><span class="sxs-lookup"><span data-stu-id="cb15a-120">In this case, if the item is selected, the **mask** member of *lParam* will have the TVIF\_SELECTEDIMAGE flag set.</span></span> <span data-ttu-id="cb15a-121">如果未選取此專案， *lParam* 的 **mask** 成員將會 \_ 設定 TVIF 影像旗標。</span><span class="sxs-lookup"><span data-stu-id="cb15a-121">If the item is not selected, the **mask** member of *lParam* will have the TVIF\_IMAGE flag set.</span></span>
-   <span data-ttu-id="cb15a-122">如果專案的 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構的 **cChildren** 成員是 I \_ CHILDRENCALLBACK 值，控制項會傳送此通知碼以取得指出專案是否有子專案的值。</span><span class="sxs-lookup"><span data-stu-id="cb15a-122">If the **cChildren** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the I\_CHILDRENCALLBACK value, the control sends this notification code to retrieve a value that indicates whether the item has child items.</span></span> <span data-ttu-id="cb15a-123">在此情況下， *lParam* 的 **mask** 成員將會設定 TVIF \_ 子旗標。</span><span class="sxs-lookup"><span data-stu-id="cb15a-123">In this case, the **mask** member of *lParam* will have the TVIF\_CHILDREN flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb15a-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb15a-124">Requirements</span></span>



| <span data-ttu-id="cb15a-125">需求</span><span class="sxs-lookup"><span data-stu-id="cb15a-125">Requirement</span></span> | <span data-ttu-id="cb15a-126">值</span><span class="sxs-lookup"><span data-stu-id="cb15a-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb15a-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb15a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cb15a-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb15a-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cb15a-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb15a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cb15a-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb15a-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cb15a-131">標頭</span><span class="sxs-lookup"><span data-stu-id="cb15a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb15a-132"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="cb15a-132"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="cb15a-133">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="cb15a-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cb15a-134">**Izdebski \_GETDISPINFOW** (Unicode) 和 **izdebski \_ GETDISPINFOA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="cb15a-134">**TVN\_GETDISPINFOW** (Unicode) and **TVN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="cb15a-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb15a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb15a-136">IZDEBSKI \_ SETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="cb15a-136">TVN\_SETDISPINFO</span></span>](tvn-setdispinfo.md)
</dt> </dl>

 

 





