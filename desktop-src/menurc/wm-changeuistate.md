---
title: 'WM_CHANGEUISTATE 訊息 (Winuser .h) '
description: 應用程式會傳送 WM \_ CHANGEUISTATE 訊息，以指出應變更 UI 狀態。
ms.assetid: d8dfc2fe-c64f-4e7e-b021-127aa85d5dd6
keywords:
- WM_CHANGEUISTATE 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_CHANGEUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdfec2a26b3b3d160d3d207c338c8ebecd32bf2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686468"
---
# <a name="wm_changeuistate-message"></a><span data-ttu-id="28352-104">WM \_ CHANGEUISTATE 訊息</span><span class="sxs-lookup"><span data-stu-id="28352-104">WM\_CHANGEUISTATE message</span></span>

<span data-ttu-id="28352-105">應用程式會傳送 **WM \_ CHANGEUISTATE** 訊息，以指出應變更 UI 狀態。</span><span class="sxs-lookup"><span data-stu-id="28352-105">An application sends the **WM\_CHANGEUISTATE** message to indicate that the UI state should be changed.</span></span>


```C++
#define WM_CHANGEUISTATE                0x0127
```



## <a name="parameters"></a><span data-ttu-id="28352-106">參數</span><span class="sxs-lookup"><span data-stu-id="28352-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28352-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="28352-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28352-108">低序位字組指定要採取的動作。</span><span class="sxs-lookup"><span data-stu-id="28352-108">The low-order word specifies the action to be taken.</span></span> <span data-ttu-id="28352-109">這個成員可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="28352-109">This member can be one of the following values.</span></span>



| <span data-ttu-id="28352-110">值</span><span class="sxs-lookup"><span data-stu-id="28352-110">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="28352-111">意義</span><span class="sxs-lookup"><span data-stu-id="28352-111">Meaning</span></span>                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <span data-ttu-id="28352-112"><dt>**Ui \_清除**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="28352-112"><dt>**UIS\_CLEAR**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="28352-113">高序位字組指定的 UI 狀態旗標應予以清除。</span><span class="sxs-lookup"><span data-stu-id="28352-113">The UI state flags specified by the high-order word should be cleared.</span></span><br/>                                                                  |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <span data-ttu-id="28352-114"><dt>**Ui \_初始化**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="28352-114"><dt>**UIS\_INITIALIZE**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="28352-115">高序位字組指定的 UI 狀態旗標應根據最後一個輸入事件來變更。</span><span class="sxs-lookup"><span data-stu-id="28352-115">The UI state flags specified by the high-order word should be changed based on the last input event.</span></span> <span data-ttu-id="28352-116">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="28352-116">For more information, see Remarks.</span></span><br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <span data-ttu-id="28352-117"><dt>**Ui \_設定**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="28352-117"><dt>**UIS\_SET**</dt> <dt>1</dt></span></span> </dl>                      | <span data-ttu-id="28352-118">應設定高序位字組所指定的 UI 狀態旗標。</span><span class="sxs-lookup"><span data-stu-id="28352-118">The UI state flags specified by the high-order word should be set.</span></span><br/>                                                                      |



 

<span data-ttu-id="28352-119">高序位單字可指定受影響的 UI 狀態元素或控制項的樣式。</span><span class="sxs-lookup"><span data-stu-id="28352-119">The high-order word specifies which UI state elements are affected or the style of the control.</span></span> <span data-ttu-id="28352-120">這個成員可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="28352-120">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="28352-121">值</span><span class="sxs-lookup"><span data-stu-id="28352-121">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="28352-122">意義</span><span class="sxs-lookup"><span data-stu-id="28352-122">Meaning</span></span>                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <span data-ttu-id="28352-123"><dt>**UISF \_現用**</dt> <dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="28352-123"><dt>**UISF\_ACTIVE**</dt> <dt>0x4</dt></span></span> </dl>          | <span data-ttu-id="28352-124">控制項應以用於作用中控制項的樣式來繪製。</span><span class="sxs-lookup"><span data-stu-id="28352-124">A control should be drawn in the style used for active controls.</span></span><br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <span data-ttu-id="28352-125"><dt>**UISF \_HIDEACCEL**</dt> <dt>0x2</dt></span><span class="sxs-lookup"><span data-stu-id="28352-125"><dt>**UISF\_HIDEACCEL**</dt> <dt>0x2</dt></span></span> </dl> | <span data-ttu-id="28352-126">鍵盤快捷為隱藏。</span><span class="sxs-lookup"><span data-stu-id="28352-126">Keyboard accelerators are hidden.</span></span><br/>                                |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <span data-ttu-id="28352-127"><dt>**UISF \_HIDEFOCUS**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="28352-127"><dt>**UISF\_HIDEFOCUS**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="28352-128">焦點指標是隱藏的。</span><span class="sxs-lookup"><span data-stu-id="28352-128">Focus indicators are hidden.</span></span><br/>                                     |



 

</dd> <dt>

<span data-ttu-id="28352-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="28352-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28352-130">未使用此參數，且必須為0。</span><span class="sxs-lookup"><span data-stu-id="28352-130">This parameter is not used and must be 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28352-131">備註</span><span class="sxs-lookup"><span data-stu-id="28352-131">Remarks</span></span>

<span data-ttu-id="28352-132">當視窗必須變更相同階層中所有視窗的 UI 狀態專案時，應該將此訊息傳送至本身或其父代。</span><span class="sxs-lookup"><span data-stu-id="28352-132">A window should send this message to itself or its parent when it must change the UI state elements of all windows in the same hierarchy.</span></span> <span data-ttu-id="28352-133">視窗程式必須讓 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 處理此訊息，讓整個視窗樹狀結構具有一致的 UI 狀態。</span><span class="sxs-lookup"><span data-stu-id="28352-133">The window procedure must let [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) process this message so that the entire window tree has a consistent UI state.</span></span> <span data-ttu-id="28352-134">當最上層視窗收到 **wm \_ CHANGEUISTATE** 訊息時，會將具有相同參數的 [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) 訊息傳送至所有子視窗。</span><span class="sxs-lookup"><span data-stu-id="28352-134">When the top-level window receives the **WM\_CHANGEUISTATE** message, it sends a [**WM\_UPDATEUISTATE**](wm-updateuistate.md) message with the same parameters to all child windows.</span></span> <span data-ttu-id="28352-135">當系統處理 **WM \_ UPDATEUISTATE** 訊息時，它會在 UI 狀態下進行變更。</span><span class="sxs-lookup"><span data-stu-id="28352-135">When the system processes the **WM\_UPDATEUISTATE** message, it makes the change in the UI state.</span></span>

<span data-ttu-id="28352-136">如果 *wParam* 的低序位文字是 ui \_ 初始化，系統會根據最後一個輸入事件，傳送具有 UI 狀態的 [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="28352-136">If the low-order word of *wParam* is UIS\_INITIALIZE, the system will send the [**WM\_UPDATEUISTATE**](wm-updateuistate.md) message with a UI state based on the last input event.</span></span> <span data-ttu-id="28352-137">例如，如果最後一個輸入來自滑鼠，系統將會隱藏鍵盤提示。而且，如果最後輸入來自鍵盤，系統將會顯示鍵盤提示。如果處理 **WM \_ CHANGEUISTATE** 所產生的狀態與舊狀態相同， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 就不會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="28352-137">For example, if the last input came from the mouse, the system will hide the keyboard cues. And, if the last input came from the keyboard, the system will show the keyboard cues. If the state that results from processing **WM\_CHANGEUISTATE** is the same as the old state, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) does not send this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="28352-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="28352-138">Requirements</span></span>



| <span data-ttu-id="28352-139">需求</span><span class="sxs-lookup"><span data-stu-id="28352-139">Requirement</span></span> | <span data-ttu-id="28352-140">值</span><span class="sxs-lookup"><span data-stu-id="28352-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28352-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="28352-141">Minimum supported client</span></span><br/> | <span data-ttu-id="28352-142">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28352-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="28352-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="28352-143">Minimum supported server</span></span><br/> | <span data-ttu-id="28352-144">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28352-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="28352-145">標頭</span><span class="sxs-lookup"><span data-stu-id="28352-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="28352-146"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="28352-146"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28352-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28352-147">See also</span></span>

<dl> <dt>

<span data-ttu-id="28352-148">**參考**</span><span class="sxs-lookup"><span data-stu-id="28352-148">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="28352-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="28352-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="28352-150">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="28352-150">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="28352-151">**WM \_ QUERYUISTATE**</span><span class="sxs-lookup"><span data-stu-id="28352-151">**WM\_QUERYUISTATE**</span></span>](wm-queryuistate.md)
</dt> <dt>

<span data-ttu-id="28352-152">**概念**</span><span class="sxs-lookup"><span data-stu-id="28352-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="28352-153">鍵盤加速器</span><span class="sxs-lookup"><span data-stu-id="28352-153">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

