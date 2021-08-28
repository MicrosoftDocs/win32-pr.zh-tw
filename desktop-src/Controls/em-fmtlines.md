---
title: 'EM_FMTLINES 訊息 (Winuser .h) '
description: 設定旗標，判斷多行編輯控制項是否包含軟換行字元。 軟換行是由兩個換行字元和換行字元所組成，且會插入到因為 wordwrapping 而中斷的行尾。
ms.assetid: bfc08062-b0a7-4ba7-8858-00cb20895c77
keywords:
- EM_FMTLINES 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_FMTLINES
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e0c0c410f13a33f0e387098178b42faaf3269c36d11f75e765eb753fa9d0844
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119545098"
---
# <a name="em_fmtlines-message"></a>EM \_ FMTLINES 訊息

設定旗標，判斷多行編輯控制項是否包含軟換行字元。 軟換行是由兩個換行字元和換行字元所組成，且會插入到因為 wordwrapping 而中斷的行尾。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定是否要插入軟換行字元。 **TRUE** 值會插入字元;**FALSE** 值會移除它們。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值與 *wParam* 參數相同。

## <a name="remarks"></a>備註

此訊息只會影響 [**EM \_ GETHANDLE**](em-gethandle.md) 訊息所傳回的緩衝區，以及由 [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext) 訊息傳回的文字。 它不會影響編輯控制項內的文字顯示方式。

**EM \_ FMTLINES** 訊息不會影響以硬換行結尾的行。 硬換行是由一個換行字元和一個換行字元所組成。

> [!Note]  
> 處理此訊息時，文字會變更的大小。

 

**Rich Edit：** 不支援 **EM \_ FMTLINES** 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ GETHANDLE**](em-gethandle.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

