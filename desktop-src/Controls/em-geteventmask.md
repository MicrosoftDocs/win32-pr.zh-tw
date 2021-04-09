---
title: 'EM_GETEVENTMASK 訊息 (Richedit .h) '
description: 抓取 rich edit 控制項的事件遮罩。 事件遮罩會指定控制項傳送至其父視窗的通知碼。
ms.assetid: cdf99f2a-e747-4b0e-9235-2719477c3ce2
keywords:
- EM_GETEVENTMASK message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f4d231bbb9d5592ff2f90da6a5096783b38c292
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934737"
---
# <a name="em_geteventmask-message"></a>EM \_ GETEVENTMASK 訊息

抓取 rich edit 控制項的事件遮罩。 事件遮罩會指定控制項傳送至其父視窗的通知碼。

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

此訊息會傳回 rich edit 控制項的事件遮罩。

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

[**EM \_ SETEVENTMASK**](em-seteventmask.md)
</dt> <dt>

[**Rich Edit 控制項事件遮罩旗標**](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





