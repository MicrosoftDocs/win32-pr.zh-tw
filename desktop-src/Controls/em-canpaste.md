---
title: 'EM_CANPASTE 訊息 (Richedit .h) '
description: 判斷 rich edit 控制項是否可以貼上指定的剪貼簿格式。
ms.assetid: 1b858ad8-1312-407b-b12a-c63668ba9f72
keywords:
- EM_CANPASTE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_CANPASTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad400b610a033b6f67177da99876a892d294ec8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025257"
---
# <a name="em_canpaste-message"></a>EM \_ CANPASTE 訊息

判斷 rich edit 控制項是否可以貼上指定的剪貼簿格式。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定要嘗試的 [剪貼簿格式](/windows/desktop/dataxchg/clipboard-formats) 。 若要嘗試目前剪貼簿上的任何格式，請將此參數設定為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果可以貼上剪貼簿格式，則傳回值為非零值。

如果無法貼上剪貼簿格式，則傳回值為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

