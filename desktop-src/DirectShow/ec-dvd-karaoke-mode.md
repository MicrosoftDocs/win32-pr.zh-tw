---
description: 表示 DVD 導覽器已開始播放或完成播放卡拉卡拉卡拉的資料。
ms.assetid: 910bf809-a56a-4d02-9c7e-429769a4ec2b
title: 'EC_DVD_KARAOKE_MODE (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_KARAOKE_MODE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: e4edbdb337c4b57a7ed09bd63a8ed4fb0d1946b289b369badab64b561000d3e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928568"
---
# <a name="ec_dvd_karaoke_mode"></a>EC \_ DVD \_ 卡拉卡拉 \_ 模式

表示 DVD 導覽 [器](data-flow-in-the-dvd-navigator.md) 已開始播放或完成播放卡拉卡拉卡拉的資料。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

布林值。 若 **為 TRUE**，表示現正播放卡拉卡拉軌。 否則，就不會播放任何的卡拉 ok 曲目。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

保留的。

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

 

 




