---
title: 'RB_SETCOLORSCHEME 訊息 (Commctrl .h) '
description: 設定 Rebar 控制項的色彩配置資訊。
ms.assetid: ddf8f3e4-66b7-4b53-a04e-b4dd372f71c4
keywords:
- RB_SETCOLORSCHEME 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- RB_SETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce7715082a371c3632d8accb8fdf60bbac50d8d7d8182732d6a62c2dbb423c34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169274"
---
# <a name="rb_setcolorscheme-message"></a>RB \_ SETCOLORSCHEME 訊息

設定 Rebar 控制項的色彩配置資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme)結構的指標，其中包含色彩配置資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此訊息的傳回值。

## <a name="remarks"></a>備註

當您在控制項和區段中繪製立體元素時，Rebar 控制項會使用色彩配置資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RB \_ GETCOLORSCHEME**](rb-getcolorscheme.md)
</dt> </dl>

 

 





