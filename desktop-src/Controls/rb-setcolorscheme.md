---
title: 'RB_SETCOLORSCHEME 訊息 (Commctrl .h) '
description: 設定 Rebar 控制項的色彩配置資訊。
ms.assetid: ddf8f3e4-66b7-4b53-a04e-b4dd372f71c4
keywords:
- RB_SETCOLORSCHEME message Windows 控制項
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
ms.openlocfilehash: b9c7725d3c0bc3f3a7a7a72db16e19626a3c4d2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508699"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RB \_ GETCOLORSCHEME**](rb-getcolorscheme.md)
</dt> </dl>

 

 





