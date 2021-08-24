---
title: 'EM_GETUNDONAME 訊息 (Richedit .h) '
description: Microsoft Rich Edit 2.0 和更新版本會捕獲下一個復原動作的類型（如果有的話）。Microsoft Rich Edit 1.0 不支援此訊息。
ms.assetid: 43351909-f8bc-425a-9d9b-655e3b47eb75
keywords:
- EM_GETUNDONAME 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETUNDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d133038c0adad2fe7eaa1ae98cf638fe6bd13fad82df3b3d2d1ac384a30e1a80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576638"
---
# <a name="em_getundoname-message"></a>EM \_ GETUNDONAME 訊息

Microsoft Rich Edit 2.0 和更新版本：抓取下一個復原動作的型別（如果有的話）。

Microsoft Rich Edit 1.0：不支援此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果有復原動作，傳回的值會是 [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) 列舉值，指出控制項復原佇列中下一個動作的類型。

如果沒有可復原的動作，或下一個復原動作的類型未知，則傳回值為零。

## <a name="remarks"></a>備註

可以復原或重做的動作類型包括輸入、刪除、拖放、卸載、剪下和貼上作業。 這項資訊對於提供復原和重做作業擴充使用者介面的應用程式很有用，例如可復原之動作的下拉式清單方塊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ GETREDONAME**](em-getredoname.md)
</dt> <dt>

[**EM \_ 重做**](em-redo.md)
</dt> <dt>

[**EM \_ 復原**](em-undo.md)
</dt> <dt>

[**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





