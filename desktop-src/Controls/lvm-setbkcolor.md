---
title: 'LVM_SETBKCOLOR 訊息 (Commctrl .h) '
description: 設定清單視圖控制項的背景色彩。 您可以明確地傳送此訊息，或使用 ListView \_ SetBkColor 宏來傳送。
ms.assetid: d579249d-421d-4e7e-8992-4c7fd7277593
keywords:
- LVM_SETBKCOLOR message Windows 控制項
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
ms.openlocfilehash: 80977ed6c95a1353889265e52cfc05c26aaa2a5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934628"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





