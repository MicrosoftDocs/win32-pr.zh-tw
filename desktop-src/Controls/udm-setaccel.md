---
title: 'UDM_SETACCEL 訊息 (Commctrl .h) '
description: 設定上下按鈕控制項的加速。
ms.assetid: af1d0a34-13ba-4bda-82f5-d7afab6bb1ed
keywords:
- UDM_SETACCEL 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- UDM_SETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc746e33c14de0dd177ecc31fc237be7cb8be36280bb2a5ceadff31d2b286ec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957737"
---
# <a name="udm_setaccel-message"></a>UDM \_ SETACCEL 訊息

設定上下按鈕控制項的加速。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

*AAccels* 所指定的 [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel)結構數目。

</dd> <dt>

*lParam* 
</dt> <dd>

[**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel)結構陣列的指標，其中包含加速資訊。 元素應以每個 **nSec** 成員的遞增順序排序。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**UDM \_ GETACCEL**](udm-getaccel.md)
</dt> </dl>

 

 





