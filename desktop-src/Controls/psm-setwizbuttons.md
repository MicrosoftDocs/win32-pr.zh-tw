---
title: 'PSM_SETWIZBUTTONS 訊息 (Prsht.idl .h) '
description: 啟用或停用 wizard 中的 [上一頁]、[下一頁] 和 [完成] 按鈕。 您也可以使用 PropSheet \_ SetWizButtons 宏來張貼訊息。
ms.assetid: e32abdb0-12d1-471e-a309-662389e0dba4
keywords:
- PSM_SETWIZBUTTONS message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_SETWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e79cb7b6fbc0c91e1e94df62c2c8401839ace2d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104195"
---
# <a name="psm_setwizbuttons-message"></a><span data-ttu-id="65349-105">PSM \_ SETWIZBUTTONS 訊息</span><span class="sxs-lookup"><span data-stu-id="65349-105">PSM\_SETWIZBUTTONS message</span></span>

<span data-ttu-id="65349-106">啟用或停用 wizard 中的 [ **上一頁**]、 **[下一頁**] 和 **[完成** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="65349-106">Enables or disables the **Back**, **Next**, and **Finish** buttons in a wizard.</span></span> <span data-ttu-id="65349-107">您也可以使用 [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) 宏來張貼訊息。</span><span class="sxs-lookup"><span data-stu-id="65349-107">You can also use the [**PropSheet\_SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) macro to post the message.</span></span>

## <a name="parameters"></a><span data-ttu-id="65349-108">參數</span><span class="sxs-lookup"><span data-stu-id="65349-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65349-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="65349-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="65349-110">將此參數設定為 PSWIZBF \_ ELE加值稅IONREQUIRED，以在 *lParam* 中指定的按鈕上顯示提高許可權的圖示。</span><span class="sxs-lookup"><span data-stu-id="65349-110">Set this parameter to PSWIZBF\_ELEVATIONREQUIRED to display the elevated icon on the buttons specified in *lParam*.</span></span> <span data-ttu-id="65349-111">提高許可權的圖示 (或 UAC 防護圖示) 指出將使用提高許可權提示來提示使用者提供核准或認證。</span><span class="sxs-lookup"><span data-stu-id="65349-111">The elevated icon (or UAC shield icon) indicates that the elevation prompt will be used to prompt the user for approval or credentials.</span></span> <span data-ttu-id="65349-112">如需詳細資訊，請參閱 [設計適用于 Windows Vista 的 UAC 應用程式]( /previous-versions/bb756973(v=msdn.10))。</span><span class="sxs-lookup"><span data-stu-id="65349-112">For more information, see [Designing UAC Applications for Windows Vista]( /previous-versions/bb756973(v=msdn.10)).</span></span>

> [!Note]  
> <span data-ttu-id="65349-113">只有 AeroWizards (PSH AEROWIZARD) 才支援顯示 UAC 防護圖示 \_ 。</span><span class="sxs-lookup"><span data-stu-id="65349-113">Displaying the UAC shield icon is only supported in AeroWizards (PSH\_AEROWIZARD).</span></span>

 

</dd> <dt>

<span data-ttu-id="65349-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="65349-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="65349-115">值，指定要啟用的屬性工作表按鈕。</span><span class="sxs-lookup"><span data-stu-id="65349-115">Value that specifies which property sheet buttons are enabled.</span></span> <span data-ttu-id="65349-116">您可以結合下列一或多個旗標。</span><span class="sxs-lookup"><span data-stu-id="65349-116">You can combine one or more of the following flags.</span></span>



| <span data-ttu-id="65349-117">值</span><span class="sxs-lookup"><span data-stu-id="65349-117">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="65349-118">意義</span><span class="sxs-lookup"><span data-stu-id="65349-118">Meaning</span></span>                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="65349-119"><dt>**PSWIZB \_ 回來**</dt></span><span class="sxs-lookup"><span data-stu-id="65349-119"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="65349-120">啟用 [ **上一頁** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="65349-120">Enables the **Back** button.</span></span> <span data-ttu-id="65349-121">如果未設定此旗標，[ **上一頁** ] 按鈕會顯示為 [已停用]。</span><span class="sxs-lookup"><span data-stu-id="65349-121">If this flag is not set, the **Back** button is displayed as disabled.</span></span><br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="65349-122"><dt>**PSWIZB \_ DISABLEDFINISH**</dt></span><span class="sxs-lookup"><span data-stu-id="65349-122"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="65349-123">顯示已停用的 **[完成]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="65349-123">Displays a disabled **Finish** button.</span></span><br/>                                                              |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="65349-124"><dt>**PSWIZB \_ 完成**</dt></span><span class="sxs-lookup"><span data-stu-id="65349-124"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="65349-125">顯示已啟用的 **[完成]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="65349-125">Displays an enabled **Finish** button.</span></span><br/>                                                              |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="65349-126"><dt>**PSWIZB \_ 下一步**</dt></span><span class="sxs-lookup"><span data-stu-id="65349-126"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="65349-127">啟用 [下一步] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="65349-127">Enables the **Next** button.</span></span> <span data-ttu-id="65349-128">如果未設定此旗標，[ **下一步]** 按鈕會顯示為停用。</span><span class="sxs-lookup"><span data-stu-id="65349-128">If this flag is not set, the **Next** button is displayed as disabled.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65349-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="65349-129">Return value</span></span>

<span data-ttu-id="65349-130">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="65349-130">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="65349-131">備註</span><span class="sxs-lookup"><span data-stu-id="65349-131">Remarks</span></span>

<span data-ttu-id="65349-132">如果您的通知處理常式使用 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 來傳送 **PSM \_ SETWIZBUTTONS** 訊息，則在處理常式傳回之前，不會影響視窗焦點。</span><span class="sxs-lookup"><span data-stu-id="65349-132">If your notification handler uses [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) to send a **PSM\_SETWIZBUTTONS** message, do nothing that will affect window focus until after the handler returns.</span></span> <span data-ttu-id="65349-133">例如，如果您在使用 **PostMessage** 傳送 **PSM \_ SETWIZBUTTONS** 之後立即呼叫 [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) ，則訊息方塊將會獲得焦點。</span><span class="sxs-lookup"><span data-stu-id="65349-133">For example, if you call [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) immediately after using **PostMessage** to send **PSM\_SETWIZBUTTONS**, the message box will receive focus.</span></span> <span data-ttu-id="65349-134">由於張貼的訊息在到達訊息佇列的標頭之前不會傳遞，所以在嚮導失去焦點至訊息方塊之前，將不會傳遞 **PSM \_ SETWIZBUTTONS** 訊息。</span><span class="sxs-lookup"><span data-stu-id="65349-134">Since posted messages are not delivered until they reach the head of the message queue, the **PSM\_SETWIZBUTTONS** message will not be delivered until after the wizard has lost focus to the message box.</span></span> <span data-ttu-id="65349-135">如此一來，屬性工作表將無法正確設定按鈕的焦點。</span><span class="sxs-lookup"><span data-stu-id="65349-135">As a result, the property sheet will not be able to properly set the focus for the buttons.</span></span>

<span data-ttu-id="65349-136">如果您在 \_ 處理 [PSN \_ advanced.field.setactive](psn-setactive.md) 通知時傳送 PSM SETWIZBUTTONS 訊息，請使用 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 函式，而不是 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 函數。</span><span class="sxs-lookup"><span data-stu-id="65349-136">If you send the PSM\_SETWIZBUTTONS message during your handling of the [PSN\_SETACTIVE](psn-setactive.md) notification, use the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function rather than the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function.</span></span> <span data-ttu-id="65349-137">否則，系統將不會正確更新按鈕。</span><span class="sxs-lookup"><span data-stu-id="65349-137">Otherwise, the system will not update the buttons properly.</span></span> <span data-ttu-id="65349-138">如果您使用 [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) 宏來傳送此訊息，則會將它張貼。</span><span class="sxs-lookup"><span data-stu-id="65349-138">If you use the [**PropSheet\_SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) macro to send this message, it will be posted.</span></span> <span data-ttu-id="65349-139">您可以在任何時候使用 **SendMessage** 來傳送 **PSM \_ SETWIZBUTTONS**。</span><span class="sxs-lookup"><span data-stu-id="65349-139">At any other time, you can use **SendMessage** to send **PSM\_SETWIZBUTTONS**.</span></span>

<span data-ttu-id="65349-140">嚮導會在每個頁面下方顯示三個或四個按鈕。</span><span class="sxs-lookup"><span data-stu-id="65349-140">Wizards display either three or four buttons below each page.</span></span> <span data-ttu-id="65349-141">此訊息是用來指定哪些按鈕已啟用。</span><span class="sxs-lookup"><span data-stu-id="65349-141">This message is used to specify which buttons are enabled.</span></span> <span data-ttu-id="65349-142">嚮導通常會顯示 [ **上一頁**]、[ **取消**] 和 **[下一步** **] 或 [完成]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="65349-142">Wizards normally display **Back**, **Cancel**, and either a **Next** or **Finish** button.</span></span> <span data-ttu-id="65349-143">您通常只會啟用 [歡迎使用] 頁面的 [**下一步** **] 按鈕、內部** 頁面，以及 [完成] 頁面的 [**上** 一步]**和** **[完成]** 。</span><span class="sxs-lookup"><span data-stu-id="65349-143">You typically enable only the **Next** button for the welcome page, **Next** and **Back** for interior pages, and **Back** and **Finish** for the completion page.</span></span> <span data-ttu-id="65349-144">[ **取消** ] 按鈕一律為啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="65349-144">The **Cancel** button is always enabled.</span></span> <span data-ttu-id="65349-145">一般來說，設定 PSWIZB \_ FINISH 或 PSWIZB \_ DISABLEDFINISH 會以 **[完成]** 按鈕取代 [**下一步**] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="65349-145">Normally, setting PSWIZB\_FINISH or PSWIZB\_DISABLEDFINISH replaces the **Next** button with a **Finish** button.</span></span> <span data-ttu-id="65349-146">若要同時顯示 **[下一個**] 和 **[完成**] 按鈕，請在 \_ 建立嚮導時，于 wizard [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)結構的 **dwFlags** 成員中設定 PSH WIZARDHASFINISH 旗標。</span><span class="sxs-lookup"><span data-stu-id="65349-146">To display **Next** and **Finish** buttons simultaneously, set the PSH\_WIZARDHASFINISH flag in the **dwFlags** member of the wizard's [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) structure when you create the wizard.</span></span> <span data-ttu-id="65349-147">然後每個頁面都會顯示四個按鈕。</span><span class="sxs-lookup"><span data-stu-id="65349-147">Every page will then display all four buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="65349-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="65349-148">Requirements</span></span>



| <span data-ttu-id="65349-149">需求</span><span class="sxs-lookup"><span data-stu-id="65349-149">Requirement</span></span> | <span data-ttu-id="65349-150">值</span><span class="sxs-lookup"><span data-stu-id="65349-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="65349-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65349-151">Minimum supported client</span></span><br/> | <span data-ttu-id="65349-152">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65349-152">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="65349-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65349-153">Minimum supported server</span></span><br/> | <span data-ttu-id="65349-154">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65349-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="65349-155">標頭</span><span class="sxs-lookup"><span data-stu-id="65349-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="65349-156"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="65349-156"><dt>Prsht.h</dt></span></span> </dl> |



 

