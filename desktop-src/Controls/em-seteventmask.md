---
title: 'EM_SETEVENTMASK 訊息 (Richedit .h) '
description: 設定 rich edit 控制項的事件遮罩。 事件遮罩會指定控制項傳送至其父視窗的通知碼。
ms.assetid: 139f6e44-fc54-40f2-a3f6-2b7efc819cae
keywords:
- EM_SETEVENTMASK message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd4d79d23f7b56a29bc4f5142ed03b23e8081687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466541"
---
# <a name="em_seteventmask-message"></a>EM \_ SETEVENTMASK 訊息

設定 rich edit 控制項的事件遮罩。 事件遮罩會指定控制項傳送至其父視窗的通知碼。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

Rich edit 控制項的新事件遮罩。 如需事件遮罩的清單，請參閱 [**Rich Edit 控制項事件遮罩旗標**](rich-edit-control-event-mask-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息會傳回先前的事件遮罩。

## <a name="remarks"></a>備註

預設事件遮罩 (在設定 [任何] 之前) ENM [ \_ 無]。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ GETEVENTMASK**](em-geteventmask.md)
</dt> <dt>

[**Rich Edit 控制項事件遮罩旗標**](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





