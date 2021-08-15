---
title: 'UDM_GETRANGE 訊息 (Commctrl .h) '
description: 抓取上下按鈕 (範圍) 的最小和最大位置。
ms.assetid: fd42538a-8d96-4a9c-a1db-07c3e9afef84
keywords:
- UDM_GETRANGE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- UDM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d13811f383886e0e4985eb3f2f5093eec53cb0745349a36ca133fa3de9656773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408098"
---
# <a name="udm_getrange-message"></a>UDM \_ GETRANGE 訊息

抓取上下按鈕 (範圍) 的最小和最大位置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是包含最小和最大位置的32位值。 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是控制項的最大位置，而 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))是最小位置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

