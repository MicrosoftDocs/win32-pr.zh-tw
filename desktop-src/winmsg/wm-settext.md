---
description: 設定視窗的文字。
ms.assetid: 1b48c309-6903-4139-bf42-e8526963e681
title: 'WM_SETTEXT 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3284855d817d5207b0d7572a41774e961c0113f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694971"
---
# <a name="wm_settext-message"></a><span data-ttu-id="88b61-103">WM \_ SETTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="88b61-103">WM\_SETTEXT message</span></span>

<span data-ttu-id="88b61-104">設定視窗的文字。</span><span class="sxs-lookup"><span data-stu-id="88b61-104">Sets the text of a window.</span></span>


```C++
#define WM_SETTEXT                      0x000C
```



## <a name="parameters"></a><span data-ttu-id="88b61-105">參數</span><span class="sxs-lookup"><span data-stu-id="88b61-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88b61-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="88b61-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="88b61-107">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="88b61-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="88b61-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="88b61-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="88b61-109">以 null 結束的字串指標，也就是視窗文字。</span><span class="sxs-lookup"><span data-stu-id="88b61-109">A pointer to a null-terminated string that is the window text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88b61-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="88b61-110">Return value</span></span>

<span data-ttu-id="88b61-111">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="88b61-111">Type: **LRESULT**</span></span>

<span data-ttu-id="88b61-112">如果已設定文字，則傳回值為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="88b61-112">The return value is **TRUE** if the text is set.</span></span> <span data-ttu-id="88b61-113">這是 **FALSE** (針對編輯控制項) 、 **LB \_ ERRSPACE** (適用于清單方塊) ，或 **CB \_ ERRSPACE** (適用于下拉式方塊) 如果空間不足，無法設定編輯控制項中的文字。</span><span class="sxs-lookup"><span data-stu-id="88b61-113">It is **FALSE** (for an edit control), **LB\_ERRSPACE** (for a list box), or **CB\_ERRSPACE** (for a combo box) if insufficient space is available to set the text in the edit control.</span></span> <span data-ttu-id="88b61-114">如果此訊息傳送至沒有編輯控制項的下拉式方塊，則為 **CB \_ 錯誤** 。</span><span class="sxs-lookup"><span data-stu-id="88b61-114">It is **CB\_ERR** if this message is sent to a combo box without an edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="88b61-115">備註</span><span class="sxs-lookup"><span data-stu-id="88b61-115">Remarks</span></span>

<span data-ttu-id="88b61-116">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會設定並顯示視窗文字。</span><span class="sxs-lookup"><span data-stu-id="88b61-116">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sets and displays the window text.</span></span> <span data-ttu-id="88b61-117">若為編輯控制項，則文字是編輯控制項的內容。</span><span class="sxs-lookup"><span data-stu-id="88b61-117">For an edit control, the text is the contents of the edit control.</span></span> <span data-ttu-id="88b61-118">如果是下拉式方塊，文字就是下拉式方塊編輯控制項部分的內容。</span><span class="sxs-lookup"><span data-stu-id="88b61-118">For a combo box, the text is the contents of the edit-control portion of the combo box.</span></span> <span data-ttu-id="88b61-119">若為按鈕，文字就是按鈕名稱。</span><span class="sxs-lookup"><span data-stu-id="88b61-119">For a button, the text is the button name.</span></span> <span data-ttu-id="88b61-120">若為其他視窗，則文字為視窗標題。</span><span class="sxs-lookup"><span data-stu-id="88b61-120">For other windows, the text is the window title.</span></span>

<span data-ttu-id="88b61-121">此訊息不會變更下拉式方塊的清單方塊中目前的選取範圍。</span><span class="sxs-lookup"><span data-stu-id="88b61-121">This message does not change the current selection in the list box of a combo box.</span></span> <span data-ttu-id="88b61-122">應用程式應該使用 [**CB \_ SELECTSTRING**](../controls/cb-selectstring.md) 訊息，在清單方塊中選取符合編輯控制項中文字的專案。</span><span class="sxs-lookup"><span data-stu-id="88b61-122">An application should use the [**CB\_SELECTSTRING**](../controls/cb-selectstring.md) message to select the item in a list box that matches the text in the edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="88b61-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="88b61-123">Requirements</span></span>



| <span data-ttu-id="88b61-124">需求</span><span class="sxs-lookup"><span data-stu-id="88b61-124">Requirement</span></span> | <span data-ttu-id="88b61-125">值</span><span class="sxs-lookup"><span data-stu-id="88b61-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b61-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88b61-126">Minimum supported client</span></span><br/> | <span data-ttu-id="88b61-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88b61-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="88b61-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88b61-128">Minimum supported server</span></span><br/> | <span data-ttu-id="88b61-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88b61-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="88b61-130">標頭</span><span class="sxs-lookup"><span data-stu-id="88b61-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="88b61-131"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="88b61-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88b61-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88b61-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="88b61-133">**參考**</span><span class="sxs-lookup"><span data-stu-id="88b61-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="88b61-134">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="88b61-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="88b61-135">**WM \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="88b61-135">**WM\_GETTEXT**</span></span>](wm-gettext.md)
</dt> <dt>

<span data-ttu-id="88b61-136">**概念**</span><span class="sxs-lookup"><span data-stu-id="88b61-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="88b61-137">Windows</span><span class="sxs-lookup"><span data-stu-id="88b61-137">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="88b61-138">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="88b61-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="88b61-139">**CB \_ SELECTSTRING**</span><span class="sxs-lookup"><span data-stu-id="88b61-139">**CB\_SELECTSTRING**</span></span>](../controls/cb-selectstring.md)
</dt> </dl>

 

 
