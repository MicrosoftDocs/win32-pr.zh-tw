---
title: 'RB_GETRECT 訊息 (Commctrl .h) '
description: 抓取 Rebar 控制項中指定範圍的周框。
ms.assetid: e272b090-1e4d-4cff-87f0-557ad8116e7e
keywords:
- RB_GETRECT message Windows 控制項
topic_type:
- apiref
api_name:
- RB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b9d5de00b638a3767df461595ff01316b23183
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187290"
---
# <a name="rb_getrect-message"></a>RB \_ GETRECT 訊息

抓取 Rebar 控制項中指定範圍的周框。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

Rebar 控制項中的寬線索引（以零為基底）。

</dd> <dt>

*lParam* 
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，此結構會接收 Rebar 區的範圍。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

