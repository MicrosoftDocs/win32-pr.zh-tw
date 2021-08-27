---
description: 表示 IDvdControl2 介面方法的可用集合已變更。
ms.assetid: dfe698b9-abe5-44a7-9844-f408f11fd0ce
title: 'EC_DVD_VALID_UOPS_CHANGE (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VALID_UOPS_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: fafdbb5443a32a8029ad73d92a2b23c5f05c96d5dfc32375fd05e6d4502484a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051808"
---
# <a name="ec_dvd_valid_uops_change"></a>EC \_ DVD \_ 有效 \_ UOPS \_ 變更

表示 [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) 介面方法的可用集合已變更。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**DWORD** 值，包含來自 [**有效 \_ UOP \_ 旗**](/windows/win32/api/strmif/ne-strmif-valid_uop_flag) 標列舉的零或多個旗標組合。 這些位會指出 DVD 光碟明確停用的 [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) 命令。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

零個。

</dd> </dl>

## <a name="remarks"></a>備註

此事件表示 DVD 光碟上的內容只會明確停用的作業。它不保證呼叫未停用的方法是有效的。 例如，如果沒有任何按鈕， [**IDvdControl2：： ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton) 方法將無法運作，即使方法未明確停用也是一樣。

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

 

 




