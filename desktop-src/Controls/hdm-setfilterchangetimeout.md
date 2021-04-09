---
title: 'HDM_SETFILTERCHANGETIMEOUT 訊息 (Commctrl .h) '
description: 設定篩選屬性中發生變更和張貼 HDN FILTERCHANGE 通知之間的逾時間隔 \_ 。 您可以明確地傳送此訊息，或使用標頭 \_ SetFilterChangeTimeout 宏。
ms.assetid: 9bc8e0e7-d7c1-4dd6-9d39-6ae937f19d60
keywords:
- HDM_SETFILTERCHANGETIMEOUT message Windows 控制項
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
ms.openlocfilehash: 9876634d12cd15001c296151694cb755ed1b34e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025345"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[HDN \_ FILTERCHANGE](hdn-filterchange.md)
</dt> </dl>

 

 





