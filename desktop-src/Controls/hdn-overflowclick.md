---
title: 'HDN_OVERFLOWCLICK (Commctrl 的通知碼) '
description: 按一下標頭的溢位按鈕時，由標題控制項傳送到其父系。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 770ae00a-b87f-4de2-b869-2a233f2c493e
keywords:
- HDN_OVERFLOWCLICK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_OVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911953fcbea785cb7024bc9d0670c8ed33239524
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843671"
---
# <a name="hdn_overflowclick-notification-code"></a>HDN \_ OVERFLOWCLICK 通知碼

按一下標頭的溢位按鈕時，由標題控制項傳送到其父系。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
HDN_OVERFLOWCLICK

    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* \[在\]
</dt> <dd>

描述通知碼的 [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) 結構指標。 呼叫進程負責配置此結構，包括包含的 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) 結構。 設定 **NMHDR** 結構的成員，包括必須設定為 HDN OVERFLOWCLICK 的程式 *代碼* 成員 \_ 。

將 [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的 **iItem** 成員設定為不可見的第一個標題專案的索引，因此應顯示在溢位上。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

通知接收者會轉換 **LPARAM** 來取出 [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) 結構。 **WPARAM** 包含傳送通知之控制項的識別碼。

只有當標題控制項上設定了 [**HDS \_ 溢**](header-control-styles.md) 位時，才會傳送此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





