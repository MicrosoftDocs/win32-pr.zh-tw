---
title: 'RB_SETBARINFO 訊息 (Commctrl .h) '
description: 設定 Rebar 控制項的特性。
ms.assetid: e4413d46-574f-4ccd-b5fd-3ba6c1e3924b
keywords:
- RB_SETBARINFO 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- RB_SETBARINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4297d73a8bca6abac1a4b99abc4a91147ad237548a67e325a9efb2f1a1f1c46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696608"
---
# <a name="rb_setbarinfo-message"></a>RB \_ SETBARINFO 訊息

設定 Rebar 控制項的特性。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo)結構的指標，其中包含要設定的資訊。 在傳送此訊息之前，您必須將此結構的 **cbSize** 成員設定為 **sizeof** (REBARINFO) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





