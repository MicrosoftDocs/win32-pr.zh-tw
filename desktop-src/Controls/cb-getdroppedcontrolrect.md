---
title: 'CB_GETDROPPEDCONTROLRECT 訊息 (Winuser .h) '
description: 應用程式會傳送 CB \_ GETDROPPEDCONTROLRECT 訊息，以取得下拉式方塊中下拉式方塊的螢幕座標。
ms.assetid: fd8d78c0-e1a8-49c8-9e35-a105d00b863c
keywords:
- CB_GETDROPPEDCONTROLRECT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETDROPPEDCONTROLRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c140abb139cc47020f333ccf66f71cf36d890449be91d66f51b646db22091c39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089278"
---
# <a name="cb_getdroppedcontrolrect-message"></a>CB \_ GETDROPPEDCONTROLRECT 訊息

應用程式會傳送 **CB \_ GETDROPPEDCONTROLRECT** 訊息，以取得下拉式方塊中下拉式方塊的螢幕座標。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，此結構會在其中斷狀態中接收下拉式方塊的座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息成功，則傳回值為非零。

如果訊息失敗，則傳回值為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**矩形**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

