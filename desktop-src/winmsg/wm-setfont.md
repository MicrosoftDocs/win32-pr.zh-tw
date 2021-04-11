---
description: 設定在繪製文字時，控制項所使用的字型。
ms.assetid: 7db6b8af-dbec-4c29-8bf7-d7e95d9813c3
title: 'WM_SETFONT 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fc334e6b8c937759555c471f00ec56254a629c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944306"
---
# <a name="wm_setfont-message"></a><span data-ttu-id="fa9eb-103">WM \_ SETFONT 訊息</span><span class="sxs-lookup"><span data-stu-id="fa9eb-103">WM\_SETFONT message</span></span>

<span data-ttu-id="fa9eb-104">設定在繪製文字時，控制項所使用的字型。</span><span class="sxs-lookup"><span data-stu-id="fa9eb-104">Sets the font that a control is to use when drawing text.</span></span>


```C++
#define WM_SETFONT                      0x0030
```



## <a name="parameters"></a><span data-ttu-id="fa9eb-105">參數</span><span class="sxs-lookup"><span data-stu-id="fa9eb-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa9eb-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fa9eb-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa9eb-107">字型 (**HFONT**) 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fa9eb-107">A handle to the font (**HFONT**).</span></span> <span data-ttu-id="fa9eb-108">如果這個參數是 **Null**，則控制項會使用預設系統字型來繪製文字。</span><span class="sxs-lookup"><span data-stu-id="fa9eb-108">If this parameter is **NULL**, the control uses the default system font to draw text.</span></span>

</dd> <dt>

<span data-ttu-id="fa9eb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa9eb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa9eb-110">*LParam* 的低序位字指定是否應在設定字型時立即重新繪製控制項。</span><span class="sxs-lookup"><span data-stu-id="fa9eb-110">The low-order word of *lParam* specifies whether the control should be redrawn immediately upon setting the font.</span></span> <span data-ttu-id="fa9eb-111">如果此參數為 **TRUE**，控制項會自行重新繪製。</span><span class="sxs-lookup"><span data-stu-id="fa9eb-111">If this parameter is **TRUE**, the control redraws itself.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa9eb-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="fa9eb-112">Return value</span></span>

<span data-ttu-id="fa9eb-113">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="fa9eb-113">Type: **LRESULT**</span></span>

<span data-ttu-id="fa9eb-114">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="fa9eb-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa9eb-115">備註</span><span class="sxs-lookup"><span data-stu-id="fa9eb-115">Remarks</span></span>

<span data-ttu-id="fa9eb-116">**WM \_ SETFONT** 訊息會套用至所有控制項，而不只是對話方塊中的控制項。</span><span class="sxs-lookup"><span data-stu-id="fa9eb-116">The **WM\_SETFONT** message applies to all controls, not just those in dialog boxes.</span></span>

<span data-ttu-id="fa9eb-117">對話方塊控制項擁有者設定控制項字型的最佳時間，是在收到 [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md) 訊息時。</span><span class="sxs-lookup"><span data-stu-id="fa9eb-117">The best time for the owner of a dialog box control to set the font of the control is when it receives the [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md) message.</span></span> <span data-ttu-id="fa9eb-118">應用程式應該呼叫 [**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject) 函式來刪除不再需要的字型;例如，在終結控制項之後。</span><span class="sxs-lookup"><span data-stu-id="fa9eb-118">The application should call the [**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject) function to delete the font when it is no longer needed; for example, after it destroys the control.</span></span>

<span data-ttu-id="fa9eb-119">由於接收此訊息的結果，控制項的大小不會變更。</span><span class="sxs-lookup"><span data-stu-id="fa9eb-119">The size of the control does not change as a result of receiving this message.</span></span> <span data-ttu-id="fa9eb-120">為了避免無法容納控制項界限內的文字，應用程式應該在設定字型之前更正控制項視窗的大小。</span><span class="sxs-lookup"><span data-stu-id="fa9eb-120">To avoid clipping text that does not fit within the boundaries of the control, the application should correct the size of the control window before it sets the font.</span></span>

<span data-ttu-id="fa9eb-121">當對話方塊使用 [DS \_ SETFONT](../dlgbox/about-dialog-boxes.md) 樣式來設定其控制項中的文字時，系統會先將 **WM \_ SETFONT** 訊息傳送至對話方塊程式，然後再建立控制項。</span><span class="sxs-lookup"><span data-stu-id="fa9eb-121">When a dialog box uses the [DS\_SETFONT](../dlgbox/about-dialog-boxes.md) style to set the text in its controls, the system sends the **WM\_SETFONT** message to the dialog box procedure before it creates the controls.</span></span> <span data-ttu-id="fa9eb-122">應用程式可以藉 \_ 由呼叫下列任何功能，來建立包含 DS SETFONT 樣式的對話方塊：</span><span class="sxs-lookup"><span data-stu-id="fa9eb-122">An application can create a dialog box that contains the DS\_SETFONT style by calling any of the following functions:</span></span>

-   [<span data-ttu-id="fa9eb-123">**CreateDialogIndirect**</span><span class="sxs-lookup"><span data-stu-id="fa9eb-123">**CreateDialogIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
-   [<span data-ttu-id="fa9eb-124">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="fa9eb-124">**CreateDialogIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
-   [<span data-ttu-id="fa9eb-125">**DialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="fa9eb-125">**DialogBoxIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
-   [<span data-ttu-id="fa9eb-126">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="fa9eb-126">**DialogBoxIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)

## <a name="requirements"></a><span data-ttu-id="fa9eb-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa9eb-127">Requirements</span></span>



| <span data-ttu-id="fa9eb-128">需求</span><span class="sxs-lookup"><span data-stu-id="fa9eb-128">Requirement</span></span> | <span data-ttu-id="fa9eb-129">值</span><span class="sxs-lookup"><span data-stu-id="fa9eb-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa9eb-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa9eb-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fa9eb-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa9eb-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fa9eb-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa9eb-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fa9eb-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa9eb-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fa9eb-134">標頭</span><span class="sxs-lookup"><span data-stu-id="fa9eb-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa9eb-135"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="fa9eb-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa9eb-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa9eb-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="fa9eb-137">**參考**</span><span class="sxs-lookup"><span data-stu-id="fa9eb-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fa9eb-138">**CreateDialogIndirect**</span><span class="sxs-lookup"><span data-stu-id="fa9eb-138">**CreateDialogIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[<span data-ttu-id="fa9eb-139">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="fa9eb-139">**CreateDialogIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="fa9eb-140">**DialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="fa9eb-140">**DialogBoxIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[<span data-ttu-id="fa9eb-141">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="fa9eb-141">**DialogBoxIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="fa9eb-142">**DLGTEMPLATE**</span><span class="sxs-lookup"><span data-stu-id="fa9eb-142">**DLGTEMPLATE**</span></span>](/windows/win32/api/winuser/ns-winuser-dlgtemplate)
</dt> <dt>

[<span data-ttu-id="fa9eb-143">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="fa9eb-143">**MAKELPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[<span data-ttu-id="fa9eb-144">**WM \_ GETFONT**</span><span class="sxs-lookup"><span data-stu-id="fa9eb-144">**WM\_GETFONT**</span></span>](wm-getfont.md)
</dt> <dt>

[<span data-ttu-id="fa9eb-145">**WM \_ INITDIALOG**</span><span class="sxs-lookup"><span data-stu-id="fa9eb-145">**WM\_INITDIALOG**</span></span>](../dlgbox/wm-initdialog.md)
</dt> <dt>

<span data-ttu-id="fa9eb-146">**概念**</span><span class="sxs-lookup"><span data-stu-id="fa9eb-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fa9eb-147">Windows</span><span class="sxs-lookup"><span data-stu-id="fa9eb-147">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="fa9eb-148">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="fa9eb-148">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="fa9eb-149">**DeleteObject**</span><span class="sxs-lookup"><span data-stu-id="fa9eb-149">**DeleteObject**</span></span>](/windows/win32/api/wingdi/nf-wingdi-deleteobject)
</dt> </dl>

 

 
