---
title: 'WM_MENUCHAR 訊息 (Winuser .h) '
description: 當功能表在使用中，且使用者按下未對應至任何助憶鍵或快速鍵的按鍵時傳送。 這則訊息會傳送至擁有功能表的視窗。
ms.assetid: de6c91bb-80fd-44b2-8d96-d016477a6547
keywords:
- WM_MENUCHAR 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_MENUCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a278e4a1b4333631741a6a542318a8a55e40b512
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686592"
---
# <a name="wm_menuchar-message"></a><span data-ttu-id="023c0-105">WM \_ MENUCHAR 訊息</span><span class="sxs-lookup"><span data-stu-id="023c0-105">WM\_MENUCHAR message</span></span>

<span data-ttu-id="023c0-106">當功能表在使用中，且使用者按下未對應至任何助憶鍵或快速鍵的按鍵時傳送。</span><span class="sxs-lookup"><span data-stu-id="023c0-106">Sent when a menu is active and the user presses a key that does not correspond to any mnemonic or accelerator key.</span></span> <span data-ttu-id="023c0-107">這則訊息會傳送至擁有功能表的視窗。</span><span class="sxs-lookup"><span data-stu-id="023c0-107">This message is sent to the window that owns the menu.</span></span>


```C++
#define WM_MENUCHAR                     0x0120
```



## <a name="parameters"></a><span data-ttu-id="023c0-108">參數</span><span class="sxs-lookup"><span data-stu-id="023c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="023c0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="023c0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="023c0-110">低序位字組指定對應至使用者所按下之按鍵的字元碼。</span><span class="sxs-lookup"><span data-stu-id="023c0-110">The low-order word specifies the character code that corresponds to the key the user pressed.</span></span>

<span data-ttu-id="023c0-111">高序位字組指定現用功能表類型。</span><span class="sxs-lookup"><span data-stu-id="023c0-111">The high-order word specifies the active menu type.</span></span> <span data-ttu-id="023c0-112">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="023c0-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="023c0-113">值</span><span class="sxs-lookup"><span data-stu-id="023c0-113">Value</span></span>                                                                                                                                                                                                                 | <span data-ttu-id="023c0-114">意義</span><span class="sxs-lookup"><span data-stu-id="023c0-114">Meaning</span></span>                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <span data-ttu-id="023c0-115"><dt>**MF \_快顯視窗**</dt> <dt>0x00000010L</dt></span><span class="sxs-lookup"><span data-stu-id="023c0-115"><dt>**MF\_POPUP**</dt> <dt>0x00000010L</dt></span></span> </dl>       | <span data-ttu-id="023c0-116">下拉式選單、子功能表或快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="023c0-116">A drop-down menu, submenu, or shortcut menu.</span></span><br/> |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <span data-ttu-id="023c0-117"><dt>**MF \_SYSMENU**</dt> <dt>0x00002000L</dt></span><span class="sxs-lookup"><span data-stu-id="023c0-117"><dt>**MF\_SYSMENU**</dt> <dt>0x00002000L</dt></span></span> </dl> | <span data-ttu-id="023c0-118">[視窗] 功能表。</span><span class="sxs-lookup"><span data-stu-id="023c0-118">The window menu.</span></span><br/>                             |



 

</dd> <dt>

<span data-ttu-id="023c0-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="023c0-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="023c0-120">現用功能表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="023c0-120">A handle to the active menu.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="023c0-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="023c0-121">Return value</span></span>

<span data-ttu-id="023c0-122">處理此訊息的應用程式應該在傳回值的高序位字中傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="023c0-122">An application that processes this message should return one of the following values in the high-order word of the return value.</span></span>



| <span data-ttu-id="023c0-123">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="023c0-123">Return code/value</span></span>                                                                                                                                  | <span data-ttu-id="023c0-124">Description</span><span class="sxs-lookup"><span data-stu-id="023c0-124">Description</span></span>                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="023c0-125"><dt>**MNC \_關閉**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="023c0-125"><dt>**MNC\_CLOSE**</dt> <dt>1</dt></span></span> </dl>   | <span data-ttu-id="023c0-126">通知系統應該關閉使用中的功能表。</span><span class="sxs-lookup"><span data-stu-id="023c0-126">Informs the system that it should close the active menu.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="023c0-127"><dt>**MNC \_執行**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="023c0-127"><dt>**MNC\_EXECUTE**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="023c0-128">通知系統應該選擇傳回值的低序位字組中指定的專案。</span><span class="sxs-lookup"><span data-stu-id="023c0-128">Informs the system that it should choose the item specified in the low-order word of the return value.</span></span> <span data-ttu-id="023c0-129">擁有者視窗會收到 [**WM \_ 命令**](wm-command.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="023c0-129">The owner window receives a [**WM\_COMMAND**](wm-command.md) message.</span></span><br/> |
| <dl> <span data-ttu-id="023c0-130"><dt>**MNC \_忽略**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="023c0-130"><dt>**MNC\_IGNORE**</dt> <dt>0</dt></span></span> </dl>  | <span data-ttu-id="023c0-131">通知系統應該捨棄使用者所按下的字元，並在系統喇叭上建立短暫的嗶聲。</span><span class="sxs-lookup"><span data-stu-id="023c0-131">Informs the system that it should discard the character the user pressed and create a short beep on the system speaker.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="023c0-132"><dt>**MNC \_選取**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="023c0-132"><dt>**MNC\_SELECT**</dt> <dt>3</dt></span></span> </dl>  | <span data-ttu-id="023c0-133">通知系統應選取傳回值的低序位字組中指定的專案。</span><span class="sxs-lookup"><span data-stu-id="023c0-133">Informs the system that it should select the item specified in the low-order word of the return value.</span></span> <br/>                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="023c0-134">備註</span><span class="sxs-lookup"><span data-stu-id="023c0-134">Remarks</span></span>

<span data-ttu-id="023c0-135">如果高序位字組包含0或1，則會忽略低序位字組。</span><span class="sxs-lookup"><span data-stu-id="023c0-135">The low-order word is ignored if the high-order word contains 0 or 1.</span></span>

<span data-ttu-id="023c0-136">當使用快速鍵來選取顯示點陣圖的功能表項目時，應用程式應該處理此訊息。</span><span class="sxs-lookup"><span data-stu-id="023c0-136">An application should process this message when an accelerator is used to select a menu item that displays a bitmap.</span></span>

## <a name="requirements"></a><span data-ttu-id="023c0-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="023c0-137">Requirements</span></span>



| <span data-ttu-id="023c0-138">需求</span><span class="sxs-lookup"><span data-stu-id="023c0-138">Requirement</span></span> | <span data-ttu-id="023c0-139">值</span><span class="sxs-lookup"><span data-stu-id="023c0-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="023c0-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="023c0-140">Minimum supported client</span></span><br/> | <span data-ttu-id="023c0-141">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="023c0-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="023c0-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="023c0-142">Minimum supported server</span></span><br/> | <span data-ttu-id="023c0-143">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="023c0-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="023c0-144">標頭</span><span class="sxs-lookup"><span data-stu-id="023c0-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="023c0-145"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="023c0-145"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="023c0-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="023c0-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="023c0-147">**參考**</span><span class="sxs-lookup"><span data-stu-id="023c0-147">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="023c0-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="023c0-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="023c0-149">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="023c0-149">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="023c0-150">**概念**</span><span class="sxs-lookup"><span data-stu-id="023c0-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="023c0-151">鍵盤加速器</span><span class="sxs-lookup"><span data-stu-id="023c0-151">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

