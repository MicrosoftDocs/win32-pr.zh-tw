---
title: 'RB_GETTOOLTIPS 訊息 (Commctrl .h) '
description: 抓取與 Rebar 控制項相關聯之任何工具提示控制項的控制碼。
ms.assetid: 87897b00-857f-4a8a-ae16-a48abf4c411d
keywords:
- RB_GETTOOLTIPS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- RB_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 859934dcdec85d0b160f9076f2a77263a02a187ebf49f8ccbb4af20fc3e82d13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540058"
---
# <a name="rb_gettooltips-message"></a>RB \_ GETTOOLTIPS 訊息

抓取與 Rebar 控制項相關聯之任何工具提示控制項的控制碼。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HWND** 值，此值是與 Rebar 控制項相關聯之工具提示控制項的控制碼; 如果沒有工具提示控制項與 Rebar 控制項相關聯，則為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





