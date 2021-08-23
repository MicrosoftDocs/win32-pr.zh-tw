---
title: 'EM_GETBIDIOPTIONS 訊息 (Richedit .h) '
description: 指出 rich edit 控制項中雙向選項的目前狀態。
ms.assetid: 055581c0-ae59-4601-a3e9-416705af429a
keywords:
- EM_GETBIDIOPTIONS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b377e0fd3a439737fea9efbc403d2ccc64d6cf78eab1c7e31feeffd6c4b0f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019906"
---
# <a name="em_getbidioptions-message"></a>EM \_ GETBIDIOPTIONS 訊息

指出 rich edit 控制項中雙向選項的目前狀態。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions)結構，此結構會接收 rich edit 控制項中雙向選項的目前狀態。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

這則訊息會將 **wMask** 和 **wEffects** 成員的值設定為 rich edit 控制項中雙向選項目前狀態的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 可轉散發套件<br/>          | Rich Edit 3。0<br/>                                                              |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[**EM \_ SETBIDIOPTIONS**](em-setbidioptions.md)
</dt> </dl>

 

 





