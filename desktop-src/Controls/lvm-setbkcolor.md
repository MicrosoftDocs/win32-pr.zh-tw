---
title: 'LVM_SETBKCOLOR 訊息 (Commctrl .h) '
description: 設定清單視圖控制項的背景色彩。 您可以明確地傳送此訊息，或使用 ListView \_ SetBkColor 宏來傳送。
ms.assetid: d579249d-421d-4e7e-8992-4c7fd7277593
keywords:
- LVM_SETBKCOLOR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b8acfb07a91fae470d893facf6af051397fac2f0d9f4f6990ab4ff67744d8ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119391608"
---
# <a name="lvm_setbkcolor-message"></a>LVM \_ SETBKCOLOR 訊息

設定清單視圖控制項的背景色彩。 您可以明確地傳送此訊息，或使用 [**ListView \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkcolor) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

要設定的背景色彩，或 \_ 無背景色彩的 CLR 無值。 具有背景色彩的清單視圖控制項，其重繪速度會比沒有背景色彩的控制項更快。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





