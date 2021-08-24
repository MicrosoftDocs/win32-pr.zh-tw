---
title: 'SB_SETBKCOLOR 訊息 (Commctrl .h) '
description: 設定狀態列中的背景色彩。
ms.assetid: 49bcd816-e3e2-45f4-8845-ef67789b8a01
keywords:
- SB_SETBKCOLOR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- SB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b97893d49d475789b07c28e17e88097aa4df4336154d6b4e0f9c4fa081e52635
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637078"
---
# <a name="sb_setbkcolor-message"></a>SB \_ SETBKCOLOR 訊息

設定狀態列中的背景色彩。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**COLORREF**](/windows/desktop/gdi/colorref) 值，指定新的背景色彩。 指定 CLR \_ 預設值，使狀態列使用其預設背景色彩。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回先前的背景色彩，或 \_ 如果背景色彩為預設色彩，則為 CLR 預設值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

