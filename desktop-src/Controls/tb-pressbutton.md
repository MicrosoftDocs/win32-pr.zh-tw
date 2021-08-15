---
title: 'TB_PRESSBUTTON 訊息 (Commctrl .h) '
description: 在工具列中按下或放開指定的按鈕。
ms.assetid: 03f6c3c2-d679-4e3a-a07b-c7e46c97972a
keywords:
- TB_PRESSBUTTON 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_PRESSBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c72bd3e58b06510463fcfb872060d7fcbb529ce3e5a96376ae8cb25e142d9e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168008"
---
# <a name="tb_pressbutton-message"></a>TB \_ PRESSBUTTON 訊息

在工具列中按下或放開指定的按鈕。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要按或放開之按鈕的命令識別碼。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是 **布林** 值，指出是否要按下或放開指定的按鈕。 若 **為 TRUE**，則會按下按鈕。 如果 **為 FALSE**，則表示按鈕已釋放。

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

