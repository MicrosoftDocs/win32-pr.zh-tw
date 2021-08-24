---
title: 'PBM_GETBKCOLOR 訊息 (Commctrl .h) '
description: 取得進度列的背景色彩。
ms.assetid: 9526ed78-08d9-468f-831b-72bb7c8c92d1
keywords:
- PBM_GETBKCOLOR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- PBM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1462d864df0440cd0567e6d6b1d04261818bb98ab4a6b5a803272e63abcb8d5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919518"
---
# <a name="pbm_getbkcolor-message"></a>PBM \_ GETBKCOLOR 訊息

取得進度列的背景色彩。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回進度列的背景色彩。

## <a name="remarks"></a>備註

這是 [**PBM \_ SETBKCOLOR**](pbm-setbkcolor.md) 訊息所設定的色彩。 預設值是 CLR \_ default，定義于 commctrl 中。

此函式只會影響傳統模式，而不會影響任何視覺效果樣式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





