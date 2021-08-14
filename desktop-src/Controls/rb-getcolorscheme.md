---
title: 'RB_GETCOLORSCHEME 訊息 (Commctrl .h) '
description: 從 Rebar 控制項抓取色彩配置資訊。
ms.assetid: 01f81c4b-bbc9-43ae-a1f5-1e289c6fa278
keywords:
- RB_GETCOLORSCHEME 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- RB_GETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b918b46d1077c0074584be2d609d486097cc2e40f7a5c62a03db914fce58e320
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169618"
---
# <a name="rb_getcolorscheme-message"></a>RB \_ GETCOLORSCHEME 訊息

從 Rebar 控制項抓取色彩配置資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme)結構的指標，此結構會接收色彩配置資訊。 在傳送此訊息之前，您必須將此結構的 **dwSize** 成員設定為 **sizeof** (COLORSCHEME) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RB \_ SETCOLORSCHEME**](rb-setcolorscheme.md)
</dt> </dl>

 

 





