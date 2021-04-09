---
title: 'BM_SETSTYLE 訊息 (Winuser .h) '
description: 設定按鈕的樣式。 您可以明確地傳送此訊息，或使用按鈕 \_ >setstyle 宏。
ms.assetid: 6439e68f-87fc-4a4a-8025-facc3c0e03e2
keywords:
- BM_SETSTYLE message Windows 控制項
topic_type:
- apiref
api_name:
- BM_SETSTYLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c080e1098d70b17e1e68bbbcd2d5598db79ef8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934099"
---
# <a name="bm_setstyle-message"></a>BM \_ >setstyle 訊息

設定按鈕的樣式。 您可以明確地傳送此訊息，或使用 [**按鈕 \_ >setstyle**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

按鈕樣式。 這個參數可以是按鈕樣式的組合。 如需按鈕樣式的表格，請參閱 [按鈕樣式](button-styles.md)。

</dd> <dt>

*lParam* 
</dt> <dd>

*LParam* 的 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是一個 **布林** 值，指定是否要重繪按鈕。 **TRUE** 值會重繪按鈕;值為 **FALSE** 時，不會重繪按鈕。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息一律會傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



 

