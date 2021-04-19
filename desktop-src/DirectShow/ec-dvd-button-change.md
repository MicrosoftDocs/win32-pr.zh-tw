---
description: 表示 DVD 功能表按鈕的數目已變更，或按鈕選取範圍已變更。
ms.assetid: af6c841d-ca06-4535-b418-14409fa78c81
title: 'EC_DVD_BUTTON_CHANGE (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BUTTON_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 8647c1100e5cca6897e2068b2a20119a8f047396
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995999"
---
# <a name="ec_dvd_button_change"></a>EC \_ DVD \_ 按鈕 \_ 變更

表示 DVD 功能表按鈕的數目已變更，或按鈕選取範圍已變更。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**DWORD** 值，表示可用按鈕的數目。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

**DWORD** 值，指出目前選取的按鈕數目。 選取的按鈕數位零表示未選取任何按鈕。

</dd> </dl>

## <a name="remarks"></a>備註

按鈕編號的範圍為1到36。

目前選取的按鈕可以使用在光碟上撰寫的流覽命令，以及透過使用 [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) 介面的應用程式控制，自動變更。

此事件可以通知任何可用的按鈕編號。 這些數位不一定會對應到用於 [**IDvdControl2：： SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton) 的按鈕編號，因為該方法只能啟用按鈕的子集。

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

 

 




