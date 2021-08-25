---
description: 表示 DVD 播放機的新網域。
ms.assetid: 4faa46d6-2ba2-44a3-b237-acac3b32f8b1
title: 'EC_DVD_DOMAIN_CHANGE (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_DOMAIN_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: a43c44e779d8ad64852b673fb053467687c50daec85acb9bc87999675200d5f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965658"
---
# <a name="ec_dvd_domain_change"></a>EC \_ DVD \_ 網域 \_ 變更

表示 DVD 播放機的新網域。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

表示新網域的 **DWORD** 值。 [**DVD \_ 網域**](/windows/win32/api/strmif/ne-strmif-dvd_domain)的成員列舉資料類型。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

零個。

</dd> </dl>

## <a name="remarks"></a>備註

只要 DVD 播放機變更網域，就會對此事件發出信號。

此事件會在所有 DVD 網域中引發。

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

 

 




