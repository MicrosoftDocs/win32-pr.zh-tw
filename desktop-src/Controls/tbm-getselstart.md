---
title: 'TBM_GETSELSTART 訊息 (Commctrl .h) '
description: 抓取目前選取範圍在 [選取範圍] 中的開始位置。
ms.assetid: 0000df2a-c40d-40c2-b120-e5d4fe6c5016
keywords:
- TBM_GETSELSTART 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETSELSTART
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a654bfcf8756bee5b39ec9fc97b82ffe84e8e48ba39f4ca2f9fab732d0d1962e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046418"
---
# <a name="tbm_getselstart-message"></a>TBM \_ GETSELSTART 訊息

抓取目前選取範圍在 [選取範圍] 中的開始位置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回32位值，指定目前選取範圍的開始位置。

## <a name="remarks"></a>備註

只有當您在建立時，如果您已指定 [ [**tb] \_ ENABLESELRANGE**](trackbar-control-styles.md) 樣式，則會有一個選取範圍。

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

[**TBM \_ GETSELEND**](tbm-getselend.md)
</dt> <dt>

[**TBM \_ SETSEL**](tbm-setsel.md)
</dt> <dt>

[**TBM \_ SETSELEND**](tbm-setselend.md)
</dt> <dt>

[**TBM \_ SETSELSTART**](tbm-setselstart.md)
</dt> </dl>

 

 





