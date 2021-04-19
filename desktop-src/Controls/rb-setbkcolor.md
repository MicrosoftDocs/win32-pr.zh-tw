---
title: 'RB_SETBKCOLOR 訊息 (Commctrl .h) '
description: 設定 Rebar 控制項的預設背景色彩。
ms.assetid: 450a1e16-24f6-4f86-8e46-14009da05efc
keywords:
- RB_SETBKCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- RB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9365de2d790b1f28b1330c038b69d30b208143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968173"
---
# <a name="rb_setbkcolor-message"></a>RB \_ SETBKCOLOR 訊息

設定 Rebar 控制項的預設背景色彩。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**COLORREF**](/windows/desktop/gdi/colorref) 值，表示新的預設背景色彩。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回代表先前預設背景色彩的 [**COLORREF**](/windows/desktop/gdi/colorref) 值。

## <a name="remarks"></a>備註

Rebar 控制項的預設背景色彩用來繪製 Rebar 控制項中的背景，以及在傳送此訊息之後加入的所有群組。 藉由在 \_ **fMask** 中設定 RBBIM 色彩旗標，並在 [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)結構中設定 **clrBack** ，即可覆寫特定頻外的預設背景色彩。

啟用視覺化樣式時，此訊息不會有任何作用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RB \_ GETBKCOLOR**](rb-getbkcolor.md)
</dt> </dl>

 

