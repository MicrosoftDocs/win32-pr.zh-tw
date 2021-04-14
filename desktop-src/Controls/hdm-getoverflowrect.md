---
title: 'HDM_GETOVERFLOWRECT 訊息 (Commctrl .h) '
description: 當在 \_ 標題控制項上設定 HDS 溢位樣式，且顯示溢位按鈕時，取得溢位按鈕的周框。 明確地傳送此訊息，或使用標頭 \_ GetOverflowRect 宏。
ms.assetid: 52fb3dc3-ce22-40da-8222-20fd75c005ae
keywords:
- HDM_GETOVERFLOWRECT message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_GETOVERFLOWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58f521bb6b188a10bb7af52ead46423e7ae0cf58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508803"
---
# <a name="hdm_getoverflowrect-message"></a>HDM \_ GETOVERFLOWRECT 訊息

當在標題控制項上設定 [**HDS \_ 溢**](header-control-styles.md) 位樣式，且顯示溢位按鈕時，取得溢位按鈕的周框。 明確地傳送此訊息，或使用 [**標頭 \_ GetOverflowRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用。 必須為零。

</dd> <dt>

*lParam* \[在\]
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，用來接收周框的資訊。 訊息寄件者負責配置此結構。 在 **矩形** 結構中傳回的座標會以螢幕座標表示。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **TRUE** ;否則 **為 FALSE**。

## <a name="remarks"></a>備註

標題控制項必須具有 **HDF \_ SPLITBUTTON** 樣式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[關於標題控制項](header-controls.md)
</dt> </dl>

 

