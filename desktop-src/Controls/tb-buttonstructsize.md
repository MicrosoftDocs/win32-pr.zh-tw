---
title: 'TB_BUTTONSTRUCTSIZE 訊息 (Commctrl .h) '
description: 指定 TBBUTTON 結構的大小。
ms.assetid: 4e63a075-4191-44c1-8df6-38fce51d4be5
keywords:
- TB_BUTTONSTRUCTSIZE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_BUTTONSTRUCTSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceed10eec9038b338d060f28acdab8a10aa88aecef6b264b6d6d0682168f4937
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919138"
---
# <a name="tb_buttonstructsize-message"></a>TB \_ BUTTONSTRUCTSIZE 訊息

指定 [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) 結構的大小。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)結構的大小（以位元組為單位）。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

系統會使用大小來判斷所使用的通用控制項動態連結程式庫 () 版本。

如果應用程式使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立工具列，則應用程式必須在傳送 [**TB \_ ADDBITMAP**](tb-addbitmap.md) 或 [**tb \_ ADDBUTTONS**](tb-addbuttons.md) 訊息之前，將此訊息傳送至工具列。 [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex)函式會自動傳送 **TB 的 \_ BUTTONSTRUCTSIZE**，而 [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)結構的大小是函數的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

