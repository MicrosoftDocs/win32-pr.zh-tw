---
title: 'LVM_ENSUREVISIBLE 訊息 (Commctrl .h) '
description: 確定清單視圖專案是完全或部分可見的，視需要滾動清單視圖控制項。 您可以明確地傳送此訊息，或使用 ListView \_ EnsureVisible 宏來傳送。
ms.assetid: 3564b6e6-b8b6-401b-85bc-8bd6261fc054
keywords:
- LVM_ENSUREVISIBLE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baeefaf90f0a4562fb187024b2c6f8676c68fb9d46377a4ced900bda6cfd3dfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920298"
---
# <a name="lvm_ensurevisible-message"></a>LVM \_ ENSUREVISIBLE 訊息

確定清單視圖專案是完全或部分可見的，視需要滾動清單視圖控制項。 您可以明確地傳送此訊息，或使用 [**ListView \_ EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_ensurevisible) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

清單視圖專案的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

值，指定是否必須完全看見專案。 如果此參數為 **TRUE**，則如果專案至少為部分可見，就不會發生任何滾動。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

如果視窗樣式包含 [**lvs) \_ NOSCROLL**](list-view-window-styles.md)，則訊息會失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





