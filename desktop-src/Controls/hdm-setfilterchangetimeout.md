---
title: 'HDM_SETFILTERCHANGETIMEOUT 訊息 (Commctrl .h) '
description: 設定篩選屬性中發生變更和張貼 HDN FILTERCHANGE 通知之間的逾時間隔 \_ 。 您可以明確地傳送此訊息，或使用標頭 \_ SetFilterChangeTimeout 宏。
ms.assetid: 9bc8e0e7-d7c1-4dd6-9d39-6ae937f19d60
keywords:
- HDM_SETFILTERCHANGETIMEOUT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- HDM_SETFILTERCHANGETIMEOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b5f8df12a7f30baa5f8b7d4bf15698b30cfbb6619fb71a81d4977b259c318b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435858"
---
# <a name="hdm_setfilterchangetimeout-message"></a>HDM \_ SETFILTERCHANGETIMEOUT 訊息

設定篩選屬性中發生變更和張貼 [HDN \_ FILTERCHANGE](hdn-filterchange.md) 通知之間的逾時間隔。 您可以明確地傳送此訊息，或使用 [**標頭 \_ SetFilterChangeTimeout**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

逾時值 (以毫秒為單位)。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回要修改之篩選控制項的索引。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[HDN \_ FILTERCHANGE](hdn-filterchange.md)
</dt> </dl>

 

 





