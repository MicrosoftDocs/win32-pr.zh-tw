---
title: 'TB_SETPADDING 訊息 (Commctrl .h) '
description: 設定工具列控制項的邊框距離。
ms.assetid: a18c4efb-1140-4149-8dce-dfc1f03bb61a
keywords:
- TB_SETPADDING 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da488c7aab3a6856fd1bd8db6911336eb52881da396e287937678600158d9655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078162"
---
# <a name="tb_setpadding-message"></a>TB \_ SETPADDING 訊息

設定工具列控制項的邊框距離。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定水準填補（以圖元為單位）。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定垂直填補（以圖元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **DWORD** 值，其中包含 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 中先前的水準填補，以及 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))中先前的垂直填補（以圖元為單位）。

## <a name="remarks"></a>備註

填補值是用來在按鈕的邊緣與按鈕的影像和/或文字之間建立空白區域。 實際套用的填補數量，取決於按鈕的類型，以及是否有影像。 水準填補會套用至按鈕的右邊和左方，而垂直填補會套用至按鈕的頂端和底部。 填補只適用于具有 [**TBSTYLE \_ AUTOSIZE**](toolbar-control-and-button-styles.md) 樣式的按鈕。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TB \_ GETPADDING**](tb-getpadding.md)
</dt> </dl>

 

