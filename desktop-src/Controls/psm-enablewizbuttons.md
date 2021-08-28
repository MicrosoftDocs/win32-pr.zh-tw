---
title: 'PSM_ENABLEWIZBUTTONS 訊息 (Prsht.idl .h) '
description: 啟用或停用 Aero wizard 中的任何標準按鈕。 您可以明確地傳送此訊息，或使用 PropSheet \_ EnableWizButtons 宏。
ms.assetid: 9e8ff2dc-c0e7-4754-8be2-2c7b65a524f4
keywords:
- PSM_ENABLEWIZBUTTONS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- PSM_ENABLEWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a677b596e57a55271224f5b22baac5d979e2806c20676065457aa47b8a66e527
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825869"
---
# <a name="psm_enablewizbuttons-message"></a>PSM \_ ENABLEWIZBUTTONS 訊息

啟用或停用 Aero wizard 中的任何標準按鈕。 您可以明確地傳送此訊息，或使用 [**PropSheet \_ EnableWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

下列其中一個或多個值，可指定要啟用的屬性工作表按鈕。 如果這個參數和 *lParam* 中包含一個按鈕值，就會啟用它。



| 值                                                                                                                                                                                 | 意義                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**PSWIZB \_ 回來**</dt> </dl>                               | [ **上一頁** ] 按鈕。<br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <dt>**PSWIZB \_ 取消**</dt> </dl>                         | [ **取消** ] 按鈕。<br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**PSWIZB \_ DISABLEDFINISH**</dt> </dl> | [ **完成]** 按鈕。<br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**PSWIZB \_ 完成**</dt> </dl>                         | [ **完成]** 按鈕。<br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**PSWIZB \_ 下一步**</dt> </dl>                               | [ **下一步]** 按鈕。<br/>   |



 

</dd> <dt>

*lParam* 
</dt> <dd>

*WParam* 中使用的一或多個相同值，指定受此呼叫影響的按鈕。 如果按鈕值出現在此參數中，但未出現在 *wParam* 中，則表示該按鈕應停用。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

 





