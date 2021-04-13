---
title: 'RB_SETTEXTCOLOR 訊息 (Commctrl .h) '
description: 設定 Rebar 控制項的預設文字色彩。
ms.assetid: 85f120bd-39aa-43f8-a794-3bb4f3fe1cd4
keywords:
- RB_SETTEXTCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- RB_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68311572927f2e8dac623c697ac366d37d7ab5fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466069"
---
# <a name="rb_settextcolor-message"></a>RB \_ SETTEXTCOLOR 訊息

設定 Rebar 控制項的預設文字色彩。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**COLORREF**](/windows/desktop/gdi/colorref) 值，表示新的預設文字色彩。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回代表先前預設文字色彩的 [**COLORREF**](/windows/desktop/gdi/colorref) 值。

## <a name="remarks"></a>備註

Rebar 控制項的預設文字色彩用來繪製 Rebar 控制項中的文字，以及在傳送此訊息之後加入的所有群組。 藉由在 \_ **fMask** 中設定 RBBIM 色彩旗標，並在 [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)結構中設定 **clrBack** ，即可覆寫特定頻外的預設文字色彩。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RB \_ GETTEXTCOLOR**](rb-gettextcolor.md)
</dt> </dl>

 

