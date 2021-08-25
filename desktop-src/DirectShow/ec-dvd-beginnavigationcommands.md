---
description: 在一組 DVD 流覽命令開始時傳送。
ms.assetid: 9cdcb211-a9e3-4a15-81bd-7ada2b9d823a
title: 'EC_DVD_BeginNavigationCommands (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BeginNavigationCommands
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: e0c39b43fc29ed5fadcac0e85ff23ef9f1945a25e26bcfdb0f1e81f804abbc07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965898"
---
# <a name="ec_dvd_beginnavigationcommands"></a>EC \_ DVD \_ BeginNavigationCommands

在一組 DVD 流覽命令開始時傳送。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

來自 [**DVD \_ NavCmdType**](/windows/win32/api/strmif/ne-strmif-dvd_navcmdtype) 列舉的值。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

零個。

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

 

 




