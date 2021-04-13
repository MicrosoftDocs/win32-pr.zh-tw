---
title: 'WM_CHARTOITEM 訊息 (Winuser .h) '
description: 由具有磅 WANTKEYBOARDINPUT 樣式的清單方塊傳送 \_ 給其擁有者，以回應 WM \_ 字元訊息。
ms.assetid: f941c00b-b836-4f1b-b8cf-8ac2b0704af3
keywords:
- WM_CHARTOITEM message Windows 控制項
topic_type:
- apiref
api_name:
- WM_CHARTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc9df55dcf9f507cb57e91fe0214eab94c53f22
ms.sourcegitcommit: ac62be2f60f757f61ea647a95c168c9841ffabac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "104322543"
---
# <a name="wm_chartoitem-message"></a><span data-ttu-id="b92cd-104">WM \_ CHARTOITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="b92cd-104">WM\_CHARTOITEM message</span></span>

<span data-ttu-id="b92cd-105">由具有 [**磅 \_ WANTKEYBOARDINPUT**](list-box-styles.md) 樣式的清單方塊傳送給其擁有者，以回應 [**WM \_ 字元**](/windows/desktop/inputdev/wm-char) 訊息。</span><span class="sxs-lookup"><span data-stu-id="b92cd-105">Sent by a list box with the [**LBS\_WANTKEYBOARDINPUT**](list-box-styles.md) style to its owner in response to a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span>


```C++
WM_CHARTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b92cd-106">參數</span><span class="sxs-lookup"><span data-stu-id="b92cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b92cd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b92cd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b92cd-108">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定使用者所按下之按鍵的字元碼。</span><span class="sxs-lookup"><span data-stu-id="b92cd-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the character code of the key the user pressed.</span></span> <span data-ttu-id="b92cd-109">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))指定插入號的目前位置。</span><span class="sxs-lookup"><span data-stu-id="b92cd-109">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the caret.</span></span>

</dd> <dt>

<span data-ttu-id="b92cd-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b92cd-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b92cd-111">清單方塊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b92cd-111">Handle to the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b92cd-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b92cd-112">Return value</span></span>

<span data-ttu-id="b92cd-113">傳回值會指定應用程式在回應訊息時所執行的動作。</span><span class="sxs-lookup"><span data-stu-id="b92cd-113">The return value specifies the action that the application performed in response to the message.</span></span> <span data-ttu-id="b92cd-114">傳回值-1 或-2 表示應用程式已處理選取專案的所有層面，而不需要在清單方塊中採取進一步的動作。</span><span class="sxs-lookup"><span data-stu-id="b92cd-114">A return value of -1 or -2 indicates that the application handled all aspects of selecting the item and requires no further action by the list box.</span></span> <span data-ttu-id="b92cd-115">傳回值0或以上會指定清單方塊中專案的以零為基底的索引，並指出清單方塊應該針對指定的專案執行擊鍵的預設動作。</span><span class="sxs-lookup"><span data-stu-id="b92cd-115">A return value of 0 or greater specifies the zero-based index of an item in the list box and indicates that the list box should perform the default action for the keystroke on the specified item.</span></span>

## <a name="remarks"></a><span data-ttu-id="b92cd-116">備註</span><span class="sxs-lookup"><span data-stu-id="b92cd-116">Remarks</span></span>

<span data-ttu-id="b92cd-117">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函數會傳回-1。</span><span class="sxs-lookup"><span data-stu-id="b92cd-117">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns -1.</span></span>

<span data-ttu-id="b92cd-118">只有擁有者繪製的清單方塊沒有 [**磅 \_ HASSTRINGS**](list-box-styles.md) 樣式可以接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="b92cd-118">Only owner-drawn list boxes that do not have the [**LBS\_HASSTRINGS**](list-box-styles.md) style can receive this message.</span></span>

<span data-ttu-id="b92cd-119">如果對話方塊程式處理此訊息，則應該將所需的傳回值轉換成 **布林** 值，並直接傳回值。</span><span class="sxs-lookup"><span data-stu-id="b92cd-119">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="b92cd-120">[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)函數所設定的 *DWL \_ MSGRESULT* 值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="b92cd-120">The *DWL\_MSGRESULT* value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="b92cd-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b92cd-121">Requirements</span></span>



| <span data-ttu-id="b92cd-122">需求</span><span class="sxs-lookup"><span data-stu-id="b92cd-122">Requirement</span></span> | <span data-ttu-id="b92cd-123">值</span><span class="sxs-lookup"><span data-stu-id="b92cd-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b92cd-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b92cd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b92cd-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b92cd-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b92cd-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b92cd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b92cd-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b92cd-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b92cd-128">標頭</span><span class="sxs-lookup"><span data-stu-id="b92cd-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b92cd-129"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b92cd-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b92cd-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b92cd-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="b92cd-131">**參考**</span><span class="sxs-lookup"><span data-stu-id="b92cd-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b92cd-132">**WM \_ VKEYTOITEM**</span><span class="sxs-lookup"><span data-stu-id="b92cd-132">**WM\_VKEYTOITEM**</span></span>](wm-vkeytoitem.md)
</dt> <dt>

<span data-ttu-id="b92cd-133">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="b92cd-133">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b92cd-134">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="b92cd-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="b92cd-135">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b92cd-135">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="b92cd-136">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b92cd-136">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b92cd-137">**WM \_ 字元**</span><span class="sxs-lookup"><span data-stu-id="b92cd-137">**WM\_CHAR**</span></span>](/windows/desktop/inputdev/wm-char)
</dt> </dl>

 

