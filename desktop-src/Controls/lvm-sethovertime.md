---
title: 'LVM_SETHOVERTIME 訊息 (Commctrl .h) '
description: 設定在選取專案之前，滑鼠游標必須停留在專案上的時間量。 您可以明確地傳送此訊息，或使用 ListView \_ SetHoverTime 宏。
ms.assetid: 454fbc38-f7fd-4dea-b223-56003b88528f
keywords:
- LVM_SETHOVERTIME 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f93edf917dc50384f3a09f7eadf013561715735a995c63a695cb8f9ad91dbce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077228"
---
# <a name="lvm_sethovertime-message"></a>LVM \_ SETHOVERTIME 訊息

設定在選取專案之前，滑鼠游標必須停留在專案上的時間量。 您可以明確地傳送此訊息，或使用 [**ListView \_ SetHoverTime**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethovertime) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

在選取專案之前，滑鼠游標必須停留在某個專案上的新時間量（以毫秒為單位）。 如果這個值是 (**DWORD**) -1，則會將暫留時間設定為預設的停留時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回先前的停留時間。

## <a name="remarks"></a>備註

暫止的時間只會影響具有 [**lvs) \_ EX \_ TRACKSELECT**](extended-list-view-styles.md)、 [**lvs) \_ ex \_ ONECLICKACTI加值稅E**](extended-list-view-styles.md)或 [**lvs) \_ ex \_ TWOCLICKACTI加值稅E**](extended-list-view-styles.md) 擴充清單視圖樣式的清單視圖控制項。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





