---
title: 'TB_MARKBUTTON 訊息 (Commctrl .h) '
description: 在工具列控制項中設定指定按鈕的醒目提示狀態。
ms.assetid: cba0e2d2-40a7-4e20-a1ef-d5f5444c96d9
keywords:
- TB_MARKBUTTON 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_MARKBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1af7ba20ed9ce3d1b289c0c28db8fc40c476dd99f4ffb1af1af28692c44cab1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168022"
---
# <a name="tb_markbutton-message"></a>TB \_ MARKBUTTON 訊息

在工具列控制項中設定指定按鈕的醒目提示狀態。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

工具列按鈕的命令識別碼。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是 **布林** 值，表示新的醒目提示狀態。 若 **為 TRUE**，則會反白顯示按鈕。 如果 **為 FALSE**，則按鈕會設定為其預設狀態。

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

