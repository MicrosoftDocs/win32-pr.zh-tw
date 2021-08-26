---
description: 發出 DVD 警告條件的信號。
ms.assetid: d7221e8a-089f-4eaf-a193-548709c14336
title: 'EC_DVD_WARNING (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_WARNING
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: a2f2d604b46a4c4bc2213fe74210defdf408336b69218589ff42209cebe025e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965558"
---
# <a name="ec_dvd_warning"></a>EC \_ DVD \_ 警告

發出 DVD 警告條件的信號。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

指出警告條件的 **DWORD** 值。 [**DVD \_ 警告**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_warning)列舉資料類型的成員。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

如果 *pParam1* 等於 DVD \_ 警告 \_ 開啟、DVD \_ 警告 \_ 搜尋或 dvd \_ 警告 \_ 讀取，則 *lParam2* 包含最後從 **GetLastError** 傳回的錯誤碼。

</dd> </dl>

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

 

 




