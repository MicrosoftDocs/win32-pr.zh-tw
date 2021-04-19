---
title: 'PSM_SHOWWIZBUTTONS 訊息 (Prsht.idl .h) '
description: 顯示或隱藏嚮導中的按鈕。 您可以使用 PropSheet ShowWizButtons 宏明確地傳送此訊息 \_ 。
ms.assetid: 669c4e51-cac1-40e1-8f23-afae0e41fc9b
keywords:
- PSM_SHOWWIZBUTTONS message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_SHOWWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22e8d1fc54d556240ef3fa6d6b6185a669978b84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967721"
---
# <a name="psm_showwizbuttons-message"></a><span data-ttu-id="10378-105">PSM \_ SHOWWIZBUTTONS 訊息</span><span class="sxs-lookup"><span data-stu-id="10378-105">PSM\_SHOWWIZBUTTONS message</span></span>

<span data-ttu-id="10378-106">顯示或隱藏嚮導中的按鈕。</span><span class="sxs-lookup"><span data-stu-id="10378-106">Shows or hides buttons in a wizard.</span></span> <span data-ttu-id="10378-107">您可以使用 [**PropSheet \_ ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="10378-107">You can send this message explicitly or by using the [**PropSheet\_ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="10378-108">參數</span><span class="sxs-lookup"><span data-stu-id="10378-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10378-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="10378-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10378-110">下列其中一個或多個值，可指定要顯示的屬性工作表按鈕。</span><span class="sxs-lookup"><span data-stu-id="10378-110">One or more of the following values that specify which property sheet buttons are to be shown.</span></span> <span data-ttu-id="10378-111">如果這個參數和 *lParam* 中包含一個按鈕值，就會顯示它。</span><span class="sxs-lookup"><span data-stu-id="10378-111">If a button value is included in both this parameter and *lParam*, it is shown.</span></span>



| <span data-ttu-id="10378-112">值</span><span class="sxs-lookup"><span data-stu-id="10378-112">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="10378-113">意義</span><span class="sxs-lookup"><span data-stu-id="10378-113">Meaning</span></span>                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="10378-114"><dt>**PSWIZB \_ 回來**</dt></span><span class="sxs-lookup"><span data-stu-id="10378-114"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="10378-115">[ **上一頁** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="10378-115">The **Back** button.</span></span><br/>                                                            |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <span data-ttu-id="10378-116"><dt>**PSWIZB \_ 取消**</dt></span><span class="sxs-lookup"><span data-stu-id="10378-116"><dt>**PSWIZB\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="10378-117">[ **取消** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="10378-117">The **Cancel** button.</span></span><br/>                                                          |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="10378-118"><dt>**PSWIZB \_ DISABLEDFINISH**</dt></span><span class="sxs-lookup"><span data-stu-id="10378-118"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="10378-119">[ **完成]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="10378-119">The **Finish** button.</span></span><br/>                                                          |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="10378-120"><dt>**PSWIZB \_ 完成**</dt></span><span class="sxs-lookup"><span data-stu-id="10378-120"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="10378-121">[ **完成]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="10378-121">The **Finish** button.</span></span><br/>                                                          |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="10378-122"><dt>**PSWIZB \_ 下一步**</dt></span><span class="sxs-lookup"><span data-stu-id="10378-122"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="10378-123">[ **下一步]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="10378-123">The **Next** button.</span></span><br/>                                                            |
| <span id="PSWIZB_SHOW"></span><span id="pswizb_show"></span><dl> <span data-ttu-id="10378-124"><dt>**PSWIZB \_ SHOW**</dt></span><span class="sxs-lookup"><span data-stu-id="10378-124"><dt>**PSWIZB\_SHOW**</dt></span></span> </dl>                               | <span data-ttu-id="10378-125">僅設定此旗標 (定義為零) 以隱藏 *lParam* 中指定的所有按鈕。</span><span class="sxs-lookup"><span data-stu-id="10378-125">Set only this flag (defined as zero) to hide all buttons specified in *lParam*.</span></span><br/> |
| <span id="PSWIZB_RESTORE"></span><span id="pswizb_restore"></span><dl> <span data-ttu-id="10378-126"><dt>**PSWIZB \_ 還原**</dt></span><span class="sxs-lookup"><span data-stu-id="10378-126"><dt>**PSWIZB\_RESTORE**</dt></span></span> </dl>                      | <span data-ttu-id="10378-127">未實作。</span><span class="sxs-lookup"><span data-stu-id="10378-127">Not implemented.</span></span><br/>                                                                |



 

</dd> <dt>

<span data-ttu-id="10378-128">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10378-128">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10378-129">*WParam* 中使用的一或多個相同值，指定受此呼叫影響的按鈕。</span><span class="sxs-lookup"><span data-stu-id="10378-129">One or more of the same values used in *wParam*, specifying which buttons are affected by this call.</span></span> <span data-ttu-id="10378-130">如果按鈕值顯示在此參數中，但未出現在 *wParam* 中，則會隱藏該按鈕。</span><span class="sxs-lookup"><span data-stu-id="10378-130">If a button value appears in this parameter but not in *wParam*, the button is hidden.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10378-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="10378-131">Return value</span></span>

<span data-ttu-id="10378-132">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="10378-132">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="10378-133">備註</span><span class="sxs-lookup"><span data-stu-id="10378-133">Remarks</span></span>

<span data-ttu-id="10378-134">嚮導會在每個頁面下方顯示三個或四個按鈕。</span><span class="sxs-lookup"><span data-stu-id="10378-134">Wizards display either three or four buttons below each page.</span></span> <span data-ttu-id="10378-135">此訊息是用來指定哪些按鈕是可見的。</span><span class="sxs-lookup"><span data-stu-id="10378-135">This message is used to specify which buttons are visible.</span></span> <span data-ttu-id="10378-136">嚮導通常會顯示 [ **上一頁**]、[ **取消**] 和 **[下一步** **] 或 [完成]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="10378-136">Wizards normally display **Back**, **Cancel**, and either a **Next** or **Finish** button.</span></span> <span data-ttu-id="10378-137">[ **取消** ] 按鈕一律可見。</span><span class="sxs-lookup"><span data-stu-id="10378-137">The **Cancel** button is always visible.</span></span>

<span data-ttu-id="10378-138">一般而言，設定 **PSWIZB \_ FINISH** 或 **PSWIZB \_ DISABLEDFINISH** ，以 **[完成**] 按鈕取代 [**下一步**] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="10378-138">Typically, set **PSWIZB\_FINISH** or **PSWIZB\_DISABLEDFINISH** to replace the **Next** button with a **Finish** button.</span></span> <span data-ttu-id="10378-139">若要同時顯示 **[下一個**] 和 **[完成]** 按鈕，請在建立嚮導時，于 [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)結構的 **dwFlags** 成員中設定 **PSH \_ WIZARDHASFINISH** 旗標。</span><span class="sxs-lookup"><span data-stu-id="10378-139">To display **Next** and **Finish** buttons simultaneously, set the **PSH\_WIZARDHASFINISH** flag in the **dwFlags** member of the [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) structure when you create the wizard.</span></span> <span data-ttu-id="10378-140">然後每個頁面都會顯示四個按鈕： [ **上一頁** **]、[下一頁]**、[ **取消** **] 和 [完成]**。</span><span class="sxs-lookup"><span data-stu-id="10378-140">Every page will then display all four buttons: **Back**, **Next**, **Cancel**, and **Finish**.</span></span>

<span data-ttu-id="10378-141">如果您使用 [**PropSheet \_ ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) 宏來傳送此訊息，則會將它張貼。</span><span class="sxs-lookup"><span data-stu-id="10378-141">If you use the [**PropSheet\_ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) macro to send this message, it will be posted.</span></span> <span data-ttu-id="10378-142">您可以在任何時候使用 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 來傳送 **PSM \_ SHOWWIZBUTTONS**。</span><span class="sxs-lookup"><span data-stu-id="10378-142">At any other time, you can use [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) to send **PSM\_SHOWWIZBUTTONS**.</span></span>

<span data-ttu-id="10378-143">如果您的通知處理常式使用 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 來傳送 **PSM \_ SHOWWIZBUTTONS** 訊息，則在處理常式傳回之前，不會影響視窗焦點。</span><span class="sxs-lookup"><span data-stu-id="10378-143">If your notification handler uses [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) to send a **PSM\_SHOWWIZBUTTONS** message, do nothing that will affect window focus until after the handler returns.</span></span> <span data-ttu-id="10378-144">例如，如果您在使用 **PostMessage** 傳送 **PSM \_ SHOWWIZBUTTONS** 之後立即呼叫 [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) ，則訊息方塊將會獲得焦點。</span><span class="sxs-lookup"><span data-stu-id="10378-144">For example, if you call [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) immediately after using **PostMessage** to send **PSM\_SHOWWIZBUTTONS**, the message box will receive focus.</span></span> <span data-ttu-id="10378-145">由於張貼的訊息在到達訊息佇列的標頭之前不會傳遞，所以在嚮導失去焦點至訊息方塊之前，將不會傳遞 **PSM \_ SHOWWIZBUTTONS** 訊息。</span><span class="sxs-lookup"><span data-stu-id="10378-145">Since posted messages are not delivered until they reach the head of the message queue, the **PSM\_SHOWWIZBUTTONS** message will not be delivered until after the wizard has lost focus to the message box.</span></span> <span data-ttu-id="10378-146">如此一來，屬性工作表將無法正確設定按鈕的焦點。</span><span class="sxs-lookup"><span data-stu-id="10378-146">As a result, the property sheet will not be able to properly set the focus for the buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="10378-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="10378-147">Requirements</span></span>



| <span data-ttu-id="10378-148">需求</span><span class="sxs-lookup"><span data-stu-id="10378-148">Requirement</span></span> | <span data-ttu-id="10378-149">值</span><span class="sxs-lookup"><span data-stu-id="10378-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="10378-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10378-150">Minimum supported client</span></span><br/> | <span data-ttu-id="10378-151">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10378-151">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="10378-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10378-152">Minimum supported server</span></span><br/> | <span data-ttu-id="10378-153">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10378-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="10378-154">標頭</span><span class="sxs-lookup"><span data-stu-id="10378-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="10378-155"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="10378-155"><dt>Prsht.h</dt></span></span> </dl> |



 

