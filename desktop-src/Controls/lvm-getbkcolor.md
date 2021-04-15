---
title: 'LVM_GETBKCOLOR 訊息 (Commctrl .h) '
description: 取得清單視圖控制項的背景色彩。 您可以明確地傳送此訊息，或使用 ListView \_ GetBkColor 宏來傳送。
ms.assetid: 077d3b2e-f6d1-4acc-b002-e9e707ad274c
keywords:
- LVM_GETBKCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4329adda75677d1cc0126eaa0196fadf143cd0b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464285"
---
# <a name="lvm_getbkcolor-message"></a>LVM \_ GETBKCOLOR 訊息

取得清單視圖控制項的背景色彩。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkcolor) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回清單視圖控制項的背景色彩。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





