---
title: 'PGM_SETBUTTONSIZE 訊息 (Commctrl .h) '
description: 設定呼機控制項目前的按鈕大小。 您可以明確地傳送此訊息，或使用呼叫器 \_ SetButtonSize 宏。
ms.assetid: b31960f8-87c2-4209-8213-df75ac883e11
keywords:
- PGM_SETBUTTONSIZE message Windows 控制項
topic_type:
- apiref
api_name:
- PGM_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecf8c164ed960675c1a68be36acfe0eff40f972f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508487"
---
# <a name="pgm_setbuttonsize-message"></a>PGM \_ SETBUTTONSIZE 訊息

設定呼機控制項目前的按鈕大小。 您可以明確地傳送此訊息，或使用 [**呼叫器 \_ SetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

**Int** 類型的值，其中包含新的按鈕大小（以圖元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回包含上一個按鈕大小的 **int** 值（以圖元為單位）。

## <a name="remarks"></a>備註

如果呼機控制項有 [**pg \_ HORZ**](pager-control-styles.md) 樣式，則按鈕大小會決定頁面導覽按鈕的寬度。 如果呼機控制項具有 [**pg \_ 垂直**](pager-control-styles.md) 樣式，則按鈕大小會決定頁面導覽按鈕的高度。 根據預設，呼機控制項會將其按鈕大小設定為捲軸寬度的三 fourths。

頁面的最小大小為目前的12圖元。 不過，這可能會變更，因此您不應該依賴此值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PGM \_ GETBUTTONSIZE**](pgm-getbuttonsize.md)
</dt> </dl>

 

 





