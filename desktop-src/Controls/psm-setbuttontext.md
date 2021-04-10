---
title: 'PSM_SETBUTTONTEXT 訊息 (Prsht.idl .h) '
description: 設定 Aero wizard 中按鈕的文字。 您可以使用 PropSheet SetButtonText 宏明確地傳送此訊息 \_ 。
ms.assetid: 30b7afd1-5094-430f-9c48-d87832d96050
keywords:
- PSM_SETBUTTONTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_SETBUTTONTEXT
- PSM_SETBUTTONTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41a0b55f73fc7084e89f54c1e741d12000b0f949
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024988"
---
# <a name="psm_setbuttontext-message"></a>PSM \_ SETBUTTONTEXT 訊息

設定 Aero wizard 中按鈕的文字。 您可以使用 [**PropSheet \_ SetButtonText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

下列其中一個值，指定要設定其文字的按鈕。



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

要設定的文字。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **PSM \_SETBUTTONTEXTW** (Unicode) <br/>                                       |



 

 





