---
title: 'RB_HITTEST 訊息 (Commctrl .h) '
description: 判斷如果在該點上存在 Rebar 帶，則在螢幕上的某個點上，Rebar 區的哪個部分是在指定的點上。
ms.assetid: 8f27db21-50d8-438f-a44c-2e65dd93fa2a
keywords:
- RB_HITTEST 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- RB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d45f2ca2c5c6cf8de61c14404ac3bb541a8c61741896cf1b2803db29332d75e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078671"
---
# <a name="rb_hittest-message"></a>RB \_ system.windows.media.visualtreehelper.hittest 訊息

判斷如果在該點上存在 Rebar 帶，則在螢幕上的某個點上，Rebar 區的哪個部分是在指定的點上。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**RBHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo)結構的指標。 傳送訊息之前，必須將此結構的 **pt** 成員初始化為在用戶端座標中進行點擊測試的時間點。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回在指定點以零為基底的範圍索引，如果沒有 Rebar 波段，則傳回-1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





