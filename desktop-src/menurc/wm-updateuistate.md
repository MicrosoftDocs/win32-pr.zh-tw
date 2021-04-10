---
title: 'WM_UPDATEUISTATE 訊息 (Winuser .h) '
description: 應用程式會傳送 WM \_ UPDATEUISTATE 訊息，以變更指定之視窗及其所有子視窗的 UI 狀態。
ms.assetid: cbdeeddd-59b2-4a73-bfe9-17647d32bcf3
keywords:
- WM_UPDATEUISTATE 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_UPDATEUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 003d9ca45b357a7d0ebc172000b1e2c01505db8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106452"
---
# <a name="wm_updateuistate-message"></a><span data-ttu-id="39ca2-104">WM \_ UPDATEUISTATE 訊息</span><span class="sxs-lookup"><span data-stu-id="39ca2-104">WM\_UPDATEUISTATE message</span></span>

<span data-ttu-id="39ca2-105">應用程式會傳送 **WM \_ UPDATEUISTATE** 訊息，以變更指定之視窗及其所有子視窗的 UI 狀態。</span><span class="sxs-lookup"><span data-stu-id="39ca2-105">An application sends the **WM\_UPDATEUISTATE** message to change the UI state for the specified window and all its child windows.</span></span>


```C++
#define WM_UPDATEUISTATE                0x0128
```



## <a name="parameters"></a><span data-ttu-id="39ca2-106">參數</span><span class="sxs-lookup"><span data-stu-id="39ca2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39ca2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="39ca2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39ca2-108">低序位字組指定要執行的動作。</span><span class="sxs-lookup"><span data-stu-id="39ca2-108">The low-order word specifies the action to be performed.</span></span> <span data-ttu-id="39ca2-109">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="39ca2-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="39ca2-110">值</span><span class="sxs-lookup"><span data-stu-id="39ca2-110">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="39ca2-111">意義</span><span class="sxs-lookup"><span data-stu-id="39ca2-111">Meaning</span></span>                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <span data-ttu-id="39ca2-112"><dt>**Ui \_清除**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="39ca2-112"><dt>**UIS\_CLEAR**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="39ca2-113">高序位字組指定的 UI 狀態元素應該是隱藏的。</span><span class="sxs-lookup"><span data-stu-id="39ca2-113">The UI state element specified by the high-order word should be hidden.</span></span><br/>                                                                   |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <span data-ttu-id="39ca2-114"><dt>**Ui \_初始化**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="39ca2-114"><dt>**UIS\_INITIALIZE**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="39ca2-115">高序位字組指定的 UI 狀態元素應根據最後一個輸入事件來變更。</span><span class="sxs-lookup"><span data-stu-id="39ca2-115">The UI state element specified by the high-order word should be changed based on the last input event.</span></span> <span data-ttu-id="39ca2-116">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="39ca2-116">For more information, see Remarks.</span></span><br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <span data-ttu-id="39ca2-117"><dt>**Ui \_設定**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="39ca2-117"><dt>**UIS\_SET**</dt> <dt>1</dt></span></span> </dl>                      | <span data-ttu-id="39ca2-118">高序位字組所指定的 UI 狀態元素應該是可見的。</span><span class="sxs-lookup"><span data-stu-id="39ca2-118">The UI state element specified by the high-order word should be visible.</span></span><br/>                                                                  |



 

<span data-ttu-id="39ca2-119">高序位單字可指定受影響的 UI 狀態元素或控制項的樣式。</span><span class="sxs-lookup"><span data-stu-id="39ca2-119">The high-order word specifies which UI state elements are affected or the style of the control.</span></span> <span data-ttu-id="39ca2-120">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="39ca2-120">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="39ca2-121">值</span><span class="sxs-lookup"><span data-stu-id="39ca2-121">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="39ca2-122">意義</span><span class="sxs-lookup"><span data-stu-id="39ca2-122">Meaning</span></span>                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <span data-ttu-id="39ca2-123"><dt>**UISF \_現用**</dt> <dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="39ca2-123"><dt>**UISF\_ACTIVE**</dt> <dt>0x4</dt></span></span> </dl>          | <span data-ttu-id="39ca2-124">控制項應以用於作用中控制項的樣式來繪製。</span><span class="sxs-lookup"><span data-stu-id="39ca2-124">A control should be drawn in the style used for active controls.</span></span><br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <span data-ttu-id="39ca2-125"><dt>**UISF \_HIDEACCEL**</dt> <dt>0x2</dt></span><span class="sxs-lookup"><span data-stu-id="39ca2-125"><dt>**UISF\_HIDEACCEL**</dt> <dt>0x2</dt></span></span> </dl> | <span data-ttu-id="39ca2-126">鍵盤加速器。</span><span class="sxs-lookup"><span data-stu-id="39ca2-126">Keyboard accelerators.</span></span><br/>                                           |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <span data-ttu-id="39ca2-127"><dt>**UISF \_HIDEFOCUS**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="39ca2-127"><dt>**UISF\_HIDEFOCUS**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="39ca2-128">焦點指標。</span><span class="sxs-lookup"><span data-stu-id="39ca2-128">Focus indicators.</span></span><br/>                                                |



 

</dd> <dt>

<span data-ttu-id="39ca2-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39ca2-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39ca2-130">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="39ca2-130">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39ca2-131">備註</span><span class="sxs-lookup"><span data-stu-id="39ca2-131">Remarks</span></span>

<span data-ttu-id="39ca2-132">視窗應該會傳送此訊息來變更其所有子視窗的 UI 狀態。</span><span class="sxs-lookup"><span data-stu-id="39ca2-132">A window should send this message to change the UI state of all its child windows.</span></span> <span data-ttu-id="39ca2-133">相對於 [**wm \_ CHANGEUISTATE**](wm-changeuistate.md) 訊息（也就是通知），當 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 處理 **WM \_ UPDATEUISTATE** 訊息時，它會變更 UI 狀態，並將變更傳播到所有的子視窗。</span><span class="sxs-lookup"><span data-stu-id="39ca2-133">In contrast to the [**WM\_CHANGEUISTATE**](wm-changeuistate.md) message, which is a notification, when [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) processes the **WM\_UPDATEUISTATE** message it changes the UI state and propagates the changes to all child windows.</span></span>

<span data-ttu-id="39ca2-134">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會根據 *WPARAM* 值更新 UI 狀態。</span><span class="sxs-lookup"><span data-stu-id="39ca2-134">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function updates the UI state according to the *wParam* value.</span></span> <span data-ttu-id="39ca2-135">如果 UI 狀態已修改，則函式會將訊息傳送至所有的直屬子視窗。</span><span class="sxs-lookup"><span data-stu-id="39ca2-135">If the UI state is modified, the function sends the message to all the immediate child windows.</span></span> <span data-ttu-id="39ca2-136">**DefWindowProc** 也會在收到 [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) 訊息時傳送此訊息，通知系統子視窗要修改 UI 狀態。</span><span class="sxs-lookup"><span data-stu-id="39ca2-136">**DefWindowProc** also sends this message when it receives a [**WM\_CHANGEUISTATE**](wm-changeuistate.md) message notifying the system that a child window intends to modify the UI state.</span></span>

## <a name="requirements"></a><span data-ttu-id="39ca2-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="39ca2-137">Requirements</span></span>



| <span data-ttu-id="39ca2-138">需求</span><span class="sxs-lookup"><span data-stu-id="39ca2-138">Requirement</span></span> | <span data-ttu-id="39ca2-139">值</span><span class="sxs-lookup"><span data-stu-id="39ca2-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39ca2-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39ca2-140">Minimum supported client</span></span><br/> | <span data-ttu-id="39ca2-141">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39ca2-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="39ca2-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39ca2-142">Minimum supported server</span></span><br/> | <span data-ttu-id="39ca2-143">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39ca2-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="39ca2-144">標頭</span><span class="sxs-lookup"><span data-stu-id="39ca2-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="39ca2-145"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="39ca2-145"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39ca2-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39ca2-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="39ca2-147">**參考**</span><span class="sxs-lookup"><span data-stu-id="39ca2-147">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="39ca2-148">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="39ca2-148">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="39ca2-149">**WM \_ CHANGEUISTATE**</span><span class="sxs-lookup"><span data-stu-id="39ca2-149">**WM\_CHANGEUISTATE**</span></span>](wm-changeuistate.md)
</dt> <dt>

[<span data-ttu-id="39ca2-150">**WM \_ QUERYUISTATE**</span><span class="sxs-lookup"><span data-stu-id="39ca2-150">**WM\_QUERYUISTATE**</span></span>](wm-queryuistate.md)
</dt> <dt>

<span data-ttu-id="39ca2-151">**概念**</span><span class="sxs-lookup"><span data-stu-id="39ca2-151">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="39ca2-152">鍵盤加速器</span><span class="sxs-lookup"><span data-stu-id="39ca2-152">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

