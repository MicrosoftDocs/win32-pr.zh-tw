---
title: 'EM_GETTEXTLENGTHEX 訊息 (Richedit .h) '
description: 以各種方式計算文字長度。 通常會在建立緩衝區之前呼叫，以接收控制項的文字。
ms.assetid: 42c89b7b-e48d-4517-9993-ce58ff9e4e40
keywords:
- EM_GETTEXTLENGTHEX message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETTEXTLENGTHEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2d91674e07ef60c2ce95535983a31cf380f9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843480"
---
# <a name="em_gettextlengthex-message"></a>EM \_ GETTEXTLENGTHEX 訊息

以各種方式計算文字長度。 通常會在建立緩衝區之前呼叫，以接收控制項的文字。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex)結構的指標，此結構會接收文字長度資訊。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

訊息會根據 [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex)結構中的旗標設定，傳回編輯控制項中的 **TCHAR** 數目。 如果 **旗** 標成員中設定了不相容的旗標，訊息會傳回 E \_ INVALIDARG。

## <a name="remarks"></a>備註

這則訊息是一種快速且簡單的方式，可判斷 rich edit 控制項的 Unicode 版本中的字元數。 不過，對於非 Unicode 目標字碼頁，您可能會轉換成單一位元組和雙位元組字元的組合。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex)
</dt> </dl>

 

 





