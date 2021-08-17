---
title: 'RB_SETPALETTE 訊息 (Commctrl .h) '
description: 設定 Rebar 控制項的目前調色板。
ms.assetid: 85f0726a-21fd-41b3-aa52-6a0a0c1947fa
keywords:
- RB_SETPALETTE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- RB_SETPALETTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85cd2968fa5fa74915e37f40f30dd47751e2316e8d91d0f51f9d3c7145b893fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434938"
---
# <a name="rb_setpalette-message"></a>RB \_ SETPALETTE 訊息

設定 Rebar 控制項的目前調色板。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

**HPALETTE** ，指定 Rebar 控制項將使用的新調色板。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HPALETTE** ，指定 Rebar 控制項先前的調色板。

## <a name="remarks"></a>備註

傳送此訊息的應用程式必須負責刪除此訊息中傳遞的 **HPALETTE** (請參閱 [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)) 。 Rebar 控制項不會刪除包含此訊息的 **HPALETTE** 集。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RB \_ GETPALETTE**](rb-getpalette.md)
</dt> </dl>

 

