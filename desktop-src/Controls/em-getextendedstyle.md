---
title: 'EM_GETEXTENDEDSTYLE 訊息 (Commctrl .h) '
description: 抓取編輯控制項的延伸樣式。 明確地傳送此訊息，或使用 Edit \_ GetExtendedStyle 宏。
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- EM_GETEXTENDEDSTYLE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 37dc117bccd57b51098a7ca8c19e8b178037bef8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466112"
---
# <a name="em_getextendedstyle-message-commctrlh"></a>EM_GETEXTENDEDSTYLE 訊息 (Commctrl .h) 

抓取樹狀檢視控制項的延伸樣式。 明確地傳送此訊息，或使用 [**Edit \_ GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getextendedstyle) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回擴充樣式的值。如需樣式的詳細資訊，請參閱 [編輯控制項延伸樣式](edit-control-window-extended-styles.md)。

## <a name="remarks"></a>備註

編輯控制項的擴充樣式與函數 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 或函數 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)所使用的擴充樣式沒有任何作用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 版本1809桌面應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2019 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

