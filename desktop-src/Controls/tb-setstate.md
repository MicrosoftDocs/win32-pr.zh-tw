---
title: 'TB_SETSTATE 訊息 (Commctrl .h) '
description: 在工具列中設定指定之按鈕的狀態。
ms.assetid: 68633b58-8d21-4931-b01f-32a66bda37b1
keywords:
- TB_SETSTATE message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7aa46dc68d9af5559e580e697bf6893b15051cff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106589"
---
# <a name="tb_setstate-message"></a>TB \_ SETSTATE 訊息

在工具列中設定指定之按鈕的狀態。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

按鈕的命令識別碼。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是列在 [工具列按鈕狀態](toolbar-button-states.md)中的值組合。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

