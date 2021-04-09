---
title: 'RB_HITTEST 訊息 (Commctrl .h) '
description: 判斷如果在該點上存在 Rebar 帶，則在螢幕上的某個點上，Rebar 區的哪個部分是在指定的點上。
ms.assetid: 8f27db21-50d8-438f-a44c-2e65dd93fa2a
keywords:
- RB_HITTEST message Windows 控制項
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
ms.openlocfilehash: e17283bfce255672391ba9d8b6acd60fe41045b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024653"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





