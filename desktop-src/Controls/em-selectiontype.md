---
title: 'EM_SELECTIONTYPE 訊息 (Richedit .h) '
description: 判斷 rich edit 控制項的選取專案類型。
ms.assetid: a4200e32-1056-47bd-be47-5fabaf99c058
keywords:
- EM_SELECTIONTYPE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_SELECTIONTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b79cb36759c857cea280b1c4beb5a476fa27a794f1f9985e1d259c345a9dc4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437838"
---
# <a name="em_selectiontype-message"></a>EM \_ SELECTIONTYPE 訊息

判斷 rich edit 控制項的選取專案類型。

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

如果選取範圍是空的，則傳回值會是 \_ 空的。

如果選取範圍不是空的，則傳回值是一組包含下列一或多個值的旗標。



| 傳回碼                                                                                     | 描述                                 |
|-------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**選取 \_ 文字**</dt> </dl>        | Text。<br/>                            |
| <dl> <dt>**SEL \_ 物件**</dt> </dl>      | 至少一個 COM 物件。<br/>         |
| <dl> <dt>**SEL \_ MULTICHAR**</dt> </dl>   | 一個以上的文字字元。<br/> |
| <dl> <dt>**SEL \_ MULTIOBJECT**</dt> </dl> | 一個以上的 COM 物件。<br/>        |



 

## <a name="remarks"></a>備註

此訊息在無底邊 rich edit 控制項父系的 [**WM \_ 大小**](/windows/desktop/winmsg/wm-size) 處理期間很有用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WM \_ 大小**](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

