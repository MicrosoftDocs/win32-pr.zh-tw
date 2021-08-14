---
title: 'CBEN_ENDEDIT (Commctrl 的通知碼) '
description: 當使用者在編輯方塊內結束作業，或已從控制項下拉式清單中選取專案時傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: b6b50951-7304-4499-b57b-a5b592de2190
keywords:
- CBEN_ENDEDIT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- CBEN_ENDEDIT
- CBEN_ENDEDITA
- CBEN_ENDEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22ae9205e84e4f1c0b10e516b1f406f2d167f1bc5cc38417a31379d20e16fcac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413948"
---
# <a name="cben_endedit-notification-code"></a>CBEN \_ ENDEDIT 通知碼

當使用者在編輯方塊內結束作業，或已從控制項下拉式清單中選取專案時傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
CBEN_ENDEDIT

    pnmEditInfo = (PNMCBEENDEDIT) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita)結構的指標，其中包含使用者如何結束編輯作業的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

**FALSE** 表示接受通知碼，並允許控制項顯示選取的專案;否則 **為 TRUE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **CBEN \_ENDEDITW** (Unicode) 和 **CBEN \_ ENDEDITA** (ANSI) <br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[關於 ComboBoxEx 控制項](comboboxex-controls.md)
</dt> </dl>

 

 





