---
title: 'TCM_SETCURFOCUS 訊息 (Commctrl .h) '
description: 將焦點設定至索引標籤控制項中的指定索引標籤。 您可以使用 TabCtrl SetCurFocus 宏明確地傳送此訊息 \_ 。
ms.assetid: bcbd5f26-b54e-492b-aff3-357b8ae23969
keywords:
- TCM_SETCURFOCUS message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_SETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe566d1e1b3cc7d257c4756fe123423fc344a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934405"
---
# <a name="tcm_setcurfocus-message"></a>TCM \_ SETCURFOCUS 訊息

將焦點設定至索引標籤控制項中的指定索引標籤。 您可以使用 [**TabCtrl \_ SetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcurfocus) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

取得焦點之索引標籤的索引。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

如果索引標籤控制項具有 [ [**TCS \_**](tab-control-styles.md) ] 按鈕樣式 (按鈕模式) ，則具有焦點的索引標籤可能會與選取的索引標籤不同。例如，選取索引標籤時，使用者可以按方向鍵將焦點設定至不同的索引標籤，而不變更選取的索引標籤。在 [按鈕] 模式中， **TCM \_ SETCURFOCUS** 會將輸入焦點設定為與指定索引標籤相關聯的按鈕，但不會變更選取的索引標籤。

如果索引標籤控制項沒有 [TCS] [**\_ 按鈕**](tab-control-styles.md) 樣式，則變更焦點也會變更選取的索引標籤。在此情況下，索引標籤控制項會將 [TCN \_ SELCHANGING](tcn-selchanging.md) 和 [TCN \_ SELCHANGE](tcn-selchange.md) 通知碼傳送至其父視窗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TCM \_ GETCURFOCUS**](tcm-getcurfocus.md)
</dt> </dl>

 

 





