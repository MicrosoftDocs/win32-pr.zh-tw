---
title: 'PSM_SHOWWIZBUTTONS 訊息 (Prsht.idl .h) '
description: 顯示或隱藏嚮導中的按鈕。 您可以使用 PropSheet ShowWizButtons 宏明確地傳送此訊息 \_ 。
ms.assetid: 669c4e51-cac1-40e1-8f23-afae0e41fc9b
keywords:
- PSM_SHOWWIZBUTTONS 訊息 Windows 控制項
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
ms.openlocfilehash: 86bbad4d6f0ce8a084709c04110d093e4d79b806226bdc1fa651278b4054fa8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088478"
---
# <a name="psm_showwizbuttons-message"></a>PSM \_ SHOWWIZBUTTONS 訊息

顯示或隱藏嚮導中的按鈕。 您可以使用 [**PropSheet \_ ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

下列其中一個或多個值，可指定要顯示的屬性工作表按鈕。 如果這個參數和 *lParam* 中包含一個按鈕值，就會顯示它。



| 值                                                                                                                                                                                 | 意義                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**PSWIZB \_ 回來**</dt> </dl>                               | [ **上一頁** ] 按鈕。<br/>                                                            |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <dt>**PSWIZB \_ 取消**</dt> </dl>                         | [ **取消** ] 按鈕。<br/>                                                          |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**PSWIZB \_ DISABLEDFINISH**</dt> </dl> | [ **完成]** 按鈕。<br/>                                                          |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**PSWIZB \_ 完成**</dt> </dl>                         | [ **完成]** 按鈕。<br/>                                                          |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**PSWIZB \_ 下一步**</dt> </dl>                               | [ **下一步]** 按鈕。<br/>                                                            |
| <span id="PSWIZB_SHOW"></span><span id="pswizb_show"></span><dl> <dt>**PSWIZB \_ SHOW**</dt> </dl>                               | 僅設定此旗標 (定義為零) 以隱藏 *lParam* 中指定的所有按鈕。<br/> |
| <span id="PSWIZB_RESTORE"></span><span id="pswizb_restore"></span><dl> <dt>**PSWIZB \_ 還原**</dt> </dl>                      | 未實作。<br/>                                                                |



 

</dd> <dt>

*lParam* 
</dt> <dd>

*WParam* 中使用的一或多個相同值，指定受此呼叫影響的按鈕。 如果按鈕值顯示在此參數中，但未出現在 *wParam* 中，則會隱藏該按鈕。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

嚮導會在每個頁面下方顯示三個或四個按鈕。 此訊息是用來指定哪些按鈕是可見的。 嚮導通常會顯示 [ **上一頁**]、[ **取消**] 和 **[下一步** **] 或 [完成]** 按鈕。 [ **取消** ] 按鈕一律可見。

一般而言，設定 **PSWIZB \_ FINISH** 或 **PSWIZB \_ DISABLEDFINISH** ，以 **[完成**] 按鈕取代 [**下一步**] 按鈕。 若要同時顯示 **[下一個**] 和 **[完成]** 按鈕，請在建立嚮導時，于 [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)結構的 **dwFlags** 成員中設定 **PSH \_ WIZARDHASFINISH** 旗標。 然後每個頁面都會顯示四個按鈕： [ **上一頁** **]、[下一頁]**、[ **取消** **] 和 [完成]**。

如果您使用 [**PropSheet \_ ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) 宏來傳送此訊息，則會將它張貼。 您可以在任何時候使用 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 來傳送 **PSM \_ SHOWWIZBUTTONS**。

如果您的通知處理常式使用 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 來傳送 **PSM \_ SHOWWIZBUTTONS** 訊息，則在處理常式傳回之前，不會影響視窗焦點。 例如，如果您在使用 **PostMessage** 傳送 **PSM \_ SHOWWIZBUTTONS** 之後立即呼叫 [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) ，則訊息方塊將會獲得焦點。 由於張貼的訊息在到達訊息佇列的標頭之前不會傳遞，所以在嚮導失去焦點至訊息方塊之前，將不會傳遞 **PSM \_ SHOWWIZBUTTONS** 訊息。 如此一來，屬性工作表將無法正確設定按鈕的焦點。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

