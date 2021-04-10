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
# <a name="psm_setwizbuttons-message"></a>PSM \_ SETWIZBUTTONS 訊息

啟用或停用 wizard 中的 [ **上一頁**]、 **[下一頁**] 和 **[完成** ] 按鈕。 您也可以使用 [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) 宏來張貼訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

將此參數設定為 PSWIZBF \_ ELE加值稅IONREQUIRED，以在 *lParam* 中指定的按鈕上顯示提高許可權的圖示。 提高許可權的圖示 (或 UAC 防護圖示) 指出將使用提高許可權提示來提示使用者提供核准或認證。 如需詳細資訊，請參閱 [設計適用于 Windows Vista 的 UAC 應用程式]( /previous-versions/bb756973(v=msdn.10))。

> [!Note]  
> 只有 AeroWizards (PSH AEROWIZARD) 才支援顯示 UAC 防護圖示 \_ 。

 

</dd> <dt>

*lParam* 
</dt> <dd>

值，指定要啟用的屬性工作表按鈕。 您可以結合下列一或多個旗標。



| 值                                                                                                                                                                                 | 意義                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**PSWIZB \_ 回來**</dt> </dl>                               | 啟用 [ **上一頁** ] 按鈕。 如果未設定此旗標，[ **上一頁** ] 按鈕會顯示為 [已停用]。<br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**PSWIZB \_ DISABLEDFINISH**</dt> </dl> | 顯示已停用的 **[完成]** 按鈕。<br/>                                                              |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**PSWIZB \_ 完成**</dt> </dl>                         | 顯示已啟用的 **[完成]** 按鈕。<br/>                                                              |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**PSWIZB \_ 下一步**</dt> </dl>                               | 啟用 [下一步] 按鈕。 如果未設定此旗標，[ **下一步]** 按鈕會顯示為停用。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

如果您的通知處理常式使用 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 來傳送 **PSM \_ SETWIZBUTTONS** 訊息，則在處理常式傳回之前，不會影響視窗焦點。 例如，如果您在使用 **PostMessage** 傳送 **PSM \_ SETWIZBUTTONS** 之後立即呼叫 [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) ，則訊息方塊將會獲得焦點。 由於張貼的訊息在到達訊息佇列的標頭之前不會傳遞，所以在嚮導失去焦點至訊息方塊之前，將不會傳遞 **PSM \_ SETWIZBUTTONS** 訊息。 如此一來，屬性工作表將無法正確設定按鈕的焦點。

如果您在 \_ 處理 [PSN \_ advanced.field.setactive](psn-setactive.md) 通知時傳送 PSM SETWIZBUTTONS 訊息，請使用 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 函式，而不是 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 函數。 否則，系統將不會正確更新按鈕。 如果您使用 [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) 宏來傳送此訊息，則會將它張貼。 您可以在任何時候使用 **SendMessage** 來傳送 **PSM \_ SETWIZBUTTONS**。

嚮導會在每個頁面下方顯示三個或四個按鈕。 此訊息是用來指定哪些按鈕已啟用。 嚮導通常會顯示 [ **上一頁**]、[ **取消**] 和 **[下一步** **] 或 [完成]** 按鈕。 您通常只會啟用 [歡迎使用] 頁面的 [**下一步** **] 按鈕、內部** 頁面，以及 [完成] 頁面的 [**上** 一步]**和** **[完成]** 。 [ **取消** ] 按鈕一律為啟用狀態。 一般來說，設定 PSWIZB \_ FINISH 或 PSWIZB \_ DISABLEDFINISH 會以 **[完成]** 按鈕取代 [**下一步**] 按鈕。 若要同時顯示 **[下一個**] 和 **[完成**] 按鈕，請在 \_ 建立嚮導時，于 wizard [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)結構的 **dwFlags** 成員中設定 PSH WIZARDHASFINISH 旗標。 然後每個頁面都會顯示四個按鈕。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

