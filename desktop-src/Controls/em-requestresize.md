---
title: 'EM_REQUESTRESIZE 訊息 (Richedit .h) '
description: 強制 rich edit 控制項將 EN \_ REQUESTRESIZE 通知程式碼傳送至其父視窗。
ms.assetid: efc22771-9b9f-4a30-a906-f02095607c21
keywords:
- EM_REQUESTRESIZE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec41e7be8e0f30d5c1ec011247f3964292c2218e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187312"
---
# <a name="em_requestresize-message"></a>EM \_ REQUESTRESIZE 訊息

強制 rich edit 控制項將 [**EN \_ REQUESTRESIZE**](en-requestresize.md) 通知程式碼傳送至其父視窗。

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

此訊息不會傳回值。

## <a name="remarks"></a>備註

此訊息在無底邊 rich edit 控制項父系的 [**WM \_ 大小**](/windows/desktop/winmsg/wm-size) 處理期間很有用。

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

[**EN \_ REQUESTRESIZE**](en-requestresize.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**WM \_ 大小**](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

