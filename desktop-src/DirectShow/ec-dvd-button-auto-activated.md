---
description: 表示 DVD 功能表按鈕已根據光碟上的指示自動啟用。發生這種情況時，當功能表超時且光碟已指定要自動啟用的按鈕時。
ms.assetid: ecd79c2a-1717-473d-b111-2b1db2ca4cc1
title: 'EC_DVD_BUTTON_AUTO_ACTI加值稅ED (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BUTTON_AUTO_ACTIVATED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: cc018630d7a994c01b81adea4b4cf567666a76625b4b3b13fbf4118b8e8a1fd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965888"
---
# <a name="ec_dvd_button_auto_activated"></a>\_ \_ \_ 自動啟用 EC DVD \_ 按鈕

表示 DVD 功能表按鈕已根據光碟上的指示自動啟用。發生這種情況時，當功能表超時且光碟已指定要自動啟用的按鈕時。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**DWORD** 值，表示已啟用的按鈕。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

零個。

</dd> </dl>

此事件會在所有網域中引發。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dvdevcode (包含 Dshow) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DVD 應用程式](dvd-applications.md)
</dt> <dt>

[DVD 事件通知碼](dvd-notification-codes.md)
</dt> <dt>

[DirectShow 中的事件通知](event-notification-in-directshow.md)
</dt> </dl>

 

 




