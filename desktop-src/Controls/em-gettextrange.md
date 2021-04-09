---
title: 'EM_GETTEXTRANGE 訊息 (Richedit .h) '
description: 從 rich edit 控制項抓取指定的字元範圍。
ms.assetid: 18398963-eb2c-4f64-99f5-9614a5d34b52
keywords:
- EM_GETTEXTRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETTEXTRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d68c4089bbe2cc09daa39d69e9094a4abaead787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934809"
---
# <a name="em_gettextrange-message"></a>EM \_ GETTEXTRANGE 訊息

從 rich edit 控制項抓取指定的字元範圍。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea)結構的指標，指定要取出的字元範圍，以及要將字元複製到其中的緩衝區。

</dd> </dl>

## <a name="return-value"></a>傳回值

訊息會傳回復制的字元數，而不包含終止的 null 字元。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea)
</dt> </dl>

 

 





