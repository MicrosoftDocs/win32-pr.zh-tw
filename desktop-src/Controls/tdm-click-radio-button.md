---
title: 'TDM_CLICK_RADIO_BUTTON 訊息 (Commctrl .h) '
description: 模擬選項按鈕在工作對話方塊中按一下的動作。
ms.assetid: ad1616fc-f64d-4575-8bd1-7ce63185d725
keywords:
- TDM_CLICK_RADIO_BUTTON 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TDM_CLICK_RADIO_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80c1eb7e72030a3c2dadc61bfd90027dab032c3342a25c72e4da9dd9a7338142
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104658"
---
# <a name="tdm_click_radio_button-message"></a>TDM \_ 按一下 \_ 單選 \_ 按鈕訊息

模擬選項按鈕在工作對話方塊中按一下的動作。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

**Int** 值，指定要按一下之選項按鈕的識別碼。

</dd> <dt>

*lParam* \[在\]
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="remarks"></a>備註

指定的選項按鈕識別碼會傳送至 [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) 回呼函式，做為 [TDN \_ 單選 \_ 按鈕 \_](tdn-radio-button-clicked.md) 的按下通知程式碼的一部分。 回呼函數傳回之後，將會選取選項按鈕。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

