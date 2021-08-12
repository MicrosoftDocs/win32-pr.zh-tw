---
title: 'BM_SETSTYLE 訊息 (Winuser .h) '
description: 設定按鈕的樣式。 您可以明確地傳送此訊息，或使用按鈕 \_ >setstyle 宏。
ms.assetid: 6439e68f-87fc-4a4a-8025-facc3c0e03e2
keywords:
- BM_SETSTYLE 訊息 Windows 控制項
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
ms.openlocfilehash: 17f635a70bf806c6c26f5b236ea939bc453d27bf0fe135f8e2586aeb59021b9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674416"
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
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



 

