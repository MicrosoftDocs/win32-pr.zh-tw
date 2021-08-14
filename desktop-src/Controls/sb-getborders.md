---
title: 'SB_GETBORDERS 訊息 (Commctrl .h) '
description: 抓取狀態視窗水準和垂直框線的目前寬度。
ms.assetid: 120c1e0d-6f42-424e-94e0-a080d216d39d
keywords:
- SB_GETBORDERS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- SB_GETBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dafa7a8c27b5c274a981e43edc5c55ec0cade67cac08a1d09a898916d792795c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169051"
---
# <a name="sb_getborders-message"></a>SB \_ GETBORDERS 訊息

抓取狀態視窗水準和垂直框線的目前寬度。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

具有三個元素之整數陣列的指標。 第一個元素會接收水準框線的寬度，第二個會接收垂直框線的寬度，而第三個專案會接收矩形之間的框線寬度。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

框線會決定視窗外緣和包含文字之視窗內的矩形之間的間距。 框線也會決定矩形之間的間距。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





