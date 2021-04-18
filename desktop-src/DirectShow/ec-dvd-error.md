---
description: 發出 DVD 錯誤狀況信號。
ms.assetid: 2cd3e0c4-e2b7-4aa1-9f3c-9003eabfb08a
title: 'EC_DVD_ERROR (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ERROR
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 3b338889836bf78a334784ea66c0e346e9f6b672
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989553"
---
# <a name="ec_dvd_error"></a>EC \_ DVD \_ 錯誤

發出 DVD 錯誤狀況信號。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

表示錯誤狀況的 **DWORD** 值。 [**DVD \_ 錯誤**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error)列舉資料類型的成員。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

意義取決於 *lParam1* 的值。 如需詳細資訊，請參閱 [**DVD \_ 錯誤**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) 。

</dd> </dl>

## <a name="remarks"></a>備註

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

 

 




