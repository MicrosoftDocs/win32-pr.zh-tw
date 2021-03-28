---
description: 指出使用者按下 F1 鍵。
ms.assetid: 6a090125-67dd-4267-9973-10e32c6e4f1f
title: 'WM_HELP 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dd1b042a2e57fb64eb3aa81f38cec336e33efab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973104"
---
# <a name="wm_help-message"></a>WM 說明 \_ 訊息

指出使用者按下 F1 鍵。 如果按下 F1 時，功能表為使用中狀態，則會將 **wm \_** 說明傳送至與功能表相關聯的視窗; 否則，會將 wm 說明傳送至具有鍵盤焦點的視窗。 **\_** 如果沒有任何視窗具有鍵盤焦點， **則 \_ 會將 WM** 說明傳送至目前的使用中視窗。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lphi* 
</dt> <dd>

[**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo)結構的位址，其中包含已要求說明之功能表項目、控制項、對話方塊或視窗的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE**。

## <a name="remarks"></a>備註

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會將 WM 說明傳遞給子視窗的父視窗，或傳遞至最上層視窗的擁有者。 **\_**

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Winuser。h</dt> </dl> |



 

 
