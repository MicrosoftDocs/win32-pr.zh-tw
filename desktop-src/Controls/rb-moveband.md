---
title: 'RB_MOVEBAND 訊息 (Commctrl .h) '
description: 將一個索引區從一個索引移至另一個索引。
ms.assetid: bb5b45de-957e-46fb-b59a-18b55b69c395
keywords:
- RB_MOVEBAND 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- RB_MOVEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ab45f63b46b8bb883ef9f1fd8708f915dba2a6860ef2f6fabb09e2b00bd8fe6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798538"
---
# <a name="rb_moveband-message"></a>RB \_ MOVEBAND 訊息

將一個索引區從一個索引移至另一個索引。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要移動之帶狀線的以零為基底的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

新的寬線位置之以零為基底的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="remarks"></a>備註

這則訊息很有可能會變更 Rebar 控制項中其他等區的索引。 如果將範圍從索引6移至索引0，則介於兩者之間的所有波段都會以1遞增其索引。

*lParam* 絕不能大於區段數減一。 您可以使用 [**RB \_ GETBANDCOUNT**](rb-getbandcount.md) 訊息來取得群組數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





