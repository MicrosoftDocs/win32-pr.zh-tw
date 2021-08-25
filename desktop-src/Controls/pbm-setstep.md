---
title: 'PBM_SETSTEP 訊息 (Commctrl .h) '
description: 指定進度列的步驟增量。 步驟遞增是進度列在收到 PBM STEPIT 訊息時，增加其目前位置的數量 \_ 。 依預設，步驟遞增會設定為10。
ms.assetid: 75c1085b-6c7a-4c44-9a12-f9bf21f7d945
keywords:
- PBM_SETSTEP 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- PBM_SETSTEP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88508654565cb3af05dd768ef7ef1e54e5ef0ee80e0797bc45631f6e3fe6912
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798768"
---
# <a name="pbm_setstep-message"></a>PBM \_ SETSTEP 訊息

指定進度列的步驟增量。 步驟遞增是進度列在收到 [**PBM \_ STEPIT**](pbm-stepit.md) 訊息時，增加其目前位置的數量。 依預設，步驟遞增會設定為10。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

新步驟增量。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回上一個步驟增量。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





