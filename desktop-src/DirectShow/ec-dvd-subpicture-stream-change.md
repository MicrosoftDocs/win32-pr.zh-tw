---
description: 表示主要標題的目前子圖片串流號碼已變更。
ms.assetid: b6da3201-55df-47dc-ad4f-5cd2e78073ee
title: 'EC_DVD_SUBPICTURE_STREAM_CHANGE (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_SUBPICTURE_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 21549ec6427b82c6d229d2e3962689bc8879815429f3a68fd32d54283c30d6a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639768"
---
# <a name="ec_dvd_subpicture_stream_change"></a>EC \_ DVD \_ 子圖片 \_ 串流 \_ 變更

表示主要標題的目前子圖片串流號碼已變更。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**DWORD** 值，指出新的使用者子圖片串流號碼。 子圖片資料流程數位的範圍是從0到31。 Stream 0xFFFFFFFF 表示未選取任何資料流程。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

指出子圖片開啟/關閉狀態的布林值。

</dd> </dl>

## <a name="remarks"></a>備註

子圖片可使用在光碟上撰寫的流覽命令，以及透過使用 [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)的應用程式控制，自動變更。

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

 

 




