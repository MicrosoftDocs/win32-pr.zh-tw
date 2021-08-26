---
title: 'UDM_GETRANGE32 訊息 (Commctrl .h) '
description: 抓取上下按鈕控制項的32位範圍。
ms.assetid: a94b50c9-cd2f-430d-875f-720e51f544f1
keywords:
- UDM_GETRANGE32 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- UDM_GETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72078327b7a580768321f14c1d512e097561ae3441667497a822dc8a8a28b4e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077098"
---
# <a name="udm_getrange32-message"></a>UDM \_ GETRANGE32 訊息

抓取上下按鈕控制項的32位範圍。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

帶正負號之整數的指標，該整數會接收最小的最小值控制項範圍。 這個參數可以是 **Null**。

</dd> <dt>

*lParam* 
</dt> <dd>

帶正負號之整數的指標，該整數會接收上下按鈕控制項範圍的上限。 這個參數可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此訊息的傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





