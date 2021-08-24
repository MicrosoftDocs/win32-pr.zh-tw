---
title: 'TTM_NEWTOOLRECT 訊息 (Commctrl .h) '
description: 設定工具的新周框矩形。
ms.assetid: 81d1b745-310e-482e-8c6e-6e98e1e67b66
keywords:
- TTM_NEWTOOLRECT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TTM_NEWTOOLRECT
- TTM_NEWTOOLRECTA
- TTM_NEWTOOLRECTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13889b0e9c0d80392b88130c33e5e9723ceb776a60a6b941d205d514d96ca22f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750978"
---
# <a name="ttm_newtoolrect-message"></a>TTM \_ NEWTOOLRECT 訊息

設定工具的新周框矩形。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的指標。 **Hwnd** 和 **uId** 成員會識別工具，而 **rect** 成員會指定新的周框。 傳送此訊息之前，必須先填入此結構的 **cbSize** 成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TTM \_NEWTOOLRECTW** (Unicode) 和 **TTM \_ NEWTOOLRECTA** (ANSI) <br/>           |



 

 





