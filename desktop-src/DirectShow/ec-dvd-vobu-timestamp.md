---
description: 當 DVD 導覽器剖析 PCI 封包時傳送。
ms.assetid: 25548c23-22f0-47cb-9062-273ad39d3007
title: 'EC_DVD_VOBU_Timestamp (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VOBU_Timestamp
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 762a900a83154ce38ee00fcf4173ebc32b41cf30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975990"
---
# <a name="ec_dvd_vobu_timestamp"></a>EC \_ DVD \_ VOBU \_ 時間戳記

當 DVD 導覽 [器](dvd-navigator-filter.md) 剖析 PCI 封包時傳送。

事件資料是最新影片物件單位的時間戳記 (VOBU) 。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

包含時間戳記的低序位 **DWORD** 。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

包含時間戳記的高序位 **DWORD** 。

</dd> </dl>

## <a name="remarks"></a>備註

此事件預設為停用。 若要啟用此事件，請呼叫 [**IDvdControl2：： SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) ，並將 **DVD \_ EnableLoggingEvents** 選項設定為 **TRUE**。

重建時間戳記，如下所示：


```C++
LARGE_INTEGER li;
li.LowPart = DWORD( lParam1 );
li.HighPart = DWORD( lParam2 );
```



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

 

 




