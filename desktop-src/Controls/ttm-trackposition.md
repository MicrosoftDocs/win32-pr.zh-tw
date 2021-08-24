---
title: 'TTM_TRACKPOSITION 訊息 (Commctrl .h) '
description: 設定追蹤工具提示的位置。
ms.assetid: 9eb7c86c-78e6-442a-ad77-5fb919cab591
keywords:
- TTM_TRACKPOSITION 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TTM_TRACKPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 547af5014bbf897d320894c4924911b830997ec3d8532e2ce2c7b63f361a11da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119542821"
---
# <a name="ttm_trackposition-message"></a>TTM \_ TRACKPOSITION 訊息

設定追蹤工具提示的位置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定要顯示追蹤工具提示之點的 x 座標（以螢幕座標表示）。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定顯示追蹤工具提示的點 y 座標（以螢幕座標表示）。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此訊息的傳回值。

## <a name="remarks"></a>備註

工具提示控制項會根據您在此訊息中提供的座標，選擇要顯示工具提示視窗的位置。 這會導致工具提示視窗顯示在其所對應的工具旁邊。 若要在特定座標顯示工具提示視窗，加入 \_ 工具時，請在 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的 **UFLAGS** 成員中包含 TTF 絕對旗標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**TTM \_ TRACKACTI加值稅E**](ttm-trackactivate.md)
</dt> <dt>

**概念**
</dt> <dt>

[使用工具提示控制項](using-tooltip-contro.md)
</dt> </dl>

 

