---
title: 'DTN_DROPDOWN (Commctrl 的通知碼) '
description: 當使用者啟動下拉式月曆時，日期和時間選擇器會傳送 (DTP) 控制。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 6f20fa87-2223-4876-b77d-2c684685bf10
keywords:
- DTN_DROPDOWN 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- DTN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 101a25a8e2da09b9f4065a54fcff9896690adbb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843936"
---
# <a name="dtn_dropdown-notification-code"></a>DTN \_ 下拉式通知碼

當使用者啟動下拉式月曆時，日期和時間選擇器會傳送 (DTP) 控制。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
DTN_DROPDOWN

    lpNmhdr = (LPNMHDR)lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含通知的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此通知的傳回值。

## <a name="remarks"></a>備註

您的通知處理常式可能需要執行的一項工作，是自訂下拉式月曆控制項。 比方說，如果您不想要「移到今天」，則必須設定控制項的 [**MCS \_ NOTODAY**](month-calendar-control-styles.md)  樣式。 若要取出月曆控制項的控制碼，請將該 DTP [**\_ GETMONTHCAL**](dtm-getmonthcal.md) 訊息傳送給 DTP。 然後，您可以使用此控制碼和 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 來設定所需的月曆樣式。

DTP 控制項不會維護靜態的子月份行事曆控制項。 在傳送此通知碼之前，將會建立新的月曆控制項。 此外，當 (可見) 時，DTP 控制項會終結子控制項。 因此，您的應用程式不能依賴控制項之子月份行事曆的靜態視窗控制碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[DTN \_ 特寫](dtn-closeup.md)
</dt> <dt>

[**DTM \_ GETMONTHCAL**](dtm-getmonthcal.md)
</dt> </dl>

 

