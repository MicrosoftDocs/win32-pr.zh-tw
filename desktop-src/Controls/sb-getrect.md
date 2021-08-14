---
title: 'SB_GETRECT 訊息 (Commctrl .h) '
description: 抓取狀態視窗中某部分的周框。
ms.assetid: 76b8d470-07ae-440b-9bf5-7875b80b0168
keywords:
- SB_GETRECT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- SB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85d874a5bf115918432bd6f0310a14ed026e0dc2df22da029bfca0be25649821
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168730"
---
# <a name="sb_getrect-message"></a>SB \_ GETRECT 訊息

抓取狀態視窗中某部分的周框。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為基底的索引，這是要抓取其周框矩形的部分。

</dd> <dt>

*lParam* 
</dt> <dd>

接收周框 [**的矩形結構指標**](/previous-versions//dd162897(v=vs.85)) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

