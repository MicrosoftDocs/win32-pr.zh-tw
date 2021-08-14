---
title: 'TB_SETCOLORSCHEME 訊息 (Commctrl .h) '
description: 設定工具列控制項的色彩配置資訊。
ms.assetid: 96cf6464-b760-46af-910f-984e41dbfca5
keywords:
- TB_SETCOLORSCHEME 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58c6a07c186fd3f5a521719ba0f75f8e468c3868d8ebfaa0595679d48b45089f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167498"
---
# <a name="tb_setcolorscheme-message"></a>TB \_ SETCOLORSCHEME 訊息

設定工具列控制項的色彩配置資訊。

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

當您在控制項中繪製立體元素時，工具列控制項會使用色彩配置資訊。

啟用視覺化樣式時，此訊息不會有任何作用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TB \_ GETCOLORSCHEME**](tb-getcolorscheme.md)
</dt> </dl>

 

 





