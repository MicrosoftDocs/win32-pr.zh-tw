---
description: 表示特定 DVD 導覽器命令已完成。
ms.assetid: f460db8e-b966-41fa-bfa1-4ad3fa65c3e3
title: 'EC_DVD_CMD_END (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CMD_END
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 550a3969ba431127b05234a0c9fe38eb5938ebf2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998710"
---
# <a name="ec_dvd_cmd_end"></a>EC \_ DVD \_ CMD \_ END

表示特定 DVD 導覽 [器](dvd-navigator-filter.md) 命令已完成。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

命令識別碼。 將此參數傳遞給 [**IDvdInfo2：： GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) 方法，以取得 [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) 介面指標。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

**HRESULT** 值，指出命令的狀態。

</dd> </dl>

## <a name="remarks"></a>備註

只有當您的應用程式 \_ \_ \_ 在採用 [**dvd \_ cmd \_ 旗標旗標**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags)的 [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)方法中設定 DVD cmd 旗標 SendEvents 旗標時，才會引發此事件。

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

[同步處理 DVD 命令](synchronizing-dvd-commands.md)
</dt> </dl>

 

 




