---
title: 'TDM_CLICK_BUTTON 訊息 (Commctrl .h) '
description: 模擬按鈕在工作對話方塊中按一下的動作。
ms.assetid: cc8a8252-3418-4a28-bfb7-11d6e3fee903
keywords:
- TDM_CLICK_BUTTON message Windows 控制項
topic_type:
- apiref
api_name:
- TDM_CLICK_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e5933668eca907f36414113091b8901bfb9c110
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "107001105"
---
# <a name="tdm_click_button-message"></a>TDM \_ CLICK \_ 按鈕訊息

模擬按鈕在工作對話方塊中按一下的動作。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

**整數**，指定要按一下之按鈕的識別碼。

</dd> <dt>

*lParam* \[在\]
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="remarks"></a>備註

*WParam* 所指定的按鈕識別碼會傳送至 [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback)回呼函式，作為 [TDN \_ 按鈕 \_](tdn-button-clicked.md)按下通知程式碼的一部分。 回呼函式傳回之後，如果 \_ 從回呼函數傳回 S OK，工作對話方塊就會關閉。 如果 \_ 從回呼函式傳回 FALSE，工作對話方塊會維持使用中狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

