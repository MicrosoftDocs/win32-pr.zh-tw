---
title: 'EM_SETBIDIOPTIONS 訊息 (Richedit .h) '
description: EM \_ SETBIDIOPTIONS 訊息會在 rich edit 控制項中設定雙向選項的目前狀態。
ms.assetid: b518e423-317a-4654-9d9f-c501028e2a0a
keywords:
- EM_SETBIDIOPTIONS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84dc4b92f7a989ab5ef283b36708094a143475de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105593"
---
# <a name="em_setbidioptions-message"></a>EM \_ SETBIDIOPTIONS 訊息

**EM \_ SETBIDIOPTIONS** 訊息會在 rich edit 控制項中設定雙向選項的目前狀態。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions)結構的指標，指出如何在 rich edit 控制項中設定雙向選項的狀態。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

Rich edit 控制項必須是純文字模式，否則 **EM \_ SETBIDIOPTIONS** 將不會進行任何動作。

在純文字控制項中， **EM \_ SETBIDIOPTIONS** 會根據內容規則自動判斷段落方向和（或）對齊。 這些規則會指出方向和/或對齊衍生自控制項中的第一個強字元。 強字元是指可從中判斷文字方向的字元 (請參閱 Unicode 標準2.0 版) 。 段落方向和/或對齊會套用至預設格式。

**EM \_SETBIDIOPTIONS** 只會將預設段落格式切換為 rtl (由右至左) 如果找到 RTL 字元，

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 可轉散發套件<br/>          | Rich Edit 3。0<br/>                                                              |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[**EM \_ GETBIDIOPTIONS**](em-getbidioptions.md)
</dt> </dl>

 

 





