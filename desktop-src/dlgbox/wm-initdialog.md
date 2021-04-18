---
title: 'WM_INITDIALOG 訊息 (Winuser .h) '
description: 在對話方塊顯示之前，立即傳送至對話方塊程式。 對話方塊程式通常會使用這個訊息來初始化控制項，並執行任何其他會影響對話方塊外觀的初始作業。
ms.assetid: bc4f4718-1dab-48db-ae3b-5a81a7be2644
keywords:
- WM_INITDIALOG 訊息對話方塊
topic_type:
- apiref
api_name:
- WM_INITDIALOG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64646075bc3d5c90076d6c1ca0d61f80111c90ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965738"
---
# <a name="wm_initdialog-message"></a><span data-ttu-id="59137-105">WM \_ INITDIALOG 訊息</span><span class="sxs-lookup"><span data-stu-id="59137-105">WM\_INITDIALOG message</span></span>

<span data-ttu-id="59137-106">在對話方塊顯示之前，立即傳送至對話方塊程式。</span><span class="sxs-lookup"><span data-stu-id="59137-106">Sent to the dialog box procedure immediately before a dialog box is displayed.</span></span> <span data-ttu-id="59137-107">對話方塊程式通常會使用這個訊息來初始化控制項，並執行任何其他會影響對話方塊外觀的初始作業。</span><span class="sxs-lookup"><span data-stu-id="59137-107">Dialog box procedures typically use this message to initialize controls and carry out any other initialization tasks that affect the appearance of the dialog box.</span></span>


```C++
#define WM_INITDIALOG                   0x0110
```



## <a name="parameters"></a><span data-ttu-id="59137-108">參數</span><span class="sxs-lookup"><span data-stu-id="59137-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59137-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="59137-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59137-110">控制項的控制碼，可接收預設鍵盤焦點。</span><span class="sxs-lookup"><span data-stu-id="59137-110">A handle to the control to receive the default keyboard focus.</span></span> <span data-ttu-id="59137-111">只有在對話方塊程式傳回 **TRUE** 時，系統才會指派預設的鍵盤焦點。</span><span class="sxs-lookup"><span data-stu-id="59137-111">The system assigns the default keyboard focus only if the dialog box procedure returns **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="59137-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59137-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59137-113">其他初始資料。</span><span class="sxs-lookup"><span data-stu-id="59137-113">Additional initialization data.</span></span> <span data-ttu-id="59137-114">這項資料會在用來建立對話方塊的 [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)、 [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)、 [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)或 [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama)函數的呼叫中，當做 *lParam* 參數傳遞給系統。</span><span class="sxs-lookup"><span data-stu-id="59137-114">This data is passed to the system as the *lParam* parameter in a call to the [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), or [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) function used to create the dialog box.</span></span> <span data-ttu-id="59137-115">針對屬性工作表，此參數是用來建立頁面之 [**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="59137-115">For property sheets, this parameter is a pointer to the [**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2) structure used to create the page.</span></span> <span data-ttu-id="59137-116">如果使用任何其他對話方塊建立函式，則此參數為零。</span><span class="sxs-lookup"><span data-stu-id="59137-116">This parameter is zero if any other dialog box creation function is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59137-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="59137-117">Return value</span></span>

<span data-ttu-id="59137-118">對話方塊程式應該會傳回 **TRUE** ，以指示系統將鍵盤焦點設定為 *wParam* 所指定的控制項。</span><span class="sxs-lookup"><span data-stu-id="59137-118">The dialog box procedure should return **TRUE** to direct the system to set the keyboard focus to the control specified by *wParam*.</span></span> <span data-ttu-id="59137-119">否則，它應該會傳回 **FALSE** ，以防止系統設定預設的鍵盤焦點。</span><span class="sxs-lookup"><span data-stu-id="59137-119">Otherwise, it should return **FALSE** to prevent the system from setting the default keyboard focus.</span></span>

<span data-ttu-id="59137-120">對話方塊程式應該會直接傳回值。</span><span class="sxs-lookup"><span data-stu-id="59137-120">The dialog box procedure should return the value directly.</span></span> <span data-ttu-id="59137-121">[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)函數所設定的 **DWL \_ MSGRESULT** 值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="59137-121">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="59137-122">備註</span><span class="sxs-lookup"><span data-stu-id="59137-122">Remarks</span></span>

<span data-ttu-id="59137-123">接收預設鍵盤焦點的控制項一律是對話方塊中可見、未停用，且具有 **WS \_ TABSTOP** 樣式的第一個控制項。</span><span class="sxs-lookup"><span data-stu-id="59137-123">The control to receive the default keyboard focus is always the first control in the dialog box that is visible, not disabled, and that has the **WS\_TABSTOP** style.</span></span> <span data-ttu-id="59137-124">當對話方塊程式傳回 **TRUE** 時，系統會檢查控制項，以確定該程式未停用該程式。</span><span class="sxs-lookup"><span data-stu-id="59137-124">When the dialog box procedure returns **TRUE**, the system checks the control to ensure that the procedure has not disabled it.</span></span> <span data-ttu-id="59137-125">如果已停用，系統會將鍵盤焦點設定為可見、未停用，且具有 **WS \_ TABSTOP** 的下一個控制項。</span><span class="sxs-lookup"><span data-stu-id="59137-125">If it has been disabled, the system sets the keyboard focus to the next control that is visible, not disabled, and has the **WS\_TABSTOP**.</span></span>

<span data-ttu-id="59137-126">只有當應用程式已將鍵盤焦點設定為對話方塊的其中一個控制項時，才會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="59137-126">An application can return **FALSE** only if it has set the keyboard focus to one of the controls of the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="59137-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="59137-127">Requirements</span></span>



| <span data-ttu-id="59137-128">需求</span><span class="sxs-lookup"><span data-stu-id="59137-128">Requirement</span></span> | <span data-ttu-id="59137-129">值</span><span class="sxs-lookup"><span data-stu-id="59137-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59137-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="59137-130">Minimum supported client</span></span><br/> | <span data-ttu-id="59137-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59137-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="59137-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="59137-132">Minimum supported server</span></span><br/> | <span data-ttu-id="59137-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59137-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="59137-134">標頭</span><span class="sxs-lookup"><span data-stu-id="59137-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="59137-135"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="59137-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59137-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59137-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="59137-137">**參考**</span><span class="sxs-lookup"><span data-stu-id="59137-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="59137-138">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="59137-138">**CreateDialogIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="59137-139">**CreateDialogParam**</span><span class="sxs-lookup"><span data-stu-id="59137-139">**CreateDialogParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)
</dt> <dt>

[<span data-ttu-id="59137-140">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="59137-140">**DialogBoxIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="59137-141">**DialogBoxParam**</span><span class="sxs-lookup"><span data-stu-id="59137-141">**DialogBoxParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama)
</dt> <dt>

[<span data-ttu-id="59137-142">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="59137-142">**SetFocus**</span></span>](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

<span data-ttu-id="59137-143">**概念**</span><span class="sxs-lookup"><span data-stu-id="59137-143">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="59137-144">對話方塊</span><span class="sxs-lookup"><span data-stu-id="59137-144">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="59137-145">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="59137-145">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="59137-146">**PROPSHEETPAGE**</span><span class="sxs-lookup"><span data-stu-id="59137-146">**PROPSHEETPAGE**</span></span>](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2)
</dt> </dl>

 

