---
title: 'TB_ISBUTTONHIDDEN 訊息 (Commctrl .h) '
description: 決定是否隱藏工具列中指定的按鈕。
ms.assetid: 3372a64f-8209-4e3f-a6a9-8fe2e7e87ff2
keywords:
- TB_ISBUTTONHIDDEN 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_ISBUTTONHIDDEN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1fac4fa28daa876b273d71e4cf80bf5e76fce8fe01c0a5517dc63fb31b4273e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078232"
---
# <a name="tb_isbuttonhidden-message"></a>TB \_ ISBUTTONHIDDEN 訊息

決定是否隱藏工具列中指定的按鈕。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

按鈕的命令識別碼。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果按鈕是隱藏的，則會傳回非零，否則會傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





