---
description: EC_DVD_VOBU_Offset-當 DVD 導覽器剖析 PCI 封包時傳送。
ms.assetid: e2e65007-7c34-4be4-86b9-9491061891e5
title: 'EC_DVD_VOBU_Offset (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VOBU_Offset
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c680aa8a4e4df63286f4ca5e5b73adb5de038324708dff4c0aab386b39d0f65d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119316808"
---
# <a name="ec_dvd_vobu_offset"></a>EC \_ DVD \_ VOBU \_ 位移

當 DVD 導覽 [器](dvd-navigator-filter.md) 剖析 PCI 封包時傳送。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

最新影片物件單位的區塊位移 (VOBU) 。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

目前的影片標題集號碼 (VTSN) 。

</dd> </dl>

## <a name="remarks"></a>備註

此事件預設為停用。 若要啟用此事件，請呼叫 [**IDvdControl2：： SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) ，並將 **DVD \_ EnableLoggingEvents** 選項設定為 **TRUE**。

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

 

 




