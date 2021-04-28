---
title: 'EM_SETLIMITTEXT 訊息 (Winuser .h) '
description: EM_SETLIMITTEXT 訊息：設定編輯控制項的文字限制。
ms.assetid: e2be7814-435b-495f-982a-32247fbc0165
keywords:
- EM_SETLIMITTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b66d4e03b5c1824ab501226482fcf51fb9121cba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109746"
---
# <a name="em_setlimittext-message"></a>EM \_ SETLIMITTEXT 訊息

設定編輯控制項的文字限制。 文字限制是使用者可以在編輯控制項中輸入的最大文字數量（以 **TCHAR** s 為限）。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

若為編輯控制項和 Microsoft Rich Edit 1.0，則會使用 bytes。 針對 Microsoft Rich Edit 2.0 和更新版本，會使用字元。

**Em \_ SETLIMITTEXT** 訊息等同于 [**em \_ LIMITTEXT**](em-limittext.md)訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

使用者可以輸入的最大 **TCHAR** 數。 若為 ANSI 文字，此為位元組數;若為 Unicode 文字，此為字元數。 此數目不包含終止的 null 字元。

**Rich edit 控制項：** 如果此參數為零，則文字長度會設定為64000個字元。

如果此參數為零，則文字長度會設為單行編輯控制項的0x7FFFFFFE 字元，或1表示多行編輯控制項。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

**EM \_ SETLIMITTEXT** 訊息只會限制使用者可以輸入的文字。 當傳送訊息時，它不會影響任何已在編輯控制項中的文字，也不會影響由 [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) 訊息複製到編輯控制項的文字長度。 如果應用程式使用 **WM \_ SETTEXT** 訊息將更多文字放入編輯控制項中，而不是在 **EM \_ SETLIMITTEXT** 訊息中指定，則使用者可以編輯編輯控制項的整個內容。

在呼叫 **EM \_ SETLIMITTEXT** 之前，使用者可以在編輯控制項中輸入的文字數量預設限制為32767個字元。

針對單行編輯控制項，文字限制為0x7FFFFFFE 個位元組或 *wParam* 參數的值，以較小者為准。 若為多行編輯控制項，此值為1個位元組或 *wParam* 參數的值，以較小者為准。

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 使用 message [**EM \_ EXLIMITTEXT**](em-exlimittext.md) 來取得大於64000的文字長度值。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ GETLIMITTEXT**](em-getlimittext.md)
</dt> </dl>

 

