---
title: 'WM_VKEYTOITEM 訊息 (Winuser .h) '
description: 由具有磅 WANTKEYBOARDINPUT 樣式的清單方塊傳送 \_ 給其擁有者，以回應 WM \_ KEYDOWN 訊息。
ms.assetid: 2eab922f-7298-436f-bd94-0eefae7284d5
keywords:
- WM_VKEYTOITEM message Windows 控制項
topic_type:
- apiref
api_name:
- WM_VKEYTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1685682d8305fff5d9d93ef59d8859e099e6ce
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "104321668"
---
# <a name="wm_vkeytoitem-message"></a><span data-ttu-id="4c7df-104">WM \_ VKEYTOITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="4c7df-104">WM\_VKEYTOITEM message</span></span>

<span data-ttu-id="4c7df-105">由具有 [**磅 \_ WANTKEYBOARDINPUT**](list-box-styles.md) 樣式的清單方塊傳送給其擁有者，以回應 [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) 訊息。</span><span class="sxs-lookup"><span data-stu-id="4c7df-105">Sent by a list box with the [**LBS\_WANTKEYBOARDINPUT**](list-box-styles.md) style to its owner in response to a [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message.</span></span>


```C++
WM_VKEYTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="4c7df-106">參數</span><span class="sxs-lookup"><span data-stu-id="4c7df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c7df-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4c7df-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c7df-108">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定使用者所按下之金鑰的虛擬金鑰碼。</span><span class="sxs-lookup"><span data-stu-id="4c7df-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the virtual-key code of the key the user pressed.</span></span> <span data-ttu-id="4c7df-109">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))指定插入號的目前位置。</span><span class="sxs-lookup"><span data-stu-id="4c7df-109">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the caret.</span></span>

</dd> <dt>

<span data-ttu-id="4c7df-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4c7df-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c7df-111">清單方塊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4c7df-111">Handle to the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c7df-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="4c7df-112">Return value</span></span>

<span data-ttu-id="4c7df-113">傳回值會指定應用程式在回應訊息時所執行的動作。</span><span class="sxs-lookup"><span data-stu-id="4c7df-113">The return value specifies the action that the application performed in response to the message.</span></span> <span data-ttu-id="4c7df-114">傳回值-2 表示應用程式已處理選取專案的所有層面，且清單方塊不需要採取進一步的動作。</span><span class="sxs-lookup"><span data-stu-id="4c7df-114">A return value of -2 indicates that the application handled all aspects of selecting the item and requires no further action by the list box.</span></span> <span data-ttu-id="4c7df-115"> (請參閱 [備註]。 ) 傳回值-1 表示清單方塊應該執行預設動作來回應擊鍵。</span><span class="sxs-lookup"><span data-stu-id="4c7df-115">(See Remarks.) A return value of -1 indicates that the list box should perform the default action in response to the keystroke.</span></span> <span data-ttu-id="4c7df-116">傳回值0或以上會指定清單方塊中專案的索引，並指出清單方塊應該針對指定的專案執行擊鍵的預設動作。</span><span class="sxs-lookup"><span data-stu-id="4c7df-116">A return value of 0 or greater specifies the index of an item in the list box and indicates that the list box should perform the default action for the keystroke on the specified item.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c7df-117">備註</span><span class="sxs-lookup"><span data-stu-id="4c7df-117">Remarks</span></span>

<span data-ttu-id="4c7df-118">只有當清單方塊控制項未轉譯為字元的索引鍵時，才會傳回-2 的傳回值。</span><span class="sxs-lookup"><span data-stu-id="4c7df-118">A return value of -2 is valid only for keys that are not translated into characters by the list box control.</span></span> <span data-ttu-id="4c7df-119">如果 [**wm 的 \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) 訊息轉譯成 [**wm \_ 字元**](/windows/desktop/inputdev/wm-char) 訊息，而應用程式處理由按鍵結果所產生的 **wm \_ VKEYTOITEM** 訊息，則清單方塊會忽略傳回值，並對該字元進行預設處理) 。</span><span class="sxs-lookup"><span data-stu-id="4c7df-119">If the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message translates to a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message and the application processes the **WM\_VKEYTOITEM** message generated as a result of the key press, the list box ignores the return value and does the default processing for that character).</span></span> <span data-ttu-id="4c7df-120">**WM \_** 由索引鍵產生的 KEYDOWN 訊息（例如 VK \_ UP、VK \_ DOWN、VK \_ NEXT 和 VK \_ PREVIOUS）不會轉譯為 **WM \_ 字元** 訊息。</span><span class="sxs-lookup"><span data-stu-id="4c7df-120">**WM\_KEYDOWN** messages generated by keys such as VK\_UP, VK\_DOWN, VK\_NEXT, and VK\_PREVIOUS are not translated to **WM\_CHAR** messages.</span></span> <span data-ttu-id="4c7df-121">在這種情況下，會捕捉 **WM \_ VKEYTOITEM** 訊息並傳回-2，以防止清單方塊執行該金鑰的預設處理。</span><span class="sxs-lookup"><span data-stu-id="4c7df-121">In such cases, trapping the **WM\_VKEYTOITEM** message and returning -2 prevents the list box from doing the default processing for that key.</span></span>

<span data-ttu-id="4c7df-122">若要對產生 char 訊息並進行特殊處理的索引鍵進行陷阱，應用程式必須將清單方塊設為子類別、將 [**WM 的 \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) 和 [**wm \_ char**](/windows/desktop/inputdev/wm-char) 訊息設為子類別，並在子類別程式中適當地處理訊息。</span><span class="sxs-lookup"><span data-stu-id="4c7df-122">To trap keys that generate a char message and do special processing, the application must subclass the list box, trap both the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) and [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages, and process the messages appropriately in the subclass procedure.</span></span>

<span data-ttu-id="4c7df-123">上述備註適用于以 [**磅 \_ WANTKEYBOARDINPUT**](list-box-styles.md) 樣式建立的一般清單方塊。</span><span class="sxs-lookup"><span data-stu-id="4c7df-123">The preceding remarks apply to regular list boxes that are created with the [**LBS\_WANTKEYBOARDINPUT**](list-box-styles.md) style.</span></span> <span data-ttu-id="4c7df-124">如果清單方塊是主控描繪的，應用程式必須處理 [**WM \_ CHARTOITEM**](wm-chartoitem.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="4c7df-124">If the list box is owner-drawn, the application must process the [**WM\_CHARTOITEM**](wm-chartoitem.md) message.</span></span>

<span data-ttu-id="4c7df-125">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函數會傳回-1。</span><span class="sxs-lookup"><span data-stu-id="4c7df-125">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns -1.</span></span>

<span data-ttu-id="4c7df-126">如果對話方塊程式處理此訊息，則應該將所需的傳回值轉換成 **布林** 值，並直接傳回值。</span><span class="sxs-lookup"><span data-stu-id="4c7df-126">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="4c7df-127">\_ [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)函數所設定的 DWL MSGRESULT 值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="4c7df-127">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c7df-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c7df-128">Requirements</span></span>



| <span data-ttu-id="4c7df-129">需求</span><span class="sxs-lookup"><span data-stu-id="4c7df-129">Requirement</span></span> | <span data-ttu-id="4c7df-130">值</span><span class="sxs-lookup"><span data-stu-id="4c7df-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c7df-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c7df-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4c7df-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c7df-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4c7df-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c7df-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4c7df-134">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c7df-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4c7df-135">標頭</span><span class="sxs-lookup"><span data-stu-id="4c7df-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c7df-136"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="4c7df-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c7df-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c7df-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="4c7df-138">**參考**</span><span class="sxs-lookup"><span data-stu-id="4c7df-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4c7df-139">**WM \_ CHARTOITEM**</span><span class="sxs-lookup"><span data-stu-id="4c7df-139">**WM\_CHARTOITEM**</span></span>](wm-chartoitem.md)
</dt> <dt>

<span data-ttu-id="4c7df-140">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="4c7df-140">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="4c7df-141">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4c7df-141">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="4c7df-142">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4c7df-142">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4c7df-143">**WM \_ KEYDOWN**</span><span class="sxs-lookup"><span data-stu-id="4c7df-143">**WM\_KEYDOWN**</span></span>](/windows/desktop/inputdev/wm-keydown)
</dt> </dl>

 

