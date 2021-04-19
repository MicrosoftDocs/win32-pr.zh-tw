---
description: 指示 DVD 播放程式在 DVD \_ 網域標題網域中開始播放新程式 \_ 。
ms.assetid: c0745615-d527-4d93-9118-30419c6c811e
title: 'EC_DVD_CHAPTER_START (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CHAPTER_START
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 87a4408f1631d8a23cf42e790688856d6c246393
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990107"
---
# <a name="ec_dvd_chapter_start"></a>EC \_ DVD \_ 章節 \_ 入門

指示 DVD 播放程式在 DVD \_ 網域標題網域中開始播放新程式 \_ 。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**DWORD** 值，指出新的章節 (程式) 號碼。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

零個。

</dd> </dl>

## <a name="remarks"></a>備註

只有簡單的線性電影會發出此事件的信號。

此事件會在標題網域中引發。

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
</dt> <dt>

[**DVD \_ 網域列舉**](/windows/win32/api/strmif/ne-strmif-dvd_domain)
</dt> </dl>

 

 




