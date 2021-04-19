---
title: 'PGM_FORWARDMOUSE 訊息 (Commctrl .h) '
description: 啟用或停用呼機控制項的滑鼠轉送。 啟用滑鼠轉寄時，分頁控制項會將 WM \_ MOUSEMOVE 訊息轉送至包含的視窗。 您可以明確地傳送此訊息，或使用呼叫器 \_ ForwardMouse 宏。
ms.assetid: 269972fe-50b3-4c9f-b5ac-65e768b30684
keywords:
- PGM_FORWARDMOUSE message Windows 控制項
topic_type:
- apiref
api_name:
- PGM_FORWARDMOUSE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: addc1c6bf762f540e9d7d785a5af2ba3fb7da93c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967746"
---
# <a name="pgm_forwardmouse-message"></a>PGM \_ FORWARDMOUSE 訊息

啟用或停用呼機控制項的滑鼠轉送。 啟用滑鼠轉寄時，分頁控制項會將 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 訊息轉送至包含的視窗。 您可以明確地傳送此訊息，或使用 [**呼叫器 \_ ForwardMouse**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

**布林** 值，決定是否啟用或停用滑鼠轉送。 如果此值為非零值，則會啟用滑鼠轉送。 如果此值為零，則會停用滑鼠轉送。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

未使用傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

