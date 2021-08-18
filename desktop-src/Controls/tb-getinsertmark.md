---
title: 'TB_GETINSERTMARK 訊息 (Commctrl .h) '
description: 抓取工具列目前的插入標記。
ms.assetid: b22770a4-e859-451d-a726-279bbc49b984
keywords:
- TB_GETINSERTMARK 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ee4a51d3110a99013ed26ccb1f2c102e7821873e63dd419b33e92636a1b655
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918748"
---
# <a name="tb_getinsertmark-message"></a>TB \_ GETINSERTMARK 訊息

抓取工具列目前的插入標記。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark)結構的指標，此結構會接收插入標記。

</dd> </dl>

## <a name="return-value"></a>傳回值

一律傳回 **TRUE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TB \_ SETINSERTMARK**](tb-setinsertmark.md)
</dt> </dl>

 

 





